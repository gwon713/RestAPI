---
description: 로그인 화면
---

# Login page

{% api-method method="post" host="movie-in-case" path="/user/logIn" %}
{% api-method-summary %}
Post Login
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
    "user_email" : "gildong@naver.com" , 
    "user_password" : "gildong" ,
    "user_deleted" : 0,
    "message" : "post login success"    
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}
로그인 실패
{% endapi-method-response-example-description %}

```
{    "message": "이메일 또는 비밀번호가 올바르지 않습니다."    }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



