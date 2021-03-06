#### 保存收发货方

##### 接口地址

```
/app/bsShipReceiveUnit/save
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| unitName| String | 收发货方名称|TRUE|
| unitType| Integer| 1:  发货、装货2：收货、卸货 |FALSE|
| transportCompanyId| Long| 运输企业ID |TRUE|
| chemicalCompanyId| Long| 危化品公司ID |TRUE|
| contactPerson| String | 联系人 |FALSE|
| contactTel| String | 联系电话 |FALSE|
| fax| String | 传真 |FALSE|
| remark| Integer| 备注 |FALSE|

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |
| data| String | 响应数据 |
| unitId| Long| 收发货方ID |
| unitName| String | 收发货方名称|
| unitType| Integer| 1:  发货、装货2：收货、卸货 |
| transportCompanyId| Long| 运输企业ID |
| chemicalCompanyId| Long| 危化品公司ID |
| contactPerson| String | 联系人 |
| contactTel| String | 联系电话 |
| fax| String | 传真 |
| remark| Integer| 备注 |

##### 调用示例

```
url: /app/bsShipReceiveUnit/saveAll
```

参数:
``` json
{	
	"unitName": "收货2",
	"unitType": 2,
	"cityType": 2,
	"transportCompanyId": 22,
	"chemicalCompanyId": 2,
	"contactPerson": "潘生22",
	"contactTel": "13710120666",
	"fax": "020-3603667",
	"remark": "收货方1备注"
}
```

##### 响应示例

``` json
{
    "status": 1,
    "data": {
        "unitId": 139,
        "unitName": "收货22",
        "unitType": 2,
        "cityType": 2,
        "transportCompanyId": 22,
        "chemicalCompanyId": 2,
        "contactPerson": "潘生22",
        "contactTel": "13710120666",
        "fax": "020-3603667",
        "remark": "收货方1备注",
        "createdUser": "zhangsan",
        "createdUserId": 1,
        "createdTime": "2018-01-18 18:35:49"
    },
    "message": "保存数据成功"
}

```



