#### 保存运单调度信息

##### 接口地址

```
/app/dyBill/save
```

##### 请求方式

POST

##### 接口描述

请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| controlMes | String | 运单人员，司机等信息JSON数据 | Y |
| ydh | String | 运单号 | Y |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |

##### 调用示例

```
/app/dyBill/save
```

参数:

```
{
“ydh”:31407,
“controlMes”:{
        "carmes": {
            "vehicleId": 20000005,
            "companyId": null,
            "numberPlate": "粤C10000-黄",
            "numberPlateColor": "黄",
            "vehicleType": null,
            "vehicleCategory": null,
            "approvedWeight": 1111,
            "approvedVolume": 1111,
            "vendor": null,
            "model": null,
            "fuelType": null,
            "engineModel": null,
            "transportCertificateNo": null,
            "certificateExpireDate": null,
            "auditExpireDate": null,
            "length": null,
            "width": null,
            "height": null,
            "equipmentLevel": null,
            "firstTransportDate": null,
            "buyDate": null,
            "uselessDate": null,
            "isEquipGps": null,
            "isImport": null,
            "totalWeight": null,
            "drivingLicense": null,
            "potVolume": null,
            "potSize": null,
            "exhaustSize": null,
            "remark": null,
            "transRange": "阿斯顿发生",
            "companyNo": "A1046421",
            "companyName": null,
            "auditResult": null,
            "transportCertificateWord": null,
            "vehicleCategoryCode": null,
            "import": null
        },
        "guacarmes": {
            "vehicleId": 2000848,
            "companyId": 871835,
            "numberPlate": "粤AB255挂-黄",
            "numberPlateColor": "黄",
            "vehicleType": "重型货车",
            "vehicleCategory": "重型特殊结构半挂车",
            "approvedWeight": 28.7,
            "approvedVolume": 0,
            "vendor": "",
            "model": "YQ9400GYYA",
            "fuelType": "",
            "engineModel": "",
            "transportCertificateNo": "000824896",
            "certificateExpireDate": "2017-10-30 00:00:00",
            "auditExpireDate": "2017-06-01 00:00:00",
            "length": 11600,
            "width": 2495,
            "height": 3550,
            "equipmentLevel": "",
            "firstTransportDate": "2007-11-19 00:00:00",
            "buyDate": null,
            "uselessDate": null,
            "isEquipGps": "其他",
            "isImport": null,
            "totalWeight": 39900,
            "drivingLicense": "",
            "potVolume": 0,
            "potSize": "",
            "exhaustSize": 0,
            "remark": "",
            "transRange": "危险货物运输[3类（仅准许运输：己烷）]\r\n禁运爆炸品，剧毒化学品，强腐蚀性危险货物。",
            "companyNo": "A1046421",
            "companyName": "广州市黄埔穗兴储运公司",
            "auditResult": "合格",
            "transportCertificateWord": "",
            "vehicleCategoryCode": 3,
            "import": null
        },
        "drivers": {
            "origId": "0YVEM6T0527T",
            "employeeId": 5475,
            "employeeName": "罗学红",
            "employeeTypeName": "危险品运输",
            "sex": "男",
            "bornDate": "1973-12-18 00:00:00",
            "telephone": "",
            "qualificationNo": "441827197312188910",
            "qualificationExpireDate": "2020-09-03 00:00:00",
            "qualificationDeliveryDate": "2017-03-30 00:00:00",
            "qualificationType": "经营性道路货物运输驾驶员、道路危险货物运输驾驶员",
            "qualificateOrganId": null,
            "qualificateOrganName": "广州市交通委员会",
            "companyNo": "A1046421",
            "createdUser": "",
            "createdTime": "2017-10-26 11:18:54",
            "updatedUser": "",
            "idCardNo": "441827197312188910",
            "udpatedTime": null,
            "nation": "汉族",
            "country": "中国",
            "driverCardNo": "",
            "driverCardType": "B2",
            "driverCardReceiveDate": "2012-08-08 00:00:00",
            "livingAddress": "广东省清新县浸潭镇建辉村委会上围村36号",
            "homeAdress": "广东省清新县浸潭镇建辉村委会上围村36号",
            "homeContactTel": "",
            "postCode": "510000",
            "educationDegree": "初中",
            "employeStatus": "在岗",
            "auditDate": null,
            "auditPerson": "",
            "auditOrgan": "",
            "remark": "",
            "employeeType": 1,
            "employeeTypeNameOrig": "危险品运输"
        },
        "yayundrivers": {
            "origId": "0Y3J731005A0",
            "employeeId": 6229,
            "employeeName": "邓全民",
            "employeeTypeName": "危险品押运",
            "sex": "男",
            "bornDate": "1965-07-02 00:00:00",
            "telephone": "",
            "qualificationNo": "511121196507021755",
            "qualificationExpireDate": "2021-01-17 00:00:00",
            "qualificationDeliveryDate": "2015-11-25 00:00:00",
            "qualificationType": "道路危险货物运输押运人员",
            "qualificateOrganId": null,
            "qualificateOrganName": "广州市交通委员会",
            "companyNo": "A1046421",
            "createdUser": "",
            "createdTime": "2017-10-26 11:18:59",
            "updatedUser": "",
            "idCardNo": "511121196507021755",
            "udpatedTime": null,
            "nation": "汉族",
            "country": "中国",
            "driverCardNo": "",
            "driverCardType": "",
            "driverCardReceiveDate": "2003-01-03 00:00:00",
            "livingAddress": "广州市海珠区工业大道南882号",
            "homeAdress": "四川省仁寿县宝石乡孙家村9组",
            "homeContactTel": "",
            "postCode": "510288",
            "educationDegree": "初中",
            "employeStatus": "在岗",
            "auditDate": null,
            "auditPerson": "",
            "auditOrgan": "",
            "remark": "",
            "employeeType": 2,
            "employeeTypeNameOrig": "危险品押运"
        },
        "shipdate": "2017-10-06",
        "receptdate": "2017-10-21"
    }
}
```

##### 响应示例

```
{
    "status": 1
    "data": null,
    "message": "成功"
}
```

