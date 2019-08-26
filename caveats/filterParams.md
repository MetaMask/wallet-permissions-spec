# filterParams

Caveat type name: `filterParams`
Caveat data structure: Array<any>

The `filterParams` caveat, when encoded, enforces mandatory requirements on the parameters that can be submitted for the parent method.

For example, if the permission object was this:

```javascript
{
  parentCapability: 'eth_sendTransaction',
  invoker: 'ens://metamask.eth',
  caveats: [
    {
      type: 'filterParams',
      value: [{ to: '0xe405fc812E90B7f8BA21d78c82fe240a476Aa7fB' }]
    }
  ]
}
```

Then the invoker (`metamask.eth`) would be permitted to call `sendTransaction`, but only if the `to` field were set to the very specific address of '0xe405fc812E90B7f8BA21d78c82fe240a476Aa7fB'.

This required parameter enforcement uses a simple object subset comaprison, and requires that the caveat `value` is a subset of the invoked parameters.

