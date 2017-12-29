#### 更新二维码

##### 接口地址

```
/app/dyBillQrcode/update
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| id | Long |  | TRUE |
| billId | Long | 运单id | FALSE |
| billNo | String | 运单号 | FALSE |
| billUnitId | Long | 运单收发货方id | FALSE |
| billAddressId | Long | 运单收发货方装卸货地址id | FALSE |
| transType | Integer | 1: 发货、装货 2：收货、卸货 | FALSE |
| driverId | Long | 驾驶员id\(从业人员id\) | FALSE |
| contactPerson | String | 联系人 | FALSE |
| contactTel | String | 联系电话 | FALSE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| id | Long |  |
| billId | Long | 运单id |
| billNo | String | 运单号 |
| billUnitId | Long | 运单收发货方id |
| billAddressId | Long | 运单收发货方装卸货地址id |
| transType | Integer | 1: 发货、装货 2：收货、卸货 |
| driverId | Long | 驾驶员id\(从业人员id\) |
| contactPerson | String | 联系人 |
| contactTel | String | 联系电话 |

##### 调用示例

```
url:/app/dyBillQrcode/update
```

参数:

##### 响应示例

```
{
    "message": "成功",
    "status": 1,
    "data": {
        "id": 1,
        "message": "成功",
        "transType": 1,
        "status": 1,
        "billNo": "1",
        "billUnitId": 1,
        "driverId": 1,
        "billId": 1,
        "contactTel": "1",
        "contactPerson": "1",
        "billAddressId": 1
    }
}
```

