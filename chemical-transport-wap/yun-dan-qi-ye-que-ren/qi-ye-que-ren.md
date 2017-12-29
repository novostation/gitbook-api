#### 企业确认

##### 接口地址

```
/app/companyConfirm
```

##### 请求方式

POST

##### 接口描述

##### 签名算法	
(1) 把appid + 时间戳组成字符串；
(3) 将应用密钥appkey分别添加到以上请求参数串的头部和尾部：<secret><请求参数字符串><secret>；
(4) 对该字符串进行SHA1加密，得到一个二进制数组；
(5) 将该二进制数组转换为十六进制的大写字符串，该字符串即是这些请求参数对应的签名；
(6) 该签名值使用sign为参数名和其它请求参数一起发送服务端。
appid和appkey由平台分配，访问接口必须申请appid和appkey，通过验证后才可以使用。

依赖
``` xml
 <dependency>
      <groupId>commons-codec</groupId>
      <artifactId>commons-codec</artifactId>
      <version>1.4</version>
</dependency>
```

``` java
import org.apache.commons.codec.digest.DigestUtils;

public static String getSign(TreeMap<String,String> map, String appPwd) {
	StringBuffer sb=new StringBuffer();	
	sb.append(appPwd);
	for(Map.Entry<String,String> entry:map.entrySet()){
		sb.append(entry.getKey()).append(entry.getValue());
	}
	sb.append(appPwd);	
	String str=sb.toString();	
	return DigestUtils.shaHex(str).toUpperCase();
}
 
 
目前测试阶段约定参数
app.appkey=chemicalTransport
app.appid=myAppid

public static void main(String[] args){
	TreeMap<String, String> map = new TreeMap<String, String>();
	map.put("appid", "myAppid");
	map.put("reqtime","1442280038");//精确到毫秒
	map.put("data",data);
	getSign(map,"chemicalTransport");
}
```

##### 请求参数

格式：JSON

| 参数名 | 类型 | 描述 | 是否必填 |
| --- | --- | --- | --- |
| billNo | String | 运单号 | TRUE|
| billUnitId | Long | 运单收发货方id | TRUE|
| addressId| Long | 运单收发货方装卸货地址id | TRUE|
| addressType| Integer | 1: 发货、装货 2：收货、卸货 | TRUE|
| comfirmUserId| String| 确认人ID| TRUE |
| comfirmUserName| Integer | 确认人| TRUE |
| contactNo| Long | 确认人电话 | TRUE|
| latitude| Long | 维度 | TRUE|
| longitude| Long | 经度| TRUE|
| companyNo| String | 本企业危化品公司统一社会编号 | TRUE|
| companyName| String | 本企业危化品公司名称 | TRUE|
| chemicalList| JSONARRAY| 货物信息 |TRUE|
| id| Long | 货物ID |TRUE|
| checkWeight| Float| 企业确认重量 |TRUE|
| checkVolume| Float| 企业确认体积 |TRUE|
|data|json字符串|需要确认的数据|TRUE|

data属性解释参考《交投提供接口看后反馈@20171115.docx》

##### 响应参数

格式：JSON

| 参数名 | 类型 | 描述 |
| --- | --- | --- |
| code| Integer| 错误编码 |
| msg| String | 信息 |


| 错误编码 | 错误说明 |
| --- | --- |
| -1 | 系统繁忙，此时请开发者稍候再试 |
| 0 | 请求成功,OK |
| 1 | 服务不可用 |
| 2 | 编码错误 |
| 3 | 请求被禁止 |
| 4 | 服务已经作废 |
| 5 | 业务逻辑出错 |
| 6 | 缺少appid参数 |
| 7 | 缺少时间戳参数 |
| 8 | appid无效 |
| 9 | 缺少sign |
| 10 | 无效sign |
| 11 | 无效时间戳 |
| 12 | 用户调用服务的次数超限 |
| 13 | 会话调用服务的次数超限 |
| 14 | 应用调用服务的次数超限 |
| 15 | 应用调用服务的频率超限 |
| 101 | 自定义错误消息 |

##### 调用示例

``` json
url:/app/companyConfirm
参数：
{
	"reqtime": "1512013356516",
	"appid": "myAppid",
	"sign": "08B036C0D951AEA3355F035885F008F2F89453BC",
	"data": {
		"billNo": "20170331010755",
		"billUnitId": "13216555", // 收发货方id，扫二维码获取
		"addressId": "12345", //地址id，扫二维码获取
		"addressType": "1",	//1 :发货,2: 收货	
		"comfirmUserId": "23135654",//确认人ID
		"comfirmUserName": "张三",//确认人
		"contactNo": "13566266320",//确认人电话
		"latitude": "0.86",//维度：
		"longitude": "132.22",//经度：
		"companyNo": "1356654321312",//本企业危化品公司统一社会编号
		"companyName": "中石油公司",//本企业危化品公司名称
		"chemicalList": [{//确认货物列表
		//Id 为运单货物id，扫码获取（对应扫码信息中的id）
			"id": "1",
			"checkWeight": "110",
			"checkVolume": "9"
		},
		{
			"id": "2",
			"checkWeight": "10",
			"checkVolume": "19"
		}]
	}
}
```
ajax示例：
``` javascript
var appid = 'myAppid';
var reqtime = '1512372556490';

var data4 =[
{ "Id":2934, "checkWeight": "", "checkVolume": "0"}
];

var data={
"billNo": "20171203337804",
	"billUnitId": "3003",
	"addressId": "2994",
	"addressType": 1,
	"comfirmUserId": "jxdf002",
	"comfirmUserName": "jxdf002",
	"contactNo": "",
	"latitude": null,
	"longitude": null,
	"companyNo": "",
	"companyName": "中油碧辟石油有限公司南沙黄阁西加油站",	
'chemicalList': data4
};

var sign = '2A84382D20EB0EA5DAAF6BF25CA2EBA14A9BE379';
$.ajax({
url:'http://dtpt.gzajj.gov.cn:8080/chemical-transport-wap/app/companyConfirm',
async:false,
type:'post',
dataType:'JSON',
data:{"appid":appid,"reqtime":reqtime,"data":JSON.stringify(data),"sign":sign},
suseecss:function(result){
console.log(result);
}
});
```

后台生成代码
```
import org.apache.commons.codec.digest.DigestUtils;
import java.util.Map;
import java.util.TreeMap;

public class Test {

    public static void main(String[] args){
        TreeMap<String, String> map = new TreeMap<String, String>();
        map.put("appid", "myAppid");
        map.put("reqtime","1512372556490");
        map.put("data","{\"billNo\":\"20171203337804\",\"billUnitId\":\"3003\",\"addressId\":\"2994\",\"addressType\":1,\"comfirmUserId\":\"jxdf002\",\"comfirmUserName\":\"jxdf002\",\"contactNo\":\"\",\"latitude\":null,\"longitude\":null,\"companyNo\":\"\",\"companyName\":\"中油碧辟石油有限公司南沙黄阁西加油站\",\"chemicalList\":[{\"Id\":2934,\"checkWeight\":\"\",\"checkVolume\":\"0\"}]}");
        System.out.println(getSign(map,"chemicalTransport"));
    }

    public static String getSign(TreeMap<String,String> map, String appPwd) {
        StringBuffer sb=new StringBuffer();
        //应用密匙添加到请求参串的头部
        sb.append(appPwd);
        for(Map.Entry<String,String> entry:map.entrySet()){
            sb.append(entry.getKey()).append(entry.getValue());
        }
        sb.append(appPwd);
        //应用密匙添加到请求参串的尾部
        String str=sb.toString();
        //SHA1签名运算
        return DigestUtils.shaHex(str).toUpperCase();
    }

}
```
##### 响应示例
```
{
    "code": 0,
    "msg": "请求成功"
}
```
