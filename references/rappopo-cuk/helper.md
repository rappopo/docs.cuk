---
description: Exported helper functions
---

# Helper

### core:bootConfig {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:bootConfig')(basename)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:bootDeep {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:bootDeep')(opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:bootFlat {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:bootFlat')(basename)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:bootInfo {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:bootInfo')(text)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:configFileExt {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:configFileExt')()
```
{% endtab %}

{% tab title="Parameters" %}
None
{% endtab %}

{% tab title="Return" %}
Return an array of supported file extension:

```javascript
...
const supported = helper('core:configFileExt')()
console.log(supported)
// displays: [".js", ".json"]
```
{% endtab %}
{% endtabs %}

### core:configLoad {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:configLoad')(dir, name)
```

`name` could be the _basename_ of the configuration file, or a directory name which hold the actual configuration file.

If it a file, it will be searched according this simple rule: `.js` first, and if not found then `.json`. If `.json` also not found, then it simply returns an empty object.

If `name` is a directory, then it will try to load `index.js` or `index.json` accordingly.

On both cases, the `.js` file needs to return a Promise and have to be wrapped inside a **cuk** wrapper like this:

{% code-tabs %}
{% code-tabs-item title="config.js" %}
```javascript
module.exports = function(cuk) {
  return new Promise((resolve, reject) => {
    ... 
    resolve({ my: 'config' })
  }
}
```
{% endcode-tabs-item %}
{% endcode-tabs %}
{% endtab %}

{% tab title="Parameters" %}
* `dir`: directory to search for name. It could be any directory, even outside your project tree. Required.
* `name`: name of configuration file you want to load, without file extension, or a sub directory with a file base named **index**. Optional. If it left empty, it defaults to: **config**
{% endtab %}

{% tab title="Return" %}
This function helper returns a Promise. If an error occurs, it will be silently discarded and returned as an empty object
{% endtab %}
{% endtabs %}

### core:makeChoices {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:bootChoices')(text)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:makeOptions {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:bootConfig')(basename)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:makeId {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:makeId')(basename)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:makeRelDir {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:bootConfig')(basename)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:merge {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:bootConfig')(basename)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:objectPickBy {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:bootConfig')(basename)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:pkgs {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:pkgs')(filter)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:pkg {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:pkg')(basename)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:parseUnitOfTime {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:bootConfig')(basename)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:collSortBy {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:bootConfig')(basename)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### core:makeError {#auth-makejwt}

{% tabs %}
{% tab title="Description" %}
```javascript
helper('core:bootConfig')(basename)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

