#### 获取常用危化品

##### 接口地址

```
/app/bsChemicalUsing/getInfoById/{id}
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| id| Long | 常用危化品主键id | TRUE|


##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| id| Long | 常用危化品id | 
| chemicalId| Long | 危化品id |
| chemicalAlias| String | 危化品别名 |
| chemicalName| String | 危化品名称 |
| packLevel| Integer | 包装级别 | 
| packSpec| String | 包装规格| 
| chemicalType| Integer | 危化品类别 | 
| itemNo| Integer | 项号 | 
| unionCode| String | 国际编号 |


##### 调用示例

```
url:/app/bsChemicalUsing/getInfoById/2
```



##### 响应示例

```
{
    "status": 1,
    "data": {
        "id": 2,
        "chemicalId": 2,
        "companyId": 837398,
        "chemicalAlias": "武器弹药筒fffffffffffsfdfasdf",
        "chemicalName": "",
        "packLevel": "",
        "packSpec": "",
        "chemicalType": "",
        "itemNo": "",
        "unionCode": "",
        "createdUser": "",
        "createdUserId": "",
        "createdTime": "2018-01-16 19:40:16"
    },
    "message": "获取数据成功"
}
```

