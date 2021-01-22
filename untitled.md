---
description: 영화 결제 페이지
---

# Payment page

{% api-method method="get" host="movie-in-case.com" path="/user/payment?mvid=1" %}
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
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
구매여부 확인할 사용자 email
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
영화 구매 했으면 movie\_purchase 1 안했으면 0
{% endapi-method-response-example-description %}

```
{
    "success": true,
    "result": [
        {
            "user_email": "user_email 1",
            "movie_id": 1
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{   
    "success" : false, 
    "message": "get purchase not found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case.com" path="/user/payment?mvid=1" %}
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
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
결제 요청을 보낸 사용자 email
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
movie\_purchase \(비구매/0 , 구매/1\)
{% endapi-method-response-example-description %}

```
{
    "success": true,
    "result": {
        "fieldCount": 0,
        "affectedRows": 1,
        "insertId": 4,
        "serverStatus": 2,
        "warningCount": 0,
        "message": "",
        "protocol41": true,
        "changedRows": 0
    }
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
Could not find a cake matching this query.
{% endapi-method-response-example-description %}

```
{    
    "success" : false,
    "message": "post payment request not found"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=500 %}
{% api-method-response-example-description %}
중복된 결제정보가 입력되었을 때
{% endapi-method-response-example-description %}

```
err : Error: ER_DUP_ENTRY: Duplicate entry 'user_email 1-1' for key 'movie_purchase.user_email'
message : Internal Server Error
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

