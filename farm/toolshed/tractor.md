# Tractor

{% hint style="info" %}
Tractor is currently not supported in the Beanstalk UI.
{% endhint %}

Maintaining and optimizing a position in Beanstalk requires manual intervention (Mowing, Planting, Harvesting Pods and Depositing the Beans, etc.). Smaller Farmers do not necessarily have the resources to automate the execution of their Beanstalk transactions, and existing generalized function call systems (i.e., smart contract accounts, Depot + Pipeline) only support the use of assets from the sender of the transaction.

Tractor is a peer-to-peer transaction marketplace that allows third party operators to perform Beanstalk actions on behalf of a Farmer.

Blueprints are off-chain data structures that are [EIP-712](https://eips.ethereum.org/EIPS/eip-712) signed to verify the intent of the publishing Farmer. Blueprints allow Farmers to define arbitrary sequences of on-chain function calls, which can be executed permissionlessly by other Farmers known as Tractor Operators.

Blueprints contain the Publisher, an Advanced Farm function call containing an arbitrary sequence of internal function calls, a set of copy instructions that define how to interpret Operator calldata, expiry parameters and the EIP-712 signature from the Publisher. Any Tractor Operator can execute any Blueprint with any calldata at anytime through the `tractor(...)` function provided that the Blueprint does not revert.

Junctions are contracts that are contain basic operations as external functions that are used by Tractor orders. Junctions allow Farmers to define Blueprints that will fail under a predefined set of conditions, such as balance limits, price thresholds, etc.

**Examples**

* A Farmer creates a Blueprint for an Operator to Plant on their behalf any time they have more than 100 Earned Beans and will pay the caller 1 Earned Bean.
* A Farmer creates a Blueprint for an Operator to Mow on their behalf any time that P > 1 and will pay the caller 5 USDC.
