# Order

{% swagger method="post" path="/order/{:user_id}/buy" baseUrl="https://server" summary="상세 설명 페이지 - 구매 " %}
{% swagger-description %}
buy button click, 구Mygpa      Mypage의 구매내역ㅠ
{% endswagger-description %}

{% swagger-parameter in="body" name="user_id" type="int" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="item_id" type="int" %}

{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
accessToken
{% endswagger-parameter %}

{% swagger-response status="201: Created" description="" %}
```javascript
{
 " `${item_name}` bought successfully" 
 }
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "you need to login to buy this"// Response
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="order/{:user_id}/borrow" baseUrl="https://server/" summary="상세 설명 페이지 - 대여" %}
{% swagger-description %}
borrow button click 
{% endswagger-description %}

{% swagger-parameter in="body" name="user_id" type="int" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="item_id " type="int" %}

{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization " type="string" %}
accessToken
{% endswagger-parameter %}

{% swagger-response status="201: Created" description="" %}
```javascript
{
 " `${item_name}` borrowed successfully" 
 }
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "you need to login to borrow this"// Response
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/order/{:user_id}/sell" baseUrl="https://server" summary="상세 상품 페이지 - 판매" %}
{% swagger-description %}
ㄴㅣsell buttom click
{% endswagger-description %}

{% swagger-parameter in="body" name="user_id" type="int" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="item_id" type="int" %}

{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
accessToken
{% endswagger-parameter %}

{% swagger-response status="201: Created" description="" %}
```javascript
{
 " `${item_name}` sold successfully" 
 }
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "you need to login to sell this"// Response
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/order/{:user_id}/sell" baseUrl="https://server" summary="Mypage - 판매내역" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
accessToken
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
  sellHistory : [
  { "id":"id", 
   "user_id":"user_id",
   // user table id
   // signup user id 아이 user _id  
   "item_name" : "item_name",
   "createdAt" : "createdAt",
   "item_grade" : "item_grade", 
   "item_size" : "item_size", 
   "item_price" : "item_price"
   }, 
   ...
   {}
   
   ]
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/order/{:user_id}/buy" baseUrl="https://server" summary="Mypage - 구매내역" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
accessToken
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
  buyHistory : [
  { "id":"id", 
   "user_id":"user_id",
   // user table id
   // signup user id 아이 user _id  
   "item_id" : "item_id",
   "item_name" : "item_name",
   "createdAt" : "createdAt",
   "item_grade" : "item_grade", 
   "item_size" : "item_size", 
    "item_price" : "item_price"
   }, 
   ..., 
   { "id":"id", 
   "user_id":"user_id",
   // user table id
   // signup user id 아이 user _id  
   "item_id" : "item_id",
   "item_name" : "item_name",
   "createdAt" : "createdAt",
   "item_grade" : "item_grade", 
   "item_size" : "item_size", 
    "item_price" : "item_price"
   }, 
   
   ]
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/order/{:user_id}/borrow" baseUrl="https://server" summary="Mypage - 대여내역" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="header" name="Authorization" type="string" %}
accessToken
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
  borrowHistory : [
  { "id":"id", 
   "user_id":"user_id",
   // user table id
   // signup user id 아이 user _id  
   "item_id" : "item_id",
   "item_name" : "item_name",
   "createdAt" : "createdAt",
   "item_grade" : "item_grade", 
   "item_size" : "item_size", 
    "item_price" : "item_price"
   }, 
   ..., 
   { "id":"id", 
   "user_id":"user_id",
   // user table id
   // signup user id 아이 user _id  
   "item_id" : "item_id",
   "item_name" : "item_name",
   "createdAt" : "createdAt",
   "item_grade" : "item_grade", 
   "item_size" : "item_size", 
    "item_price" : "item_price"
   }, 
   
   ]
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}

