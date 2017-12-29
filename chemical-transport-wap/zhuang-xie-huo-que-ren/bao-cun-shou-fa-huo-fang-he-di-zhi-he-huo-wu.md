#### 保存收发货方和地址和货物 {#-1}

##### 接口地址
```
/app/dyBillShipReceiveUnit/saveAll
```
##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| data| JSON| 收发货方和地址和货物JSON数据 | TRUE|
| unitType| Integer | 1: 发货、装货 2：收货、卸货 | TRUE|

data:
```
{
	"ydh": "123456",
	"shipBaseMes": {
		"unitId": 21,
		"unitName": "对个话gg",
		"unitType": 1,
		"cityType": null,
		"transportCompanyId": 1,
		"chemicalCompanyId": 1,
		"contactPerson": "对个话",
		"contactTel": "13710120665",
		"fax": "07533606222",
		"remark": "1"
	},
	"shipAdderssGoodsMes": [{
		"addressMes": {
			"addressId": 39,
			"transportCompanyId": 1,
			"provinceId": 1,
			"cityId": 1,
			"regionId": 1,
			"provinceName": "广东",
			"cityName": "广州",
			"regionName": "萝岗区",
			"roadDetail": "萝岗科汇金谷",
			"addressType": 1,
			"addressName": "潘"
		},
		"addressGoodsMes": [{
			"bieming": {
				"id": 28,
				"chemicalId": 2933,
				"companyId": 855722,
				"chemicalAlias": "2351"
			},
			"baozhaung": {
				"id": 28,
				"companyId": 855722,
				"packMethod": "2351",
				"packLevel": 2,
				"chemicalId": 2933
			},
			"weight": "1",
			"volume": "5"
		},
		{
			"bieming": {
				"id": 29,
				"chemicalId": 2928,
				"companyId": 855722,
				"chemicalAlias": "2345"
			},
			"baozhaung": {
				"id": 29,
				"companyId": 855722,
				"packMethod": "2345",
				"packLevel": 2,
				"chemicalId": 2928
			},
			"weight": "5",
			"volume": "6"
		}]
	},
	{
		"addressMes": {
			"addressId": 32,
			"transportCompanyId": 1,
			"provinceId": 1,
			"cityId": 1,
			"regionId": 1,
			"provinceName": "北京",
			"cityName": "东城区",
			"regionName": "",
			"roadDetail": "pp",
			"addressType": 1,
			"addressName": "pp"
		},
		"addressGoodsMes": [{
			"bieming": {
				"id": 16,
				"chemicalId": 2930,
				"companyId": 855722,
				"chemicalAlias": "gg"
			},
			"baozhaung": {
				"id": 16,
				"companyId": 855722,
				"packMethod": "gg",
				"packLevel": 2,
				"chemicalId": 2930
			},
			"weight": "6",
			"volume": "6"
		}]
	}]
}
```
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


##### 调用示例
```
/app/dyBillShipReceiveUnit/saveAll
```
参数:
```
{
"data":...,
"unitType":1
}
```

##### 响应示例
```

```
