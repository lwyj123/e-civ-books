## User

1. 发送私信
    1. [发送消息](#send)
2. 获取私信列表
    1. [获取列表](#get-list)
3. 获取私信详情
    1. [获取私信详情](#get-item)

#### 发送私信

<h6 id="send">发送消息</h6>

> POST /letters

**参数**
```JSON
{
	"title": "test123",
	"content": "kekasdsadeke",
	"to_user_id": "5ab89a49e98e131c9180c020"
}
```

**返回**
204或400

#### User信息

<h6 id="get-list">获取私信列表，默认是当前用户全部私信</h6>

> 获取全部用户信息
> GET /letters

**参数**
`size`: 获取条数, 默认`20`。

`page`: 第几页，从1开始，默认为`1`。

`sort`: 默认时间降序`desc`,可选值`desc`与`asc`

**返回**

```JSON
{
    "letters": [
        {
            "updated_at": "2018-03-26T08:35:33.549Z",
            "created_at": "2018-03-26T08:35:33.549Z",
            "title": "wtasd",
            "content": "kekasdsadeke",
            "from_user_id": "5ab8b01594d0772127a5a651",
            "to_user_id": "5ab89a49e98e131c9180c020",
            "id": "5ab8b0d594d0772127a5a652"
        },
        {
            "updated_at": "2018-03-26T08:35:41.535Z",
            "created_at": "2018-03-26T08:35:41.535Z",
            "title": "wtasd52",
            "content": "kekasdsadeke",
            "from_user_id": "5ab8b01594d0772127a5a651",
            "to_user_id": "5ab89a49e98e131c9180c020",
            "id": "5ab8b0dd94d0772127a5a653"
        },
        {
            "updated_at": "2018-03-26T08:35:45.695Z",
            "created_at": "2018-03-26T08:35:45.695Z",
            "title": "wtasd1",
            "content": "kekasdsadeke",
            "from_user_id": "5ab8b01594d0772127a5a651",
            "to_user_id": "5ab89a49e98e131c9180c020",
            "id": "5ab8b0e194d0772127a5a654"
        },
        {
            "updated_at": "2018-03-26T08:35:48.829Z",
            "created_at": "2018-03-26T08:35:48.829Z",
            "title": "test1",
            "content": "kekasdsadeke",
            "from_user_id": "5ab8b01594d0772127a5a651",
            "to_user_id": "5ab89a49e98e131c9180c020",
            "id": "5ab8b0e494d0772127a5a655"
        },
        {
            "updated_at": "2018-03-26T08:35:51.699Z",
            "created_at": "2018-03-26T08:35:51.699Z",
            "title": "test12",
            "content": "kekasdsadeke",
            "from_user_id": "5ab8b01594d0772127a5a651",
            "to_user_id": "5ab89a49e98e131c9180c020",
            "id": "5ab8b0e794d0772127a5a656"
        },
        {
            "updated_at": "2018-03-26T08:35:53.928Z",
            "created_at": "2018-03-26T08:35:53.928Z",
            "title": "test123",
            "content": "kekasdsadeke",
            "from_user_id": "5ab8b01594d0772127a5a651",
            "to_user_id": "5ab89a49e98e131c9180c020",
            "id": "5ab8b0e994d0772127a5a657"
        },
        {
            "updated_at": "2018-03-26T08:39:29.464Z",
            "created_at": "2018-03-26T08:39:29.464Z",
            "title": "test14",
            "content": "kekasdsadeke",
            "from_user_id": "5ab8b01594d0772127a5a651",
            "to_user_id": "5ab89a49e98e131c9180c020",
            "id": "5ab8b1c148be70213bd731cc"
        },
        {
            "updated_at": "2018-03-26T08:39:31.596Z",
            "created_at": "2018-03-26T08:39:31.596Z",
            "title": "test146",
            "content": "kekasdsadeke",
            "from_user_id": "5ab8b01594d0772127a5a651",
            "to_user_id": "5ab89a49e98e131c9180c020",
            "id": "5ab8b1c348be70213bd731cd"
        },
        {
            "updated_at": "2018-03-26T08:39:35.071Z",
            "created_at": "2018-03-26T08:39:35.071Z",
            "title": "test1465",
            "content": "kekasdsadeke",
            "from_user_id": "5ab8b01594d0772127a5a651",
            "to_user_id": "5ab89a49e98e131c9180c020",
            "id": "5ab8b1c748be70213bd731ce"
        },
        {
            "updated_at": "2018-03-26T08:39:37.131Z",
            "created_at": "2018-03-26T08:39:37.131Z",
            "title": "test14365",
            "content": "kekasdsadeke",
            "from_user_id": "5ab8b01594d0772127a5a651",
            "to_user_id": "5ab89a49e98e131c9180c020",
            "id": "5ab8b1c948be70213bd731cf"
        }
    ],
    "page": 1,
    "pages": 4
}
```


<h6 id="info-by-name">获取私信详情</h6>

> GET /letters/:id

```JSON
{
    "updated_at": "2018-03-26T08:35:53.928Z",
    "created_at": "2018-03-26T08:35:53.928Z",
    "title": "test123",
    "content": "kekasdsadeke",
    "from_user_id": "5ab8b01594d0772127a5a651",
    "to_user_id": "5ab89a49e98e131c9180c020",
    "id": "5ab8b0e994d0772127a5a657"
}
```

