#### 删除收发货方

##### 接口地址

```
/app/dyBillShipReceiveUnit/delete/{billUnitId}
```

##### 请求方式

POST

##### 接口描述

删除收发货方及地址及货物

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billUnitId| String | 查询运单ID为null的收发货方 | True |
| transType | String | 收发货方类型 1：发货方 2 ：收货方 | FALSE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |

##### 调用示例

```
url: /app/dyBillShipReceiveUnit/delete/27886
```

##### 响应示例

```
{
    "status": 1
    "data": null,
    "message": "删除数据成功"
}
```