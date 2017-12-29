#### 司机装卸货确认

##### 接口地址

```
/app/dyBillChemical/driverConfirm
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| data | JSONARRAY | 页码 | TRUE |
| transType | Integer | 1: 发货、装货 2：收货、卸货 | TRUE |
| billUnitId | Long | 运单收发货方id | TRUE |
| billAddressId | Long | 运单收发货方装卸货地址id | TRUE |
| contactPerson | String | 联系人 | TRUE |
| billUnitName | String | 收发货方名称 | TRUE |
| contactTel | String | 联系电话 | TRUE |
| chemicalName | String | 危化品名称 | TRUE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |

##### 调用示例

```
url:/app/dyBillChemical/driverConfirm
```

参数：

```
{
	"data": "[
		{id: "92", loadCheckWeight: "10086", loadCheckVolume: "5",billId:"1",chemicalName:"15"},
		{id: "93", loadCheckWeight: "6", loadCheckVolume: "6",chemicalName:"186456"}
		]",
	"transType": "1",
	"billUnitId": "1",
	"billAddressId": "49022",
	"contactPerson": "12",
	"contactTel": "159",
	"billUnitName": "145562"
}
```

##### 响应示例

```json
{
    "status": 1,
    "data": {
        "dyBillAddress": {
            "billAddressId": 49022,
            "origId": "0Z8ML9M1R52J0Z8ML9M1R52Q",
            "bsAddressId": null,
            "billUnitId": 30529,
            "billId": 17294,
            "provinceId": null,
            "provinceName": null,
            "cityId": null,
            "cityName": null,
            "regionId": null,
            "regionName": null,
            "roadDetail": "",
            "addressType": "2",
            "addressName": "广东省 阳江市 江城区 广东省阳江市江城区金山路与石湾路交汇处",
            "chemicalUnit": null,
            "totalWeight": 0,
            "totalVolume": 0,
            "loadCkeckUserId": 523,
            "loadCheckUserName": null,
            "loacCheckUserTel": null,
            "loadCheckTime": "2017-11-17 13:15:53",
            "loadCheckTotalWeight": 10092,
            "loadCheckTotalVolume": 11,
            "loadCheckRemark": "",
            "ckeckUserId": null,
            "ckeckUserName": null,
            "checkUserTel": null,
            "ckeckCompanyId": null,
            "ckeckCompanyName": null,
            "ckeckTime": null,
            "ckeckTotalWeight": null,
            "ckeckTotalVolume": null,
            "ckeckRemark": null,
            "transType": 2,
            "longitude": null,
            "latitude": null
        },
        "chemicalName": "145615",
        "qrcodeId": 56,
        "billNo": "20161224002065",
        "loadCheckTime": "2017-11-17 13:15:53",
        "billStatus": "运输中",
        "billUnitName": "145562"
    },
    "message": "更新数据成功"
}
```



