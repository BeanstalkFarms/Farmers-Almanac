# Beanstalk

A robust decentralized governance mechanism must balance the principles of decentralization with resistance to attempted protocol changes, both malicious and ignorant, and the ability to quickly adapt to changing information. In practice, Beanstalk must balance ensuring sufficient time for all ecosystem participants to consider a Beanstalk Improvement Proposal (BIP) with the ability to be quickly upgraded in cases of emergency.

Prior to Beanstalk’s April 17, 2022 exploit, Beanstalk Improvement Proposals (BIPs) were entirely on-chain and autonomous. However, after the exploit, Beanstalk was Paused and the ability to propose BIPs on-chain halted. Until governance is removed entirely, BIPs will be voted on off-chain via Snapshot and will be executed on-chain by the [Beanstalk Community Multisig (BCM)](bcm-process.md). Stalkholders are able to vote on BIPs via Snapshot.

BIPs are proposed on the [Beanstalk DAO Snapshot page](https://snapshot.org/#/beanstalkdao.eth/). Stalkholders can vote on BIPs on the [Beanstalk UI Governance page](https://app.bean.money/#/governance). Past BIPs can be read [here](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/blob/master/bip/).

### **Participation**

Anyone can become a Stalkholder and participate in Beanstalk governance by Depositing whitelisted assets in the Silo to earn Stalk.

A Stalkholder’s voting power is proportional to their Stalk balance relative to the total Stalk supply. Any Stalkholder can vote For or Against on any BIP. A Stalkholder's vote for a given proposal is counted as their Stalk at the beginning of the Voting Period that still exists. Stalkholders have the ability to delegate their vote to any other user.

Any Stalkholder that owns more than 0.1% of total outstanding Stalk can submit a BIP per the [#bip-proposal-process](bcm-process.md#bip-proposal-process "mention"). The submitter of a BIP must still own more than 0.1% of Stalk at the end of the Voting Period for the BIP to be able to pass.

### **Voting Period**

The Voting Period opens when the Snapshot proposal for a BIP can be voted on and ends 7 days later or when it is committed with a supermajority.

If at the end of the Voting Period:

* Less than or equal to one-third of the total outstanding Stalk, plus the amount of Stalk voting Against, is voting For, it fails, or
* More than one-third of the total outstanding Stalk, plus the amount of Stalk voting Against, is voting For, or more than half of total outstanding Stalk is voting For, it passes.

If at any time 24 hours or more after the beginning and before the end of the Voting Period more than two-thirds of the total outstanding Stalk is voting in favor of the BIP, the BCM can execute the BIP on-chain.

Beanstalk governance is designed to move slow and steady. When trying to become an issuer of money, the potential for rapid monetary policy changes is unattractive. By requiring more than one-third of Stalk to vote in favor of a BIP for it to pass, it is quite difficult for a BIP to pass. Therefore, unless the proposed change is _significantly preferred_ by Stalkholders, it is unlikely to pass.

### **Pause**

In case of a particularly dangerous vulnerability to Beanstalk, the BCM can Pause Beanstalk without a Snapshot. You can read more about which actions the BCM can take without a Snapshot proposal [here](bcm-process.md#snapshots). The Beanstalk DAO can also Pause Beanstalk via BIP.

When Paused, Beanstalk does not accept a `gm` function call. Once Unpaused, the `gm` function can be called at the beginning of the next hour.

### **Commit**

The BCM address has the exclusive and unilateral ability to Pause or Unpause Beanstalk, and commit a BIP. In the future, it is expected that BIPs will remove governance entirely, revoking these abilities from the BCM. You can read more about the BCM [here](bcm-process.md).
