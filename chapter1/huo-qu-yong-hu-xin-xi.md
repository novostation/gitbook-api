#### 获取用户信息

##### 接口地址

```
/app/system/getUserInfo
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

 1. 无参数
 2. 需要登录

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：存在空车单；0：没有空车单 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| companyName| String | 企业名称 |
| companyType| String |企业类型（1.运输企业，2、生产企业，3：存储企业，4.销售企业，5 .消费企业）|
| employeeId| String | 员工id |
| employeeName| String | 企业名称 |
| employeeType| String | 从业人员类型1：驾驶员；2：押运员；3：驾驶员和押运员 |
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
        "employeeType": 1,
        "employeeId": 6909,
        "address": [
            "广州市南沙区万顷沙镇钢铁基地"
        ],
        "companyType": 1,
        "contactTel": "86474841",
        "companyName": "广钢林德气体（广州）有限公司",
        "employeeName": "www"
    },
    "message": "成功"
}
```