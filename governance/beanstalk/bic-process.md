# BIC Process

**This document can be found on Arweave** [**here**](https://bean.money/bic-process)**.**

The **Beanstalk Immunefi Committee**, **or BIC**, determines the categorization and payout of bug bounties in accordance with the bug bounty program structure approved by the Beanstalk DAO. The [BCM](https://docs.bean.money/bcm-process) executes the will of the BIC as determined by Beanstalk Immunefi Responses (BIRs), up to a maximum number of Beans approved via governance.

The Immunefi Bug Bounty Program is primarily focused preventing loss of Farmers' Beanstalk assets in Beanstalk and other ecosystem smart contracts.

You can read more about the current BIC Members and data on past Beans minted for bounties on the [BIC Dashboard](https://docs.bean.money/almanac/governance/beanstalk/bic-dashboard) in the Farmers' Almanac. All Immunefi bug reports and their response are logged [here](https://community.bean.money/bug-reports).

## Immunefi Program

You can read the full program and submit bug reports on the [Immunefi Bug Bounty Program](https://immunefi.com/bounty/beanstalk) page. The latest version of the program approved by the DAO can be found on Arweave [here](https://bean.money/immunefi).

In summary:

* The max bounty is 1,100,000 Beans;
* Immunefi takes a 10% fee in Beans on top of any bounty;
* Bugs are categorized as Critical, High or Medium severity;
* The BIC determines whether a whitehat is entitled to a bug bounty/reward, and if so, the amount of such bounty/reward according to the defined bug bounty program structure; and
* Immunefi serves as a mediator in cases where a whitehat disputes the BIC's determination of whether the whitehat is entitled to any bug bounty/reward, or what the appropriate bounty/reward should be within each Impact range.

Security is paramount to the success of Beanstalk. Immunefi is crypto's leading bug bounty platform that many other well-known DeFi protocols use to facilitate their bug bounty programs. This bounty program is competitive with the largest programs currently on Immunefi, making it likely to attract whitehat hackers.

This program establishes a method for the reporting and fixing bugs in a way that minimizes the risk to Beanstalk between the report and the fix, as well as the fair and transparent compensation for the reporting of bugs. The program gives bounty hunters a clear process and structure in order to increase the likelihood they attempt to find issues with Beanstalk and its related contracts and code.

The BIC structure of community-known members (see [BIC Dashboard](https://docs.bean.money/almanac/governance/beanstalk/bic-dashboard)) and public Snapshot proposals (see [Beanstalk Bug Bounty Snapshot space](https://snapshot.org/#/beanstalkbugbounty.eth)) allows the Beanstalk community to scrutinize decisions, while still allowing the BIC to move swiftly in response to bug reports. The BIC consists of technical members of the Beanstalk community due to the nature of the BIC. The BIC can keep the bug information private while the bug is unfixed, and then has a clear process to disclose the bug to the public and compensate the whitehat.&#x20;

Having several members on the BIC increases decentralization. The two-thirds majority required to approve a BIR and the BCM minting the Beans introduces multiple steps to mint Beans as a reward, which improves censorship-resistance.

## Responsibilities

The BIC has the following primary responsibilities:

* Following the processes outlined in [#response-process](bic-process.md#response-process "mention"); and
* Updating the Immunefi Bug Bounty Program when necessary.

The BIC may update the Immunefi Bug Bounty Program without a proposal in the following cases:

* Adding new assets as in-scope, particularly contracts that have been audited and/or have attracted large amounts of Beans/BDV;
* Updating the list of pull requests / repositories whose code is in-scope, but has not yet been deployed on-chain;
* Adding documentation and links; and
* Updating language to improve clarity.

Any other changes to the Immunefi Bug Bounty Program require a BOP (or BIP).

## Changing Members

In the event that one or more members are deemed unfit for the BIC (or a member voluntarily chooses to be removed), the BIC will rotate them out and replace them with a backup member approved by the DAO.

## Response Process

The following outlines the process that the BIC follows upon receipt of a bug report.

### Immediate Response

After a bug report is submitted through the Immunefi Dashboard, all BIC Members are notified via email.

As mentioned in the bug bounty program, in order to be considered for the maximum potential reward, bug reports must come with (1) a Proof of Concept (PoC), and (2) code implementing the fix.

In response to each bug report, the BIC will immediately:

* Forward the bug report (and fix PoC if included in the bug report) to an auditor, if applicable; and
* Evaluate the validity and severity of the bug, as well as the fix PoC if included in the bug report.

### Bug Fix

If it is determined that the bug report is invalid, the BIC will close the report on the Immunefi Dashboard. BIC responses to all bug reports are logged [here](https://community.bean.money/bug-reports).

If it is determined that the bug report is valid, the BIC will work with the corresponding party (the [BCM](https://bean.money/bcm-process), the [Root DAO Multisig (RDM)](https://docs.roottoken.org/governance/root-token/rdm-dashboard), etc.) to resolve the issue as soon as possible via an emergency upgrade. The fix will be forwarded to an auditor for review, if applicable.

For Beanstalk UI bug reports, the BIC will work with Beanstalk Farms to resolve the issue.

### BIR Proposal

As soon as possible after completing the above, the BIC will prepare, but not publish, a BIR, which includes:

* Whether the bug report qualifies for a Critical, High or Medium Impact bounty/reward;
* What the potential practicable economic damage of the bug is (if categorized as Critical or High Impact);
* What the appropriate bounty/reward should be within the Impact range; and
* Whether the whitehat is entitled to a bug bounty/reward, and if so, the amount of such bounty/reward.

In instances where there are multiple bugs reported in the same report, a BIR will be prepared for each bug.

After preparing the BIR, the BIC will:

* Confirm the contents of the BIR with the whitehat via the Immunefi Dashboard (as outlined in the [Immunefi Bug Bounty Program](https://immunefi.com/bounty/beanstalk), in certain instances where the whitehat disputes the BIC's determination of the bug report, Immunefi mediates);
* Forward the following information to the BCM (or other applicable multisig) for their submission of the Safe transaction:
  * The whitehat's address;
  * The corresponding bounty amount in Beans;
  * Immunefi's address; and
  * The corresponding fee amount in Beans;
* Include a **Beans Minted** section in the BIR that describes the number of Beans minted by the execution of the proposal;
* Publish the BIR on Snapshot;
* Announce the existence of the BIR to the community in the [Beanstalk Discord](https://discord.gg/beanstalk); and
* Vote on the BIR.

BIR voting takes place on the [Beanstalk Bug Bounty Snapshot space](https://snapshot.org/#/beanstalkbugbounty.eth) and lasts for 3 days. Only BIC members propose and vote on BIRs, and each member has one vote. BIC members can either vote For or Against a BIR, and a two-thirds majority of the BIC voting For is required to pass.

### BIR Execution

Once a BIR passes, the BCM executes it by:

* Minting Beans corresponding to the bounty to the whitehat's address; and
* Minting Beans corresponding to the 10% fee to Immunefi's address.
