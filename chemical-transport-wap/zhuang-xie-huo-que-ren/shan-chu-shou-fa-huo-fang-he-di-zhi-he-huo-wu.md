#### 删除收发货方和地址和货物 {#-1}

##### 接口地址
```
/app/dyBillShipReceiveUnit/delete/{billUnitId}
```
##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billUnitId | Long | 运单收发货方id |TRUE|

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- ||
| status| Integer | 1: 成功 0：失败|


##### 调用示例
```
/app/dyBillShipReceiveUnit/delete/5584
```

##### 响应示例


