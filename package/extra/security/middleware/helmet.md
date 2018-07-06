# helmet

[Helmet](https://helmetjs.github.io/) is a collection of 12 middleware to help set some security headers. 

This CUK middleware is a tiny wrapper arround [koa-helmet](https://github.com/venables/koa-helmet) which is Koa implementation of the fore mention middleware. 

{% hint style="info" %}
Use `security:helmet<Name>` instead to get the standalone version, where name is one of the keys in options.
{% endhint %}

### Usage {#usage}

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

### Options {#options}

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

