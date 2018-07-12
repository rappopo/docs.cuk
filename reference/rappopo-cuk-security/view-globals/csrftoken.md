# csrfToken

This global variable is injected into View Engine so you could use it any time anywhere inside your template easily.

### Usage

Your route file:

{% code-tabs %}
{% code-tabs-item title="test.js" %}
```javascript
...
return {
  method: 'POST',
  middleware: 'security:csrf',
  handler: ctx => {
    ctx.render('/test')
  }
}
...
  
```
{% endcode-tabs-item %}
{% endcode-tabs %}

Your view template:

{% code-tabs %}
{% code-tabs-item title="test.html" %}
```markup
{% extends '/layout' %}
<form method="POST">
  <input type="hidden" name="_csrf" value="{{ securityCsrfToken }}">
  ...
</form>
```
{% endcode-tabs-item %}
{% endcode-tabs %}

