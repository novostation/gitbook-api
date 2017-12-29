#### 查询收发货方

##### 接口地址

```
/app/dyBillShipReceiveUnit/listPage/1/5?billIdIsNull=null
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billIdIsNull | String | 查询运单ID为null的收发货方 | True |
| billNo | String | 运单号 | FALSE |
| unitType | String | 收发货方类型 1：发货方 2 ：收货方 | FALSE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |

##### 调用示例

```
url: /app/dyBillShipReceiveUnit/listPage/1/5?billIdIsNull=null
```

##### 响应示例

```
{
    "status": 1,
    "data": {
        "pageNum": 1,
        "pageSize": 5,
        "size": 3,
        "startRow": 1,
        "endRow": 3,
        "total": 3,
        "pages": 1,
        "list": [
            {
                "billUnitId": 31417,
                "billId": null,
                "billNo": "123456",
                "companyId": 1,
                "bsUnitId": 21,
                "unitName": "对个话gg",
                "unitType": 1,
                "contactPerson": "对个话",
                "contactTel": "13710120665",
                "fax": "07533606222",
                "remark": "1",
                "createdUser": "1"
            },
            {
                "billUnitId": 31415,
                "billId": null,
                "billNo": "20171030420604",
                "companyId": null,
                "bsUnitId": null,
                "unitName": "ghdfh",
                "unitType": 1,
                "contactPerson": "dhgfhd",
                "contactTel": "13710120645",
                "fax": "07533606555",
                "remark": null,
                "createdUser": "1"
            },
            {
                "billUnitId": 31409,
                "billId": null,
                "billNo": "123456",
                "companyId": 1,
                "bsUnitId": 21,
                "unitName": "对个话gg",
                "unitType": 1,
                "contactPerson": "对个话",
                "contactTel": "13710120665",
                "fax": "07533606222",
                "remark": "1",
                "createdUser": "1"
            }
        ],
        "prePage": 0,
        "nextPage": 0,
        "isFirstPage": true,
        "isLastPage": true,
        "hasPreviousPage": false,
        "hasNextPage": false,
        "navigatePages": 8,
        "navigatepageNums": [
            1
        ],
        "navigateFirstPage": 1,
        "navigateLastPage": 1,
        "lastPage": 1,
        "firstPage": 1
    },
    "message": "成功"
}
```