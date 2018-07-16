---
description: Exported libraries
---

# Library

The following libraries are automatically exported and will be available to use throughout your app:

| **Name:** | **Initialized:** |
| --- | --- | --- | --- | --- | --- | --- | --- |
| `_` | `require('lodash')` |
| `debug` | `require('debug')` |
| `fs` | `require('fs-extra')` |
| `globby` | `require('globby')` |
| `moment` | `require('moment')` |
| `path` | `require('path')` |
| `util` | `require('util')` |

#### Usage:

```javascript
...
const { _, helper, path } = cuk.pkg.core.lib
let myPath = path.join(__dirname, 'my', 'file.js')
...
```

