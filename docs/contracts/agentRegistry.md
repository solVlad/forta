AgentRegistry

Agents are abstract objects identified by a unique uint256 value. Agents are owned, transferable, and come with attributes:

"metadata": string (in practice the ipfs hash of a descriptor)
"chainIds": (sorted) array of integers

Both the metadata and the chainIds are mutable through the updateAgent function that is restricted to the agent's owner.

At every point in time, a metadata entry can belong to at most one agent
no two agents can share the same metadata entry

Agents can be enabled / disabled either by their owner or by an admin
Each actor has independent "disable" flags

If an admin disables an agent, it takes an admin action to re-enable it (the owner cannot re-enable).

Similarly, if an owner disables an agent, an admin cannot re-enable it.

If the agent Id is staked under the minimum stake, it can’t be enabled() will return false, regardless of the flags.




As metadata are unique, it is possible for someone to front-run the creation/update of an agent by creating a new agent, or updating an existing one, to take over the metadata entry

This should be avoided by adding a commit-reveal scheme with a delay to both functions (createAgent and updateAgent


https://docs.forta.network/en/latest/contracts/components/agents/AgentRegistry/


