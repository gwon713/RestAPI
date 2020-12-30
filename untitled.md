---
description: 영화 결제 페이지
---

# Payment page

{% api-method method="get" host="movie-in-case" path="/user/payment?mvid=1&email=gildong@naver.com" %}
{% api-method-summary %}
Get Payment
{% endapi-method-summary %}

{% api-method-description %}
결제 여부 정보를 서버에서 가져옴
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="mvid" type="string" required=false %}
구매여부 확인할 영화 id
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
구매여부 확인할 사용자 email
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
d영화 구매 했으면 movie\_purchase 1 안했으면 0
{% endapi-method-response-example-description %}

```
{    
    "user_email": "gildong@naver.com",    
    "movie_id": 1,    
    "message" : "get purchase success"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "get purchase not found"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case" path="/user/payment?mvid=1&email=gildong@naver.com" %}
{% api-method-summary %}
Post Payment
{% endapi-method-summary %}

{% api-method-description %}
결제처리된 정보를 서버로 추가
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="mvid" type="integer" required=false %}
결제할 영화의 id
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
결제 요청을 보낸 사용자 email
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
movie\_purchase \(비구매/0 , 구매/1\)
{% endapi-method-response-example-description %}

```
{    
    "user_email": "gildong@naver.com",   
    "movie_id": 1,    
    "message" : "post payment request success"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    "message": "post payment request not found"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

