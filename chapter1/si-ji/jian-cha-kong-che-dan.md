#### 检查空车单

##### 接口地址

```
/app/dyBillEmpty/checkDyBillEmpty
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

 无：需要登录

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：存在空车单；0：没有空车单 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |

##### 调用示例

```
url:/app/dyBillEmpty/checkDyBillEmpty
```

##### 响应示例
```
{
    "status": 0,
    "data": "",
    "message": "车辆找到0条空车单"
}
```