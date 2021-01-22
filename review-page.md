---
description: 리뷰 페이지
---

# Review page

{% api-method method="get" host="movie-in-case.com" path="/movie/reviews?mvid=1&loadNum=20" %}
{% api-method-summary %}
Get Reviews
{% endapi-method-summary %}

{% api-method-description %}
해당 url mvid와 일치하는 영화의 리뷰 정보를 받음
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="mvid" type="string" required=false %}
리뷰 정보를 가져올 영화의 movie\_id
{% endapi-method-parameter %}

{% api-method-parameter name="loadNum" type="integer" required=false %}
가져올 리뷰 숫자
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "success": true,
    "result": [
        {
            "review_id": 8,
            "review_name": "review_name 6",
            "review_rating": 3,
            "review_comment": "review_comment 6",
            "review_picture": null,
            "review_time": "2020-12-21T14:01:19.000Z"
        },
        {
            "review_id": 2,
            "review_name": "review_name 2",
            "review_rating": 5,
            "review_comment": "review_comment 2",
            "review_picture": null,
            "review_time": "2020-12-17T14:12:13.000Z"
        },
        {
            "review_id": 1,
            "review_name": "review_name 1",
            "review_rating": 4,
            "review_comment": "review_comment 1",
            "review_picture": "review_picture 1",
            "review_time": "2020-12-17T14:11:28.000Z"
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
    "message": "get review not found"    
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="movie-in-case.com" path="/user/reviewAcc?mvid=1" %}
{% api-method-summary %}
Get Review Access
{% endapi-method-summary %}

{% api-method-description %}
해당 리뷰를 작성하기 위한 권한 체크
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="mvid" type="integer" required=false %}
작성할려고 하는 영화 id
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
d작성할려고 하는 사용자 email
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
리뷰 작성 권한 반환 \(영화 시청중/0 , 시청완료/1 반환\)
{% endapi-method-response-example-description %}

```
{
    "success": true,
    "result": [
        {
            "movie_id": 1,
            "user_email": "user_email 1",
            "progress_movie": 1
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
    "message": "get review access data not found"    
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case.com" path="/movie/saveReview?mvid=1" %}
{% api-method-summary %}
Post Review
{% endapi-method-summary %}

{% api-method-description %}
리뷰 작성내용 서버 전송
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="mvid" type="integer" required=false %}
작성한 리뷰의 영화 id
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=false %}
리뷰를 작성하는 사용자 name
{% endapi-method-parameter %}

{% api-method-parameter name="rating" type="integer" required=false %}
리뷰 평점
{% endapi-method-parameter %}

{% api-method-parameter name="comment" type="string" required=false %}
리뷰 내용
{% endapi-method-parameter %}

{% api-method-parameter name="picture" type="string" required=false %}
리뷰 사진 
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "success": true,
    "result": {
        "fieldCount": 0,
        "affectedRows": 1,
        "insertId": 9,
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

{% endapi-method-response-example-description %}

```
{    
    "success" : false,
    "message": "post review data not found"    
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



