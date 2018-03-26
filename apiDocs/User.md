## User

1. 注册用户
    1. [注册](#signup)
2. 登录
    1. [登录](#login)
3. 人物
    1. [获取人物信息](#info)

#### 注册用户

<h6 id="signup">注册</h6>

> POST /users
```JSON
{
  "name": "admin",
  "username": "admin",
  "password": "admin",
  "meta": {
	"age": 22,
	"sex": "male"
  }
}
```

#### 登录

<h6 id="login">登录</h6>

> POST /users/login

**参数**
```JSON
{
	"username": "admin",
	"password": "admin"
}
```

**返回**
```JSON
{
    "name": "admin",
    "username": "admin",
    "person_id": null,
    "meta": {
        "age": 22,
        "sex": "male"
    },
    "id": "5ab89a49e98e131c9180c020",
    "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9.eyJuYW1lIjoiYWRtaW4iLCJ1c2VybmFtZSI6ImFkbWluIiwicGVyc29uX2lkIjpudWxsLCJtZXRhIjp7ImFnZSI6MjIsInNleCI6Im1hbGUifSwiaWQiOiI1YWI4OWE0OWU5OGUxMzFjOTE4MGMwMjAiLCJpYXQiOjE1MjIwNDg1NTksImV4cCI6MTUyMjEzNDk1OX0.JR3A4uWMEbYoKeCQzT3VBxu1RcIWrpiDSNamWcRDrac"
}
```

#### User信息

<h6 id="info-all">根据获取人物信息列表</h6>

> 获取全部用户信息
> GET /users

```JSON
[
    {
        "name": "admin",
        "username": "admin",
        "person_id": "5ab87749730e62122dcc9f92",
        "meta": {
            "age": 22,
            "sex": "male"
        }
    }
]
```

<h6 id="info-by-name">根据名字获取单个人物信息</h6>

> 根据id获取用户信息
> GET /users/:id

```JSON
{
    "name": "admin",
    "person_id": "5ab87749730e62122dcc9f92",
    "meta": {
        "age": 22,
        "sex": "male"
    },
    "id": "5ab8750b62a6e611b75d6c83"
}
```

