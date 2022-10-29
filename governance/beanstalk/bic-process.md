# BIC Process

The **Beanstalk Immunefi Committee,** or BIC, determines the categorization and payout of bug bounties in accordance with the bug bounty program structure approved by the DAO in [BIP-26](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/blob/master/bip/bip-26-bug-bounty-program.md). The [Beanstalk Community Multisig](bcm-process.md) (BCM) executes the will of the BIC as determined by [BIRs](../proposals.md#bir), up to 3,000,000 Beans total.

The bug bounty program is focused on the Beanstalk smart contracts and on preventing loss of user funds.

You can find the bug bounty program and submit bug reports [here](https://immunefi.com/bounty/beanstalk). The program approved by the DAO in BIP-26 can be found [here](https://arweave.net/IFdanx-jNv8VQ2FWRa8tVsvwrPH3coz60S2wAPPm\_Uw).

In summary:

* The max bounty is 1,100,000 Beans;
* Immunefi takes a 10% fee in Beans on top of any bounty;
* Bugs are categorized as Critical, High or Medium severity;
* The BIC determines whether a submitting party is entitled to a bug bounty/reward, and if so, the amount of such bounty/reward according to the defined bug bounty program structure; and
* Immunefi serves as a mediator in cases where a submitting party disputes the BIC’s determination of whether the submitting party is entitled to any bug bounty/reward, or what the appropriate bounty/reward should be within each Impact range.

Read more about the current BIC members [here](bic-dashboard.md).

### Immediate Response

After a bug report is submitted through the Immunefi platform, all members of the BIC are notified via email.

As mentioned in the [program structure approved by the DAO](https://arweave.net/IFdanx-jNv8VQ2FWRa8tVsvwrPH3coz60S2wAPPm\_Uw), in order to be considered for the maximum potential reward, bug reports must come with (1) a Proof of Concept (PoC), and (2) code implementing the fix.

In response to each bug report, the BIC will immediately:

* Forward the the bug report (and fix PoC if included in the bug report) to Halborn via the Audit Slack channel, and the BCM; and
* Evaluate the validity and severity of the bug, as well as the fix PoC if included in the bug report.

### Proposal

As soon as possible after completing the above, the BIC will prepare, but not publish, a Beanstalk Immunefi Response (BIR), which includes:

* What the potential practicable economic damage of the bug is;
* Whether the submission qualifies for a Critical, High or Medium Impact bounty/reward;
* What the appropriate bounty/reward should be within the Impact range; and
* Whether the submitting party is entitled to a bug bounty/reward, and if so, the amount of such bounty/reward.

In the instance where there are multiple bugs reported in the same report, a BIR will be prepared for each bug, such that the BIR can be released shortly after the implementation of the fix.

Before a BIR is proposed, its contents are confirmed with the submitter of the bug report via the Immunefi platform. As outlined in the bug bounty structure, in certain instances where the submitting party disputes the BIC’s proposal, Immunefi mediates.

Immediately after the implementation of a fix by the BCM or the Beanstalk DAO, the BIC will:

* Publish the BIR to Snapshot;
* Announce the existence of the BIR to the Beanstalk community via the Discord; and
* Vote on the BIR.

BIR voting takes place on Snapshot and lasts for 3 days. Only BIC members propose and vote on BIRs, and each member has one vote. BIC members can either vote For or Against a BIR, and a two-thirds majority of the BIC voting For is required to pass.

### Execution

Once a BIR passes, the BCM executes it by:

* Minting the corresponding number of Beans to cover the bug bounty and the 10% fee from Immunefi;
* Transferring the Beans corresponding to the bounty to the submitting party’s address; and
* Transferring the Beans corresponding to the 10% fee to Immunefi’s address.

The BIC may extend the bug bounty program to account for new assets that are in-scope. For example, after the Beanstalk UI is audited it is appropriate to add it as in-scope for the bug bounty program. Any other changes to the bug bounty program structure require a [BOP](../proposals.md#bop) (or [BIP](../proposals.md#bip)).

### Rationale

Security is paramount to the success of Beanstalk. Immunefi is crypto’s leading bug bounty platform that many other well-known DeFi protocols use to facilitate their bug bounty programs. This bounty program is competitive with the largest programs currently on Immunefi, making it likely to attract whitehat hackers.

This program establishes a method for the reporting and fixing bugs in a way that minimizes the risk to Beanstalk between the report and the fix, as well as the fair and transparent compensation for the reporting of bugs. The program gives bounty hunters a clear process and structure in order to increase the likelihood they attempt to find issues with Beanstalk and its related contracts and code.

The BIC structure of community-known members and public Snapshot proposals allows the Beanstalk community to scrutinize decisions, while still allowing the BIC to move swiftly in response to bug reports. The BIC consists of technical members of the Beanstalk community due to the nature of the BIC. The BIC can keep the bug information private while the bug is unfixed, and then has a clear process to disclose the bug to the public and compensate the submitter of the bug bounty. Having several members increases decentralization. The two-thirds majority required to approve a BIR and the BCM minting the Beans introduces multiple steps to mint Beans as a reward, which improves censorship-resistance.
