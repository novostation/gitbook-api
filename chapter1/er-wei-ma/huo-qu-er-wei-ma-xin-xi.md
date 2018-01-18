#### 获取二维码信息

##### 接口地址

```
/app/dyBill/getCompanyBillQrCodeInfo
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| qrCodeId| Integer | 二维码ID| TRUE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| createdTime| String | 运单日期|
| unitName| String | 收发货方 |
| billNo| String| 运单号 |
| qrCode|String| 二维码BASE64字符 |
| billStatus| String| 运单状态 |
| roadDetail| String| 装货地址 |
| chemical| JSON数组| 地址对应的货物 |
| chemicalName| String | 物品名称(别名) |
| weight| Float| 重量 |
| volume| Float| 体积 |
| chemicalUnit| String | 货物单位|

##### 调用示例

```
url:/app/dyBill/getCompanyBillQrCodeInfo

参数:{qrCodeId:283}
```

##### 响应示例