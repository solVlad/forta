
Operational monitoring

Operational (“performance”) monitoring checks that your protocol is functioning as expected, within some predetermined bounds. These types of checks are beneficial for the protocol’s community, as they provide some assurance of the overall health of the protocol while still highlighting some of the more extraordinary transactions that occur. Beyond the financial operation, this monitoring may provide information about when implementation contracts are upgraded, admin addresses change, or critical administrative smart contract methods are called. This type of monitoring would provide alerts that may be appropriate for display in a dashboard like Splunk, DataDog, etc.




For example, the total liquidity of pools may fluctuate by ±1% over the course of a day, so any single transaction that affects the liquidity by more than that should trigger an alert. Alternatively, because some pools may have relatively little liquidity, it may make sense to use a fixed value threshold (denominated in USDC, ETH, USD, etc.) rather than a percentage.


Threat monitoring

Threat detection monitoring provides alerts on transactions and events that may indicate malicious activity. One of the main challenges in threat monitoring is determining “what to look for” in transactions.

Therefore, a useful monitoring pattern may be to identify EOAs performing transactions with a protocol and then check if those EOAs have performed withdrawals from any Tornado Cash contracts within the recent past 
