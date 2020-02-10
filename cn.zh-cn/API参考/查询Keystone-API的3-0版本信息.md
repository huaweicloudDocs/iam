# 查询Keystone API的3.0版本信息<a name="zh-cn_topic_0057845613"></a>

## 功能介绍<a name="zh-cn_topic_0222037460_section117695785215"></a>

该接口用于查询Keystone API的3.0版本的信息。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="zh-cn_topic_0222037460_section6822572529"></a>

GET /v3

## 请求参数<a name="zh-cn_topic_0222037460_section16863574524"></a>

无

## 响应参数<a name="zh-cn_topic_0222037460_section790175714522"></a>

**表 1**  响应Body参数

<a name="zh-cn_topic_0222037460_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037460_row129214572520"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0222037460_p149325710528"><a name="zh-cn_topic_0222037460_p149325710528"></a><a name="zh-cn_topic_0222037460_p149325710528"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0222037460_p795115745213"><a name="zh-cn_topic_0222037460_p795115745213"></a><a name="zh-cn_topic_0222037460_p795115745213"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0222037460_p159645765217"><a name="zh-cn_topic_0222037460_p159645765217"></a><a name="zh-cn_topic_0222037460_p159645765217"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037460_row1492115720527"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037460_p1798657165212"><a name="zh-cn_topic_0222037460_p1798657165212"></a><a name="zh-cn_topic_0222037460_p1798657165212"></a><a href="#zh-cn_topic_0222037460_response_Rs152Version">version</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037460_p13991571528"><a name="zh-cn_topic_0222037460_p13991571528"></a><a name="zh-cn_topic_0222037460_p13991571528"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037460_p1710235715522"><a name="zh-cn_topic_0222037460_p1710235715522"></a><a name="zh-cn_topic_0222037460_p1710235715522"></a>Keystone API的3.0版本信息。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  version

<a name="zh-cn_topic_0222037460_response_Rs152Version"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037460_row13103185714526"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0222037460_p19105135795218"><a name="zh-cn_topic_0222037460_p19105135795218"></a><a name="zh-cn_topic_0222037460_p19105135795218"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0222037460_p1410715578521"><a name="zh-cn_topic_0222037460_p1410715578521"></a><a name="zh-cn_topic_0222037460_p1410715578521"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0222037460_p131081578521"><a name="zh-cn_topic_0222037460_p131081578521"></a><a name="zh-cn_topic_0222037460_p131081578521"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037460_row9103457195218"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037460_p101091957125219"><a name="zh-cn_topic_0222037460_p101091957125219"></a><a name="zh-cn_topic_0222037460_p101091957125219"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037460_p12111125717529"><a name="zh-cn_topic_0222037460_p12111125717529"></a><a name="zh-cn_topic_0222037460_p12111125717529"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037460_p18113165715525"><a name="zh-cn_topic_0222037460_p18113165715525"></a><a name="zh-cn_topic_0222037460_p18113165715525"></a>版本状态。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037460_row8103857165214"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037460_p141151357205216"><a name="zh-cn_topic_0222037460_p141151357205216"></a><a name="zh-cn_topic_0222037460_p141151357205216"></a>updated</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037460_p191172057185218"><a name="zh-cn_topic_0222037460_p191172057185218"></a><a name="zh-cn_topic_0222037460_p191172057185218"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037460_p1211815577528"><a name="zh-cn_topic_0222037460_p1211815577528"></a><a name="zh-cn_topic_0222037460_p1211815577528"></a>最后更新时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037460_row6103157145216"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037460_p17120657165212"><a name="zh-cn_topic_0222037460_p17120657165212"></a><a name="zh-cn_topic_0222037460_p17120657165212"></a><a href="#zh-cn_topic_0222037460_response_Rs152VersionLinksArritem">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037460_p812215716527"><a name="zh-cn_topic_0222037460_p812215716527"></a><a name="zh-cn_topic_0222037460_p812215716527"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037460_p17124857185213"><a name="zh-cn_topic_0222037460_p17124857185213"></a><a name="zh-cn_topic_0222037460_p17124857185213"></a>版本的资源链接信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037460_row210312575522"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037460_p14125125711527"><a name="zh-cn_topic_0222037460_p14125125711527"></a><a name="zh-cn_topic_0222037460_p14125125711527"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037460_p11127257135215"><a name="zh-cn_topic_0222037460_p11127257135215"></a><a name="zh-cn_topic_0222037460_p11127257135215"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037460_p2129125716526"><a name="zh-cn_topic_0222037460_p2129125716526"></a><a name="zh-cn_topic_0222037460_p2129125716526"></a>版本号，如v3.6。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037460_row19103157195219"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037460_p19130357115215"><a name="zh-cn_topic_0222037460_p19130357115215"></a><a name="zh-cn_topic_0222037460_p19130357115215"></a><a href="#zh-cn_topic_0222037460_response_Rs152VersionMediatypesArritem">media-types</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037460_p181331457205210"><a name="zh-cn_topic_0222037460_p181331457205210"></a><a name="zh-cn_topic_0222037460_p181331457205210"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037460_p1413415775210"><a name="zh-cn_topic_0222037460_p1413415775210"></a><a name="zh-cn_topic_0222037460_p1413415775210"></a>支持的消息格式。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  version.links

<a name="zh-cn_topic_0222037460_response_Rs152VersionLinksArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037460_row17151145716525"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0222037460_p1415335713525"><a name="zh-cn_topic_0222037460_p1415335713525"></a><a name="zh-cn_topic_0222037460_p1415335713525"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0222037460_p01542578521"><a name="zh-cn_topic_0222037460_p01542578521"></a><a name="zh-cn_topic_0222037460_p01542578521"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0222037460_p215655725214"><a name="zh-cn_topic_0222037460_p215655725214"></a><a name="zh-cn_topic_0222037460_p215655725214"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037460_row415118575523"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037460_p9157185785214"><a name="zh-cn_topic_0222037460_p9157185785214"></a><a name="zh-cn_topic_0222037460_p9157185785214"></a>rel</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037460_p61595575529"><a name="zh-cn_topic_0222037460_p61595575529"></a><a name="zh-cn_topic_0222037460_p61595575529"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037460_p1816145795219"><a name="zh-cn_topic_0222037460_p1816145795219"></a><a name="zh-cn_topic_0222037460_p1816145795219"></a>链接类型。self：自助链接包含了版本链接的资源。bookmark：书签链接提供了一个永久资源的永久链接。alternate：备用链接包含了资源的替换表示形式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037460_row2151957135217"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037460_p1716275735218"><a name="zh-cn_topic_0222037460_p1716275735218"></a><a name="zh-cn_topic_0222037460_p1716275735218"></a>href</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037460_p131641857135214"><a name="zh-cn_topic_0222037460_p131641857135214"></a><a name="zh-cn_topic_0222037460_p131641857135214"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037460_p016519579528"><a name="zh-cn_topic_0222037460_p016519579528"></a><a name="zh-cn_topic_0222037460_p016519579528"></a>资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  version.media-types

<a name="zh-cn_topic_0222037460_response_Rs152VersionMediatypesArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037460_row21361957155218"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0222037460_p51371057165211"><a name="zh-cn_topic_0222037460_p51371057165211"></a><a name="zh-cn_topic_0222037460_p51371057165211"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0222037460_p413955765211"><a name="zh-cn_topic_0222037460_p413955765211"></a><a name="zh-cn_topic_0222037460_p413955765211"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0222037460_p15140657155210"><a name="zh-cn_topic_0222037460_p15140657155210"></a><a name="zh-cn_topic_0222037460_p15140657155210"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037460_row1813625795218"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037460_p15142155725214"><a name="zh-cn_topic_0222037460_p15142155725214"></a><a name="zh-cn_topic_0222037460_p15142155725214"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037460_p4143135718528"><a name="zh-cn_topic_0222037460_p4143135718528"></a><a name="zh-cn_topic_0222037460_p4143135718528"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037460_p6145195775216"><a name="zh-cn_topic_0222037460_p6145195775216"></a><a name="zh-cn_topic_0222037460_p6145195775216"></a>媒体类型。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037460_row1513612570528"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037460_p14146205785213"><a name="zh-cn_topic_0222037460_p14146205785213"></a><a name="zh-cn_topic_0222037460_p14146205785213"></a>base</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037460_p111483576524"><a name="zh-cn_topic_0222037460_p111483576524"></a><a name="zh-cn_topic_0222037460_p111483576524"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037460_p215012579528"><a name="zh-cn_topic_0222037460_p215012579528"></a><a name="zh-cn_topic_0222037460_p215012579528"></a>基础类型。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0222037460_section17166155717525"></a>

```
GET https://iam.myhuaweicloud.com/v3
```

## 响应示例<a name="zh-cn_topic_0222037460_section1517195710521"></a>

**状态码为 200 时:**

请求成功。

```
{
    "version": {
        "status": "stable",
        "updated": "2016-04-04T00:00:00Z",
        "media-types": [
            {
                "base": "application/json",
                "type": "application/vnd.openstack.identity-v3+json"
            }
        ],
        "id": "v3.6",
        "links": [
            {
                "href": "https://www.example.com/v3/",
                "rel": "self"
            }
        ]
    }
}
```

## 返回值<a name="zh-cn_topic_0222037460_section1520325735212"></a>

<a name="zh-cn_topic_0222037460_table330"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037460_row82041457175213"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0222037460_p5206957175215"><a name="zh-cn_topic_0222037460_p5206957175215"></a><a name="zh-cn_topic_0222037460_p5206957175215"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0222037460_p1620735719529"><a name="zh-cn_topic_0222037460_p1620735719529"></a><a name="zh-cn_topic_0222037460_p1620735719529"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037460_row17204957135211"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0222037460_p192092574524"><a name="zh-cn_topic_0222037460_p192092574524"></a><a name="zh-cn_topic_0222037460_p192092574524"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037460_p9211125716527"><a name="zh-cn_topic_0222037460_p9211125716527"></a><a name="zh-cn_topic_0222037460_p9211125716527"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037460_row14204155716526"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0222037460_p221255719521"><a name="zh-cn_topic_0222037460_p221255719521"></a><a name="zh-cn_topic_0222037460_p221255719521"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037460_p172143571528"><a name="zh-cn_topic_0222037460_p172143571528"></a><a name="zh-cn_topic_0222037460_p172143571528"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037460_row13204205711526"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0222037460_p8215105765211"><a name="zh-cn_topic_0222037460_p8215105765211"></a><a name="zh-cn_topic_0222037460_p8215105765211"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037460_p2021765710528"><a name="zh-cn_topic_0222037460_p2021765710528"></a><a name="zh-cn_topic_0222037460_p2021765710528"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037460_row2020415712525"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0222037460_p42181457125212"><a name="zh-cn_topic_0222037460_p42181457125212"></a><a name="zh-cn_topic_0222037460_p42181457125212"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037460_p1122020576524"><a name="zh-cn_topic_0222037460_p1122020576524"></a><a name="zh-cn_topic_0222037460_p1122020576524"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0222037460_section1322105765214"></a>

无

