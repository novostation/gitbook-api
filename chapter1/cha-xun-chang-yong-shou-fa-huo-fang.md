#### 查询收发货方

##### 接口地址

```
/app/bsShipReceiveUnit/listPage
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
|pageNum| Integer | 页码| TRUE |
| pageSize| Integer | 每页最大数量| TRUE |
| unitName| String | 收发货方名称| FALSE|

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
url: /app/bsShipReceiveUnit/listPage
```

##### 响应示例

```
{
    "status": 1,
    "data": {
        "pageNum": 1,
        "pageSize": 1,
        "size": 1,
        "startRow": 1,
        "endRow": 1,
        "total": 17,
        "pages": 17,
        "list": [
            {
                "unitId": 137,
                "unitName": "收货2",
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
                "createdTime": "2018-01-18 18:34:20"
            }
        ],
        "prePage": 0,
        "nextPage": 2,
        "isFirstPage": true,
        "isLastPage": false,
        "hasPreviousPage": false,
        "hasNextPage": true,
        "navigatePages": 8,
        "navigatepageNums": [
            1,
            2,
            3,
            4,
            5,
            6,
            7,
            8
        ],
        "navigateFirstPage": 1,
        "navigateLastPage": 8,
        "firstPage": 1,
        "lastPage": 8
    },
    "message": "成功"
}
```