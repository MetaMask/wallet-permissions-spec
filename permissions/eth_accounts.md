# eth_accounts

This method, defined by the [Ethereum JSON RPC API](https://github.com/ethereum/wiki/wiki/JSON-RPC) originally would return all accounts owned by a user. For privacy reasons, it has gone through multiple revisions, most notably [EIP 1102](https://github.com/ethereum/EIPs/blob/master/EIPS/eip-1102.md), which introduced "Privacy Mode", which required user consent for any accounts to be returned by this method.

In this Wallet Permissions framework, `eth_accounts` can be defined as a restricted method like any other.

