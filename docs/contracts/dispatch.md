
dispatch

The dispatch contract keeps track of the agent <> scanner links. An agent can be run by multiple scanners and a scanner can run multiple agents.

Links between scanners and agents are managed by the DISPATCHER_ROLE which could be given to a future contract that defines some rules to link/unlink

In order to be linked, both agents and scanners have to be enabled and staked over their minimum defined stake

This contract includes a "hash" mechanism that can be used to produce agent hash or scanner hash

These hash identify the state of the relations for an object and change if one of the associated values changes

For example, if a scanner is linked to an agent, and the agent is updated, the scanner hash will be affected. If an agent is added, removed, or change its enable/disable status, the scanner hash will also be affected

These hash functions should only be called as part of RPC calls, and not during transaction execution. 
They are here to help the scanner entity detect changes if event subscriptions are missing or failing.

https://docs.forta.network/en/latest/contracts/components/dispatch/Dispatch/


