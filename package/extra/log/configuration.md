# Configuration

Default configuration:

```javascript
{
  "disabled": [],
  "common": {
    "opts": {
      "colorize": false,
      "timestamp": true,
      "json": true,
      "size": "100m",
      "keep": 5,
      "compress": true
    }
  }
}

```

To override these settings, create **log.json** inside your data directory \(`<data dir>/config/log.json`\).

* `opts`: winston transport default options. [Read more here](https://github.com/winstonjs/winston/tree/2.x).

