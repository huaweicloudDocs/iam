# 获取委托Token<a name="zh-cn_topic_0064274720"></a>

## 功能介绍<a name="zh-cn_topic_0221482426_section1799876182019"></a>

该接口可以用于获取委托方的token。

例如：A账号希望B账号管理自己的某些资源，所以A账号创建了委托给B账号，则A账号为委托方，B账号为被委托方。那么B账号可以通过该接口获取委托token。B账号仅能使用该token管理A账号的委托资源，不能管理自己账号中的资源。如果B账号需要管理自己账号中的资源，则需要获取自己的用户token。

token是系统颁发给用户的访问令牌，承载用户的身份、权限等信息。调用IAM以及其他云服务的接口时，可以使用本接口获取的token进行鉴权。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。如果使用全局区域的Endpoint调用，该token可以在所有区域使用；如果使用非全局区域的Endpoint调用，则该token仅在该区域生效，不能跨区域使用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   token的有效期为24小时，建议进行缓存，避免频繁调用。  

## URI<a name="zh-cn_topic_0221482426_section1199914614206"></a>

POST /v3/auth/tokens

**表 1**  Query参数

<a name="zh-cn_topic_0221482426_table39991066202"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row49995617208"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482426_p705710202"><a name="zh-cn_topic_0221482426_p705710202"></a><a name="zh-cn_topic_0221482426_p705710202"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482426_p906715206"><a name="zh-cn_topic_0221482426_p906715206"></a><a name="zh-cn_topic_0221482426_p906715206"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482426_p170079200"><a name="zh-cn_topic_0221482426_p170079200"></a><a name="zh-cn_topic_0221482426_p170079200"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482426_p19013713207"><a name="zh-cn_topic_0221482426_p19013713207"></a><a name="zh-cn_topic_0221482426_p19013713207"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row29992615202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p160147162011"><a name="zh-cn_topic_0221482426_p160147162011"></a><a name="zh-cn_topic_0221482426_p160147162011"></a>nocatalog</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p50127182017"><a name="zh-cn_topic_0221482426_p50127182017"></a><a name="zh-cn_topic_0221482426_p50127182017"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p12014712016"><a name="zh-cn_topic_0221482426_p12014712016"></a><a name="zh-cn_topic_0221482426_p12014712016"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p2197192012"><a name="zh-cn_topic_0221482426_p2197192012"></a><a name="zh-cn_topic_0221482426_p2197192012"></a>如果设置该参数，返回的响应体中将不显示catalog信息。任何非空字符串都将解释为true，并使该字段生效。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482426_section315752010"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482426_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row10157152016"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482426_p92578204"><a name="zh-cn_topic_0221482426_p92578204"></a><a name="zh-cn_topic_0221482426_p92578204"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482426_p1123742020"><a name="zh-cn_topic_0221482426_p1123742020"></a><a name="zh-cn_topic_0221482426_p1123742020"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482426_p821372202"><a name="zh-cn_topic_0221482426_p821372202"></a><a name="zh-cn_topic_0221482426_p821372202"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482426_p9247162016"><a name="zh-cn_topic_0221482426_p9247162016"></a><a name="zh-cn_topic_0221482426_p9247162016"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row3115722020"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p2219722013"><a name="zh-cn_topic_0221482426_p2219722013"></a><a name="zh-cn_topic_0221482426_p2219722013"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p2020710202"><a name="zh-cn_topic_0221482426_p2020710202"></a><a name="zh-cn_topic_0221482426_p2020710202"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p9313717201"><a name="zh-cn_topic_0221482426_p9313717201"></a><a name="zh-cn_topic_0221482426_p9313717201"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p1936710201"><a name="zh-cn_topic_0221482426_p1936710201"></a><a name="zh-cn_topic_0221482426_p1936710201"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row1118717201"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p123117152017"><a name="zh-cn_topic_0221482426_p123117152017"></a><a name="zh-cn_topic_0221482426_p123117152017"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p124170209"><a name="zh-cn_topic_0221482426_p124170209"></a><a name="zh-cn_topic_0221482426_p124170209"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p12447162020"><a name="zh-cn_topic_0221482426_p12447162020"></a><a name="zh-cn_topic_0221482426_p12447162020"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p1545732010"><a name="zh-cn_topic_0221482426_p1545732010"></a><a name="zh-cn_topic_0221482426_p1545732010"></a>被委托方B账号中的IAM用户B具有Agent Operator权限的token。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="zh-cn_topic_0221482426_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row744762011"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482426_p351575202"><a name="zh-cn_topic_0221482426_p351575202"></a><a name="zh-cn_topic_0221482426_p351575202"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482426_p5513718204"><a name="zh-cn_topic_0221482426_p5513718204"></a><a name="zh-cn_topic_0221482426_p5513718204"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482426_p1651276209"><a name="zh-cn_topic_0221482426_p1651276209"></a><a name="zh-cn_topic_0221482426_p1651276209"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482426_p0514720206"><a name="zh-cn_topic_0221482426_p0514720206"></a><a name="zh-cn_topic_0221482426_p0514720206"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row842710205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p19513772016"><a name="zh-cn_topic_0221482426_p19513772016"></a><a name="zh-cn_topic_0221482426_p19513772016"></a><a href="#zh-cn_topic_0221482426_request_Rq32Auth">auth</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p1356712201"><a name="zh-cn_topic_0221482426_p1356712201"></a><a name="zh-cn_topic_0221482426_p1356712201"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p351679201"><a name="zh-cn_topic_0221482426_p351679201"></a><a name="zh-cn_topic_0221482426_p351679201"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p2617720203"><a name="zh-cn_topic_0221482426_p2617720203"></a><a name="zh-cn_topic_0221482426_p2617720203"></a>认证信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  auth

<a name="zh-cn_topic_0221482426_request_Rq32Auth"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row1162722013"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482426_p106127152017"><a name="zh-cn_topic_0221482426_p106127152017"></a><a name="zh-cn_topic_0221482426_p106127152017"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482426_p16610710204"><a name="zh-cn_topic_0221482426_p16610710204"></a><a name="zh-cn_topic_0221482426_p16610710204"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482426_p771179200"><a name="zh-cn_topic_0221482426_p771179200"></a><a name="zh-cn_topic_0221482426_p771179200"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482426_p87971205"><a name="zh-cn_topic_0221482426_p87971205"></a><a name="zh-cn_topic_0221482426_p87971205"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row168752017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p12716712202"><a name="zh-cn_topic_0221482426_p12716712202"></a><a name="zh-cn_topic_0221482426_p12716712202"></a><a href="#zh-cn_topic_0221482426_request_Rq32AuthIdentity">identity</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p13714712013"><a name="zh-cn_topic_0221482426_p13714712013"></a><a name="zh-cn_topic_0221482426_p13714712013"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p16717132012"><a name="zh-cn_topic_0221482426_p16717132012"></a><a name="zh-cn_topic_0221482426_p16717132012"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p6777172010"><a name="zh-cn_topic_0221482426_p6777172010"></a><a name="zh-cn_topic_0221482426_p6777172010"></a>认证参数。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row5612742010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p478710204"><a name="zh-cn_topic_0221482426_p478710204"></a><a name="zh-cn_topic_0221482426_p478710204"></a><a href="#zh-cn_topic_0221482426_request_Rq32AuthScope">scope</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p1083762010"><a name="zh-cn_topic_0221482426_p1083762010"></a><a name="zh-cn_topic_0221482426_p1083762010"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p10837122013"><a name="zh-cn_topic_0221482426_p10837122013"></a><a name="zh-cn_topic_0221482426_p10837122013"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p7810720203"><a name="zh-cn_topic_0221482426_p7810720203"></a><a name="zh-cn_topic_0221482426_p7810720203"></a>token的使用范围，需要填写委托方A的project或domain，填写其中任一即可。</p>
<div class="note" id="zh-cn_topic_0221482426_note148571204"><a name="zh-cn_topic_0221482426_note148571204"></a><a name="zh-cn_topic_0221482426_note148571204"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0221482426_p1288714202"><a name="zh-cn_topic_0221482426_p1288714202"></a><a name="zh-cn_topic_0221482426_p1288714202"></a>使用全局区域的Endpoint调用该接口时，推荐您将scope设置为domain，该token可以跨区域使用，如果将scope设置为project，该token仅能在指定的project中使用，不能跨区域使用。</p>
</div></div>
</td>
</tr>
</tbody>
</table>

**表 5**  auth.identity

<a name="zh-cn_topic_0221482426_request_Rq32AuthIdentity"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row18827152012"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482426_p14919719200"><a name="zh-cn_topic_0221482426_p14919719200"></a><a name="zh-cn_topic_0221482426_p14919719200"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482426_p491772012"><a name="zh-cn_topic_0221482426_p491772012"></a><a name="zh-cn_topic_0221482426_p491772012"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482426_p495742016"><a name="zh-cn_topic_0221482426_p495742016"></a><a name="zh-cn_topic_0221482426_p495742016"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482426_p490711200"><a name="zh-cn_topic_0221482426_p490711200"></a><a name="zh-cn_topic_0221482426_p490711200"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row158971201"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p69197102011"><a name="zh-cn_topic_0221482426_p69197102011"></a><a name="zh-cn_topic_0221482426_p69197102011"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p161037162013"><a name="zh-cn_topic_0221482426_p161037162013"></a><a name="zh-cn_topic_0221482426_p161037162013"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p8106732014"><a name="zh-cn_topic_0221482426_p8106732014"></a><a name="zh-cn_topic_0221482426_p8106732014"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p111018782015"><a name="zh-cn_topic_0221482426_p111018782015"></a><a name="zh-cn_topic_0221482426_p111018782015"></a>token的获取方式，该字段内容为["assume_role"]。</p>
<p id="zh-cn_topic_0221482426_p1101875205"><a name="zh-cn_topic_0221482426_p1101875205"></a><a name="zh-cn_topic_0221482426_p1101875205"></a>取值范围：</p>
<a name="zh-cn_topic_0221482426_ul21019742012"></a><a name="zh-cn_topic_0221482426_ul21019742012"></a><ul id="zh-cn_topic_0221482426_ul21019742012"><li>assume_role</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row158874203"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p81014792015"><a name="zh-cn_topic_0221482426_p81014792015"></a><a name="zh-cn_topic_0221482426_p81014792015"></a><a href="#zh-cn_topic_0221482426_request_Rq32AuthIdentityAssumerole">assume_role</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p1410378200"><a name="zh-cn_topic_0221482426_p1410378200"></a><a name="zh-cn_topic_0221482426_p1410378200"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p181019719203"><a name="zh-cn_topic_0221482426_p181019719203"></a><a name="zh-cn_topic_0221482426_p181019719203"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p1111776204"><a name="zh-cn_topic_0221482426_p1111776204"></a><a name="zh-cn_topic_0221482426_p1111776204"></a>assume_role的具体信息。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  auth.identity.assume\_role

<a name="zh-cn_topic_0221482426_request_Rq32AuthIdentityAssumerole"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row211172204"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482426_p181115717204"><a name="zh-cn_topic_0221482426_p181115717204"></a><a name="zh-cn_topic_0221482426_p181115717204"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482426_p6111371207"><a name="zh-cn_topic_0221482426_p6111371207"></a><a name="zh-cn_topic_0221482426_p6111371207"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482426_p01287142018"><a name="zh-cn_topic_0221482426_p01287142018"></a><a name="zh-cn_topic_0221482426_p01287142018"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482426_p131287172014"><a name="zh-cn_topic_0221482426_p131287172014"></a><a name="zh-cn_topic_0221482426_p131287172014"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row01118712017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p012167182014"><a name="zh-cn_topic_0221482426_p012167182014"></a><a name="zh-cn_topic_0221482426_p012167182014"></a>domain_name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p312167192011"><a name="zh-cn_topic_0221482426_p312167192011"></a><a name="zh-cn_topic_0221482426_p312167192011"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p1112137102012"><a name="zh-cn_topic_0221482426_p1112137102012"></a><a name="zh-cn_topic_0221482426_p1112137102012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p1122715203"><a name="zh-cn_topic_0221482426_p1122715203"></a><a name="zh-cn_topic_0221482426_p1122715203"></a>委托方A的账号名称。“domain_id”与“domain_name”至少填写一个。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row151120752015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p1127717207"><a name="zh-cn_topic_0221482426_p1127717207"></a><a name="zh-cn_topic_0221482426_p1127717207"></a>xrole_name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p313207192017"><a name="zh-cn_topic_0221482426_p313207192017"></a><a name="zh-cn_topic_0221482426_p313207192017"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p51314742018"><a name="zh-cn_topic_0221482426_p51314742018"></a><a name="zh-cn_topic_0221482426_p51314742018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p12134715209"><a name="zh-cn_topic_0221482426_p12134715209"></a><a name="zh-cn_topic_0221482426_p12134715209"></a>委托方A创建的委托的名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row171112719205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p713137142011"><a name="zh-cn_topic_0221482426_p713137142011"></a><a name="zh-cn_topic_0221482426_p713137142011"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p19131677202"><a name="zh-cn_topic_0221482426_p19131677202"></a><a name="zh-cn_topic_0221482426_p19131677202"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p1013117102019"><a name="zh-cn_topic_0221482426_p1013117102019"></a><a name="zh-cn_topic_0221482426_p1013117102019"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p141311712018"><a name="zh-cn_topic_0221482426_p141311712018"></a><a name="zh-cn_topic_0221482426_p141311712018"></a>委托方A的账号ID。“domain_id”与“domain_name”至少填写一个。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  auth.scope

<a name="zh-cn_topic_0221482426_request_Rq32AuthScope"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row18144710206"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482426_p171413792011"><a name="zh-cn_topic_0221482426_p171413792011"></a><a name="zh-cn_topic_0221482426_p171413792011"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482426_p81410720209"><a name="zh-cn_topic_0221482426_p81410720209"></a><a name="zh-cn_topic_0221482426_p81410720209"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482426_p10151711206"><a name="zh-cn_topic_0221482426_p10151711206"></a><a name="zh-cn_topic_0221482426_p10151711206"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482426_p1615171207"><a name="zh-cn_topic_0221482426_p1615171207"></a><a name="zh-cn_topic_0221482426_p1615171207"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row1814207162012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p11151712203"><a name="zh-cn_topic_0221482426_p11151712203"></a><a name="zh-cn_topic_0221482426_p11151712203"></a><a href="#zh-cn_topic_0221482426_request_Rq32AuthScopeDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p115207152016"><a name="zh-cn_topic_0221482426_p115207152016"></a><a name="zh-cn_topic_0221482426_p115207152016"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p191577142015"><a name="zh-cn_topic_0221482426_p191577142015"></a><a name="zh-cn_topic_0221482426_p191577142015"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p1515207142014"><a name="zh-cn_topic_0221482426_p1515207142014"></a><a name="zh-cn_topic_0221482426_p1515207142014"></a>委托方A的domain信息。表示获取的token可以跨区域使用，domain支持id和name，填写任一即可。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row81410715203"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p91510717208"><a name="zh-cn_topic_0221482426_p91510717208"></a><a name="zh-cn_topic_0221482426_p91510717208"></a><a href="#zh-cn_topic_0221482426_request_Rq32AuthScopeProject">project</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p121697102011"><a name="zh-cn_topic_0221482426_p121697102011"></a><a name="zh-cn_topic_0221482426_p121697102011"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p20165762011"><a name="zh-cn_topic_0221482426_p20165762011"></a><a name="zh-cn_topic_0221482426_p20165762011"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p171617711202"><a name="zh-cn_topic_0221482426_p171617711202"></a><a name="zh-cn_topic_0221482426_p171617711202"></a>委托方A的项目信息，表示获取的token仅能访问指定项目下的资源，project支持id和name，填写任一即可。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  auth.scope.domain

<a name="zh-cn_topic_0221482426_request_Rq32AuthScopeDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row416197122018"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482426_p418478203"><a name="zh-cn_topic_0221482426_p418478203"></a><a name="zh-cn_topic_0221482426_p418478203"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482426_p2186712204"><a name="zh-cn_topic_0221482426_p2186712204"></a><a name="zh-cn_topic_0221482426_p2186712204"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482426_p01816716204"><a name="zh-cn_topic_0221482426_p01816716204"></a><a name="zh-cn_topic_0221482426_p01816716204"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482426_p1418973202"><a name="zh-cn_topic_0221482426_p1418973202"></a><a name="zh-cn_topic_0221482426_p1418973202"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row6169710201"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p51957202014"><a name="zh-cn_topic_0221482426_p51957202014"></a><a name="zh-cn_topic_0221482426_p51957202014"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p82010710203"><a name="zh-cn_topic_0221482426_p82010710203"></a><a name="zh-cn_topic_0221482426_p82010710203"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p4201976203"><a name="zh-cn_topic_0221482426_p4201976203"></a><a name="zh-cn_topic_0221482426_p4201976203"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p1220374203"><a name="zh-cn_topic_0221482426_p1220374203"></a><a name="zh-cn_topic_0221482426_p1220374203"></a>委托方A的账号ID，获取方式请参见：<a href="获取IAM用户-项目-用户组-委托的名称和ID.md">获取IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row101613792014"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p1201776202"><a name="zh-cn_topic_0221482426_p1201776202"></a><a name="zh-cn_topic_0221482426_p1201776202"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p4209718207"><a name="zh-cn_topic_0221482426_p4209718207"></a><a name="zh-cn_topic_0221482426_p4209718207"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p120670203"><a name="zh-cn_topic_0221482426_p120670203"></a><a name="zh-cn_topic_0221482426_p120670203"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p8208716203"><a name="zh-cn_topic_0221482426_p8208716203"></a><a name="zh-cn_topic_0221482426_p8208716203"></a>委托方A的账号名。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  auth.scope.project

<a name="zh-cn_topic_0221482426_request_Rq32AuthScopeProject"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row132118742013"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482426_p92118782018"><a name="zh-cn_topic_0221482426_p92118782018"></a><a name="zh-cn_topic_0221482426_p92118782018"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482426_p621107152011"><a name="zh-cn_topic_0221482426_p621107152011"></a><a name="zh-cn_topic_0221482426_p621107152011"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482426_p122127192013"><a name="zh-cn_topic_0221482426_p122127192013"></a><a name="zh-cn_topic_0221482426_p122127192013"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482426_p0223716204"><a name="zh-cn_topic_0221482426_p0223716204"></a><a name="zh-cn_topic_0221482426_p0223716204"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row52112772011"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p1228710203"><a name="zh-cn_topic_0221482426_p1228710203"></a><a name="zh-cn_topic_0221482426_p1228710203"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p14221576202"><a name="zh-cn_topic_0221482426_p14221576202"></a><a name="zh-cn_topic_0221482426_p14221576202"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p122219715201"><a name="zh-cn_topic_0221482426_p122219715201"></a><a name="zh-cn_topic_0221482426_p122219715201"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p02217202015"><a name="zh-cn_topic_0221482426_p02217202015"></a><a name="zh-cn_topic_0221482426_p02217202015"></a>委托方A项目的ID，获取方式请参见：<a href="获取IAM用户-项目-用户组-委托的名称和ID.md">获取IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row2211876203"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482426_p52218715207"><a name="zh-cn_topic_0221482426_p52218715207"></a><a name="zh-cn_topic_0221482426_p52218715207"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482426_p82357192019"><a name="zh-cn_topic_0221482426_p82357192019"></a><a name="zh-cn_topic_0221482426_p82357192019"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482426_p7231379202"><a name="zh-cn_topic_0221482426_p7231379202"></a><a name="zh-cn_topic_0221482426_p7231379202"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482426_p2023127142018"><a name="zh-cn_topic_0221482426_p2023127142018"></a><a name="zh-cn_topic_0221482426_p2023127142018"></a>委托方A项目的名称，获取方式请参见：<a href="获取IAM用户-项目-用户组-委托的名称和ID.md">获取IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482426_section13239762012"></a>

**表 10**  响应Header参数

<a name="zh-cn_topic_0221482426_ResponseHeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row723207172012"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p17247702010"><a name="zh-cn_topic_0221482426_p17247702010"></a><a name="zh-cn_topic_0221482426_p17247702010"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p62417142014"><a name="zh-cn_topic_0221482426_p62417142014"></a><a name="zh-cn_topic_0221482426_p62417142014"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p4241576205"><a name="zh-cn_topic_0221482426_p4241576205"></a><a name="zh-cn_topic_0221482426_p4241576205"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row1523976201"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p15245715208"><a name="zh-cn_topic_0221482426_p15245715208"></a><a name="zh-cn_topic_0221482426_p15245715208"></a>X-Subject-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p324672209"><a name="zh-cn_topic_0221482426_p324672209"></a><a name="zh-cn_topic_0221482426_p324672209"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p82417142017"><a name="zh-cn_topic_0221482426_p82417142017"></a><a name="zh-cn_topic_0221482426_p82417142017"></a>签名后的token。</p>
</td>
</tr>
</tbody>
</table>

**表 11**  响应Body参数

<a name="zh-cn_topic_0221482426_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row11257715203"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p182507122014"><a name="zh-cn_topic_0221482426_p182507122014"></a><a name="zh-cn_topic_0221482426_p182507122014"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p32597112013"><a name="zh-cn_topic_0221482426_p32597112013"></a><a name="zh-cn_topic_0221482426_p32597112013"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p1925117132011"><a name="zh-cn_topic_0221482426_p1925117132011"></a><a name="zh-cn_topic_0221482426_p1925117132011"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row8259712020"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p02515742019"><a name="zh-cn_topic_0221482426_p02515742019"></a><a name="zh-cn_topic_0221482426_p02515742019"></a><a href="#zh-cn_topic_0221482426_response_Rs32Token">token</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p12261377207"><a name="zh-cn_topic_0221482426_p12261377207"></a><a name="zh-cn_topic_0221482426_p12261377207"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p142637182013"><a name="zh-cn_topic_0221482426_p142637182013"></a><a name="zh-cn_topic_0221482426_p142637182013"></a>token信息列表。</p>
</td>
</tr>
</tbody>
</table>

**表 12**  token

<a name="zh-cn_topic_0221482426_response_Rs32Token"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row72611732020"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p528975201"><a name="zh-cn_topic_0221482426_p528975201"></a><a name="zh-cn_topic_0221482426_p528975201"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p132827152014"><a name="zh-cn_topic_0221482426_p132827152014"></a><a name="zh-cn_topic_0221482426_p132827152014"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p16283792019"><a name="zh-cn_topic_0221482426_p16283792019"></a><a name="zh-cn_topic_0221482426_p16283792019"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row10268762019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p1728078208"><a name="zh-cn_topic_0221482426_p1728078208"></a><a name="zh-cn_topic_0221482426_p1728078208"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1129127112020"><a name="zh-cn_topic_0221482426_p1129127112020"></a><a name="zh-cn_topic_0221482426_p1129127112020"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p129197122014"><a name="zh-cn_topic_0221482426_p129197122014"></a><a name="zh-cn_topic_0221482426_p129197122014"></a>获取token的方式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row1926167202011"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p72913732015"><a name="zh-cn_topic_0221482426_p72913732015"></a><a name="zh-cn_topic_0221482426_p72913732015"></a>expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1030875209"><a name="zh-cn_topic_0221482426_p1030875209"></a><a name="zh-cn_topic_0221482426_p1030875209"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p63019718208"><a name="zh-cn_topic_0221482426_p63019718208"></a><a name="zh-cn_topic_0221482426_p63019718208"></a>token到期时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row13261970209"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p230167142014"><a name="zh-cn_topic_0221482426_p230167142014"></a><a name="zh-cn_topic_0221482426_p230167142014"></a>issued_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1630177142015"><a name="zh-cn_topic_0221482426_p1630177142015"></a><a name="zh-cn_topic_0221482426_p1630177142015"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p103016712012"><a name="zh-cn_topic_0221482426_p103016712012"></a><a name="zh-cn_topic_0221482426_p103016712012"></a>token下发时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row72620720208"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p193011715202"><a name="zh-cn_topic_0221482426_p193011715202"></a><a name="zh-cn_topic_0221482426_p193011715202"></a><a href="#zh-cn_topic_0221482426_response_Rs32TokenAssumedby">assumed_by</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p9301172203"><a name="zh-cn_topic_0221482426_p9301172203"></a><a name="zh-cn_topic_0221482426_p9301172203"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p20311716204"><a name="zh-cn_topic_0221482426_p20311716204"></a><a name="zh-cn_topic_0221482426_p20311716204"></a>被委托方B的相关信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row4261978202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p83197152017"><a name="zh-cn_topic_0221482426_p83197152017"></a><a name="zh-cn_topic_0221482426_p83197152017"></a><a href="#zh-cn_topic_0221482426_response_Rs31TokenCatalogArritem">catalog</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p9314719209"><a name="zh-cn_topic_0221482426_p9314719209"></a><a name="zh-cn_topic_0221482426_p9314719209"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p13112782017"><a name="zh-cn_topic_0221482426_p13112782017"></a><a name="zh-cn_topic_0221482426_p13112782017"></a>服务目录信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row1626673203"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p163117711200"><a name="zh-cn_topic_0221482426_p163117711200"></a><a name="zh-cn_topic_0221482426_p163117711200"></a><a href="#zh-cn_topic_0221482426_response_Rs32TokenDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p131147132012"><a name="zh-cn_topic_0221482426_p131147132012"></a><a name="zh-cn_topic_0221482426_p131147132012"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p133111717206"><a name="zh-cn_topic_0221482426_p133111717206"></a><a name="zh-cn_topic_0221482426_p133111717206"></a>委托方A的账号信息。如果获取token时请求体中scope参数设置为domain，则返回该字段。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row102620720205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p232177182016"><a name="zh-cn_topic_0221482426_p232177182016"></a><a name="zh-cn_topic_0221482426_p232177182016"></a><a href="#zh-cn_topic_0221482426_response_Rs32TokenProject">project</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p33218713206"><a name="zh-cn_topic_0221482426_p33218713206"></a><a name="zh-cn_topic_0221482426_p33218713206"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p5321710201"><a name="zh-cn_topic_0221482426_p5321710201"></a><a name="zh-cn_topic_0221482426_p5321710201"></a>委托方A的项目信息。如果获取token时请求体中scope参数设置为project，则返回该字段。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row8272742019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p3323792014"><a name="zh-cn_topic_0221482426_p3323792014"></a><a name="zh-cn_topic_0221482426_p3323792014"></a><a href="#zh-cn_topic_0221482426_response_Rs31TokenRolesArritem">roles</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p33217710204"><a name="zh-cn_topic_0221482426_p33217710204"></a><a name="zh-cn_topic_0221482426_p33217710204"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p183314712015"><a name="zh-cn_topic_0221482426_p183314712015"></a><a name="zh-cn_topic_0221482426_p183314712015"></a>委托token的权限信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row1727673202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p143310742020"><a name="zh-cn_topic_0221482426_p143310742020"></a><a name="zh-cn_topic_0221482426_p143310742020"></a><a href="#zh-cn_topic_0221482426_response_Rs32TokenUser">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1933197172014"><a name="zh-cn_topic_0221482426_p1933197172014"></a><a name="zh-cn_topic_0221482426_p1933197172014"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p2331878201"><a name="zh-cn_topic_0221482426_p2331878201"></a><a name="zh-cn_topic_0221482426_p2331878201"></a>委托方A所创建的委托的信息。</p>
</td>
</tr>
</tbody>
</table>

**表 13**  token.assumed\_by

<a name="zh-cn_topic_0221482426_response_Rs32TokenAssumedby"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row11338792012"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p15341792012"><a name="zh-cn_topic_0221482426_p15341792012"></a><a name="zh-cn_topic_0221482426_p15341792012"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p12341378205"><a name="zh-cn_topic_0221482426_p12341378205"></a><a name="zh-cn_topic_0221482426_p12341378205"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p73410752015"><a name="zh-cn_topic_0221482426_p73410752015"></a><a name="zh-cn_topic_0221482426_p73410752015"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row143318711205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p2344713200"><a name="zh-cn_topic_0221482426_p2344713200"></a><a name="zh-cn_topic_0221482426_p2344713200"></a><a href="#zh-cn_topic_0221482426_response_Rs32TokenAssumedbyUser">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p134157122013"><a name="zh-cn_topic_0221482426_p134157122013"></a><a name="zh-cn_topic_0221482426_p134157122013"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p1535167162012"><a name="zh-cn_topic_0221482426_p1535167162012"></a><a name="zh-cn_topic_0221482426_p1535167162012"></a>被委托方B中IAM用户的用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 14**  token.assumed\_by.user

<a name="zh-cn_topic_0221482426_response_Rs32TokenAssumedbyUser"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row6351976202"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p12359716200"><a name="zh-cn_topic_0221482426_p12359716200"></a><a name="zh-cn_topic_0221482426_p12359716200"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p2356792015"><a name="zh-cn_topic_0221482426_p2356792015"></a><a name="zh-cn_topic_0221482426_p2356792015"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p15362713209"><a name="zh-cn_topic_0221482426_p15362713209"></a><a name="zh-cn_topic_0221482426_p15362713209"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row93510752013"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p133253716201"><a name="zh-cn_topic_0221482426_p133253716201"></a><a name="zh-cn_topic_0221482426_p133253716201"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p5325197132015"><a name="zh-cn_topic_0221482426_p5325197132015"></a><a name="zh-cn_topic_0221482426_p5325197132015"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p23253715207"><a name="zh-cn_topic_0221482426_p23253715207"></a><a name="zh-cn_topic_0221482426_p23253715207"></a>被委托方B中IAM用户的用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row035167142010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p203254714209"><a name="zh-cn_topic_0221482426_p203254714209"></a><a name="zh-cn_topic_0221482426_p203254714209"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p532577142013"><a name="zh-cn_topic_0221482426_p532577142013"></a><a name="zh-cn_topic_0221482426_p532577142013"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p43251178205"><a name="zh-cn_topic_0221482426_p43251178205"></a><a name="zh-cn_topic_0221482426_p43251178205"></a>被委托方B中IAM用户的用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row203515772018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p93257720202"><a name="zh-cn_topic_0221482426_p93257720202"></a><a name="zh-cn_topic_0221482426_p93257720202"></a><a href="#zh-cn_topic_0221482426_response_Rs32TokenAssumedbyUserDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1232597122010"><a name="zh-cn_topic_0221482426_p1232597122010"></a><a name="zh-cn_topic_0221482426_p1232597122010"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p132517192010"><a name="zh-cn_topic_0221482426_p132517192010"></a><a name="zh-cn_topic_0221482426_p132517192010"></a>被委托方B的账号信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row1535117192018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p193254720209"><a name="zh-cn_topic_0221482426_p193254720209"></a><a name="zh-cn_topic_0221482426_p193254720209"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1032515714204"><a name="zh-cn_topic_0221482426_p1032515714204"></a><a name="zh-cn_topic_0221482426_p1032515714204"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p2325673204"><a name="zh-cn_topic_0221482426_p2325673204"></a><a name="zh-cn_topic_0221482426_p2325673204"></a>被委托方B中IAM用户的密码过期时间（UTC时间），“”表示密码不过期。</p>
</td>
</tr>
</tbody>
</table>

**表 15**  token.assumed\_by.user.domain

<a name="zh-cn_topic_0221482426_response_Rs32TokenAssumedbyUserDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row183815714204"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p8325117102018"><a name="zh-cn_topic_0221482426_p8325117102018"></a><a name="zh-cn_topic_0221482426_p8325117102018"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p183259720202"><a name="zh-cn_topic_0221482426_p183259720202"></a><a name="zh-cn_topic_0221482426_p183259720202"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p173257720204"><a name="zh-cn_topic_0221482426_p173257720204"></a><a name="zh-cn_topic_0221482426_p173257720204"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row18384714203"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p832511772011"><a name="zh-cn_topic_0221482426_p832511772011"></a><a name="zh-cn_topic_0221482426_p832511772011"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p173251473202"><a name="zh-cn_topic_0221482426_p173251473202"></a><a name="zh-cn_topic_0221482426_p173251473202"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p23251273209"><a name="zh-cn_topic_0221482426_p23251273209"></a><a name="zh-cn_topic_0221482426_p23251273209"></a>被委托方B的账号名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row0381979202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p93251713208"><a name="zh-cn_topic_0221482426_p93251713208"></a><a name="zh-cn_topic_0221482426_p93251713208"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p132527152013"><a name="zh-cn_topic_0221482426_p132527152013"></a><a name="zh-cn_topic_0221482426_p132527152013"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p17325177152016"><a name="zh-cn_topic_0221482426_p17325177152016"></a><a name="zh-cn_topic_0221482426_p17325177152016"></a>被委托方B的账号ID。</p>
</td>
</tr>
</tbody>
</table>

**表 16**  token.catalog

<a name="zh-cn_topic_0221482426_response_Rs31TokenCatalogArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row15401579202"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p1232520792015"><a name="zh-cn_topic_0221482426_p1232520792015"></a><a name="zh-cn_topic_0221482426_p1232520792015"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p183255782011"><a name="zh-cn_topic_0221482426_p183255782011"></a><a name="zh-cn_topic_0221482426_p183255782011"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p19325187122019"><a name="zh-cn_topic_0221482426_p19325187122019"></a><a name="zh-cn_topic_0221482426_p19325187122019"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row20401475202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p183258712011"><a name="zh-cn_topic_0221482426_p183258712011"></a><a name="zh-cn_topic_0221482426_p183258712011"></a><a href="#zh-cn_topic_0221482426_response_Rs31TokenCatalogArritemEndpointsArritem">endpoints</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1932513722016"><a name="zh-cn_topic_0221482426_p1932513722016"></a><a name="zh-cn_topic_0221482426_p1932513722016"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p232616722011"><a name="zh-cn_topic_0221482426_p232616722011"></a><a name="zh-cn_topic_0221482426_p232616722011"></a>终端节点。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row14401972205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p53267752010"><a name="zh-cn_topic_0221482426_p53267752010"></a><a name="zh-cn_topic_0221482426_p53267752010"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p173262720204"><a name="zh-cn_topic_0221482426_p173262720204"></a><a name="zh-cn_topic_0221482426_p173262720204"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p203261274205"><a name="zh-cn_topic_0221482426_p203261274205"></a><a name="zh-cn_topic_0221482426_p203261274205"></a>服务ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row164014719209"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p14326273202"><a name="zh-cn_topic_0221482426_p14326273202"></a><a name="zh-cn_topic_0221482426_p14326273202"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p17326117152019"><a name="zh-cn_topic_0221482426_p17326117152019"></a><a name="zh-cn_topic_0221482426_p17326117152019"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p13264720205"><a name="zh-cn_topic_0221482426_p13264720205"></a><a name="zh-cn_topic_0221482426_p13264720205"></a>服务名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row240167172012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p17326187112019"><a name="zh-cn_topic_0221482426_p17326187112019"></a><a name="zh-cn_topic_0221482426_p17326187112019"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p11326137122010"><a name="zh-cn_topic_0221482426_p11326137122010"></a><a name="zh-cn_topic_0221482426_p11326137122010"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p2032620782020"><a name="zh-cn_topic_0221482426_p2032620782020"></a><a name="zh-cn_topic_0221482426_p2032620782020"></a>该接口所属服务。</p>
</td>
</tr>
</tbody>
</table>

**表 17**  token.catalog.endpoints

<a name="zh-cn_topic_0221482426_response_Rs31TokenCatalogArritemEndpointsArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row343147192018"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p5326107192010"><a name="zh-cn_topic_0221482426_p5326107192010"></a><a name="zh-cn_topic_0221482426_p5326107192010"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p632612715208"><a name="zh-cn_topic_0221482426_p632612715208"></a><a name="zh-cn_topic_0221482426_p632612715208"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p14326207182016"><a name="zh-cn_topic_0221482426_p14326207182016"></a><a name="zh-cn_topic_0221482426_p14326207182016"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row643107132014"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p163267720208"><a name="zh-cn_topic_0221482426_p163267720208"></a><a name="zh-cn_topic_0221482426_p163267720208"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p143269712207"><a name="zh-cn_topic_0221482426_p143269712207"></a><a name="zh-cn_topic_0221482426_p143269712207"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p133261742015"><a name="zh-cn_topic_0221482426_p133261742015"></a><a name="zh-cn_topic_0221482426_p133261742015"></a>终端节点ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row17431752018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p173260782016"><a name="zh-cn_topic_0221482426_p173260782016"></a><a name="zh-cn_topic_0221482426_p173260782016"></a>interface</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p183267752016"><a name="zh-cn_topic_0221482426_p183267752016"></a><a name="zh-cn_topic_0221482426_p183267752016"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p193267718203"><a name="zh-cn_topic_0221482426_p193267718203"></a><a name="zh-cn_topic_0221482426_p193267718203"></a>接口类型，描述接口在该终端节点的可见性。值为“public”，表示该接口为公开接口。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row104312792011"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p12326476203"><a name="zh-cn_topic_0221482426_p12326476203"></a><a name="zh-cn_topic_0221482426_p12326476203"></a>region</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1232615712202"><a name="zh-cn_topic_0221482426_p1232615712202"></a><a name="zh-cn_topic_0221482426_p1232615712202"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p432687112016"><a name="zh-cn_topic_0221482426_p432687112016"></a><a name="zh-cn_topic_0221482426_p432687112016"></a>终端节点所属区域。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row174319742019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p132614702012"><a name="zh-cn_topic_0221482426_p132614702012"></a><a name="zh-cn_topic_0221482426_p132614702012"></a>region_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1232611752016"><a name="zh-cn_topic_0221482426_p1232611752016"></a><a name="zh-cn_topic_0221482426_p1232611752016"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p93263752013"><a name="zh-cn_topic_0221482426_p93263752013"></a><a name="zh-cn_topic_0221482426_p93263752013"></a>终端节点所属区域ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row124387112016"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p13326370201"><a name="zh-cn_topic_0221482426_p13326370201"></a><a name="zh-cn_topic_0221482426_p13326370201"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p10326117122020"><a name="zh-cn_topic_0221482426_p10326117122020"></a><a name="zh-cn_topic_0221482426_p10326117122020"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p23265742013"><a name="zh-cn_topic_0221482426_p23265742013"></a><a name="zh-cn_topic_0221482426_p23265742013"></a>终端节点的URL。</p>
</td>
</tr>
</tbody>
</table>

**表 18**  token.domain

<a name="zh-cn_topic_0221482426_response_Rs32TokenDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row3468712011"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p83261971207"><a name="zh-cn_topic_0221482426_p83261971207"></a><a name="zh-cn_topic_0221482426_p83261971207"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p143261873204"><a name="zh-cn_topic_0221482426_p143261873204"></a><a name="zh-cn_topic_0221482426_p143261873204"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p23261573206"><a name="zh-cn_topic_0221482426_p23261573206"></a><a name="zh-cn_topic_0221482426_p23261573206"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row1746107132020"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p93269762015"><a name="zh-cn_topic_0221482426_p93269762015"></a><a name="zh-cn_topic_0221482426_p93269762015"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p63261471204"><a name="zh-cn_topic_0221482426_p63261471204"></a><a name="zh-cn_topic_0221482426_p63261471204"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p123268716208"><a name="zh-cn_topic_0221482426_p123268716208"></a><a name="zh-cn_topic_0221482426_p123268716208"></a>委托方A的账号名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row1474792018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p83261979201"><a name="zh-cn_topic_0221482426_p83261979201"></a><a name="zh-cn_topic_0221482426_p83261979201"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p173268714204"><a name="zh-cn_topic_0221482426_p173268714204"></a><a name="zh-cn_topic_0221482426_p173268714204"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p83262070207"><a name="zh-cn_topic_0221482426_p83262070207"></a><a name="zh-cn_topic_0221482426_p83262070207"></a>委托方A的账号ID。</p>
</td>
</tr>
</tbody>
</table>

**表 19**  token.project

<a name="zh-cn_topic_0221482426_response_Rs32TokenProject"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row194914710202"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p532712742018"><a name="zh-cn_topic_0221482426_p532712742018"></a><a name="zh-cn_topic_0221482426_p532712742018"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p183272073205"><a name="zh-cn_topic_0221482426_p183272073205"></a><a name="zh-cn_topic_0221482426_p183272073205"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p2327147152011"><a name="zh-cn_topic_0221482426_p2327147152011"></a><a name="zh-cn_topic_0221482426_p2327147152011"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row164937132010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p14327678203"><a name="zh-cn_topic_0221482426_p14327678203"></a><a name="zh-cn_topic_0221482426_p14327678203"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p432719762011"><a name="zh-cn_topic_0221482426_p432719762011"></a><a name="zh-cn_topic_0221482426_p432719762011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p133277722012"><a name="zh-cn_topic_0221482426_p133277722012"></a><a name="zh-cn_topic_0221482426_p133277722012"></a>委托方A的项目名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row1749178202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p63271871207"><a name="zh-cn_topic_0221482426_p63271871207"></a><a name="zh-cn_topic_0221482426_p63271871207"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p12327177182011"><a name="zh-cn_topic_0221482426_p12327177182011"></a><a name="zh-cn_topic_0221482426_p12327177182011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p1332711711200"><a name="zh-cn_topic_0221482426_p1332711711200"></a><a name="zh-cn_topic_0221482426_p1332711711200"></a>委托方A的项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row7491772017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p163279732012"><a name="zh-cn_topic_0221482426_p163279732012"></a><a name="zh-cn_topic_0221482426_p163279732012"></a><a href="#zh-cn_topic_0221482426_response_Rs32TokenProjectDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1932787182015"><a name="zh-cn_topic_0221482426_p1932787182015"></a><a name="zh-cn_topic_0221482426_p1932787182015"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p18327107192019"><a name="zh-cn_topic_0221482426_p18327107192019"></a><a name="zh-cn_topic_0221482426_p18327107192019"></a>委托方A的账号信息。</p>
</td>
</tr>
</tbody>
</table>

**表 20**  token.project.domain

<a name="zh-cn_topic_0221482426_response_Rs32TokenProjectDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row4517710206"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p1032711702016"><a name="zh-cn_topic_0221482426_p1032711702016"></a><a name="zh-cn_topic_0221482426_p1032711702016"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p432717710205"><a name="zh-cn_topic_0221482426_p432717710205"></a><a name="zh-cn_topic_0221482426_p432717710205"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p1632719717202"><a name="zh-cn_topic_0221482426_p1632719717202"></a><a name="zh-cn_topic_0221482426_p1632719717202"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row05147172015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p103278717202"><a name="zh-cn_topic_0221482426_p103278717202"></a><a name="zh-cn_topic_0221482426_p103278717202"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p7327137132017"><a name="zh-cn_topic_0221482426_p7327137132017"></a><a name="zh-cn_topic_0221482426_p7327137132017"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p1432757102011"><a name="zh-cn_topic_0221482426_p1432757102011"></a><a name="zh-cn_topic_0221482426_p1432757102011"></a>委托方A的账号名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row11511378207"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p53271975209"><a name="zh-cn_topic_0221482426_p53271975209"></a><a name="zh-cn_topic_0221482426_p53271975209"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p13327373203"><a name="zh-cn_topic_0221482426_p13327373203"></a><a name="zh-cn_topic_0221482426_p13327373203"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p93271974206"><a name="zh-cn_topic_0221482426_p93271974206"></a><a name="zh-cn_topic_0221482426_p93271974206"></a>委托方A的账号ID。</p>
</td>
</tr>
</tbody>
</table>

**表 21**  token.roles

<a name="zh-cn_topic_0221482426_response_Rs31TokenRolesArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row19521074201"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p1332777142012"><a name="zh-cn_topic_0221482426_p1332777142012"></a><a name="zh-cn_topic_0221482426_p1332777142012"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p532715762010"><a name="zh-cn_topic_0221482426_p532715762010"></a><a name="zh-cn_topic_0221482426_p532715762010"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p932767132011"><a name="zh-cn_topic_0221482426_p932767132011"></a><a name="zh-cn_topic_0221482426_p932767132011"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row1152978207"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p33271671201"><a name="zh-cn_topic_0221482426_p33271671201"></a><a name="zh-cn_topic_0221482426_p33271671201"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1932713702010"><a name="zh-cn_topic_0221482426_p1932713702010"></a><a name="zh-cn_topic_0221482426_p1932713702010"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p143271177202"><a name="zh-cn_topic_0221482426_p143271177202"></a><a name="zh-cn_topic_0221482426_p143271177202"></a>权限名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row11521972208"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p19327571202"><a name="zh-cn_topic_0221482426_p19327571202"></a><a name="zh-cn_topic_0221482426_p19327571202"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1432719712013"><a name="zh-cn_topic_0221482426_p1432719712013"></a><a name="zh-cn_topic_0221482426_p1432719712013"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p2032713722010"><a name="zh-cn_topic_0221482426_p2032713722010"></a><a name="zh-cn_topic_0221482426_p2032713722010"></a>权限ID。默认显示为0，非真实权限ID。</p>
</td>
</tr>
</tbody>
</table>

**表 22**  token.user

<a name="zh-cn_topic_0221482426_response_Rs32TokenUser"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row95319792015"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p53271176208"><a name="zh-cn_topic_0221482426_p53271176208"></a><a name="zh-cn_topic_0221482426_p53271176208"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p332714719206"><a name="zh-cn_topic_0221482426_p332714719206"></a><a name="zh-cn_topic_0221482426_p332714719206"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p232719792014"><a name="zh-cn_topic_0221482426_p232719792014"></a><a name="zh-cn_topic_0221482426_p232719792014"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row753673209"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p9327879206"><a name="zh-cn_topic_0221482426_p9327879206"></a><a name="zh-cn_topic_0221482426_p9327879206"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p143281478205"><a name="zh-cn_topic_0221482426_p143281478205"></a><a name="zh-cn_topic_0221482426_p143281478205"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p9328127152018"><a name="zh-cn_topic_0221482426_p9328127152018"></a><a name="zh-cn_topic_0221482426_p9328127152018"></a>委托方A账号名/委托名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row165415714205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p43281676202"><a name="zh-cn_topic_0221482426_p43281676202"></a><a name="zh-cn_topic_0221482426_p43281676202"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1732837172013"><a name="zh-cn_topic_0221482426_p1732837172013"></a><a name="zh-cn_topic_0221482426_p1732837172013"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p43286742016"><a name="zh-cn_topic_0221482426_p43286742016"></a><a name="zh-cn_topic_0221482426_p43286742016"></a>委托ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row18549702015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p2328977208"><a name="zh-cn_topic_0221482426_p2328977208"></a><a name="zh-cn_topic_0221482426_p2328977208"></a><a href="#zh-cn_topic_0221482426_response_Rs32TokenUserDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p20328273207"><a name="zh-cn_topic_0221482426_p20328273207"></a><a name="zh-cn_topic_0221482426_p20328273207"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p103289702013"><a name="zh-cn_topic_0221482426_p103289702013"></a><a name="zh-cn_topic_0221482426_p103289702013"></a>委托方A的账号信息。</p>
</td>
</tr>
</tbody>
</table>

**表 23**  token.user.domain

<a name="zh-cn_topic_0221482426_response_Rs32TokenUserDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row1956147112016"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482426_p83281477203"><a name="zh-cn_topic_0221482426_p83281477203"></a><a name="zh-cn_topic_0221482426_p83281477203"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482426_p03282712011"><a name="zh-cn_topic_0221482426_p03282712011"></a><a name="zh-cn_topic_0221482426_p03282712011"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482426_p83289711203"><a name="zh-cn_topic_0221482426_p83289711203"></a><a name="zh-cn_topic_0221482426_p83289711203"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row85620752012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p1332811762019"><a name="zh-cn_topic_0221482426_p1332811762019"></a><a name="zh-cn_topic_0221482426_p1332811762019"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p1432815752015"><a name="zh-cn_topic_0221482426_p1432815752015"></a><a name="zh-cn_topic_0221482426_p1432815752015"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p33286718209"><a name="zh-cn_topic_0221482426_p33286718209"></a><a name="zh-cn_topic_0221482426_p33286718209"></a>委托方A的账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row16569712012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482426_p23286772012"><a name="zh-cn_topic_0221482426_p23286772012"></a><a name="zh-cn_topic_0221482426_p23286772012"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482426_p12328575209"><a name="zh-cn_topic_0221482426_p12328575209"></a><a name="zh-cn_topic_0221482426_p12328575209"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482426_p1328574209"><a name="zh-cn_topic_0221482426_p1328574209"></a><a name="zh-cn_topic_0221482426_p1328574209"></a>委托方A的账号名称。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482426_section53281074208"></a>

-   由被委托方B（账号名为IAMDomainB）中的IAM用户B（用户名IAMUserB，请求头中的X-Auth-Token字段需要填写IAMUserB的用户token，且该token需要具有Agent Operator权限），获取委托方A（账号名为IAMDomainA）创建的委托名为IAMAgency，作用范围为委托方A的项目“cn-north-1”，且返回的响应体中将不显示catalog信息的token。

    ```
    POST https://iam.myhuaweicloud.com/v3/auth/tokens?nocatalog=true
    ```

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "assume_role"
                ],
                "assume_role": {
                    "domain_name": "IAMDomainA",
                    "xrole_name": "IAMAgency"
                }
            },
            "scope": {
                "project": {
                    "name": "cn-north-1"
                }
            }
        }
    }
    ```

-   由被委托方B（账号名为IAMDomainB）中的IAM用户B（用户名IAMUserB，请求头中的X-Auth-Token字段需要填写IAMUserB的用户token，且该token需要具有Agent Operator权限），获取委托方A（账号名为IAMDomainA）创建的委托名为IAMAgency，作用范围为委托方A整个账号的token。

    ```
    POST https://iam.myhuaweicloud.com/v3/auth/tokens
    ```

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "assume_role"
                ],
                "assume_role": {
                    "domain_name": "IAMDomainA",
                    "xrole_name": "IAMAgency"
                }
            },
            "scope": {
                "domain": {
                    "name": "IAMDomainA"
                }
            }
        }
    }
    ```


## 响应示例<a name="zh-cn_topic_0221482426_section1032910752015"></a>

**状态码为 201 时:**

创建成功。

示例1：由被委托方B（账号名为IAMDomainB）中的IAM用户B（用户名IAMUserB，请求头中的X-Auth-Token字段需要填写IAMUserB的用户token，且该token需要具有Agent Operator权限），获取委托方A（账号名为IAMDomainA）创建的委托名为IAMAgency，作用范围为委托方A整个账号的token。

示例2：由被委托方B（账号名为IAMDomainB）中的IAM用户B（用户名IAMUserB，请求头中的X-Auth-Token字段需要填写IAMUserB的用户token，且该token需要具有Agent Operator权限），获取委托方A（账号名为IAMDomainA）创建的委托名为IAMAgency，作用范围为委托方A的项目“cn-north-1”，且返回的响应体中将不显示catalog信息的token。

-   示例 1

    ```
    响应Header参数：
    X-Subject-Token:MIIatAYJKoZIhvcNAQcCoIIapTCCGqECAQExDTALB...
    ```

    ```
    响应Body参数：
    {
        "token": {
            "expires_at": "2020-01-05T05:05:17.429000Z",
            "methods": [
                "assume_role"
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
                }
            ],
            "domain": {
                "id": "d78cbac186b744899480f25bd022f468",
                "name": "IAMDomainA"
            },
            "roles": [
                {
                    "id": "0",
                    "name": "op_gated_eip_ipv6"
                },
                {
                    "id": "0",
                    "name": "op_gated_rds_mcs"
                }
            ],
            "issued_at": "2020-01-04T05:05:17.429000Z",
            "user": {
                "domain": {
                    "id": "d78cbac186b744899480f25bd022f468",
                    "name": "IAMDomainA"
                },
                "id": "0760a9e2a60026664f1fc0031f9f205e",
                "name": "IAMDomainA/IAMAgency"
            },
            "assumed_by": {
                "user": {
                    "domain": {
                        "id": "a2cd82a33fb043dc9304bf72a0f38f00",
                        "name": "IAMDomainB"
                    },
                    "id": "0760a0bdee8026601f44c006524b17a9",
                    "name": "IAMUserB",
                    "password_expires_at": ""
                }
            }
        }
    }
    ```

-   示例 2

    ```
    响应Header参数：
    X-Subject-Token:MIIatAYJKoZIhvcNAQcCoIIapTCCGqECAQExDTALB...
    ```

    ```
    响应Body参数：
    {
        "token": {
            "expires_at": "2020-01-05T06:49:28.094000Z",
            "methods": [
                "assume_role"
            ],
            "catalog": [],
            "roles": [
                {
                    "id": "0",
                    "name": "op_gated_eip_ipv6"
                },
                {
                    "id": "0",
                    "name": "op_gated_rds_mcs"
                }
            ],
            "project": {
                "domain": {
                    "id": "d78cbac186b744899480f25bd022f468",
                    "name": "IAMDomainA"
                },
                "id": "aa2d97d7e62c4b7da3ffdfc11551f878",
                "name": "cn-north-1"
            },
            "issued_at": "2020-01-04T06:49:28.094000Z",
            "user": {
                "domain": {
                    "id": "d78cbac186b744899480f25bd022f468",
                    "name": "IAMDomainA"
                },
                "id": "0760a9e2a60026664f1fc0031f9f205e",
                "name": "IAMDomainA/IAMAgency"
            },
            "assumed_by": {
                "user": {
                    "domain": {
                        "id": "a2cd82a33fb043dc9304bf72a0f38f00",
                        "name": "IAMDomainB"
                    },
                    "id": "0760a0bdee8026601f44c006524b17a9",
                    "name": "IAMUserB",
                    "password_expires_at": ""
                }
            }
        }
    }
    ```


**状态码为 400 时:**

参数无效。

```
{
    "error": {
        "code": 400,
        "message": "The request body is invalid",
        "title": "Bad Request"
    }
}
```

**状态码为 401 时:**

认证失败。

```
{
    "error": {
        "code": 401,
        "message": "The X-Auth-Token is invalid!",
        "title": "Unauthorized"
    }
}
```

**状态码为 403 时:**

没有操作权限。

-   可能原因：被委托方B中用户B的用户token（即X-Auth-Token填写的token）缺少Agent Operator权限，请添加权限。

```
{
    "error": {
        "code": 403,
        "message": "You have no right to do this action",
        "title": "Forbidden"
    }
}
```

## 返回值<a name="zh-cn_topic_0221482426_section233216732016"></a>

<a name="zh-cn_topic_0221482426_table2419"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482426_row13706715203"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482426_p153331578202"><a name="zh-cn_topic_0221482426_p153331578202"></a><a name="zh-cn_topic_0221482426_p153331578202"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482426_p17333117112018"><a name="zh-cn_topic_0221482426_p17333117112018"></a><a name="zh-cn_topic_0221482426_p17333117112018"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482426_row07018762019"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482426_p163331677200"><a name="zh-cn_topic_0221482426_p163331677200"></a><a name="zh-cn_topic_0221482426_p163331677200"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482426_p1333315711208"><a name="zh-cn_topic_0221482426_p1333315711208"></a><a name="zh-cn_topic_0221482426_p1333315711208"></a>创建成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row27047142012"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482426_p4333117102015"><a name="zh-cn_topic_0221482426_p4333117102015"></a><a name="zh-cn_topic_0221482426_p4333117102015"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482426_p13332711202"><a name="zh-cn_topic_0221482426_p13332711202"></a><a name="zh-cn_topic_0221482426_p13332711202"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row87012716205"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482426_p183331476209"><a name="zh-cn_topic_0221482426_p183331476209"></a><a name="zh-cn_topic_0221482426_p183331476209"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482426_p173336752015"><a name="zh-cn_topic_0221482426_p173336752015"></a><a name="zh-cn_topic_0221482426_p173336752015"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row9701377204"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482426_p153330713202"><a name="zh-cn_topic_0221482426_p153330713202"></a><a name="zh-cn_topic_0221482426_p153330713202"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482426_p53337772010"><a name="zh-cn_topic_0221482426_p53337772010"></a><a name="zh-cn_topic_0221482426_p53337772010"></a>没有操作权限。</p>
<p id="zh-cn_topic_0221482426_p45581399511"><a name="zh-cn_topic_0221482426_p45581399511"></a><a name="zh-cn_topic_0221482426_p45581399511"></a>可能原因：被委托方B中用户B的用户token（即X-Auth-Token填写的token）缺少Agent Operator权限，请添加权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row67012752019"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482426_p1933312772015"><a name="zh-cn_topic_0221482426_p1933312772015"></a><a name="zh-cn_topic_0221482426_p1933312772015"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482426_p16333207102017"><a name="zh-cn_topic_0221482426_p16333207102017"></a><a name="zh-cn_topic_0221482426_p16333207102017"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row117013717202"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482426_p233315710204"><a name="zh-cn_topic_0221482426_p233315710204"></a><a name="zh-cn_topic_0221482426_p233315710204"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482426_p1933319717206"><a name="zh-cn_topic_0221482426_p1933319717206"></a><a name="zh-cn_topic_0221482426_p1933319717206"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482426_row870187132012"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482426_p1633377202013"><a name="zh-cn_topic_0221482426_p1633377202013"></a><a name="zh-cn_topic_0221482426_p1633377202013"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482426_p13330717200"><a name="zh-cn_topic_0221482426_p13330717200"></a><a name="zh-cn_topic_0221482426_p13330717200"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482426_section3333167152016"></a>

无

