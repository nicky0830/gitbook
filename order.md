# Order

{% swagger method="post" path="/order/{:user_id}/buy" baseUrl="https://server" summary="상세 설명 페이지 - 구매 " %}
{% swagger-description %}
buy button click
{% endswagger-description %}
{% endswagger %}

{% swagger method="post" path="order/{:user_id}/borrow" baseUrl="https://server/" summary="상세 설명 페이지 - 대여" %}
{% swagger-description %}
borrow button click 
{% endswagger-description %}
{% endswagger %}

{% swagger method="post" path="/order/{:user_id}/sell" baseUrl="https://server" summary="상세 상품 페이지 - 판매" %}
{% swagger-description %}
ㄴㅣsell buttom click
{% endswagger-description %}
{% endswagger %}

{% swagger method="get" path="/order/{:user_id}/sell-history" baseUrl="https://server" summary="Mypage - 판매내역" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% swagger method="get" path="/order/{:user_id}/buy-history" baseUrl="https://server" summary="Mypage - 구매내역" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% swagger method="get" path="/order/{:user_id}/borrow-history" baseUrl="https://server" summary="Mypage - 대여내역" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% swagger method="get" path="/order/{:user_id}/borrow-cart" baseUrl="https://server" summary="관심상품 - 대여" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

{% swagger method="get" path="/order/{:user_id}/buy-cart" baseUrl="https://server" summary="관심상품-구매" %}
{% swagger-description %}

{% endswagger-description %}
{% endswagger %}

