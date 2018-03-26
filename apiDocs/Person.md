## Person

1. 创建角色
    1. [创建角色](#create)
2. 查看角色
    1. [查看角色](#info-by-id)
3. 删除角色
    1. [删除角色](#delete)
4. 更新角色        
    1. [更新角色信息](#update)


#### 创建角色

<h6 id="create">创建角色</h6>

> POST /persons

**参数**
```JSON
{
	"name": "管理员3",
	"meta": {
		"sex": "male"
	}
}
```

**返回**
```JSON
{
    "updated_at": "2018-03-26T04:30:03.104Z",
    "created_at": "2018-03-26T04:30:03.104Z",
    "name": "管理员3",
    "user_id": "5ab8750b62a6e611b75d6c83",
    "attributes": {
        "str": 1,
        "dex": 1,
        "con": 1,
        "int": 1,
        "wis": 1,
        "cha": 1
    },
    "status": [],
    "conditions": {
        "health": 100,
        "maxHealth": 100,
        "stamina": 120,
        "maxStamina": 120
    },
    "items": []
}
```

#### 查看角色

<h6 id="info-by-id">根据id查看角色</h6>

> GET /persons/:id

**参数**


**返回**
```JSON
{
    "updated_at": "2018-03-26T04:30:03.104Z",
    "created_at": "2018-03-26T04:30:03.104Z",
    "name": "管理员3",
    "user_id": "5ab8750b62a6e611b75d6c83",
    "attributes": {
        "str": 1,
        "dex": 1,
        "con": 1,
        "int": 1,
        "wis": 1,
        "cha": 1
    },
    "status": [],
    "conditions": {
        "health": 100,
        "maxHealth": 100,
        "stamina": 120,
        "maxStamina": 120
    },
    "items": [],
    "id": "5ab87749730e62122dcc9f92"
}
```

#### 删除角色

<h6 id="delete">删除角色</h6>

> DELETE /persons/:id

删除角色，并更新用户角色

**参数**
无

**返回**
204

#### 更新角色

<h6 id="update">更新角色信息</h6>

> PUT /persons/:id

**参数**


**返回**

