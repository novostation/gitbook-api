#### 获取用户信息

##### 接口地址

```
/app/system/getUserInfo
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
| companyName| String | 企业名称 |
| address| String数组 | 地址 |

##### 调用示例

```
url:/app/system/getUserInfo
```

##### 响应示例
```
{
    "status": 0,
    "data": {
        "address": [
            "广州市南沙区万顷沙镇钢铁基地",
            "广州市南沙区万顷沙镇钢铁基地"
        ],
        "companyName": "广钢林德气体（广州）有限公司"
    },
    "message": "成功"
}
```