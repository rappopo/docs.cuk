# Helper

### model:find

{% tabs %}
{% tab title="Description" %}
```javascript
helper('model:find')(name, opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:findOne

{% tabs %}
{% tab title="Description" %}
```javascript
helper('model:findOne')(name, id, opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:create

{% tabs %}
{% tab title="Description" %}
```javascript
helper('model:create')(name, body, opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:update

{% tabs %}
{% tab title="Description" %}
```javascript
helper('model:update')(name, id, body, opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:remove

{% tabs %}
{% tab title="Description" %}
```javascript
helper('model:remove')(name, id, opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:bulkCreate

{% tabs %}
{% tab title="Description" %}
```javascript
helper('model:bulkCreate')(name, body, opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:bulkUpdate

{% tabs %}
{% tab title="Description" %}
```javascript
helper('model:bulkUpdate')(name, body, opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:bulkRemove

{% tabs %}
{% tab title="Description" %}
```javascript
helper('model:bulkRemove')(name, body, opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:copyFrom

{% tabs %}
{% tab title="Description" %}
```javascript
helper('model:copyFrom')(name, src, opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:copyTo

{% tabs %}
{% tab title="Description" %}
```javascript
helper('model:copyTo')(name, dest, opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:get

{% tabs %}
{% tab title="Description" %}

{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}
Object of the following convenient proxy helpers & instance or throws error if something isn't right:

* `dab`: convenient helper of [getDab](helper.md#model-getdab)
* `schema`: convenient proxy of [getSchema](helper.md#model-getschema)
* `hook`: convenient proxy of [getHook](helper.md#model-gethook)
* `find`: convenient proxy of [find](helper.md#model-find)
* `findOne`: convenient proxy of [findOne](helper.md#model-findone)
* `create`: convenient proxy of [create](helper.md#model-create)
* `update`: convenient proxy of [update](helper.md#model-update)
* `remove`: convenient proxy of [remove](helper.md#model-remove)
* `bulkCreate`: convenient proxy of [bulkCreate](helper.md#model-bulkcreate)
* `bulkUpdate`: convenient proxy of [bulkUpdate](helper.md#model-bulkupdate)
* `bulkRemove`: convenient proxy of [bulkRemove](helper.md#model-bulkremove)
* `copyFrom`: convenient proxy of [copyFrom](helper.md#model-copyfrom)
* `copyTo`: convenient proxy of [copyTo](helper.md#model-copyto)
{% endtab %}

{% tab title="Example" %}
```javascript
...
const model = helper('model:get')('app:myModel')
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
{% endtab %}
{% endtabs %}

### model:getConnector

{% tabs %}
{% tab title="Description" %}

{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:getDab

{% tabs %}
{% tab title="Description" %}

{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:getHook

{% tabs %}
{% tab title="Description" %}

{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:getSchema

{% tabs %}
{% tab title="Description" %}

{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

