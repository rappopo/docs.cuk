# Middleware

### security:csrf

{% tabs %}
{% tab title="Description" %}
This middleware is a tiny wrapper around [Koa CSRF](https://github.com/koajs/csrf): it provides CSRF support for your application.
{% endtab %}

{% tab title="Options" %}
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

To change options individually \(per route call\), please [read here](../rappopo-cuk-http/).
{% endtab %}

{% tab title="Usage" %}
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

And don't forget to put CSRF token on your form template as [shown here](view-globals.md#csrftoken)
{% endtab %}
{% endtabs %}

### security:helmet

{% tabs %}
{% tab title="Description" %}
[Helmet](https://helmetjs.github.io/) is a collection of 12 middleware to help set some security headers. 

This CUK middleware is a tiny wrapper arround [koa-helmet](https://github.com/venables/koa-helmet) which is Koa implementation of the fore mention middleware. 

{% hint style="info" %}
Use `security:helmet<Name>` instead to get the standalone version, where name is one of the keys in options.
{% endhint %}
{% endtab %}

{% tab title="Options" %}
By default, the following options serve as default:

```javascript
{
  "contentSecurityPolicy": false,
  "expectCt": false,
  "dnsPrefetchControl": true,
  "frameguard": true,
  "hidePoweredBy": true,
  "hpkp": false,
  "hsts": false,
  "ieNoOpen": true,
  "noCache": false,
  "noSniff": true,
  "referrerPolicy": false,
  "xssFilter": true
}
```

To change globally, edit the configuration in **security.json** in your config directory \(&lt;DDIR&gt;/config\) as shown below:

```javascript
{  
  "cuks": {
    "http": {
      "middleware": {        
        "helmet": {          
          // your global helmet options here        
        }      
      }    
    }  
  }
}
```

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http).

Putting `false` on one of the options above means disabling the named middleware, while `true` means enabling it with its default options. Consult [helmet documentations](https://helmetjs.github.io/docs/) for custom options.

If you put custom options on one or more keys above, those options will also be use as global options for the standalone versions.
{% endtab %}

{% tab title="Usage" %}
Inside your CUK Route file:

```javascript
...
return {  
  middleware: "security:helmet",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}

### security:contentSecurityPolicy

{% tabs %}
{% tab title="Description" %}
This is the standalone version of [helmet](middleware.md#security-helmet)'s Content Security Policy.
{% endtab %}

{% tab title="Options" %}
This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)
{% endtab %}

{% tab title="Usage" %}
Inside your CUK Route file:

```javascript
...
return {  
  middleware: "security:contentSecurityPolicy",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}

### security:dnsPrefetchControl

{% tabs %}
{% tab title="Description" %}
This is the standalone version of [helmet](middleware.md#security-helmet)'s DNS Prefetch Control.
{% endtab %}

{% tab title="Options" %}
This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)
{% endtab %}

{% tab title="Usage" %}
Inside your route file:

```javascript
...
return {  
  middleware: "security:helmetDnsPrefetchControl",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}

### security:expectCt

{% tabs %}
{% tab title="Description" %}
This is the standalone version of [helmet](middleware.md#security-helmet)'s Expect CT.
{% endtab %}

{% tab title="Options" %}
This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)
{% endtab %}

{% tab title="Usage" %}
Inside your route file:

```javascript
...
return {  
  middleware: "security:expectCt",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}

### security:frameguard

{% tabs %}
{% tab title="Description" %}
This is the standalone version of [helmet](middleware.md#security-helmet)'s Frameguard.
{% endtab %}

{% tab title="Options" %}
This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)
{% endtab %}

{% tab title="Usage" %}
Inside your route file:

```javascript
...
return {  
  middleware: "security:frameguard",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}

### security:hidePoweredBy

{% tabs %}
{% tab title="Description" %}
This is the standalone version of [helmet](middleware.md#security-helmet)'s Hide Powered By.
{% endtab %}

{% tab title="Options" %}
This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)
{% endtab %}

{% tab title="Usage" %}
Inside your route file:

```javascript
...
return {  
  middleware: "security:hidePoweredBy",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}

### security:hpkp

{% tabs %}
{% tab title="Description" %}
This is the standalone version of [helmet](middleware.md#security-helmet)'s HPKP.
{% endtab %}

{% tab title="Options" %}
This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)
{% endtab %}

{% tab title="Usage" %}
Inside your route file:

```javascript
...
return {  
  middleware: "security:hpkp",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}

### security:hsts

{% tabs %}
{% tab title="Description" %}
This is the standalone version of [helmet](middleware.md#security-helmet)'s HSTS.
{% endtab %}

{% tab title="Options" %}
This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)
{% endtab %}

{% tab title="Usage" %}
Inside your route file:

```javascript
...
return {  
  middleware: "security:hsts",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}

### security:ieNoOpen

{% tabs %}
{% tab title="Description" %}
This is the standalone version of [helmet](middleware.md#security-helmet)'s IE No Open.
{% endtab %}

{% tab title="Options" %}
This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)
{% endtab %}

{% tab title="Usage" %}
Inside your route file:

```javascript
...
return {  
  middleware: "security:ieNoOpen",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}

### security:noCache

{% tabs %}
{% tab title="Description" %}
This is the standalone version of [helmet](middleware.md#security-helmet)'s No Cache.
{% endtab %}

{% tab title="Options" %}
This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)
{% endtab %}

{% tab title="Usage" %}
Inside your route file:

```javascript
...
return {  
  middleware: "security:noCache",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}

### security:noSniff

{% tabs %}
{% tab title="Description" %}
This is the standalone version of [helmet](middleware.md#security-helmet)'s No Sniff.
{% endtab %}

{% tab title="Options" %}
This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)
{% endtab %}

{% tab title="Usage" %}
Inside your route file:

```javascript
...
return {  
  middleware: "security:noSniff",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}

### security:referrerPolicy

{% tabs %}
{% tab title="Description" %}
This is the standalone version of [helmet](middleware.md#security-helmet)'s Referrer Policy.
{% endtab %}

{% tab title="Options" %}
This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)
{% endtab %}

{% tab title="Usage" %}
Inside your route file:

```javascript
...
return {  
  middleware: "security:referrerPolicy",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}

### security:xssFilter

{% tabs %}
{% tab title="Description" %}
This is the standalone version of [helmet](middleware.md#security-helmet)'s XSS Filter
{% endtab %}

{% tab title="Options" %}
This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)
{% endtab %}

{% tab title="Usage" %}
Inside your route file:

```javascript
...
return {  
  middleware: "security:xssFilter",  
  handler: ctx => {    
    ...  
  }
}
...
```
{% endtab %}
{% endtabs %}



