# Library

The following libraries are automatically exported and will be available to use throughout your app:

| **Name:** | **Initialized with:** |
| --- | --- | --- |
| `jwt` | `require('jsonwebtoken')` |
| `bcrypt` | `require('bcrypt')` |

#### Usage

```javascript
const { jwt } = cuk.pkg.auth.lib
jwt.sign({ 
  first_name: 'James',
  last_name: 'Bond'
}, 'mysuperdupersecretkey')
```

