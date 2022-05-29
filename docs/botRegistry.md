

Bot Registry

The Bot Registry refers to a smart contract (currently deployed on the Polygon public mainnet) that records the existence of all detection bots. Developers publish their bot manifests to this registry, and scan nodes listen for events from this contract to know how to manage the bots they are running.


Bot Manifest

A bot manifest refers to a signed JSON document that describes the contents of a bot container. Specifically, it provides information like the bot version as well as an IPFS reference to the bot container image. Manifests are stored on the IPFS network, with their IPFS references stored in the Bot Registry.

