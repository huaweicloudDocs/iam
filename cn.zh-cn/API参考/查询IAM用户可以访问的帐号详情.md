# 查询IAM用户可以访问的帐号详情<a name="iam_07_0001"></a>

## 功能介绍<a name="zh-cn_topic_0221482482_section4153183514019"></a>

该接口可以用于查询IAM用户可以访问的帐号详情。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section312117368587"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneListAuthDomains)中调试该接口。

## URI<a name="zh-cn_topic_0221482482_section415413359402"></a>

GET /v3/auth/domains

## 请求参数<a name="zh-cn_topic_0221482482_section7155435204020"></a>

**表 1**  请求Header参数

<a name="zh-cn_topic_0221482482_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482482_row16156835144016"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482482_p121571635194018"><a name="zh-cn_topic_0221482482_p121571635194018"></a><a name="zh-cn_topic_0221482482_p121571635194018"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482482_p1915783515408"><a name="zh-cn_topic_0221482482_p1915783515408"></a><a name="zh-cn_topic_0221482482_p1915783515408"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482482_p6158735104011"><a name="zh-cn_topic_0221482482_p6158735104011"></a><a name="zh-cn_topic_0221482482_p6158735104011"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482482_p3158535154012"><a name="zh-cn_topic_0221482482_p3158535154012"></a><a name="zh-cn_topic_0221482482_p3158535154012"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482482_row14156143513406"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482482_p1215814352401"><a name="zh-cn_topic_0221482482_p1215814352401"></a><a name="zh-cn_topic_0221482482_p1215814352401"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482482_p131590351404"><a name="zh-cn_topic_0221482482_p131590351404"></a><a name="zh-cn_topic_0221482482_p131590351404"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482482_p21596352408"><a name="zh-cn_topic_0221482482_p21596352408"></a><a name="zh-cn_topic_0221482482_p21596352408"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482482_p11607359404"><a name="zh-cn_topic_0221482482_p11607359404"></a><a name="zh-cn_topic_0221482482_p11607359404"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row13156635184016"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482482_p18160153534017"><a name="zh-cn_topic_0221482482_p18160153534017"></a><a name="zh-cn_topic_0221482482_p18160153534017"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482482_p3161133574011"><a name="zh-cn_topic_0221482482_p3161133574011"></a><a name="zh-cn_topic_0221482482_p3161133574011"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482482_p12161153584018"><a name="zh-cn_topic_0221482482_p12161153584018"></a><a name="zh-cn_topic_0221482482_p12161153584018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482482_p1416117353408"><a name="zh-cn_topic_0221482482_p1416117353408"></a><a name="zh-cn_topic_0221482482_p1416117353408"></a>IAM用户的token（无需特殊权限）。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482482_section61621835184013"></a>

**表 2**  响应Body参数

<a name="zh-cn_topic_0221482482_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482482_row9163335134015"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482482_p716493574011"><a name="zh-cn_topic_0221482482_p716493574011"></a><a name="zh-cn_topic_0221482482_p716493574011"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482482_p2164173518402"><a name="zh-cn_topic_0221482482_p2164173518402"></a><a name="zh-cn_topic_0221482482_p2164173518402"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482482_p10164103514012"><a name="zh-cn_topic_0221482482_p10164103514012"></a><a name="zh-cn_topic_0221482482_p10164103514012"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482482_row141631435154012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482482_p1116543514018"><a name="zh-cn_topic_0221482482_p1116543514018"></a><a name="zh-cn_topic_0221482482_p1116543514018"></a><a href="#zh-cn_topic_0221482482_response_Rs71DomainsArritem">domains</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482482_p616553534020"><a name="zh-cn_topic_0221482482_p616553534020"></a><a name="zh-cn_topic_0221482482_p616553534020"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482482_p17166113514402"><a name="zh-cn_topic_0221482482_p17166113514402"></a><a name="zh-cn_topic_0221482482_p17166113514402"></a>帐号信息列表。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row18163035124015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482482_p11669350403"><a name="zh-cn_topic_0221482482_p11669350403"></a><a name="zh-cn_topic_0221482482_p11669350403"></a><a href="#zh-cn_topic_0221482482_response_Rs71Links">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482482_p101671335124017"><a name="zh-cn_topic_0221482482_p101671335124017"></a><a name="zh-cn_topic_0221482482_p101671335124017"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482482_p116753514407"><a name="zh-cn_topic_0221482482_p116753514407"></a><a name="zh-cn_topic_0221482482_p116753514407"></a>资源链接信息。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  domains

<a name="zh-cn_topic_0221482482_response_Rs71DomainsArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482482_row101682353406"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482482_p1316919352402"><a name="zh-cn_topic_0221482482_p1316919352402"></a><a name="zh-cn_topic_0221482482_p1316919352402"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482482_p1416933504015"><a name="zh-cn_topic_0221482482_p1416933504015"></a><a name="zh-cn_topic_0221482482_p1416933504015"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482482_p1517043554017"><a name="zh-cn_topic_0221482482_p1517043554017"></a><a name="zh-cn_topic_0221482482_p1517043554017"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482482_row1116813359406"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482482_p617053510402"><a name="zh-cn_topic_0221482482_p617053510402"></a><a name="zh-cn_topic_0221482482_p617053510402"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482482_p617063517408"><a name="zh-cn_topic_0221482482_p617063517408"></a><a name="zh-cn_topic_0221482482_p617063517408"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482482_p1517119357403"><a name="zh-cn_topic_0221482482_p1517119357403"></a><a name="zh-cn_topic_0221482482_p1517119357403"></a>是否启用帐号，true为启用，false为停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row111687359407"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482482_p81711735114017"><a name="zh-cn_topic_0221482482_p81711735114017"></a><a name="zh-cn_topic_0221482482_p81711735114017"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482482_p717243518403"><a name="zh-cn_topic_0221482482_p717243518403"></a><a name="zh-cn_topic_0221482482_p717243518403"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482482_p1717213534012"><a name="zh-cn_topic_0221482482_p1717213534012"></a><a name="zh-cn_topic_0221482482_p1717213534012"></a>帐号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row316873513408"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482482_p1817320352402"><a name="zh-cn_topic_0221482482_p1817320352402"></a><a name="zh-cn_topic_0221482482_p1817320352402"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482482_p11731835164011"><a name="zh-cn_topic_0221482482_p11731835164011"></a><a name="zh-cn_topic_0221482482_p11731835164011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482482_p141731335194020"><a name="zh-cn_topic_0221482482_p141731335194020"></a><a name="zh-cn_topic_0221482482_p141731335194020"></a>帐号名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row8168435104018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482482_p017443584011"><a name="zh-cn_topic_0221482482_p017443584011"></a><a name="zh-cn_topic_0221482482_p017443584011"></a><a href="#zh-cn_topic_0221482482_response_Rs71DomainsArritemLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482482_p11741035144019"><a name="zh-cn_topic_0221482482_p11741035144019"></a><a name="zh-cn_topic_0221482482_p11741035144019"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482482_p1617563534010"><a name="zh-cn_topic_0221482482_p1617563534010"></a><a name="zh-cn_topic_0221482482_p1617563534010"></a>帐号的资源链接信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row1116843512408"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482482_p4175123554019"><a name="zh-cn_topic_0221482482_p4175123554019"></a><a name="zh-cn_topic_0221482482_p4175123554019"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482482_p1317643514403"><a name="zh-cn_topic_0221482482_p1317643514403"></a><a name="zh-cn_topic_0221482482_p1317643514403"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482482_p5176635114010"><a name="zh-cn_topic_0221482482_p5176635114010"></a><a name="zh-cn_topic_0221482482_p5176635114010"></a>帐号的描述信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  domains.links

<a name="zh-cn_topic_0221482482_response_Rs71DomainsArritemLinks"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482482_row14177163518403"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482482_p11177133544015"><a name="zh-cn_topic_0221482482_p11177133544015"></a><a name="zh-cn_topic_0221482482_p11177133544015"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482482_p2178335174016"><a name="zh-cn_topic_0221482482_p2178335174016"></a><a name="zh-cn_topic_0221482482_p2178335174016"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482482_p5178143512405"><a name="zh-cn_topic_0221482482_p5178143512405"></a><a name="zh-cn_topic_0221482482_p5178143512405"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482482_row4177113504012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482482_p517903520408"><a name="zh-cn_topic_0221482482_p517903520408"></a><a name="zh-cn_topic_0221482482_p517903520408"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482482_p1017993515404"><a name="zh-cn_topic_0221482482_p1017993515404"></a><a name="zh-cn_topic_0221482482_p1017993515404"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482482_p9179153584016"><a name="zh-cn_topic_0221482482_p9179153584016"></a><a name="zh-cn_topic_0221482482_p9179153584016"></a>资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  links

<a name="zh-cn_topic_0221482482_response_Rs71Links"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482482_row91801035154016"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482482_p10181535114014"><a name="zh-cn_topic_0221482482_p10181535114014"></a><a name="zh-cn_topic_0221482482_p10181535114014"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482482_p1618143544012"><a name="zh-cn_topic_0221482482_p1618143544012"></a><a name="zh-cn_topic_0221482482_p1618143544012"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482482_p818119352401"><a name="zh-cn_topic_0221482482_p818119352401"></a><a name="zh-cn_topic_0221482482_p818119352401"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482482_row818003514010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482482_p19182163513407"><a name="zh-cn_topic_0221482482_p19182163513407"></a><a name="zh-cn_topic_0221482482_p19182163513407"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482482_p41821435174018"><a name="zh-cn_topic_0221482482_p41821435174018"></a><a name="zh-cn_topic_0221482482_p41821435174018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482482_p13183133514401"><a name="zh-cn_topic_0221482482_p13183133514401"></a><a name="zh-cn_topic_0221482482_p13183133514401"></a>资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482482_section61831835134013"></a>

```
GET https://iam.myhuaweicloud.com/v3/auth/domains
```

## 响应示例<a name="zh-cn_topic_0221482482_section1184143574015"></a>

**状态码为 200 时:**

请求成功。

```
{
    "domains": [
        {
            "description": "",
            "enabled": true,
            "id": "d78cbac186b744899480f25bd022f468",
            "links": {
                "self": "https://iam.myhuaweicloud.com/v3/domains/d78cbac186b744899480f25bd022f468"
            },
            "name": "IAMDomain"
        }
    ],
    "links": {
        "self": "https://iam.myhuaweicloud.com/v3/auth/domains"
    }
}
```

## 返回值<a name="zh-cn_topic_0221482482_section13191635194014"></a>

<a name="zh-cn_topic_0221482482_table2438"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482482_row12192335174014"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482482_p419333515402"><a name="zh-cn_topic_0221482482_p419333515402"></a><a name="zh-cn_topic_0221482482_p419333515402"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482482_p151931835164018"><a name="zh-cn_topic_0221482482_p151931835164018"></a><a name="zh-cn_topic_0221482482_p151931835164018"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482482_row101921135174020"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482482_p16194133513408"><a name="zh-cn_topic_0221482482_p16194133513408"></a><a name="zh-cn_topic_0221482482_p16194133513408"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482482_p1019413544014"><a name="zh-cn_topic_0221482482_p1019413544014"></a><a name="zh-cn_topic_0221482482_p1019413544014"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row51921350404"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482482_p8195435174013"><a name="zh-cn_topic_0221482482_p8195435174013"></a><a name="zh-cn_topic_0221482482_p8195435174013"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482482_p819513514019"><a name="zh-cn_topic_0221482482_p819513514019"></a><a name="zh-cn_topic_0221482482_p819513514019"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row14192935104010"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482482_p11196135174015"><a name="zh-cn_topic_0221482482_p11196135174015"></a><a name="zh-cn_topic_0221482482_p11196135174015"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482482_p819614358401"><a name="zh-cn_topic_0221482482_p819614358401"></a><a name="zh-cn_topic_0221482482_p819614358401"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row131921535174010"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482482_p3196635114011"><a name="zh-cn_topic_0221482482_p3196635114011"></a><a name="zh-cn_topic_0221482482_p3196635114011"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482482_p16197173574015"><a name="zh-cn_topic_0221482482_p16197173574015"></a><a name="zh-cn_topic_0221482482_p16197173574015"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row13192113510402"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482482_p71971535164010"><a name="zh-cn_topic_0221482482_p71971535164010"></a><a name="zh-cn_topic_0221482482_p71971535164010"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482482_p71981735124019"><a name="zh-cn_topic_0221482482_p71981735124019"></a><a name="zh-cn_topic_0221482482_p71981735124019"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row121921235154015"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482482_p20198103516407"><a name="zh-cn_topic_0221482482_p20198103516407"></a><a name="zh-cn_topic_0221482482_p20198103516407"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482482_p2019973513402"><a name="zh-cn_topic_0221482482_p2019973513402"></a><a name="zh-cn_topic_0221482482_p2019973513402"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row1619223504016"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482482_p101991354401"><a name="zh-cn_topic_0221482482_p101991354401"></a><a name="zh-cn_topic_0221482482_p101991354401"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482482_p719914355402"><a name="zh-cn_topic_0221482482_p719914355402"></a><a name="zh-cn_topic_0221482482_p719914355402"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482482_row1219211359406"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482482_p112001435134012"><a name="zh-cn_topic_0221482482_p112001435134012"></a><a name="zh-cn_topic_0221482482_p112001435134012"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482482_p202001135174018"><a name="zh-cn_topic_0221482482_p202001135174018"></a><a name="zh-cn_topic_0221482482_p202001135174018"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482482_section10201143513403"></a>

无

