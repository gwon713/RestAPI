---
description: 비밀번호 찾기
---

# Find password page

{% api-method method="post" host="movie-in-case.com" path="/user/findPwd" %}
{% api-method-summary %}
Post Password find
{% endapi-method-summary %}

{% api-method-description %}
이메일이 존재하면 이메일로 확인 코드 보냄
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
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
    "success" : true,   
    "user_email": "test_email"    
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "success : false
    "message": "해당 유저가 존재하지 않습니다."    
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="post" host="movie-in-case.com" path="/user/authCodeCheck" %}
{% api-method-summary %}
Post Check Auth Code
{% endapi-method-summary %}

{% api-method-description %}
이메일 인증코드 확인
{% endapi-method-description %}

{% api-method-spec %}
{% api-method-request %}
{% api-method-body-parameters %}
{% api-method-parameter name="email" type="string" required=false %}
인증코드를 확인 받을 사용자 email
{% endapi-method-parameter %}

{% api-method-parameter name="authCode" type="string" required=false %}
사용자가 입력한 인증코드
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
    message : '확인되었습니다.'
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    success : false,
    message : '인증 코드가 올바르지 않습니다.'
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    success : false,
    message : '인증 코드가 올바르지 않습니다.'
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}

{% api-method method="put" host="movie-in-case.com" path="/user/findPwd/editPwd" %}
{% api-method-summary %}
Put Edit password \(로그인 안되어있는 상태\)
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

{% api-method-parameter name="authCode" type="string" required=false %}
사용자가 입력한 인증번호
{% endapi-method-parameter %}

{% api-method-parameter name="new\_password" type="string" required=false %}
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

{% api-method-response-example httpCode=403 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    success : false,
    message : '인증 코드가 올바르지 않습니다.'
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=404 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{    
    "success" : false
    "message" : "edit password not found"    
}
```
{% endapi-method-response-example %}

{% api-method-response-example httpCode=409 %}
{% api-method-response-example-description %}

{% endapi-method-response-example-description %}

```
{
    success : false,
    message : '기존 비밀번호는 사용하실 수 없습니다.'
}
```
{% endapi-method-response-example %}
{% endapi-method-response %}
{% endapi-method-spec %}
{% endapi-method %}



