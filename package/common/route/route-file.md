# Route File

### 

### Route Forms

CUK Route accepts many forms of route files as outlined below:

#### Raw body content

Returned string will be assigned as `ctx.body` and sent to the browser:

```javascript
module.exports = function(cuk) {
  ...
  return '<p>Your content here...</p>'
}
```

#### View content

In this form, you only need to return the name of your view file and CUK Route will **try** render that view file right away. Make sure that you've installed the right package \(that your view file belongs to\) before:

```javascript
module.exports = function(cuk) {
  ...
  return 'app:/my/view'
}
```

#### One and only route object

This is my preferred choice. Clear & concise. In this case:

* `method`: HTTP Verb to choose. Optional, defaults to `GET`
* `middleware`: middleware to use. More info [here](../http/). Optional.
* `path`: if the auto generated route path doesn't satisfy you, override here. Optional.
* `param`: [Read here](https://github.com/alexmingoia/koa-router#module_koa-router--Router+param) for more info on this. Optional.
* `handler`: your route handler. Required.

```javascript
module.exports = function(cuk) {
  ...
  return {
    method: 'GET',
    middleware: 'app:routeMiddleware',
    path: '/my/custom/route/path',
    param: {
      routeParam: (routeParam, ctx, next) => {
        ...
        return next()
      }
      ...
    },
    handler: async (ctx, next) => {
      ...
      ctx.render('app:/my/view')
    }
  }
}
```

#### Array of many route objects

The same as above to handle multiple routes in one route file:

```javascript
module.exports = function(cuk) {
  ...
  return [{
    method: 'GET',
    middleware: 'app:routeMiddleware',
    path: '/my/custom/route/path',
    param: {
      routeParam: (routeParam, ctx, next) => {
        ...
        return next()
      }
      ...
    },
    handler: async (ctx, next) => {
      ...
      ctx.render('app:/my/view')
    }
  }, {
    ...
  }]
}
```

#### Complete with global options

Pretty much the same as above, except that it supports global options:

* `middleware`: put here to have global middleware for all routes. Optional.
* `param`: global parameters to be inspected. Optional.
* `route`: routes container. Required.

```javascript
module.exports = function(cuk) {
  ...
  return {
    middleware: 'app:globalMiddleware',
    param: {
      globalParam: (globalParam, ctx, next) => {
        ...
        return next()
      },
      ...
    },
    route: [
      {
        method: 'GET',
        middleware: 'app:routeMiddleware',
        path: '/my/custom/route/path',
        param: {
          routeParam: (routeParam, ctx, next) => {
            ...
            return next()
          }
          ...
        },
        handler: async (ctx, next) => {
          ...
          ctx.render('app:/my/view')
        }
      },
      ...
    ]
  }
}
```

### Redirect

How to redirect request to an external URL? Pretty easy:

```javascript
return {
  method: 'GET',
  redirect: 'https://www.google.com'
}
```

In this case, all other settings are irrelevant. They're simply ignored. Except one: middleware still be executed before the actual redirect, if you put one. This is useful for example you'd only allow certain user to be redirected, etc.

### Router Instance

If you have a Koa Router instance ready, or  any of route forms above doesn't suit you well, you could just attach router instance like this:

```javascript
module.exports = function(cuk) {
  ...
  const { Router } = cuk.pkg.route.lib
  const router = new Router()
  router.get('/hello', async ctx => {
    ctx.body = 'Hello world'
  })
  ...
  return router
}
```

{% hint style="warning" %}
If you want to use any of CUK middleware, you need to make a wrapper around this. 
{% endhint %}

Wrong, it won't work:

```javascript
router.get('/hello', 'http:responseTime', async ctx => {
  ctx.body = 'Hello world'
})
```

Right:

```javascript
const middleware = helper('http:middleware')('http:responseTime')
router.get('/hello', middleware, async ctx => {
  ctx.body = 'Hello world'
})
```

Right, multiple middleware:

```javascript
const middleware = helper('http:composeMiddleware')('http:responseTime, http:cors')
router.get('/hello', middleware, async ctx => {
  ctx.body = 'Hello world'
})
```



