---
description: Exported helper functions
---

# Helper

### core:bootConfig {#auth-makejwt}

```javascript
helper('core:bootConfig')(basename)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:bootDeep {#auth-makejwt}

```javascript
helper('core:bootDeep')(opts)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:bootFlat {#auth-makejwt}

```javascript
helper('core:bootFlat')(basename)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:bootInfo {#auth-makejwt}

```javascript
helper('core:bootInfo')(text)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:loadConfig {#auth-makejwt}

```javascript
helper('core:loadConfig')(dir, name)
```

{% tabs %}
{% tab title="Arguments" %}
* `dir`: directory to search for name. It could be any directory, even outside your project tree. Required.
* `name`: name of configuration file you want to load, without file extension, or a sub directory with a file base named **index**. Optional. If it left empty, it defaults to: **config**
{% endtab %}

{% tab title="Returns" %}
This function helper returns a Promise. If an error occurs, it will be silently discarded and returned as an empty object
{% endtab %}

{% tab title="Description" %}
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
{% endtabs %}

### core:makeChoices {#auth-makejwt}

```javascript
helper('core:bootChoices')(text)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:makeOptions {#auth-makejwt}

```javascript
helper('core:bootConfig')(basename)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:makeId {#auth-makejwt}

```javascript
helper('core:makeId')(basename)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:makeRelDir {#auth-makejwt}

```javascript
helper('core:bootConfig')(basename)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:merge {#auth-makejwt}

```javascript
helper('core:bootConfig')(basename)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:objectPickBy {#auth-makejwt}

```javascript
helper('core:bootConfig')(basename)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:pkgs {#auth-makejwt}

```javascript
helper('core:pkgs')(filter)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:pkg {#auth-makejwt}

```javascript
helper('core:pkg')(basename)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:parseUnitOfTime {#auth-makejwt}

```javascript
helper('core:bootConfig')(basename)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:collSortBy {#auth-makejwt}

```javascript
helper('core:bootConfig')(basename)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

### core:makeError {#auth-makejwt}

```javascript
helper('core:bootConfig')(basename)
```

{% tabs %}
{% tab title="Arguments" %}

{% endtab %}

{% tab title="Returns" %}

{% endtab %}
{% endtabs %}

