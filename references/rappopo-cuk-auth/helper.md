# Helper

### auth:makeJwt

{% tabs %}
{% tab title="Description" %}
```javascript
helper('auth:makeJwt')(payload, secret, opts)
```
{% endtab %}

{% tab title="Parameters" %}
* `payload`: object to be encoded & serialized. Required.
* `secret`: secret phrase. Optional, defaults to `common.jwt.secret` in **auth.json** 
* `opts`: jsonwebtoken options. Optional, defaults to `common.jwt.opts` in **auth.json** 
{% endtab %}

{% tab title="Return" %}
String of encoded payload
{% endtab %}
{% endtabs %}



