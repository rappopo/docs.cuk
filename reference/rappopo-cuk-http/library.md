# Library

The following libraries are automatically exported and will be available to use throughout your app:

| **Name:** | **Initialized with:** |
| --- | --- | --- | --- | --- | --- |
| `Koa` | `require('koa')` |
| `app` | `new Koa()` |
| `koaMount` | `require('koa-mount')` |
| `koaCompose` | `require('koa-compose')` |
| `koaBodyParser` | `require('koa-bodyparser')` |

Example:

```javascript
const { app, koaMount } = cuk.pkg.http.lib
const hello = async function(ctx, next) {
  ctx.body = 'Hello'
}
app.use(koaMount('/hello', hello))
```



