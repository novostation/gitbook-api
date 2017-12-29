### 线路告警

#### 查询线路告警

##### 接口地址

```
/app/dyAlarmRoute/listPage/{pageNum}/{pageSize}
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


##### 响应参数

格式：JSON

| 参数名 | **类型** | **描述** |
| --- | --- | --- |
| alarmId | Long | 告警id |
| billId | Long | bill_id |
| billNo | String | 运单号 |
| alarmCategoryId | Long | 告警类别id |
| alarmCategoryName | String | 告警类别名称 |
| alarmTypeId | Long | 告警类型id |
| alarmTypeName | String | 告警类型名称 |
| alarmName | String | 告警名称 |
| alarmDesc | String | 告警描述 |
| alarmBeginTime | String | 告警开始时间 |
| alarmEndTime | String | 告警结束时间 |
| transportCompanyId | Long | 运输公司id |
| transportCompanyName | String | 运输公司名称 |
| numberPlate | String | 车牌（包括颜色） |
| tailerNumberPlate | String | 挂车车牌（包括颜色） |
| driverId | Long | 司机id |
| driverName | String | 司机名称 |
| escortId | Long | 押运员id\n |
| escortName | String | 押运员名称 |
| handleStatus | Integer | 1: 未通知\n2：已通知\n3：已确认\n4：已处理 |
| handleTime | String | 处理时间 |
| driverContactTel | String | 司机电话 |
| escortContactTel | String | 押运员电话 |
| companyContactTel | String | 运输公司联系电话 |
| createTime | String | 创建时间 |
| sendCompanyName | String | 发货企业名称(拼接) |
| receiveCompanyName | String | 收货企业名称(拼接) |
| sendCompanyId | String | 发货企业id(拼接) |
| receiveCompanyId | String | 收货企业id(拼接) |
| chemicalName | String | chemical_name |
| remark | String | 备注 |
| alarmType | String | 告警类型1: 超速告警2：停车超时告警3：线路偏离告警 |
| settingValue | String | 设定值 |
| currentValue | String | 告警值 |
| startLatitude | String | 开始告警纬度 |
| startLongitude | String | 开始告警经度 |
| endLatitude | String | 结束告警纬度 |
| endLongitude | String | 结束告警经度 |
| startAddress | String | 开始告警地址 |
| endAddress | String | 结束告警地址 |
| startTime | String | 起始时间 |
| endTime | String | 结束时间 |
| maxValue | String | 最大速度 |

##### 调用示例

```
url:/app/dyAlarmRoute/listPage/1/1
```

##### 响应示例

```json
{
    "status": 1,
    "data": {
        "pageNum": 1,
        "pageSize": 1,
        "size": 1,
        "startRow": 1,
        "endRow": 1,
        "total": 476,
        "pages": 476,
        "list": [
            {
                "alarmId": 13607,
                "billNo": "20171129326086",
                "billId": 730,
                "alarmCategoryId": 3,
                "alarmCategoryName": "线路监控告警",
                "alarmTypeId": 10,
                "alarmTypeName": "超速告警",
                "alarmName": "超速告警",
                "alarmDesc": "",
                "alarmBeginTime": "2017-11-29 15:51:55",
                "alarmEndTime": "",
                "transportCompanyId": 871835,
                "transportCompanyName": "广州市黄埔穗兴储运公司",
                "numberPlate": "粤AK9361-黄",
                "tailerNumberPlate": "粤AS537挂-黄",
                "driverId": 4046,
                "driverName": "欧壬寿",
                "escortId": 4072,
                "escortName": "欧均荣",
                "handleStatus": 1,
                "handleTime": "",
                "driverContactTel": "13690385651",
                "escortContactTel": "",
                "companyContactTel": "A1042206",
                "createTime": "2017-11-29 15:51:55",
                "sendCompanyName": "东莞竣成;广州赫尔普化工有限公司",
                "receiveCompanyName": "东莞竣成;广州赫尔普化工有限公司",
                "sendCompanyId": "",
                "receiveCompanyId": "",
                "chemicalName": "己烷",
                "remark": "",
                "alarmType": "1",
                "settingValue": 70,
                "currentValue": 74,
                "startLatitude": 22.8394,
                "startLongitude": 113.145,
                "endLatitude": 22.9058,
                "endLongitude": 113.485,
                "startAddress": "广东省 佛山市 顺德区新城村正南 370 米",
                "endAddress": "广东省 广州市 番禺区Ｇ４Ｗ广澳高速(从石清公路出入口到观音沙大桥)观音沙大桥西南 28 米",
                "startTime": "2017-11-29 15:19:59",
                "endTime": "",
                "maxValue": ""
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



