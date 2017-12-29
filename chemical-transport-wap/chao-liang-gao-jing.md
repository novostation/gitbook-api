### 超量告警

#### 查询超量告警

##### 接口地址

```
/app/dyAlarmExcess/listExcess/{pageNum}/{pageSize}
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
| permitWeight | String | 核定运输量 |
| realWeight | String | 实际运输量 |
| chemicalUnit | String | 货物单位 |
| permitTransRange | String | 许可运输范围 |
| realTransChemical | String | 实际运输品种 |
| permitVolume | String | 核定运输体积 |
| realVolume | String | 实际运输体积 |
| message | String | 告警信息 |

##### 调用示例

```
url:/app/dyAlarmExcess/listExcess/1/1
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
        "total": 9,
        "pages": 9,
        "list": [
            {
                "alarmId": 13587,
                "billNo": "20171129325102",
                "billId": 559,
                "alarmCategoryId": 6,
                "alarmCategoryName": "运输超量告警",
                "alarmTypeId": 9,
                "alarmTypeName": "车辆运输范围不符告警",
                "alarmName": "车辆运输范围不符告警",
                "alarmDesc": "车辆允许的运输范围是:危险货物运输[2类1项（仅准许运输：液化石油气）]\r\n禁运爆炸品，剧毒化学品，强腐蚀性危险货物。  实际运输的是:2类2项(二氧化碳)",
                "alarmBeginTime": "2017-11-29 09:45:51",
                "alarmEndTime": "",
                "transportCompanyId": 874862,
                "transportCompanyName": "广州市芳村东兴运输有限公司",
                "numberPlate": "粤A173GZ-蓝",
                "tailerNumberPlate": "",
                "driverId": 1236,
                "driverName": "廖国金",
                "escortId": 72,
                "escortName": "高岩",
                "handleStatus": "",
                "handleTime": "",
                "driverContactTel": "",
                "escortContactTel": "13048056994",
                "companyContactTel": "81512890",
                "createTime": "2017-11-29 10:40:14",
                "sendCompanyName": "喜威石榴岗气站",
                "receiveCompanyName": "张亮麻辣烫",
                "sendCompanyId": "1173",
                "receiveCompanyId": "1174",
                "chemicalName": "二氧化碳",
                "remark": "",
                "permitWeight": "",
                "realWeight": "",
                "chemicalUnit": "",
                "permitTransRange": "危险货物运输[2类1项（仅准许运输：液化石油气）]\r\n禁运爆炸品，剧毒化学品，强腐蚀性危险货物。",
                "realTransChemical": "2类2项(二氧化碳)",
                "permitVolume": "",
                "realVolume": "",
                "message": ""
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



