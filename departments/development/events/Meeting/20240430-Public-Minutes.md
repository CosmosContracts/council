# Juno Dev Dept Meeting Minutes - April 30th, 2024 14:30UTC
## Public Meeting

- **Location:** [Public Meeting Location](https://discord.com/channels/816256689078403103/1195704025664978966)
- **Participants:**
  - [ ] @JakeHartnell (Meow)
  - [x] @poroburu
  - [x] @Dat-Andre
  - [x] @kopeboy (Lorenzo)
  - [x] @rayraspberry

- **Contact:** [Juno Development Department Contact Form](https://forms.gle/rzCphth2rTPjKzum9)
- **Chair:** @Dat-Andre
- **Secretary:** @rayraspberry

- **Recording:** [Craig Recording](https://craig.horse/rec/M68BHHeeT2XJ?key=aeXyWQ)

1. Approve Previous Minutes
    - [x] [April 23rd, 2024](./20240409-Meeting-Internal-Minutes.md)
      - Submitted to Github and Approved
        - Discussion on the minutes submission and approval process
    
2. Working Group Updates
    - 🤝 **Vesting** 🤝 @kopeboy
      - Vesting Proposal PASSED AND EXECUTED: [DAODAO Proposal A21](https://daodao.zone/dao/juno1gyjl26rnqqyk6cuh6nqtvx8t885jgqagusvpqpvtgaygcjg2wjdqz0rzle/proposals/A21)
      - Reclaimation of Noah and Reece vesting went as expected
        - A: owner_withdrawable (Noah + Reece cancelled vestings) = 279972002399 + 269405058498
        - B: distributable (Noah + Reece) = 11899853118 + 2987144427
        - C: Previous Dev Dept Treasury = 469685648344
        - D: Current treasury = 1004218650799
          => D - C - B - A ≈ 0
        - Open points (asked to Jake in DM & in DAODAO Discord server): 
          - clarify why the difference is 47 JUNO (not zero)
          - how did WYND Foundation contract had a different owner?
          - DAO Vestings tab doesn't update the list of owned contracts
      - Wynd Contract
        - Development Department is not the owner
        - Executed Withdrawal
        - The Juno did not go to dev department treasury, but to to the vesting contract owner
          - OWNER ADDRESS: `juno1j6glql3xmrcnga0gytecsucq3kd88jexxamxg3yn2xnqhunyvflqr7lxx3`
          - Core1 SubDAO treasury
          - [Core1 SubDAO](https://daodao.zone/dao/juno1j6glql3xmrcnga0gytecsucq3kd88jexxamxg3yn2xnqhunyvflqr7lxx3/proposals)
        - @kopeboy contacted DAODAO and @JakeHartnell regarding the discrepency
      - Return Vesting to Council after the Budget
    - 🤝 **Github Ownership** 🤝 @kopeboy + @rayraspberry
       - @rayraspberry contacted @blockcreators on telegram: NO ANSWER after 1 week+
       - Asset Management temporary file: [hackMD](https://hackmd.io/xaRvq0BgT3yJ6cUhnhg6zg)
       - Ray will take the issue up to the council
       - @poroburu, @Dat-Andre, @kopeboy agree sufficient time has been provided
       - @rayraspberry will attempt to contact @blockcreators again this week
    - 🤝 **Critical Infrastructure** 🤝 @Dat-Andre
      - Comms is now using github as the source material but there is reference
    - 🤝 **Budget & Treasury** 🤝 @rayraspberry
      - Council Meeting on Budget tomorrow, April 24th, 2024
      - Waiting on Operations to submit the Council budget proposal
      - Dev Department will return the current treasury to the council
      - @rayraspberry notified Cristiano from Operations regarding this change
    - 🤝 **Department Policies** 🤝
      - [closed as of last meeting]
      - @poroburu says he prefers github over discord for coordinating policy work
    - 🤝 **Conflict of Interest Policy** 🤝 @kopeboy
      - **REFERENCE**: [Draft Policy](https://github.com/CosmosContracts/council/pull/17)
      - Updated procedures
      - Using DAODAO Press Features
        - DAODAO can be used for members to update their conflict of interests
          - Immutable information regarding the conflict of interest is placed in an NFT
      - No feedback from Operations department
      - Procedure Overview
        - @rayraspberry: The conflicts of interest should not be editable by the Council or Department members because they are potential subject of Conflict of Interest inquiries. 
        - Clarify shortcomings of implementations
      - @Dat-Andre : public v private - delegates should be open to criticism / attacks
      - @poroburu : positions should be open to public scrutiny
    - 🤝 **Development Relations** 🤝 @poroburu
      - No Update
    - 🤝 **Asset Management** 🤝 @poroburu
      - **RESOURCE**: Temporary File: [hackMD](https://hackmd.io/xaRvq0BgT3yJ6cUhnhg6zg)
      - **RESOURCE**: [Asset Management Discord Group](https://discord.com/channels/816256689078403103/1218394733705953411)
    - 🤝 **Internal Tooling** 🤝
      - No Updates

1. Review responses to Dev Department Contact Form
 - No new messages

1. Juno Havling Website
  - [ ] @kopeboy will place the code in the Documentation Repository

1. Darkside Podcast Response
  - Email was not delivered, reply email / domain was not valid

1. Juno.tools
  - waiting on the budget 

1. Support RFP
  - Two weeks for the proposal presentation window.
  - tentatively 16:00 (4pm) UTC Thursday May 2nd - dApp proposal
  - tentatively 18:00 (6pm) UTC Friday May 3rd - Blockchain Engineer
  - publish: 
    - Blockchain - submitted via form, upload submissions in markdown in the Github
      - `/council/departments/development/rfp/001-Blockchain_Maintenance_Provider`
    - dApp - submitted via email, upload submission in Github 
      - `/council/departments/development/rfp/003-dApp_Development_Support`
  - create:
    - Commonwealth Post for each Submission

1. RFP Presentation Meeting Structure [45 minutes in total]
  1. Introduction to Juno Request (Dev Department) [5 minutes]
    1. Submissions received, accepted, rejected
  2. Candidate Presentation (Candidate) [ 20 minutes ]
  3. Open for Questions for Department or Public [ 20 minutes ]
  4. Announcement Commonwealth Discussion to Open Afterwards

1. @kopeboy RFP Presentation Preparation
  - [ ] Create Template for Response
  - [ ] Send Email to Confirm Meeting Times with Submittors
  - [ ] Receive Confirmation from Submittors
  - [ ] Publish Submissions to Github @Dat-Andre
  - [ ] Contact Communications to Send Out Announcements of Meetings
  - [ ] Create Discord Events

1. Council Meeting Meeting Preparation - May 2nd 2024 14:00 UTC
  - DAODAO Vesting
  - 

1. Github Dev Department Structure Organization
  - remove from future agenda

1. Proposal to Create Osmosis Address for Council
  - @kopeboy will put Dev Dept Proposal Up

1. PUBLIC COMMENT
  - returniflost: 
    - Wrappr (Legal Wrappr entity in CosmWasm)
      - Neutron DAO + Wrapper are interested in supporting this effort
      - Would appreciate Feedback
    - Custom Treasury Implementation
      - purpose: to mitigate SPAM / unsolicited tokens being sent to the treasury
    - LEXDAO and Kali DAO
      - Recardian Mint
      - On-chain signature represents the keyholder
