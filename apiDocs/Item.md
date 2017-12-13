## Item

1. 创建物品
    1. [创建物品](#create_item)
2. 查看物品
    1. [查看角色所有物品](#get_all_item)
    2. [查看角色特定物品](#get_special_item)
3. 删除物品
    1. [删除角色所有物品](#delete_item)
    2. [删除角色特定物品](#get_special_item)
4. 更新物品        
    1. [更新角色特定物品](#update_item)


#### 创建物品

<h6 id="create_item">创建物品</h6>

> POST /items

**parameters**

| parameters | 描述 | 是否必须 | 数据类型 | 默认值 |
| ---- | ---- | ---- | ---- | --- |
| id | 角色id | true | string | null |
| name | 物品名 | true | string |  |
| type | 物品分类 | false | string | 'other' |
| des | 物品描述 | false | string | '' |
| meta | 角色附加信息 | true | object | {age: null, sex: 'female'}

#### 查看物品

<h6 id="get_all_item">查看角色所有物品</h6>

> GET /items/:id

**parameters**

| parameters | 描述 | 是否必须 | 默认值 | 结果 |
| ---- | ---- | ---- | ---- | --- |
| id | 角色id | true | null | 获取角色所有物品信息 |

<h6 id="get_item_info">查看角色特定物品</h6>

> GET /items/:owner_id/:

**parameters**

| parameters | 描述 | 是否必须 | 默认值 | 数据类型 |
| ---- | ---- | ---- | ---- | --- |
| id | 角色id | true | null | string |
| type | 物品分类信息,默认query参数是物品id | false | 'particular' | string 

这里有个问题，就是

#### 删除物品

<h6 id="delete_item">删除角色</h6>

> DELETE /items/:id

删除物品，并更新用户角色信息

#### 更新物品

<h6 id="update_item_info">更新角色信息</h6>

> UPDATE /items/:id

| parameters | 描述 | 是否必须 | 数据类型 | 默认值 |
| ---- | ---- | ---- | ---- | --- |
| name | 角色名 | true | string |  |
| meta | 角色附加信息 | true | object | {age: null, sex: 'female'}
| conditions | 角色状态 | false | object | {health: 100,maxHealth: 100, stamina: 100,maxStamina: 100} |
| attributes | 角色属性 | false | object | |
| status | 角色。。 | false | Buffer | |




TODO:
    确认是否使用这种api形式，还是说将物品操作api转到角色api里
    是否需要物品模板
    物品属性是否正确
    获取某类物品问题
    这是不是restful api