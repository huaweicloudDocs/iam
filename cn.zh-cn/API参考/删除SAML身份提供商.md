# 删除SAML身份提供商<a name="iam_13_0206"></a>

## 功能介绍<a name="zh-cn_topic_0224276870_section14911125185016"></a>

该接口可以用于<u>[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)</u><u></u>  删除基于SAML协议的身份提供商。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section2485151619141"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneDeleteIdentityProvider)中调试该接口。

## URI<a name="zh-cn_topic_0224276870_section991115555016"></a>

DELETE /v3/OS-FEDERATION/identity\_providers/\{id\}

**表 1**  路径参数

<a name="zh-cn_topic_0224276870_table1091245155014"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276870_row891245175013"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276870_p13912654509"><a name="zh-cn_topic_0224276870_p13912654509"></a><a name="zh-cn_topic_0224276870_p13912654509"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276870_p189134518508"><a name="zh-cn_topic_0224276870_p189134518508"></a><a name="zh-cn_topic_0224276870_p189134518508"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276870_p119132595019"><a name="zh-cn_topic_0224276870_p119132595019"></a><a name="zh-cn_topic_0224276870_p119132595019"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276870_p19913205185019"><a name="zh-cn_topic_0224276870_p19913205185019"></a><a name="zh-cn_topic_0224276870_p19913205185019"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276870_row891218518500"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276870_p29137555016"><a name="zh-cn_topic_0224276870_p29137555016"></a><a name="zh-cn_topic_0224276870_p29137555016"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276870_p1191317512509"><a name="zh-cn_topic_0224276870_p1191317512509"></a><a name="zh-cn_topic_0224276870_p1191317512509"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276870_p1191412575011"><a name="zh-cn_topic_0224276870_p1191412575011"></a><a name="zh-cn_topic_0224276870_p1191412575011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276870_p89147575012"><a name="zh-cn_topic_0224276870_p89147575012"></a><a name="zh-cn_topic_0224276870_p89147575012"></a>待删除的身份提供商ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0224276870_section15914175165015"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0224276870_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276870_row189142513503"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276870_p59153585017"><a name="zh-cn_topic_0224276870_p59153585017"></a><a name="zh-cn_topic_0224276870_p59153585017"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276870_p159163513506"><a name="zh-cn_topic_0224276870_p159163513506"></a><a name="zh-cn_topic_0224276870_p159163513506"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276870_p79161055505"><a name="zh-cn_topic_0224276870_p79161055505"></a><a name="zh-cn_topic_0224276870_p79161055505"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276870_p15917175155017"><a name="zh-cn_topic_0224276870_p15917175155017"></a><a name="zh-cn_topic_0224276870_p15917175155017"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276870_row1891410515506"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276870_p1991755115017"><a name="zh-cn_topic_0224276870_p1991755115017"></a><a name="zh-cn_topic_0224276870_p1991755115017"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276870_p15918145195011"><a name="zh-cn_topic_0224276870_p15918145195011"></a><a name="zh-cn_topic_0224276870_p15918145195011"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276870_p1591911513501"><a name="zh-cn_topic_0224276870_p1591911513501"></a><a name="zh-cn_topic_0224276870_p1591911513501"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276870_p2919254505"><a name="zh-cn_topic_0224276870_p2919254505"></a><a name="zh-cn_topic_0224276870_p2919254505"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276870_row1191515516507"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276870_p1591912545015"><a name="zh-cn_topic_0224276870_p1591912545015"></a><a name="zh-cn_topic_0224276870_p1591912545015"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276870_p0919153506"><a name="zh-cn_topic_0224276870_p0919153506"></a><a name="zh-cn_topic_0224276870_p0919153506"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276870_p2920855502"><a name="zh-cn_topic_0224276870_p2920855502"></a><a name="zh-cn_topic_0224276870_p2920855502"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276870_p792010516507"><a name="zh-cn_topic_0224276870_p792010516507"></a><a name="zh-cn_topic_0224276870_p792010516507"></a>请参见<a href="授权项.md">授权项</a>。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0224276870_section189201750508"></a>

无

## 请求示例<a name="zh-cn_topic_0224276870_section2920115115017"></a>

```
DELETE https://iam.myhuaweicloud.com/v3/OS-FEDERATION/identity_providers/{id}
```

## 响应示例<a name="zh-cn_topic_0224276870_section59219595011"></a>

无

## 返回值<a name="zh-cn_topic_0224276870_section79211055501"></a>

<a name="zh-cn_topic_0224276870_table4314"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276870_row89227595014"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0224276870_p18922115175016"><a name="zh-cn_topic_0224276870_p18922115175016"></a><a name="zh-cn_topic_0224276870_p18922115175016"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0224276870_p59222565013"><a name="zh-cn_topic_0224276870_p59222565013"></a><a name="zh-cn_topic_0224276870_p59222565013"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276870_row892218545018"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276870_p292316535012"><a name="zh-cn_topic_0224276870_p292316535012"></a><a name="zh-cn_topic_0224276870_p292316535012"></a>204</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276870_p69234515019"><a name="zh-cn_topic_0224276870_p69234515019"></a><a name="zh-cn_topic_0224276870_p69234515019"></a>删除成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276870_row1922155145018"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276870_p69233515013"><a name="zh-cn_topic_0224276870_p69233515013"></a><a name="zh-cn_topic_0224276870_p69233515013"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276870_p1992355135020"><a name="zh-cn_topic_0224276870_p1992355135020"></a><a name="zh-cn_topic_0224276870_p1992355135020"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276870_row169224519504"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276870_p7923652501"><a name="zh-cn_topic_0224276870_p7923652501"></a><a name="zh-cn_topic_0224276870_p7923652501"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276870_p199241057506"><a name="zh-cn_topic_0224276870_p199241057506"></a><a name="zh-cn_topic_0224276870_p199241057506"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276870_row4922454502"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276870_p15924255505"><a name="zh-cn_topic_0224276870_p15924255505"></a><a name="zh-cn_topic_0224276870_p15924255505"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276870_p1992413505016"><a name="zh-cn_topic_0224276870_p1992413505016"></a><a name="zh-cn_topic_0224276870_p1992413505016"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276870_row10922165155016"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276870_p119245511508"><a name="zh-cn_topic_0224276870_p119245511508"></a><a name="zh-cn_topic_0224276870_p119245511508"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276870_p1692411516506"><a name="zh-cn_topic_0224276870_p1692411516506"></a><a name="zh-cn_topic_0224276870_p1692411516506"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276870_row159225517501"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276870_p159254565011"><a name="zh-cn_topic_0224276870_p159254565011"></a><a name="zh-cn_topic_0224276870_p159254565011"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276870_p592516510502"><a name="zh-cn_topic_0224276870_p592516510502"></a><a name="zh-cn_topic_0224276870_p592516510502"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276870_row192235165011"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276870_p592516535017"><a name="zh-cn_topic_0224276870_p592516535017"></a><a name="zh-cn_topic_0224276870_p592516535017"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276870_p29254512509"><a name="zh-cn_topic_0224276870_p29254512509"></a><a name="zh-cn_topic_0224276870_p29254512509"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276870_row892225125018"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276870_p14925458506"><a name="zh-cn_topic_0224276870_p14925458506"></a><a name="zh-cn_topic_0224276870_p14925458506"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276870_p1292620595017"><a name="zh-cn_topic_0224276870_p1292620595017"></a><a name="zh-cn_topic_0224276870_p1292620595017"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276870_row192225205016"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276870_p592613545013"><a name="zh-cn_topic_0224276870_p592613545013"></a><a name="zh-cn_topic_0224276870_p592613545013"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276870_p159263555016"><a name="zh-cn_topic_0224276870_p159263555016"></a><a name="zh-cn_topic_0224276870_p159263555016"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0224276870_section1092617585010"></a>

无

