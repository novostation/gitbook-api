#### 企业确认地址和货物数量

##### 接口地址

```
/app/confirm/companyConfirmAddressAndChemical
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| data | JSONARRAY | 数据 | TRUE |
| transType | Integer | 1: 发货、装货 2：收货、卸货 | TRUE |
| billAddressId | Long | 运单收发货方装卸货地址id | TRUE |
| transType | Integer | 1: 发货、装货 2：收货、卸货 | TRUE |
| remark| String |备注|FALSE|
| chemical| JSONARRAY| 货物信息 |TRUE|
| id| Long | 货物ID |TRUE|
| weight| Float| 企业确认重量 |TRUE|
| volume| Float| 企业确认体积 |TRUE|

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |

##### 调用示例

```
url:/app/confirm/companyConfirmAddressAndChemical

```

参数：

```
{
	"data": {
		"billAddressId": "29001",
		"transType": "1",
		"remark": "",
		"chemical": [{
			id: "31571",
			weight: "10086",
			volume: "5"
		}]
	}
}
```

##### 响应示例

```json
{
    "status": 1,
    "data": {
        "billStatus": "运输中"
    },
    "message": "更新数据成功"
}
```



