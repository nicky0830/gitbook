# Item

{% swagger method="get" path="/item/{:user_id}/fav" baseUrl="https://server" summary="랜딩 페이지 선호 브랜드" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name=":user_fav" %}

{% endswagger-parameter %}

{% swagger-parameter in="header" name="Authorization" %}
accessToken&#x20;

if expired, req.cookies -> refreshToken

ㅜ n ew accessTioken&#x20;
{% endswagger-parameter %}

{% swagger-response status="200: OK" description="get user's favorite brand items" %}
```javascript
{
   fav_brands : [
   {id:"id", 
   name: "name", 
   price: "buy_price", 
   img : "img"
   }, 
   {id:"id", 
   name: "name", 
   price: "buy_price", 
   img : "img"},
   ...,
    {id:"id", 
   name: "name", 
   price: "buy_price", 
   img : "img"}
   
   ]
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```
err
```


{% endswagger-response %}
{% endswagger %}

{% swagger method="get" path="/item/popular" baseUrl="https://server" summary="랜딩 페이지 인기브랜드" %}
{% swagger-description %}
4개씩 보내고 더보기 누르면 4개씩 더 보내 
{% endswagger-description %}

{% swagger-response status="200: OK" description="" %}
```javascript
{
    popular : [
    {item_id, img, name, price},
     {item_id, img, name, price},
      {item_id, img, name, price},
       {item_id, img, name, price}
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

{% swagger method="get" path="/item/{:item_id}" baseUrl="https://server" summary="랜딩페이지  제품 선택 -> 상세 설명 페이지 " %}
{% swagger-description %}
선제품 선택 시 요청
{% endswagger-description %}

{% swagger-parameter in="path" name=":item_id" type="string" %}

{% endswagger-parameter %}

{% swagger-response status="200: OK" description="상세 상품 페이지에서 " %}
```javascript
{ 
"item_id": “item_id”, 
"name": "name",
"size": “size”, 
"grade": “grade”
}
```
{% endswagger-response %}

{% swagger-response status="500: Internal Server Error" description="" %}
```javascript
err
```
{% endswagger-response %}
{% endswagger %}
