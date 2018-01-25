#### 司机广州取货创建卸货单

##### 接口地址

```
/app/dyBill/saveDriverUnloadingBill
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billId| Integer| 地址| TRUE |
| companyId| Integer | 危化品企业ID| TRUE |
| companyPhone| String| 地址| TRUE |
| address| String| 地址| TRUE |
| companyId| Integer | 危化品企业ID| TRUE |
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
| qrCodeId| Integer | 二维码ID|

##### 调用示例

``` json
url:/app/dyBill/saveDriverUnloadingBill
```
参数:
```
{
	"data": {
		"billId": "71347",
		"companyId": "20000001",
		"companyPhone": "15920113404",
		"address": "dadwa",		
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
        "qrCodeId": 290
    },
    "message": "成功"
}
```