# Vote on Governance Proposals

Beanstalk is [governed](../../governance/beanstalk/) by Stalkholders. Anyone with Stalk can vote for [Beanstalk Improvement Proposals](../../governance/proposals.md#bip) (BIPs), [Beanstalk Operations Proposals](../../governance/proposals.md#bop) (BOPs), [Beanstalk Farms Committee Proposals](../../governance/proposals.md#bfcp) (BFCPs) and [Bean Sprout Proposals](../../governance/proposals.md#bsp) (BSPs).&#x20;

View past governance proposals [here](https://github.com/BeanstalkFarms/Beanstalk-Governance-Proposals/).

1. Make sure you are on [app.bean.money](https://app.bean.money/) and [connect your wallet](../getting-started/connect-wallet.md).
2. Select “More” then “Governance” to navigate to the [Governance](https://app.bean.money/#/governance) page.
3. Your voting power in Stalk is listed under "Stalkholder".&#x20;
4. Select "[DAO](https://app.bean.money/#/governance?type=dao)", "[Beanstalk Farms](https://app.bean.money/#/governance?type=beanstalk-farms)" or "[Bean Sprout](https://app.bean.money/#/governance?type=bean-sprout)" to view governance proposals. A green circle will appear by the category if there are active governance proposals.
5. Active governance proposals are listed first and have a green circle. Closed governance proposals have a gray circle. Select the active governance proposal you want to vote on.
6. Under the “Results” section select the choice you want to vote for.
   * Note: Selecting the “Abstain” choice on a BIP or BOP is the same as not voting. It is not possible to remove a vote on Snapshot, so the “Abstain” choice exists on some proposals to allow Farmers to unvote after voting.
7. Select “Vote”.
8. Sign the message in your wallet and your hardware wallet, if applicable. You should verify the message before signing it. Snapshot votes are plain text messages. An example is shown [below](vote-on-proposals.md#snapshot-vote-signature).
9. After signing, it may take some time for your vote to appear on the Beanstalk UI. Check Snapshot by selecting "View on Snapshot" for the latest results.&#x20;
10. You may change your vote by repeating this process before the proposal is closed at the time specified in "Vote ends in". The exact time a proposal closes is viewable by selecting "View on Snapshot".

#### Example Snapshot Vote Signature

```
{
 "types": {
  "Vote": [
   {
    "name": "from",
    "type": "address"
   },
   {
    "name": "space",
    "type": "string"
   },
   {
    "name": "timestamp",
    "type": "uint64"
   },
   {
    "name": "proposal",
    "type": "bytes32"
   },
   {
    "name": "choice",
    "type": "uint32"
   },
   {
    "name": "app",
    "type": "string"
   }
  ]
 },
 "domain": {
  "name": "snapshot",
  "version": "0.1.4"
 },
 "primaryType": "Vote",
 "message": {
  "from": "[Ethereum address]",
  "space": "wearebeansprout.eth",
  "timestamp": "1661055899",
  "proposal": "0x7b2d54f3691fa65fc784e3398425d518eab93d233f3ad0abd3d87b572cf5ab2f",
  "choice": "2",
  "app": "snapshot"
 }
}
```

****
