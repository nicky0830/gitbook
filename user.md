---
description: 사용자 정보
---

# User

{% swagger method="post" path="/users/login" baseUrl="https://server" summary="Login" %}
{% swagger-description %}
Login 성공 시 기입한 id, pw 일치하는 user 정보 찾아서 돌려주기
{% endswagger-description %}

{% swagger-parameter in="path" name="login " %}

{% endswagger-parameter %}

{% swagger-parameter in="body" required="true" name="email" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="password " type="int" required="true" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="response user data table" %}
```javascript
{
    "id": PK,
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

{% swagger method="post" path="/users/signout" baseUrl="https://server" summary="Signout" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name="signout" %}

{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization " %}
//req.cookie에 있는 ㄱrefreshToken    brwoToken
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{ "successfully signed out!" }
```
{% endswagger-response %}

{% swagger-response status="400: Bad Request" description="" %}
```javascript
{ "you're currently not logined" }
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/users/signup" baseUrl="https://server" summary="Signup" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="id" type="int" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="name" type="string" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="email" type="string" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="password" type="int" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="phone_number" type="int" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="fav_brand" type="string" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
1
```
{% endswagger-response %}

{% swagger-response status="201" description="" %}
```javascript
{
    "id": PK,
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

{% swagger-response status="409: Conflict" description="" %}
```javascript
{ "이미 존재하는 아이입니다." }
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}

