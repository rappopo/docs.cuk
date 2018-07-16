# makeJwt

```javascript
helper('auth:makeJwt')(payload, secret, opts)
```

### Arguments

* `payload`: object to be encoded & serialized. Required.
* `secret`: secret phrase. Optional, defaults to `common.jwt.secret` in **auth.json** 
* `opts`: jsonwebtoken options. Optional, defaults to `common.jwt.opts` in **auth.json** 

### Returns

String of encoded payload above.

\*\*\*\*

