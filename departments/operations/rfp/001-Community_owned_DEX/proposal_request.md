# Request for Proposal (RFP)

## Juno Network - Community-owned DEX

## Project Overview

The JUNO Operations Departments (Ops) is seeking proposals for teams looking to create a community-owned DEX on Juno.

In particular, Ops is requesting proposals to create a tokenless and permissionless DEX and hand over control to the Juno community. Future maintenance and improvements are not part of RFP_1, and will be published separately.

Ops department wants to preselect the team with the best proposal (based on price-performance ratio) and then wants to seek approval from the community to get funding for this grant.

**We favour cost-efficient proposals and also with regard to necessary audits we prefer to use proven and battle-tested smart contracts.**

## Problem statement

### High level

Juno does currently not have a reputable DEX with a team maintaining it. Therefore the Juno community is forced to swap on other DEXs in the interchain. While Juno does not want to compete as a liquidity hub nor in DeFi, a DEX is seen as a cornerstone of a blockchain by the community and can enable/facilitate other use cases on the chain.

### Requirements

The following requirements were the result of discussions from a Juno Working Group (JWG) and additional community feedback:

- [ ] DEX-type: Standard AMM (there are more efficient DEX-designs, but the community-owned DEX should utilize an easy to understand and well-known model - at least initially)
- [ ] Small Swap Fee: Set fee to 0.2% (100% to liquidity provider) - governance should be able to change this for each liquidity pool individually
- [ ] Fee Distribution: Enable the possibility to split the fee and direct it to different destinations (f.e. 80% to liquidity providers and 20% to community pool)
- [ ] Incentivization: It should be possible to add incentives to a specific liquidity pool. The incentives should be distributed on an ongoing basis until they are exhausted.
- [ ] Permissionless: Everyone can add new liquidity pools and has the ability to add incentives to their LP in order to attract liquidity. Pools should be sorted by the value of its available liquidity (high to low).
- [ ] Tokenless: The DEX is owned by the Juno community and governed by $JUNO - no additional farm token is needed.
- [ ] Possibility to connect to SKIP API: Requirements can be found here: <https://api-docs.skip.money/docs/skip-api-swap-venue-requirements>
- [ ] Frontend:
  - [ ] Keep the UI as simple as possible. Juno users are used to the simplistic UI of Junoswap (<https://junoswap.com/>). You can draw inspiration from it, but their frontend itself is outdated.
  - [ ] Design should be adapted to the official Juno website (<https://junonetwork.io/>) (background images, colors etc.), because we intend to host it as a subdomain.
  - [ ] Safety: Automatic risk indication for tokens ("risky asset") based on parameters defined by the community (to be determined). Parameters could be: local liquidity, cross-chain liquidity and duration of listing and others
  - [ ] Notifications: The user should get clear notifications, when he tries to do a swap in a pool with shallow liquidity (f.e.: “Warning: Liquidity in this pool is low. The price impact of your swap exceeds the current market price by  xx%. Do you really want to execute this trade?”)
- [ ] Hand over ownership to the Juno community

## RFP Details

As noted above, the Ops department is looking for a single team, which creates a tokenless and permissionless DEX and implements the required features (requirements). The final proposal has to be approved by Juno governance, but the selection process is handled by Ops and Ops is your main point of contact.

### Process summary

The entire process can be summarized as follows:

1. Request: Ops releases RFP_1 (this post)
2. Gather: Teams signal their intent to hand in a proposal until the deadline
3. Discuss: Teams can reach out to Ops to discuss any open question and ask for additional resources (information/ documents etc.)
4. Gather II: Teams submit their final proposals before the deadline
5. Deliberate: Ops analyzes proposals, discusses dynamically any suggestions in structure, direction, fee schedule, and/or timeline, and comes up with a plan based on the resources and needs of the accepted proposal(s).
6. Propose: Ops proposes a final structure of the proposal based upon deliberations/discussions.
7. Community Decision: Ops chooses the final proposal and asks for funding from the community
8. Begin: Team accepts and work begins

### Engagement timeline

Ops does not specify a timeline for implementation. However, we ask that you include timelines for all milestones in your proposal and we will take this into account when selecting your offer.

Getting this assignment and doing a good job will increase your reputation in the Juno community and give you an advantage in future RFPs.

### Deliverables

The team is expected to define their own deliverables as a part of scoping the project and give a timeline for their implementation. Requirements of this RFP_1 should be taken into account.

## Bidding instructions

Upon reception of this request, interested Teams are expected to confirm receipt and intention to submit a proposal before submission.

In this confirmation, Teams should explain what they need from Ops in order to make a meaningful proposal. Ops is happy to help get you up to speed via sharing additional resources and/or answering direct questions.

Proposals must be submitted by March 1, 2024.

Please send initial confirmations, and proposals (in PDF format) to one of the following  addresses:
<dimi@junonetwork.io> <cristiano@junonetwork.io> <tank@junonetwork.io> <macks@junonetwork.io>
