# Helper

### model:find\(name, opts\)

{% tabs %}
{% tab title="Description" %}
Find records from DAB that matched your query. 



See [this](https://docs.rappopo.com/dab/method/common/find) for details.

Usage:

```javascript
helper('model:find')(name, opts)
```
{% endtab %}

{% tab title="Parameters" %}
* `name` _&lt;string&gt;_ **Required**.
* `body` _&lt;Object&gt;_ **Required**.
* `opts` _&lt;Object&gt;_ Default: `{}`
  * `query` _&lt;object&gt;_ DAB query. Default: `{}`
  * `limit` _&lt;integer&gt;_ Limit number of results. Defaults to `common.default.limit` from your **model.json**
  * `page` _&lt;integer&gt;_ Page number. Default: `1`
  * `sort` _&lt;Object&gt;_ Default: `{}`
{% endtab %}

{% tab title="Return" %}
Object like this:

```javascript
{
  "success": true,
  "total": 100,
  "data": [{
    "_id": "james-bond",
    "first_name": "James",
    "last_name": "Bond",
    "age": 38
  }, {
    "_id": "jack-bauer",
    "first_name": "Jack",
    "last_name": "Bauer",
    "age": null
  }]
} 
```

More info [here](https://docs.rappopo.com/dab/method/common/find)
{% endtab %}
{% endtabs %}

### model:findOne\(name, id\)

{% tabs %}
{% tab title="Description" %}
Usage:

```javascript
helper('model:findOne')(name, id, opts)
```
{% endtab %}

{% tab title="Parameters" %}
* `name` _&lt;string&gt;_ **Required**.
* `id` _&lt;string \| integer&gt;_ **Required**.
* `opts` _&lt;Object&gt;_ Default: `{}`
  * `dab` _&lt;object&gt;_ DAB options. Default: `{}`
{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:create

{% tabs %}
{% tab title="Description" %}
Usage:

```javascript
helper('model:create')(name, body, opts)
```
{% endtab %}

{% tab title="Parameters" %}
* `name` _&lt;string&gt;_ **Required**.
* `body` _&lt;Object&gt;_ **Required**.
* `opts` _&lt;Object&gt;_ Default: `{}`

  * `dab` _&lt;object&gt;_ DAB options. Default: `{}`
  * `skipValidation`  _&lt;Object&gt;_ Default: `{}`
  * `skipHook`: _&lt;Object&gt;_ Default: `{}`
    * `beforeValidate` _&lt;boolean&gt;_ Default: `false`
    * `afterValidate` _&lt;boolean&gt;_ Default: `false`
    * `beforeCreate` _&lt;boolean&gt;_ Default: `false`
    * `afterCreate` _&lt;boolean&gt;_ Default: `false`
    * `all` _&lt;boolean&gt;_ Skip all hooks altogether. Default: `false`
{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:update

{% tabs %}
{% tab title="Description" %}
Usage:

```javascript
helper('model:update')(name, id, body, opts)
```
{% endtab %}

{% tab title="Parameters" %}
* `name` _&lt;string&gt;_ **Required**.
* `id` _&lt;string \| integer&gt;_ **Required**.
* `body` _&lt;Object&gt;_ **Required**.
* `opts` _&lt;Object&gt;_ Default: `{}`

  * `dab` _&lt;object&gt;_ DAB options. Default: `{}`
  * `skipValidation`  _&lt;Object&gt;_ Default: `{}`
  * `skipHook` _&lt;Object&gt;_ Default: `{}`
    * `beforeValidate` _&lt;boolean&gt;_ Default: `false`
    * `afterValidate` _&lt;boolean&gt;_ Default: `false`
    * `beforeUpdate` _&lt;boolean&gt;_ Default: `false`
    * `afterUpdate` _&lt;boolean&gt;_ Default: `false`
    * `all` _&lt;boolean&gt;_ Skip all hooks altogether. Default: `false`
{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:remove

{% tabs %}
{% tab title="Description" %}
Usage:

```javascript
helper('model:remove')(name, id, opts)
```
{% endtab %}

{% tab title="Parameters" %}
* `name` _&lt;string&gt;_ **Required**.
* `id` _&lt;string \| integer&gt;_ **Required**.
* `opts` _&lt;Object&gt;_ Default: `{}`

  * `dab` _&lt;object&gt;_ DAB options. Default: `{}`
  * `skipValidation`  _&lt;Object&gt;_ Default: `{}`
  * `skipHook` _&lt;Object&gt;_ Default: `{}`
    * `beforeValidate` _&lt;boolean&gt;_ Default: `false`
    * `afterValidate` _&lt;boolean&gt;_ Default: `false`
    * `beforeRemove` _&lt;boolean&gt;_ Default: `false`
    * `afterRemove` _&lt;boolean&gt;_ Default: `false`
    * `all` _&lt;boolean&gt;_ Skip all hooks altogether. Default: `false`
{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:bulkCreate

{% tabs %}
{% tab title="Description" %}
Usage:

```javascript
helper('model:bulkCreate')(name, body, opts)
```
{% endtab %}

{% tab title="Parameters" %}
* `name` _&lt;string&gt;_ **Required**.
* `body` _&lt;Object&gt;_ **Required**.
* `opts` _&lt;Object&gt;_ Default: `{}`

  * `dab` _&lt;object&gt;_ DAB options. Default: `{}`
  * `skipHook` _&lt;Object&gt;_ Default: `{}`
  * * `beforeBulkCreate` _&lt;boolean&gt;_ Default: `false`
    * `afterBulkCreate` _&lt;boolean&gt;_ Default: `false`
    * `all` _&lt;boolean&gt;_ Skip all hooks altogether. Default: `false`
{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:bulkUpdate

{% tabs %}
{% tab title="Description" %}
Usage:

```javascript
helper('model:bulkUpdate')(name, body, opts)
```
{% endtab %}

{% tab title="Parameters" %}
* `name` _&lt;string&gt;_ **Required**.
* `body` _&lt;Object&gt;_ **Required**.
* `opts` _&lt;Object&gt;_ Default: `{}`

  * `dab` _&lt;object&gt;_ DAB options. Default: `{}`
  * `skipHook` _&lt;Object&gt;_ Default: `{}`
  * * `beforeBulkUpdate` _&lt;boolean&gt;_ Default: `false`
    * `afterBulkUpdate` _&lt;boolean&gt;_ Default: `false`
    * `all` _&lt;boolean&gt;_ Skip all hooks altogether. Default: `false`
{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:bulkRemove

{% tabs %}
{% tab title="Description" %}
Usage:

```javascript
helper('model:bulkRemove')(name, body, opts)
```
{% endtab %}

{% tab title="Parameters" %}
* `name` _&lt;string&gt;_ **Required**.
* `body` _&lt;Object&gt;_ **Required**.
* `opts` _&lt;Object&gt;_ Default: `{}`

  * `dab` _&lt;object&gt;_ DAB options. Default: `{}`
  * `skipHook` _&lt;Object&gt;_ Default: `{}`
  * * `beforeBulkRemove` _&lt;boolean&gt;_ Default: `false`
    * `afterBulkRemove` _&lt;boolean&gt;_ Default: `false`
    * `all` _&lt;boolean&gt;_ Skip all hooks altogether. Default: `false`
{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:copyFrom\(name, src, opts\)

{% tabs %}
{% tab title="Description" %}
Usage:

```javascript
helper('model:copyFrom')(name, src, opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:copyTo\(name, dest, opts\)

{% tabs %}
{% tab title="Description" %}
Usage:

```javascript
helper('model:copyTo')(name, dest, opts)
```
{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:validate\(name, ...args\)

{% tabs %}
{% tab title="Description" %}

{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:get\(name\)

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

### model:getConnector\(name, follow\)

{% tabs %}
{% tab title="Description" %}

{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:getDab\(name\)

{% tabs %}
{% tab title="Description" %}

{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:getHook\(name, hook\)

{% tabs %}
{% tab title="Description" %}

{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}

### model:getSchema\(name\)

{% tabs %}
{% tab title="Description" %}

{% endtab %}

{% tab title="Parameters" %}

{% endtab %}

{% tab title="Return" %}

{% endtab %}
{% endtabs %}



