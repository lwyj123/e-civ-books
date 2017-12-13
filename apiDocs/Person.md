## Person

1. 创建角色
    1. [创建角色](#create_person)
2. 查看角色
    1. [查看角色](#get_all_person)
    2. [查看角色特定信息](#get_person_info)
3. 删除角色
    1. [删除角色](#delete_person)
4. 更新角色        
    1. [更新角色信息](#update_person_info)


#### 创建角色

<h6 id="create_preson">创建角色</h6>

> POST /persons

**parameters**

| parameters | 描述 | 是否必须 | 数据类型 | 默认值 |
| ---- | ---- | ---- | ---- | --- |
| user_id | 用户id | true | string | null |
| name | 角色名 | true | string |  |
| meta | 角色附加信息 | true | object | {age: null, sex: 'female'}

#### 查看角色

<h6 id="get_all_person">查看角色</h6>

> GET /persons/:id

**parameters**

| parameters | 描述 | 是否必须 | 默认值 | 结果 |
| ---- | ---- | ---- | ---- | --- |
| id | 用户id | true | null | 用户添加角色 |

<h6 id="get_person_info">查看角色特定信息</h6>

待议

#### 删除角色

<h6 id="delete_person">删除角色</h6>

> DELETE /persons/:id

删除角色，并更新用户角色

#### 更新角色

<h6 id="update_person_info">更新角色信息</h6>

> UPDATE /persons/:id

| parameters | 描述 | 是否必须 | 数据类型 | 默认值 |
| ---- | ---- | ---- | ---- | --- |
| name | 角色名 | true | string |  |
| meta | 角色附加信息 | true | object | {age: null, sex: 'female'}
| conditions | 角色状态 | false | object | {health: 100,maxHealth: 100, stamina: 100,maxStamina: 100} |
| attributes | 角色属性 | false | object | |
| status | 角色。。 | false | Buffer | |
