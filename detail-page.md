---
description: 영화 상세페이지
---

# Detail page

{% api-method method="get" host="movie-in-case.com" path="/movie/detail?mvid=1" %}
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

{% endapi-method-response-example-description %}

```
{
    "success": true,
    "result": [
        {
            "detail_poster": "detail_poster 1",
            "movie_name": "movie_name 1",
            "movie_genre": "movie_genre 1",
            "detail_running_time": "detail_running_time 1",
            "movie_difficulty": "movie_difficulty 1",
            "detail_place": "detail_place 1",
            "detail_price": "0",
            "detail_plot": "detail_plot 1",
            "review_liked": 15,
            "review_unliked": 17,
            "liked_percent": 47,
            "movie_review_num": 32
        }
    ]
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
.
{% endapi-method-response-example-description %}

```
{   
    "success" : false, 
    "message": "get detail not found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



