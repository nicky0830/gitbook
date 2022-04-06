# Item

{% swagger method="get" path="/items" baseUrl="https://server" summary="랜딩 페이지 선호 브랜드" %}
{% swagger-description %}

{% endswagger-description %}

{% swagger-parameter in="path" name=":user_fav" %}

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
{% endswagger %}

{% swagger method="get" path="/items/popular" baseUrl="https://server" summary="랜딩 페이지 인기브랜드" %}
{% swagger-description %}
랜ㅓ
{% endswagger-description %}
{% endswagger %}
