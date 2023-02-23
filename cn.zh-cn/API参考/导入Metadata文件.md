# 导入Metadata文件<a name="iam_13_0504"></a>

## 功能介绍<a name="zh-cn_topic_0224276912_section14111103315508"></a>

该接口可以用于<u>[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)</u><u></u>导入Metadata文件。

帐号在使用联邦认证功能前，需要先将Metadata文件导入到IAM中。Metadata文件是SAML 2.0协议约定的接口文件，包含访问接口地址和证书信息，请找企业管理员获取企业IdP的Metadata文件。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section139581617181619"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=CreateMetadata)中调试该接口。

## URI<a name="zh-cn_topic_0224276912_section131141933175011"></a>

POST /v3-ext/OS-FEDERATION/identity\_providers/\{idp\_id\}/protocols/\{protocol\_id\}/metadata

**表 1**  路径参数

<a name="zh-cn_topic_0224276912_table18116183317501"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276912_row4115203315017"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276912_p711716336503"><a name="zh-cn_topic_0224276912_p711716336503"></a><a name="zh-cn_topic_0224276912_p711716336503"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276912_p211711334504"><a name="zh-cn_topic_0224276912_p211711334504"></a><a name="zh-cn_topic_0224276912_p211711334504"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276912_p1911853318506"><a name="zh-cn_topic_0224276912_p1911853318506"></a><a name="zh-cn_topic_0224276912_p1911853318506"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276912_p41185332509"><a name="zh-cn_topic_0224276912_p41185332509"></a><a name="zh-cn_topic_0224276912_p41185332509"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276912_row21164336509"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276912_p1111943320506"><a name="zh-cn_topic_0224276912_p1111943320506"></a><a name="zh-cn_topic_0224276912_p1111943320506"></a>idp_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276912_p61191533165016"><a name="zh-cn_topic_0224276912_p61191533165016"></a><a name="zh-cn_topic_0224276912_p61191533165016"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276912_p181205338509"><a name="zh-cn_topic_0224276912_p181205338509"></a><a name="zh-cn_topic_0224276912_p181205338509"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276985_p134475234912"><a name="zh-cn_topic_0224276985_p134475234912"></a><a name="zh-cn_topic_0224276985_p134475234912"></a>身份提供商名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276912_row14116033155019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276912_p4121933175016"><a name="zh-cn_topic_0224276912_p4121933175016"></a><a name="zh-cn_topic_0224276912_p4121933175016"></a>protocol_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276912_p2122193335019"><a name="zh-cn_topic_0224276912_p2122193335019"></a><a name="zh-cn_topic_0224276912_p2122193335019"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276912_p16122433105010"><a name="zh-cn_topic_0224276912_p16122433105010"></a><a name="zh-cn_topic_0224276912_p16122433105010"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276912_p111231733135018"><a name="zh-cn_topic_0224276912_p111231733135018"></a><a name="zh-cn_topic_0224276912_p111231733135018"></a>协议ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0224276912_section4123633115014"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0224276912_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276912_row1512473312509"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276912_p91256334504"><a name="zh-cn_topic_0224276912_p91256334504"></a><a name="zh-cn_topic_0224276912_p91256334504"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276912_p412633385019"><a name="zh-cn_topic_0224276912_p412633385019"></a><a name="zh-cn_topic_0224276912_p412633385019"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276912_p312633316506"><a name="zh-cn_topic_0224276912_p312633316506"></a><a name="zh-cn_topic_0224276912_p312633316506"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276912_p1127833115019"><a name="zh-cn_topic_0224276912_p1127833115019"></a><a name="zh-cn_topic_0224276912_p1127833115019"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276912_row512493385016"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276912_p912717335505"><a name="zh-cn_topic_0224276912_p912717335505"></a><a name="zh-cn_topic_0224276912_p912717335505"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276912_p31281033135012"><a name="zh-cn_topic_0224276912_p31281033135012"></a><a name="zh-cn_topic_0224276912_p31281033135012"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276912_p15129163375014"><a name="zh-cn_topic_0224276912_p15129163375014"></a><a name="zh-cn_topic_0224276912_p15129163375014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276912_p11291633125014"><a name="zh-cn_topic_0224276912_p11291633125014"></a><a name="zh-cn_topic_0224276912_p11291633125014"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276912_row3124163355017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276912_p2013013385020"><a name="zh-cn_topic_0224276912_p2013013385020"></a><a name="zh-cn_topic_0224276912_p2013013385020"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276912_p10130123385014"><a name="zh-cn_topic_0224276912_p10130123385014"></a><a name="zh-cn_topic_0224276912_p10130123385014"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276912_p513133355016"><a name="zh-cn_topic_0224276912_p513133355016"></a><a name="zh-cn_topic_0224276912_p513133355016"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1660104731011"><a name="p1660104731011"></a><a name="p1660104731011"></a>访问令牌，承载用户的身份、权限等信息。</p>
<p id="p1560347141016"><a name="p1560347141016"></a><a name="p1560347141016"></a>token所需权限请参见<a href="授权项.md">授权项</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="zh-cn_topic_0224276912_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276912_row15132173320506"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276912_p41331833145016"><a name="zh-cn_topic_0224276912_p41331833145016"></a><a name="zh-cn_topic_0224276912_p41331833145016"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276912_p2134143317504"><a name="zh-cn_topic_0224276912_p2134143317504"></a><a name="zh-cn_topic_0224276912_p2134143317504"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276912_p13134103312505"><a name="zh-cn_topic_0224276912_p13134103312505"></a><a name="zh-cn_topic_0224276912_p13134103312505"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276912_p171351833195017"><a name="zh-cn_topic_0224276912_p171351833195017"></a><a name="zh-cn_topic_0224276912_p171351833195017"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276912_row31329336500"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276912_p2135153318503"><a name="zh-cn_topic_0224276912_p2135153318503"></a><a name="zh-cn_topic_0224276912_p2135153318503"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276912_p181361433155018"><a name="zh-cn_topic_0224276912_p181361433155018"></a><a name="zh-cn_topic_0224276912_p181361433155018"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276912_p16137163320505"><a name="zh-cn_topic_0224276912_p16137163320505"></a><a name="zh-cn_topic_0224276912_p16137163320505"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276912_p14137153314502"><a name="zh-cn_topic_0224276912_p14137153314502"></a><a name="zh-cn_topic_0224276912_p14137153314502"></a>用户所属帐号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276912_row1213233305018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276912_p11381533115016"><a name="zh-cn_topic_0224276912_p11381533115016"></a><a name="zh-cn_topic_0224276912_p11381533115016"></a>xaccount_type</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276912_p4138333105020"><a name="zh-cn_topic_0224276912_p4138333105020"></a><a name="zh-cn_topic_0224276912_p4138333105020"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276912_p1139113395011"><a name="zh-cn_topic_0224276912_p1139113395011"></a><a name="zh-cn_topic_0224276912_p1139113395011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276912_p1913933315010"><a name="zh-cn_topic_0224276912_p1913933315010"></a><a name="zh-cn_topic_0224276912_p1913933315010"></a>该字段为标识租户来源字段，默认为空。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276912_row14132143312507"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276912_p114023312505"><a name="zh-cn_topic_0224276912_p114023312505"></a><a name="zh-cn_topic_0224276912_p114023312505"></a>metadata</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276912_p14141183315509"><a name="zh-cn_topic_0224276912_p14141183315509"></a><a name="zh-cn_topic_0224276912_p14141183315509"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276912_p51416338503"><a name="zh-cn_topic_0224276912_p51416338503"></a><a name="zh-cn_topic_0224276912_p51416338503"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276912_p51417335502"><a name="zh-cn_topic_0224276912_p51417335502"></a><a name="zh-cn_topic_0224276912_p51417335502"></a>该字段为用户IdP服务器的Metadata文件的内容。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0224276912_section61421333135010"></a>

**表 4**  响应Body参数

<a name="zh-cn_topic_0224276912_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276912_row1014453385014"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276912_p1814503375013"><a name="zh-cn_topic_0224276912_p1814503375013"></a><a name="zh-cn_topic_0224276912_p1814503375013"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276912_p1414503345015"><a name="zh-cn_topic_0224276912_p1414503345015"></a><a name="zh-cn_topic_0224276912_p1414503345015"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276912_p13146113395016"><a name="zh-cn_topic_0224276912_p13146113395016"></a><a name="zh-cn_topic_0224276912_p13146113395016"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276912_row2144143395016"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276912_p15146143315015"><a name="zh-cn_topic_0224276912_p15146143315015"></a><a name="zh-cn_topic_0224276912_p15146143315015"></a>message</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276912_p11471533115017"><a name="zh-cn_topic_0224276912_p11471533115017"></a><a name="zh-cn_topic_0224276912_p11471533115017"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276912_p414773315010"><a name="zh-cn_topic_0224276912_p414773315010"></a><a name="zh-cn_topic_0224276912_p414773315010"></a>导入结果信息。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0224276912_section10148193385019"></a>

```
POST https://iam.myhuaweicloud.com/v3-ext/OS-FEDERATION/identity_providers/{idp_id}/protocols/{protocol_id}/metadata
```

```
{
    "xaccount_type": "",
    "domain_id": "d78cbac186b744899480f25bd...",
    "metadata": "<md:EntityDescript..."
}
```

## 响应示例<a name="zh-cn_topic_0224276912_section415123355014"></a>

**状态码为 201 时:**

导入成功。

```
{
    "message": "Import metadata successful"
}
```

## 返回值<a name="zh-cn_topic_0224276912_section121533331502"></a>

<a name="zh-cn_topic_0224276912_table4326"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276912_row91541333105013"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0224276912_p6155153316504"><a name="zh-cn_topic_0224276912_p6155153316504"></a><a name="zh-cn_topic_0224276912_p6155153316504"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0224276912_p71551033115010"><a name="zh-cn_topic_0224276912_p71551033115010"></a><a name="zh-cn_topic_0224276912_p71551033115010"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276912_row15154333185016"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276912_p215693314508"><a name="zh-cn_topic_0224276912_p215693314508"></a><a name="zh-cn_topic_0224276912_p215693314508"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276912_p16156633175015"><a name="zh-cn_topic_0224276912_p16156633175015"></a><a name="zh-cn_topic_0224276912_p16156633175015"></a>导入成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276912_row1715420334504"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276912_p20157113325016"><a name="zh-cn_topic_0224276912_p20157113325016"></a><a name="zh-cn_topic_0224276912_p20157113325016"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276912_p131577336509"><a name="zh-cn_topic_0224276912_p131577336509"></a><a name="zh-cn_topic_0224276912_p131577336509"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276912_row1515415337503"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276912_p10158333135014"><a name="zh-cn_topic_0224276912_p10158333135014"></a><a name="zh-cn_topic_0224276912_p10158333135014"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276912_p8158033145011"><a name="zh-cn_topic_0224276912_p8158033145011"></a><a name="zh-cn_topic_0224276912_p8158033145011"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276912_row1415473375010"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276912_p1015916332504"><a name="zh-cn_topic_0224276912_p1015916332504"></a><a name="zh-cn_topic_0224276912_p1015916332504"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276912_p8159143317506"><a name="zh-cn_topic_0224276912_p8159143317506"></a><a name="zh-cn_topic_0224276912_p8159143317506"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276912_row121542332509"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276912_p7160183335011"><a name="zh-cn_topic_0224276912_p7160183335011"></a><a name="zh-cn_topic_0224276912_p7160183335011"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276912_p116113395011"><a name="zh-cn_topic_0224276912_p116113395011"></a><a name="zh-cn_topic_0224276912_p116113395011"></a>内部服务错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0224276912_section101612033155011"></a>

无

