# Juno Dev Dept Meeting Minutes - April 23rd, 2024

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
      - Created generalized [procedure on Github](https://github.com/CosmosContracts/council/blob/7a64afce765054919062927916927e5bc2565f6a/procedures/withdraw_from_canceled_vestings.md) and recap with the specific data on [HackMD](https://hackmd.io/@kopeboy/r1YkK-b-A).
      - @JakeHartnell to review and approve
        - The withdrawal amount for the owner is not shown in the UI
        - the balance of the contract (what was unstaked) is more than the `owner_withdrawable`, because there is some `distributable` (still going to the vestee, right?)
        - Transferred vesting contracts are not updated automatically on daodao.zone (Max's vesting is still showing in the Dev Dept & not on Comms Dept).
      - Wynd Vesting Contract Owner is `juno1a4pjj5l4szl7kq8u4h07se3675fsqcfh66vtks7hlckgz2kpaq0ssn309f`, ie. not Dev Dept. (check with `junod query wasm contract-state smart juno1a4pjj5l4szl7kq8u4h07se3675fsqcfh66vtks7hlckgz2kpaq0ssn309f '{"ownership": {}}'`)
      - @kopeboy would like @JakeHartnell to be more active on DA0DA0 contracts' issues, but aknowledges he can ask in their Discord server.
      - Vesting Proposal up for vote: [DAODAO Proposal A21](https://daodao.zone/dao/juno1gyjl26rnqqyk6cuh6nqtvx8t885jgqagusvpqpvtgaygcjg2wjdqz0rzle/proposals/A21)
    - 🤝 **Github & ~~Asset Ownership~~** 🤝 @kopeboy + @rayraspberry
       - @rayraspberry contacted @blockcreators on telegram to have a conversation about the ownership of the Github
       - Asset Management temporary file: [hackMD](https://hackmd.io/xaRvq0BgT3yJ6cUhnhg6zg)
    - 🤝 **Critical Infrastructure** 🤝 @Dat-Andre
      - One response for dApp
      - No response for the other 3 RFPs
      - @dat-andre to resubmit the 3 RFPs that received no responses
      - @poroburu bring more engagement to Validators
    - 🤝 **Budget & Treasury** 🤝 @rayraspberry
      - Council Meeting on Budget tomorrow, April 24th, 2024
      - Budget Discussion:
        - #budget-planning
        - Discussion about Highlander 309 in the Comms budget
    - 🤝 **Department Policies** 🤝 [closed]
      - put up templates for the department in Github
      - @rayraspberry to create the templates for outstanding policies
      - close this working group
    - 🤝 **Conflict of Interest Policy** 🤝 @kopeboy
      - @kopeboy will put Policy on Council Github
      - next week bring up at the Council Meeting
      - Cristiano suggested @kopeboy work with Macks from operations
    - 🤝 **Development Relations** 🤝 @poroburu
      - No Update
    - 🤝 **Asset Management** 🤝 @poroburu
      - **RESOURCE**: Temporary File: [hackMD](https://hackmd.io/xaRvq0BgT3yJ6cUhnhg6zg)
      - No Update
      - Andre Offered to Help
    - 🤝 **Internal Tooling** 🤝
      - RFP and Task Management
      - @rayraspberry : should be integrated into existing UX for JunoNetwork.io
      - @poroburu - A simple portal for users - dashboard for Council metrics
      - RFP integration into Website

1. Review responses to Dev Department Contact Form
 - No new messages

1. Darkside Podcast Response
  - Email sent yesterday to Scott

1. Juno.tools
  - @rayraspberry Juno Tools RFP
  - @Dat-Andre work on Asset Management
  - @rayraspberry - Multiple Juno domains and web services shouldn't be running their own hosting services for each

1. New Metric Public Presentation
  - 

1. Juno.Tools
   - **ACTION**
     - [ ] Create RFP to Maintain Juno.Tools

1. Juno Havling Website
  - @kopeboy has the source code for this
  - @Dat-Andre insert the calculation for the halving in the Documentation Repo

1. New Metric Meeting Review
  - @Dat-Andre would be good to understand the project and make other people aware of the project existance

1. Support RFP
  - Private Meeting to Commense after this meeting
  - Public Meeting Posted

1. Contact Approved Submissions for Blockchain Engineer RFP
  - @rayraspberry to put up template for review on Council Github
  - @kopeboy will send out messages to individual parties
  
1. Github Dev Department Structure Organization
   - Will resolve in the Github Issue
    - Public/Stage to Public
    - Remove OTHER Categories

1. Council Meeting Budget Meeting - April 24th, 2024 2:00 PM UTC
 - @rayraspberry previously discussed in this meeting
 - Council Meeting Planning for tomorrow

1. Council Meeting Planning for Thursday May 2nd, 2024 [name=Ray Raspberry]

