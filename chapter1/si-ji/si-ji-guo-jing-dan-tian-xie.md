#### 司机广州送货创建卸货单

##### 接口地址

```
/app/dyBill/saveDriverTransitBill
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| sendAddress| String| 出发地址| TRUE |
| receiveAddress| String| 目的地| TRUE |
| car| JSON字符串| 调度信息 |TRUE |
| vehicleId| Integer | 车辆ID| TRUE |
|tailerVehicleId| Integer | 挂车ID |False|
| driverId| Integer |司机ID|TRUE |
| escortId|Integer | 押运员ID |TRUE |
| chemical| String| JSON数组 |TRUE |
| chemicalId| String| 危化品ID |TRUE |
| chemicalAliasUsing| String| 常用危化品别名 |TRUE |
| weight| String| 重量 |TRUE |
| volume| String| 体积 |TRUE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| billId| Integer | 运单ID|

##### 调用示例

``` json
url:/app/dyBill/saveDriverTransitBill
```
参数:
```
{
	"data": {
		"sendAddress": "44",
		"receiveAddress": "44",
		"car": {
			"vehicleId": "2748126",
			"tailerVehicleId": "2110646",
			"driverId": "4786",
			"escortId": "5137"
		},
		"chemical": [{
			"chemicalId": "3",
			"chemicalAliasUsing": "别名1",
			"weight": "5",
			"volume": "0"
		},
		{
			"chemicalId": "2",
			"chemicalAliasUsing": "别名2",
			"weight": "5",
			"volume": "0"
		}]
	}
}
```

##### 响应示例
```
{
    "status": 1,
    "data": {
        "billId": 71344
    },
    "message": "成功"
}
```