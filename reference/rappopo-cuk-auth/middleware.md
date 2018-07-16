# Middleware

### auth:basic

{% tabs %}
{% tab title="Description" %}

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

