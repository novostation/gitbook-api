#### 运单查询

##### 接口地址

```
/app/dyBill/listPage/{pageNum}/{pageSize}

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
| startTime| String | 运输开始时间 | FALSE |
| endTime | String | 运输结束时间 | FALSE |
| receiveCompany| String | 收货方名称 | FALSE |
| sendCompany| String | 发货方名称| FALSE |
| billNo| String | 运单号 | FALSE |
| receiveCompany| String | 收发货方类型 1：发货方 2 ：收货方 | FALSE |
| loadBillStatus| String |装卸货列表过滤标识，传任意值可过滤bill_status<=4的运单 | FALSE |
| billId | Number | 运单id | FALSE  |
| origId | String | orig_id | FALSE  |
| billNo | String | 运单号 | FALSE  |
| vehicleId | Number | 车辆id | FALSE |
| numberPlate | String | 运输车牌号 | FALSE  |
| numberPlateColor | String | 运输车辆车牌颜色 | FALSE  |
| tailerVehicleId | String | 挂车车牌颜色 | FALSE  |
| tailerNumberPlate | Number | 挂车车辆id | FALSE |
| tailerNumberPlateColor | String | 挂车车牌号 | FALSE |
| driverId | Number | 驾驶员id(从业人员id) | FALSE  |
| driverName | String | 驾驶员 | FALSE |
| driverCertificateNo | String | 驾驶员资格证号 | FALSE  |
| escortContactNo | String | 驾驶员联系电话 | FALSE  |
| escortId | Number | 押运员id | FALSE  |
| escortName | String | 押运员名称 | FALSE |
| escortCertificateNo | String | 押运员资格证号 | FALSE |
| escortContactNo | String | 押运员联系电话 | FALSE  |
| transportCompanyId | Number | 运输公司id | FALSE  |
| transportCompanyNo | String | 运输企业社会编号 | FALSE |
| transportCompanyName | String | 运输企业名称 | FALSE |
| createdUser | String | 创建人员 | FALSE  |
| updatedUser | String | 更新人员 | FALSE |
| billStatus | Number | 运单状态 1 ：待装货 2：装货中 3 ：运输中 4：已卸货 5 ：已完成 6:已取消 | FALSE |
| billSource | Number | 1: 来源于运单系统：来源于手机app | FALSE |
| remark | String | remark | FALSE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status | Integer | 状态码 1:成功；0：失败 |
| message | String | 响应消息 |
| billId | Number | 运单id |  |
| origId | String | orig_id |
| billNo | String | 运单号 |
| vehicleId | Number | 车辆id |
| numberPlate | String | 运输车牌号 | 
| numberPlateColor | String | 运输车辆车牌颜色 |
| tailerVehicleId | String | 挂车车牌颜色 | 
| tailerNumberPlate | Number | 挂车车辆id | 
| tailerNumberPlateColor | String | 挂车车牌号 | 
| driverId | Number | 驾驶员id(从业人员id) | 
| driverName | String | 驾驶员 |
| driverCertificateNo | String | 驾驶员资格证号 | 
| escortContactNo | String | 驾驶员联系电话 | 
| escortId | Number | 押运员id | 
| escortName | String | 押运员名称 | 
| escortCertificateNo | String | 押运员资格证号 | 
| escortContactNo | String | 押运员联系电话 | 
| transportCompanyId | Number | 运输公司id | 
| transportCompanyNo | String | 运输企业社会编号 | 
| transportCompanyName | String | 运输企业名称 | 
| loadGoodsDate | String | 装货日期 | 
| unloadGoodsDate | String | 卸货日期 | 
| predictUnloadDate | String | 预到日期 | 
| transportBeginTime | String | 运单开始时间 | 
| transportEndTime | String | 运单结束时间 | 
| createdTime | String | 运单创建时间 | 
| createdUser | String | 创建人员 | 
| updatedTime | String | 更新时间 | 
| updatedUser | String | 更新人员 | 
| billStatus | Number | 运单状态 1 ：待装货 2：装货中 3 ：运输中 4：已卸货 5 ：已完成 6:已取消 | 
| billSource | Number | 1: 来源于运单系统\n2：来源于手机app | 
| remark | String | remark | 
| chemicalName| String | 危化品名称| 
| codeName| String | 运单状态名称| 
| loadStatus| String | 装卸货状态名称 | 



##### 调用示例

```
url: /app/dyBill/listPage/1/1
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
        "total": 17320,
        "pages": 17320,
        "list": [
            {
                "origId": "0Z6F0FL19GXD",
                "billId": 17320,
                "billNo": "20171014215559",
                "vehicleId": 2991826,
                "numberPlate": "粤AN5878-黄",
                "numberPlateColor": "黄",
                "tailerVehicleId": 2992459,
                "tailerNumberPlate": "粤AS968挂-黄",
                "tailerNumberPlateColor": "黄",
                "driverContactNo": "13622758599",
                "escortContactNo": null,
                "driverId": 1520,
                "driverName": "肖健",
                "driverCertificateNo": "430525196108010051",
                "escortId": 6446,
                "escortName": "宋玉娟",
                "escortCertificateNo": "650202197704080720",
                "transportCompanyId": 990513,
                "transportCompanyNo": "A1072514",
                "transportCompanyName": "中国石油天然气运输公司广东分公司",
                "loadGoodsDate": "2017-10-14 00:00:00",
                "unloadGoodsDate": null,
                "predictUnloadDate": "2017-10-14 00:00:00",
                "transportBeginTime": null,
                "transportEndTime": null,
                "createdTime": "2017-10-14 10:31:38",
                "createdUser": "中国石油天然气运输公司广东分公司",
                "updatedTime": "2017-11-14 14:23:07",
                "updatedUser": null,
                "billStatus": 1,
                "billSource": 1,
                "remark": "接口同步数据",
                "weight": 0,
                "chemicalName": "车用汽油或汽油,车用汽油或汽油,车用汽油或汽油,车用汽油或汽油",
                "codeName": "待装货",
                "loadStatus": "未装货"
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
