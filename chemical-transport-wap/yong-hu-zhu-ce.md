#### 用户注册

##### 接口地址

```
/app/bsEmployee/addUser
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| name| String | 姓名 | TRUE |
| sex | String| 性别 | FALSE |
| idNumber| String | 身份证号码 | FALSE |
| phone| String| 手机号码 | TRUE |
| qualificationNo| String| 从业资格证 | FALSE |
| qualificationExpireDate | String|资格证有效日期 | FALSE|
|companyName|String| 公司| TRUE |
|socialNo|String | 统一社会编号 | TRUE |


##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer|1成功；0失败  |
| data| String | 相应数据 |
| message| String | 相应消息 |
##### 调用示例

```
url:/app/bsEmployee/addUser

{
	"phone": "15920113404",
	"sex": "男",
	"name": "发生的",
	"companyName": "111",
	"qualificationNo": "512531248515",
	"socialNo": "111",
	"qualificationExpireDate": "2017-12-20"
}
```

##### 响应示例
```
{
    "status": 1,
    "data": "",
    "message": "用户注册成功！用户已存在了公司，根据从业资格证或身份证查询到已经存在人员，"
}
```
