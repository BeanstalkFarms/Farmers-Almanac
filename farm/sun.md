# Sun

The Beanstalk peg maintenance mechanism requires a protocol-native timekeeping mechanism and regular code execution on Ethereum. The Sun keeps time on the Farm in Seasons and incentivizes cost-efficient and timely calling of the sunrise() function.

Beanstalk adjusts itself to return the Bean price to its value peg at the beginning of every Season. Each Season is \~1 hour long. The first Season began when Beanstalk was deployed on August 6, 2021.

The exact beginning of each Season may vary as Seasons do not begin until the sunrise() function has been called through an Ethereum transaction. The first transaction that successfully calls the sunrise() function after the top of each hour UTC begins a new Season. Beanstalk only accepts one sunrise() function call per Season.

Beanstalk covers the cost of calling the sunrise() function by awarding the sender of an accepted sunrise() function call with newly minted Beans. To encourage regular sunrise() function calls even during periods of congestion on Ethereum while minimizing cost, the award starts at 100 Beans and compounds 1% every additional second that elapses for 300 seconds.

Upon acceptance of the sunrise() call, the Sun:

1. Increments the Season number;
2. Calculates deltaB, the time and liquidity weighted average shortage or excess Beans in the BEAN:3CRV liquidity pool;
3. Changes the Temperature if necessary and checks for Flood;
4. Sets the new Soil supply;
5. Mints Beans if necessary; and
6. Awards Beans to the address that successfully called the sunrise() function.
