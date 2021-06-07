---
description: 회원가입 페이지
---

# Sign Up page

{% api-method method="post" host="movie-in-case.com" path="/user/emailAuth" %}
{% api-method-summary %}
Post Email Auth
{% endapi-method-summary %}

{% api-method-description %}
이메일 중복확인 및 이메일 인증메일 보내기
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="auth\_code" type="string" required=false %}
메일로 전송할 인증코드
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
인증을 할 email
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "success" : true,
    "user_email": "test_email"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "success" : false,
    "message": "중복 이메일."    
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case.com" path="/user/email/overLapCheck" %}
{% api-method-summary %}
Post Email overlap check
{% endapi-method-summary %}

{% api-method-description %}
이메일 중복 확인\(DB\)
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
중복체크를 할 사용자 email
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    success : true,
    user_email : userEmail,
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    success : false,
    message : '중복 이메일'
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case" path="/user/signUp" %}
{% api-method-summary %}
Post Sign up
{% endapi-method-summary %}

{% api-method-description %}
회원가입 정보 서버 입력
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="user\_terms" type="string" required=false %}
이용 약관
{% endapi-method-parameter %}

{% api-method-parameter name="login\_type" type="string" required=false %}
로그인 타입
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
회원가입 email
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
회원가입 me
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=false %}
회원가입 password \(kakao: kakaoID\)
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "success" : true,
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
    "message": "post signUp not found"    
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



