---
description: 로그인 화면
---

# Login page

{% api-method method="post" host="movie-in-case.com" path="/user/logIn/local" %}
{% api-method-summary %}
Post Local Login
{% endapi-method-summary %}

{% api-method-description %}
로그인 요청
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
사용자 email
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=false %}
사용자 password
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
로그인 성공
{% endapi-method-response-example-description %}

```
{
    "user": {
        "user_email": "test_email",
        "user_password": "$2b$05$m5dp.T7.Adn/vs.mYoPxVe6Xj6AOGsNgOeDl/9eMLSrcHyE7iNmJK"
    },
    "success": true,
    "message": "로그인 성공."
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
로그인 실패
{% endapi-method-response-example-description %}

```
{
    "success": false,
    "message": "비밀번호가 일치하지 않습니다." or "해당 유저가 존재하지 않습니다."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case.com" path="/user/logOut" %}
{% api-method-summary %}
Post Logout
{% endapi-method-summary %}

{% api-method-description %}
로그아웃 \(세션 삭제\)
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
 성공적인 로그아웃
{% endapi-method-response-example-description %}

```
{
    "success": true,
    "user": {
        "user_email": "test_email",
        "user_password": "$2b$05$m5dp.T7.Adn/vs.mYoPxVe6Xj6AOGsNgOeDl/9eMLSrcHyE7iNmJK"
    },
    "message": "logout success"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}
 로그인 필
{% endapi-method-response-example-description %}

```
{
    "success": false,
    "message": "로그인 필요"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
로그아웃 실패
{% endapi-method-response-example-description %}

```
{
    "success": false,
    "user": {
        "user_email": "test_email",
        "user_password": "$2b$05$m5dp.T7.Adn/vs.mYoPxVe6Xj6AOGsNgOeDl/9eMLSrcHyE7iNmJK"
    },
    "message": "logout fail"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case.com" path="/user/sessionCheck" %}
{% api-method-summary %}
Post sessionCheck
{% endapi-method-summary %}

{% api-method-description %}
 세션 확
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
현재 앱기준 로그인 처리되어있는  
사용자 email\(cookie\)
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
    message : "로그인 상태"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    success : false,
    message : "로그인 필요"
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    success : false,
    message : "현재 로그인 정보와 다름"
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case.com" path="/user/logIn/kakao" %}
{% api-method-summary %}
Post Login Kako
{% endapi-method-summary %}

{% api-method-description %}

{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
사용자 email
{% endapi-method-parameter %}

{% api-method-parameter name="accessToken" type="string" required=false %}
kakao access 토큰
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    "user": {
        "user_email": "test_email",
        "user_login_type": "kakao"
    },
    "success": true,
    "message": "로그인 성공."
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

