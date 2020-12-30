---
description: 영화 상세페이지
---

# Detail page

{% api-method method="get" host="movie-in-case" path="/movie/detail?mvid=1" %}
{% api-method-summary %}
Get Detail
{% endapi-method-summary %}

{% api-method-description %}
상세 정보 서버에서 가져옴
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="mvid" type="integer" required=false %}
상세 정보를 보려고하는 영화의 id
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
movie\_review\_num은 db추가 x
{% endapi-method-response-example-description %}

```
{   
    "detail_poster" : "image link", 
    "movie_name" : "피금화" , 
    "movie_genre" : "추리" , 
    "detail_running_time" : "20~40분" , 
    "movie_difficulty" : "하" , 
    "detail_place" : "실내" , 
    "detail_price" : "무료" , 
    "detail_plot" : "추리 줄거리 인사동 줄거리 추리추리추리 줄거리" , 
    "movie_rating_avg" : 4.7 , 
    "movie_review_num" : 120 ,
    "message": "get detail success"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
.
{% endapi-method-response-example-description %}

```
{    "message": "get detail not found"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



