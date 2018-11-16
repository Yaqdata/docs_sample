## Script

[字段详解](objects.md)

- [脚本列表](#脚本列表)
- [创建脚本](#创建脚本)

### 脚本列表

```
GET /scripts/
```

| Name | Type | Description | Required |
| --- | --- | --- | --- |
| page | int | 当前页 | - |
| per_page | int | 每页个数 | - |


#### Response

| STATUS 200 OK |
| :-----------: |

```
[
    {
        "id": 1,
        "created_at": "2018-11-16T05:42:50.317669Z",
        "updated_at": "2018-11-16T05:42:50.318083Z",
        "name": "脚本-1542346964506",
        "author": "1",
        "script_sub_type": 1,
        "script_type": 1,
        "application": "1397",
        "comment": ""
    }
]
```

### 创建脚本

```
POST /scripts/
```

| Name | Type | Description | Required |
| --- | --- | --- | --- |
| name | string | 名称 | Y |
| script_type | string | 脚本类型(1: python, 2: shell) | Y |
| script_sub_type | string | 脚本所属类型(1: 私有, 2: 公有) | Y |
| content | string | 脚本内容 | Y |
| application | string | 所属应用 | Y |


#### Response

| STATUS 201 CREATED |
| :----------------: |

```
{
    "id": 1,
    "created_at": "2018-11-16T05:42:50.317669Z",
    "updated_at": "2018-11-16T05:42:50.318083Z",
    "name": "脚本-1542346964506",
    "author": "1",
    "script_sub_type": 1,
    "script_type": 1,
    "application": "1397",
    "comment": ""
}
```