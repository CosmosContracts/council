# Withdraw unstacked JUNO from canceled vesting contracts

## On-chain Proposal example text

Following on our Proposal [`[proposal:id]`](`[proposal:link]`) to unstake the JUNO in our canceled vesting contracts (currently [cw-vesting v2.1.0](https://crates.io/crates/cw-vesting/2.1.0)), each contract has now a liquid (unbonded) balance that we can withdraw:

- `[contract:label]` (optional: `[contract:recipient:human_friendly_label]`), `[contract:address]`: `[contract:address:balance]`

To send it back to our treasury, we must execute its `withdraw_canceled_payment` function, that according to the [contract code](`[contract:offchain_code_repo:url]#L[function:line_number_anchor]`), should send the requested amount to the owner (our account).

## On-chain Execution messages

// This is using DAODAO UI notation, #TODO generalized version
Execute smart contract:
- `[contract]`:
  ```language=json
  {
    "withdraw_canceled_payment": {
      "amount": "[contract:address:balance]"
    }
  }
  ```

## Explanation

To withdraw everything, you should request the amount returned from the query balance of each address:

- `[contract]`:
  query: `junod q bank balances [contract:address]`
  response:
    ```
    balances:
    - amount: "[integer_amount_as_string]"
      denom: `[token:id]`
    ```
Example `[token:id]`'s are: `ujuno` (native coin label), `factory/[contract:address]/[token:label]` (token-factory token).

You could also verify that the `owner` of the contract is your account:
- `[contract]`:
  query: `junod query wasm contract-state smart [contract:address] '{"ownership": {}}'`
  response:
  ```
  data:
    owner: [owner:address]
  ```

Finally, the contract might have a `distributable` amount (#TODO explanation):
- `[contract]`:
  query: `junod query wasm contract-state smart [contract:address] '{"distributable": {}}'`
  response:
  ```
  data:
    owner: "[integer_amount_as_string]"
  ```

## TODO
Open questions:
1. How to verify the relevant on-chain contract code?
2. Can there be a different owner (ie. NOT the DAO/account who started the vesting contract)?
3. Why is daodao.zone showing the cancelled vesting contract on our DAO page, even if we aren't the owners?
4. Given that the vesting has been cancelled and the vestee has already withdrawn, why is the `distributable` still there, and if it's really distributable, where is going to go?
