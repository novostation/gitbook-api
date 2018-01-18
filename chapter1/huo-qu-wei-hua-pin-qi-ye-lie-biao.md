#### 获取危化品企业列表

##### 接口地址

```
/app/bsCompany/listChemicalCompany
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| pageNum| Integer | 页码| TRUE |
| pageSize| Integer | 每页最大数量| TRUE |
| billNo| String| 运单号| FALSE|
| startTime| String| 开始时间| FALSE |
| endTime| String| 结束时间| FALSE|

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| pageNum| Integer | 页码|
| pageSize| Integer | 每页最大数量|
| list| JSON数组| 响应数据|
| billId| Integer | 运单ID|
| billNo| String| 运单号|
| predictUnloadDate| String | 预到日期|
| numberPlate| String| 车牌号 |
| codeName| String| 运单状态 |

##### 调用示例

```
url:/app/bsCompany/listChemicalCompany
参数:{pageNum:1,pageSize:1}
```

##### 响应示例
``` json
{
    "status": 1,
    "data": {
        "pageNum": 1,
        "pageSize": 1,
        "size": 1,
        "startRow": 1,
        "endRow": 1,
        "total": 201845,
        "pages": 201845,
        "list": [
            {
                "companyId": 20201845,
                "companyName": "广东侨丰实业股份有限公司",
                "companyType": 2,
                "companyTransportType": "",
                "companyNo": "",
                "regionId": "",
                "regionName": "",
                "socialNo": "",
                "registrationMark": "",
                "registrationExpireDate": "",
                "registrationMoney": "",
                "businessPermitNo": "",
                "permitExpireDate": "",
                "artificialPerson": "",
                "artificialPersonIdNo": "",
                "artificialPersonTel": "",
                "totalPerson": "",
                "contactPerson": "",
                "contactTel": "",
                "contactDepartment": "",
                "address": "默认地址",
                "longitude": "",
                "latitude": "",
                "createdUser": "",
                "createdUserId": "",
                "createdTime": "2018-01-17 14:21:38",
                "updatedUser": "",
                "udpatedTime": "2018-01-17 14:21:38",
                "bussinessRange": "",
                "postCode": "",
                "chargePerson": "",
                "chargePersonIdNo": "",
                "chargePersonTel": "",
                "area": "",
                "remark": ""
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
