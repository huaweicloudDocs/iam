# 管理员查询IAM用户列表<a name="zh-cn_topic_0057845638"></a>

## 功能介绍<a name="zh-cn_topic_0221482398_section127721037132313"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/zh-cn_topic_0079496985.html)查询IAM用户列表。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="zh-cn_topic_0221482398_section1774173742315"></a>

GET /v3/users

**表 1**  Query参数

<a name="zh-cn_topic_0221482398_table27761437102313"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482398_row16775173772310"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482398_p4776113732311"><a name="zh-cn_topic_0221482398_p4776113732311"></a><a name="zh-cn_topic_0221482398_p4776113732311"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482398_p277612375231"><a name="zh-cn_topic_0221482398_p277612375231"></a><a name="zh-cn_topic_0221482398_p277612375231"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482398_p277723762313"><a name="zh-cn_topic_0221482398_p277723762313"></a><a name="zh-cn_topic_0221482398_p277723762313"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482398_p16778143752314"><a name="zh-cn_topic_0221482398_p16778143752314"></a><a name="zh-cn_topic_0221482398_p16778143752314"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482398_row277523722317"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482398_p1477820374238"><a name="zh-cn_topic_0221482398_p1477820374238"></a><a name="zh-cn_topic_0221482398_p1477820374238"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482398_p27793373234"><a name="zh-cn_topic_0221482398_p27793373234"></a><a name="zh-cn_topic_0221482398_p27793373234"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482398_p147791837122317"><a name="zh-cn_topic_0221482398_p147791837122317"></a><a name="zh-cn_topic_0221482398_p147791837122317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482398_p37808376233"><a name="zh-cn_topic_0221482398_p37808376233"></a><a name="zh-cn_topic_0221482398_p37808376233"></a>IAM用户所属账号ID，获取方式请参见：<a href="获取IAM用户-项目-用户组-委托的名称和ID.md">获取IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row1377523718232"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482398_p14780163732317"><a name="zh-cn_topic_0221482398_p14780163732317"></a><a name="zh-cn_topic_0221482398_p14780163732317"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482398_p12781437182318"><a name="zh-cn_topic_0221482398_p12781437182318"></a><a name="zh-cn_topic_0221482398_p12781437182318"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482398_p7781183717239"><a name="zh-cn_topic_0221482398_p7781183717239"></a><a name="zh-cn_topic_0221482398_p7781183717239"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482398_p1378219377234"><a name="zh-cn_topic_0221482398_p1378219377234"></a><a name="zh-cn_topic_0221482398_p1378219377234"></a>是否启IAM用户，true为启用，false为停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row17775237112311"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482398_p12782137162320"><a name="zh-cn_topic_0221482398_p12782137162320"></a><a name="zh-cn_topic_0221482398_p12782137162320"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482398_p778310371231"><a name="zh-cn_topic_0221482398_p778310371231"></a><a name="zh-cn_topic_0221482398_p778310371231"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482398_p8783133702317"><a name="zh-cn_topic_0221482398_p8783133702317"></a><a name="zh-cn_topic_0221482398_p8783133702317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482398_p17841137172311"><a name="zh-cn_topic_0221482398_p17841137172311"></a><a name="zh-cn_topic_0221482398_p17841137172311"></a>IAM用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row6775937102317"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482398_p47841837112312"><a name="zh-cn_topic_0221482398_p47841837112312"></a><a name="zh-cn_topic_0221482398_p47841837112312"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482398_p1978503722315"><a name="zh-cn_topic_0221482398_p1978503722315"></a><a name="zh-cn_topic_0221482398_p1978503722315"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482398_p7785163715233"><a name="zh-cn_topic_0221482398_p7785163715233"></a><a name="zh-cn_topic_0221482398_p7785163715233"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482398_p678633772314"><a name="zh-cn_topic_0221482398_p678633772314"></a><a name="zh-cn_topic_0221482398_p678633772314"></a>密码过期时间，格式为：password_expires_at={operator}:{timestamp}。timestamp格式为：YYYY-MM-DDTHH:mm:ssZ。示例：</p>
<pre class="screen" id="zh-cn_topic_0221482398_screen147861737112310"><a name="zh-cn_topic_0221482398_screen147861737112310"></a><a name="zh-cn_topic_0221482398_screen147861737112310"></a>password_expires_at=lt:2016-12-08T22:02:00Z</pre>
<div class="note" id="zh-cn_topic_0221482398_note1178883792312"><a name="zh-cn_topic_0221482398_note1178883792312"></a><a name="zh-cn_topic_0221482398_note1178883792312"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0221482398_ul5789237102314"></a><a name="zh-cn_topic_0221482398_ul5789237102314"></a><ul id="zh-cn_topic_0221482398_ul5789237102314"><li>operator取值范围：lt，lte，gt，gte，eq，neq。</li><li>lt：过期时间小于timestamp。</li><li>lte：过期时间小于等于timestamp。</li><li>gt：过期时间大于timestamp。</li><li>gte：过期时间大于等于timestamp。</li><li>eq：过期时间等于timestamp。</li><li>neq：过期时间不等于timestamp。</li></ul>
</div></div>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482398_section187931337202311"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482398_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482398_row107931837202315"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482398_p879453714236"><a name="zh-cn_topic_0221482398_p879453714236"></a><a name="zh-cn_topic_0221482398_p879453714236"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482398_p779503716239"><a name="zh-cn_topic_0221482398_p779503716239"></a><a name="zh-cn_topic_0221482398_p779503716239"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482398_p1479516371235"><a name="zh-cn_topic_0221482398_p1479516371235"></a><a name="zh-cn_topic_0221482398_p1479516371235"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482398_p147968377236"><a name="zh-cn_topic_0221482398_p147968377236"></a><a name="zh-cn_topic_0221482398_p147968377236"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482398_row16793737182311"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482398_p3796183712316"><a name="zh-cn_topic_0221482398_p3796183712316"></a><a name="zh-cn_topic_0221482398_p3796183712316"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482398_p14797123712317"><a name="zh-cn_topic_0221482398_p14797123712317"></a><a name="zh-cn_topic_0221482398_p14797123712317"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482398_p177971337172319"><a name="zh-cn_topic_0221482398_p177971337172319"></a><a name="zh-cn_topic_0221482398_p177971337172319"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482398_p17985371236"><a name="zh-cn_topic_0221482398_p17985371236"></a><a name="zh-cn_topic_0221482398_p17985371236"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row1479393722320"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482398_p167983379235"><a name="zh-cn_topic_0221482398_p167983379235"></a><a name="zh-cn_topic_0221482398_p167983379235"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482398_p13799183742319"><a name="zh-cn_topic_0221482398_p13799183742319"></a><a name="zh-cn_topic_0221482398_p13799183742319"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482398_p479963792318"><a name="zh-cn_topic_0221482398_p479963792318"></a><a name="zh-cn_topic_0221482398_p479963792318"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482398_p4800133742320"><a name="zh-cn_topic_0221482398_p4800133742320"></a><a name="zh-cn_topic_0221482398_p4800133742320"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482398_section128011537162317"></a>

**表 3**  响应Body参数

<a name="zh-cn_topic_0221482398_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482398_row1780153792319"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482398_p178021137152312"><a name="zh-cn_topic_0221482398_p178021137152312"></a><a name="zh-cn_topic_0221482398_p178021137152312"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482398_p5803637182314"><a name="zh-cn_topic_0221482398_p5803637182314"></a><a name="zh-cn_topic_0221482398_p5803637182314"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482398_p17803153715231"><a name="zh-cn_topic_0221482398_p17803153715231"></a><a name="zh-cn_topic_0221482398_p17803153715231"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482398_row4801193717235"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p18041737162311"><a name="zh-cn_topic_0221482398_p18041737162311"></a><a name="zh-cn_topic_0221482398_p18041737162311"></a><a href="#zh-cn_topic_0221482398_response_Rs81Links">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p14804173782320"><a name="zh-cn_topic_0221482398_p14804173782320"></a><a name="zh-cn_topic_0221482398_p14804173782320"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p12805137122316"><a name="zh-cn_topic_0221482398_p12805137122316"></a><a name="zh-cn_topic_0221482398_p12805137122316"></a>资源链接信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row1180213712310"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p4805153719239"><a name="zh-cn_topic_0221482398_p4805153719239"></a><a name="zh-cn_topic_0221482398_p4805153719239"></a><a href="#zh-cn_topic_0221482398_response_Rs81UsersArritem">users</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p1780653742313"><a name="zh-cn_topic_0221482398_p1780653742313"></a><a name="zh-cn_topic_0221482398_p1780653742313"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p280793719233"><a name="zh-cn_topic_0221482398_p280793719233"></a><a name="zh-cn_topic_0221482398_p280793719233"></a>IAM用户信息列表。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  links

<a name="zh-cn_topic_0221482398_response_Rs81Links"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482398_row18807193714239"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482398_p148089371239"><a name="zh-cn_topic_0221482398_p148089371239"></a><a name="zh-cn_topic_0221482398_p148089371239"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482398_p2080983716236"><a name="zh-cn_topic_0221482398_p2080983716236"></a><a name="zh-cn_topic_0221482398_p2080983716236"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482398_p480943772314"><a name="zh-cn_topic_0221482398_p480943772314"></a><a name="zh-cn_topic_0221482398_p480943772314"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482398_row6807637192312"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p081013711230"><a name="zh-cn_topic_0221482398_p081013711230"></a><a name="zh-cn_topic_0221482398_p081013711230"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p1081083715239"><a name="zh-cn_topic_0221482398_p1081083715239"></a><a name="zh-cn_topic_0221482398_p1081083715239"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p881110371233"><a name="zh-cn_topic_0221482398_p881110371233"></a><a name="zh-cn_topic_0221482398_p881110371233"></a>资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row20807837132317"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p188110372231"><a name="zh-cn_topic_0221482398_p188110372231"></a><a name="zh-cn_topic_0221482398_p188110372231"></a>previous</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p681273713232"><a name="zh-cn_topic_0221482398_p681273713232"></a><a name="zh-cn_topic_0221482398_p681273713232"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p381253702312"><a name="zh-cn_topic_0221482398_p381253702312"></a><a name="zh-cn_topic_0221482398_p381253702312"></a>前一邻接资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row98071837182319"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p5813173772313"><a name="zh-cn_topic_0221482398_p5813173772313"></a><a name="zh-cn_topic_0221482398_p5813173772313"></a>next</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p138131737182317"><a name="zh-cn_topic_0221482398_p138131737182317"></a><a name="zh-cn_topic_0221482398_p138131737182317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p48141337112314"><a name="zh-cn_topic_0221482398_p48141337112314"></a><a name="zh-cn_topic_0221482398_p48141337112314"></a>后一邻接资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  users

<a name="zh-cn_topic_0221482398_response_Rs81UsersArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482398_row38141637162316"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482398_p481523782319"><a name="zh-cn_topic_0221482398_p481523782319"></a><a name="zh-cn_topic_0221482398_p481523782319"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482398_p981653732320"><a name="zh-cn_topic_0221482398_p981653732320"></a><a name="zh-cn_topic_0221482398_p981653732320"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482398_p1481603752310"><a name="zh-cn_topic_0221482398_p1481603752310"></a><a name="zh-cn_topic_0221482398_p1481603752310"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482398_row15814037142320"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p13817163711235"><a name="zh-cn_topic_0221482398_p13817163711235"></a><a name="zh-cn_topic_0221482398_p13817163711235"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p17817103712315"><a name="zh-cn_topic_0221482398_p17817103712315"></a><a name="zh-cn_topic_0221482398_p17817103712315"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p8818123720239"><a name="zh-cn_topic_0221482398_p8818123720239"></a><a name="zh-cn_topic_0221482398_p8818123720239"></a>IAM用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row981553732312"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p108183373231"><a name="zh-cn_topic_0221482398_p108183373231"></a><a name="zh-cn_topic_0221482398_p108183373231"></a><a href="#zh-cn_topic_0221482398_response_Rs81UsersArritemLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p281916372234"><a name="zh-cn_topic_0221482398_p281916372234"></a><a name="zh-cn_topic_0221482398_p281916372234"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p2082073722310"><a name="zh-cn_topic_0221482398_p2082073722310"></a><a name="zh-cn_topic_0221482398_p2082073722310"></a>IAM用户的资源链接信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row78158371239"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p68201372236"><a name="zh-cn_topic_0221482398_p68201372236"></a><a name="zh-cn_topic_0221482398_p68201372236"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p1882193722319"><a name="zh-cn_topic_0221482398_p1882193722319"></a><a name="zh-cn_topic_0221482398_p1882193722319"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p13821183742310"><a name="zh-cn_topic_0221482398_p13821183742310"></a><a name="zh-cn_topic_0221482398_p13821183742310"></a>IAM用户所属账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row128155372232"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p1382213377238"><a name="zh-cn_topic_0221482398_p1382213377238"></a><a name="zh-cn_topic_0221482398_p1382213377238"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p08221637202317"><a name="zh-cn_topic_0221482398_p08221637202317"></a><a name="zh-cn_topic_0221482398_p08221637202317"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p1682212372236"><a name="zh-cn_topic_0221482398_p1682212372236"></a><a name="zh-cn_topic_0221482398_p1682212372236"></a>IAM用户是否启用。true表示启用，false表示停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row7815153710231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p178231937142316"><a name="zh-cn_topic_0221482398_p178231937142316"></a><a name="zh-cn_topic_0221482398_p178231937142316"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p9823737152311"><a name="zh-cn_topic_0221482398_p9823737152311"></a><a name="zh-cn_topic_0221482398_p9823737152311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p1782413752310"><a name="zh-cn_topic_0221482398_p1782413752310"></a><a name="zh-cn_topic_0221482398_p1782413752310"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row15815163772316"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p17824137132312"><a name="zh-cn_topic_0221482398_p17824137132312"></a><a name="zh-cn_topic_0221482398_p17824137132312"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p2082520377235"><a name="zh-cn_topic_0221482398_p2082520377235"></a><a name="zh-cn_topic_0221482398_p2082520377235"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p382514371233"><a name="zh-cn_topic_0221482398_p382514371233"></a><a name="zh-cn_topic_0221482398_p382514371233"></a>IAM用户密码过期时间（UTC时间），“null”表示密码不过期。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row681518372231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p138261437152313"><a name="zh-cn_topic_0221482398_p138261437152313"></a><a name="zh-cn_topic_0221482398_p138261437152313"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p1682673732311"><a name="zh-cn_topic_0221482398_p1682673732311"></a><a name="zh-cn_topic_0221482398_p1682673732311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p4827183722313"><a name="zh-cn_topic_0221482398_p4827183722313"></a><a name="zh-cn_topic_0221482398_p4827183722313"></a>IAM用户描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row48151378231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p48270374232"><a name="zh-cn_topic_0221482398_p48270374232"></a><a name="zh-cn_topic_0221482398_p48270374232"></a>pwd_status</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p1482816373238"><a name="zh-cn_topic_0221482398_p1482816373238"></a><a name="zh-cn_topic_0221482398_p1482816373238"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p20828637152313"><a name="zh-cn_topic_0221482398_p20828637152313"></a><a name="zh-cn_topic_0221482398_p20828637152313"></a>IAM用户密码状态。true：需要修改密码，false：正常。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row14815937122312"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p38291137132310"><a name="zh-cn_topic_0221482398_p38291137132310"></a><a name="zh-cn_topic_0221482398_p38291137132310"></a>forceResetPwd</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p1982933712238"><a name="zh-cn_topic_0221482398_p1982933712238"></a><a name="zh-cn_topic_0221482398_p1982933712238"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p13830837132313"><a name="zh-cn_topic_0221482398_p13830837132313"></a><a name="zh-cn_topic_0221482398_p13830837132313"></a>IAM用户下次登录是否强制重置密码。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row9815137142316"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p1483012373235"><a name="zh-cn_topic_0221482398_p1483012373235"></a><a name="zh-cn_topic_0221482398_p1483012373235"></a>default_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p18317374238"><a name="zh-cn_topic_0221482398_p18317374238"></a><a name="zh-cn_topic_0221482398_p18317374238"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p118312037112314"><a name="zh-cn_topic_0221482398_p118312037112314"></a><a name="zh-cn_topic_0221482398_p118312037112314"></a>IAM用户登录控制台后默认跳转的项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row481517375231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p1583223714236"><a name="zh-cn_topic_0221482398_p1583223714236"></a><a name="zh-cn_topic_0221482398_p1583223714236"></a>last_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p1832163711231"><a name="zh-cn_topic_0221482398_p1832163711231"></a><a name="zh-cn_topic_0221482398_p1832163711231"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p98331037202314"><a name="zh-cn_topic_0221482398_p98331037202314"></a><a name="zh-cn_topic_0221482398_p98331037202314"></a>IAM用户退出系统前，在控制台最后访问的项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row1881543717237"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p483315379236"><a name="zh-cn_topic_0221482398_p483315379236"></a><a name="zh-cn_topic_0221482398_p483315379236"></a>pwd_strength</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p14834143716231"><a name="zh-cn_topic_0221482398_p14834143716231"></a><a name="zh-cn_topic_0221482398_p14834143716231"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p6834337102318"><a name="zh-cn_topic_0221482398_p6834337102318"></a><a name="zh-cn_topic_0221482398_p6834337102318"></a>IAM用户的密码强度。high：密码强度高；mid：密码强度中等；low：密码强度低。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  users.links

<a name="zh-cn_topic_0221482398_response_Rs81UsersArritemLinks"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482398_row1383511378238"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482398_p14836133716232"><a name="zh-cn_topic_0221482398_p14836133716232"></a><a name="zh-cn_topic_0221482398_p14836133716232"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482398_p1383615371231"><a name="zh-cn_topic_0221482398_p1383615371231"></a><a name="zh-cn_topic_0221482398_p1383615371231"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482398_p1483733719234"><a name="zh-cn_topic_0221482398_p1483733719234"></a><a name="zh-cn_topic_0221482398_p1483733719234"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482398_row19835193720231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p2837337172316"><a name="zh-cn_topic_0221482398_p2837337172316"></a><a name="zh-cn_topic_0221482398_p2837337172316"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p683893712312"><a name="zh-cn_topic_0221482398_p683893712312"></a><a name="zh-cn_topic_0221482398_p683893712312"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p1783893712230"><a name="zh-cn_topic_0221482398_p1783893712230"></a><a name="zh-cn_topic_0221482398_p1783893712230"></a>资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row1283553752320"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p11839737142318"><a name="zh-cn_topic_0221482398_p11839737142318"></a><a name="zh-cn_topic_0221482398_p11839737142318"></a>previous</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p1883963715230"><a name="zh-cn_topic_0221482398_p1883963715230"></a><a name="zh-cn_topic_0221482398_p1883963715230"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p1084073722317"><a name="zh-cn_topic_0221482398_p1084073722317"></a><a name="zh-cn_topic_0221482398_p1084073722317"></a>前一邻接资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row4835103711239"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482398_p7840113713238"><a name="zh-cn_topic_0221482398_p7840113713238"></a><a name="zh-cn_topic_0221482398_p7840113713238"></a>next</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p3841163742314"><a name="zh-cn_topic_0221482398_p3841163742314"></a><a name="zh-cn_topic_0221482398_p3841163742314"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482398_p1384173762315"><a name="zh-cn_topic_0221482398_p1384173762315"></a><a name="zh-cn_topic_0221482398_p1384173762315"></a>后一邻接资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482398_section138421337152310"></a>

```
GET https://iam.myhuaweicloud.com/v3/users
```

## 响应示例<a name="zh-cn_topic_0221482398_section10843173717237"></a>

**状态码为 200 时:**

请求成功。

```
{
    "links": {
        "next": null,
        "previous": null,
        "self": "https://iam.huaweicloud.com/v3/users"
    },
    "users": [
        {
            "domain_id": "d78cbac186b744899480f25bd022f468",
            "default_project_id": "",
            "name": "IAMUserA",
            "description": "IAMDescriptionA",
            "password_expires_at": null,
            "links": {
                "next": null,
                "previous": null,
                "self": "https://iam.huaweicloud.com/v3/users/07667db96a00265f1fc0c003a3b1c6cd"
            },
            "id": "07667db96a00265f1fc0c003a3b1c6cd",
            "enabled": true
        },
        {
            "pwd_status": true,
            "domain_id": "d78cbac186b744899480f25bd022f468",
            "last_project_id": "065a7c66da0010992ff7c0031e5a5e7d",
            "forceResetPwd": false,
            "name": "IAMUserB",
            "description": "IAMDescriptionB",
            "password_expires_at": null,
            "links": {
                "next": null,
                "previous": null,
                "self": "https://iam.huaweicloud.com/v3/users/07609fb9358010e21f7bc003751c7c32"
            },
            "id": "07609fb9358010e21f7bc003751c7c32",
            "enabled": true
        }
    ]
}
```

## 返回值<a name="zh-cn_topic_0221482398_section185803712236"></a>

<a name="zh-cn_topic_0221482398_table2443"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482398_row6859123720233"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482398_p19859153742319"><a name="zh-cn_topic_0221482398_p19859153742319"></a><a name="zh-cn_topic_0221482398_p19859153742319"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482398_p13860143710231"><a name="zh-cn_topic_0221482398_p13860143710231"></a><a name="zh-cn_topic_0221482398_p13860143710231"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482398_row188591837142316"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482398_p586019374237"><a name="zh-cn_topic_0221482398_p586019374237"></a><a name="zh-cn_topic_0221482398_p586019374237"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482398_p686153718235"><a name="zh-cn_topic_0221482398_p686153718235"></a><a name="zh-cn_topic_0221482398_p686153718235"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row8859737142319"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482398_p118611137192319"><a name="zh-cn_topic_0221482398_p118611137192319"></a><a name="zh-cn_topic_0221482398_p118611137192319"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482398_p48621937122310"><a name="zh-cn_topic_0221482398_p48621937122310"></a><a name="zh-cn_topic_0221482398_p48621937122310"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row15859133772313"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482398_p186213716234"><a name="zh-cn_topic_0221482398_p186213716234"></a><a name="zh-cn_topic_0221482398_p186213716234"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482398_p5863193718232"><a name="zh-cn_topic_0221482398_p5863193718232"></a><a name="zh-cn_topic_0221482398_p5863193718232"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row13859837172310"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482398_p1686310372236"><a name="zh-cn_topic_0221482398_p1686310372236"></a><a name="zh-cn_topic_0221482398_p1686310372236"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482398_p486433716235"><a name="zh-cn_topic_0221482398_p486433716235"></a><a name="zh-cn_topic_0221482398_p486433716235"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row585973718236"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482398_p1086418371235"><a name="zh-cn_topic_0221482398_p1086418371235"></a><a name="zh-cn_topic_0221482398_p1086418371235"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482398_p68659377235"><a name="zh-cn_topic_0221482398_p68659377235"></a><a name="zh-cn_topic_0221482398_p68659377235"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row38598374234"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482398_p0865133718239"><a name="zh-cn_topic_0221482398_p0865133718239"></a><a name="zh-cn_topic_0221482398_p0865133718239"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482398_p1886614375230"><a name="zh-cn_topic_0221482398_p1886614375230"></a><a name="zh-cn_topic_0221482398_p1886614375230"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row3859173720235"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482398_p68661437122312"><a name="zh-cn_topic_0221482398_p68661437122312"></a><a name="zh-cn_topic_0221482398_p68661437122312"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482398_p78671137182313"><a name="zh-cn_topic_0221482398_p78671137182313"></a><a name="zh-cn_topic_0221482398_p78671137182313"></a>资源冲突。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row19859537102313"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482398_p78673372234"><a name="zh-cn_topic_0221482398_p78673372234"></a><a name="zh-cn_topic_0221482398_p78673372234"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482398_p128681837112311"><a name="zh-cn_topic_0221482398_p128681837112311"></a><a name="zh-cn_topic_0221482398_p128681837112311"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482398_row11859637192317"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482398_p16868193722317"><a name="zh-cn_topic_0221482398_p16868193722317"></a><a name="zh-cn_topic_0221482398_p16868193722317"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482398_p2869123716231"><a name="zh-cn_topic_0221482398_p2869123716231"></a><a name="zh-cn_topic_0221482398_p2869123716231"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482398_section11869143713235"></a>

无

