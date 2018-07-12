# Library

The following libraries are automatically exported and will be available to use throughout your app

| **Name:** | **Initialized with:** |
| --- | --- | --- | --- |
| `xml` | `require('fast-xml-parser')` |
| `yaml` | `require('js-yaml')` |
| `coBody` | `require('co-body')` |

Example:

```javascript
...
const { fs } = cuk.pkg.core.lib
const { yaml } = cuk.pkg.util.lib
let result = yaml.safeLoad(fs.readFileSync('/my/yaml/file.yml'))
...
```

