# Middleware

### auth:basic

Basic authentication middleware

{% tabs %}
{% tab title="Description" %}
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

{% tab title="Example" %}
#### REST file:

```javascript
module.exports = function(cuk) {
  return {
    middleware: 'auth:basic, ..., auth:checkPoint',
    method: {
      create: {
        handler: ctx => {
          ...
        }
      },
      ...
    }
  }
}
```

#### Route file:

```javascript
module.exports =function(cuk) {
  return {
    middleware: 'auth:basic, ..., auth:checkPoint',
    method: 'GET, POST',
    handler: ctx => {
      ...
      ctx.render('app:/myform')
    }
  }
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

{% tab title="Example" %}
#### REST file:

```javascript
module.exports = function(cuk) {
  return {
    middleware: 'auth:jwt, ..., auth:checkPoint',
    method: {
      create: {
        handler: ctx => {
          ...
        }
      },
      ...
    }
  }
}
```

#### Route file:

```javascript
module.exports =function(cuk) {
  return {
    middleware: 'auth:jwt, ..., auth:checkPoint',
    method: 'GET, POST',
    handler: ctx => {
      ...
      ctx.render('app:/myform')
    }
  }
}
```
{% endtab %}
{% endtabs %}

### auth:checkPoint

{% tabs %}
{% tab title="Description" %}

{% endtab %}

{% tab title="Example" %}
#### REST file:

```javascript
module.exports = function(cuk) {
  return {
    middleware: 'auth:basic, auth:jwt, ..., auth:checkPoint',
    method: {
      create: {
        handler: ctx => {
          ...
        }
      },
      ...
    }
  }
}
```

#### Route file:

```javascript
module.exports =function(cuk) {
  return {
    middleware: 'auth:basic, auth:jwt, ..., auth:checkPoint',
    method: 'GET, POST',
    handler: ctx => {
      ...
      ctx.render('app:/myform')
    }
  }
}
```
{% endtab %}
{% endtabs %}

