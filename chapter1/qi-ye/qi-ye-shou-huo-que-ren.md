#### 企业收货确认

##### 接口地址

```
/app/confirm/companyUnloadConfirm
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billUnitId| String| 待装货装货中标识| TRUE |
| billAddressId| String| 运单号| FALSE|
| chemical| String| JSON数组 |TRUE |
| id| String| 货物ID |TRUE |
| weight| String| 重量 |TRUE |
| volume| String| 体积 |TRUE |



##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |

##### 调用示例

```
url:/app/confirm/companyUnloadConfirm
```
参数:
``` json
{
	"data": {
		"billUnitId": "32645",
		"billAddressId": "33034",
		"chemical": [{
			"id": "35472",
			"weight": "5",
			"volume": "0"
		},
		{
			"id": "35473",
			"weight": "6",
			"volume": "0"
		}]
	}
}
```
##### 响应示例
``` json
{
    "status": 1,
    "data": "",
    "message": "成功"
}
```
