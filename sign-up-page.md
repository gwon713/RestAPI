---
description: 회원가입 페이지
---

# Sign Up page

{% api-method method="post" host="movie-in-case" path="/user/emailAuth" %}
{% api-method-summary %}
Post Email Auth
{% endapi-method-summary %}

{% api-method-description %}
이메일 중복확인 및 이메일 인증메일 보내기
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
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
    "user_email": "gildong@naver.com", 
    "Certifiedcode" : "574394", 
    "message": "post emailCertified success"    
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "이메일이 존재하지 않습니다."    }
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "중복 이메일."    }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case" path="/user/nameAuth" %}
{% api-method-summary %}
Post Name Auth
{% endapi-method-summary %}

{% api-method-description %}
이름 중복 확인
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="name" type="string" required=false %}
중복 확인을 위한 name
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "user_name" : "gildong",
    "message" : "post nameCertified success" 
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "nameCertified not found"    }
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "이름 중복."    }
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
{% api-method-parameter name="login\_type" type="string" required=false %}
로그인 타입
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
회원가입 email
{% endapi-method-parameter %}

{% api-method-parameter name="name" type="string" required=false %}
회원가입 name
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=false %}
회원가입 password
{% endapi-method-parameter %}

{% api-method-parameter name="service" type="boolean" required=false %}
서비스 이용약관
{% endapi-method-parameter %}

{% api-method-parameter name="personal\_info" type="boolean" required=false %}
개인정보 취급방침
{% endapi-method-parameter %}

{% api-method-parameter name="location\_info" type="boolean" required=false %}
위치정보 이용 약관
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
{    
    "user_email" : "gildong@naver.com", 
    "user_name" : "gildong", 
    "user_pass" : "gildongpwd", 
    "tou_service" : 1, 
    "tou_personal_info" : 1, 
    "tou_location_info" : 1, 
    "tou_marketing_info" : 0,
    "message" : "post signup success"
}    
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "post signUp not found"    }
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

