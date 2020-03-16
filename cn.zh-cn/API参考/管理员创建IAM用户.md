# 管理员创建IAM用户<a name="iam_08_0006"></a>

## 功能介绍<a name="zh-cn_topic_0221482425_section3530950182512"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)创建IAM用户。IAM用户首次登录时需要修改密码。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 接口约束<a name="zh-cn_topic_0221482425_section953375022520"></a>

使用该接口创建IAM用户时，不能预置IAM用户的手机号码和邮箱，如需预置上述信息，请参见：[管理员创建IAM用户（推荐）](管理员创建IAM用户（推荐）.md)。

## URI<a name="zh-cn_topic_0221482425_section135347504256"></a>

POST /v3/users

## 请求参数<a name="zh-cn_topic_0221482425_section45357502252"></a>

**表 1**  请求Header参数

<a name="zh-cn_topic_0221482425_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482425_row14536195020253"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482425_p20538450112515"><a name="zh-cn_topic_0221482425_p20538450112515"></a><a name="zh-cn_topic_0221482425_p20538450112515"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482425_p105392050152517"><a name="zh-cn_topic_0221482425_p105392050152517"></a><a name="zh-cn_topic_0221482425_p105392050152517"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482425_p20541850172512"><a name="zh-cn_topic_0221482425_p20541850172512"></a><a name="zh-cn_topic_0221482425_p20541850172512"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482425_p1454285017257"><a name="zh-cn_topic_0221482425_p1454285017257"></a><a name="zh-cn_topic_0221482425_p1454285017257"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482425_row1553613505251"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482425_p954355012253"><a name="zh-cn_topic_0221482425_p954355012253"></a><a name="zh-cn_topic_0221482425_p954355012253"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482425_p754485010252"><a name="zh-cn_topic_0221482425_p754485010252"></a><a name="zh-cn_topic_0221482425_p754485010252"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482425_p854535017259"><a name="zh-cn_topic_0221482425_p854535017259"></a><a name="zh-cn_topic_0221482425_p854535017259"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482425_p1054619505257"><a name="zh-cn_topic_0221482425_p1054619505257"></a><a name="zh-cn_topic_0221482425_p1054619505257"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row1953716502251"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482425_p354675010254"><a name="zh-cn_topic_0221482425_p354675010254"></a><a name="zh-cn_topic_0221482425_p354675010254"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482425_p19547145015253"><a name="zh-cn_topic_0221482425_p19547145015253"></a><a name="zh-cn_topic_0221482425_p19547145015253"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482425_p6548145010255"><a name="zh-cn_topic_0221482425_p6548145010255"></a><a name="zh-cn_topic_0221482425_p6548145010255"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482425_p185481450162510"><a name="zh-cn_topic_0221482425_p185481450162510"></a><a name="zh-cn_topic_0221482425_p185481450162510"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  请求Body参数

<a name="zh-cn_topic_0221482425_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482425_row7550175012253"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482425_p655175052518"><a name="zh-cn_topic_0221482425_p655175052518"></a><a name="zh-cn_topic_0221482425_p655175052518"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482425_p75521350192511"><a name="zh-cn_topic_0221482425_p75521350192511"></a><a name="zh-cn_topic_0221482425_p75521350192511"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482425_p55521550132515"><a name="zh-cn_topic_0221482425_p55521550132515"></a><a name="zh-cn_topic_0221482425_p55521550132515"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482425_p7553550182511"><a name="zh-cn_topic_0221482425_p7553550182511"></a><a name="zh-cn_topic_0221482425_p7553550182511"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482425_row7550950132516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482425_p1055485002513"><a name="zh-cn_topic_0221482425_p1055485002513"></a><a name="zh-cn_topic_0221482425_p1055485002513"></a><a href="#zh-cn_topic_0221482425_request_Rq87User">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482425_p05551850122510"><a name="zh-cn_topic_0221482425_p05551850122510"></a><a name="zh-cn_topic_0221482425_p05551850122510"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482425_p175561150182513"><a name="zh-cn_topic_0221482425_p175561150182513"></a><a name="zh-cn_topic_0221482425_p175561150182513"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482425_p55571050122510"><a name="zh-cn_topic_0221482425_p55571050122510"></a><a name="zh-cn_topic_0221482425_p55571050122510"></a>用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  user

<a name="zh-cn_topic_0221482425_request_Rq87User"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482425_row13559650102515"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482425_p1561195042516"><a name="zh-cn_topic_0221482425_p1561195042516"></a><a name="zh-cn_topic_0221482425_p1561195042516"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482425_p1056211508255"><a name="zh-cn_topic_0221482425_p1056211508255"></a><a name="zh-cn_topic_0221482425_p1056211508255"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482425_p75631750182510"><a name="zh-cn_topic_0221482425_p75631750182510"></a><a name="zh-cn_topic_0221482425_p75631750182510"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482425_p1456325072513"><a name="zh-cn_topic_0221482425_p1456325072513"></a><a name="zh-cn_topic_0221482425_p1456325072513"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482425_row125595502253"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482425_p85641650142516"><a name="zh-cn_topic_0221482425_p85641650142516"></a><a name="zh-cn_topic_0221482425_p85641650142516"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482425_p13565850162519"><a name="zh-cn_topic_0221482425_p13565850162519"></a><a name="zh-cn_topic_0221482425_p13565850162519"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482425_p1156655072514"><a name="zh-cn_topic_0221482425_p1156655072514"></a><a name="zh-cn_topic_0221482425_p1156655072514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482425_p9566175092519"><a name="zh-cn_topic_0221482425_p9566175092519"></a><a name="zh-cn_topic_0221482425_p9566175092519"></a>IAM用户名，长度5~32之间，首位不能为数字，特殊字符只能包含下划线“_”、中划线“-”和空格。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row7559850172516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482425_p0567450152514"><a name="zh-cn_topic_0221482425_p0567450152514"></a><a name="zh-cn_topic_0221482425_p0567450152514"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482425_p17568135013259"><a name="zh-cn_topic_0221482425_p17568135013259"></a><a name="zh-cn_topic_0221482425_p17568135013259"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482425_p2569250132511"><a name="zh-cn_topic_0221482425_p2569250132511"></a><a name="zh-cn_topic_0221482425_p2569250132511"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482425_p135704503251"><a name="zh-cn_topic_0221482425_p135704503251"></a><a name="zh-cn_topic_0221482425_p135704503251"></a>IAM用户所属账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row1855935020254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482425_p957125032514"><a name="zh-cn_topic_0221482425_p957125032514"></a><a name="zh-cn_topic_0221482425_p957125032514"></a>password</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482425_p10572155072514"><a name="zh-cn_topic_0221482425_p10572155072514"></a><a name="zh-cn_topic_0221482425_p10572155072514"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482425_p2572250192520"><a name="zh-cn_topic_0221482425_p2572250192520"></a><a name="zh-cn_topic_0221482425_p2572250192520"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482425_p8573175032519"><a name="zh-cn_topic_0221482425_p8573175032519"></a><a name="zh-cn_topic_0221482425_p8573175032519"></a>IAM用户密码。</p>
<a name="zh-cn_topic_0221482425_ul15573105010256"></a><a name="zh-cn_topic_0221482425_ul15573105010256"></a><ul id="zh-cn_topic_0221482425_ul15573105010256"><li>系统默认密码最小长度为6位字符，在6-32位之间支持用户自定义密码长度。</li><li>至少包含以下四种字符中的两种： 大写字母、小写字母、数字和特殊字符。</li><li>不能包含手机号和邮箱。</li><li>必须满足账户设置中<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0607.html" target="_blank" rel="noopener noreferrer">密码策略</a>的要求。</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row35591550172515"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482425_p557695010253"><a name="zh-cn_topic_0221482425_p557695010253"></a><a name="zh-cn_topic_0221482425_p557695010253"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482425_p357765012515"><a name="zh-cn_topic_0221482425_p357765012515"></a><a name="zh-cn_topic_0221482425_p357765012515"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482425_p457765019259"><a name="zh-cn_topic_0221482425_p457765019259"></a><a name="zh-cn_topic_0221482425_p457765019259"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482425_p135783506259"><a name="zh-cn_topic_0221482425_p135783506259"></a><a name="zh-cn_topic_0221482425_p135783506259"></a>是否启用IAM用户。true为启用，false为停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row4559195072514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482425_p115781850182516"><a name="zh-cn_topic_0221482425_p115781850182516"></a><a name="zh-cn_topic_0221482425_p115781850182516"></a>default_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482425_p1457912501253"><a name="zh-cn_topic_0221482425_p1457912501253"></a><a name="zh-cn_topic_0221482425_p1457912501253"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482425_p1858011500252"><a name="zh-cn_topic_0221482425_p1858011500252"></a><a name="zh-cn_topic_0221482425_p1858011500252"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482425_p0580175032515"><a name="zh-cn_topic_0221482425_p0580175032515"></a><a name="zh-cn_topic_0221482425_p0580175032515"></a>IAM用户默认项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row255914509254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482425_p5581175092515"><a name="zh-cn_topic_0221482425_p5581175092515"></a><a name="zh-cn_topic_0221482425_p5581175092515"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482425_p4582150122517"><a name="zh-cn_topic_0221482425_p4582150122517"></a><a name="zh-cn_topic_0221482425_p4582150122517"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482425_p858211508252"><a name="zh-cn_topic_0221482425_p858211508252"></a><a name="zh-cn_topic_0221482425_p858211508252"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482425_p1158325017257"><a name="zh-cn_topic_0221482425_p1158325017257"></a><a name="zh-cn_topic_0221482425_p1158325017257"></a>IAM用户描述信息。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482425_section12584115022515"></a>

**表 4**  响应Body参数

<a name="zh-cn_topic_0221482425_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482425_row95851550102517"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482425_p15871950112511"><a name="zh-cn_topic_0221482425_p15871950112511"></a><a name="zh-cn_topic_0221482425_p15871950112511"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482425_p8587145017250"><a name="zh-cn_topic_0221482425_p8587145017250"></a><a name="zh-cn_topic_0221482425_p8587145017250"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482425_p9588175042516"><a name="zh-cn_topic_0221482425_p9588175042516"></a><a name="zh-cn_topic_0221482425_p9588175042516"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482425_row1058585015254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482425_p8589250132515"><a name="zh-cn_topic_0221482425_p8589250132515"></a><a name="zh-cn_topic_0221482425_p8589250132515"></a><a href="#zh-cn_topic_0221482425_response_Rs87User">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482425_p75891550162512"><a name="zh-cn_topic_0221482425_p75891550162512"></a><a name="zh-cn_topic_0221482425_p75891550162512"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482425_p1459015092514"><a name="zh-cn_topic_0221482425_p1459015092514"></a><a name="zh-cn_topic_0221482425_p1459015092514"></a>IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  user

<a name="zh-cn_topic_0221482425_response_Rs87User"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482425_row185911506254"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482425_p16593185042513"><a name="zh-cn_topic_0221482425_p16593185042513"></a><a name="zh-cn_topic_0221482425_p16593185042513"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482425_p959475062516"><a name="zh-cn_topic_0221482425_p959475062516"></a><a name="zh-cn_topic_0221482425_p959475062516"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482425_p13595175012257"><a name="zh-cn_topic_0221482425_p13595175012257"></a><a name="zh-cn_topic_0221482425_p13595175012257"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482425_row859235015253"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482425_p259516506255"><a name="zh-cn_topic_0221482425_p259516506255"></a><a name="zh-cn_topic_0221482425_p259516506255"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482425_p2596155018258"><a name="zh-cn_topic_0221482425_p2596155018258"></a><a name="zh-cn_topic_0221482425_p2596155018258"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482425_p459719504250"><a name="zh-cn_topic_0221482425_p459719504250"></a><a name="zh-cn_topic_0221482425_p459719504250"></a>是否启用IAM用户。true为启用，false为停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row45921850122511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482425_p18598205015256"><a name="zh-cn_topic_0221482425_p18598205015256"></a><a name="zh-cn_topic_0221482425_p18598205015256"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482425_p75984501253"><a name="zh-cn_topic_0221482425_p75984501253"></a><a name="zh-cn_topic_0221482425_p75984501253"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482425_p10599165002517"><a name="zh-cn_topic_0221482425_p10599165002517"></a><a name="zh-cn_topic_0221482425_p10599165002517"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row13592135012254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482425_p5600950122513"><a name="zh-cn_topic_0221482425_p5600950122513"></a><a name="zh-cn_topic_0221482425_p5600950122513"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482425_p360175010257"><a name="zh-cn_topic_0221482425_p360175010257"></a><a name="zh-cn_topic_0221482425_p360175010257"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482425_p5601165012251"><a name="zh-cn_topic_0221482425_p5601165012251"></a><a name="zh-cn_topic_0221482425_p5601165012251"></a>IAM用户所属账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row1859295013252"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482425_p9602185013258"><a name="zh-cn_topic_0221482425_p9602185013258"></a><a name="zh-cn_topic_0221482425_p9602185013258"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482425_p1460305072518"><a name="zh-cn_topic_0221482425_p1460305072518"></a><a name="zh-cn_topic_0221482425_p1460305072518"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482425_p11604135022511"><a name="zh-cn_topic_0221482425_p11604135022511"></a><a name="zh-cn_topic_0221482425_p11604135022511"></a>IAM用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row17592850122511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482425_p18605175019252"><a name="zh-cn_topic_0221482425_p18605175019252"></a><a name="zh-cn_topic_0221482425_p18605175019252"></a><a href="#zh-cn_topic_0221482425_response_Rs87UserLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482425_p56101550132512"><a name="zh-cn_topic_0221482425_p56101550132512"></a><a name="zh-cn_topic_0221482425_p56101550132512"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482425_p10610105019256"><a name="zh-cn_topic_0221482425_p10610105019256"></a><a name="zh-cn_topic_0221482425_p10610105019256"></a>IAM用户的资源链接信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row9592115052515"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482425_p20611195016259"><a name="zh-cn_topic_0221482425_p20611195016259"></a><a name="zh-cn_topic_0221482425_p20611195016259"></a>default_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482425_p7612125017253"><a name="zh-cn_topic_0221482425_p7612125017253"></a><a name="zh-cn_topic_0221482425_p7612125017253"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482425_p166123509258"><a name="zh-cn_topic_0221482425_p166123509258"></a><a name="zh-cn_topic_0221482425_p166123509258"></a>IAM用户默认项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row12592155022513"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482425_p361395032514"><a name="zh-cn_topic_0221482425_p361395032514"></a><a name="zh-cn_topic_0221482425_p361395032514"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482425_p186140507257"><a name="zh-cn_topic_0221482425_p186140507257"></a><a name="zh-cn_topic_0221482425_p186140507257"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482425_p961415022519"><a name="zh-cn_topic_0221482425_p961415022519"></a><a name="zh-cn_topic_0221482425_p961415022519"></a>密码过期时间（UTC时间），“null”表示密码不过期。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row13592165012254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482425_p761515509257"><a name="zh-cn_topic_0221482425_p761515509257"></a><a name="zh-cn_topic_0221482425_p761515509257"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482425_p76161508251"><a name="zh-cn_topic_0221482425_p76161508251"></a><a name="zh-cn_topic_0221482425_p76161508251"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482425_p1661612509252"><a name="zh-cn_topic_0221482425_p1661612509252"></a><a name="zh-cn_topic_0221482425_p1661612509252"></a>IAM用户描述信息。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  user.links

<a name="zh-cn_topic_0221482425_response_Rs87UserLinks"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482425_row116179501258"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482425_p186192508257"><a name="zh-cn_topic_0221482425_p186192508257"></a><a name="zh-cn_topic_0221482425_p186192508257"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482425_p1161985072515"><a name="zh-cn_topic_0221482425_p1161985072515"></a><a name="zh-cn_topic_0221482425_p1161985072515"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482425_p1962015011258"><a name="zh-cn_topic_0221482425_p1962015011258"></a><a name="zh-cn_topic_0221482425_p1962015011258"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482425_row9617195019251"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482425_p186211450192512"><a name="zh-cn_topic_0221482425_p186211450192512"></a><a name="zh-cn_topic_0221482425_p186211450192512"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482425_p862155072520"><a name="zh-cn_topic_0221482425_p862155072520"></a><a name="zh-cn_topic_0221482425_p862155072520"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482425_p17622350142515"><a name="zh-cn_topic_0221482425_p17622350142515"></a><a name="zh-cn_topic_0221482425_p17622350142515"></a>资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482425_section16623185092512"></a>

```
POST https://iam.myhuaweicloud.com/v3/users
```

```
{
    "user": {
        "name": "IAMUser",
        "domain_id": "d78cbac186b744899480f25bd02...",
        "enabled": true,
        "password": "IAMPassword@",
        "default_project_id": "aa2d97d7e62c4b7da3ffdfc1155...",
        "description": "IAMDescription"
    }
}
```

## 响应示例<a name="zh-cn_topic_0221482425_section1763075042516"></a>

**状态码为 201 时:**

创建成功。

```
{
    "user": {
        "description": "IAMDescription",
        "name": "IAMUser",
        "enabled": true,
        "links": {
            "self": "https://iam.myhuaweicloud.com/v3/users/076598a17b0010e21fdec003f3a2aa45"
        },
        "domain_id": "d78cbac186b744899480f25b...",
        "default_project_id": "aa2d97d7e62c4b7da3ffdfc115...",
        "id": "076598a17b0010e21fdec003f3a2a..."
    }
}
```

## 返回值<a name="zh-cn_topic_0221482425_section17638750142512"></a>

<a name="zh-cn_topic_0221482425_table2441"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482425_row4639250162511"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482425_p564005011253"><a name="zh-cn_topic_0221482425_p564005011253"></a><a name="zh-cn_topic_0221482425_p564005011253"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482425_p1764165052515"><a name="zh-cn_topic_0221482425_p1764165052515"></a><a name="zh-cn_topic_0221482425_p1764165052515"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482425_row196394509256"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482425_p664235042515"><a name="zh-cn_topic_0221482425_p664235042515"></a><a name="zh-cn_topic_0221482425_p664235042515"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482425_p7642135022514"><a name="zh-cn_topic_0221482425_p7642135022514"></a><a name="zh-cn_topic_0221482425_p7642135022514"></a>创建成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row206393501255"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482425_p19643145012518"><a name="zh-cn_topic_0221482425_p19643145012518"></a><a name="zh-cn_topic_0221482425_p19643145012518"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482425_p96431050112513"><a name="zh-cn_topic_0221482425_p96431050112513"></a><a name="zh-cn_topic_0221482425_p96431050112513"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row36391150112512"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482425_p6644135017257"><a name="zh-cn_topic_0221482425_p6644135017257"></a><a name="zh-cn_topic_0221482425_p6644135017257"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482425_p1264495014259"><a name="zh-cn_topic_0221482425_p1264495014259"></a><a name="zh-cn_topic_0221482425_p1264495014259"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row11639550132517"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482425_p5645105012257"><a name="zh-cn_topic_0221482425_p5645105012257"></a><a name="zh-cn_topic_0221482425_p5645105012257"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482425_p1364520503251"><a name="zh-cn_topic_0221482425_p1364520503251"></a><a name="zh-cn_topic_0221482425_p1364520503251"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row17639145019251"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482425_p20646350162516"><a name="zh-cn_topic_0221482425_p20646350162516"></a><a name="zh-cn_topic_0221482425_p20646350162516"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482425_p664675072518"><a name="zh-cn_topic_0221482425_p664675072518"></a><a name="zh-cn_topic_0221482425_p664675072518"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row156401250132513"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482425_p1664755013253"><a name="zh-cn_topic_0221482425_p1664755013253"></a><a name="zh-cn_topic_0221482425_p1664755013253"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482425_p156491750102520"><a name="zh-cn_topic_0221482425_p156491750102520"></a><a name="zh-cn_topic_0221482425_p156491750102520"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row764055012519"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482425_p96501550142511"><a name="zh-cn_topic_0221482425_p96501550142511"></a><a name="zh-cn_topic_0221482425_p96501550142511"></a>409</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482425_p10651250182510"><a name="zh-cn_topic_0221482425_p10651250182510"></a><a name="zh-cn_topic_0221482425_p10651250182510"></a>资源冲突。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row16640105011257"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482425_p16651135072514"><a name="zh-cn_topic_0221482425_p16651135072514"></a><a name="zh-cn_topic_0221482425_p16651135072514"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482425_p3652125032516"><a name="zh-cn_topic_0221482425_p3652125032516"></a><a name="zh-cn_topic_0221482425_p3652125032516"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row10640105014258"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482425_p6652850102514"><a name="zh-cn_topic_0221482425_p6652850102514"></a><a name="zh-cn_topic_0221482425_p6652850102514"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482425_p156533507251"><a name="zh-cn_topic_0221482425_p156533507251"></a><a name="zh-cn_topic_0221482425_p156533507251"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row1664045092512"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482425_p18654250112516"><a name="zh-cn_topic_0221482425_p18654250112516"></a><a name="zh-cn_topic_0221482425_p18654250112516"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482425_p26546508258"><a name="zh-cn_topic_0221482425_p26546508258"></a><a name="zh-cn_topic_0221482425_p26546508258"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482425_section126555502253"></a>

<a name="zh-cn_topic_0221482425_table2442"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482425_row065745042515"><th class="cellrowborder" valign="top" width="27.27272727272727%" id="mcps1.1.4.1.1"><p id="zh-cn_topic_0221482425_p19659175072513"><a name="zh-cn_topic_0221482425_p19659175072513"></a><a name="zh-cn_topic_0221482425_p19659175072513"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="36.36363636363636%" id="mcps1.1.4.1.2"><p id="zh-cn_topic_0221482425_p11660185015254"><a name="zh-cn_topic_0221482425_p11660185015254"></a><a name="zh-cn_topic_0221482425_p11660185015254"></a>错误码</p>
</th>
<th class="cellrowborder" valign="top" width="36.36363636363636%" id="mcps1.1.4.1.3"><p id="zh-cn_topic_0221482425_p17660175052519"><a name="zh-cn_topic_0221482425_p17660175052519"></a><a name="zh-cn_topic_0221482425_p17660175052519"></a>错误信息</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482425_row36573503253"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p5662115017255"><a name="zh-cn_topic_0221482425_p5662115017255"></a><a name="zh-cn_topic_0221482425_p5662115017255"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p2663650142510"><a name="zh-cn_topic_0221482425_p2663650142510"></a><a name="zh-cn_topic_0221482425_p2663650142510"></a>1100</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p466375062511"><a name="zh-cn_topic_0221482425_p466375062511"></a><a name="zh-cn_topic_0221482425_p466375062511"></a>缺失必选参数。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row1765714508254"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p116651506257"><a name="zh-cn_topic_0221482425_p116651506257"></a><a name="zh-cn_topic_0221482425_p116651506257"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p156661350132512"><a name="zh-cn_topic_0221482425_p156661350132512"></a><a name="zh-cn_topic_0221482425_p156661350132512"></a>1101</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p266735012257"><a name="zh-cn_topic_0221482425_p266735012257"></a><a name="zh-cn_topic_0221482425_p266735012257"></a>用户名校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row0657950102511"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p966845018253"><a name="zh-cn_topic_0221482425_p966845018253"></a><a name="zh-cn_topic_0221482425_p966845018253"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p766945015254"><a name="zh-cn_topic_0221482425_p766945015254"></a><a name="zh-cn_topic_0221482425_p766945015254"></a>1102</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p066912506251"><a name="zh-cn_topic_0221482425_p066912506251"></a><a name="zh-cn_topic_0221482425_p066912506251"></a>邮箱校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row6657350192516"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p10671185052512"><a name="zh-cn_topic_0221482425_p10671185052512"></a><a name="zh-cn_topic_0221482425_p10671185052512"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p1467165012515"><a name="zh-cn_topic_0221482425_p1467165012515"></a><a name="zh-cn_topic_0221482425_p1467165012515"></a>1103</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p13672175082514"><a name="zh-cn_topic_0221482425_p13672175082514"></a><a name="zh-cn_topic_0221482425_p13672175082514"></a>密码校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row265725042510"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p16673175062519"><a name="zh-cn_topic_0221482425_p16673175062519"></a><a name="zh-cn_topic_0221482425_p16673175062519"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p116744502257"><a name="zh-cn_topic_0221482425_p116744502257"></a><a name="zh-cn_topic_0221482425_p116744502257"></a>1104</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p1674115052520"><a name="zh-cn_topic_0221482425_p1674115052520"></a><a name="zh-cn_topic_0221482425_p1674115052520"></a>手机号校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row865715015259"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p156762504253"><a name="zh-cn_topic_0221482425_p156762504253"></a><a name="zh-cn_topic_0221482425_p156762504253"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p1631351102515"><a name="zh-cn_topic_0221482425_p1631351102515"></a><a name="zh-cn_topic_0221482425_p1631351102515"></a>1105</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p432115142510"><a name="zh-cn_topic_0221482425_p432115142510"></a><a name="zh-cn_topic_0221482425_p432115142510"></a>xuser_type必须与xdomain_type相同。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row146581150192514"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p173214510259"><a name="zh-cn_topic_0221482425_p173214510259"></a><a name="zh-cn_topic_0221482425_p173214510259"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p1532551182514"><a name="zh-cn_topic_0221482425_p1532551182514"></a><a name="zh-cn_topic_0221482425_p1532551182514"></a>1106</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p183313519255"><a name="zh-cn_topic_0221482425_p183313519255"></a><a name="zh-cn_topic_0221482425_p183313519255"></a>国家码、手机号必须同时存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row16658185052511"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p3336513255"><a name="zh-cn_topic_0221482425_p3336513255"></a><a name="zh-cn_topic_0221482425_p3336513255"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p4331951122517"><a name="zh-cn_topic_0221482425_p4331951122517"></a><a name="zh-cn_topic_0221482425_p4331951122517"></a>1107</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p133651182513"><a name="zh-cn_topic_0221482425_p133651182513"></a><a name="zh-cn_topic_0221482425_p133651182513"></a>账号管理员不能被删除。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row106581950132513"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p14341751132520"><a name="zh-cn_topic_0221482425_p14341751132520"></a><a name="zh-cn_topic_0221482425_p14341751132520"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p113435119255"><a name="zh-cn_topic_0221482425_p113435119255"></a><a name="zh-cn_topic_0221482425_p113435119255"></a>1108</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p834115113254"><a name="zh-cn_topic_0221482425_p834115113254"></a><a name="zh-cn_topic_0221482425_p834115113254"></a>新密码不能与原密码相同。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row1365845082512"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p103585162515"><a name="zh-cn_topic_0221482425_p103585162515"></a><a name="zh-cn_topic_0221482425_p103585162515"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p835135119252"><a name="zh-cn_topic_0221482425_p835135119252"></a><a name="zh-cn_topic_0221482425_p835135119252"></a>1109</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p23585172511"><a name="zh-cn_topic_0221482425_p23585172511"></a><a name="zh-cn_topic_0221482425_p23585172511"></a>用户名已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row146583500259"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p1236451132514"><a name="zh-cn_topic_0221482425_p1236451132514"></a><a name="zh-cn_topic_0221482425_p1236451132514"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p636105112255"><a name="zh-cn_topic_0221482425_p636105112255"></a><a name="zh-cn_topic_0221482425_p636105112255"></a>1110</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p203614512258"><a name="zh-cn_topic_0221482425_p203614512258"></a><a name="zh-cn_topic_0221482425_p203614512258"></a>邮箱已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row206583509250"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p137155192510"><a name="zh-cn_topic_0221482425_p137155192510"></a><a name="zh-cn_topic_0221482425_p137155192510"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p237105152514"><a name="zh-cn_topic_0221482425_p237105152514"></a><a name="zh-cn_topic_0221482425_p237105152514"></a>1111</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p183717516254"><a name="zh-cn_topic_0221482425_p183717516254"></a><a name="zh-cn_topic_0221482425_p183717516254"></a>手机号已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row1365885010258"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p12381551152513"><a name="zh-cn_topic_0221482425_p12381551152513"></a><a name="zh-cn_topic_0221482425_p12381551152513"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p133835182517"><a name="zh-cn_topic_0221482425_p133835182517"></a><a name="zh-cn_topic_0221482425_p133835182517"></a>1113</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p18391751112516"><a name="zh-cn_topic_0221482425_p18391751112516"></a><a name="zh-cn_topic_0221482425_p18391751112516"></a>xuser_id、xuser_type已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row165875002515"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p103945162510"><a name="zh-cn_topic_0221482425_p103945162510"></a><a name="zh-cn_topic_0221482425_p103945162510"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p039155114254"><a name="zh-cn_topic_0221482425_p039155114254"></a><a name="zh-cn_topic_0221482425_p039155114254"></a>1115</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p1839125110253"><a name="zh-cn_topic_0221482425_p1839125110253"></a><a name="zh-cn_topic_0221482425_p1839125110253"></a>IAM用户数量达到最大限制。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482425_row1465855062511"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482425_p18401151162515"><a name="zh-cn_topic_0221482425_p18401151162515"></a><a name="zh-cn_topic_0221482425_p18401151162515"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482425_p1140105182516"><a name="zh-cn_topic_0221482425_p1140105182516"></a><a name="zh-cn_topic_0221482425_p1140105182516"></a>1117</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482425_p194085142511"><a name="zh-cn_topic_0221482425_p194085142511"></a><a name="zh-cn_topic_0221482425_p194085142511"></a>用户描述校验失败。</p>
</td>
</tr>
</tbody>
</table>

