# 管理员创建IAM用户（推荐）<a name="iam_08_0015"></a>

## 功能介绍<a name="zh-cn_topic_0221482430_section1474415507251"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)创建IAM用户。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="zh-cn_topic_0221482430_section12746115052514"></a>

POST /v3.0/OS-USER/users

## 请求参数<a name="zh-cn_topic_0221482430_section187477503255"></a>

**表 1**  请求Header参数

<a name="zh-cn_topic_0221482430_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482430_row14748115052514"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482430_p1374955019259"><a name="zh-cn_topic_0221482430_p1374955019259"></a><a name="zh-cn_topic_0221482430_p1374955019259"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482430_p16749750182517"><a name="zh-cn_topic_0221482430_p16749750182517"></a><a name="zh-cn_topic_0221482430_p16749750182517"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482430_p87501450132515"><a name="zh-cn_topic_0221482430_p87501450132515"></a><a name="zh-cn_topic_0221482430_p87501450132515"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482430_p177505505252"><a name="zh-cn_topic_0221482430_p177505505252"></a><a name="zh-cn_topic_0221482430_p177505505252"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482430_row77483504251"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p1875119508252"><a name="zh-cn_topic_0221482430_p1875119508252"></a><a name="zh-cn_topic_0221482430_p1875119508252"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p175225011258"><a name="zh-cn_topic_0221482430_p175225011258"></a><a name="zh-cn_topic_0221482430_p175225011258"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p575211503259"><a name="zh-cn_topic_0221482430_p575211503259"></a><a name="zh-cn_topic_0221482430_p575211503259"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p1975310500255"><a name="zh-cn_topic_0221482430_p1975310500255"></a><a name="zh-cn_topic_0221482430_p1975310500255"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row1974810502254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p1775395092513"><a name="zh-cn_topic_0221482430_p1775395092513"></a><a name="zh-cn_topic_0221482430_p1775395092513"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p3754135019251"><a name="zh-cn_topic_0221482430_p3754135019251"></a><a name="zh-cn_topic_0221482430_p3754135019251"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p5754155052519"><a name="zh-cn_topic_0221482430_p5754155052519"></a><a name="zh-cn_topic_0221482430_p5754155052519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p5755950142512"><a name="zh-cn_topic_0221482430_p5755950142512"></a><a name="zh-cn_topic_0221482430_p5755950142512"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  请求Body参数

<a name="zh-cn_topic_0221482430_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482430_row6755650142510"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482430_p11756135012256"><a name="zh-cn_topic_0221482430_p11756135012256"></a><a name="zh-cn_topic_0221482430_p11756135012256"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482430_p37576500257"><a name="zh-cn_topic_0221482430_p37576500257"></a><a name="zh-cn_topic_0221482430_p37576500257"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482430_p10758155062515"><a name="zh-cn_topic_0221482430_p10758155062515"></a><a name="zh-cn_topic_0221482430_p10758155062515"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482430_p1275955016255"><a name="zh-cn_topic_0221482430_p1275955016255"></a><a name="zh-cn_topic_0221482430_p1275955016255"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482430_row87551450132518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p167601950142511"><a name="zh-cn_topic_0221482430_p167601950142511"></a><a name="zh-cn_topic_0221482430_p167601950142511"></a><a href="#zh-cn_topic_0221482430_request_Rq86User">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p1376010501256"><a name="zh-cn_topic_0221482430_p1376010501256"></a><a name="zh-cn_topic_0221482430_p1376010501256"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p3761105082517"><a name="zh-cn_topic_0221482430_p3761105082517"></a><a name="zh-cn_topic_0221482430_p3761105082517"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p1576215022512"><a name="zh-cn_topic_0221482430_p1576215022512"></a><a name="zh-cn_topic_0221482430_p1576215022512"></a>IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  user

<a name="zh-cn_topic_0221482430_request_Rq86User"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482430_row8763150142511"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482430_p1576505011253"><a name="zh-cn_topic_0221482430_p1576505011253"></a><a name="zh-cn_topic_0221482430_p1576505011253"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482430_p07665504255"><a name="zh-cn_topic_0221482430_p07665504255"></a><a name="zh-cn_topic_0221482430_p07665504255"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482430_p17671500252"><a name="zh-cn_topic_0221482430_p17671500252"></a><a name="zh-cn_topic_0221482430_p17671500252"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482430_p1676745092515"><a name="zh-cn_topic_0221482430_p1676745092515"></a><a name="zh-cn_topic_0221482430_p1676745092515"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482430_row18763145062515"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p10768105012259"><a name="zh-cn_topic_0221482430_p10768105012259"></a><a name="zh-cn_topic_0221482430_p10768105012259"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p976975002515"><a name="zh-cn_topic_0221482430_p976975002515"></a><a name="zh-cn_topic_0221482430_p976975002515"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p076935072511"><a name="zh-cn_topic_0221482430_p076935072511"></a><a name="zh-cn_topic_0221482430_p076935072511"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p117701350162518"><a name="zh-cn_topic_0221482430_p117701350162518"></a><a name="zh-cn_topic_0221482430_p117701350162518"></a>IAM用户名。长度5~32之间，首位不能为数字，特殊字符只能包含下划线“_”、中划线“-”和空格。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row1376418507254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p1771165052515"><a name="zh-cn_topic_0221482430_p1771165052515"></a><a name="zh-cn_topic_0221482430_p1771165052515"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p577135032516"><a name="zh-cn_topic_0221482430_p577135032516"></a><a name="zh-cn_topic_0221482430_p577135032516"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p1277215014254"><a name="zh-cn_topic_0221482430_p1277215014254"></a><a name="zh-cn_topic_0221482430_p1277215014254"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p11772750162514"><a name="zh-cn_topic_0221482430_p11772750162514"></a><a name="zh-cn_topic_0221482430_p11772750162514"></a>IAM用户所属的账号ID，获取方式请参见：<a href="获取账号-IAM用户-项目-用户组-委托的名称和ID.md">获取账号、IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row117641350122514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p27741507250"><a name="zh-cn_topic_0221482430_p27741507250"></a><a name="zh-cn_topic_0221482430_p27741507250"></a>password</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p277515014256"><a name="zh-cn_topic_0221482430_p277515014256"></a><a name="zh-cn_topic_0221482430_p277515014256"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p1177625014252"><a name="zh-cn_topic_0221482430_p1177625014252"></a><a name="zh-cn_topic_0221482430_p1177625014252"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p157764507258"><a name="zh-cn_topic_0221482430_p157764507258"></a><a name="zh-cn_topic_0221482430_p157764507258"></a>IAM用户密码。</p>
<a name="zh-cn_topic_0221482430_ul77771250112518"></a><a name="zh-cn_topic_0221482430_ul77771250112518"></a><ul id="zh-cn_topic_0221482430_ul77771250112518"><li>系统默认密码最小长度为6位字符，在6-32位之间支持用户自定义密码长度。</li><li>至少包含以下四种字符中的两种： 大写字母、小写字母、数字和特殊字符。</li><li>不能包含手机号和邮箱。</li><li>必须满足账户设置中密码策略的要求。</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row17764205011250"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p077925020259"><a name="zh-cn_topic_0221482430_p077925020259"></a><a name="zh-cn_topic_0221482430_p077925020259"></a>email</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p117800508254"><a name="zh-cn_topic_0221482430_p117800508254"></a><a name="zh-cn_topic_0221482430_p117800508254"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p1378185092516"><a name="zh-cn_topic_0221482430_p1378185092516"></a><a name="zh-cn_topic_0221482430_p1378185092516"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p187825501258"><a name="zh-cn_topic_0221482430_p187825501258"></a><a name="zh-cn_topic_0221482430_p187825501258"></a>IAM用户邮箱，需符合邮箱格式，长度小于等于255位。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row1976465012516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p978285017257"><a name="zh-cn_topic_0221482430_p978285017257"></a><a name="zh-cn_topic_0221482430_p978285017257"></a>areacode</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p4783450142513"><a name="zh-cn_topic_0221482430_p4783450142513"></a><a name="zh-cn_topic_0221482430_p4783450142513"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p2078375092512"><a name="zh-cn_topic_0221482430_p2078375092512"></a><a name="zh-cn_topic_0221482430_p2078375092512"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p478425020258"><a name="zh-cn_topic_0221482430_p478425020258"></a><a name="zh-cn_topic_0221482430_p478425020258"></a>国家码。必须与手机号同时存在。中国大陆为“0086”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row11764205013252"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p14784125062518"><a name="zh-cn_topic_0221482430_p14784125062518"></a><a name="zh-cn_topic_0221482430_p14784125062518"></a>phone</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p1978514506253"><a name="zh-cn_topic_0221482430_p1978514506253"></a><a name="zh-cn_topic_0221482430_p1978514506253"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p97851750182516"><a name="zh-cn_topic_0221482430_p97851750182516"></a><a name="zh-cn_topic_0221482430_p97851750182516"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p147861950182512"><a name="zh-cn_topic_0221482430_p147861950182512"></a><a name="zh-cn_topic_0221482430_p147861950182512"></a>IAM用户手机号，纯数字，长度小于等于32位。必须与国家码同时存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row197641550142516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p17786195011254"><a name="zh-cn_topic_0221482430_p17786195011254"></a><a name="zh-cn_topic_0221482430_p17786195011254"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p1978725012250"><a name="zh-cn_topic_0221482430_p1978725012250"></a><a name="zh-cn_topic_0221482430_p1978725012250"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p6788105012519"><a name="zh-cn_topic_0221482430_p6788105012519"></a><a name="zh-cn_topic_0221482430_p6788105012519"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p07881350122520"><a name="zh-cn_topic_0221482430_p07881350122520"></a><a name="zh-cn_topic_0221482430_p07881350122520"></a>是否启用IAM用户。true为启用，false为停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row1076455042512"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p7789750152515"><a name="zh-cn_topic_0221482430_p7789750152515"></a><a name="zh-cn_topic_0221482430_p7789750152515"></a>pwd_status</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p12791115020255"><a name="zh-cn_topic_0221482430_p12791115020255"></a><a name="zh-cn_topic_0221482430_p12791115020255"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p1679445082515"><a name="zh-cn_topic_0221482430_p1679445082515"></a><a name="zh-cn_topic_0221482430_p1679445082515"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p147945504252"><a name="zh-cn_topic_0221482430_p147945504252"></a><a name="zh-cn_topic_0221482430_p147945504252"></a>IAM用户首次登录是否重置密码，默认需要重置。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row1576465018251"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p779513501255"><a name="zh-cn_topic_0221482430_p779513501255"></a><a name="zh-cn_topic_0221482430_p779513501255"></a>default_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p679625092516"><a name="zh-cn_topic_0221482430_p679625092516"></a><a name="zh-cn_topic_0221482430_p679625092516"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p779719505253"><a name="zh-cn_topic_0221482430_p779719505253"></a><a name="zh-cn_topic_0221482430_p779719505253"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p127985501256"><a name="zh-cn_topic_0221482430_p127985501256"></a><a name="zh-cn_topic_0221482430_p127985501256"></a>IAM用户默认项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row17764145072518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p147991450142515"><a name="zh-cn_topic_0221482430_p147991450142515"></a><a name="zh-cn_topic_0221482430_p147991450142515"></a>xuser_type</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p97991506252"><a name="zh-cn_topic_0221482430_p97991506252"></a><a name="zh-cn_topic_0221482430_p97991506252"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p7800175002515"><a name="zh-cn_topic_0221482430_p7800175002515"></a><a name="zh-cn_topic_0221482430_p7800175002515"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p1680175020252"><a name="zh-cn_topic_0221482430_p1680175020252"></a><a name="zh-cn_topic_0221482430_p1680175020252"></a>IAM用户在外部系统中的类型。长度小于等于64位。xuser_type如果存在，则需要与同一租户中的xaccount_type、xdomain_type校验，须与xuser_id同时存在。</p>
<div class="note" id="zh-cn_topic_0221482430_note118031650102520"><a name="zh-cn_topic_0221482430_note118031650102520"></a><a name="zh-cn_topic_0221482430_note118031650102520"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0221482430_p16804175013252"><a name="zh-cn_topic_0221482430_p16804175013252"></a><a name="zh-cn_topic_0221482430_p16804175013252"></a>外部系统指与华为云对接的外部企业管理系统，xaccount_type、xaccount_id、xdomain_type、xdomain_id、xuser_type、xuser_id等参数值，无法在华为云获取，请咨询企业管理员。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row12764195018254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p158053509252"><a name="zh-cn_topic_0221482430_p158053509252"></a><a name="zh-cn_topic_0221482430_p158053509252"></a>xuser_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p980610508258"><a name="zh-cn_topic_0221482430_p980610508258"></a><a name="zh-cn_topic_0221482430_p980610508258"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p13807185052520"><a name="zh-cn_topic_0221482430_p13807185052520"></a><a name="zh-cn_topic_0221482430_p13807185052520"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p18071950162515"><a name="zh-cn_topic_0221482430_p18071950162515"></a><a name="zh-cn_topic_0221482430_p18071950162515"></a>IAM用户在外部系统中的ID。长度小于等于128位，须与xuser_type同时存在。</p>
<div class="note" id="zh-cn_topic_0221482430_note980910503251"><a name="zh-cn_topic_0221482430_note980910503251"></a><a name="zh-cn_topic_0221482430_note980910503251"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0221482430_p881015503255"><a name="zh-cn_topic_0221482430_p881015503255"></a><a name="zh-cn_topic_0221482430_p881015503255"></a>外部系统指与华为云对接的外部企业管理系统，xaccount_type、xaccount_id、xdomain_type、xdomain_id、xuser_type、xuser_id等参数值，无法在华为云获取，请咨询企业管理员。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row7764250112516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482430_p1811115042513"><a name="zh-cn_topic_0221482430_p1811115042513"></a><a name="zh-cn_topic_0221482430_p1811115042513"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482430_p58111350172519"><a name="zh-cn_topic_0221482430_p58111350172519"></a><a name="zh-cn_topic_0221482430_p58111350172519"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482430_p9812185082516"><a name="zh-cn_topic_0221482430_p9812185082516"></a><a name="zh-cn_topic_0221482430_p9812185082516"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482430_p98126503253"><a name="zh-cn_topic_0221482430_p98126503253"></a><a name="zh-cn_topic_0221482430_p98126503253"></a>IAM用户描述信息。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482430_section481319508251"></a>

**表 4**  响应Body参数

<a name="zh-cn_topic_0221482430_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482430_row381455015254"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482430_p15815350172519"><a name="zh-cn_topic_0221482430_p15815350172519"></a><a name="zh-cn_topic_0221482430_p15815350172519"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482430_p181618506254"><a name="zh-cn_topic_0221482430_p181618506254"></a><a name="zh-cn_topic_0221482430_p181618506254"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482430_p181612508258"><a name="zh-cn_topic_0221482430_p181612508258"></a><a name="zh-cn_topic_0221482430_p181612508258"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482430_row128141950112514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p681785014257"><a name="zh-cn_topic_0221482430_p681785014257"></a><a name="zh-cn_topic_0221482430_p681785014257"></a><a href="#zh-cn_topic_0221482430_response_Rs86User">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p981795012512"><a name="zh-cn_topic_0221482430_p981795012512"></a><a name="zh-cn_topic_0221482430_p981795012512"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p19818250152511"><a name="zh-cn_topic_0221482430_p19818250152511"></a><a name="zh-cn_topic_0221482430_p19818250152511"></a>IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  user

<a name="zh-cn_topic_0221482430_response_Rs86User"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482430_row14819165019257"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482430_p3823125010258"><a name="zh-cn_topic_0221482430_p3823125010258"></a><a name="zh-cn_topic_0221482430_p3823125010258"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482430_p7824195022516"><a name="zh-cn_topic_0221482430_p7824195022516"></a><a name="zh-cn_topic_0221482430_p7824195022516"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482430_p1782616501255"><a name="zh-cn_topic_0221482430_p1782616501255"></a><a name="zh-cn_topic_0221482430_p1782616501255"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482430_row1181910500252"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p1982755012258"><a name="zh-cn_topic_0221482430_p1982755012258"></a><a name="zh-cn_topic_0221482430_p1982755012258"></a>status</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p12828165018251"><a name="zh-cn_topic_0221482430_p12828165018251"></a><a name="zh-cn_topic_0221482430_p12828165018251"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p168281150182519"><a name="zh-cn_topic_0221482430_p168281150182519"></a><a name="zh-cn_topic_0221482430_p168281150182519"></a>IAM用户状态信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row4820350142511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p19829350192513"><a name="zh-cn_topic_0221482430_p19829350192513"></a><a name="zh-cn_topic_0221482430_p19829350192513"></a>pwd_status</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p182985072510"><a name="zh-cn_topic_0221482430_p182985072510"></a><a name="zh-cn_topic_0221482430_p182985072510"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p083095011256"><a name="zh-cn_topic_0221482430_p083095011256"></a><a name="zh-cn_topic_0221482430_p083095011256"></a>IAM用户首次登录是否重置密码。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row14820185013259"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p3831175042511"><a name="zh-cn_topic_0221482430_p3831175042511"></a><a name="zh-cn_topic_0221482430_p3831175042511"></a>xuser_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p158311150112513"><a name="zh-cn_topic_0221482430_p158311150112513"></a><a name="zh-cn_topic_0221482430_p158311150112513"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p48326503256"><a name="zh-cn_topic_0221482430_p48326503256"></a><a name="zh-cn_topic_0221482430_p48326503256"></a>IAM用户在外部系统中的ID。</p>
<div class="note" id="zh-cn_topic_0221482430_note9833115052519"><a name="zh-cn_topic_0221482430_note9833115052519"></a><a name="zh-cn_topic_0221482430_note9833115052519"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0221482430_p2834050172514"><a name="zh-cn_topic_0221482430_p2834050172514"></a><a name="zh-cn_topic_0221482430_p2834050172514"></a>外部系统指与华为云对接的外部企业管理系统，xaccount_type、xaccount_id、xdomain_type、xdomain_id、xuser_type、xuser_id等参数值，无法在华为云获取，请咨询企业管理员。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row14820145012252"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p1983517502251"><a name="zh-cn_topic_0221482430_p1983517502251"></a><a name="zh-cn_topic_0221482430_p1983517502251"></a>xuser_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p183735072518"><a name="zh-cn_topic_0221482430_p183735072518"></a><a name="zh-cn_topic_0221482430_p183735072518"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p1483710506251"><a name="zh-cn_topic_0221482430_p1483710506251"></a><a name="zh-cn_topic_0221482430_p1483710506251"></a>用户在外部系统中的类型。</p>
<div class="note" id="zh-cn_topic_0221482430_note1583915013258"><a name="zh-cn_topic_0221482430_note1583915013258"></a><a name="zh-cn_topic_0221482430_note1583915013258"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0221482430_p1483915503258"><a name="zh-cn_topic_0221482430_p1483915503258"></a><a name="zh-cn_topic_0221482430_p1483915503258"></a>外部系统指与华为云对接的外部企业管理系统，xaccount_type、xaccount_id、xdomain_type、xdomain_id、xuser_type、xuser_id等参数值，无法在华为云获取，请咨询企业管理员。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row28211950112515"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p284011507255"><a name="zh-cn_topic_0221482430_p284011507255"></a><a name="zh-cn_topic_0221482430_p284011507255"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p158411450122514"><a name="zh-cn_topic_0221482430_p158411450122514"></a><a name="zh-cn_topic_0221482430_p158411450122514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p684135012259"><a name="zh-cn_topic_0221482430_p684135012259"></a><a name="zh-cn_topic_0221482430_p684135012259"></a>IAM用户描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row582195014254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p1384215509257"><a name="zh-cn_topic_0221482430_p1384215509257"></a><a name="zh-cn_topic_0221482430_p1384215509257"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p0843650152514"><a name="zh-cn_topic_0221482430_p0843650152514"></a><a name="zh-cn_topic_0221482430_p0843650152514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p4844650182515"><a name="zh-cn_topic_0221482430_p4844650182515"></a><a name="zh-cn_topic_0221482430_p4844650182515"></a>IAM用户名，长度5~32之间，首位不能为数字，特殊字符只能包含下划线“_”、中划线“-”和空格。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row082145013254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p884455011258"><a name="zh-cn_topic_0221482430_p884455011258"></a><a name="zh-cn_topic_0221482430_p884455011258"></a>phone</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p1284505022516"><a name="zh-cn_topic_0221482430_p1284505022516"></a><a name="zh-cn_topic_0221482430_p1284505022516"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p784519503255"><a name="zh-cn_topic_0221482430_p784519503255"></a><a name="zh-cn_topic_0221482430_p784519503255"></a>IAM用户手机号，纯数字，长度小于等于32位。必须与国家码同时存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row1782185019258"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p1184615012517"><a name="zh-cn_topic_0221482430_p1184615012517"></a><a name="zh-cn_topic_0221482430_p1184615012517"></a>is_domain_owner</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p1384735092513"><a name="zh-cn_topic_0221482430_p1384735092513"></a><a name="zh-cn_topic_0221482430_p1384735092513"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p1784719503258"><a name="zh-cn_topic_0221482430_p1784719503258"></a><a name="zh-cn_topic_0221482430_p1784719503258"></a>IAM用户是否为账号<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row8821950132518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p18848105052520"><a name="zh-cn_topic_0221482430_p18848105052520"></a><a name="zh-cn_topic_0221482430_p18848105052520"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p1184912507251"><a name="zh-cn_topic_0221482430_p1184912507251"></a><a name="zh-cn_topic_0221482430_p1184912507251"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p178491450202519"><a name="zh-cn_topic_0221482430_p178491450202519"></a><a name="zh-cn_topic_0221482430_p178491450202519"></a>IAM用户所属账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row182135016258"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p2085014501255"><a name="zh-cn_topic_0221482430_p2085014501255"></a><a name="zh-cn_topic_0221482430_p2085014501255"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p14851145017251"><a name="zh-cn_topic_0221482430_p14851145017251"></a><a name="zh-cn_topic_0221482430_p14851145017251"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p4853850152512"><a name="zh-cn_topic_0221482430_p4853850152512"></a><a name="zh-cn_topic_0221482430_p4853850152512"></a>是否启用IAM用户。true为启用，false为停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row98211550102518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p14854155082515"><a name="zh-cn_topic_0221482430_p14854155082515"></a><a name="zh-cn_topic_0221482430_p14854155082515"></a>areacode</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p985415505257"><a name="zh-cn_topic_0221482430_p985415505257"></a><a name="zh-cn_topic_0221482430_p985415505257"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p6855250172514"><a name="zh-cn_topic_0221482430_p6855250172514"></a><a name="zh-cn_topic_0221482430_p6855250172514"></a>国家码。中国大陆为“0086”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row482155010251"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p58561250112520"><a name="zh-cn_topic_0221482430_p58561250112520"></a><a name="zh-cn_topic_0221482430_p58561250112520"></a>email</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p15857175092517"><a name="zh-cn_topic_0221482430_p15857175092517"></a><a name="zh-cn_topic_0221482430_p15857175092517"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p1285845016257"><a name="zh-cn_topic_0221482430_p1285845016257"></a><a name="zh-cn_topic_0221482430_p1285845016257"></a>IAM用户邮箱。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row198218501254"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p7858105042518"><a name="zh-cn_topic_0221482430_p7858105042518"></a><a name="zh-cn_topic_0221482430_p7858105042518"></a>create_time</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p586014502254"><a name="zh-cn_topic_0221482430_p586014502254"></a><a name="zh-cn_topic_0221482430_p586014502254"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p3861950122515"><a name="zh-cn_topic_0221482430_p3861950122515"></a><a name="zh-cn_topic_0221482430_p3861950122515"></a>IAM用户创建时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row98211050112511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p14862135017252"><a name="zh-cn_topic_0221482430_p14862135017252"></a><a name="zh-cn_topic_0221482430_p14862135017252"></a>default_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p10862350132518"><a name="zh-cn_topic_0221482430_p10862350132518"></a><a name="zh-cn_topic_0221482430_p10862350132518"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p1786325062515"><a name="zh-cn_topic_0221482430_p1786325062515"></a><a name="zh-cn_topic_0221482430_p1786325062515"></a>IAM用户默认项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row1082115017256"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p16864750132519"><a name="zh-cn_topic_0221482430_p16864750132519"></a><a name="zh-cn_topic_0221482430_p16864750132519"></a>xdomain_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p38651504259"><a name="zh-cn_topic_0221482430_p38651504259"></a><a name="zh-cn_topic_0221482430_p38651504259"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p986565052518"><a name="zh-cn_topic_0221482430_p986565052518"></a><a name="zh-cn_topic_0221482430_p986565052518"></a>运营主体的客户编码。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row682235018255"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p48661650172511"><a name="zh-cn_topic_0221482430_p48661650172511"></a><a name="zh-cn_topic_0221482430_p48661650172511"></a>xdomain_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p16867145019254"><a name="zh-cn_topic_0221482430_p16867145019254"></a><a name="zh-cn_topic_0221482430_p16867145019254"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p386815502258"><a name="zh-cn_topic_0221482430_p386815502258"></a><a name="zh-cn_topic_0221482430_p386815502258"></a>运营主体。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row12822450162511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p1986918503258"><a name="zh-cn_topic_0221482430_p1986918503258"></a><a name="zh-cn_topic_0221482430_p1986918503258"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p138701350142512"><a name="zh-cn_topic_0221482430_p138701350142512"></a><a name="zh-cn_topic_0221482430_p138701350142512"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p38711650132518"><a name="zh-cn_topic_0221482430_p38711650132518"></a><a name="zh-cn_topic_0221482430_p38711650132518"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row9822145017253"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482430_p2871135042512"><a name="zh-cn_topic_0221482430_p2871135042512"></a><a name="zh-cn_topic_0221482430_p2871135042512"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482430_p13872125062516"><a name="zh-cn_topic_0221482430_p13872125062516"></a><a name="zh-cn_topic_0221482430_p13872125062516"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482430_p17873350152510"><a name="zh-cn_topic_0221482430_p17873350152510"></a><a name="zh-cn_topic_0221482430_p17873350152510"></a>密码过期时间（UTC时间），“null”表示密码不过期。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482430_section12874125032513"></a>

```
POST https://iam.myhuaweicloud.com/v3.0/OS-USER/users
```

```
{
    "user": {
        "domain_id": "d78cbac186b744899480f25...",
        "name": "IAMUser",
        "password": "IAMPassword@",
        "email": "IAMEmail@huawei.com",
        "areacode": "0086",
        "phone": "12345678910",
        "enabled": true,
        "pwd_status": false,
        "default_project_id": "",
        "xuser_type": "",
        "xuser_id": "",
        "description": "IAMDescription"
    }
}
```

## 响应示例<a name="zh-cn_topic_0221482430_section11884125022515"></a>

**状态码为 201 时:**

创建成功。

```
{
    "user": {
        "pwd_status": false,
        "xuser_id": "",
        "xuser_type": "",
        "description": "IAMDescription",
        "name": "IAMUser",
        "phone": "12345678910",
        "is_domain_owner": false,
        "enabled": true,
        "domain_id": "d78cbac186b744899480f25bd...",
        "areacode": "0086",
        "email": "IAMEmail@huawei.com",
        "create_time": "2020-01-06T08:05:16.000000",
        "default_project_id": "",
        "xdomain_id": "",
        "xdomain_type": "",
        "id": "07664aec578026691f00c003a..."
    }
}
```

## 返回值<a name="zh-cn_topic_0221482430_section1147551202513"></a>

<a name="zh-cn_topic_0221482430_table2454"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482430_row2899850192514"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482430_p44715119255"><a name="zh-cn_topic_0221482430_p44715119255"></a><a name="zh-cn_topic_0221482430_p44715119255"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482430_p12481951162518"><a name="zh-cn_topic_0221482430_p12481951162518"></a><a name="zh-cn_topic_0221482430_p12481951162518"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482430_row1589905012517"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482430_p1048115122510"><a name="zh-cn_topic_0221482430_p1048115122510"></a><a name="zh-cn_topic_0221482430_p1048115122510"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482430_p1948165120257"><a name="zh-cn_topic_0221482430_p1948165120257"></a><a name="zh-cn_topic_0221482430_p1948165120257"></a>创建成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row78991750122520"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482430_p1948051162516"><a name="zh-cn_topic_0221482430_p1948051162516"></a><a name="zh-cn_topic_0221482430_p1948051162516"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482430_p104985132512"><a name="zh-cn_topic_0221482430_p104985132512"></a><a name="zh-cn_topic_0221482430_p104985132512"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row489945032515"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482430_p54985152514"><a name="zh-cn_topic_0221482430_p54985152514"></a><a name="zh-cn_topic_0221482430_p54985152514"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482430_p649251102513"><a name="zh-cn_topic_0221482430_p649251102513"></a><a name="zh-cn_topic_0221482430_p649251102513"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row19899115052510"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482430_p249651162511"><a name="zh-cn_topic_0221482430_p249651162511"></a><a name="zh-cn_topic_0221482430_p249651162511"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482430_p850115117259"><a name="zh-cn_topic_0221482430_p850115117259"></a><a name="zh-cn_topic_0221482430_p850115117259"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row88991750182514"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482430_p1250175117250"><a name="zh-cn_topic_0221482430_p1250175117250"></a><a name="zh-cn_topic_0221482430_p1250175117250"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482430_p1850651122518"><a name="zh-cn_topic_0221482430_p1850651122518"></a><a name="zh-cn_topic_0221482430_p1850651122518"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row118991450132518"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482430_p1251551162516"><a name="zh-cn_topic_0221482430_p1251551162516"></a><a name="zh-cn_topic_0221482430_p1251551162516"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482430_p1515516255"><a name="zh-cn_topic_0221482430_p1515516255"></a><a name="zh-cn_topic_0221482430_p1515516255"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row58991550132513"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482430_p55165117251"><a name="zh-cn_topic_0221482430_p55165117251"></a><a name="zh-cn_topic_0221482430_p55165117251"></a>409</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482430_p251145172511"><a name="zh-cn_topic_0221482430_p251145172511"></a><a name="zh-cn_topic_0221482430_p251145172511"></a>资源冲突。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row14900165018251"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482430_p14526514250"><a name="zh-cn_topic_0221482430_p14526514250"></a><a name="zh-cn_topic_0221482430_p14526514250"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482430_p35295113253"><a name="zh-cn_topic_0221482430_p35295113253"></a><a name="zh-cn_topic_0221482430_p35295113253"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row79008501255"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482430_p145245172517"><a name="zh-cn_topic_0221482430_p145245172517"></a><a name="zh-cn_topic_0221482430_p145245172517"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482430_p5535519251"><a name="zh-cn_topic_0221482430_p5535519251"></a><a name="zh-cn_topic_0221482430_p5535519251"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row490014508257"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482430_p1553451202513"><a name="zh-cn_topic_0221482430_p1553451202513"></a><a name="zh-cn_topic_0221482430_p1553451202513"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482430_p1053175116252"><a name="zh-cn_topic_0221482430_p1053175116252"></a><a name="zh-cn_topic_0221482430_p1053175116252"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482430_section195413515254"></a>

<a name="zh-cn_topic_0221482430_table2455"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482430_row9914155002517"><th class="cellrowborder" valign="top" width="27.27272727272727%" id="mcps1.1.4.1.1"><p id="zh-cn_topic_0221482430_p1155951182511"><a name="zh-cn_topic_0221482430_p1155951182511"></a><a name="zh-cn_topic_0221482430_p1155951182511"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="36.36363636363636%" id="mcps1.1.4.1.2"><p id="zh-cn_topic_0221482430_p155175152512"><a name="zh-cn_topic_0221482430_p155175152512"></a><a name="zh-cn_topic_0221482430_p155175152512"></a>错误码</p>
</th>
<th class="cellrowborder" valign="top" width="36.36363636363636%" id="mcps1.1.4.1.3"><p id="zh-cn_topic_0221482430_p1055115112258"><a name="zh-cn_topic_0221482430_p1055115112258"></a><a name="zh-cn_topic_0221482430_p1055115112258"></a>错误信息</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482430_row1491415509255"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p056851112513"><a name="zh-cn_topic_0221482430_p056851112513"></a><a name="zh-cn_topic_0221482430_p056851112513"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p135610518251"><a name="zh-cn_topic_0221482430_p135610518251"></a><a name="zh-cn_topic_0221482430_p135610518251"></a>1100</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p1757185115259"><a name="zh-cn_topic_0221482430_p1757185115259"></a><a name="zh-cn_topic_0221482430_p1757185115259"></a>缺失必选参数。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row491425032511"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p1571351112519"><a name="zh-cn_topic_0221482430_p1571351112519"></a><a name="zh-cn_topic_0221482430_p1571351112519"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p6581951192516"><a name="zh-cn_topic_0221482430_p6581951192516"></a><a name="zh-cn_topic_0221482430_p6581951192516"></a>1101</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p358155116257"><a name="zh-cn_topic_0221482430_p358155116257"></a><a name="zh-cn_topic_0221482430_p358155116257"></a>用户名校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row2091445032510"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p17593518251"><a name="zh-cn_topic_0221482430_p17593518251"></a><a name="zh-cn_topic_0221482430_p17593518251"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p659451102517"><a name="zh-cn_topic_0221482430_p659451102517"></a><a name="zh-cn_topic_0221482430_p659451102517"></a>1102</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p1959145162510"><a name="zh-cn_topic_0221482430_p1959145162510"></a><a name="zh-cn_topic_0221482430_p1959145162510"></a>邮箱校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row1691565010251"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p1060951122511"><a name="zh-cn_topic_0221482430_p1060951122511"></a><a name="zh-cn_topic_0221482430_p1060951122511"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p13604519258"><a name="zh-cn_topic_0221482430_p13604519258"></a><a name="zh-cn_topic_0221482430_p13604519258"></a>1103</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p1861175111257"><a name="zh-cn_topic_0221482430_p1861175111257"></a><a name="zh-cn_topic_0221482430_p1861175111257"></a>密码校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row13915145042513"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p1961105115254"><a name="zh-cn_topic_0221482430_p1961105115254"></a><a name="zh-cn_topic_0221482430_p1961105115254"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p96235110259"><a name="zh-cn_topic_0221482430_p96235110259"></a><a name="zh-cn_topic_0221482430_p96235110259"></a>1104</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p15621513253"><a name="zh-cn_topic_0221482430_p15621513253"></a><a name="zh-cn_topic_0221482430_p15621513253"></a>手机号校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row12915135012252"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p263195172518"><a name="zh-cn_topic_0221482430_p263195172518"></a><a name="zh-cn_topic_0221482430_p263195172518"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p126315116256"><a name="zh-cn_topic_0221482430_p126315116256"></a><a name="zh-cn_topic_0221482430_p126315116256"></a>1105</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p4631451132511"><a name="zh-cn_topic_0221482430_p4631451132511"></a><a name="zh-cn_topic_0221482430_p4631451132511"></a>xuser_type必须与xdomain_type相同。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row1591512501252"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p464185115250"><a name="zh-cn_topic_0221482430_p464185115250"></a><a name="zh-cn_topic_0221482430_p464185115250"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p1364195111254"><a name="zh-cn_topic_0221482430_p1364195111254"></a><a name="zh-cn_topic_0221482430_p1364195111254"></a>1106</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p16435152517"><a name="zh-cn_topic_0221482430_p16435152517"></a><a name="zh-cn_topic_0221482430_p16435152517"></a>国家码、手机号必须同时存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row18915185022513"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p4651851132516"><a name="zh-cn_topic_0221482430_p4651851132516"></a><a name="zh-cn_topic_0221482430_p4651851132516"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p106545113255"><a name="zh-cn_topic_0221482430_p106545113255"></a><a name="zh-cn_topic_0221482430_p106545113255"></a>1107</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p065175142514"><a name="zh-cn_topic_0221482430_p065175142514"></a><a name="zh-cn_topic_0221482430_p065175142514"></a>账号管理员不能被删除。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row691525072516"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p465251102517"><a name="zh-cn_topic_0221482430_p465251102517"></a><a name="zh-cn_topic_0221482430_p465251102517"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p56665122511"><a name="zh-cn_topic_0221482430_p56665122511"></a><a name="zh-cn_topic_0221482430_p56665122511"></a>1108</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p1466115122514"><a name="zh-cn_topic_0221482430_p1466115122514"></a><a name="zh-cn_topic_0221482430_p1466115122514"></a>新密码不能与原密码相同。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row4915115012517"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p176718510255"><a name="zh-cn_topic_0221482430_p176718510255"></a><a name="zh-cn_topic_0221482430_p176718510255"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p176725182515"><a name="zh-cn_topic_0221482430_p176725182515"></a><a name="zh-cn_topic_0221482430_p176725182515"></a>1109</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p1067185192518"><a name="zh-cn_topic_0221482430_p1067185192518"></a><a name="zh-cn_topic_0221482430_p1067185192518"></a>用户名已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row18915205015256"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p196895162518"><a name="zh-cn_topic_0221482430_p196895162518"></a><a name="zh-cn_topic_0221482430_p196895162518"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p1681551202520"><a name="zh-cn_topic_0221482430_p1681551202520"></a><a name="zh-cn_topic_0221482430_p1681551202520"></a>1110</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p26875117253"><a name="zh-cn_topic_0221482430_p26875117253"></a><a name="zh-cn_topic_0221482430_p26875117253"></a>邮箱已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row29161950172519"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p1369551122510"><a name="zh-cn_topic_0221482430_p1369551122510"></a><a name="zh-cn_topic_0221482430_p1369551122510"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p1469651162515"><a name="zh-cn_topic_0221482430_p1469651162515"></a><a name="zh-cn_topic_0221482430_p1469651162515"></a>1111</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p19691651182510"><a name="zh-cn_topic_0221482430_p19691651182510"></a><a name="zh-cn_topic_0221482430_p19691651182510"></a>手机号已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row189161350142519"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p177095122517"><a name="zh-cn_topic_0221482430_p177095122517"></a><a name="zh-cn_topic_0221482430_p177095122517"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p670105113255"><a name="zh-cn_topic_0221482430_p670105113255"></a><a name="zh-cn_topic_0221482430_p670105113255"></a>1113</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p57018512254"><a name="zh-cn_topic_0221482430_p57018512254"></a><a name="zh-cn_topic_0221482430_p57018512254"></a>xuser_id、xuser_type已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row1191675012510"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p1071115152517"><a name="zh-cn_topic_0221482430_p1071115152517"></a><a name="zh-cn_topic_0221482430_p1071115152517"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p27245172514"><a name="zh-cn_topic_0221482430_p27245172514"></a><a name="zh-cn_topic_0221482430_p27245172514"></a>1115</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p2721651172510"><a name="zh-cn_topic_0221482430_p2721651172510"></a><a name="zh-cn_topic_0221482430_p2721651172510"></a>IAM用户数量达到最大限制。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482430_row1691610508257"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482430_p1472185120254"><a name="zh-cn_topic_0221482430_p1472185120254"></a><a name="zh-cn_topic_0221482430_p1472185120254"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482430_p47325110257"><a name="zh-cn_topic_0221482430_p47325110257"></a><a name="zh-cn_topic_0221482430_p47325110257"></a>1117</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482430_p17416510253"><a name="zh-cn_topic_0221482430_p17416510253"></a><a name="zh-cn_topic_0221482430_p17416510253"></a>用户描述校验失败。</p>
</td>
</tr>
</tbody>
</table>

