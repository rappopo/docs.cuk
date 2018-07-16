# Helper

### log:get

{% tabs %}
{% tab title="Description" %}
```javascript
helper('log:get')(name)
```
{% endtab %}

{% tab title="Arguments" %}
* `name`: must be in `<pkgId>:<itemName>` syntax. Required.
{% endtab %}

{% tab title="Returns" %}
The matched winston logger is returned.
{% endtab %}
{% endtabs %}

### log:make

{% tabs %}
{% tab title="Description" %}
```javascript
helper('log:make')(name, opts)
```

If a log with that name already exists, then it will be returned immediately. If it doesn't exist yet, a new winston logger is created and returned. 

Log file will be saved in your data directory:

```bash
/<data dir>
  /log
    /<pkgId>
      <itemName>.log
```

Log file will also be automatically rotated every day.
{% endtab %}

{% tab title="Arguments" %}
* `name`: must be in `<pkgId>:<itemName>` syntax. Required.
* `opts`: the same winston transport options as in config file. Optional.
{% endtab %}

{% tab title="Returns" %}
Instance of winston logger.
{% endtab %}
{% endtabs %}



