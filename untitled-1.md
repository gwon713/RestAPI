---
description: 영화 시청 화면
---

# Unity

{% api-method method="get" host="movie-in-case" path="/movie/progress?mvid=1&email=gildong@naver.com" %}
{% api-method-summary %}
Get Progress
{% endapi-method-summary %}

{% api-method-description %}
현재 영화 진행 상황 가져오기
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="mvid" type="integer" required=false %}
진행 상황을 가져올 영화 id
{% endapi-method-parameter %}

{% api-method-parameter name="email " type="string" required=false %}
진행 상황에 해당되는 사용자 email
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "user_email": "dildong@naver.com", 
    "movie_id": 1,    
    "progress_movie" : 0,
    "clip_info" : clip_info.json,
    "progress_clip_info" : progressClipInfo.json,
    "progress_last_num" : 4,
    "message" : "get progress success"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "get progress not found"    }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case" path="/movie/progress?mvid=1&email=gildong@naver.com" %}
{% api-method-summary %}
Post Progress
{% endapi-method-summary %}

{% api-method-description %}
영화 진행상황 추가
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="mvid" type="integer" required=false %}
진행 상황을 추가할 영화 id
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
진행 상황을 추가할 영화 사용자 email
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="progress\_last\_num" type="number" required=false %}
마지막으로 시청한 클립 번호
{% endapi-method-parameter %}

{% api-method-parameter name="progress\_movie" type="boolean" required=false %}
영화 시청 여부\(시청중/0 시청완료/1\)
{% endapi-method-parameter %}

{% api-method-parameter name="progress\_clip\_info" type="string" required=false %}
영화 진행 상
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "user_email": "gildong@naver.com",
    "movie_id": 1,    
    "progress_movie" : 0,
    "clip_info" : clip_info.json,
    "progress_clip_info" : progressClipInfo.json,
    "progress_last_num" : 0,
    "message" : "post progress success"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "post progress not found"    }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="movie-in-case" path="/movie/progress?mvid=1&email=gildong@naver.com" %}
{% api-method-summary %}
Put Progress
{% endapi-method-summary %}

{% api-method-description %}
영화 진행상황 업데이트
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="mvid" type="integer" required=false %}
진행 상황을 수정할 영화 id
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
진행 상황을 수정할 영화 사용자 email
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="progress\_last\_num" type="number" required=false %}
마지막으로 시청한 클립 번호
{% endapi-method-parameter %}

{% api-method-parameter name="progress\_movie" type="boolean" required=false %}
영화 시청 여부\(시청중/0 시청완료/1\)
{% endapi-method-parameter %}

{% api-method-parameter name="progress\_clip\_info" type="string" required=false %}
영화 진행 상황
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
progress
{% endapi-method-response-example-description %}

```
{    
    "user_email": "gildong@naver.com", 
    "movie_id": 1,       
    "progress_movie" : 1,
    "clip_info" : clip_info.json,
    "progress_clip_info" : progressClipInfo.json,
    "progress_last_num" : 6,
    "message" : "put progress success"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "put progress not found"    }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

