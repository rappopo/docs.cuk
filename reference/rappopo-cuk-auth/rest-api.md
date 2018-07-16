# REST Api

{% api-method method="post" host="http://mydomain.com" path="/api/auth/jwt.:ext" %}
{% api-method-summary %}
create:auth:/jwt
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-path-parameters %}
{% api-method-parameter name="ext" type="string" required=true %}
Result format
{% endapi-method-parameter %}
{% endapi-method-path-parameters %}

{% api-method-query-parameters %}
{% api-method-parameter name="lang" type="string" required=false %}
Language
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="username" type="string" required=true %}
User login
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
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



