# Like

{% swagger method="get" path="/like/{:user_id}/buy" baseUrl="https://server" summary="장바구니 페이지 - 구매" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
   buyCart: [
   {item_id, 
   item_size, 
   item_grade, 
   item_name
   }, 
    {item_id, 
   item_size, 
   item_grade, 
   item_name
   }
   ...
    {item_id, 
   item_size, 
   item_grade, 
   item_name
   }
   ]
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "you need to login"
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/like/{:user_id}/borrow" baseUrl="https://server" summary="장바구니 페이지 - 대여" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
   buyCart: [
   {item_id, 
   item_size, 
   item_grade, 
   item_name
   }, 
    {item_id, 
   item_size, 
   item_grade, 
   item_name
   }
   ...
    {item_id, 
   item_size, 
   item_grade, 
   item_name
   }
   ]
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
    "you need to login"
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/like/{:user_id}/buy" baseUrl="https://server" summary="상세 상품 페이지 - 구매 관심상품" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="user_id" type="int" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="item_id" type="int" %}

{% endswagger-parameter %}

{% swagger-response status="201: Created" description="" %}
```javascript
{
 `${item_id} is in buyCart`
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
   'You need to login'
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}

{% swagger method="post" path="/like/{:user_id}/borrow" baseUrl="https://server" summary="상세 상품 페이지 - 대여 관심상품" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="body" name="user_id" type="int" %}

{% endswagger-parameter %}

{% swagger-parameter in="body" name="item_id" type="int" %}

{% endswagger-parameter %}

{% swagger-response status="201: Created" description="" %}
```javascript
{
 `${item_id} is in buyCart`
}
```
{% endswagger-response %}

{% swagger-response status="401: Unauthorized" description="" %}
```javascript
{
  'You need to login'
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}

