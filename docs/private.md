

Pushing data directly from the Forta detection bot to an External API Endpoint - As in the case of the data sources, there is no mechanism for keeping an API key secret. This is ill-advised.

Performing on-chain actions from within a Forta detection bot is not advised, given the public nature of the Forta detection bot code and any keys it may use

However, Forta detection bot alerts can be monitored by OpenZeppelin Defender Forta Sentinels, where the Defender account is private

When a Forta Sentinel detects a new alert from a specific Forta detection bot, it can execute a Defender Autotask to initiate on-chain transactions to call specific contract methods, such as pause()


For users that prefer to deploy bots to a private environment without any public exposure, or that simply want redundancy for their bots on the public network, Forta also can support these users running private nodes, which remain completely independent of the public Forta network and do not participate in public detection bot assignment or public broadcast of detection bot findings.


