# Terms of the Kintsugi proposal to the Community Owned DEX RFP

## Legend

- **Final proposal** = **#TBD**: an NFT referencing an immutable version of the full proposal (same `token_id`), sent by both the *receiver* and the *payer* to each other.
- **Deliverables** = **#TBD**: an NFT referencing an immutable version of all the deliverables (same `token_id`), sent by both the *receiver* and the *payer* to each other.
- **Signatories**:
  - **Payer** = *Council*: `juno1nmezpepv3lx45mndyctz2lzqxa6d9xzd2xumkxf7a6r4nxt0y95qypm6c0`
  - **Receiver** = *Kintsugi*: `osmo1ruxpcljuhpepuw2ywxlqsuhy8u3eulz5hdrsedcvwex8qnsd9yqsqv09j7`
- **Payment Amount denomination(s)** =
  - *USDC* = Noble USDC on Osmosis: `ibc/498A0751C798A0D9A389AA3691123DADA57DAA4FE165D5C75894505B876BA6E4`
- **Technical verification** = **#TBD** an NFT referencing the verified *deliverables* sent from the *verifier* to the *payer*, or *default verification*:
  - Verifier = *Development Department*: `juno1nmezpepv3lx45mndyctz2lzqxa6d9xzd2xumkxf7a6r4nxt0y95qypm6c0`
  - Default verification = **#TBD** 2 weeks after *verifier* is given access to *deliverables* relevant for each payment.

## Payments

### Project Kickstart

Tranche 1 (Initial Payment):

- Upon: *Council* approval of the *final proposal*
- Amount: 13500 *USDC*
- Deadline: none
- Bonus: none
- Malus: none

### MVP

Tranche 2 (Mid Payment):

- Upon: Completion & technical verification of the `MVP Phase` *deliverables*
- Amount: 13500 *USDC*
- Deadline: none
- Bonus: none
- Malus: none

### Final Release

Tranche 3 (Final Payment):

- Upon: Completion & technical verification of all *deliverables*
- Amount: 18000 *USDC*
- Deadline: none
- Bonus: none
- Malus: none

## Jurisdiction

In case of disputes, the *Juno* network community will be the competent court and have the final say by expressing their vote on *Governance* proposals.

*Juno*:

- Chain ID = `juno-1`
- Address prefix (bech32) = `juno`
- Governance = Cosmos SDK `x/gov` module on Juno:
  - address = `juno10d07y265gmmuvt4z0w9aw880jnsr700jvss730`
  - message type = `cosmos-sdk/MsgVote`
- Voters: all JUNO stake-holders (1 JUNO = 1 vote) through *Governance*.

### Disputes

After 2 weeks delay on any payment, a dispute can be opened by either *Signatory* with a public statement.

### Mediation

Both the receiver and the payer can select one independent mediator each that will conduct public meetings on the [Juno Discord server](https://discord.gg/EUGFpdnc) to find resolution agreements. In case mediators are agreed upon before any dispute, they must work towards resolution for at least 4 weeks before a new payment to the *Receiver* is proposed in the *Jurisdiction*.

### Termination

In case a dispute cannot be resolved by a new agreement between *signatories* and the *Juno* court is invoked, this proposal is considered terminated.
