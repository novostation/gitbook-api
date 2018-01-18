#### 获取运单二维码信息

##### 接口地址

```
/app/dyBill/getBillQrCodeInfo
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billId| LONG| 二维码ID| TRUE |
| transType| Integer | 1: 发货、装货2：收货、卸货 | FALSE|

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON数组| 响应数据 |
| unitName| String | 收发货方 |
| loadGoodsDate| String| 运单号 |
| qrCode|String| 二维码BASE64字符 |
| roadDetail| String| 地址 |


##### 调用示例

```
url:/app/dyBill/getBillQrCodeInfo

参数:{qrCodeId:283}
```

##### 响应示例
```
{
    "status": 1,
    "data": [
        {
            "unitName": "广钢林德气体（广州）有限公司",
            "loadGoodsDate": "2018-01-18 14:08:32",
            "qrCode":"二维码BASE64"
            "roadDetail": "广州市白云区石井镇龙湖龙窖路1252号"
        }
    ],
    "message": "获取数据成功"
}
```

