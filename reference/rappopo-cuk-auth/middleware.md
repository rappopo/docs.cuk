# Middleware

### auth:basic

{% tabs %}
{% tab title="Description" %}
Basic authentication middleware

This middleware reads authorization header. If empty, it simply skips to the next middleware. 

If found, it'll look for user with matched credential passed by authorization header. If a user is found and not temporarily disabled, app context will be filled with stuffs like this:

```javascript
ctx.state.auth = {
  method: 'basic',
  user: {
    _id: '<my_id'>
    ...
  }
}
```
{% endtab %}

{% tab title="Usage" %}
Route file:

```javascript
...
return {
  middleware: 'auth:basic, ..., auth:checkPoint',
  ...
}
```
{% endtab %}
{% endtabs %}

### auth:jwt

{% tabs %}
{% tab title="Description" %}
This middleware reads authorization header and looking for JWT token.

If found, token payload will be decoded and matched user will be looked up in user database. If a user is found and not temporarily disabled, app context will be filled with stuffs like above
{% endtab %}

{% tab title="Usage" %}
Route file:

```javascript
...
return {
  middleware: 'auth:jwt, ..., auth:checkPoint',
  ...
}
```
{% endtab %}
{% endtabs %}

### auth:checkPoint

{% tabs %}
{% tab title="Description" %}

{% endtab %}

{% tab title="Usage" %}
Route file:

```javascript
...
return {
  middleware: 'auth:basic, auth:jwt, ..., auth:checkPoint',
  ...
}
```

#### 
{% endtab %}
{% endtabs %}

