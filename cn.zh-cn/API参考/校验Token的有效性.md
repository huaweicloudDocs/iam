# 校验Token的有效性<a name="iam_30_0004"></a>

## 功能介绍<a name="zh-cn_topic_0221482410_section159226622018"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)校验本帐号中IAM用户token的有效性，或IAM用户校验自己token的有效性。管理员仅能校验本帐号中IAM用户token的有效性，不能校验其他帐号中IAM用户token的有效性。如果被校验的token有效，则返回该token的详细信息。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section99315113538"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneValidateToken)中调试该接口。

## URI<a name="zh-cn_topic_0221482410_section792319692016"></a>

GET /v3/auth/tokens

**表 1**  Query参数

<a name="zh-cn_topic_0221482410_table14923196132019"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row119231264208"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482410_p1092415642020"><a name="zh-cn_topic_0221482410_p1092415642020"></a><a name="zh-cn_topic_0221482410_p1092415642020"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482410_p109242066205"><a name="zh-cn_topic_0221482410_p109242066205"></a><a name="zh-cn_topic_0221482410_p109242066205"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482410_p149249617202"><a name="zh-cn_topic_0221482410_p149249617202"></a><a name="zh-cn_topic_0221482410_p149249617202"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482410_p092415619203"><a name="zh-cn_topic_0221482410_p092415619203"></a><a name="zh-cn_topic_0221482410_p092415619203"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row119233652013"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482410_p1924563208"><a name="zh-cn_topic_0221482410_p1924563208"></a><a name="zh-cn_topic_0221482410_p1924563208"></a>nocatalog</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482410_p169246617203"><a name="zh-cn_topic_0221482410_p169246617203"></a><a name="zh-cn_topic_0221482410_p169246617203"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482410_p79244602012"><a name="zh-cn_topic_0221482410_p79244602012"></a><a name="zh-cn_topic_0221482410_p79244602012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482410_p1292519622010"><a name="zh-cn_topic_0221482410_p1292519622010"></a><a name="zh-cn_topic_0221482410_p1292519622010"></a>如果设置该参数，返回的响应体中将不显示catalog参数。任何非空字符串都将解释为true，并使该字段生效。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482410_section159254613209"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482410_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row1192518632018"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482410_p209251368205"><a name="zh-cn_topic_0221482410_p209251368205"></a><a name="zh-cn_topic_0221482410_p209251368205"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.2%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482410_p1592618620202"><a name="zh-cn_topic_0221482410_p1592618620202"></a><a name="zh-cn_topic_0221482410_p1592618620202"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.8%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482410_p179260682019"><a name="zh-cn_topic_0221482410_p179260682019"></a><a name="zh-cn_topic_0221482410_p179260682019"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482410_p29266652015"><a name="zh-cn_topic_0221482410_p29266652015"></a><a name="zh-cn_topic_0221482410_p29266652015"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row792546142015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482410_p179265622016"><a name="zh-cn_topic_0221482410_p179265622016"></a><a name="zh-cn_topic_0221482410_p179265622016"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482410_p092611610205"><a name="zh-cn_topic_0221482410_p092611610205"></a><a name="zh-cn_topic_0221482410_p092611610205"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.8%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482410_p16926116192018"><a name="zh-cn_topic_0221482410_p16926116192018"></a><a name="zh-cn_topic_0221482410_p16926116192018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482410_p20926126152018"><a name="zh-cn_topic_0221482410_p20926126152018"></a><a name="zh-cn_topic_0221482410_p20926126152018"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row1292516102014"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482410_p7927964200"><a name="zh-cn_topic_0221482410_p7927964200"></a><a name="zh-cn_topic_0221482410_p7927964200"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482410_p1292716142015"><a name="zh-cn_topic_0221482410_p1292716142015"></a><a name="zh-cn_topic_0221482410_p1292716142015"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.8%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482410_p49275613206"><a name="zh-cn_topic_0221482410_p49275613206"></a><a name="zh-cn_topic_0221482410_p49275613206"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482410_p1492716692011"><a name="zh-cn_topic_0221482410_p1492716692011"></a><a name="zh-cn_topic_0221482410_p1492716692011"></a><a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>校验本帐号中IAM用户的token的有效性：拥有Security Administrator权限的token。</p>
<p id="zh-cn_topic_0221482410_p179271063205"><a name="zh-cn_topic_0221482410_p179271063205"></a><a name="zh-cn_topic_0221482410_p179271063205"></a>IAM用户校验自己token的有效性：该IAM用户的token（无需特殊权限）。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row16925186102020"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482410_p092896112012"><a name="zh-cn_topic_0221482410_p092896112012"></a><a name="zh-cn_topic_0221482410_p092896112012"></a>X-Subject-Token</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482410_p159289632018"><a name="zh-cn_topic_0221482410_p159289632018"></a><a name="zh-cn_topic_0221482410_p159289632018"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.8%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482410_p09281565200"><a name="zh-cn_topic_0221482410_p09281565200"></a><a name="zh-cn_topic_0221482410_p09281565200"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482410_p6928196162020"><a name="zh-cn_topic_0221482410_p6928196162020"></a><a name="zh-cn_topic_0221482410_p6928196162020"></a>待校验的token。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482410_section139585662019"></a>

```
GET https://iam.myhuaweicloud.com/v3/auth/tokens
```

## 响应参数<a name="zh-cn_topic_0221482410_section10928063206"></a>

**表 3**  响应Header参数

<a name="zh-cn_topic_0221482410_ResponseHeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row15928566202"><th class="cellrowborder" valign="top" width="20.23%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482410_p1092976142017"><a name="zh-cn_topic_0221482410_p1092976142017"></a><a name="zh-cn_topic_0221482410_p1092976142017"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.62%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482410_p592918617203"><a name="zh-cn_topic_0221482410_p592918617203"></a><a name="zh-cn_topic_0221482410_p592918617203"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60.150000000000006%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482410_p139297617206"><a name="zh-cn_topic_0221482410_p139297617206"></a><a name="zh-cn_topic_0221482410_p139297617206"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row2092916122016"><td class="cellrowborder" valign="top" width="20.23%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p189291865200"><a name="zh-cn_topic_0221482410_p189291865200"></a><a name="zh-cn_topic_0221482410_p189291865200"></a>X-Subject-Token</p>
</td>
<td class="cellrowborder" valign="top" width="19.62%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p19304622011"><a name="zh-cn_topic_0221482410_p19304622011"></a><a name="zh-cn_topic_0221482410_p19304622011"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="60.150000000000006%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p793015616202"><a name="zh-cn_topic_0221482410_p793015616202"></a><a name="zh-cn_topic_0221482410_p793015616202"></a>已校验的token。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  响应Body参数

<a name="zh-cn_topic_0221482410_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row159302069208"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482410_p20930146152017"><a name="zh-cn_topic_0221482410_p20930146152017"></a><a name="zh-cn_topic_0221482410_p20930146152017"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482410_p793118632014"><a name="zh-cn_topic_0221482410_p793118632014"></a><a name="zh-cn_topic_0221482410_p793118632014"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482410_p19311365201"><a name="zh-cn_topic_0221482410_p19311365201"></a><a name="zh-cn_topic_0221482410_p19311365201"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row193015613204"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p49311963207"><a name="zh-cn_topic_0221482410_p49311963207"></a><a name="zh-cn_topic_0221482410_p49311963207"></a><a href="#zh-cn_topic_0221482410_response_Rs31Token">token</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p149314615205"><a name="zh-cn_topic_0221482410_p149314615205"></a><a name="zh-cn_topic_0221482410_p149314615205"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p1493110612206"><a name="zh-cn_topic_0221482410_p1493110612206"></a><a name="zh-cn_topic_0221482410_p1493110612206"></a>获取到的token信息。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  token

<a name="zh-cn_topic_0221482410_response_Rs31Token"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row893216652015"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482410_p17932146142017"><a name="zh-cn_topic_0221482410_p17932146142017"></a><a name="zh-cn_topic_0221482410_p17932146142017"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482410_p493216692010"><a name="zh-cn_topic_0221482410_p493216692010"></a><a name="zh-cn_topic_0221482410_p493216692010"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482410_p2933766207"><a name="zh-cn_topic_0221482410_p2933766207"></a><a name="zh-cn_topic_0221482410_p2933766207"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row8932116122017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p1293311622010"><a name="zh-cn_topic_0221482410_p1293311622010"></a><a name="zh-cn_topic_0221482410_p1293311622010"></a><a href="#zh-cn_topic_0221482410_response_Rs31TokenCatalogArritem">catalog</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p193319692020"><a name="zh-cn_topic_0221482410_p193319692020"></a><a name="zh-cn_topic_0221482410_p193319692020"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p1093316619200"><a name="zh-cn_topic_0221482410_p1093316619200"></a><a name="zh-cn_topic_0221482410_p1093316619200"></a>服务目录信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row169324602015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p18933869204"><a name="zh-cn_topic_0221482410_p18933869204"></a><a name="zh-cn_topic_0221482410_p18933869204"></a><a href="#zh-cn_topic_0221482410_response_Rs31TokenDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p139342612017"><a name="zh-cn_topic_0221482410_p139342612017"></a><a name="zh-cn_topic_0221482410_p139342612017"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p119340615207"><a name="zh-cn_topic_0221482410_p119340615207"></a><a name="zh-cn_topic_0221482410_p119340615207"></a>被校验token的IAM用户所属的帐号信息。如果获取token时请求体中scope参数设置为domain，则返回该字段。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row169321560205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p29341620208"><a name="zh-cn_topic_0221482410_p29341620208"></a><a name="zh-cn_topic_0221482410_p29341620208"></a>expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p09346611209"><a name="zh-cn_topic_0221482410_p09346611209"></a><a name="zh-cn_topic_0221482410_p09346611209"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p693411602014"><a name="zh-cn_topic_0221482410_p693411602014"></a><a name="zh-cn_topic_0221482410_p693411602014"></a>token过期时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row3932126142018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p19934360209"><a name="zh-cn_topic_0221482410_p19934360209"></a><a name="zh-cn_topic_0221482410_p19934360209"></a>issued_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p17934116102019"><a name="zh-cn_topic_0221482410_p17934116102019"></a><a name="zh-cn_topic_0221482410_p17934116102019"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p12934262204"><a name="zh-cn_topic_0221482410_p12934262204"></a><a name="zh-cn_topic_0221482410_p12934262204"></a>token下发时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row1493211662015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p1193586152015"><a name="zh-cn_topic_0221482410_p1193586152015"></a><a name="zh-cn_topic_0221482410_p1193586152015"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p7935156112019"><a name="zh-cn_topic_0221482410_p7935156112019"></a><a name="zh-cn_topic_0221482410_p7935156112019"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p793517642018"><a name="zh-cn_topic_0221482410_p793517642018"></a><a name="zh-cn_topic_0221482410_p793517642018"></a>获取token的方式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row1293215618207"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p1093513622013"><a name="zh-cn_topic_0221482410_p1093513622013"></a><a name="zh-cn_topic_0221482410_p1093513622013"></a><a href="#zh-cn_topic_0221482410_response_Rs31TokenProject">project</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p49351967204"><a name="zh-cn_topic_0221482410_p49351967204"></a><a name="zh-cn_topic_0221482410_p49351967204"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p199358662018"><a name="zh-cn_topic_0221482410_p199358662018"></a><a name="zh-cn_topic_0221482410_p199358662018"></a>被校验token的IAM用户所属帐号的项目信息。如果获取token时请求体中scope参数设置为project，则返回该字段。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row3932176142014"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p159354662012"><a name="zh-cn_topic_0221482410_p159354662012"></a><a name="zh-cn_topic_0221482410_p159354662012"></a><a href="#zh-cn_topic_0221482410_response_Rs31TokenRolesArritem">roles</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p169369618205"><a name="zh-cn_topic_0221482410_p169369618205"></a><a name="zh-cn_topic_0221482410_p169369618205"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p1593613614205"><a name="zh-cn_topic_0221482410_p1593613614205"></a><a name="zh-cn_topic_0221482410_p1593613614205"></a>token的权限信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row119327611201"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p1993686132010"><a name="zh-cn_topic_0221482410_p1993686132010"></a><a name="zh-cn_topic_0221482410_p1993686132010"></a><a href="#zh-cn_topic_0221482410_response_Rs31TokenUser">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p169369616203"><a name="zh-cn_topic_0221482410_p169369616203"></a><a name="zh-cn_topic_0221482410_p169369616203"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p3936136172017"><a name="zh-cn_topic_0221482410_p3936136172017"></a><a name="zh-cn_topic_0221482410_p3936136172017"></a>获取token的IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  token.catalog

<a name="zh-cn_topic_0221482410_response_Rs31TokenCatalogArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row1893710614205"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482410_p10937126142014"><a name="zh-cn_topic_0221482410_p10937126142014"></a><a name="zh-cn_topic_0221482410_p10937126142014"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482410_p99372662012"><a name="zh-cn_topic_0221482410_p99372662012"></a><a name="zh-cn_topic_0221482410_p99372662012"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482410_p0938126172014"><a name="zh-cn_topic_0221482410_p0938126172014"></a><a name="zh-cn_topic_0221482410_p0938126172014"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row49375692017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p093815615204"><a name="zh-cn_topic_0221482410_p093815615204"></a><a name="zh-cn_topic_0221482410_p093815615204"></a><a href="#zh-cn_topic_0221482410_response_Rs31TokenCatalogArritemEndpointsArritem">endpoints</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p493876102019"><a name="zh-cn_topic_0221482410_p493876102019"></a><a name="zh-cn_topic_0221482410_p493876102019"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p139381669203"><a name="zh-cn_topic_0221482410_p139381669203"></a><a name="zh-cn_topic_0221482410_p139381669203"></a>终端节点。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row893718615208"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p139389620201"><a name="zh-cn_topic_0221482410_p139389620201"></a><a name="zh-cn_topic_0221482410_p139389620201"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p9938260204"><a name="zh-cn_topic_0221482410_p9938260204"></a><a name="zh-cn_topic_0221482410_p9938260204"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p593911642016"><a name="zh-cn_topic_0221482410_p593911642016"></a><a name="zh-cn_topic_0221482410_p593911642016"></a>服务ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row1293718692010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p15939126152020"><a name="zh-cn_topic_0221482410_p15939126152020"></a><a name="zh-cn_topic_0221482410_p15939126152020"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p1993917632014"><a name="zh-cn_topic_0221482410_p1993917632014"></a><a name="zh-cn_topic_0221482410_p1993917632014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p1993912613205"><a name="zh-cn_topic_0221482410_p1993912613205"></a><a name="zh-cn_topic_0221482410_p1993912613205"></a>服务名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row149371366206"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p1793916162015"><a name="zh-cn_topic_0221482410_p1793916162015"></a><a name="zh-cn_topic_0221482410_p1793916162015"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p1893996172011"><a name="zh-cn_topic_0221482410_p1893996172011"></a><a name="zh-cn_topic_0221482410_p1893996172011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p109391365205"><a name="zh-cn_topic_0221482410_p109391365205"></a><a name="zh-cn_topic_0221482410_p109391365205"></a>该接口所属服务。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  token.catalog.endpoints

<a name="zh-cn_topic_0221482410_response_Rs31TokenCatalogArritemEndpointsArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row6940465209"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482410_p3940106192014"><a name="zh-cn_topic_0221482410_p3940106192014"></a><a name="zh-cn_topic_0221482410_p3940106192014"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482410_p1094010652018"><a name="zh-cn_topic_0221482410_p1094010652018"></a><a name="zh-cn_topic_0221482410_p1094010652018"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482410_p1094196152015"><a name="zh-cn_topic_0221482410_p1094196152015"></a><a name="zh-cn_topic_0221482410_p1094196152015"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row2940176122015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p694112682017"><a name="zh-cn_topic_0221482410_p694112682017"></a><a name="zh-cn_topic_0221482410_p694112682017"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p1194146182011"><a name="zh-cn_topic_0221482410_p1194146182011"></a><a name="zh-cn_topic_0221482410_p1194146182011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p119411618201"><a name="zh-cn_topic_0221482410_p119411618201"></a><a name="zh-cn_topic_0221482410_p119411618201"></a>终端节点ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row18940966203"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p149411618202"><a name="zh-cn_topic_0221482410_p149411618202"></a><a name="zh-cn_topic_0221482410_p149411618202"></a>interface</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p1494112692013"><a name="zh-cn_topic_0221482410_p1494112692013"></a><a name="zh-cn_topic_0221482410_p1494112692013"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p1894126162017"><a name="zh-cn_topic_0221482410_p1894126162017"></a><a name="zh-cn_topic_0221482410_p1894126162017"></a>接口类型，描述接口在该终端节点的可见性。值为“public”，表示该接口为公开接口。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row1994013616203"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p1294186102010"><a name="zh-cn_topic_0221482410_p1294186102010"></a><a name="zh-cn_topic_0221482410_p1294186102010"></a>region</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p0942186152016"><a name="zh-cn_topic_0221482410_p0942186152016"></a><a name="zh-cn_topic_0221482410_p0942186152016"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p11942126192016"><a name="zh-cn_topic_0221482410_p11942126192016"></a><a name="zh-cn_topic_0221482410_p11942126192016"></a>终端节点所属区域。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row209401760205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p6942176152019"><a name="zh-cn_topic_0221482410_p6942176152019"></a><a name="zh-cn_topic_0221482410_p6942176152019"></a>region_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p1294213652020"><a name="zh-cn_topic_0221482410_p1294213652020"></a><a name="zh-cn_topic_0221482410_p1294213652020"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p1294214622015"><a name="zh-cn_topic_0221482410_p1294214622015"></a><a name="zh-cn_topic_0221482410_p1294214622015"></a>终端节点所属区域ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row129401662204"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p1942176102019"><a name="zh-cn_topic_0221482410_p1942176102019"></a><a name="zh-cn_topic_0221482410_p1942176102019"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p1594210610201"><a name="zh-cn_topic_0221482410_p1594210610201"></a><a name="zh-cn_topic_0221482410_p1594210610201"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p1994212613206"><a name="zh-cn_topic_0221482410_p1994212613206"></a><a name="zh-cn_topic_0221482410_p1994212613206"></a>终端节点的URL。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  token.domain

<a name="zh-cn_topic_0221482410_response_Rs31TokenDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row17943126192016"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482410_p8943196112013"><a name="zh-cn_topic_0221482410_p8943196112013"></a><a name="zh-cn_topic_0221482410_p8943196112013"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482410_p994326192014"><a name="zh-cn_topic_0221482410_p994326192014"></a><a name="zh-cn_topic_0221482410_p994326192014"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482410_p59436612202"><a name="zh-cn_topic_0221482410_p59436612202"></a><a name="zh-cn_topic_0221482410_p59436612202"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row69431616205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p15944196192016"><a name="zh-cn_topic_0221482410_p15944196192016"></a><a name="zh-cn_topic_0221482410_p15944196192016"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p119441366206"><a name="zh-cn_topic_0221482410_p119441366206"></a><a name="zh-cn_topic_0221482410_p119441366206"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p3944469207"><a name="zh-cn_topic_0221482410_p3944469207"></a><a name="zh-cn_topic_0221482410_p3944469207"></a>帐号名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row189431066206"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p59444652019"><a name="zh-cn_topic_0221482410_p59444652019"></a><a name="zh-cn_topic_0221482410_p59444652019"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p294412612015"><a name="zh-cn_topic_0221482410_p294412612015"></a><a name="zh-cn_topic_0221482410_p294412612015"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p159457692010"><a name="zh-cn_topic_0221482410_p159457692010"></a><a name="zh-cn_topic_0221482410_p159457692010"></a>帐号ID。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  token.project

<a name="zh-cn_topic_0221482410_response_Rs31TokenProject"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row69464611204"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482410_p49461867201"><a name="zh-cn_topic_0221482410_p49461867201"></a><a name="zh-cn_topic_0221482410_p49461867201"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482410_p19464662017"><a name="zh-cn_topic_0221482410_p19464662017"></a><a name="zh-cn_topic_0221482410_p19464662017"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482410_p89461264207"><a name="zh-cn_topic_0221482410_p89461264207"></a><a name="zh-cn_topic_0221482410_p89461264207"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row1946176132013"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p10947146112013"><a name="zh-cn_topic_0221482410_p10947146112013"></a><a name="zh-cn_topic_0221482410_p10947146112013"></a><a href="#zh-cn_topic_0221482410_response_Rs31TokenProjectDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p894766122015"><a name="zh-cn_topic_0221482410_p894766122015"></a><a name="zh-cn_topic_0221482410_p894766122015"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p18947468200"><a name="zh-cn_topic_0221482410_p18947468200"></a><a name="zh-cn_topic_0221482410_p18947468200"></a>项目所属帐号信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row394620632010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p1947061201"><a name="zh-cn_topic_0221482410_p1947061201"></a><a name="zh-cn_topic_0221482410_p1947061201"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p4947764209"><a name="zh-cn_topic_0221482410_p4947764209"></a><a name="zh-cn_topic_0221482410_p4947764209"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p1694896172017"><a name="zh-cn_topic_0221482410_p1694896172017"></a><a name="zh-cn_topic_0221482410_p1694896172017"></a>项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row2094616672010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p394813622017"><a name="zh-cn_topic_0221482410_p394813622017"></a><a name="zh-cn_topic_0221482410_p394813622017"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p179482063208"><a name="zh-cn_topic_0221482410_p179482063208"></a><a name="zh-cn_topic_0221482410_p179482063208"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p39480682016"><a name="zh-cn_topic_0221482410_p39480682016"></a><a name="zh-cn_topic_0221482410_p39480682016"></a>项目名称。</p>
</td>
</tr>
</tbody>
</table>

**表 10**  token.project.domain

<a name="zh-cn_topic_0221482410_response_Rs31TokenProjectDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row149483672010"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482410_p1294916672019"><a name="zh-cn_topic_0221482410_p1294916672019"></a><a name="zh-cn_topic_0221482410_p1294916672019"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482410_p1094917617203"><a name="zh-cn_topic_0221482410_p1094917617203"></a><a name="zh-cn_topic_0221482410_p1094917617203"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482410_p39491614204"><a name="zh-cn_topic_0221482410_p39491614204"></a><a name="zh-cn_topic_0221482410_p39491614204"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row12948176102018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p109504622018"><a name="zh-cn_topic_0221482410_p109504622018"></a><a name="zh-cn_topic_0221482410_p109504622018"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p295036112010"><a name="zh-cn_topic_0221482410_p295036112010"></a><a name="zh-cn_topic_0221482410_p295036112010"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p129501166206"><a name="zh-cn_topic_0221482410_p129501166206"></a><a name="zh-cn_topic_0221482410_p129501166206"></a>帐号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row15948106102011"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p179509611203"><a name="zh-cn_topic_0221482410_p179509611203"></a><a name="zh-cn_topic_0221482410_p179509611203"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p1695015612013"><a name="zh-cn_topic_0221482410_p1695015612013"></a><a name="zh-cn_topic_0221482410_p1695015612013"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p19951186112010"><a name="zh-cn_topic_0221482410_p19951186112010"></a><a name="zh-cn_topic_0221482410_p19951186112010"></a>帐号名称。</p>
</td>
</tr>
</tbody>
</table>

**表 11**  token.roles

<a name="zh-cn_topic_0221482410_response_Rs31TokenRolesArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row695116102013"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482410_p8952267209"><a name="zh-cn_topic_0221482410_p8952267209"></a><a name="zh-cn_topic_0221482410_p8952267209"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482410_p1595217662017"><a name="zh-cn_topic_0221482410_p1595217662017"></a><a name="zh-cn_topic_0221482410_p1595217662017"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482410_p69526617202"><a name="zh-cn_topic_0221482410_p69526617202"></a><a name="zh-cn_topic_0221482410_p69526617202"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row1195112615202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p1952968204"><a name="zh-cn_topic_0221482410_p1952968204"></a><a name="zh-cn_topic_0221482410_p1952968204"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p495236202017"><a name="zh-cn_topic_0221482410_p495236202017"></a><a name="zh-cn_topic_0221482410_p495236202017"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p595256122017"><a name="zh-cn_topic_0221482410_p595256122017"></a><a name="zh-cn_topic_0221482410_p595256122017"></a>权限名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row2951126172015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p5952176172019"><a name="zh-cn_topic_0221482410_p5952176172019"></a><a name="zh-cn_topic_0221482410_p5952176172019"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p8953667201"><a name="zh-cn_topic_0221482410_p8953667201"></a><a name="zh-cn_topic_0221482410_p8953667201"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p1895317642018"><a name="zh-cn_topic_0221482410_p1895317642018"></a><a name="zh-cn_topic_0221482410_p1895317642018"></a>权限ID。默认显示为0，非真实权限ID。</p>
</td>
</tr>
</tbody>
</table>

**表 12**  token.user

<a name="zh-cn_topic_0221482410_response_Rs31TokenUser"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row495317619205"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482410_p99547618201"><a name="zh-cn_topic_0221482410_p99547618201"></a><a name="zh-cn_topic_0221482410_p99547618201"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482410_p1795410602016"><a name="zh-cn_topic_0221482410_p1795410602016"></a><a name="zh-cn_topic_0221482410_p1795410602016"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482410_p1595496172014"><a name="zh-cn_topic_0221482410_p1595496172014"></a><a name="zh-cn_topic_0221482410_p1595496172014"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row1895318616201"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p99549672019"><a name="zh-cn_topic_0221482410_p99549672019"></a><a name="zh-cn_topic_0221482410_p99549672019"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p4954166142012"><a name="zh-cn_topic_0221482410_p4954166142012"></a><a name="zh-cn_topic_0221482410_p4954166142012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p17954116142020"><a name="zh-cn_topic_0221482410_p17954116142020"></a><a name="zh-cn_topic_0221482410_p17954116142020"></a>IAM用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row109534672011"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p59555616204"><a name="zh-cn_topic_0221482410_p59555616204"></a><a name="zh-cn_topic_0221482410_p59555616204"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p2095510652017"><a name="zh-cn_topic_0221482410_p2095510652017"></a><a name="zh-cn_topic_0221482410_p2095510652017"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p9955206192013"><a name="zh-cn_topic_0221482410_p9955206192013"></a><a name="zh-cn_topic_0221482410_p9955206192013"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row16953565209"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p199552617207"><a name="zh-cn_topic_0221482410_p199552617207"></a><a name="zh-cn_topic_0221482410_p199552617207"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p1595519620204"><a name="zh-cn_topic_0221482410_p1595519620204"></a><a name="zh-cn_topic_0221482410_p1595519620204"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p119550612017"><a name="zh-cn_topic_0221482410_p119550612017"></a><a name="zh-cn_topic_0221482410_p119550612017"></a>密码过期时间（UTC时间），“”表示密码不过期。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row1095320612203"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p14955467204"><a name="zh-cn_topic_0221482410_p14955467204"></a><a name="zh-cn_topic_0221482410_p14955467204"></a><a href="#zh-cn_topic_0221482410_response_Rs31TokenUserDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p895617619204"><a name="zh-cn_topic_0221482410_p895617619204"></a><a name="zh-cn_topic_0221482410_p895617619204"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p1495618618207"><a name="zh-cn_topic_0221482410_p1495618618207"></a><a name="zh-cn_topic_0221482410_p1495618618207"></a>IAM用户所属的帐号信息。</p>
</td>
</tr>
</tbody>
</table>

**表 13**  token.user.domain

<a name="zh-cn_topic_0221482410_response_Rs31TokenUserDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row79561769207"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482410_p1795610692010"><a name="zh-cn_topic_0221482410_p1795610692010"></a><a name="zh-cn_topic_0221482410_p1795610692010"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482410_p195711611206"><a name="zh-cn_topic_0221482410_p195711611206"></a><a name="zh-cn_topic_0221482410_p195711611206"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482410_p1795715615205"><a name="zh-cn_topic_0221482410_p1795715615205"></a><a name="zh-cn_topic_0221482410_p1795715615205"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row1095614602019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p69575662018"><a name="zh-cn_topic_0221482410_p69575662018"></a><a name="zh-cn_topic_0221482410_p69575662018"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p1095715616206"><a name="zh-cn_topic_0221482410_p1095715616206"></a><a name="zh-cn_topic_0221482410_p1095715616206"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p1195713611204"><a name="zh-cn_topic_0221482410_p1195713611204"></a><a name="zh-cn_topic_0221482410_p1195713611204"></a>IAM用户所属帐号名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row19956962205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482410_p595712692015"><a name="zh-cn_topic_0221482410_p595712692015"></a><a name="zh-cn_topic_0221482410_p595712692015"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482410_p7957166142015"><a name="zh-cn_topic_0221482410_p7957166142015"></a><a name="zh-cn_topic_0221482410_p7957166142015"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482410_p6958167202"><a name="zh-cn_topic_0221482410_p6958167202"></a><a name="zh-cn_topic_0221482410_p6958167202"></a>IAM用户所属帐号ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 响应示例<a name="zh-cn_topic_0221482410_section495813682010"></a>

**状态码为 200 时:**

请求成功。

```
响应Header参数：
X-Subject-Token:MIIatAYJKoZIhvcNAQcCoIIapTCCGqECAQExDTALB...
```

```
响应Body参数：
{
    "token": {
        "expires_at": "2020-01-04T09:08:49.965000Z",
        "methods": [
            "password"
        ],
        "catalog": [
            {
                "endpoints": [
                    {
                        "id": "33e1cbdd86d34e89a63cf8ad16a5f49f",
                        "interface": "public",
                        "region": "*",
                        "region_id": "*",
                        "url": "https://iam.myhuaweicloud.com/v3.0"
                    }
                ],
                "id": "100a6a3477f1495286579b819d399e36",
                "name": "iam",
                "type": "iam"
            },
            {
                "endpoints": [
                    {
                        "id": "29319cf2052d4e94bcf438b55d143832",
                        "interface": "public",
                        "region": "*",
                        "region_id": "*",
                        "url": "https://bss.sample.domain.com/v1.0"
                    }
                ],
                "id": "c6db69fabbd549908adcb861c7e47ca4",
                "name": "bssv1",
                "type": "bssv1"
            }
        ],
        "domain": {
            "id": "d78cbac186b744899480f25bd022f468",
            "name": "IAMDomain"
        },
        "roles": [
            {
                "id": "0",
                "name": "te_admin"
            },
            {
                "id": "0",
                "name": "secu_admin"
            },
            {
                "id": "0",
                "name": "te_agency"
            }
        ],
        "issued_at": "2020-01-03T09:08:49.965000Z",
        "user": {
            "domain": {
                "id": "d78cbac186b744899480f25bd022f468",
                "name": "IAMDomain"
            },
            "id": "7116d09f88fa41908676fdd4b039e95b",
            "name": "IAMUser",
            "password_expires_at": ""
        }
    }
}
```

**状态码为 404 时:**

未找到相应的资源。

```
{
    "error": {
        "code": 404,
        "message": "X-Subject-Token is invalid in the request",
        "title": "Not Found"
    }
}
```

## 返回值<a name="zh-cn_topic_0221482410_section182241675208"></a>

<a name="zh-cn_topic_0221482410_table2417"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482410_row1296886182015"><th class="cellrowborder" valign="top" width="15.040000000000001%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482410_p13224778204"><a name="zh-cn_topic_0221482410_p13224778204"></a><a name="zh-cn_topic_0221482410_p13224778204"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="84.96000000000001%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482410_p142241775205"><a name="zh-cn_topic_0221482410_p142241775205"></a><a name="zh-cn_topic_0221482410_p142241775205"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482410_row096819672011"><td class="cellrowborder" valign="top" width="15.040000000000001%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482410_p922413772016"><a name="zh-cn_topic_0221482410_p922413772016"></a><a name="zh-cn_topic_0221482410_p922413772016"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="84.96000000000001%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482410_p5224471201"><a name="zh-cn_topic_0221482410_p5224471201"></a><a name="zh-cn_topic_0221482410_p5224471201"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row14968196132015"><td class="cellrowborder" valign="top" width="15.040000000000001%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482410_p222415712010"><a name="zh-cn_topic_0221482410_p222415712010"></a><a name="zh-cn_topic_0221482410_p222415712010"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="84.96000000000001%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482410_p102243712020"><a name="zh-cn_topic_0221482410_p102243712020"></a><a name="zh-cn_topic_0221482410_p102243712020"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row99681462201"><td class="cellrowborder" valign="top" width="15.040000000000001%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482410_p13224167182010"><a name="zh-cn_topic_0221482410_p13224167182010"></a><a name="zh-cn_topic_0221482410_p13224167182010"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="84.96000000000001%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482410_p10224371202"><a name="zh-cn_topic_0221482410_p10224371202"></a><a name="zh-cn_topic_0221482410_p10224371202"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row29689610208"><td class="cellrowborder" valign="top" width="15.040000000000001%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482410_p8224978206"><a name="zh-cn_topic_0221482410_p8224978206"></a><a name="zh-cn_topic_0221482410_p8224978206"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="84.96000000000001%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482410_p722417713206"><a name="zh-cn_topic_0221482410_p722417713206"></a><a name="zh-cn_topic_0221482410_p722417713206"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482410_row109681367206"><td class="cellrowborder" valign="top" width="15.040000000000001%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482410_p22248782016"><a name="zh-cn_topic_0221482410_p22248782016"></a><a name="zh-cn_topic_0221482410_p22248782016"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="84.96000000000001%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482410_p62246713207"><a name="zh-cn_topic_0221482410_p62246713207"></a><a name="zh-cn_topic_0221482410_p62246713207"></a>内部服务错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482410_section52247715209"></a>

无

