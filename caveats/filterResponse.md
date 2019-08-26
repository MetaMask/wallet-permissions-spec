## filterResponse

Caveat type name: `filterResponse`
Caveat data structure: Array<any>

The `filterResponse` caveat, when encoded, enforces a filter on the responses returned to the requestor.

Currently it only performs an exact-match comparison, and so only works on simple values. Was devised for the purposes of selecting accounts.

For example, if the permission object was this:

```javascript
{
  parentCapability: 'eth_accounts',
  invoker: 'ens://metamask.eth',
  caveats: [
    {
      type: 'filterResponse',
      value: ['0xe405fc812E90B7f8BA21d78c82fe240a476Aa7fB']
    }
  ]
}
```

Then the invoker (`metamask.eth`) would be permitted to call `eth_accounts`, but regardless of how many accounts the user had, the only account that could ever be returned would be '0xe405fc812E90B7f8BA21d78c82fe240a476Aa7fB'. If the user removed this account, the requesting application would receive an empty array.

