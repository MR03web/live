# DescribeLiveCertificateDetail {#doc_api_live_DescribeLiveCertificateDetail .reference}

调用DescribeLiveCertificateDetail获取证书详细信息。

## 调试 {#api_explorer .section}

[您可以在OpenAPI Explorer中直接运行该接口，免去您计算签名的困扰。运行成功后，OpenAPI Explorer可以自动生成SDK代码示例。](https://api.aliyun.com/#product=live&api=DescribeLiveCertificateDetail&type=RPC&version=2016-11-01)

## 请求参数 {#parameters .section}

|名称|类型|是否必选|示例值|描述|
|--|--|----|---|--|
|Action|String|是|DescribeLiveCertificateDetail|系统规定参数，取值：**DescribeLiveCertificateDetail**。

 |
|CertName|String|是|certname|证书名称。

 |

## 返回数据 {#resultMapping .section}

|名称|类型|示例值|描述|
|--|--|---|--|
|Cert|String|-----BEGIN CERTIFICATE-----xxx-----END CERTIFICATE-----|证书内容

 |
|CertId|Long|23456234|证书ID

 |
|CertName|String|证书名称|证书名称

 |
|Key|String|XXX|证书秘钥

 |
|RequestId|String|C7C69682-7F88-40DD-A198-10D0309E439B|请求ID

 |

## 示例 {#demo .section}

请求示例

``` {#request_demo}

http(s)://[Endpoint]/?Action=DescribeLiveCertificateDetail
&CertName=certname
&<公共请求参数>

```

正常返回示例

`XML` 格式

``` {#xml_return_success_demo}
<DescribeLiveCertificateDetailResponse>
	  <CertId>xxx</CertId>
	  <RequestId>C7C69682-7F88-40DD-A198-10D0309E439B</RequestId>
	  <CertName>证书名称</CertName>
	  <Cert>-----BEGIN CERTIFICATE-----xxx-----END CERTIFICATE-----</Cert>
</DescribeLiveCertificateDetailResponse>
```

`JSON` 格式

``` {#json_return_success_demo}
{
	"CertId":"xxx",
	"RequestId":"C7C69682-7F88-40DD-A198-10D0309E439B",
	"CertName":"证书名称",
	"Cert":"-----BEGIN CERTIFICATE-----xxx-----END CERTIFICATE-----"
}
```

## 错误码 { .section}

访问[错误中心](https://error-center.aliyun.com/status/product/live)查看更多错误码。

