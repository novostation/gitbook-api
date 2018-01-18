#### 删除收发货方

##### 接口地址

```
/app/bsShipReceiveUnit/delete/{unitId}
```

##### 请求方式

POST

##### 接口描述

删除收发货方及地址及货物

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| unitId| String | 收发货方ID | True |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |

##### 调用示例

```
url: /app/bsShipReceiveUnit/delete/139
```

##### 响应示例

```
{
    "status": 1
    "data": null,
    "message": "删除数据成功"
}
```