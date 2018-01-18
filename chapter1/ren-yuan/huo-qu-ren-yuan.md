#### 获取人员

##### 接口地址

```
/app/bsEmployee/getInfoById/{employeeId}
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| employeeId| Long| 人员ID |TRUE|

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
url:/app/bsEmployee/getInfoById/1
```



##### 响应示例

```
{
    "status": 1,
    "data": {
        "origId": "0Y3J731004ZN",
        "employeeId": 1,
        "employeeName": "刘佳",
        "employeeTypeName": "危险品押运员",
        "sex": "男",
        "bornDate": "1983-01-22 00:00:00",
        "telephone": "18922743848",
        "qualificationNo": "120102198301222910",
        "qualificationExpireDate": "2019-04-27 00:00:00",
        "qualificationDeliveryDate": "2013-04-27 00:00:00",
        "qualificationType": "道路危险货物押运人员",
        "qualificateOrganId": "",
        "qualificateOrganName": "广州市交通运输管理局",
        "companyId": 1016459,
        "companyNo": "A1072797",
        "createdUser": "",
        "createdUserId": "",
        "createdTime": "2018-01-12 11:53:17",
        "updatedUser": "",
        "idCardNo": "120102198301222910",
        "udpatedTime": "",
        "nation": "汉",
        "country": "中国",
        "driverCardNo": "",
        "driverCardType": "A2",
        "driverCardReceiveDate": "",
        "livingAddress": "天津市河东区卫国道益寿东里31号楼603号",
        "homeAdress": "天津市河东区卫国道益寿东里31号楼603号",
        "homeContactTel": "",
        "postCode": "510000",
        "educationDegree": "本科",
        "employeStatus": "在岗",
        "auditDate": "",
        "auditPerson": "",
        "auditOrgan": "",
        "remark": "",
        "employeeType": 2,
        "employeeTypeNameOrig": "危险品押运"
    },
    "message": "获取数据成功"
}
```

