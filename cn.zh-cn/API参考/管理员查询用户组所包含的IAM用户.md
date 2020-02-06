# 管理员查询用户组所包含的IAM用户<a name="zh-cn_topic_0057845561"></a>

## 功能介绍<a name="zh-cn_topic_0221482391_section1388584911254"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/zh-cn_topic_0079496985.html)查询用户组中所包含的IAM用户。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="zh-cn_topic_0221482391_section58874491255"></a>

GET /v3/groups/\{group\_id\}/users

**表 1**  路径参数

<a name="zh-cn_topic_0221482391_table7889549132518"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482391_row10888134912519"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482391_p188891449172516"><a name="zh-cn_topic_0221482391_p188891449172516"></a><a name="zh-cn_topic_0221482391_p188891449172516"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482391_p5890849162518"><a name="zh-cn_topic_0221482391_p5890849162518"></a><a name="zh-cn_topic_0221482391_p5890849162518"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482391_p489010496257"><a name="zh-cn_topic_0221482391_p489010496257"></a><a name="zh-cn_topic_0221482391_p489010496257"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482391_p14891194912514"><a name="zh-cn_topic_0221482391_p14891194912514"></a><a name="zh-cn_topic_0221482391_p14891194912514"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482391_row178881549102512"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482391_p389119499258"><a name="zh-cn_topic_0221482391_p389119499258"></a><a name="zh-cn_topic_0221482391_p389119499258"></a>group_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482391_p0892749102510"><a name="zh-cn_topic_0221482391_p0892749102510"></a><a name="zh-cn_topic_0221482391_p0892749102510"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482391_p14892124962512"><a name="zh-cn_topic_0221482391_p14892124962512"></a><a name="zh-cn_topic_0221482391_p14892124962512"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482391_p128931249182514"><a name="zh-cn_topic_0221482391_p128931249182514"></a><a name="zh-cn_topic_0221482391_p128931249182514"></a>待查询的用户组ID，获取方式请参见：<a href="获取IAM用户-项目-用户组的名称和ID.md">获取IAM用户、项目、用户组的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482391_section189419499255"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482391_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482391_row10894174913256"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482391_p9896184919251"><a name="zh-cn_topic_0221482391_p9896184919251"></a><a name="zh-cn_topic_0221482391_p9896184919251"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482391_p108968496254"><a name="zh-cn_topic_0221482391_p108968496254"></a><a name="zh-cn_topic_0221482391_p108968496254"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482391_p18897249152520"><a name="zh-cn_topic_0221482391_p18897249152520"></a><a name="zh-cn_topic_0221482391_p18897249152520"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482391_p10897134922514"><a name="zh-cn_topic_0221482391_p10897134922514"></a><a name="zh-cn_topic_0221482391_p10897134922514"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482391_row118951749172516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482391_p1389819490253"><a name="zh-cn_topic_0221482391_p1389819490253"></a><a name="zh-cn_topic_0221482391_p1389819490253"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482391_p1689994917251"><a name="zh-cn_topic_0221482391_p1689994917251"></a><a name="zh-cn_topic_0221482391_p1689994917251"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482391_p789920491251"><a name="zh-cn_topic_0221482391_p789920491251"></a><a name="zh-cn_topic_0221482391_p789920491251"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482391_p17900164972516"><a name="zh-cn_topic_0221482391_p17900164972516"></a><a name="zh-cn_topic_0221482391_p17900164972516"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row8895194912511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482391_p16900749202513"><a name="zh-cn_topic_0221482391_p16900749202513"></a><a name="zh-cn_topic_0221482391_p16900749202513"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482391_p9901134912251"><a name="zh-cn_topic_0221482391_p9901134912251"></a><a name="zh-cn_topic_0221482391_p9901134912251"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482391_p1890144932517"><a name="zh-cn_topic_0221482391_p1890144932517"></a><a name="zh-cn_topic_0221482391_p1890144932517"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482391_p6902449142513"><a name="zh-cn_topic_0221482391_p6902449142513"></a><a name="zh-cn_topic_0221482391_p6902449142513"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482391_section59071049172512"></a>

**表 3**  响应Body参数

<a name="zh-cn_topic_0221482391_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482391_row13908164920252"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482391_p1790984911250"><a name="zh-cn_topic_0221482391_p1790984911250"></a><a name="zh-cn_topic_0221482391_p1790984911250"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482391_p591015498255"><a name="zh-cn_topic_0221482391_p591015498255"></a><a name="zh-cn_topic_0221482391_p591015498255"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482391_p8910154918250"><a name="zh-cn_topic_0221482391_p8910154918250"></a><a name="zh-cn_topic_0221482391_p8910154918250"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482391_row0908154911259"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p191118498253"><a name="zh-cn_topic_0221482391_p191118498253"></a><a name="zh-cn_topic_0221482391_p191118498253"></a><a href="#zh-cn_topic_0221482391_response_Rs85Links">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p7911049122512"><a name="zh-cn_topic_0221482391_p7911049122512"></a><a name="zh-cn_topic_0221482391_p7911049122512"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p7912249112517"><a name="zh-cn_topic_0221482391_p7912249112517"></a><a name="zh-cn_topic_0221482391_p7912249112517"></a>用户组资源的链接。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row1090818498257"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p1191314499254"><a name="zh-cn_topic_0221482391_p1191314499254"></a><a name="zh-cn_topic_0221482391_p1191314499254"></a><a href="#zh-cn_topic_0221482391_response_Rs85UsersArritem">users</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p1491304972519"><a name="zh-cn_topic_0221482391_p1491304972519"></a><a name="zh-cn_topic_0221482391_p1491304972519"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p1591412498253"><a name="zh-cn_topic_0221482391_p1591412498253"></a><a name="zh-cn_topic_0221482391_p1591412498253"></a>IAM用户信息列表。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  links

<a name="zh-cn_topic_0221482391_response_Rs85Links"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482391_row191515496257"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482391_p16919134902516"><a name="zh-cn_topic_0221482391_p16919134902516"></a><a name="zh-cn_topic_0221482391_p16919134902516"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482391_p4920144982511"><a name="zh-cn_topic_0221482391_p4920144982511"></a><a name="zh-cn_topic_0221482391_p4920144982511"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482391_p092015497251"><a name="zh-cn_topic_0221482391_p092015497251"></a><a name="zh-cn_topic_0221482391_p092015497251"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482391_row13915174962518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p1392194915254"><a name="zh-cn_topic_0221482391_p1392194915254"></a><a name="zh-cn_topic_0221482391_p1392194915254"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p11922154914256"><a name="zh-cn_topic_0221482391_p11922154914256"></a><a name="zh-cn_topic_0221482391_p11922154914256"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p169222495255"><a name="zh-cn_topic_0221482391_p169222495255"></a><a name="zh-cn_topic_0221482391_p169222495255"></a>资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row1915249112518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p792310496258"><a name="zh-cn_topic_0221482391_p792310496258"></a><a name="zh-cn_topic_0221482391_p792310496258"></a>previous</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p149234498258"><a name="zh-cn_topic_0221482391_p149234498258"></a><a name="zh-cn_topic_0221482391_p149234498258"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p1392444922512"><a name="zh-cn_topic_0221482391_p1392444922512"></a><a name="zh-cn_topic_0221482391_p1392444922512"></a>前一邻接资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row1491513498255"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p10924184918255"><a name="zh-cn_topic_0221482391_p10924184918255"></a><a name="zh-cn_topic_0221482391_p10924184918255"></a>next</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p692514498259"><a name="zh-cn_topic_0221482391_p692514498259"></a><a name="zh-cn_topic_0221482391_p692514498259"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p892524915254"><a name="zh-cn_topic_0221482391_p892524915254"></a><a name="zh-cn_topic_0221482391_p892524915254"></a>后一邻接资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  users

<a name="zh-cn_topic_0221482391_response_Rs85UsersArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482391_row492714952514"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482391_p109301497253"><a name="zh-cn_topic_0221482391_p109301497253"></a><a name="zh-cn_topic_0221482391_p109301497253"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482391_p1493174912513"><a name="zh-cn_topic_0221482391_p1493174912513"></a><a name="zh-cn_topic_0221482391_p1493174912513"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482391_p993218491253"><a name="zh-cn_topic_0221482391_p993218491253"></a><a name="zh-cn_topic_0221482391_p993218491253"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482391_row129271549182517"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p14933174912250"><a name="zh-cn_topic_0221482391_p14933174912250"></a><a name="zh-cn_topic_0221482391_p14933174912250"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p59337496259"><a name="zh-cn_topic_0221482391_p59337496259"></a><a name="zh-cn_topic_0221482391_p59337496259"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p693474922514"><a name="zh-cn_topic_0221482391_p693474922514"></a><a name="zh-cn_topic_0221482391_p693474922514"></a>IAM用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row692716496257"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p393410497255"><a name="zh-cn_topic_0221482391_p393410497255"></a><a name="zh-cn_topic_0221482391_p393410497255"></a><a href="#zh-cn_topic_0221482391_response_Rs85UsersArritemLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p4935174910257"><a name="zh-cn_topic_0221482391_p4935174910257"></a><a name="zh-cn_topic_0221482391_p4935174910257"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p893654962517"><a name="zh-cn_topic_0221482391_p893654962517"></a><a name="zh-cn_topic_0221482391_p893654962517"></a>IAM用户的资源链接信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row1992720499257"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p2093634913254"><a name="zh-cn_topic_0221482391_p2093634913254"></a><a name="zh-cn_topic_0221482391_p2093634913254"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p149371049172510"><a name="zh-cn_topic_0221482391_p149371049172510"></a><a name="zh-cn_topic_0221482391_p149371049172510"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p393710495250"><a name="zh-cn_topic_0221482391_p393710495250"></a><a name="zh-cn_topic_0221482391_p393710495250"></a>IAM用户所属账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row139271498256"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p13938134916258"><a name="zh-cn_topic_0221482391_p13938134916258"></a><a name="zh-cn_topic_0221482391_p13938134916258"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p59391149182515"><a name="zh-cn_topic_0221482391_p59391149182515"></a><a name="zh-cn_topic_0221482391_p59391149182515"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p17940164992511"><a name="zh-cn_topic_0221482391_p17940164992511"></a><a name="zh-cn_topic_0221482391_p17940164992511"></a>用户是否启用。true表示启用，false表示停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row20927114952520"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p14940144902518"><a name="zh-cn_topic_0221482391_p14940144902518"></a><a name="zh-cn_topic_0221482391_p14940144902518"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p0941174920254"><a name="zh-cn_topic_0221482391_p0941174920254"></a><a name="zh-cn_topic_0221482391_p0941174920254"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p494164932512"><a name="zh-cn_topic_0221482391_p494164932512"></a><a name="zh-cn_topic_0221482391_p494164932512"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row292718496251"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p12942649122518"><a name="zh-cn_topic_0221482391_p12942649122518"></a><a name="zh-cn_topic_0221482391_p12942649122518"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p3942549112514"><a name="zh-cn_topic_0221482391_p3942549112514"></a><a name="zh-cn_topic_0221482391_p3942549112514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p89431496251"><a name="zh-cn_topic_0221482391_p89431496251"></a><a name="zh-cn_topic_0221482391_p89431496251"></a>密码过期时间（UTC时间），“null”表示密码不过期。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row7927164918253"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p11943184952510"><a name="zh-cn_topic_0221482391_p11943184952510"></a><a name="zh-cn_topic_0221482391_p11943184952510"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p894444982511"><a name="zh-cn_topic_0221482391_p894444982511"></a><a name="zh-cn_topic_0221482391_p894444982511"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p11944649102520"><a name="zh-cn_topic_0221482391_p11944649102520"></a><a name="zh-cn_topic_0221482391_p11944649102520"></a>IAM用户描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row199271449122520"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p1994514932515"><a name="zh-cn_topic_0221482391_p1994514932515"></a><a name="zh-cn_topic_0221482391_p1994514932515"></a>pwd_status</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p2946949162519"><a name="zh-cn_topic_0221482391_p2946949162519"></a><a name="zh-cn_topic_0221482391_p2946949162519"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p39471349112519"><a name="zh-cn_topic_0221482391_p39471349112519"></a><a name="zh-cn_topic_0221482391_p39471349112519"></a>密码状态。true：需要修改密码，false：正常。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row109271349162516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p139473494256"><a name="zh-cn_topic_0221482391_p139473494256"></a><a name="zh-cn_topic_0221482391_p139473494256"></a>forceResetPwd</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p494834912511"><a name="zh-cn_topic_0221482391_p494834912511"></a><a name="zh-cn_topic_0221482391_p494834912511"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p139481493257"><a name="zh-cn_topic_0221482391_p139481493257"></a><a name="zh-cn_topic_0221482391_p139481493257"></a>IAM用户下次登录是否强制重置密码。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row1992844913253"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p18949144932512"><a name="zh-cn_topic_0221482391_p18949144932512"></a><a name="zh-cn_topic_0221482391_p18949144932512"></a>default_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p894911493257"><a name="zh-cn_topic_0221482391_p894911493257"></a><a name="zh-cn_topic_0221482391_p894911493257"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p5950849122518"><a name="zh-cn_topic_0221482391_p5950849122518"></a><a name="zh-cn_topic_0221482391_p5950849122518"></a>IAM用户登录控制台后默认跳转的项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row17928134932517"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p79505497256"><a name="zh-cn_topic_0221482391_p79505497256"></a><a name="zh-cn_topic_0221482391_p79505497256"></a>last_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p189515496254"><a name="zh-cn_topic_0221482391_p189515496254"></a><a name="zh-cn_topic_0221482391_p189515496254"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p139511349172516"><a name="zh-cn_topic_0221482391_p139511349172516"></a><a name="zh-cn_topic_0221482391_p139511349172516"></a>IAM用户退出华为云前，在控制台最后访问的项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row12928134932510"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p1695214911259"><a name="zh-cn_topic_0221482391_p1695214911259"></a><a name="zh-cn_topic_0221482391_p1695214911259"></a>pwd_strength</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p1895284913254"><a name="zh-cn_topic_0221482391_p1895284913254"></a><a name="zh-cn_topic_0221482391_p1895284913254"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p169531349112518"><a name="zh-cn_topic_0221482391_p169531349112518"></a><a name="zh-cn_topic_0221482391_p169531349112518"></a>IAM用户的密码强度。high：密码强度高；mid：密码强度中等；low：密码强度低。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row7928104982513"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p695354913255"><a name="zh-cn_topic_0221482391_p695354913255"></a><a name="zh-cn_topic_0221482391_p695354913255"></a>mobile</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p169541949192514"><a name="zh-cn_topic_0221482391_p169541949192514"></a><a name="zh-cn_topic_0221482391_p169541949192514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p179547493257"><a name="zh-cn_topic_0221482391_p179547493257"></a><a name="zh-cn_topic_0221482391_p179547493257"></a>IAM用户的手机号。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row3928184972518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p89552498256"><a name="zh-cn_topic_0221482391_p89552498256"></a><a name="zh-cn_topic_0221482391_p89552498256"></a>email</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p12955649172512"><a name="zh-cn_topic_0221482391_p12955649172512"></a><a name="zh-cn_topic_0221482391_p12955649172512"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p13956049132519"><a name="zh-cn_topic_0221482391_p13956049132519"></a><a name="zh-cn_topic_0221482391_p13956049132519"></a>IAM用户的邮箱。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  Users.links

<a name="zh-cn_topic_0221482391_response_Rs85UsersArritemLinks"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482391_row199577498255"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482391_p19958149112518"><a name="zh-cn_topic_0221482391_p19958149112518"></a><a name="zh-cn_topic_0221482391_p19958149112518"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482391_p159581749142515"><a name="zh-cn_topic_0221482391_p159581749142515"></a><a name="zh-cn_topic_0221482391_p159581749142515"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482391_p495914942519"><a name="zh-cn_topic_0221482391_p495914942519"></a><a name="zh-cn_topic_0221482391_p495914942519"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482391_row495716496256"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p1495914496251"><a name="zh-cn_topic_0221482391_p1495914496251"></a><a name="zh-cn_topic_0221482391_p1495914496251"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p10960114916259"><a name="zh-cn_topic_0221482391_p10960114916259"></a><a name="zh-cn_topic_0221482391_p10960114916259"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p1961154912259"><a name="zh-cn_topic_0221482391_p1961154912259"></a><a name="zh-cn_topic_0221482391_p1961154912259"></a>资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row17957154942512"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p1396214920256"><a name="zh-cn_topic_0221482391_p1396214920256"></a><a name="zh-cn_topic_0221482391_p1396214920256"></a>previous</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p996264952519"><a name="zh-cn_topic_0221482391_p996264952519"></a><a name="zh-cn_topic_0221482391_p996264952519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p7963949132519"><a name="zh-cn_topic_0221482391_p7963949132519"></a><a name="zh-cn_topic_0221482391_p7963949132519"></a>前一邻接资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row195734918258"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482391_p1696418495258"><a name="zh-cn_topic_0221482391_p1696418495258"></a><a name="zh-cn_topic_0221482391_p1696418495258"></a>next</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482391_p14964449132515"><a name="zh-cn_topic_0221482391_p14964449132515"></a><a name="zh-cn_topic_0221482391_p14964449132515"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482391_p1296511496252"><a name="zh-cn_topic_0221482391_p1296511496252"></a><a name="zh-cn_topic_0221482391_p1296511496252"></a>后一邻接资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482391_section1196619490255"></a>

```
GET https://iam.myhuaweicloud.com/v3/groups/{group_id}/users
```

## 响应示例<a name="zh-cn_topic_0221482391_section4968164922515"></a>

**状态码为 200 时:**

请求成功。

```
{
    "links": {
        "self": "https://iam.huaweicloud.com/v3/groups/07609e7eb200250a3f7dc003cb7a4e2d/users"
    },
    "users": [
        {
            "pwd_status": true,
            "domain_id": "d78cbac186b744899480f25bd022f468",
            "last_project_id": "065a7c66da0010992ff7c0031e5a5e7d",
            "forceResetPwd": false,
            "name": "IAMUserA",
            "description": "--",
            "links": {
                "self": "https://iam.huaweicloud.com/v3/users/07609fb9358010e21f7bc003751c7c32"
            },
            "id": "07609fb9358010e21f7bc003751c7c32",
            "enabled": true
        },
        {
            "pwd_status": true,
            "domain_id": "d78cbac186b744899480f25bd022f468",
            "last_project_id": "065a7c66da0010992ff7c0031e5a5e7d",
            "forceResetPwd": false,
            "name": "IAMUserB",
            "description": "",
            "links": {
                "self": "https://iam.huaweicloud.com/v3/users/076837351e80251c1f0fc003afe43c7e"
            },
            "id": "076837351e80251c1f0fc003afe43c7e",
            "enabled": true
        }
    ]
}
```

## 返回值<a name="zh-cn_topic_0221482391_section1698364902510"></a>

<a name="zh-cn_topic_0221482391_table2453"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482391_row18985749152511"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482391_p17986204932516"><a name="zh-cn_topic_0221482391_p17986204932516"></a><a name="zh-cn_topic_0221482391_p17986204932516"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482391_p16986184952518"><a name="zh-cn_topic_0221482391_p16986184952518"></a><a name="zh-cn_topic_0221482391_p16986184952518"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482391_row59851549192517"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482391_p179871349152516"><a name="zh-cn_topic_0221482391_p179871349152516"></a><a name="zh-cn_topic_0221482391_p179871349152516"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482391_p498744952518"><a name="zh-cn_topic_0221482391_p498744952518"></a><a name="zh-cn_topic_0221482391_p498744952518"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row179851649182514"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482391_p69881649102513"><a name="zh-cn_topic_0221482391_p69881649102513"></a><a name="zh-cn_topic_0221482391_p69881649102513"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482391_p29883495250"><a name="zh-cn_topic_0221482391_p29883495250"></a><a name="zh-cn_topic_0221482391_p29883495250"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row1298564932516"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482391_p119894497258"><a name="zh-cn_topic_0221482391_p119894497258"></a><a name="zh-cn_topic_0221482391_p119894497258"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482391_p17989134912513"><a name="zh-cn_topic_0221482391_p17989134912513"></a><a name="zh-cn_topic_0221482391_p17989134912513"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row198519493259"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482391_p1799018490255"><a name="zh-cn_topic_0221482391_p1799018490255"></a><a name="zh-cn_topic_0221482391_p1799018490255"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482391_p3990144902517"><a name="zh-cn_topic_0221482391_p3990144902517"></a><a name="zh-cn_topic_0221482391_p3990144902517"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482391_row1498594992511"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482391_p1991184922517"><a name="zh-cn_topic_0221482391_p1991184922517"></a><a name="zh-cn_topic_0221482391_p1991184922517"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482391_p2099118498250"><a name="zh-cn_topic_0221482391_p2099118498250"></a><a name="zh-cn_topic_0221482391_p2099118498250"></a>未找到相应的资源。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482391_section1999294932516"></a>

无

