# csrf

This middleware is a tiny wrapper around [Koa CSRF](https://github.com/koajs/csrf): it provides CSRF support for your application.

View

### Usage

Inside your CUK Route file:

```javascript
...
return {
  method: 'POST',
  middleware: "http:bodyParser, security:csrf",
  handler: ctx => {
    ...
  }
}
...
```

And don't forget to put CSRF token on your form template as [shown here](../view-globals/csrftoken.md#usage)

### Options

By default, the following options serve as default:

```javascript
{
  "invalidSessionSecretMessage": "Invalid session secret",
  "invalidSessionSecretStatusCode": 403,
  "invalidTokenMessage": "Invalid CSRF token",
  "invalidTokenStatusCode": 403,
  "excludedMethods": ["GET", "HEAD", "OPTIONS"],
  "disableQuery": false
}
```

To change globally, edit the configuration in **security.json** in your config directory \(&lt;DDIR&gt;/config\) as shown below:

```javascript
{
  "cuks": {
    "http": {
      "middleware": {
        "csrf": {
          // your global CSRF options here
        }
      }
    }
  }
}
```

To change options individually \(per route call\), please [read here](../../rappopo-cuk-http/).

