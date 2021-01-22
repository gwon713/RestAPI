---
description: '영화 포스터, 정보'
---

# Home

{% api-method method="get" host="movie-in-case" path="/movie/info" %}
{% api-method-summary %}
Get Movie info
{% endapi-method-summary %}

{% api-method-description %}
 메인화면 정보를 서버에서 가져옴
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
메인화면에 표시될 정보보내기\(\*순서 바뀔수 있음\) movie\_review\_num db 추가x
{% endapi-method-response-example-description %}

```
[
    {    
        "movie_id" : 1 , 
        "movie_name" : "피금화", 
        "movie_rating_avg" : 4.7 , 
        "movie_review_num" : 120 , 
        "movie_plot" : "줄거리" , 
        "movie_genre" : "추리" , 
        "movie_difficulty" : "하" , 
        "movie_poster" : "image link" ,
        "message": "get movie info success"
    },
    {    
        "movie_id" : 2 , 
        "movie_name" : "피금화2", 
        "movie_rating_avg" : 4.3 , 
        "movie_review_num" : 180 , 
        "movie_plot" : "줄거리" , 
        "movie_genre" : "공" , 
        "movie_difficulty" : "하" , 
        "movie_poster" : "image link" ,
        "message": "get movie info success"
    }
]
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "get movie info not found"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



