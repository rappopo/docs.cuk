# Configuration

By default, the following configuration apply:

```javascript
{
  "common": {
    "ext": "",
    "trimIndex": true,
    "session": {
      "key": "cuk:sess",
      "maxAge": 86400000,
      "overwrite": true,
      "httpOnly": true,
      "signed": true,
      "rolling": false,
      "renew": false
    }
  }
}
```

To override this config, create **route.json** inside your data directory \(`<data dir>/config/route.json`\)

* `ext`: route extension. To set all route to have an extension, simply put e.g `.html` in it. Optional, defaults to empty string.
* `trimIndex`: set true to short named route path \(`/my/route/index` to `/my/route`\). Optional, defaults to true.
* `session`: session options according to [this](https://github.com/koajs/session). 

