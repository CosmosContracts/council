# Conflict Of Interest policy (draft proposal)

1. Any Juno Council Department member should disclose immediately or as soon as it becomes relevant, if he has any potential Conflict Of Interest (COI), defined as:

    1. on-chain compensation from an entity surpassing compensation from the Council, its Departments & SubDAOs, on a monthly basis, excluding staking rewards;
    2. ownership or governance rights of an entity that is entering an agreement with, or receiving any funding, delegation or token from, the Department or its SubDAOs;
    3. direct or indirect control of at least 0.5% of the current total supply of an entity's native token whose trading volume is more than the compensation of all members.

2. Any proposal made by the member to his Department (or any of its SubDAOs) regarding such entities must note the proposer COI in its on-chain text.

3. The member with COI must vote ABSTAIN (or abstain from voting) on Department's (or any of its sub-DAOs') proposals regarding such entities; the member might participate in public discussions regarding such proposals only after remarking his COI. 

4. Members of the Council and its SubDAOs cannot accept gifts and won't individually claim, transfer or use unsolicited airdropped tokens in any way during their mandate.

## Methodology

5. COI as defined above should be disclosed by the subject member with an on-chain text proposal to his Department, titled `COI Disclosure & Acknowledgement` and listing the ID or linked brand name of entities defined above for each month or for an indefinite period: in the latter case, the COI is valid until the member is removed or posts a new COI.

6. Compensations & trading volumes are compared at their single most exchanged pair or route over the last 28 days (UTC closings average price & total volume).

## Monitoring & Consequences

7. To allow "transparency agents" to report undisclosed COI and violations of this policy, the Council must provide a publicly-accessible & free-to-submit `COI Reporting` form:
    1. its submissions should be visible only to Council members (to avoid public defamation) for at least 28 days;
    2. the Council should set its URL as value of a `COI_Reporting` *storage item* on its DAO and link it on a post on its DAO's *Press* page.

8. To incentivise reporters and disincentivize violations, the Council must freeze its compensation to the subject member until relevant submissions are verified, and redirect it to the reporter with a proposal that, when passed, confirms the veridicity of the report.

9. When failing to comply with any of points 1 to 5 above, the member should be removed from the Council, Department and its SubDAOs and stop receiving related compensations.

## Unforeseen conflicts

10. This present policy tries to defend Juno community by prescribing duties for Council members, but it's important to remind that anyone may at anytime submit a Juno Governance Proposal directly to all JUNO stake-holders to report unforeseen conflicts, suggest remedies or improvements, veto or override Council's decisions in general.

---

*The following section is not part of the policy*

## Implementation procedure, example 1

### Pre-requisites
- Council members create the "COI Reporting" form.
- Each Department and the Council DAOs activate the DAODAO's Press widget.
### Activation
- One member proposes the policy to the Council through his Department, by adding its text and the link to the COI Reporting in a Press post (which will mint an NFT to the DAO with the IPFS CID as token ID).
- Optionally, each department's Council Representative collects initial COI Disclosures from his department's members to fill the "Conflict Of Interest Disclosures" post on creation.
- Each Representative (or one of each Department members) creates the "Conflict Of Interest Disclosure" Press post on its Department, in which he links the Council's policy & "COI Reporting" form.
### Monitoring
- Each member updates the "Conflict Of Interest Disclosure" post by listing his current COI disclosures with a proposal to his department titled `COI Disclosure update`, with description `I hereby update my potential conflict of interest disclosures according to our [policy](URL).`
- Anyone submits to the "COI Reporting" form to inform the whole Council of an undisclosed COI or a violation to the policy by a member.
- Any Council member verifies the submission and either does nothing (false or unverifiable) or confirms it by proposing to the Council to freeze the subject member's compensation & redirect it to the reporter.

### On-chain proposal template

**Title:** `Publish our Conflict Of Interest Disclosures` or `COI Disclosure update`
**Description:**
`This creates the post that will be updated by each member's proposal with his new COI disclosures, according to our [policy](URL).`
or
`I hereby disclose my potential conflict of interests according to our [policy](URL):`
**Action:**
`Create Post` or `Update Post`:
_Title_: `Conflict Of Interest Disclosure` (insert or select)
_Description_: `This post contains or links to our official & current Conflict Of Interest (COI) Policy, COI Disclosures from our members, COI Reporting form.`
_Content_:

```
## Conflict Of Interest (COI) policy

This DAO is a member of the Juno Council and adheres to its official [COI policy](URL).

## Current COI disclosures by our members

|COI Definition|Entity|Period|Member|
|-|-|-|-|
1.1 Compensation from|[Company brand name](https://www.company.com/)|indefinite|Member 1 `juno1__MEMBER_ADDRESS__`|
1.1 Compensation from|[DAO name](https://explorer.com/wasm/contract/[dao:address])|Jan-June 2024|Member 2 `juno1__MEMBER_ADDRESS__`|
1.2 Rights on receiver|[Chaintools validator](https://www.mintscan.io/juno/validators/junovaloper1dru5985k4n5q369rxeqfdsjl8ezutch8mc6nx9)|indefinite|Member 3 `juno19nt2pfvcrpsgasm2rv2mpalsd52hq69tyhyfn8`|
1.3 Significant share of|[WOSMO DAO](https://daodao.zone/dao/osmo1elw4psm8sddcvu8fsdx3hs0zkctcdzwu8qspuxzthepc6ev55c8qvp08u6/treasury)|indefinite|Member 3 `juno1__MEMBER_ADDRESS__`|

## How to report undisclosed COI

After having read the policy and the disclosures above, please report any violation or undisclosed COI from our [members](https://daodao.zone/dao/[dao:address]/members) with [this form](coi_reporting:form:url). Submissions will be visible only to the Council's members until they are verified, published & rewarded with an on-chain proposal to the Council.
```

## Implementation procedure, example 2

An alternative implementation (without using the DAODAO UI's Press feature) would be to directly (manually) upload the policy and each member's disclosures on IPFS and add their Content IDs (CID) to either the corresponding proposals' text or as storage items on each DAO account.
To decentralize the COI Reporting steps instead, one would need to create a specific contract on-chain (but it's still unclear what would be the best way to make submissions visible only to the Council members to avoid public defamation).


## Rationale

The Juno community is sovereign but has delegated some power to the Council by approving [Proposal #319](https://www.mintscan.io/juno/proposals/319). Since Council members might temporarely use that power to their own exclusive or disproportionate advantage, the Charter already included a [Conflict of interest section (V.9)](https://hackmd.io/@G2q75faESMyRkexdnhUCpA/B1NPVxxRh#Section-V9-%E2%80%94-Conflicts-of-Interest). Unfortunately that is a bit unclear and does not include prevention nor remediation procedures.

I suggest we introduce a common policy for all Departments to avoid or reduce potential conflict between the members' special interests & the community, providing more clarity than what's already in the Charter and a real implementation.

This should not discourage participation in the Council, but only provide honest members with peace of mind and the ability to prevail over grifters with their vote.

## Simulations of policy application

1. **DAO-JUNO token swap**
The swap was approved by the community with [Juno Gov Prop#285](https://www.mintscan.io/juno/proposals/285). The funds were sent to the Juno Growth Fund (JGF), which used them to create a vesting payment to DA0DA0 with [Prop#A15](https://daodao.zone/dao/juno1xz54y0ktew0dcm00f9vjw0p7x29pa4j5p9rwq6zerkytugzg27qs4shxnt/proposals/A15). Since JGF isn't a SubDAO of a Council Department, this agreement wouldn't be subject to COI. **What if JGF was a SubDAO of a Council Department?**
    - If Rarma, the proposer, had COI with DA0DA0, he should have disclosed it in propA15 and abstained. The vote would have reached the quorum and passed anyway.
    - If at least 50% of members of JGF had COI with DA0DA0, the vote shouldn't have passed, and the vesting payment shouldn't have started. Otherwise, this could lead the Council or Community (with a Juno Gov Prop) to use the COI policy as a valid argument to stop the vesting and remove the members with COI that activated it.
    - Anyone could report undisclosed COI between DA0DA0 and JGF members during the 12 months of vesting. If such report is confirmed by the Council:
        - the vesting should be canceled (signaling a COI) and the member(s) removed
        - the JUNO equivalent vested last month & going to members with COI should be sent to the "transparency reporter"
        - the remaining vesting could restart with a new proposal following COI policy

2. **DEX RFP**
A Request For Proposal (RFP) about a comunity-owned DEX on Juno was [published](https://x.com/JunoNetwork/status/1761029221378371784). 
    > Ops department wants to preselect the team with the best proposal (based on price-performance ratio) and then wants to seek approval from the community to get funding for this grant.

    If the Operations Department will pay the selected team directly, their members could be subject to this COI policy. If they have ownership or governance rights of the receiving entity, they should disclose it as in [Methodology](#Methodology) & abstain from relevant spend proposals.

3. **Delegation program**
The Operations Department might delegate [~6M JUNO](https://hackmd.io/@G2q75faESMyRkexdnhUCpA/B1NPVxxRh#Existing-Treasuries-amp-SubDAOs) through its [Delegations SubDAO](https://daodao.zone/dao/juno1mjsgk02jyn72jm2x7fgw72uu9wj7xy0v6pnuj2jd3aq7rgeqg5qq4dnhes/subdaos). According to this policy (1.2), an Ops. Dep. member would be subject to COI if he has ownership or governance rights in a Validator receiving a delegation from the SubDAO.
The COI member should abstain from voting on such proposals. If a majority is unable to form (because of COI on ≥50% of members), such proposals could be voted on the Council or Juno Governance (by the community at large), leaving the Delegation SubDAO only the duty of providing the rationale and information to suggest such delegations.

4. **Hypothetical collusion between members**
TODO for a future version because it's not simple to write a rule on this that doesn't add significant liabilities to all Council members.

    For example, here's a point I was trying to add:
    > Collusion: in case a Department’s or its SubDAOs’ proposal creates a new COI (which is not already noted on the proposal’s text) to another member, proposer & subject must both vote ABSTAIN, and the subject must disclose his COI before the proposal's veto lock expires.


## Relevant reads

[A comparative analysis of financial disclosure obligations on members of parliaments:](https://www.europarl.europa.eu/RegData/etudes/STUD/2023/747911/EPRS_STU(2023)747911_EN.pdf)
> 1. all EU Member States currently impose financial disclosure obligations on the members of their national parliaments
> 2. all Member States require them to disclose that information shortly after taking up their duties and to update it either at regular intervals or when the situation has changed
> 3. 19 out of 27 Member States ensure the declaration(s) provided by members of parliament are made public through unrestricted access via the internet. A few have opted for a different solution, providing access to declarations only on request, or restricting access to relevant parts of the declarations to competent national authorities. 


[Criminal conflict of interest laws:](https://www.oge.gov/web/oge.nsf/0/7646D1C6ECAE9863852585B6005A1A20/$FILE/Criminal%20Conflicts%20of%20Interest%20508.pdf)

> 1. You are prohibited from working on Government matters in which you, your spouse or minor child, or certain others have a financial interest. 
> 2. You may not be paid by someone other than the United States for doing your Government duties.
> 3. You are prohibited from accepting bribes or gratuities to influence your Government actions.
> 4. You are generally prohibited from certain involvement in claims against the United States, or from representing another before the Government in matters in which the United States is a party or has a direct and substantial interest.
> 5. You are prohibited from receiving compensation for representational activities involving certain matters in which the United States is a party or has a direct and substantial interest.
> 6. After you leave Government service (or leave certain highlevel positions), you may be subject to limitations on your post employment activities.
