#### 删除二维码

##### 接口地址

```
/app/dyBillQrcode/delete/{id}
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| id | Long |  | TRUE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |

##### 调用示例

```
url:/app/dyBillQrcode/delete/1
```

参数:

##### 响应示例

```
{"message":"成功","status":1}
```

