# Wallet Permissions Spec

A repository for defining "restricted methods" that can be exposed over a web3 provider, through API-providing wallets like MetaMask, as defined in our [Web3 Wallet Permissions](https://ethereum-magicians.org/t/web3-login-permissions/3583/3) proposal, and encoded in [json-rpc-capabilities-middleware](https://github.com/MetaMask/json-rpc-capabilities-middleware).

## Structure

This is a very young repository, so it definitely has room to grow and expand its structure. At the very least, I think two folders should be useful:

- `permissions`
- `caveats`

### Permissions

Items in this folder will be named the same as the method they specify, with a filetype suffix (like `.md`).

These files should include:

- The method name
- A human readable description of what the method does, as could be presented to a user at the time of login.
- Any additional context that could be helpful to why this permission is useful.
- Optional sample implementation.

### Caveats

Items in the `caveats` folder will be named the same as that caveat's valid `type` value.

This folder will include supported caveats, or limitations on a given permission. Any number of caveats can be applied to a given permission, and each one has the ability to invalidate or adjust the parameters or return values of a method call.

A caveat is a JSON object with two traits:

- type (string)
- value (optional, can be any data type, depending on the type of caveat).

