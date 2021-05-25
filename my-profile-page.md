---
description: 내정보 페이지
---

# My profile page

{% api-method method="get" host="movie-in-case.com" path="/user/profile" %}
{% api-method-summary %}
Get My profile
{% endapi-method-summary %}

{% api-method-description %}
내 정보 가져오기 \(세션으로 처리함\)
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

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
            "user_name": "RN_test",
            “user_terms” : "{“user_service” : 1 , “user_personal_info”: 1, “user_location_info” : 0, “user_marketing_info” : 1}"
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
    "message": "get my profile no found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case.com" path="/user/nameAuth" %}
{% api-method-summary %}
Post Profiile NameAuth
{% endapi-method-summary %}

{% api-method-description %}
내 프로필에서 이름 수정할  때 이름 중복 확인
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=false %}
중복 확인을 할 이름
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
    "user_name" : "RN_test"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "success": false,
    "user_name" : "중복 이름"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="movie-in-case.com" path="/user/editName" %}
{% api-method-summary %}
Put Edit name
{% endapi-method-summary %}

{% api-method-description %}
이름변경
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=false %}
변경할 이름
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "success : true,
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
    "message" : "put edit name not found"
}   
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="movie-in-case.com" path="/user/profile/editPwd" %}
{% api-method-summary %}
Put Edit password \(로그인 되어있는 상태\)
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="old\_password" type="string" required=false %}
현재 비밀번호
{% endapi-method-parameter %}

{% api-method-parameter name="new\_password" type="string" required=false %}
변경할 비밀번호
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "success : true,
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

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    success : false,
    message : '현재 비밀번호가 일치하지 않습니다.'
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "success" : false,
    "message" : "put edit password not found"
}   
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="moive-in-case.com" path="/user/editTerms" %}
{% api-method-summary %}
Put Edit Terms
{% endapi-method-summary %}

{% api-method-description %}
선택 이용약관 수정
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="location\_info" type="boolean" required=false %}
위치정보 이용약관
{% endapi-method-parameter %}

{% api-method-parameter name="marketing\_info" type="boolean" required=false %}
마케팅 정보 수신 약관
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```

```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="movie-in-case.com" path="/user/deleteAccount" %}
{% api-method-summary %}
 Put Delete account
{% endapi-method-summary %}

{% api-method-description %}
회원 탈퇴 \(세션으로 처리\)
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "success" : true
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
    "success" : false
    "message": "put delete user not found"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



