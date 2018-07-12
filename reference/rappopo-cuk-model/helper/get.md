---
description: Wraps the most commonly used helpers into one object
---

# get

```javascript
helper('model:get')(name)
```

### Arguments

* `name`: the model name, required

### Returns

Object of the following convenient proxy helpers & instance or throws error if something isn't right:

* `dab`: convenient helper of [getDab](get-dab.md)
* `schema`: convenient proxy of [getSchema](get-schema.md)
* `hook`: convenient proxy of [getHook](get-hook.md)
* `find`: convenient proxy of [find](find.md)
* `findOne`: convenient proxy of [findOne](find-one.md)
* `create`: convenient proxy of [create](create.md)
* `update`: convenient proxy of [update](update.md)
* `remove`: convenient proxy of [remove](remove.md)
* `bulkCreate`: convenient proxy of [bulkCreate](bulk-create.md)
* `bulkUpdate`: convenient proxy of [bulkUpdate](bulk-update.md)
* `bulkRemove`: convenient proxy of [bulkRemove](bulk-remove.md)
* `copyFrom`: convenient proxy of [copyFrom](copy-from.md)
* `copyTo`: convenient proxy of [copyTo](copy-to.md)

### Example

```javascript
...
let model = helper('model:get')('app:myModel')
model.create({ first_name: 'James', last_name: 'Blondy' })
.then(result => {
  return model.update(result.data.id, { last_name: 'Bond' })
})
.then(result => {
  return model.find()
})
.then(result => {
  console.log(result)
  /* result is object of something like this:
  { 
    success: true,
    total: 1,
    data: [{
      _id: '<auto_generated_id>',
      first_name: 'James',
      last_name: 'Bond'
    }]
  }
  */
})
.catch(err => {
  console.log(err.message)
})

```

