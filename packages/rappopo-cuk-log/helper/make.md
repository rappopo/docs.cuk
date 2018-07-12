# make

```javascript
helper('log:make')(name, opts)
```

### Arguments

* `name`: must be in `<pkgId>:<basename>` syntax. Required.
* `opts`: the same winston transport options as in config file. Optional.

### Returned

Instance of winston logger.

If a log with that name already exists, then it will be returned immediately. If it doesn't exist yet, a new winston logger is created and returned. 

Log file will be saved in your data directory:

```bash
/<data dir>
  /log
    /<pkgId>
      <name>.log
```

Log file will also be automatically rotated every day.





