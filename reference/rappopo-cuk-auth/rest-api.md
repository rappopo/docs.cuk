# REST Api

{% api-method method="post" host="/api/auth/jwt" path="" %}
{% api-method-summary %}
Create new JSON Web Token
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="username" type="string" required=true %}
Username
{% endapi-method-parameter %}

{% api-method-parameter name="passwd" type="string" required=true %}
User password
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```javascript
{
  "success": true,
  "data": {
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJmaXJzdF9uYW1lIjoiSmFtZXMiLCJsYXN0X25hbWUiOiJCb25kIn0.kDGk8rSdnueu9bNofaJbGlIXHA3tDmWrtv-7161XX-Q"
  }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

