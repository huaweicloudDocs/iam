# 查询Metadata文件<a name="iam_13_0502"></a>

## 功能介绍<a name="zh-cn_topic_0224276918_section745715165013"></a>

该接口可以用于<u>[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)</u><u></u>查询身份提供商导入到IAM中的Metadata文件。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section12629173181617"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=ShowMetadata)中调试该接口。

## URI<a name="zh-cn_topic_0224276918_section19463154503"></a>

GET /v3-ext/OS-FEDERATION/identity\_providers/\{idp\_id\}/protocols/\{protocol\_id\}/metadata

**表 1**  路径参数

<a name="zh-cn_topic_0224276918_table64720153502"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276918_row6473154503"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276918_p14471815125015"><a name="zh-cn_topic_0224276918_p14471815125015"></a><a name="zh-cn_topic_0224276918_p14471815125015"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276918_p24881512501"><a name="zh-cn_topic_0224276918_p24881512501"></a><a name="zh-cn_topic_0224276918_p24881512501"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276918_p174817150509"><a name="zh-cn_topic_0224276918_p174817150509"></a><a name="zh-cn_topic_0224276918_p174817150509"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276918_p84881516507"><a name="zh-cn_topic_0224276918_p84881516507"></a><a name="zh-cn_topic_0224276918_p84881516507"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276918_row154714159501"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276918_p148111513509"><a name="zh-cn_topic_0224276918_p148111513509"></a><a name="zh-cn_topic_0224276918_p148111513509"></a>idp_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276918_p1349215205012"><a name="zh-cn_topic_0224276918_p1349215205012"></a><a name="zh-cn_topic_0224276918_p1349215205012"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276918_p3492157507"><a name="zh-cn_topic_0224276918_p3492157507"></a><a name="zh-cn_topic_0224276918_p3492157507"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276985_p134475234912"><a name="zh-cn_topic_0224276985_p134475234912"></a><a name="zh-cn_topic_0224276985_p134475234912"></a>身份提供商名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row17471415165019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276918_p17507155502"><a name="zh-cn_topic_0224276918_p17507155502"></a><a name="zh-cn_topic_0224276918_p17507155502"></a>protocol_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276918_p1350201545010"><a name="zh-cn_topic_0224276918_p1350201545010"></a><a name="zh-cn_topic_0224276918_p1350201545010"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276918_p1550815185011"><a name="zh-cn_topic_0224276918_p1550815185011"></a><a name="zh-cn_topic_0224276918_p1550815185011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276918_p3512015195010"><a name="zh-cn_topic_0224276918_p3512015195010"></a><a name="zh-cn_topic_0224276918_p3512015195010"></a>协议ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0224276918_section10511315195020"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0224276918_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276918_row7512156509"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276918_p2052101520508"><a name="zh-cn_topic_0224276918_p2052101520508"></a><a name="zh-cn_topic_0224276918_p2052101520508"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276918_p11521315115010"><a name="zh-cn_topic_0224276918_p11521315115010"></a><a name="zh-cn_topic_0224276918_p11521315115010"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276918_p953315195016"><a name="zh-cn_topic_0224276918_p953315195016"></a><a name="zh-cn_topic_0224276918_p953315195016"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276918_p1053415155015"><a name="zh-cn_topic_0224276918_p1053415155015"></a><a name="zh-cn_topic_0224276918_p1053415155015"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276918_row151915155014"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276918_p15536153507"><a name="zh-cn_topic_0224276918_p15536153507"></a><a name="zh-cn_topic_0224276918_p15536153507"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276918_p4539156507"><a name="zh-cn_topic_0224276918_p4539156507"></a><a name="zh-cn_topic_0224276918_p4539156507"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276918_p35451519507"><a name="zh-cn_topic_0224276918_p35451519507"></a><a name="zh-cn_topic_0224276918_p35451519507"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276918_p154161519506"><a name="zh-cn_topic_0224276918_p154161519506"></a><a name="zh-cn_topic_0224276918_p154161519506"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row351111515508"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276918_p154161514501"><a name="zh-cn_topic_0224276918_p154161514501"></a><a name="zh-cn_topic_0224276918_p154161514501"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276918_p9543158502"><a name="zh-cn_topic_0224276918_p9543158502"></a><a name="zh-cn_topic_0224276918_p9543158502"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276918_p1254315125013"><a name="zh-cn_topic_0224276918_p1254315125013"></a><a name="zh-cn_topic_0224276918_p1254315125013"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p370593811019"><a name="p370593811019"></a><a name="p370593811019"></a>访问令牌，承载用户的身份、权限等信息。</p>
<p id="p170533831018"><a name="p170533831018"></a><a name="p170533831018"></a>token所需权限请参见<a href="授权项.md">授权项</a>。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0224276918_section75510157503"></a>

**表 3**  响应Body参数

<a name="zh-cn_topic_0224276918_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276918_row7551215145020"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276918_p356141565017"><a name="zh-cn_topic_0224276918_p356141565017"></a><a name="zh-cn_topic_0224276918_p356141565017"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276918_p1057121545012"><a name="zh-cn_topic_0224276918_p1057121545012"></a><a name="zh-cn_topic_0224276918_p1057121545012"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276918_p657715105015"><a name="zh-cn_topic_0224276918_p657715105015"></a><a name="zh-cn_topic_0224276918_p657715105015"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276918_row145511516509"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276918_p115713157503"><a name="zh-cn_topic_0224276918_p115713157503"></a><a name="zh-cn_topic_0224276918_p115713157503"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276918_p1157171514505"><a name="zh-cn_topic_0224276918_p1157171514505"></a><a name="zh-cn_topic_0224276918_p1157171514505"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276918_p258111519509"><a name="zh-cn_topic_0224276918_p258111519509"></a><a name="zh-cn_topic_0224276918_p258111519509"></a>Metadata的ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row5561015195019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276918_p1058815145012"><a name="zh-cn_topic_0224276918_p1058815145012"></a><a name="zh-cn_topic_0224276918_p1058815145012"></a>idp_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276918_p185831514505"><a name="zh-cn_topic_0224276918_p185831514505"></a><a name="zh-cn_topic_0224276918_p185831514505"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1973311093314"><a name="p1973311093314"></a><a name="p1973311093314"></a>身份提供商名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row956415155019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276918_p858161545014"><a name="zh-cn_topic_0224276918_p858161545014"></a><a name="zh-cn_topic_0224276918_p858161545014"></a>entity_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276918_p175981595017"><a name="zh-cn_topic_0224276918_p175981595017"></a><a name="zh-cn_topic_0224276918_p175981595017"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276918_p1159141555013"><a name="zh-cn_topic_0224276918_p1159141555013"></a><a name="zh-cn_topic_0224276918_p1159141555013"></a>Metadata文件中的entityID字段。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row1656191535019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276918_p155921525017"><a name="zh-cn_topic_0224276918_p155921525017"></a><a name="zh-cn_topic_0224276918_p155921525017"></a>protocol_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276918_p35915158509"><a name="zh-cn_topic_0224276918_p35915158509"></a><a name="zh-cn_topic_0224276918_p35915158509"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276918_p8591915175017"><a name="zh-cn_topic_0224276918_p8591915175017"></a><a name="zh-cn_topic_0224276918_p8591915175017"></a>协议ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row056111511503"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276918_p13601515165016"><a name="zh-cn_topic_0224276918_p13601515165016"></a><a name="zh-cn_topic_0224276918_p13601515165016"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276918_p46011518502"><a name="zh-cn_topic_0224276918_p46011518502"></a><a name="zh-cn_topic_0224276918_p46011518502"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276918_p460121585015"><a name="zh-cn_topic_0224276918_p460121585015"></a><a name="zh-cn_topic_0224276918_p460121585015"></a>用户所属帐号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row1056015145018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276918_p12609151505"><a name="zh-cn_topic_0224276918_p12609151505"></a><a name="zh-cn_topic_0224276918_p12609151505"></a>xaccount_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276918_p360191515501"><a name="zh-cn_topic_0224276918_p360191515501"></a><a name="zh-cn_topic_0224276918_p360191515501"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276918_p1061181525012"><a name="zh-cn_topic_0224276918_p1061181525012"></a><a name="zh-cn_topic_0224276918_p1061181525012"></a>帐号来源，默认为空。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row16560151502"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276918_p86181555011"><a name="zh-cn_topic_0224276918_p86181555011"></a><a name="zh-cn_topic_0224276918_p86181555011"></a>update_time</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276918_p1361915145011"><a name="zh-cn_topic_0224276918_p1361915145011"></a><a name="zh-cn_topic_0224276918_p1361915145011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276918_p176131535016"><a name="zh-cn_topic_0224276918_p176131535016"></a><a name="zh-cn_topic_0224276918_p176131535016"></a>导入或更新Metadata文件的时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row256201575019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276918_p4611515135010"><a name="zh-cn_topic_0224276918_p4611515135010"></a><a name="zh-cn_topic_0224276918_p4611515135010"></a>data</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276918_p1362171514507"><a name="zh-cn_topic_0224276918_p1362171514507"></a><a name="zh-cn_topic_0224276918_p1362171514507"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276918_p18621715115018"><a name="zh-cn_topic_0224276918_p18621715115018"></a><a name="zh-cn_topic_0224276918_p18621715115018"></a>Metadata文件的内容。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0224276918_section962201517505"></a>

```
GET https://iam.myhuaweicloud.com/v3-ext/OS-FEDERATION/identity_providers/{idp_id}/protocols/{protocol_id}/metadata
```

## 响应示例<a name="zh-cn_topic_0224276918_section15632153509"></a>

**状态码为 200 时:**

请求成功。

```
{
    "domain_id": "d78cbac186b744899480f25bd022f468",
    "update_time": "2020-02-12T13:26:25.000000",
    "data": "<md:EntityDescript...",
    "idp_id": "ACME",
    "protocol_id": "saml",
    "id": "11354739a6c940bc899fd9070ed1036d",
    "entity_id": "https://idp.test.com/idp/shibboleth",
    "xaccount_type": ""
}
```

## 返回值<a name="zh-cn_topic_0224276918_section966111575013"></a>

<a name="zh-cn_topic_0224276918_table4327"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276918_row106651545014"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0224276918_p1367171565013"><a name="zh-cn_topic_0224276918_p1367171565013"></a><a name="zh-cn_topic_0224276918_p1367171565013"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0224276918_p1967215195018"><a name="zh-cn_topic_0224276918_p1967215195018"></a><a name="zh-cn_topic_0224276918_p1967215195018"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276918_row1866121517504"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276918_p106781510502"><a name="zh-cn_topic_0224276918_p106781510502"></a><a name="zh-cn_topic_0224276918_p106781510502"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276918_p56761518504"><a name="zh-cn_topic_0224276918_p56761518504"></a><a name="zh-cn_topic_0224276918_p56761518504"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row8661615195016"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276918_p16861545016"><a name="zh-cn_topic_0224276918_p16861545016"></a><a name="zh-cn_topic_0224276918_p16861545016"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276918_p1868215135017"><a name="zh-cn_topic_0224276918_p1868215135017"></a><a name="zh-cn_topic_0224276918_p1868215135017"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row196611545015"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276918_p96851515020"><a name="zh-cn_topic_0224276918_p96851515020"></a><a name="zh-cn_topic_0224276918_p96851515020"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276918_p18684153501"><a name="zh-cn_topic_0224276918_p18684153501"></a><a name="zh-cn_topic_0224276918_p18684153501"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row16641525018"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276918_p16819153507"><a name="zh-cn_topic_0224276918_p16819153507"></a><a name="zh-cn_topic_0224276918_p16819153507"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276918_p76921512508"><a name="zh-cn_topic_0224276918_p76921512508"></a><a name="zh-cn_topic_0224276918_p76921512508"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276918_row106617152504"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276918_p186915156508"><a name="zh-cn_topic_0224276918_p186915156508"></a><a name="zh-cn_topic_0224276918_p186915156508"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276918_p13691515135019"><a name="zh-cn_topic_0224276918_p13691515135019"></a><a name="zh-cn_topic_0224276918_p13691515135019"></a>内部服务错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0224276918_section1569111565011"></a>

无

