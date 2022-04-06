---
description: 사용자 정보
---

# User

{% swagger method="post" path="" baseUrl="https://server" summary="Login" %}
{% swagger-description %}
Login용 
{% endswagger-description %}

{% swagger-parameter in="path" name="login " %}

{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="password " type="int" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="response user data table" %}
```javascript
{
    "id": PK,
    "user_id": "user_id",
    "username": "username",
    "email": "email",
    "password": "password",
    "phonenumber": "phonenumber",
    "fav_brand" : "fav_brand",
    "createdAt": "created time",
    "updatedAt": "updated time"
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="Wrong request" %}
```javascript
{ "Invalid user or Wrong password" }
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}
