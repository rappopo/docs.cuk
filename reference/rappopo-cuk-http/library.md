# Library

The following libraries are automatically exported and will be available to use throughout your app:

```javascript
const { app, koaMount } = cuk.http.lib
const hello = async function(ctx, next) {
  await next()
  ctx.body = 'Hello'
}
app.use(koaMount('/hello', hello))
```

| **Name:** | **Initialized with:** |
| --- | --- | --- | --- | --- | --- |
| `Koa` | `require('koa')` |
| `app` | `new Koa()` |
| `koaMount` | `require('koa-mount')` |
| `koaCompose` | `require('koa-compose')` |
| `koaBodyParser` | `require('koa-bodyparser')` |



