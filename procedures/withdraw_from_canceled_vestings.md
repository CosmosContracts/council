# Withdraw unstacked JUNO from canceled vesting contracts

## On-chain Proposal example text

Following on our Proposal [`[proposal:id]`](`[proposal:link]`) to unstake the JUNO in our canceled vesting contracts, each contract has now a liquid (unbonded) balance that we can withdraw:

- `[contract:label]` (optional: `[contract:recipient:human_friendly_label]`), `[contract:address]`: `[contract:owner_withdrawable]`

To send it back to our treasury, we must execute the `withdraw_canceled_payment` [function](`[contract:verified_offchain_code_repo:url]#L[function:line_number]`).

You can read the full explanation `[here]([this_procedure_doc:url#explanation])`.

## On-chain Execution messages

(This is using DAODAO UI notation, #TODO generalized msg version)

Execute smart contract:

- `[contract:address]`:

  ```language=json
  {
    "withdraw_canceled_payment": {
      "amount": "[contract:info:data:status:canceled:owner_withdrawable:value]"
    }
  }
  ```

## Explanation

The amount to withdraw is optional; to withdraw everything just execute `{"withdraw_canceled_payment":{}}`.

You may notice that the balance on the `[contract:address]` account is higher. That may be because there is still a `distributable` amount:

**balance - owner_withdrawable = distributable = vested - claimed**

<details>
<summary>Distributable amount</summary>

This is attributable to the vestee, in case he hasn't withdrawn yet:

- query: `junod query wasm contract-state smart [contract:address] '{"distributable": {}}'`
- response: `data: "[integer_amount_as_string]"`

This can be distributed by any account with the permissionless `distribute` execution message.

</details>

<details>
<summary>Contract address balance</summary>

You can get the available amount with the bank query like on any account:

- Query: `junod q bank balances [contract:address]`
- Response:

  ```language=bash
  balances:
  - amount: "[integer_as_string]"
    denom: [token:id]
  pagination:
    next_key: null
    total: "0"
  ```

Example `[token:id]`'s are: `ujuno` (native coin label), `factory/[contract:address]/[token:label]` (token-factory token).

</details>

<details>
<summary>Owner withdrawable, vested, claimed amounts</summary>

You can get these with a single wasm smart query, on the contract's `info` method:

- Query: `junod q wasm contract-state smart [contract:address] '{"info":{}}'`
- Response (example with native coin):

  ```language=bash
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

Any potential small difference is attributable to ..#TODO.

Before withdrawing, you could also verify that the `owner` of the contract is (still) your account:

- Query: `junod query wasm contract-state smart [contract:address] '{"ownership": {}}'`
- Response:

  ```language=bash
  data:
    owner: [owner:address]
  ```

### TODO

1. Why is (balance - owner_withdrawable) *<* distributable? Maybe cause of unregistered slashing?
  (it's slightly less, like 27 JUNO on Noah's vesting, ie. 0.01% of the original total to vest, after 1 year)
2. Verify that the `distributable` is always going to the vestee, especially after cancelation and after he had already withdrawn (when there were staked coins).
3. Why is daodao.zone showing a cancelled vesting contract on a DAO who's not the owner?
4. How to verify the relevant on-chain contract code?
