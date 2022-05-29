AccessControl

other contract in the platform will refer to for role management. Rather than having all contracts include their own access management, roles are centralized here to simplify things. For example, giving the ENS_MANAGER_ROLE here will give the corresponding ability on all contracts in one single transaction.


The setNewRole function allows the DEFAULT_ADMIN_ROLE to updated role administration rules at any time. Note that this contract is mostly role agnostic and that roles identifiers that are not yet known/defined can be granted at any point without requiring an upgrade of this contract.


https://docs.forta.network/en/latest/contracts/components/access/AccessManager/
