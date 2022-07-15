# Beanstalk

A robust decentralized governance mechanism must balance the principles of decentralization with resistance to attempted protocol changes, both malicious and ignorant, and the ability to quickly adapt to changing information. In practice, Beanstalk must balance ensuring sufficient time for all ecosystem participants to consider a Beanstalk Improvement Proposal (BIP) with the ability to be quickly upgraded in cases of emergency.

Prior to Beanstalk’s April 17 exploit, Beanstalk Improvement Proposals (BIPs) were entirely on-chain and autonomous. However, after the exploit, Beanstalk was Paused and the ability to propose BIPs on-chain halted. Until a robust on-chain governance system is implemented, BIPs will be voted on off-chain via Snapshot and will be executed on-chain by the [Beanstalk Community Multisig (BCM)](bcm-process.md). Stalkholders are able to vote on BIPs via Snapshot.

The BCM has been formed, but ownership of Beanstalk has not yet been transferred to the BCM. Publius, the founders of Beanstalk, currently custody ownership of the Beanstalk contract. The transfer of ownership to the BCM will be proposed in the BIP to Replant Beanstalk.

**Beanstalk DAO Snapshot page:**

{% embed url="https://snapshot.org/#/beanstalkfarms.eth" %}

### **Participation**

Anyone can become a Stalkholder and participate in Beanstalk governance by Depositing whitelisted assets in the Silo to earn Stalk. A Stalkholder’s voting power is proportional to their total Stalk ownership relative to the total Stalk supply. Any Stalkholder can vote for or abstain from BIPs. In all instances, 1 Stalk equals 1 vote, and abstaining is equivalent to voting against the proposal.

Any Stalkholder that owns more than 0.1% of total outstanding Stalk can submit a BIP per the [#proposing-a-bip](bcm-process.md#proposing-a-bip "mention") process.

### **Voting Period**

Voting for BIPs will take place on Snapshot, using Stalk ownership at the time of proposal on Snapshot. The Voting Period opens when a BIP is submitted to Snapshot and closes after \~7 days or when it is committed with a supermajority.

If at the end of the Voting Period:

* Less than or equal to half of the total outstanding Stalk at the time of proposal on Snapshot votes in favor of the BIP, the BIP fails; or
* More than half of the total outstanding Stalk at the time of proposal on Snapshot votes in favor of the BIP, the BIP passes.

Any time 24 hours or more after the opening and before the closing of the Voting Period that more than two-thirds of the total outstanding Stalk votes in favor of a BIP, the BCM can execute the BIP on-chain.

### **Pause**

In case of a particularly dangerous vulnerability to Beanstalk, the BCM can Pause Beanstalk without a Snapshot. You can read more about which actions the BCM can take without a Snapshot proposal [here](bcm-process.md#snapshots). The Silo can also Pause Beanstalk via BIP.

When Paused, Beanstalk does not accept a sunrise() function call. Once Unpaused, the sunrise() function can be called at the beginning of the next hour.

### **Commit**

At Replant, the Beanstalk Community Multisig (BCM) address has the exclusive and unilateral ability to Pause or Unpause Beanstalk, and commit a BIP. In the future, we expect a BIP will revoke these abilities from the BCM and reimplement on-chain governance. You can read more about the BCM [here](bcm-process.md).

****

**BIPs folder on GitHub (before BIP-20):**

{% embed url="https://github.com/BeanstalkFarms/Beanstalk/tree/master/bips" %}