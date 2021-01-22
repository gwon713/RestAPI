---
description: 비밀번호 찾기
---

# Find password page

{% api-method method="post" host="movie-in-case" path="/user/findPwd" %}
{% api-method-summary %}
Post Password find
{% endapi-method-summary %}

{% api-method-description %}
이메일이 존재하면 이메일로 확인 코드 보냄
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="authCode" type="string" required=false %}
인증코드
{% endapi-method-parameter %}

{% api-method-parameter name="email" type="string" required=false %}
비밀번호를 찾을 사용자 email
{% endapi-method-parameter %}
{% endapi-method-body-parameters %}
{% endapi-method-request %}

{% api-method-response %}
{% api-method-response-example httpCode=200 %}
{% api-method-response-example-description %}
성공적인 email 입력
{% endapi-method-response-example-description %}

```
{    
    "user_email": "gildong@naver.com",    
    "message": "password find success"    
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
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="movie-in-case" path="/user/editPwd" %}
{% api-method-summary %}
Put Edit password
{% endapi-method-summary %}

{% api-method-description %}
확인코드 인증 후 새비밀번호 입력
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
비밀번호를 변경할 사용자의 email
{% endapi-method-parameter %}

{% api-method-parameter name="password" type="string" required=false %}
변경할 새 비밀번호
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
    "new_password" : "gildong1234",
    "message": "edit password success"    
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "message": "edit password not found"    
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



