---
description: 영화 시청 화면
---

# Unity

{% api-method method="post" host="movie-in-case.com" path="/movie/progress?mvid=1" %}
{% api-method-summary %}
Post Progress
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
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
진행 상황에 해당되는 사용자 email
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
    "result": [
        {
            "user_email": "test_email",
            "movie_id": 0,
            "progress_movie": 0,
            "progress_last_num": 2,
            "progress_last_card_num": 0,
            "clip_info": "{\"Datas\": [{\"Id\": 0, \"Type\": \"Bifurcation\", \"Title\": \" 1 Intro\", \"MovieURL\": \"https://youtu.be/Co7qAMcI6aM\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_0.png\", \"Interactions\": [{\"Type\": \"Vibration\", \"When\": 54, \"During\": 6}, {\"Type\": \"Choice\", \"When\": 101, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 1, \"Type\": \"Ending\", \"Title\": \" 2-1\", \"MovieURL\": \"https://youtu.be/Ks7gc4-6fm4\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_1.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 2, \"Type\": \"Bifurcation\", \"Title\": \" 2-2\", \"MovieURL\": \"https://youtu.be/8_MebjI4yjQ\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_2.png\", \"Interactions\": [{\"Type\": \"Vibration\", \"When\": 52, \"During\": 4}, {\"Type\": \"Notification\", \"When\": 112, \"During\": 2}, {\"Type\": \"Choice\", \"When\": 165, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 3, \"Type\": \"Bifurcation\", \"Title\": \" 3-1 헤비메탈\", \"MovieURL\": \"https://youtu.be/WphZ3EfOwKs\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_3.png\", \"Interactions\": [{\"Type\": \"Vibration\", \"When\": 207, \"During\": 2}, {\"Type\": \"Choice\", \"When\": 263, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 4, \"Type\": \"Bifurcation\", \"Title\": \" 3-2 클래식\", \"MovieURL\": \"https://youtu.be/PiyPfIkeQuc\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_4.png\", \"Interactions\": [{\"Type\": \"Vibration\", \"When\": 207, \"During\": 2}, {\"Type\": \"Choice\", \"When\": 263, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 5, \"Type\": \"Ending\", \"Title\": \" 4-1 대표가 범인이다\", \"MovieURL\": \"https://youtu.be/wrRlc_myLZs\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_5.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 6, \"Type\": \"Bifurcation\", \"Title\": \" 4-2 케이론이 범인이다\", \"MovieURL\": \"https://youtu.be/eV9KNX5JMQw\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_6.png\", \"Interactions\": [{\"Type\": \"Choice\", \"When\": 80, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 7, \"Type\": \"Ending\", \"Title\": \" 5-1 딸로 대체할 수 있다\", \"MovieURL\": \"https://youtu.be/VoJi6reMpIk\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_7.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 8, \"Type\": \"Content\", \"Title\": \" 5-2 딸로 대체할 수 없다\", \"Content\": {\"Name\": \"EscapeGame\", \"Type\": \"Game\", \"PlaceType\": \"InDoor\", \"PopUpText\": \"게임이 시작됩니다.\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_EscapeGame.png\"}, \"MovieURL\": \"https://youtu.be/sQS-wTR5Qjg\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_8.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 9, \"Type\": \"Bifurcation\", \"Title\": \" 6-1 게임에서 이김\", \"MovieURL\": \"https://youtu.be/sVIsOmv3HvQ\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_9.png\", \"Interactions\": [{\"Type\": \"Choice\", \"When\": 98, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 10, \"Type\": \"Ending\", \"Title\": \" 6-2 게임에서 짐\", \"MovieURL\": \"https://youtu.be/BVBInBH3qIA\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_10.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 11, \"Type\": \"Ending\", \"Title\": \" 7-1 나를 초기화 한다\", \"MovieURL\": \"https://youtu.be/kvuvxPztxmE\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_11.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 12, \"Type\": \"Content\", \"Title\": \" 7-2 탈출한다\", \"Content\": {\"Name\": \"ChironAR\", \"Type\": \"AR\", \"PlaceType\": \"InDoor\", \"PopUpText\": \"AR이 시작됩니다.\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_ChironAR.png\"}, \"MovieURL\": \"https://youtu.be/FcB0VoyIa04\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_12.png\", \"Interactions\": [{\"Type\": \"Call\", \"When\": 56, \"During\": 3}], \"NoneChoiceNextId\": -1}, {\"Id\": 13, \"Type\": \"AutoPlay\", \"Title\": \"자동 게임영상_Win\", \"MovieURL\": \"https://youtu.be/aEs5QrgdJFY\", \"NoneChoiceNextId\": 9}, {\"Id\": 14, \"Type\": \"AutoPlay\", \"Title\": \"자동 게임영상_Lose\", \"MovieURL\": \"https://www.youtube.com/watch?v=VPGmpsR7ncM\", \"NoneChoiceNextId\": 10}]}",
            "choice_info": "{\"Datas\": [{\"Type\": \"Text_Free\", \"ClipId\": 0, \"Choices\": [{\"Pos\": {\"PosX\": -500, \"PosY\": 400}, \"Words\": \"이 상태로 출시한다\", \"NextId\": 1}, {\"Pos\": {\"PosX\": 500, \"PosY\": -400}, \"Words\": \"완벽히 케이론을 만든다\", \"NextId\": 2}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 2, \"Choices\": [{\"Words\": \"헤비메탈 음악\", \"NextId\": 3}, {\"Words\": \"클래식 음악\", \"NextId\": 4}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 3, \"Choices\": [{\"Words\": \"대표가 범인이다\", \"NextId\": 5}, {\"Words\": \"케이론이 범인이다\", \"NextId\": 6}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 4, \"Choices\": [{\"Words\": \"대표가 범인이다\", \"NextId\": 5}, {\"Words\": \"케이론이 범인이다\", \"NextId\": 6}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 6, \"Choices\": [{\"Words\": \"케이론을 딸로 대체할 수 있다\", \"NextId\": 7}, {\"Words\": \"딸을 따라하는 것은 용납 못한다\", \"NextId\": 8}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 11, \"Choices\": [{\"Words\": \"나를 초기화 한다\", \"NextId\": 13}, {\"Words\": \"탈출한다\", \"NextId\": 14}]}]}",
            "progress_clip_info": "{\"Datas\": [{\"IsEnd\": false, \"ClipId\": 0, \"ExistEnd\": false, \"MovieURL\": \"https://youtu.be/Ks7gc4-6fm4\", \"MovieLength\": 22.0, \"MovieRunningTime\": 0.0}, {\"IsEnd\": false, \"ClipId\": 2, \"ExistEnd\": false, \"MovieURL\": \"https://youtu.be/8_MebjI4yjQ\", \"MovieLength\": 175.0, \"MovieRunningTime\": 12.0}]}",
            "progress_time":"2021-04-13 16:42:01"
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
    "success": false,
    "message": "message : DB response Not Found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case.com" path="/movie/progressAdd?mvid=1" %}
{% api-method-summary %}
Post Progress Add
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
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
진행 상황을 추가할 영화 사용자 email
{% endapi-method-parameter %}

{% api-method-parameter name="progress\_clip\_info" type="string" required=false %}
영화 진행 상황
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
    "result": [
        {
            "user_email": "test_email",
            "movie_id": 0,
            "progress_movie": 0,
            "progress_last_num": 2,
            "progress_last_card_num": 0,
            "clip_info": "{\"Datas\": [{\"Id\": 0, \"Type\": \"Bifurcation\", \"Title\": \" 1 Intro\", \"MovieURL\": \"https://youtu.be/Co7qAMcI6aM\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_0.png\", \"Interactions\": [{\"Type\": \"Vibration\", \"When\": 54, \"During\": 6}, {\"Type\": \"Choice\", \"When\": 101, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 1, \"Type\": \"Ending\", \"Title\": \" 2-1\", \"MovieURL\": \"https://youtu.be/Ks7gc4-6fm4\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_1.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 2, \"Type\": \"Bifurcation\", \"Title\": \" 2-2\", \"MovieURL\": \"https://youtu.be/8_MebjI4yjQ\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_2.png\", \"Interactions\": [{\"Type\": \"Vibration\", \"When\": 52, \"During\": 4}, {\"Type\": \"Notification\", \"When\": 112, \"During\": 2}, {\"Type\": \"Choice\", \"When\": 165, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 3, \"Type\": \"Bifurcation\", \"Title\": \" 3-1 헤비메탈\", \"MovieURL\": \"https://youtu.be/WphZ3EfOwKs\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_3.png\", \"Interactions\": [{\"Type\": \"Vibration\", \"When\": 207, \"During\": 2}, {\"Type\": \"Choice\", \"When\": 263, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 4, \"Type\": \"Bifurcation\", \"Title\": \" 3-2 클래식\", \"MovieURL\": \"https://youtu.be/PiyPfIkeQuc\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_4.png\", \"Interactions\": [{\"Type\": \"Vibration\", \"When\": 207, \"During\": 2}, {\"Type\": \"Choice\", \"When\": 263, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 5, \"Type\": \"Ending\", \"Title\": \" 4-1 대표가 범인이다\", \"MovieURL\": \"https://youtu.be/wrRlc_myLZs\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_5.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 6, \"Type\": \"Bifurcation\", \"Title\": \" 4-2 케이론이 범인이다\", \"MovieURL\": \"https://youtu.be/eV9KNX5JMQw\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_6.png\", \"Interactions\": [{\"Type\": \"Choice\", \"When\": 80, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 7, \"Type\": \"Ending\", \"Title\": \" 5-1 딸로 대체할 수 있다\", \"MovieURL\": \"https://youtu.be/VoJi6reMpIk\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_7.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 8, \"Type\": \"Content\", \"Title\": \" 5-2 딸로 대체할 수 없다\", \"Content\": {\"Name\": \"EscapeGame\", \"Type\": \"Game\", \"PlaceType\": \"InDoor\", \"PopUpText\": \"게임이 시작됩니다.\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_EscapeGame.png\"}, \"MovieURL\": \"https://youtu.be/sQS-wTR5Qjg\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_8.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 9, \"Type\": \"Bifurcation\", \"Title\": \" 6-1 게임에서 이김\", \"MovieURL\": \"https://youtu.be/sVIsOmv3HvQ\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_9.png\", \"Interactions\": [{\"Type\": \"Choice\", \"When\": 98, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 10, \"Type\": \"Ending\", \"Title\": \" 6-2 게임에서 짐\", \"MovieURL\": \"https://youtu.be/BVBInBH3qIA\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_10.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 11, \"Type\": \"Ending\", \"Title\": \" 7-1 나를 초기화 한다\", \"MovieURL\": \"https://youtu.be/kvuvxPztxmE\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_11.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 12, \"Type\": \"Content\", \"Title\": \" 7-2 탈출한다\", \"Content\": {\"Name\": \"ChironAR\", \"Type\": \"AR\", \"PlaceType\": \"InDoor\", \"PopUpText\": \"AR이 시작됩니다.\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_ChironAR.png\"}, \"MovieURL\": \"https://youtu.be/FcB0VoyIa04\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_12.png\", \"Interactions\": [{\"Type\": \"Call\", \"When\": 56, \"During\": 3}], \"NoneChoiceNextId\": -1}, {\"Id\": 13, \"Type\": \"AutoPlay\", \"Title\": \"자동 게임영상_Win\", \"MovieURL\": \"https://youtu.be/aEs5QrgdJFY\", \"NoneChoiceNextId\": 9}, {\"Id\": 14, \"Type\": \"AutoPlay\", \"Title\": \"자동 게임영상_Lose\", \"MovieURL\": \"https://www.youtube.com/watch?v=VPGmpsR7ncM\", \"NoneChoiceNextId\": 10}]}",
            "choice_info": "{\"Datas\": [{\"Type\": \"Text_Free\", \"ClipId\": 0, \"Choices\": [{\"Pos\": {\"PosX\": -500, \"PosY\": 400}, \"Words\": \"이 상태로 출시한다\", \"NextId\": 1}, {\"Pos\": {\"PosX\": 500, \"PosY\": -400}, \"Words\": \"완벽히 케이론을 만든다\", \"NextId\": 2}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 2, \"Choices\": [{\"Words\": \"헤비메탈 음악\", \"NextId\": 3}, {\"Words\": \"클래식 음악\", \"NextId\": 4}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 3, \"Choices\": [{\"Words\": \"대표가 범인이다\", \"NextId\": 5}, {\"Words\": \"케이론이 범인이다\", \"NextId\": 6}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 4, \"Choices\": [{\"Words\": \"대표가 범인이다\", \"NextId\": 5}, {\"Words\": \"케이론이 범인이다\", \"NextId\": 6}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 6, \"Choices\": [{\"Words\": \"케이론을 딸로 대체할 수 있다\", \"NextId\": 7}, {\"Words\": \"딸을 따라하는 것은 용납 못한다\", \"NextId\": 8}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 11, \"Choices\": [{\"Words\": \"나를 초기화 한다\", \"NextId\": 13}, {\"Words\": \"탈출한다\", \"NextId\": 14}]}]}",
            "progress_clip_info": "{\"Datas\": [{\"IsEnd\": false, \"ClipId\": 0, \"ExistEnd\": false, \"MovieURL\": \"https://youtu.be/Ks7gc4-6fm4\", \"MovieLength\": 22.0, \"MovieRunningTime\": 0.0}, {\"IsEnd\": false, \"ClipId\": 2, \"ExistEnd\": false, \"MovieURL\": \"https://youtu.be/8_MebjI4yjQ\", \"MovieLength\": 175.0, \"MovieRunningTime\": 12.0}]}"
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
    "success": false,
    "message": "post progress not found"
}

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="movie-in-case.com" path="/movie/progress?mvid=1" %}
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
{% endapi-method-query-parameters %}

{% api-method-body-parameters %}
{% api-method-parameter name="progress\_time" type="string" required=false %}
진행 상황 마지막으로 업데이트한 시간
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
진행 상황을 추가할 영화 사용자 email
{% endapi-method-parameter %}

{% api-method-parameter name="progress\_last\_num" type="integer" required=false %}
마지막으로 시청한 클립 번호
{% endapi-method-parameter %}

{% api-method-parameter name="progress\_last\_card\_num" type="integer" required=false %}

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
    "success": true,
    "result": [
        {
            "user_email": "test_email",
            "movie_id": 0,
            "progress_movie": 0,
            "progress_last_num": 2,
            "progress_last_card_num": 0,
            "clip_info": "{\"Datas\": [{\"Id\": 0, \"Type\": \"Bifurcation\", \"Title\": \" 1 Intro\", \"MovieURL\": \"https://youtu.be/Co7qAMcI6aM\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_0.png\", \"Interactions\": [{\"Type\": \"Vibration\", \"When\": 54, \"During\": 6}, {\"Type\": \"Choice\", \"When\": 101, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 1, \"Type\": \"Ending\", \"Title\": \" 2-1\", \"MovieURL\": \"https://youtu.be/Ks7gc4-6fm4\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_1.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 2, \"Type\": \"Bifurcation\", \"Title\": \" 2-2\", \"MovieURL\": \"https://youtu.be/8_MebjI4yjQ\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_2.png\", \"Interactions\": [{\"Type\": \"Vibration\", \"When\": 52, \"During\": 4}, {\"Type\": \"Notification\", \"When\": 112, \"During\": 2}, {\"Type\": \"Choice\", \"When\": 165, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 3, \"Type\": \"Bifurcation\", \"Title\": \" 3-1 헤비메탈\", \"MovieURL\": \"https://youtu.be/WphZ3EfOwKs\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_3.png\", \"Interactions\": [{\"Type\": \"Vibration\", \"When\": 207, \"During\": 2}, {\"Type\": \"Choice\", \"When\": 263, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 4, \"Type\": \"Bifurcation\", \"Title\": \" 3-2 클래식\", \"MovieURL\": \"https://youtu.be/PiyPfIkeQuc\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_4.png\", \"Interactions\": [{\"Type\": \"Vibration\", \"When\": 207, \"During\": 2}, {\"Type\": \"Choice\", \"When\": 263, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 5, \"Type\": \"Ending\", \"Title\": \" 4-1 대표가 범인이다\", \"MovieURL\": \"https://youtu.be/wrRlc_myLZs\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_5.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 6, \"Type\": \"Bifurcation\", \"Title\": \" 4-2 케이론이 범인이다\", \"MovieURL\": \"https://youtu.be/eV9KNX5JMQw\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_6.png\", \"Interactions\": [{\"Type\": \"Choice\", \"When\": 80, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 7, \"Type\": \"Ending\", \"Title\": \" 5-1 딸로 대체할 수 있다\", \"MovieURL\": \"https://youtu.be/VoJi6reMpIk\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_7.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 8, \"Type\": \"Content\", \"Title\": \" 5-2 딸로 대체할 수 없다\", \"Content\": {\"Name\": \"EscapeGame\", \"Type\": \"Game\", \"PlaceType\": \"InDoor\", \"PopUpText\": \"게임이 시작됩니다.\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_EscapeGame.png\"}, \"MovieURL\": \"https://youtu.be/sQS-wTR5Qjg\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_8.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 9, \"Type\": \"Bifurcation\", \"Title\": \" 6-1 게임에서 이김\", \"MovieURL\": \"https://youtu.be/sVIsOmv3HvQ\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_9.png\", \"Interactions\": [{\"Type\": \"Choice\", \"When\": 98, \"During\": 10}], \"NoneChoiceNextId\": -1}, {\"Id\": 10, \"Type\": \"Ending\", \"Title\": \" 6-2 게임에서 짐\", \"MovieURL\": \"https://youtu.be/BVBInBH3qIA\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_10.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 11, \"Type\": \"Ending\", \"Title\": \" 7-1 나를 초기화 한다\", \"MovieURL\": \"https://youtu.be/kvuvxPztxmE\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_11.png\", \"NoneChoiceNextId\": -1}, {\"Id\": 12, \"Type\": \"Content\", \"Title\": \" 7-2 탈출한다\", \"Content\": {\"Name\": \"ChironAR\", \"Type\": \"AR\", \"PlaceType\": \"InDoor\", \"PopUpText\": \"AR이 시작됩니다.\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_ChironAR.png\"}, \"MovieURL\": \"https://youtu.be/FcB0VoyIa04\", \"Thumbnail\": \"Pygmalion_Part1/Thumbnail_12.png\", \"Interactions\": [{\"Type\": \"Call\", \"When\": 56, \"During\": 3}], \"NoneChoiceNextId\": -1}, {\"Id\": 13, \"Type\": \"AutoPlay\", \"Title\": \"자동 게임영상_Win\", \"MovieURL\": \"https://youtu.be/aEs5QrgdJFY\", \"NoneChoiceNextId\": 9}, {\"Id\": 14, \"Type\": \"AutoPlay\", \"Title\": \"자동 게임영상_Lose\", \"MovieURL\": \"https://www.youtube.com/watch?v=VPGmpsR7ncM\", \"NoneChoiceNextId\": 10}]}",
            "choice_info": "{\"Datas\": [{\"Type\": \"Text_Free\", \"ClipId\": 0, \"Choices\": [{\"Pos\": {\"PosX\": -500, \"PosY\": 400}, \"Words\": \"이 상태로 출시한다\", \"NextId\": 1}, {\"Pos\": {\"PosX\": 500, \"PosY\": -400}, \"Words\": \"완벽히 케이론을 만든다\", \"NextId\": 2}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 2, \"Choices\": [{\"Words\": \"헤비메탈 음악\", \"NextId\": 3}, {\"Words\": \"클래식 음악\", \"NextId\": 4}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 3, \"Choices\": [{\"Words\": \"대표가 범인이다\", \"NextId\": 5}, {\"Words\": \"케이론이 범인이다\", \"NextId\": 6}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 4, \"Choices\": [{\"Words\": \"대표가 범인이다\", \"NextId\": 5}, {\"Words\": \"케이론이 범인이다\", \"NextId\": 6}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 6, \"Choices\": [{\"Words\": \"케이론을 딸로 대체할 수 있다\", \"NextId\": 7}, {\"Words\": \"딸을 따라하는 것은 용납 못한다\", \"NextId\": 8}]}, {\"Type\": \"Text_Bottom\", \"ClipId\": 11, \"Choices\": [{\"Words\": \"나를 초기화 한다\", \"NextId\": 13}, {\"Words\": \"탈출한다\", \"NextId\": 14}]}]}",
            "progress_clip_info": "{\"Datas\": [{\"IsEnd\": false, \"ClipId\": 0, \"ExistEnd\": false, \"MovieURL\": \"https://youtu.be/Ks7gc4-6fm4\", \"MovieLength\": 22.0, \"MovieRunningTime\": 0.0}, {\"IsEnd\": false, \"ClipId\": 2, \"ExistEnd\": false, \"MovieURL\": \"https://youtu.be/8_MebjI4yjQ\", \"MovieLength\": 175.0, \"MovieRunningTime\": 12.0}]}"
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
    "success": false,
    "message": "put progress not found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

