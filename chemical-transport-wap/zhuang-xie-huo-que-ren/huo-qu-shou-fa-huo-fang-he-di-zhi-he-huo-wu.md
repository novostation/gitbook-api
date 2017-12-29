#### 获取收发货方和地址和货物

##### 接口地址
```
/app/dyBillShipReceiveUnit/getInfoById/{billUnitId}
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
| billUnitId | Long | 运单收发货方id | TRUE |
| transType | Integer | 1: 发货、装货 2：收货、卸货 |FALSE|

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
| unitName | String | 收发货方名称 |
| chemicalName | String | 货物名称 |
| loadGoodsDate | Date | 装卸货日期 |
| roadDetail | String | 地址信息 |

##### 调用示例
```
url:/app/dyBillShipReceiveUnit/getInfoById/4
```

##### 响应示例
``` json
{
	"unitType": "1",
	"shipAdderssGoodsMes": [{
		"addressMes": {
			"billAddressId": 587,
			"origId": null,
			"bsAddressId": 42,
			"billUnitId": 595,
			"billId": null,
			"provinceId": null,
			"provinceName": "北京",
			"cityId": null,
			"cityName": "西城区",
			"regionId": null,
			"regionName": "",
			"roadDetail": "辅导辅导费到付的",
			"addressType": "1",
			"addressName": "东方饭店放到fd",
			"chemicalUnit": "吨",
			"totalWeight": 10.0,
			"totalVolume": 0.0,
			"loadCkeckUserId": null,
			"loadCheckUserName": null,
			"loacCheckUserTel": null,
			"loadCheckTime": null,
			"loadCheckTotalWeight": null,
			"loadCheckTotalVolume": null,
			"loadCheckRemark": null,
			"ckeckUserId": null,
			"ckeckUserName": null,
			"checkUserTel": null,
			"ckeckCompanyId": null,
			"ckeckCompanyName": null,
			"ckeckTime": null,
			"ckeckTotalWeight": null,
			"ckeckTotalVolume": null,
			"ckeckRemark": null,
			"transType": null
		},
		"addressGoodsMes": [{
			"weight": 10.0,
			"volume": null,
			"baozhaung": {
				"id": 585,
				"origId": null,
				"billId": null,
				"billAddressId": 587,
				"billUnitId": 595,
				"chemicalId": 2933,
				"chemicalName": "亚硝酸丁酯",
				"chemicalType": 3,
				"chemicalItemNo": null,
				"chemicalUnit": "吨",
				"packLevel": 2,
				"unionCode": "2351",
				"weight": 10.0,
				"volume": null,
				"driveMileage": null,
				"checkWeight": null,
				"checkVolume": null,
				"loadCheckWeight": null,
				"loadCheckVolume": null,
				"transType": 1,
				"chemicalTypeName": null,
				"chemicalAlias": null
			},
			"bieming": {
				"id": 27,
				"chemicalId": 2933,
				"chemicalAlias": "亚硝酸丁脂",
				"companyId": 855722
			}
		}]
	}],
	"shipBaseMes": {
		"origId": null,
		"billUnitId": 595,
		"billId": null,
		"billNo": "20171111601209",
		"companyId": null,
		"bsUnitId": 31,
		"unitName": "广州市昌联储运有限公司",
		"unitType": 1,
		"contactPerson": "唐辉",
		"contactTel": "020-38180318",
		"fax": "020-38180319",
		"remark": null,
		"createdUser": "zhangsan"
	},
	"ydh": "20171111601209"
}
```