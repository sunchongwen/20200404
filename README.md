# 20200404 
# **1.登录**
#### Post /User/Login

###### request
```javascript
Content-Type: application/json

{
	"username":"admin",
	"password":"admin",
}
```
###### response

fail
```javascript
{
    "status": 1,
    "msg": "密码错误"
}
```
success
```javascript
{
    "status": 0,
    "data": {
        "id": 12,
        "username": "aaa",
        "email": "aaa@163.com",
        "phone": null,
        "role": 0,
        "createTime": 1479048325000,
        "updateTime": 1479048325000
    }
}
```
# **2.注册**
##### POST /user/register

###### request
```javascript
{
	"username":"admin",
	"password":"admin",
	"email":"admin@qq.com"
}
```
##### response

success
```javascript
{
    "status": 0,
    "msg": "校验成功"
}
```
fail
```javascript
{
    "status": 2,
    "msg": "用户已存在"
}
```
# **3.获取登录用户信息**
#### GET /user
POST /user/logout

##### request
```javascript
无参数
```

#####response

success
```javascript
{
    "status": 0,
    "data": {
        "id": 12,
        "username": "aaa",
        "email": "aaa@163.com",
        "phone": null,
        "role": 0,
        "createTime": 1479048325000,
        "updateTime": 1479048325000
    }
}
```
fail
```javascript
{
    "status": 10,
    "msg": "用户未登录,无法获取当前用户信息"
}
```
# **4.退出登录**
#### GET /user
POST /user/logout

##### request

```javascript
无
```
##### response

success
```javascript
{
    "status": 0,
    "msg": "退出成功"
}
```
fail
```javascript
{
    "status": -1,
    "msg": "服务端异常"
}
```
