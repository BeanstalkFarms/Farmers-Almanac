# BIC Process

**This document can be found on Arweave** [**here**](https://bean.money/bic-process)**.**

The **Beanstalk Immunefi Committee**, **or BIC**, determines the categorization and payout of bug bounties in accordance with the bug bounty program structure approved by the Beanstalk DAO.

The Immunefi Bug Bounty Program is primarily focused preventing loss of Farmers' Beanstalk assets in Beanstalk and other ecosystem smart contracts.

You can read more about the current BIC Members and data on past Beans minted for bounties on the [BICM Dashboard](bicm-dashboard.md) in the Farmers' Almanac. All Immunefi bug reports and their responses are logged [here](https://community.bean.money/bug-reports).

## Immunefi Program

You can read the full program and submit bug reports on the [Immunefi Bug Bounty Program](https://immunefi.com/bounty/beanstalk) page. The latest version of the program approved by the DAO can be found on Arweave [here](https://arweave.net/ddA6z28UiKLkxfAv-VcNPP\_fEcjAZs7jII7iZfgMdu0).

In summary:

* The max bounty is 1,100,000 Beans;
* Bugs are categorized as Critical, High or Medium severity;
* The BIC determines whether a whitehat is entitled to a bug bounty/reward, and if so, the amount of such bounty/reward according to the defined bug bounty program structure; and
* Immunefi serves as a mediator in cases where a whitehat disputes the BIC's determination of whether the whitehat is entitled to any bug bounty/reward, or what the appropriate bounty/reward should be within each Impact range.

Security is paramount to the success of Beanstalk. Immunefi is crypto's leading bug bounty platform that many other well-known DeFi protocols use to facilitate their bug bounty programs. This bounty program is competitive with the largest programs currently on Immunefi.

This program establishes a method for the reporting and fixing bugs in a way that minimizes the risk to Beanstalk (and other ecosystem contracts) between the report and the fix, as well as the fair and transparent compensation for the reporting of bugs. The program gives bounty hunters a clear process and structure in order to increase the likelihood they attempt to find issues with Beanstalk and its related contracts and code.

The BIC structure of community-known members (see [BICM Dashboard](bicm-dashboard.md)) and public Snapshot proposals (see [Beanstalk Bug Bounty Snapshot space](https://snapshot.org/#/beanstalkbugbounty.eth)) allows the Beanstalk community to scrutinize decisions, while still allowing the BIC to move swiftly in response to bug reports. The BIC consists of technical members of the Beanstalk community due to the nature of the BIC. The BIC can keep the bug information private while the bug is unfixed, and then has a clear process to disclose the bug to the public and compensate the whitehat.&#x20;

Having several members on the BIC and requiring a majority vote to execute bug bounty payments increases decentralization.

## Responsibilities

The BIC has the following primary responsibilities:

* Following the processes outlined in [#response-process](bic-process.md#response-process "mention"); and
* Updating the Immunefi Bug Bounty Program when necessary.

The BIC may update the Immunefi Bug Bounty Program without a proposal in the following cases:

* Adding/removing assets as in scope, particularly adding contracts that have been audited and/or have attracted large amounts of Beans/BDV;
* Adding/removing impacts as in scope;
* Adding/removing rules to the Out of Scope section;
* Adding documentation and links; and
* Updating language to improve clarity.

Any other changes to the Immunefi Bug Bounty Program require a BOP (or BIP).

## Changing Members

In the event that one or more members are deemed unfit for the BIC (or a member voluntarily chooses to be removed), the BIC will rotate them out and replace them with a backup member approved by the DAO (no Snapshot proposal required).

## Response Process

The following outlines the process that the BIC follows upon receipt of a bug report.

### Immediate Response

After a bug report is submitted through the Immunefi Dashboard, all BIC Members are notified via email.

As mentioned in the bug bounty program, in order to be considered for the maximum potential reward, bug reports must come with a Proof of Concept (PoC).

In response to each bug report, the BIC will immediately evaluate the validity and severity of the bug, as well as the PoC if included in the bug report.

### Bug Fix

If it is determined that the bug report is invalid, the BIC will close the report on the Immunefi Dashboard. BIC responses to all bug reports are logged [here](https://community.bean.money/bug-reports).

If it is determined that the bug report is valid, the BIC will work with the corresponding party (the [BCM](bcm-dashboard.md), etc.) to resolve the issue as soon as possible via an emergency upgrade. The fix will be forwarded to an auditor for review, if applicable.

For Beanstalk and Basin UI bug reports, the BIC will work with Beanstalk Farms to resolve the issue.

### BIR Proposal

As soon as possible after completing the above, the BIC will prepare, but not publish, a BIR, which includes:

* Whether the bug report qualifies for a Critical, High or Medium Impact bounty/reward;
* What the potential practicable economic damage of the bug is (if categorized as Critical or High Impact);
* What the appropriate bounty/reward should be within the Impact range; and
* Whether the whitehat is entitled to a bug bounty/reward, and if so, the amount of such bounty/reward.

In instances where there are multiple bugs reported in the same report, a BIR will be prepared for each bug.

Before a BIR is proposed, its contents are confirmed with the submitter of the bug report via the Immunefi platform. As outlined in the bug bounty structure, in certain instances where the submitting party disputes the BIC’s proposal, Immunefi mediates.

If the bounty/reward is less than 50,000 Beans, the BIC may pay the bounty without formally voting on the BIR on Snapshot.

If the bounty/reward is greater than or equal to 50,000 Beans, as soon as possible after the implementation of a fix by the BCM, the BIC will:

* Publish the BIR to Snapshot;
* Announce the existence of the BIR to the Beanstalk community via the Discord; and
* Vote on the BIR.

BIR voting takes place on the [Beanstalk Bug Bounty Snapshot space](https://snapshot.org/#/beanstalkbugbounty.eth) and lasts for 3 days. Only BIC members propose and vote on BIRs, and each member has one vote. BIC members can either vote For or Against a BIR, and a majority of the BIC voting For is required to pass.

### BIR Exection

Once a BIR passes, the BICM executes it by:

* Transferring Beans from the BICM to the [Immunefi Vault](https://immunefisupport.zendesk.com/hc/en-us/articles/18233838041745-Vaults-System), if necessary and to the extent that Beans remain available in the BICM; and
* Transferring Beans in the Immunefi Vault to the submitting party’s address.
