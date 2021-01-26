---
description: 내정보 페이지
---

# My profile page

{% api-method method="get" host="movie-in-case" path="/user/profile?email=gildong@naver.com" %}
{% api-method-summary %}
Get My profile
{% endapi-method-summary %}

{% api-method-description %}
내 정보 가져오기
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
정보를 가져올 사용자 email
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "user_email" : "gildong@naver.com", 
    "user_name" : "gildong", 
    "user_password" : "gildongpwd", 
    "message" : "get my profile success"
}    
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "get my profile no found"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="movie-in-case" path="/user/editName?email=gildong@naver.com" %}
{% api-method-summary %}
Put Edit name
{% endapi-method-summary %}

{% api-method-description %}
이름변경
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
이름 변경을 할 사용자 email
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}

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
    "user_email" : "gildong@naver.com", 
    "user_name" : "gildong edit", 
    "message" : "put edit name success"
}   
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "message" : "put edit name not found"
}   
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="movie-in-case" path="/user/deleteAccount?email=gildong@naver.com" %}
{% api-method-summary %}
 Put Delete account
{% endapi-method-summary %}

{% api-method-description %}
회원 탈퇴
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-query-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
회원 탈퇴를 할 사용자 email
{% endapi-method-parameter %}
{% endapi-method-query-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "user_email" : "gildong@naver.com", 
    "user_name" : "gildong", 
    "user_password" : "gildongpwd", 
    "user_deleted" : 1
    "message" : "put delete user success"
}   
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    "message": "put delete user not found"}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



