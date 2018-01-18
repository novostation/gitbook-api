#### 获取用户地址

##### 接口地址

```
/app/dyBill/getInfoById/{billId}
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billId| Integer | 运单ID| TRUE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| createdTime| String | 运单日期|
| unitName| String | 收发货方 |
| billNo| String| 运单号 |
| loadGoodsDate|String| 装货日期 |
| predictUnloadDate| String | 预到日期|
| numberPlate| String| 车牌号 |
| tailerNumberPlate| String| 挂车车牌号 |
| transportCompanyName| String| 运输企业 |
| driverName| String| 驾驶员|
| driverContactNo| String| 驾驶员电话号码 |
| escortName| String| 押运员 |
| escortContactNo| String| 押运员电话号码 |
| dyBillShipReceiveUnitDtoList1| JSON字符串| 发货方信息 |
| dyBillShipReceiveUnitDtoList2| JSON字符串| 收货方信息 |
| unitName| String| 收发货方名称 |
| dyBillAddressDtoList|Jsong数组| 地址信息 |
| roadDetail| String| 地址详情 |
| loadCheckUserName| String| 装卸货司机 |
| loacCheckUserTel| String| 装卸货司机电话 |
| loadCheckTime| String| 装卸货时间 |
| ckeckUserName| String| 收发货企业人员 |
| checkUserTel| String| 收发货企业人员电话 |
| ckeckTime| String| 收发货时间 |
| dyBillChemicalDtoList| Jsong数组| 货物信息 |
| chemicalName| String| 货物名称 |
| weight| Float| 重量 |
| volume| Float| 体积 |
| checkWeight| Float| 企业确认重量 |
| checkVolume| Float| 企业确认体积 |
| loadCheckWeight| Float| 司机确认重量 |
| loadCheckVolume| Float| 司机确认体积 |
| chemicalTypeName| String| 货物类型 |
| chemicalUnit| String | 货物单位|
| checkRemark| String | 备注|

##### 调用示例

```
url:/app/dyBill/getInfoById/70730
```
##### 响应示例