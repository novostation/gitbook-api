## 超量告警查询

### 接口地址

```
/app/dyAlarmExcess/listExcess/{pageNumber}/{pageSize}
```

## 请求方式：POST

## 接口描述

运输企业超量预警信息列表及查询

## 请求参数

请求格式:JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| :---: | :---: | :---: | :---: |
| pageNumber | Integer | 页码 | Y |
| pageSize | Integer | 每页最大记录数 | Y |
| numberPlate | String | 车牌号 | N |
| alarmTypeId | Integer | 告警类型 | N |
| transportCompanyName | String | 运输企业名称 | N |
| alarmBeginTime | String | 起始时间段 | N |
| alarmEndTime | String | 终止时间段 | N |

## 相应参数

参数格式：JSON

| 参数名 | 类型 | 描述 |
| :---: | :---: | :---: |
| alarmId | Long | 基础告警ID |
| alarmTypeId | Long | 告警类型ID |
| numberPlate | String | 车牌号 |
| chemicalName | String | 危化品名称 |
| transportCompanyName | String | 运输企业名称 |
| chuCompany | String | 流出企业名称 |
| ruCompany | String | 流入企业名称 |
| alarmTypeName | String | 告警类型名称 |
| vehicleCategory | String | 车辆准载类型 |
| realWeight | Float | 车辆实载重量 |
| permitWeight | Float | 车辆准载重量 |
| alarmBeginTime | String | 告警起始时间 |
| chemicalUnit | String | 货物单位 |

告警类型：

| 名称 | alarmTypeId |
| --- | --- |
| 运输超载告警 | 8 |
| 运输范围不符告警 | 9 |

## 请求示例

url:

```
/app/dyAlarmExcess/listExcess/1/2?numberPlate=989
```

参数：

## 响应示例

```json
{
    "status": 1,
    "data": {
        "pageNum": 1,
        "pageSize": 10,
        "size": 1,
        "startRow": 1,
        "endRow": 1,
        "total": 1,
        "pages": 1,
        "list": [
            {
                "alarmId": 161,
                "alarmTypeId": 8,
                "numberPlate": "粤ABD989-黄-黄-黄-黄",
                "chemicalName": "3-溴丙炔",
                "transportCompanyName": "广州二运集团有限公司",
                "chuCompany": null,
                "ruCompany": null,
                "alarmTypeName": "运输超载告警",
                "vehicleCategory": "重型罐式货车",
                "permitWeight": 13.5,
                "realWeight": 0,
                "alarmBeginTime": "2017-11-08 11:29:33"
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