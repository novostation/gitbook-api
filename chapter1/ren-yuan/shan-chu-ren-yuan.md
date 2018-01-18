#### 更新人员

##### 接口地址

```
/app/bsEmployee/delete/{employeeId}
```

##### 请求方式

POST

##### 接口描述

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| employeeId| Long| 人员ID |TRUE|

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| status| Integer | 状态：1：成功；0：失败 |
| message| String | 响应消息 |
| data| JSON字符串| 响应数据 |

##### 调用示例

```
url:/app/bsEmployee/delete/1
```



##### 响应示例

```
{
    "status": 1,
    "data":"",
    "message": "删除数据成功"
}
```

