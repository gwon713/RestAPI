---
description: 리뷰 페이지
---

# Review page

{% api-method method="get" host="movie-in-case" path="/movie/reviews?mvid=1&loadNum=20" %}
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
[
    {    
      "review_num" : 1,    
      "review_name" : "gildong",
      "review_movie_id" : 1,
      "review_rating" : 4,
      "review_comment" : "인사동 구석구석 돌아보고 있으니 어떤 분들이 혹시 무비인케이스....",
      "review_picture" : "image link",
      "review_time" : "20200502-09:20"
      "message": "get review success"
    },
    {    
      "review_num" : 2,    
      "review_name" : "reviewer",
      "review_movie_id" : 1,
      "review_rating" : 5,
      "review_comment" : "재미있었습니다 ....",
      "review_picture" : "image link",
      "review_time" : "20200503-17:10"
      "message": "get review success"
    }
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "get review not found"    }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="get" host="movie-in-case" path="/user/reviewAcc?mvid=1&email=gildong@naver.com" %}
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

{% api-method-parameter name="email" type="string" required=false %}
작성할려고 하는 사용자email
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
리뷰 작성 권한 반환 \(영화 시청중/0 , 시청완료/1 반환\)
{% endapi-method-response-example-description %}

```
{    
    "movie_id" : 1,
    "user_email" : "gildong@naver.com",
    "progress_movie" : 1,
    "message": "get review access success"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "get review access data not found"    }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case" path="/movie/saveReview?mvid=1" %}
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
    "review_id" : 1,    
    "review_name" : "gildong",
    "review_movie_id" : 1,
    "review_rating" : 5,
    "review_comment" : "인사동 구석구석 돌아보고 있으니 어떤 분들이 혹시 무비인케이스....",
    "review_picture" : "image link",
    "review_time" : "20201210-13:40",
    "message" : "post review success"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "post review data not found"    }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



