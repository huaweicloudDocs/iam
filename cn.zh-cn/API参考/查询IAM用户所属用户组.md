# 查询IAM用户所属用户组<a name="iam_08_0004"></a>

## 功能介绍<a name="zh-cn_topic_0221482366_section17731164910257"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)查询IAM用户所属用户组，或IAM用户查询自己所属用户组。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section99983300597"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneListGroupsForUser)中调试该接口。

## URI<a name="zh-cn_topic_0221482366_section13732249132519"></a>

GET /v3/users/\{user\_id\}/groups

**表 1**  路径参数

<a name="zh-cn_topic_0221482366_table57340497253"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482366_row2734134922516"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482366_p7735749162511"><a name="zh-cn_topic_0221482366_p7735749162511"></a><a name="zh-cn_topic_0221482366_p7735749162511"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482366_p5735104982514"><a name="zh-cn_topic_0221482366_p5735104982514"></a><a name="zh-cn_topic_0221482366_p5735104982514"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482366_p16736649122515"><a name="zh-cn_topic_0221482366_p16736649122515"></a><a name="zh-cn_topic_0221482366_p16736649122515"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482366_p27362049122516"><a name="zh-cn_topic_0221482366_p27362049122516"></a><a name="zh-cn_topic_0221482366_p27362049122516"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482366_row12734104972516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482366_p12737134913251"><a name="zh-cn_topic_0221482366_p12737134913251"></a><a name="zh-cn_topic_0221482366_p12737134913251"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482366_p127379493257"><a name="zh-cn_topic_0221482366_p127379493257"></a><a name="zh-cn_topic_0221482366_p127379493257"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482366_p573810498256"><a name="zh-cn_topic_0221482366_p573810498256"></a><a name="zh-cn_topic_0221482366_p573810498256"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482366_p4739184912254"><a name="zh-cn_topic_0221482366_p4739184912254"></a><a name="zh-cn_topic_0221482366_p4739184912254"></a>待查询的IAM用户ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482366_section1873910496259"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482366_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482366_row974054918253"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482366_p37411849102515"><a name="zh-cn_topic_0221482366_p37411849102515"></a><a name="zh-cn_topic_0221482366_p37411849102515"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482366_p14742144942520"><a name="zh-cn_topic_0221482366_p14742144942520"></a><a name="zh-cn_topic_0221482366_p14742144942520"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482366_p177421496250"><a name="zh-cn_topic_0221482366_p177421496250"></a><a name="zh-cn_topic_0221482366_p177421496250"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482366_p174314916259"><a name="zh-cn_topic_0221482366_p174314916259"></a><a name="zh-cn_topic_0221482366_p174314916259"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482366_row9740134962512"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482366_p0743349142513"><a name="zh-cn_topic_0221482366_p0743349142513"></a><a name="zh-cn_topic_0221482366_p0743349142513"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482366_p1746949102512"><a name="zh-cn_topic_0221482366_p1746949102512"></a><a name="zh-cn_topic_0221482366_p1746949102512"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482366_p274714917259"><a name="zh-cn_topic_0221482366_p274714917259"></a><a name="zh-cn_topic_0221482366_p274714917259"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482366_p1074710498259"><a name="zh-cn_topic_0221482366_p1074710498259"></a><a name="zh-cn_topic_0221482366_p1074710498259"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row11740154913258"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482366_p197485497255"><a name="zh-cn_topic_0221482366_p197485497255"></a><a name="zh-cn_topic_0221482366_p197485497255"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482366_p174824918256"><a name="zh-cn_topic_0221482366_p174824918256"></a><a name="zh-cn_topic_0221482366_p174824918256"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482366_p674913491259"><a name="zh-cn_topic_0221482366_p674913491259"></a><a name="zh-cn_topic_0221482366_p674913491259"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482366_p1974915495256"><a name="zh-cn_topic_0221482366_p1974915495256"></a><a name="zh-cn_topic_0221482366_p1974915495256"></a><a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询IAM用户所属用户组：拥有Security Administrator权限的token。</p>
<p id="zh-cn_topic_0221482366_p1575064992513"><a name="zh-cn_topic_0221482366_p1575064992513"></a><a name="zh-cn_topic_0221482366_p1575064992513"></a>IAM用户查询自己所属用户组：URL中user_id所对应IAM用户的token（无需特殊权限）。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482366_section177501849192512"></a>

**表 3**  响应Body参数

<a name="zh-cn_topic_0221482366_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482366_row1875184911256"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482366_p157531949182511"><a name="zh-cn_topic_0221482366_p157531949182511"></a><a name="zh-cn_topic_0221482366_p157531949182511"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482366_p775324902517"><a name="zh-cn_topic_0221482366_p775324902517"></a><a name="zh-cn_topic_0221482366_p775324902517"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482366_p1775414962517"><a name="zh-cn_topic_0221482366_p1775414962517"></a><a name="zh-cn_topic_0221482366_p1775414962517"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482366_row275294919256"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p16755449142516"><a name="zh-cn_topic_0221482366_p16755449142516"></a><a name="zh-cn_topic_0221482366_p16755449142516"></a><a href="#zh-cn_topic_0221482366_response_Rs84GroupsArritem">groups</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p1755349162519"><a name="zh-cn_topic_0221482366_p1755349162519"></a><a name="zh-cn_topic_0221482366_p1755349162519"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p775674918258"><a name="zh-cn_topic_0221482366_p775674918258"></a><a name="zh-cn_topic_0221482366_p775674918258"></a>用户组信息列表。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row17521049192514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p475774912255"><a name="zh-cn_topic_0221482366_p475774912255"></a><a name="zh-cn_topic_0221482366_p475774912255"></a><a href="#zh-cn_topic_0221482366_response_Rs84Links">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p2759104912252"><a name="zh-cn_topic_0221482366_p2759104912252"></a><a name="zh-cn_topic_0221482366_p2759104912252"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p15759749112513"><a name="zh-cn_topic_0221482366_p15759749112513"></a><a name="zh-cn_topic_0221482366_p15759749112513"></a>资源链接信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  groups

<a name="zh-cn_topic_0221482366_response_Rs84GroupsArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482366_row476124902510"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482366_p1576294952519"><a name="zh-cn_topic_0221482366_p1576294952519"></a><a name="zh-cn_topic_0221482366_p1576294952519"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482366_p16763194972513"><a name="zh-cn_topic_0221482366_p16763194972513"></a><a name="zh-cn_topic_0221482366_p16763194972513"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482366_p2764204915252"><a name="zh-cn_topic_0221482366_p2764204915252"></a><a name="zh-cn_topic_0221482366_p2764204915252"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482366_row1376114917253"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p1776474912510"><a name="zh-cn_topic_0221482366_p1776474912510"></a><a name="zh-cn_topic_0221482366_p1776474912510"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p14765949202514"><a name="zh-cn_topic_0221482366_p14765949202514"></a><a name="zh-cn_topic_0221482366_p14765949202514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p8765194972517"><a name="zh-cn_topic_0221482366_p8765194972517"></a><a name="zh-cn_topic_0221482366_p8765194972517"></a>用户组描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row137611949182510"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p2766154902520"><a name="zh-cn_topic_0221482366_p2766154902520"></a><a name="zh-cn_topic_0221482366_p2766154902520"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p17661496251"><a name="zh-cn_topic_0221482366_p17661496251"></a><a name="zh-cn_topic_0221482366_p17661496251"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p1976712499250"><a name="zh-cn_topic_0221482366_p1976712499250"></a><a name="zh-cn_topic_0221482366_p1976712499250"></a>用户组ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row676110492254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p476718496253"><a name="zh-cn_topic_0221482366_p476718496253"></a><a name="zh-cn_topic_0221482366_p476718496253"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p27682495255"><a name="zh-cn_topic_0221482366_p27682495255"></a><a name="zh-cn_topic_0221482366_p27682495255"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p1776834932510"><a name="zh-cn_topic_0221482366_p1776834932510"></a><a name="zh-cn_topic_0221482366_p1776834932510"></a>用户组所属帐号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row976184912255"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p11769154932510"><a name="zh-cn_topic_0221482366_p11769154932510"></a><a name="zh-cn_topic_0221482366_p11769154932510"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p47698494254"><a name="zh-cn_topic_0221482366_p47698494254"></a><a name="zh-cn_topic_0221482366_p47698494254"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p14770194952518"><a name="zh-cn_topic_0221482366_p14770194952518"></a><a name="zh-cn_topic_0221482366_p14770194952518"></a>用户组名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row1076115491258"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p9770144918258"><a name="zh-cn_topic_0221482366_p9770144918258"></a><a name="zh-cn_topic_0221482366_p9770144918258"></a><a href="#zh-cn_topic_0221482366_response_Rs84GroupsArritemLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p6771649182513"><a name="zh-cn_topic_0221482366_p6771649182513"></a><a name="zh-cn_topic_0221482366_p6771649182513"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p1771184902516"><a name="zh-cn_topic_0221482366_p1771184902516"></a><a name="zh-cn_topic_0221482366_p1771184902516"></a>用户组的资源链接信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row1761174918254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p13772134972515"><a name="zh-cn_topic_0221482366_p13772134972515"></a><a name="zh-cn_topic_0221482366_p13772134972515"></a>create_time</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p117721949182513"><a name="zh-cn_topic_0221482366_p117721949182513"></a><a name="zh-cn_topic_0221482366_p117721949182513"></a><span>Long</span></p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p377316494257"><a name="zh-cn_topic_0221482366_p377316494257"></a><a name="zh-cn_topic_0221482366_p377316494257"></a>用户组创建时间。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  groups.links

<a name="zh-cn_topic_0221482366_response_Rs84GroupsArritemLinks"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482366_row677464972519"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482366_p14775154915254"><a name="zh-cn_topic_0221482366_p14775154915254"></a><a name="zh-cn_topic_0221482366_p14775154915254"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482366_p277613490252"><a name="zh-cn_topic_0221482366_p277613490252"></a><a name="zh-cn_topic_0221482366_p277613490252"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482366_p17776174982511"><a name="zh-cn_topic_0221482366_p17776174982511"></a><a name="zh-cn_topic_0221482366_p17776174982511"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482366_row13774449112514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p877784952514"><a name="zh-cn_topic_0221482366_p877784952514"></a><a name="zh-cn_topic_0221482366_p877784952514"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p19777124912251"><a name="zh-cn_topic_0221482366_p19777124912251"></a><a name="zh-cn_topic_0221482366_p19777124912251"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p6778114918252"><a name="zh-cn_topic_0221482366_p6778114918252"></a><a name="zh-cn_topic_0221482366_p6778114918252"></a>资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row57741049102512"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p377824942516"><a name="zh-cn_topic_0221482366_p377824942516"></a><a name="zh-cn_topic_0221482366_p377824942516"></a>previous</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p0779174911254"><a name="zh-cn_topic_0221482366_p0779174911254"></a><a name="zh-cn_topic_0221482366_p0779174911254"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p1177964972515"><a name="zh-cn_topic_0221482366_p1177964972515"></a><a name="zh-cn_topic_0221482366_p1177964972515"></a>前一邻接资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row57742498252"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p47801497256"><a name="zh-cn_topic_0221482366_p47801497256"></a><a name="zh-cn_topic_0221482366_p47801497256"></a>next</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p4781749112510"><a name="zh-cn_topic_0221482366_p4781749112510"></a><a name="zh-cn_topic_0221482366_p4781749112510"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p1178112494251"><a name="zh-cn_topic_0221482366_p1178112494251"></a><a name="zh-cn_topic_0221482366_p1178112494251"></a>后一邻接资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  links

<a name="zh-cn_topic_0221482366_response_Rs84Links"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482366_row2782144942512"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482366_p1878311498251"><a name="zh-cn_topic_0221482366_p1878311498251"></a><a name="zh-cn_topic_0221482366_p1878311498251"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482366_p17841949102512"><a name="zh-cn_topic_0221482366_p17841949102512"></a><a name="zh-cn_topic_0221482366_p17841949102512"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482366_p4784114917257"><a name="zh-cn_topic_0221482366_p4784114917257"></a><a name="zh-cn_topic_0221482366_p4784114917257"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482366_row2078212496254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p19785134918256"><a name="zh-cn_topic_0221482366_p19785134918256"></a><a name="zh-cn_topic_0221482366_p19785134918256"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p27851449122518"><a name="zh-cn_topic_0221482366_p27851449122518"></a><a name="zh-cn_topic_0221482366_p27851449122518"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p978674962514"><a name="zh-cn_topic_0221482366_p978674962514"></a><a name="zh-cn_topic_0221482366_p978674962514"></a>资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row27822492253"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p378618498252"><a name="zh-cn_topic_0221482366_p378618498252"></a><a name="zh-cn_topic_0221482366_p378618498252"></a>previous</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p9787114918256"><a name="zh-cn_topic_0221482366_p9787114918256"></a><a name="zh-cn_topic_0221482366_p9787114918256"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p878734902516"><a name="zh-cn_topic_0221482366_p878734902516"></a><a name="zh-cn_topic_0221482366_p878734902516"></a>前一邻接资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row37821949142515"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482366_p778844914257"><a name="zh-cn_topic_0221482366_p778844914257"></a><a name="zh-cn_topic_0221482366_p778844914257"></a>next</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482366_p197880493257"><a name="zh-cn_topic_0221482366_p197880493257"></a><a name="zh-cn_topic_0221482366_p197880493257"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482366_p19789174932517"><a name="zh-cn_topic_0221482366_p19789174932517"></a><a name="zh-cn_topic_0221482366_p19789174932517"></a>后一邻接资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482366_section479154914251"></a>

```
GET https://iam.myhuaweicloud.com/v3/users/{user_id}/groups
```

## 响应示例<a name="zh-cn_topic_0221482366_section87938497251"></a>

**状态码为 200 时:**

请求成功。

```
{
    "groups": [
        {
            "domain_id": "d78cbac186b744899480f25bd0...",
            "create_time": 1578107542861,
            "name": "IAMGroup",
            "description": "",
            "links": {
                "next": null,
                "previous": null,
                "self": "https://iam.huaweicloud.com/v3/groups/07609e7eb200250a3f7dc003cb..."
            },
            "id": "07609e7eb200250a3f7dc003cb7..."
        }
    ],
    "links": {
        "next": null,
        "previous": null,
        "self": "https://iam.huaweicloud.com/v3/users/076837351e80251c1f0fc003afe43.../groups"
    }
}
```

## 返回值<a name="zh-cn_topic_0221482366_section1980224912519"></a>

<a name="zh-cn_topic_0221482366_table2452"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482366_row380434911257"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482366_p1380724972513"><a name="zh-cn_topic_0221482366_p1380724972513"></a><a name="zh-cn_topic_0221482366_p1380724972513"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482366_p28081649102519"><a name="zh-cn_topic_0221482366_p28081649102519"></a><a name="zh-cn_topic_0221482366_p28081649102519"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482366_row180512499258"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482366_p28091249152512"><a name="zh-cn_topic_0221482366_p28091249152512"></a><a name="zh-cn_topic_0221482366_p28091249152512"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482366_p881044912512"><a name="zh-cn_topic_0221482366_p881044912512"></a><a name="zh-cn_topic_0221482366_p881044912512"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row08051349182519"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482366_p4810949132520"><a name="zh-cn_topic_0221482366_p4810949132520"></a><a name="zh-cn_topic_0221482366_p4810949132520"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482366_p208112049172518"><a name="zh-cn_topic_0221482366_p208112049172518"></a><a name="zh-cn_topic_0221482366_p208112049172518"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row680514912516"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482366_p1481124962518"><a name="zh-cn_topic_0221482366_p1481124962518"></a><a name="zh-cn_topic_0221482366_p1481124962518"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482366_p19812144917256"><a name="zh-cn_topic_0221482366_p19812144917256"></a><a name="zh-cn_topic_0221482366_p19812144917256"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row580594952515"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482366_p1681217492252"><a name="zh-cn_topic_0221482366_p1681217492252"></a><a name="zh-cn_topic_0221482366_p1681217492252"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482366_p2813149102518"><a name="zh-cn_topic_0221482366_p2813149102518"></a><a name="zh-cn_topic_0221482366_p2813149102518"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row580564915259"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482366_p08132496254"><a name="zh-cn_topic_0221482366_p08132496254"></a><a name="zh-cn_topic_0221482366_p08132496254"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482366_p88143495257"><a name="zh-cn_topic_0221482366_p88143495257"></a><a name="zh-cn_topic_0221482366_p88143495257"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row28052496259"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482366_p128141449172515"><a name="zh-cn_topic_0221482366_p128141449172515"></a><a name="zh-cn_topic_0221482366_p128141449172515"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482366_p148152495258"><a name="zh-cn_topic_0221482366_p148152495258"></a><a name="zh-cn_topic_0221482366_p148152495258"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row1380511499251"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482366_p178161449122512"><a name="zh-cn_topic_0221482366_p178161449122512"></a><a name="zh-cn_topic_0221482366_p178161449122512"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482366_p9816114913253"><a name="zh-cn_topic_0221482366_p9816114913253"></a><a name="zh-cn_topic_0221482366_p9816114913253"></a>资源冲突。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row12805649122518"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482366_p681734982518"><a name="zh-cn_topic_0221482366_p681734982518"></a><a name="zh-cn_topic_0221482366_p681734982518"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482366_p168172049162518"><a name="zh-cn_topic_0221482366_p168172049162518"></a><a name="zh-cn_topic_0221482366_p168172049162518"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482366_row128051649172510"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482366_p1081814962518"><a name="zh-cn_topic_0221482366_p1081814962518"></a><a name="zh-cn_topic_0221482366_p1081814962518"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482366_p148181949112513"><a name="zh-cn_topic_0221482366_p148181949112513"></a><a name="zh-cn_topic_0221482366_p148181949112513"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482366_section168191949172519"></a>

无

