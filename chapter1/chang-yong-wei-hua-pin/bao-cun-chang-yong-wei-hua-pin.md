#### 保存常用危化品

##### 接口地址

```
/app/bsChemicalUsing/save
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| chemicalId| Long | 危化品id | TRUE|
| chemicalAlias| String | 危化品别名 | TRUE|
| chemicalName| String | 危化品名称 | FALSE |
| packLevel| Integer | 包装级别 | TRUE|
| packSpec| String | 包装规格| TRUE|
| chemicalType| Integer | 危化品类别 | FALSE |
| itemNo| Integer | 项号 | FALSE |
| unionCode| String | 国际编号 | FALSE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |

##### 调用示例

```
url:/app/bsChemicalUsing/save

参数:

{        
"chemicalId": 1,
"chemicalAlias": "1",
"chemicalName": "",
"packLevel": 2,
"packSpec": "",
"chemicalType": "",
"itemNo": "",
"unionCode": ""
}
```



##### 响应示例

```
{
    "status": 1,
    "data":"",
    "message": "保存数据成功"
}
```

