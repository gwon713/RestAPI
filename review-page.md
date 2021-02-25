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
            "review_id": 43,
            "review_name": "RN_test1",
            "review_liked": 0,
            "review_comment": "Aa",
            "review_picture": null,
            "review_time": "2021-02-03T19:40:54.000Z"
        },
        {
            "review_id": 42,
            "review_name": "RN_test1",
            "review_liked": 0,
            "review_comment": "Tt",
            "review_picture": null,
            "review_time": "2021-02-03T19:18:16.000Z"
        },
        {
            "review_id": 41,
            "review_name": "RN_test1",
            "review_liked": 0,
            "review_comment": "ㄴ",
            "review_picture": null,
            "review_time": "2021-02-03T19:14:17.000Z"
        },
        {
            "review_id": 40,
            "review_name": "RN_test1",
            "review_liked": 1,
            "review_comment": "ㅠ",
            "review_picture": null,
            "review_time": "2021-02-03T18:14:29.000Z"
        },
        {
            "review_id": 39,
            "review_name": "RN_test1",
            "review_liked": 1,
            "review_comment": "A",
            "review_picture": null,
            "review_time": "2021-02-03T17:58:20.000Z"
        },
        {
            "review_id": 38,
            "review_name": "RN_test1",
            "review_liked": 1,
            "review_comment": "Test",
            "review_picture": null,
            "review_time": "2021-02-03T17:56:34.000Z"
        },
        {
            "review_id": 37,
            "review_name": "RN_test1",
            "review_liked": 0,
            "review_comment": "Cc",
            "review_picture": null,
            "review_time": "2021-02-03T17:50:17.000Z"
        },
        {
            "review_id": 36,
            "review_name": "RN_test1",
            "review_liked": 1,
            "review_comment": "Aw",
            "review_picture": null,
            "review_time": "2021-02-03T17:47:12.000Z"
        },
        {
            "review_id": 35,
            "review_name": "RN_test1",
            "review_liked": 1,
            "review_comment": "Ga",
            "review_picture": null,
            "review_time": "2021-02-03T17:46:09.000Z"
        },
        {
            "review_id": 34,
            "review_name": "RN_test1",
            "review_liked": 0,
            "review_comment": "Asf",
            "review_picture": null,
            "review_time": "2021-02-03T17:17:03.000Z"
        },
        {
            "review_id": 32,
            "review_name": "RN_test1",
            "review_liked": 0,
            "review_comment": "22",
            "review_picture": null,
            "review_time": "2021-02-03T00:45:47.000Z"
        },
        {
            "review_id": 31,
            "review_name": "RN_test1",
            "review_liked": 1,
            "review_comment": "21",
            "review_picture": null,
            "review_time": "2021-02-03T00:11:07.000Z"
        },
        {
            "review_id": 30,
            "review_name": "RN_test1",
            "review_liked": 1,
            "review_comment": "20",
            "review_picture": "RN_test1_1612342108.jpg",
            "review_time": "2021-02-02T23:48:28.000Z"
        },
        {
            "review_id": 29,
            "review_name": "RN_test1",
            "review_liked": 1,
            "review_comment": "19",
            "review_picture": null,
            "review_time": "2021-02-02T23:46:25.000Z"
        },
        {
            "review_id": 28,
            "review_name": "RN_test1",
            "review_liked": 0,
            "review_comment": "18",
            "review_picture": "RN_test1_1612341953.jpg",
            "review_time": "2021-02-02T23:45:54.000Z"
        },
        {
            "review_id": 27,
            "review_name": "RN_test1",
            "review_liked": 0,
            "review_comment": "17",
            "review_picture": "RN_test1_1612341907.jpg",
            "review_time": "2021-02-02T23:45:08.000Z"
        },
        {
            "review_id": 26,
            "review_name": "RN_test1",
            "review_liked": 1,
            "review_comment": "16",
            "review_picture": "RN_test1_1612341710.jpg",
            "review_time": "2021-02-02T23:41:51.000Z"
        },
        {
            "review_id": 25,
            "review_name": "RN_test1",
            "review_liked": 0,
            "review_comment": "15",
            "review_picture": "RN_test1_1612341660.jpg",
            "review_time": "2021-02-02T23:41:02.000Z"
        },
        {
            "review_id": 24,
            "review_name": "RN_test1",
            "review_liked": 1,
            "review_comment": "14",
            "review_picture": "RN_test1_1612341572.jpg",
            "review_time": "2021-02-02T23:39:32.000Z"
        },
        {
            "review_id": 23,
            "review_name": "RN_test1",
            "review_liked": 0,
            "review_comment": "13",
            "review_picture": "RN_test1_1612341447.jpg",
            "review_time": "2021-02-02T23:37:27.000Z"
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

{% api-method method="post" host="movie-in-case.com" path="/user/reviewAcc?mvid=1" %}
{% api-method-summary %}
Post Review Access
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

{% api-method-parameter name="liked" type="boolean" required=false %}
리뷰  좋아요\(1\) 싫어요\(0\)
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



