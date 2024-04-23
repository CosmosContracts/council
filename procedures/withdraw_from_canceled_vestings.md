# Withdraw unstacked JUNO from canceled vesting contracts

## On-chain Proposal example text

Following on our Proposal [`[proposal:id]`](`[proposal:link]`) to unstake the JUNO in our canceled vesting contracts, each contract has now a liquid (unbonded) balance that we can withdraw:

- `[contract:label]` (optional: `[contract:recipient:human_friendly_label]`), `[contract:address]`: `[contract:address:balance]`

To send it back to our treasury, we must execute its `withdraw_canceled_payment` function, that according to the [contract code](`[contract:verified_offchain_code_repo:url]#L[function:line_number_anchor]`), should send the optional requested amount, or all that's available, to the owner (our account).

## On-chain Execution messages

// This is using DAODAO UI notation, #TODO generalized version
Execute smart contract:

- `[contract]`:

  ```
  {
    "withdraw_canceled_payment": {
      "amount": "[contract:info:data:status:canceled:owner_withdrawable:value]"
    }
  }
  ```

## Explanation

**balance - owner_withdrawable = distributable = vested - claimed**

<details><summary>Contract address balance</summary>
You can get the available amount with the bank query like on any account:
- Query: `junod q bank balances [contract:address]`
- Response:
  ```
  balances:
  - amount: "[integer_as_string]"
    denom: [token:id]
  pagination:
    next_key: null
    total: "0"
  ```

Example `[token:id]`'s are: `ujuno` (native coin label), `factory/[contract:address]/[token:label]` (token-factory token).
</details>

<details><summary>Owner withdrawable, vested, claimed amounts</summary>
You can get those by query the contract info:
- Query: `junod q wasm contract-state smart [contract:address] '{"info":{}}'`
- Response (example with native coin):
  ```
  data:
    claimed: "[integer_as_string]"
    denom:
      native: ujuno
    description: '[vesting_description]'
    recipient: [vesting:recipient]
    slashed: "0"
    start_time: "[timestamp_in_nanoseconds]"
    status:
      canceled:
        owner_withdrawable: "[integer_as_string]"
    title: '[vesting:title]'
    vested:
      constant:
        "y": "[integer_as_string]"
  ```
</details>

<details><summary>Distributable amount</summary>
Finally, there could be some `distributable` amount (vested - claimed) attributable to the vestee, in case he hasn't withdrawn yet:
- query: `junod query wasm contract-state smart [contract:address] '{"distributable": {}}'`
- response: `data: "[integer_amount_as_string]"`

This can be distributed by any account with the permissionless `distribute` execution message.
</details>

Any potential small difference is attributable to ..#TODO.

Before withdrawing, you could also verify that the `owner` of the contract is (still) your account:

- Query: `junod query wasm contract-state smart [contract:address] '{"ownership": {}}'`
- Response:

  ```
  data:
    owner: [owner:address]
  ```

### TODO

1. Why is (balance - owner_withdrawable) *<* distributable? Maybe cause of unregistered slashing?
  (it's slightly less, like 27 JUNO on Noah's vesting, ie. 0.01% of the original total to vest, after 1 year)
2. Verify that the `distributable` is always going to the vestee, especially after cancelation and after he had already withdrawn (when there were staked coins).
3. Why is daodao.zone showing a cancelled vesting contract on a DAO who's not the owner?
4. How to verify the relevant on-chain contract code?
