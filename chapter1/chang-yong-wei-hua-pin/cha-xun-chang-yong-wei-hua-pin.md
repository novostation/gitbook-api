#### 查询常用危化品

##### 接口地址

```
/app/bsChemical/listChemicalAndChemicalUsing
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| pageNum | Integer | 页码 | TRUE |
| pageSize | Integer | 每页记录数 | TRUE |
|chemicalNameUnionCode | String| 危化品名称和联合国编码联合查询 | FALSE |


##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| id| Long| 常用危化品ID |
| chemicalId| Long| 危化品ID |
| chemicalName| String | 危化品名称 |
| chemicalAliasUsing| String |常用危化品别名 |
| unionCode| String | 联合国编码 |
| chemicalUnit| String | 货物单位 |

##### 调用示例

```
url:/app/bsChemical/listChemicalAndChemicalUsing

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
        "total": 9,
        "pages": 9,
        "list": [
            {
                "chemicalId": 2924,
                "chemicalName": "溴甲基丙烷",
                "chemicalType": 3,
                "itemNo": "",
                "chemicalCode": "",
                "unionCode": "2342",
                "chemicalAlias": "",
                "characters": "",
                "flag": "",
                "packLevel": 2,
                "packMethod": "",
                "packSpec": "",
                "extinguisher": "",
                "washNo": "",
                "emergencyMeasure": "",
                "specialRules": "",
                "chemicalLevel": "",
                "seqNo": "",
                "createdUser": "",
                "createdTime": "2017-12-21 14:48:47",
                "updatedUser": "",
                "updatedTime": "2017-09-25 16:38:34",
                "auditUser": "",
                "auditTime": "2016-11-28 09:28:21",
                "auditStatus": "",
                "casName": "",
                "secondaryDanger": "",
                "remark": "",
                "chemicalUnit": "吨",
                "id": 64,
                "companyId": 20000004,
                "chemicalAliasUsing": "溴甲基丙烷"
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
        "lastPage": 8,
        "firstPage": 1
    },
    "message": "成功"
}

```
