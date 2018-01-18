#### 查询人员

##### 接口地址

```
/app/bsEmployee/listPage
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
| employeeName| String| 人员姓名 |FALSE|

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| employeeId| Long| 人员ID |
| employeeName| String | 姓名 |
| employeeType| Integer | 从业人员类型1：驾驶员；2：押运员；3：驾驶员和押运员 | 
| sex| String | 性别 | 
| telephone| String | 电话号码 | 
| idCardNo| String | 身份证| 
| qualificationNo| String | 从业资格证 | 
| qualificationExpireDate| String | 资格证有效期 |


##### 调用示例

```
url:/app/bsEmployee/listPage
参数:{pageNum:1,pageSize:1}
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
        "total": 8,
        "pages": 8,
        "list": [
            {
                "origId": "",
                "employeeId": 6968,
                "employeeName": "何汉通",
                "employeeTypeName": "",
                "sex": "男",
                "bornDate": "1972-01-25 00:00:00",
                "telephone": "15875338309",
                "qualificationNo": "441824197201250612",
                "qualificationExpireDate": "2021-04-20 00:00:00",
                "qualificationDeliveryDate": "2016-05-18 00:00:00",
                "qualificationType": "经营性道路旅客运输驾驶员、经营性道路货物运输驾驶员",
                "qualificateOrganId": "",
                "qualificateOrganName": "广州市交通运输管理局",
                "companyId": 1767771,
                "companyNo": "",
                "createdUser": "zhangsan",
                "createdUserId": 1,
                "createdTime": "2008-12-08 09:15:20",
                "updatedUser": "陈琳@广州市交通运输管理局",
                "idCardNo": "441824197201250612",
                "udpatedTime": "2016-05-18 10:29:22",
                "nation": "汉",
                "country": "",
                "driverCardNo": "",
                "driverCardType": "A",
                "driverCardReceiveDate": "1994-12-26 00:00:00",
                "livingAddress": "广东省连州市连州镇人民路168号",
                "homeAdress": "广东省连州市连州镇人民路168号",
                "homeContactTel": "null",
                "postCode": "513400",
                "educationDegree": "高中",
                "employeStatus": "",
                "auditDate": "",
                "auditPerson": "",
                "auditOrgan": "",
                "remark": "123",
                "employeeType": 1,
                "employeeTypeNameOrig": ""
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

