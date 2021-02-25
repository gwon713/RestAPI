---
description: '영화 포스터, 정보'
---

# Home

{% api-method method="get" host="movie-in-case.com" path="/movie/info" %}
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
{
    "success": true,
    "result": [
        {
            "movie_id": 2,
            "movie_name": "movie_name 2",
            "liked_percent": 0,
            "movie_plot": "movie_plot 2",
            "movie_genre": "movie_genre 2",
            "movie_difficulty": "movie_difficulty 2",
            "movie_poster": "breakfast.jpg",
            "detail_place": "detail_place 2"
        },
        {
            "movie_id": 3,
            "movie_name": "movie_name 3",
            "liked_percent": 67,
            "movie_plot": "movie_plot 3",
            "movie_genre": "movie_genre 3",
            "movie_difficulty": "movie_difficulty 3",
            "movie_poster": "balloons.jpg",
            "detail_place": "detail_place 3"
        },
        {
            "movie_id": 1,
            "movie_name": "movie_name 1",
            "liked_percent": 54,
            "movie_plot": "movie_plot 1",
            "movie_genre": "movie_genre 1",
            "movie_difficulty": "movie_difficulty 1",
            "movie_poster": "Pygmalion_Part1.PNG",
            "detail_place": "detail_place 1"
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
    "message": "get movie info not found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



