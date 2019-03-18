# DescribeLiveDomainLog {#reference_qsg_rkl_5fb .reference}

获取直播指定域名的原始访问日志的下载地址。

-   不指定StartTime和EndTime时，默认读取过去24小时的日志数据。
-   StartTime和EndTime需要同时指定。按指定的起止时间查询日志。

## 请求参数 {#section_ihn_ykl_5fb .section}

|参数|类型|是否必选|描述|
|:-|:-|:---|:-|
|Action|String|是|操作接口名，系统规定参数，取值：DescribeLiveDomainLog|
|DomainName|String|是|域名（只支持单个查询）。|
|StartTime|String|否|获取日志起始时间点。-   日期格式按照ISO8601表示法，并使用UTC时间。
-   例如：2016-10-20T04:00:00Z

|
|EndTime|String|否|结束时间需大于起始时间。-   起止时间和结束时间，间隔不超过一年。
-   获取日期格式按照ISO8601表示法，并使用UTC时间。
-   例如：2016-10-20T04:00:00Z

|
|PageSize|Long|否|分页大小。-   最大值：1000
-   取值范围：1~1000之前的任意整数。
-   默认值：300

|
|PageNumber|Long|否|取得第几页。取值范围：\>1的任意整数。

|

## 返回参数 {#section_sgb_jll_5fb .section}

|名称|类型|描述|
|:-|:-|:-|
|DomainLogDetails|DomainLogDetail|DomainLogDetail组成的数据|

数据类型DomainLogDetail

|数据|类型|描述|
|:-|:-|:-|
|LogCount|Long|本页返回的总条数|
|DomainName|String|域名|
|PageInfos|PageInfoDetail|PageInfoDetail组成的数据|
|LogInfos|LogInfoDetail|LogInfoDetail组成的数据|

数据类型PageInfoDetail

|名称|类型|描述|
|:-|:-|:-|
|PageIndex|Long|返回数据的页码|
|PageSize|Long|整页大小|
|Total|Long|总条数|

数据类型LogInfoDetail

|名称|类型|描述|
|:-|:-|:-|
|LogName|String|日志名称|
|LogPath|String|日志路径|
|StartTime|String|开始时间|
|EndTime|String|结束时间|
|LogSize|Long|日志大小|

## 示例 {#section_alh_kml_5fb .section}

请求示例

```
https://live.aliyuncs.com?Action=DescribeLiveDomainLog&DomainName=example.com&<公共请求参数>
```

返回示例

```
{
    "RequestId": "077D0284-F041-4A41-A932-B48377FDAA25",
    "DomainLogDetails": {
        "DomainLogDetail": [
            {
                "LogInfos": {
                    "LogInfoDetail": [
                        {
                            "LogName": "example.com_2018_03_25_180000_190000.gz",
                            "LogPath": "livelog2.aliyuncs.com/example.com/2018_03_25/example.com_2018_03_25_180000_190000.gz?Expires=1522659931&OSSAccessKeyId=exampleLTAIstjGueo4ZEuA&Signature=suZFyJHoD3RzZqK%2Bcu6P4VaNAVI%3D",
                            "EndTime": "1521975600",
                            "StartTime": "1521972000",
                            "LogSize": 2645401
                        },
                        {
                            "LogName": "example.com_2018_03_25_190000_200000.gz",
                            "LogPath": "livelog2.aliyuncs.com/example.com/2018_03_25/example.com_2018_03_25_190000_200000.gz?Expires=1522659931&OSSAccessKeyId=example&Signature=C01p%2BtA%2BfLywKP9Sru2Oxwy7Do0%3D",
                            "EndTime": "1521979200",
                            "StartTime": "1521975600",
                            "LogSize": 2653965
                        }
                    ]
                },
                "LogCount": 20,
                "PageInfos": {
                    "PageNumber": 1,
                    "PageSize": 20,
                    "Total": 20
                },
                "DomainName": "example.com"
            }
        ]
    }
}
```

