# DescribeLiveStreamsNotifyUrlConfig {#doc_api_live_DescribeLiveStreamsNotifyUrlConfig .reference}

调用DescribeLiveStreamsNotifyUrlConfig查询推流回调配置。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=live&api=DescribeLiveStreamsNotifyUrlConfig&type=RPC&version=2016-11-01)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeLiveStreamsNotifyUrlConfig|系统规定参数。取值：**DescribeLiveStreamsNotifyUrlConfig**。

 |
|DomainName|String|是|www.yourdomain.com|您的加速域名。

 |
|RegionId|String|否|cn-shanghai|地域。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|RequestId|String|rtmp://play.aliyunlive.com/AppName/StreamName|请求ID。

 |
|LiveStreamsNotifyConfig| | |查询Notify配置。

 |
|DomainName|String|play.aliyunlive.com|您的加速域名

 |
|NotifyUrl|String|rtmp://play.aliyunlive.com/notify|回调地址。

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeLiveStreamsNotifyUrlConfig
&DomainName=www.yourdomain.com
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeLiveStreamsNotifyUrlConfigResponse>
	  <NotifyUrlConfig>
		    <DomainName>live.aliyunlive.com</DomainName>
		    <NotifyUrl>http://xxx.com/xx</NotifyUrl>
	  </NotifyUrlConfig>
	  <RequestId>4C747C97-7ECD-4C61-8A92-67AD806331FF</RequestId>
</DescribeLiveStreamsNotifyUrlConfigResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"NotifyUrlConfig":{
		"NotifyUrl":"http://xxx.com/xx",
		"DomainName":"live.aliyunlive.com"
	},
	"RequestId":"4C747C97-7ECD-4C61-8A92-67AD806331FF"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/live)查看更多错误码。

