# loadConfig

```javascript
helper('core:loadConfig')(dir, name)
```

### Arguments

* `dir`: directory to search for name. It could be any directory, even outside your project tree. Required.
* `name`: name of configuration file you want to load, without file extension. Optional. If it left empty, it defaults to: **config**

### Description

`name` could be the basename of the configuration file, or a directory name which hold the actual configuration file.

If it a file, it will be searched according this simple rule: `js` first, and if not found then `json`. If no json also not found, then it simple return an empty object.

if `name` is a directory, then it will try to load `index.js` or `index.json` accordingly.

On both cases above, the javascript file needs to return a Promise and have to be wrapped inside a cuk wrapper like this:

{% code-tabs %}
{% code-tabs-item title="config.js" %}
```javascript
'use strict'
module.exports = function(cuk) {
  return new Promise((resolve, reject) => {
    ... 
    resolve({ my: 'config' })
  }
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Some packages might extend these file formats, \(e.g: [@rappopo/cuk-util](../../rappopo-cuk-util/) add two supported format: `yml` & `xml`\)

### Result

Result will be a returned as a Promise. If an error occurs, it will be silently discarded and returned as an empty object



