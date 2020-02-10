# 查询Keystone API的版本信息<a name="zh-cn_topic_0057845569"></a>

## 功能介绍<a name="zh-cn_topic_0222037544_section1386945615526"></a>

该接口用于查询Keystone API的版本信息。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="zh-cn_topic_0222037544_section8874156115214"></a>

GET /

## 请求参数<a name="zh-cn_topic_0222037544_section78771656195216"></a>

无

## 响应参数<a name="zh-cn_topic_0222037544_section88824562529"></a>

**表 1**  响应Body参数

<a name="zh-cn_topic_0222037544_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037544_row3885145665210"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0222037544_p588755695217"><a name="zh-cn_topic_0222037544_p588755695217"></a><a name="zh-cn_topic_0222037544_p588755695217"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0222037544_p16888165685215"><a name="zh-cn_topic_0222037544_p16888165685215"></a><a name="zh-cn_topic_0222037544_p16888165685215"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0222037544_p1889065614527"><a name="zh-cn_topic_0222037544_p1889065614527"></a><a name="zh-cn_topic_0222037544_p1889065614527"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037544_row288565675216"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037544_p16891115618524"><a name="zh-cn_topic_0222037544_p16891115618524"></a><a name="zh-cn_topic_0222037544_p16891115618524"></a><a href="#zh-cn_topic_0222037544_response_Rs151Versions">versions</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037544_p208931556205219"><a name="zh-cn_topic_0222037544_p208931556205219"></a><a name="zh-cn_topic_0222037544_p208931556205219"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037544_p78951256195216"><a name="zh-cn_topic_0222037544_p78951256195216"></a><a name="zh-cn_topic_0222037544_p78951256195216"></a>Keystone API的版本信息。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  versions

<a name="zh-cn_topic_0222037544_response_Rs151Versions"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037544_row889675635213"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0222037544_p13898105620523"><a name="zh-cn_topic_0222037544_p13898105620523"></a><a name="zh-cn_topic_0222037544_p13898105620523"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0222037544_p490016565524"><a name="zh-cn_topic_0222037544_p490016565524"></a><a name="zh-cn_topic_0222037544_p490016565524"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0222037544_p1090145617527"><a name="zh-cn_topic_0222037544_p1090145617527"></a><a name="zh-cn_topic_0222037544_p1090145617527"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037544_row2896155615219"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037544_p1790317560526"><a name="zh-cn_topic_0222037544_p1790317560526"></a><a name="zh-cn_topic_0222037544_p1790317560526"></a><a href="#zh-cn_topic_0222037544_response_Rs151VersionsValuesArritem">values</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037544_p090510569524"><a name="zh-cn_topic_0222037544_p090510569524"></a><a name="zh-cn_topic_0222037544_p090510569524"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037544_p7907356135214"><a name="zh-cn_topic_0222037544_p7907356135214"></a><a name="zh-cn_topic_0222037544_p7907356135214"></a>Keystone API的版本信息列表。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  versions.values

<a name="zh-cn_topic_0222037544_response_Rs151VersionsValuesArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037544_row159083567521"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0222037544_p199101956125217"><a name="zh-cn_topic_0222037544_p199101956125217"></a><a name="zh-cn_topic_0222037544_p199101956125217"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0222037544_p199121856135210"><a name="zh-cn_topic_0222037544_p199121856135210"></a><a name="zh-cn_topic_0222037544_p199121856135210"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0222037544_p291312569522"><a name="zh-cn_topic_0222037544_p291312569522"></a><a name="zh-cn_topic_0222037544_p291312569522"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037544_row15908145695212"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037544_p49151856105215"><a name="zh-cn_topic_0222037544_p49151856105215"></a><a name="zh-cn_topic_0222037544_p49151856105215"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037544_p15916956185212"><a name="zh-cn_topic_0222037544_p15916956185212"></a><a name="zh-cn_topic_0222037544_p15916956185212"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037544_p7918135610522"><a name="zh-cn_topic_0222037544_p7918135610522"></a><a name="zh-cn_topic_0222037544_p7918135610522"></a>版本状态。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037544_row2908165610520"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037544_p20919165645210"><a name="zh-cn_topic_0222037544_p20919165645210"></a><a name="zh-cn_topic_0222037544_p20919165645210"></a>updated</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037544_p7921156115219"><a name="zh-cn_topic_0222037544_p7921156115219"></a><a name="zh-cn_topic_0222037544_p7921156115219"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037544_p692318566529"><a name="zh-cn_topic_0222037544_p692318566529"></a><a name="zh-cn_topic_0222037544_p692318566529"></a>最后更新时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037544_row1590895613523"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037544_p09243568525"><a name="zh-cn_topic_0222037544_p09243568525"></a><a name="zh-cn_topic_0222037544_p09243568525"></a><a href="#zh-cn_topic_0222037544_response_Rs151VersionsValuesArritemLinksArritem">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037544_p292675612525"><a name="zh-cn_topic_0222037544_p292675612525"></a><a name="zh-cn_topic_0222037544_p292675612525"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037544_p203481645153515"><a name="zh-cn_topic_0222037544_p203481645153515"></a><a name="zh-cn_topic_0222037544_p203481645153515"></a>版本的资源链接信息</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037544_row0908115645219"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037544_p393015565529"><a name="zh-cn_topic_0222037544_p393015565529"></a><a name="zh-cn_topic_0222037544_p393015565529"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037544_p1932956135213"><a name="zh-cn_topic_0222037544_p1932956135213"></a><a name="zh-cn_topic_0222037544_p1932956135213"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037544_p193475620529"><a name="zh-cn_topic_0222037544_p193475620529"></a><a name="zh-cn_topic_0222037544_p193475620529"></a>版本号，如v3.6。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037544_row1908195620521"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037544_p3935195695218"><a name="zh-cn_topic_0222037544_p3935195695218"></a><a name="zh-cn_topic_0222037544_p3935195695218"></a><a href="#zh-cn_topic_0222037544_response_Rs151VersionsValuesArritemMediatypesArritem">media-types</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037544_p16937155635212"><a name="zh-cn_topic_0222037544_p16937155635212"></a><a name="zh-cn_topic_0222037544_p16937155635212"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037544_p1892814568522"><a name="zh-cn_topic_0222037544_p1892814568522"></a><a name="zh-cn_topic_0222037544_p1892814568522"></a>支持的消息格式。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  versions.values.links

<a name="zh-cn_topic_0222037544_response_Rs151VersionsValuesArritemLinksArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037544_row189561356155211"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0222037544_p19958135665212"><a name="zh-cn_topic_0222037544_p19958135665212"></a><a name="zh-cn_topic_0222037544_p19958135665212"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0222037544_p1395985614524"><a name="zh-cn_topic_0222037544_p1395985614524"></a><a name="zh-cn_topic_0222037544_p1395985614524"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0222037544_p096015625218"><a name="zh-cn_topic_0222037544_p096015625218"></a><a name="zh-cn_topic_0222037544_p096015625218"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037544_row1195685615213"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037544_p1962105615218"><a name="zh-cn_topic_0222037544_p1962105615218"></a><a name="zh-cn_topic_0222037544_p1962105615218"></a>rel</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037544_p16963115675214"><a name="zh-cn_topic_0222037544_p16963115675214"></a><a name="zh-cn_topic_0222037544_p16963115675214"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037544_p896555618525"><a name="zh-cn_topic_0222037544_p896555618525"></a><a name="zh-cn_topic_0222037544_p896555618525"></a>链接类型。self：自助链接包含了版本链接的资源。bookmark：书签链接提供了一个永久资源的永久链接。alternate：备用链接包含了资源的替换表示形式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037544_row1295635685212"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037544_p19671556115212"><a name="zh-cn_topic_0222037544_p19671556115212"></a><a name="zh-cn_topic_0222037544_p19671556115212"></a>href</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037544_p8968856125210"><a name="zh-cn_topic_0222037544_p8968856125210"></a><a name="zh-cn_topic_0222037544_p8968856125210"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037544_p99701356175211"><a name="zh-cn_topic_0222037544_p99701356175211"></a><a name="zh-cn_topic_0222037544_p99701356175211"></a>资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  versions.values.media-types

<a name="zh-cn_topic_0222037544_response_Rs151VersionsValuesArritemMediatypesArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037544_row6940195625210"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0222037544_p15942125615212"><a name="zh-cn_topic_0222037544_p15942125615212"></a><a name="zh-cn_topic_0222037544_p15942125615212"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0222037544_p19944135615217"><a name="zh-cn_topic_0222037544_p19944135615217"></a><a name="zh-cn_topic_0222037544_p19944135615217"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0222037544_p18945135615525"><a name="zh-cn_topic_0222037544_p18945135615525"></a><a name="zh-cn_topic_0222037544_p18945135615525"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037544_row59401856145212"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037544_p10947145605217"><a name="zh-cn_topic_0222037544_p10947145605217"></a><a name="zh-cn_topic_0222037544_p10947145605217"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037544_p9949115635213"><a name="zh-cn_topic_0222037544_p9949115635213"></a><a name="zh-cn_topic_0222037544_p9949115635213"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037544_p29509567526"><a name="zh-cn_topic_0222037544_p29509567526"></a><a name="zh-cn_topic_0222037544_p29509567526"></a>媒体类型。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037544_row29401456125220"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0222037544_p14952256155211"><a name="zh-cn_topic_0222037544_p14952256155211"></a><a name="zh-cn_topic_0222037544_p14952256155211"></a>base</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0222037544_p2953105615215"><a name="zh-cn_topic_0222037544_p2953105615215"></a><a name="zh-cn_topic_0222037544_p2953105615215"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0222037544_p49551856185217"><a name="zh-cn_topic_0222037544_p49551856185217"></a><a name="zh-cn_topic_0222037544_p49551856185217"></a>基础类型。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0222037544_section1697185613528"></a>

```
GET https://iam.myhuaweicloud.com/
```

## 响应示例<a name="zh-cn_topic_0222037544_section297695645212"></a>

**状态码为 300 时:**

查询成功。（Multiple Choices）

```
{
    "versions": {
        "values": [
            {
                "media-types": [
                    {
                        "type": "application/vnd.openstack.identity-v3+json",
                        "base": "application/json"
                    }
                ],
                "links": [
                    {
                        "rel": "self",
                        "href": "https://iam.myhuaweicloud.com/v3/"
                    }
                ],
                "id": "v3.6",
                "updated": "2016-04-04T00:00:00Z",
                "status": "stable"
            }
        ]
    }
}
```

## 返回值<a name="zh-cn_topic_0222037544_section2014135765219"></a>

<a name="zh-cn_topic_0222037544_table329"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037544_row91635715214"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0222037544_p81855785210"><a name="zh-cn_topic_0222037544_p81855785210"></a><a name="zh-cn_topic_0222037544_p81855785210"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0222037544_p820165713524"><a name="zh-cn_topic_0222037544_p820165713524"></a><a name="zh-cn_topic_0222037544_p820165713524"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037544_row316757185217"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0222037544_p122145755215"><a name="zh-cn_topic_0222037544_p122145755215"></a><a name="zh-cn_topic_0222037544_p122145755215"></a>300</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037544_p523957155211"><a name="zh-cn_topic_0222037544_p523957155211"></a><a name="zh-cn_topic_0222037544_p523957155211"></a>查询成功。（Multiple Choices）</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037544_row3161457125220"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0222037544_p1124957175213"><a name="zh-cn_topic_0222037544_p1124957175213"></a><a name="zh-cn_topic_0222037544_p1124957175213"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037544_p826195785214"><a name="zh-cn_topic_0222037544_p826195785214"></a><a name="zh-cn_topic_0222037544_p826195785214"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037544_row171695735214"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0222037544_p1227105712522"><a name="zh-cn_topic_0222037544_p1227105712522"></a><a name="zh-cn_topic_0222037544_p1227105712522"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037544_p929125718529"><a name="zh-cn_topic_0222037544_p929125718529"></a><a name="zh-cn_topic_0222037544_p929125718529"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0222037544_row18161257165215"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0222037544_p730165785214"><a name="zh-cn_topic_0222037544_p730165785214"></a><a name="zh-cn_topic_0222037544_p730165785214"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037544_p9321857175213"><a name="zh-cn_topic_0222037544_p9321857175213"></a><a name="zh-cn_topic_0222037544_p9321857175213"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0222037544_section193495725216"></a>

无

