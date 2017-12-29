#### 查询二维码 {#-0}

##### 接口地址

```
/app/dyBillQrcode/listPage/{pageNum}/{pageSize}
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| pageNum | Integer | 页码 | TRUE |
| pageSize | Integer | 每页记录数 | TRUE |
| id | Long | 主键 | FALSE |
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
| qrcodeType | Integer | 二维码类型：1发货方；2收货方 |
| unitName | String | 收发货方名称 |
| chemicalName | String | 货物名称 |
| loadGoodsDate | Date | 装卸货日期 |
| roadDetail | String | 地址信息 |
| qrcode | String | 二维码BASE64字符串 |

##### 调用示例

```
url:/app/dyBillQrcode/listPage/1/1
```

##### 响应示例

