#### 保存人员

##### 接口地址

```
/app/bsEmployee/save
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| employeeName| String | 姓名 | TRUE|
| employeeType| Integer | 从业人员类型1：驾驶员；2：押运员；3：驾驶员和押运员 | TRUE|
| sex| String | 性别 | FALSE |
| telephone| String | 电话号码 | FALSE |
| idCardNo| String | 身份证| FALSE |
| qualificationNo| String | 从业资格证 | FALSE |
| qualificationExpireDate| String | 资格证有效期 | FALSE |

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |
| employeeId| Long| 人员ID |
##### 调用示例

```
url:/app/bsEmployee/save

参数:

{      
    
    "employeeName": "何汉通",
    "sex": "男",
    "telephone": "15875338309",
    "qualificationNo": "441824197201250612",
    "qualificationExpireDate": "2021-04-20 00:00:00",       
    "idCardNo": "441824197201250612",      
    "employeeType": 1: ""
}
```



##### 响应示例

```
{
    "status": 1,
    "data":6968,
    "message": "获取数据成功"
}
```

