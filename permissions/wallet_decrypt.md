# wallet_decrypt

- Depends on: `eth_accounts`.

A method for decrypting a payload with a currently available account from `eth_accounts`.

This is an example of a _dependent permission_. A dependent permission depends on another permission internally, in this case, on a selected account as defined by [eth_accounts](./eth_accounts.md).

## Parameters

This method takes an `options` object as its sole parameter.

```javascript
const options = {
  address: '0x_prefixed_string',
  data: 'Any encrypted blob',
  algorithm: 'A supported algorithm identifier',
}
const decrypted = await provider.send({ method: 'wallet_decrypt', options);
```

## Stability

Not stable at all! Mostly composed as a reference doc, meant to be improved into a final spec.  Should probably be modified to resemble [EIP 1024](https://ethereum-magicians.org/t/eip-1024-cross-client-encrypt-decrypt/505).

