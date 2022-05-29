
deploy your own detection bots on Forta using the SDK


https://github.com/arbitraryexecution/forta-agent-templates

https://github.com/forta-protocol/forta-bot-examples


Detection Bots

Detection bots refer to a set of code scripts within a Docker container that process some blockchain data (i.e. a block or transaction) and detect specific threat conditions (e.g. whether a flash loan attack occured, or whether a particular account balance fell below some threshold). Bots emit alerts for their findings. Bots are executed by scan nodes



By default, detection bot alerts are sent from Scan Nodes to a Forta maintained ElasticSearch database and then displayed in the Forta Explorer dashboard

If the detection bot is specified as private, the alerts will not appear in the Forta Explorer dashboard, but they will still be accessible through the Forta Public GraphQL API via queries specifying the detection bot ID


Forta bots are not required to publish their source code, and the bot code in the deployed container can be obfuscated in a variety of ways
Alert findings output from bots can be coded or encrypted.


