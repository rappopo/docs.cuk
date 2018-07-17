# View Globals

### csrfToken

{% tabs %}
{% tab title="Description" %}
**csrfToken** is a global variable injected into View Engine. It sole purpose is to provide you easy access of CSRF token inside your view template.
{% endtab %}

{% tab title="Usage" %}
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
{% endtab %}
{% endtabs %}



