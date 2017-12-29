#### 更新收发货方

##### 接口地址

```
/app/dyBillShipReceiveUnit/updateAll
```

##### 请求方式

POST

##### 接口描述

先删除收发货方及地址及货物,后重新保存数据

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| data | String | 收发货方和地址和货物JSON信息 | Y |
| unitType | INTEGER | 1：发货方2收货方 | N |
| billUnitId | INTEGER | 收发货方主键ID | Y |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |

##### 调用示例

```
/app/dyBillShipReceiveUnit/updateAll
```

参数：

```
{
“billUnitId”:31407,
“unitType”:1,
“data”:{
    "ydh": "123456",
    "shipBaseMes": {
        "unitId": 21,
        "unitName": "对个话gg",
        "unitType": 1,
        "cityType": null,
        "transportCompanyId": 1,
        "chemicalCompanyId": 1,
        "contactPerson": "对个话",
        "contactTel": "13710120665",
        "fax": "07533606222",
        "remark": "1"
    },
    "shipAdderssGoodsMes": [{
        "addressMes": {
            "addressId": 39,
            "transportCompanyId": 1,
            "provinceId": 1,
            "cityId": 1,
            "regionId": 1,
            "provinceName": "广东",
            "cityName": "广州",
            "regionName": "萝岗区",
            "roadDetail": "萝岗科汇金谷",
            "addressType": 1,
            "addressName": "潘"
        },
        "addressGoodsMes": [{
            "bieming": {
                "id": 28,
                "chemicalId": 2933,
                "companyId": 855722,
                "chemicalAlias": "2351"
            },
            "baozhaung": {
                "id": 28,
                "companyId": 855722,
                "packMethod": "2351",
                "packLevel": 2,
                "chemicalId": 2933
            },
            "weight": "1",
            "volume": "5"
        },
        {
            "bieming": {
                "id": 29,
                "chemicalId": 2928,
                "companyId": 855722,
                "chemicalAlias": "2345"
            },
            "baozhaung": {
                "id": 29,
                "companyId": 855722,
                "packMethod": "2345",
                "packLevel": 2,
                "chemicalId": 2928
            },
            "weight": "5",
            "volume": "6"
        }]
    },
    {
        "addressMes": {
            "addressId": 32,
            "transportCompanyId": 1,
            "provinceId": 1,
            "cityId": 1,
            "regionId": 1,
            "provinceName": "北京",
            "cityName": "东城区",
            "regionName": "",
            "roadDetail": "pp",
            "addressType": 1,
            "addressName": "pp"
        },
        "addressGoodsMes": [{
            "bieming": {
                "id": 16,
                "chemicalId": 2930,
                "companyId": 855722,
                "chemicalAlias": "gg"
            },
            "baozhaung": {
                "id": 16,
                "companyId": 855722,
                "packMethod": "gg",
                "packLevel": 2,
                "chemicalId": 2930
            },
            "weight": "6",
            "volume": "6"
        }]
    }]
    }
}
```

##### 响应示例

```
{
    "status": 1
    "data": null,
    "message": "更新数据成功"
}
```