# helmetContentSecurityPolicy

This is the standalone version of [helmet](helmet.md)'s Content Security Policy.

### Usage {#usage}

Inside your CUK Route file:

```javascript
...
return {  
  middleware: "security:helmetContentSecurityPolicy",  
  handler: ctx => {    
    ...  
  }
}
...
```

### Options {#options}

This standalone version use the same key options of helmet in **security.json**. If custom options is set there, then it will be used globally. Otherwise it will use default options. 

To change options individually \(per route call\), please [read here](https://docs.rappopo.com/cuk/package/common/http) and [helmet documentations](https://helmetjs.github.io/docs/)

