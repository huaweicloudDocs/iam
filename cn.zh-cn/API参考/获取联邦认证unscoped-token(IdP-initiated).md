# 获取联邦认证unscoped token\(IdP initiated\)<a name="iam_02_0003"></a>

## 功能介绍<a name="zh-cn_topic_0224276696_section4257164314509"></a>

该接口可以用于通过IdP initiated的联邦认证方式获取unscoped token。

Unscoped token不能用来鉴权，若联邦用户需要使用token进行鉴权，请参考[获取联邦认证scoped token](获取联邦认证scoped-token.md)获取scoped token。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   该接口支持在命令行侧调用，需要客户端使用IdP initiated的联邦认证方式获取SAMLResponse，并采用浏览器提交表单数据的方式，获取unscoped token。  

## URI<a name="zh-cn_topic_0224276696_section6269643155017"></a>

POST /v3.0/OS-FEDERATION/tokens

## 请求参数<a name="zh-cn_topic_0224276696_section1327294365013"></a>

**表 1**  请求Header参数

<a name="zh-cn_topic_0224276696_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276696_row1727494319503"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276696_p627524325011"><a name="zh-cn_topic_0224276696_p627524325011"></a><a name="zh-cn_topic_0224276696_p627524325011"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276696_p42771243145020"><a name="zh-cn_topic_0224276696_p42771243145020"></a><a name="zh-cn_topic_0224276696_p42771243145020"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276696_p12781043125016"><a name="zh-cn_topic_0224276696_p12781043125016"></a><a name="zh-cn_topic_0224276696_p12781043125016"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276696_p1127994318502"><a name="zh-cn_topic_0224276696_p1127994318502"></a><a name="zh-cn_topic_0224276696_p1127994318502"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276696_row12274134316503"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276696_p628184335012"><a name="zh-cn_topic_0224276696_p628184335012"></a><a name="zh-cn_topic_0224276696_p628184335012"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276696_p728244313509"><a name="zh-cn_topic_0224276696_p728244313509"></a><a name="zh-cn_topic_0224276696_p728244313509"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276696_p1928314314508"><a name="zh-cn_topic_0224276696_p1928314314508"></a><a name="zh-cn_topic_0224276696_p1928314314508"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276696_p132847431501"><a name="zh-cn_topic_0224276696_p132847431501"></a><a name="zh-cn_topic_0224276696_p132847431501"></a>客户端必须使用浏览器提交表单数据的方式向服务端传SAMLResponse参数，故该字段需取值如下：application/x-www-form-urlencoded</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row20274124365019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276696_p328564365013"><a name="zh-cn_topic_0224276696_p328564365013"></a><a name="zh-cn_topic_0224276696_p328564365013"></a>X-Idp-Id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276696_p228618439504"><a name="zh-cn_topic_0224276696_p228618439504"></a><a name="zh-cn_topic_0224276696_p228618439504"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276696_p52871643195010"><a name="zh-cn_topic_0224276696_p52871643195010"></a><a name="zh-cn_topic_0224276696_p52871643195010"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276696_p11288943165010"><a name="zh-cn_topic_0224276696_p11288943165010"></a><a name="zh-cn_topic_0224276696_p11288943165010"></a>身份提供商ID。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  请求formData参数

<a name="zh-cn_topic_0224276696_table8973102018441"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276696_row3973192018442"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276696_p1497312084417"><a name="zh-cn_topic_0224276696_p1497312084417"></a><a name="zh-cn_topic_0224276696_p1497312084417"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276696_p8973122012449"><a name="zh-cn_topic_0224276696_p8973122012449"></a><a name="zh-cn_topic_0224276696_p8973122012449"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276696_p139731620194412"><a name="zh-cn_topic_0224276696_p139731620194412"></a><a name="zh-cn_topic_0224276696_p139731620194412"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276696_p1197315206445"><a name="zh-cn_topic_0224276696_p1197315206445"></a><a name="zh-cn_topic_0224276696_p1197315206445"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276696_row1497318207448"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276696_p1397314207442"><a name="zh-cn_topic_0224276696_p1397314207442"></a><a name="zh-cn_topic_0224276696_p1397314207442"></a>SAMLResponse</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276696_p119731120154416"><a name="zh-cn_topic_0224276696_p119731120154416"></a><a name="zh-cn_topic_0224276696_p119731120154416"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276696_p17973162019448"><a name="zh-cn_topic_0224276696_p17973162019448"></a><a name="zh-cn_topic_0224276696_p17973162019448"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276696_p1597352015446"><a name="zh-cn_topic_0224276696_p1597352015446"></a><a name="zh-cn_topic_0224276696_p1597352015446"></a>在IdP认证成功后返回的响应体。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0224276696_section429004315505"></a>

**表 3**  响应Header参数

<a name="zh-cn_topic_0224276696_ResponseHeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276696_row42921743155012"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276696_p1429315432502"><a name="zh-cn_topic_0224276696_p1429315432502"></a><a name="zh-cn_topic_0224276696_p1429315432502"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276696_p20294144310502"><a name="zh-cn_topic_0224276696_p20294144310502"></a><a name="zh-cn_topic_0224276696_p20294144310502"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276696_p12295124345016"><a name="zh-cn_topic_0224276696_p12295124345016"></a><a name="zh-cn_topic_0224276696_p12295124345016"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276696_row112926435505"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p0296943105010"><a name="zh-cn_topic_0224276696_p0296943105010"></a><a name="zh-cn_topic_0224276696_p0296943105010"></a>X-Subject-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p11298104375013"><a name="zh-cn_topic_0224276696_p11298104375013"></a><a name="zh-cn_topic_0224276696_p11298104375013"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p4299114355014"><a name="zh-cn_topic_0224276696_p4299114355014"></a><a name="zh-cn_topic_0224276696_p4299114355014"></a>签名后的unscoped token。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  响应Body参数

<a name="zh-cn_topic_0224276696_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276696_row1300104375010"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276696_p1230224311504"><a name="zh-cn_topic_0224276696_p1230224311504"></a><a name="zh-cn_topic_0224276696_p1230224311504"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276696_p16303104335013"><a name="zh-cn_topic_0224276696_p16303104335013"></a><a name="zh-cn_topic_0224276696_p16303104335013"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276696_p530415439506"><a name="zh-cn_topic_0224276696_p530415439506"></a><a name="zh-cn_topic_0224276696_p530415439506"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276696_row5300343145012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p1630513431501"><a name="zh-cn_topic_0224276696_p1630513431501"></a><a name="zh-cn_topic_0224276696_p1630513431501"></a><a href="#zh-cn_topic_0224276696_response_Rs1362Token">token</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p93065433508"><a name="zh-cn_topic_0224276696_p93065433508"></a><a name="zh-cn_topic_0224276696_p93065433508"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p5307144319502"><a name="zh-cn_topic_0224276696_p5307144319502"></a><a name="zh-cn_topic_0224276696_p5307144319502"></a>联邦认证的unscoped token信息。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  token

<a name="zh-cn_topic_0224276696_response_Rs1362Token"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276696_row19308114312502"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276696_p1310164345016"><a name="zh-cn_topic_0224276696_p1310164345016"></a><a name="zh-cn_topic_0224276696_p1310164345016"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276696_p33111443105011"><a name="zh-cn_topic_0224276696_p33111443105011"></a><a name="zh-cn_topic_0224276696_p33111443105011"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276696_p831218430507"><a name="zh-cn_topic_0224276696_p831218430507"></a><a name="zh-cn_topic_0224276696_p831218430507"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276696_row830884315502"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p103136430508"><a name="zh-cn_topic_0224276696_p103136430508"></a><a name="zh-cn_topic_0224276696_p103136430508"></a>issued_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p1314134325017"><a name="zh-cn_topic_0224276696_p1314134325017"></a><a name="zh-cn_topic_0224276696_p1314134325017"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p173151543155019"><a name="zh-cn_topic_0224276696_p173151543155019"></a><a name="zh-cn_topic_0224276696_p173151543155019"></a>token产生时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row8308943115018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p631624325013"><a name="zh-cn_topic_0224276696_p631624325013"></a><a name="zh-cn_topic_0224276696_p631624325013"></a>expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p1031774375018"><a name="zh-cn_topic_0224276696_p1031774375018"></a><a name="zh-cn_topic_0224276696_p1031774375018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p3318154345011"><a name="zh-cn_topic_0224276696_p3318154345011"></a><a name="zh-cn_topic_0224276696_p3318154345011"></a>token到期时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row9308164316500"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p1131994319507"><a name="zh-cn_topic_0224276696_p1131994319507"></a><a name="zh-cn_topic_0224276696_p1131994319507"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p1032004310509"><a name="zh-cn_topic_0224276696_p1032004310509"></a><a name="zh-cn_topic_0224276696_p1032004310509"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p1032174320507"><a name="zh-cn_topic_0224276696_p1032174320507"></a><a name="zh-cn_topic_0224276696_p1032174320507"></a>获取token的方式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row19308194365014"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p10322124395018"><a name="zh-cn_topic_0224276696_p10322124395018"></a><a name="zh-cn_topic_0224276696_p10322124395018"></a><a href="#zh-cn_topic_0224276696_response_Rs1362TokenUser">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p3323104315015"><a name="zh-cn_topic_0224276696_p3323104315015"></a><a name="zh-cn_topic_0224276696_p3323104315015"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p11325443145016"><a name="zh-cn_topic_0224276696_p11325443145016"></a><a name="zh-cn_topic_0224276696_p11325443145016"></a>获取token的用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  token.user

<a name="zh-cn_topic_0224276696_response_Rs1362TokenUser"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276696_row632611434506"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276696_p113281243115011"><a name="zh-cn_topic_0224276696_p113281243115011"></a><a name="zh-cn_topic_0224276696_p113281243115011"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276696_p14329243125019"><a name="zh-cn_topic_0224276696_p14329243125019"></a><a name="zh-cn_topic_0224276696_p14329243125019"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276696_p1733014335017"><a name="zh-cn_topic_0224276696_p1733014335017"></a><a name="zh-cn_topic_0224276696_p1733014335017"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276696_row3326643135014"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p1733194395011"><a name="zh-cn_topic_0224276696_p1733194395011"></a><a name="zh-cn_topic_0224276696_p1733194395011"></a><a href="#zh-cn_topic_0224276696_response_Rs1362TokenUserDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p633219437506"><a name="zh-cn_topic_0224276696_p633219437506"></a><a name="zh-cn_topic_0224276696_p633219437506"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p6333144385016"><a name="zh-cn_topic_0224276696_p6333144385016"></a><a name="zh-cn_topic_0224276696_p6333144385016"></a>用户所属账号信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row1332634325017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p33342433509"><a name="zh-cn_topic_0224276696_p33342433509"></a><a name="zh-cn_topic_0224276696_p33342433509"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p2335543165010"><a name="zh-cn_topic_0224276696_p2335543165010"></a><a name="zh-cn_topic_0224276696_p2335543165010"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p11336443105010"><a name="zh-cn_topic_0224276696_p11336443105010"></a><a name="zh-cn_topic_0224276696_p11336443105010"></a>用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row23265434501"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p1933710435501"><a name="zh-cn_topic_0224276696_p1933710435501"></a><a name="zh-cn_topic_0224276696_p1933710435501"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p1733814430508"><a name="zh-cn_topic_0224276696_p1733814430508"></a><a name="zh-cn_topic_0224276696_p1733814430508"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p10339114317507"><a name="zh-cn_topic_0224276696_p10339114317507"></a><a name="zh-cn_topic_0224276696_p10339114317507"></a>用户名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row15326124316501"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p153405435506"><a name="zh-cn_topic_0224276696_p153405435506"></a><a name="zh-cn_topic_0224276696_p153405435506"></a><a href="#zh-cn_topic_0224276696_response_Rs1362TokenUserOsfederation">OS-FEDERATION</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p13411843145010"><a name="zh-cn_topic_0224276696_p13411843145010"></a><a name="zh-cn_topic_0224276696_p13411843145010"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p834254315017"><a name="zh-cn_topic_0224276696_p834254315017"></a><a name="zh-cn_topic_0224276696_p834254315017"></a>联邦身份认证信息。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  token.user.domain

<a name="zh-cn_topic_0224276696_response_Rs1362TokenUserDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276696_row334444310505"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276696_p4345174310504"><a name="zh-cn_topic_0224276696_p4345174310504"></a><a name="zh-cn_topic_0224276696_p4345174310504"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276696_p3347114385015"><a name="zh-cn_topic_0224276696_p3347114385015"></a><a name="zh-cn_topic_0224276696_p3347114385015"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276696_p1348114335015"><a name="zh-cn_topic_0224276696_p1348114335015"></a><a name="zh-cn_topic_0224276696_p1348114335015"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276696_row123441143125018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p1034915438501"><a name="zh-cn_topic_0224276696_p1034915438501"></a><a name="zh-cn_topic_0224276696_p1034915438501"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p1935011431503"><a name="zh-cn_topic_0224276696_p1935011431503"></a><a name="zh-cn_topic_0224276696_p1935011431503"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p1535194385012"><a name="zh-cn_topic_0224276696_p1535194385012"></a><a name="zh-cn_topic_0224276696_p1535194385012"></a>用户所属账号名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row2344154318508"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p193531843165016"><a name="zh-cn_topic_0224276696_p193531843165016"></a><a name="zh-cn_topic_0224276696_p193531843165016"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p535414335011"><a name="zh-cn_topic_0224276696_p535414335011"></a><a name="zh-cn_topic_0224276696_p535414335011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p203558431509"><a name="zh-cn_topic_0224276696_p203558431509"></a><a name="zh-cn_topic_0224276696_p203558431509"></a>用户所属账号ID。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  token.user.OS-FEDERATION

<a name="zh-cn_topic_0224276696_response_Rs1362TokenUserOsfederation"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276696_row535634325011"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276696_p33571343155011"><a name="zh-cn_topic_0224276696_p33571343155011"></a><a name="zh-cn_topic_0224276696_p33571343155011"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276696_p335824310505"><a name="zh-cn_topic_0224276696_p335824310505"></a><a name="zh-cn_topic_0224276696_p335824310505"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276696_p113591243165016"><a name="zh-cn_topic_0224276696_p113591243165016"></a><a name="zh-cn_topic_0224276696_p113591243165016"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276696_row935684305010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p336194365014"><a name="zh-cn_topic_0224276696_p336194365014"></a><a name="zh-cn_topic_0224276696_p336194365014"></a><a href="#zh-cn_topic_0224276696_response_Rs1362TokenUserOsfederationGroupsArritem">groups</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p3362114345011"><a name="zh-cn_topic_0224276696_p3362114345011"></a><a name="zh-cn_topic_0224276696_p3362114345011"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p03634430502"><a name="zh-cn_topic_0224276696_p03634430502"></a><a name="zh-cn_topic_0224276696_p03634430502"></a>用户组信息列表。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row1435664345018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p15364194312502"><a name="zh-cn_topic_0224276696_p15364194312502"></a><a name="zh-cn_topic_0224276696_p15364194312502"></a><a href="#zh-cn_topic_0224276696_response_Rs1362TokenUserOsfederationIdentityprovider">identity_provider</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p53661743105019"><a name="zh-cn_topic_0224276696_p53661743105019"></a><a name="zh-cn_topic_0224276696_p53661743105019"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p336714315017"><a name="zh-cn_topic_0224276696_p336714315017"></a><a name="zh-cn_topic_0224276696_p336714315017"></a>身份提供商信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row1635614430502"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p103681243125012"><a name="zh-cn_topic_0224276696_p103681243125012"></a><a name="zh-cn_topic_0224276696_p103681243125012"></a><a href="#zh-cn_topic_0224276696_response_Rs1362TokenUserOsfederationProtocol">protocol</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p636910438504"><a name="zh-cn_topic_0224276696_p636910438504"></a><a name="zh-cn_topic_0224276696_p636910438504"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p837010432503"><a name="zh-cn_topic_0224276696_p837010432503"></a><a name="zh-cn_topic_0224276696_p837010432503"></a>协议信息。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  token.user.OS-FEDERATION.groups

<a name="zh-cn_topic_0224276696_response_Rs1362TokenUserOsfederationGroupsArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276696_row83711943175013"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276696_p16373124325011"><a name="zh-cn_topic_0224276696_p16373124325011"></a><a name="zh-cn_topic_0224276696_p16373124325011"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276696_p8374743105010"><a name="zh-cn_topic_0224276696_p8374743105010"></a><a name="zh-cn_topic_0224276696_p8374743105010"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276696_p43751543195015"><a name="zh-cn_topic_0224276696_p43751543195015"></a><a name="zh-cn_topic_0224276696_p43751543195015"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276696_row17371164318501"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p16376154313504"><a name="zh-cn_topic_0224276696_p16376154313504"></a><a name="zh-cn_topic_0224276696_p16376154313504"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p1837710433505"><a name="zh-cn_topic_0224276696_p1837710433505"></a><a name="zh-cn_topic_0224276696_p1837710433505"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p19378104335020"><a name="zh-cn_topic_0224276696_p19378104335020"></a><a name="zh-cn_topic_0224276696_p19378104335020"></a>用户组ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row10371443125012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p3379194312508"><a name="zh-cn_topic_0224276696_p3379194312508"></a><a name="zh-cn_topic_0224276696_p3379194312508"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p238094319503"><a name="zh-cn_topic_0224276696_p238094319503"></a><a name="zh-cn_topic_0224276696_p238094319503"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p12381164365018"><a name="zh-cn_topic_0224276696_p12381164365018"></a><a name="zh-cn_topic_0224276696_p12381164365018"></a>用户组名称。</p>
</td>
</tr>
</tbody>
</table>

**表 10**  token.user.OS-FEDERATION.identity\_provider

<a name="zh-cn_topic_0224276696_response_Rs1362TokenUserOsfederationIdentityprovider"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276696_row63821243165017"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276696_p0384144318509"><a name="zh-cn_topic_0224276696_p0384144318509"></a><a name="zh-cn_topic_0224276696_p0384144318509"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276696_p7385184335011"><a name="zh-cn_topic_0224276696_p7385184335011"></a><a name="zh-cn_topic_0224276696_p7385184335011"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276696_p123868435506"><a name="zh-cn_topic_0224276696_p123868435506"></a><a name="zh-cn_topic_0224276696_p123868435506"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276696_row83821843105011"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p1038710432508"><a name="zh-cn_topic_0224276696_p1038710432508"></a><a name="zh-cn_topic_0224276696_p1038710432508"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p1388843195013"><a name="zh-cn_topic_0224276696_p1388843195013"></a><a name="zh-cn_topic_0224276696_p1388843195013"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p9389154385012"><a name="zh-cn_topic_0224276696_p9389154385012"></a><a name="zh-cn_topic_0224276696_p9389154385012"></a>身份提供商ID。</p>
</td>
</tr>
</tbody>
</table>

**表 11**  token.user.OS-FEDERATION.protocol

<a name="zh-cn_topic_0224276696_response_Rs1362TokenUserOsfederationProtocol"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276696_row153903436505"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276696_p16392114355017"><a name="zh-cn_topic_0224276696_p16392114355017"></a><a name="zh-cn_topic_0224276696_p16392114355017"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276696_p17393114355010"><a name="zh-cn_topic_0224276696_p17393114355010"></a><a name="zh-cn_topic_0224276696_p17393114355010"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276696_p4394043125020"><a name="zh-cn_topic_0224276696_p4394043125020"></a><a name="zh-cn_topic_0224276696_p4394043125020"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276696_row43901043125015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276696_p2395174345010"><a name="zh-cn_topic_0224276696_p2395174345010"></a><a name="zh-cn_topic_0224276696_p2395174345010"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276696_p339644375012"><a name="zh-cn_topic_0224276696_p339644375012"></a><a name="zh-cn_topic_0224276696_p339644375012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276696_p1339764305013"><a name="zh-cn_topic_0224276696_p1339764305013"></a><a name="zh-cn_topic_0224276696_p1339764305013"></a>协议ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0224276696_section1639819432501"></a>

```
POST https://iam.myhuaweicloud.com/v3.0/OS-FEDERATION/tokens
```

```
SAMLResponse=PD94b...
```

## 响应示例<a name="zh-cn_topic_0224276696_section840114365010"></a>

**状态码为 201 时:**

创建成功。

```
响应Header参数：
X-Subject-Token:MIIatAYJKoZIhvcNAQcCoIIapTCCGqECAQExDTALB...
```

```
响应Body参数：
{
    "token": {
        "expires_at": "2020-02-13T14:21:34.042000Z",
        "methods": [
            "mapped"
        ],
        "issued_at": "2020-02-12T14:21:34.042000Z",
        "user": {
            "OS-FEDERATION": {
                "identity_provider": {
                    "id": "ACME"
                },
                "protocol": {
                    "id": "saml"
                },
                "groups": [
                    {
                        "id": "06aa22601502cec4a23ac0084a74038f",
                        "name": "admin"
                    }
                ]
            },
            "domain": {
                "name": "IAMDomain",
                "id": "06ba0970a097acc0f36c0086bb6cfe0"
            },
            "name": "FederationUser",
            "id": "LdUTYSC7zmJVIic3yaCbLBXDxPAdDxLg"
        }
    }
}
```

## 返回值<a name="zh-cn_topic_0224276696_section1543684395012"></a>

<a name="zh-cn_topic_0224276696_table4330"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276696_row24386435502"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0224276696_p20440114375012"><a name="zh-cn_topic_0224276696_p20440114375012"></a><a name="zh-cn_topic_0224276696_p20440114375012"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0224276696_p1844284317502"><a name="zh-cn_topic_0224276696_p1844284317502"></a><a name="zh-cn_topic_0224276696_p1844284317502"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276696_row1438243205012"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276696_p444319432500"><a name="zh-cn_topic_0224276696_p444319432500"></a><a name="zh-cn_topic_0224276696_p444319432500"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276696_p1944515435509"><a name="zh-cn_topic_0224276696_p1944515435509"></a><a name="zh-cn_topic_0224276696_p1944515435509"></a>创建成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row1743834395010"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276696_p174461043115019"><a name="zh-cn_topic_0224276696_p174461043115019"></a><a name="zh-cn_topic_0224276696_p174461043115019"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276696_p2447104315509"><a name="zh-cn_topic_0224276696_p2447104315509"></a><a name="zh-cn_topic_0224276696_p2447104315509"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row7438184315504"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276696_p34482431508"><a name="zh-cn_topic_0224276696_p34482431508"></a><a name="zh-cn_topic_0224276696_p34482431508"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276696_p1644920433507"><a name="zh-cn_topic_0224276696_p1644920433507"></a><a name="zh-cn_topic_0224276696_p1644920433507"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row4438144313508"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276696_p1745134318502"><a name="zh-cn_topic_0224276696_p1745134318502"></a><a name="zh-cn_topic_0224276696_p1745134318502"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276696_p445216439509"><a name="zh-cn_topic_0224276696_p445216439509"></a><a name="zh-cn_topic_0224276696_p445216439509"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row14381643185010"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276696_p2453124395012"><a name="zh-cn_topic_0224276696_p2453124395012"></a><a name="zh-cn_topic_0224276696_p2453124395012"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276696_p1345424335013"><a name="zh-cn_topic_0224276696_p1345424335013"></a><a name="zh-cn_topic_0224276696_p1345424335013"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row3439104315504"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276696_p1645594345016"><a name="zh-cn_topic_0224276696_p1645594345016"></a><a name="zh-cn_topic_0224276696_p1645594345016"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276696_p44561743105014"><a name="zh-cn_topic_0224276696_p44561743105014"></a><a name="zh-cn_topic_0224276696_p44561743105014"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row194394435505"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276696_p2457124318504"><a name="zh-cn_topic_0224276696_p2457124318504"></a><a name="zh-cn_topic_0224276696_p2457124318504"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276696_p8458104318503"><a name="zh-cn_topic_0224276696_p8458104318503"></a><a name="zh-cn_topic_0224276696_p8458104318503"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276696_row2439144395014"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276696_p846020439509"><a name="zh-cn_topic_0224276696_p846020439509"></a><a name="zh-cn_topic_0224276696_p846020439509"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276696_p1046154325011"><a name="zh-cn_topic_0224276696_p1046154325011"></a><a name="zh-cn_topic_0224276696_p1046154325011"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0224276696_section10463104365012"></a>

无

