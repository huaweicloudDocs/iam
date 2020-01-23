# 管理员修改IAM用户信息（推荐）<a name="iam_08_0011"></a>

## 功能介绍<a name="zh-cn_topic_0221482439_section13155155913310"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/zh-cn_topic_0079496985.html)修改IAM用户信息 。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="zh-cn_topic_0221482439_section111801059193111"></a>

PUT /v3.0/OS-USER/users/\{user\_id\}

**表 1**  路径参数

<a name="zh-cn_topic_0221482439_table919325911315"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482439_row9191959103110"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482439_p16196105915314"><a name="zh-cn_topic_0221482439_p16196105915314"></a><a name="zh-cn_topic_0221482439_p16196105915314"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482439_p18202145953120"><a name="zh-cn_topic_0221482439_p18202145953120"></a><a name="zh-cn_topic_0221482439_p18202145953120"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482439_p15208185953110"><a name="zh-cn_topic_0221482439_p15208185953110"></a><a name="zh-cn_topic_0221482439_p15208185953110"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482439_p12217115973111"><a name="zh-cn_topic_0221482439_p12217115973111"></a><a name="zh-cn_topic_0221482439_p12217115973111"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482439_row1919113592310"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p11222105910318"><a name="zh-cn_topic_0221482439_p11222105910318"></a><a name="zh-cn_topic_0221482439_p11222105910318"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p14226115913113"><a name="zh-cn_topic_0221482439_p14226115913113"></a><a name="zh-cn_topic_0221482439_p14226115913113"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p1023275911313"><a name="zh-cn_topic_0221482439_p1023275911313"></a><a name="zh-cn_topic_0221482439_p1023275911313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p32391559143119"><a name="zh-cn_topic_0221482439_p32391559143119"></a><a name="zh-cn_topic_0221482439_p32391559143119"></a>待修改信息的IAM用户ID，获取方式请参见：<a href="获取IAM用户-项目-用户组的名称和ID.md">获取IAM用户、项目、用户组的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482439_section13247135953113"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482439_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482439_row1625917593318"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482439_p6267165943111"><a name="zh-cn_topic_0221482439_p6267165943111"></a><a name="zh-cn_topic_0221482439_p6267165943111"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482439_p427285913314"><a name="zh-cn_topic_0221482439_p427285913314"></a><a name="zh-cn_topic_0221482439_p427285913314"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482439_p1727765910315"><a name="zh-cn_topic_0221482439_p1727765910315"></a><a name="zh-cn_topic_0221482439_p1727765910315"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482439_p92822595319"><a name="zh-cn_topic_0221482439_p92822595319"></a><a name="zh-cn_topic_0221482439_p92822595319"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482439_row13260859193110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p182871459183117"><a name="zh-cn_topic_0221482439_p182871459183117"></a><a name="zh-cn_topic_0221482439_p182871459183117"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p1129175933111"><a name="zh-cn_topic_0221482439_p1129175933111"></a><a name="zh-cn_topic_0221482439_p1129175933111"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p129875915319"><a name="zh-cn_topic_0221482439_p129875915319"></a><a name="zh-cn_topic_0221482439_p129875915319"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p16303159163113"><a name="zh-cn_topic_0221482439_p16303159163113"></a><a name="zh-cn_topic_0221482439_p16303159163113"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row11260115973117"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p73101259153116"><a name="zh-cn_topic_0221482439_p73101259153116"></a><a name="zh-cn_topic_0221482439_p73101259153116"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p113151859113118"><a name="zh-cn_topic_0221482439_p113151859113118"></a><a name="zh-cn_topic_0221482439_p113151859113118"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p33201859173118"><a name="zh-cn_topic_0221482439_p33201859173118"></a><a name="zh-cn_topic_0221482439_p33201859173118"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p632725918311"><a name="zh-cn_topic_0221482439_p632725918311"></a><a name="zh-cn_topic_0221482439_p632725918311"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="zh-cn_topic_0221482439_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482439_row163321759113120"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482439_p1033965915314"><a name="zh-cn_topic_0221482439_p1033965915314"></a><a name="zh-cn_topic_0221482439_p1033965915314"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482439_p123454598318"><a name="zh-cn_topic_0221482439_p123454598318"></a><a name="zh-cn_topic_0221482439_p123454598318"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482439_p1835214598314"><a name="zh-cn_topic_0221482439_p1835214598314"></a><a name="zh-cn_topic_0221482439_p1835214598314"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482439_p18359559123115"><a name="zh-cn_topic_0221482439_p18359559123115"></a><a name="zh-cn_topic_0221482439_p18359559123115"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482439_row633220596312"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p14364105943111"><a name="zh-cn_topic_0221482439_p14364105943111"></a><a name="zh-cn_topic_0221482439_p14364105943111"></a><a href="#zh-cn_topic_0221482439_request_Rq810User">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p1368195917311"><a name="zh-cn_topic_0221482439_p1368195917311"></a><a name="zh-cn_topic_0221482439_p1368195917311"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p1437515912313"><a name="zh-cn_topic_0221482439_p1437515912313"></a><a name="zh-cn_topic_0221482439_p1437515912313"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p9380195918312"><a name="zh-cn_topic_0221482439_p9380195918312"></a><a name="zh-cn_topic_0221482439_p9380195918312"></a>IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  user

<a name="zh-cn_topic_0221482439_request_Rq810User"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482439_row163841598315"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482439_p43911459113113"><a name="zh-cn_topic_0221482439_p43911459113113"></a><a name="zh-cn_topic_0221482439_p43911459113113"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482439_p1239575963111"><a name="zh-cn_topic_0221482439_p1239575963111"></a><a name="zh-cn_topic_0221482439_p1239575963111"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482439_p7400159143112"><a name="zh-cn_topic_0221482439_p7400159143112"></a><a name="zh-cn_topic_0221482439_p7400159143112"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482439_p4406165912313"><a name="zh-cn_topic_0221482439_p4406165912313"></a><a name="zh-cn_topic_0221482439_p4406165912313"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482439_row173841459123110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p18410195919314"><a name="zh-cn_topic_0221482439_p18410195919314"></a><a name="zh-cn_topic_0221482439_p18410195919314"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p441475923118"><a name="zh-cn_topic_0221482439_p441475923118"></a><a name="zh-cn_topic_0221482439_p441475923118"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p1242085914313"><a name="zh-cn_topic_0221482439_p1242085914313"></a><a name="zh-cn_topic_0221482439_p1242085914313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p13425125913111"><a name="zh-cn_topic_0221482439_p13425125913111"></a><a name="zh-cn_topic_0221482439_p13425125913111"></a>新IAM用户名，长度5~32之间，首位不能为数字，特殊字符只能包含下划线“_”、中划线“-”和空格。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row83841859133112"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p12429959113118"><a name="zh-cn_topic_0221482439_p12429959113118"></a><a name="zh-cn_topic_0221482439_p12429959113118"></a>password</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p13435195993117"><a name="zh-cn_topic_0221482439_p13435195993117"></a><a name="zh-cn_topic_0221482439_p13435195993117"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p144401759103111"><a name="zh-cn_topic_0221482439_p144401759103111"></a><a name="zh-cn_topic_0221482439_p144401759103111"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p1144510594314"><a name="zh-cn_topic_0221482439_p1144510594314"></a><a name="zh-cn_topic_0221482439_p1144510594314"></a>IAM用户新密码。</p>
<a name="zh-cn_topic_0221482439_ul14452559183112"></a><a name="zh-cn_topic_0221482439_ul14452559183112"></a><ul id="zh-cn_topic_0221482439_ul14452559183112"><li>系统默认密码最小长度为6位字符，在6-32位之间支持用户自定义密码长度。</li><li>至少包含以下四种字符中的两种： 大写字母、小写字母、数字和特殊字符。</li><li>不能包含手机号和邮箱。</li><li>必须满足账户设置中<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0607.html" target="_blank" rel="noopener noreferrer">密码策略</a>的要求。</li><li>新密码不能与当前密码相同。</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row11384145913316"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p7485759203119"><a name="zh-cn_topic_0221482439_p7485759203119"></a><a name="zh-cn_topic_0221482439_p7485759203119"></a>email</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p2490115993113"><a name="zh-cn_topic_0221482439_p2490115993113"></a><a name="zh-cn_topic_0221482439_p2490115993113"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p249805917313"><a name="zh-cn_topic_0221482439_p249805917313"></a><a name="zh-cn_topic_0221482439_p249805917313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p5502145963118"><a name="zh-cn_topic_0221482439_p5502145963118"></a><a name="zh-cn_topic_0221482439_p5502145963118"></a>IAM用户新邮箱，需符合邮箱格式，长度小于等于255字节。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row2038419595315"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p1250635917319"><a name="zh-cn_topic_0221482439_p1250635917319"></a><a name="zh-cn_topic_0221482439_p1250635917319"></a>areacode</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p1051165919314"><a name="zh-cn_topic_0221482439_p1051165919314"></a><a name="zh-cn_topic_0221482439_p1051165919314"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p751685993111"><a name="zh-cn_topic_0221482439_p751685993111"></a><a name="zh-cn_topic_0221482439_p751685993111"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p1952115590315"><a name="zh-cn_topic_0221482439_p1952115590315"></a><a name="zh-cn_topic_0221482439_p1952115590315"></a>国家码。必须与手机号同时存在。中国大陆为“0086”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row63851659143117"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p12528359143110"><a name="zh-cn_topic_0221482439_p12528359143110"></a><a name="zh-cn_topic_0221482439_p12528359143110"></a>phone</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p353445915310"><a name="zh-cn_topic_0221482439_p353445915310"></a><a name="zh-cn_topic_0221482439_p353445915310"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p115392597317"><a name="zh-cn_topic_0221482439_p115392597317"></a><a name="zh-cn_topic_0221482439_p115392597317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p55491159183118"><a name="zh-cn_topic_0221482439_p55491159183118"></a><a name="zh-cn_topic_0221482439_p55491159183118"></a>IAM用户新手机号，纯数字，长度小于等于32位。必须与国家码同时存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1238511594317"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p25536599319"><a name="zh-cn_topic_0221482439_p25536599319"></a><a name="zh-cn_topic_0221482439_p25536599319"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p65631559143112"><a name="zh-cn_topic_0221482439_p65631559143112"></a><a name="zh-cn_topic_0221482439_p65631559143112"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p1256885983116"><a name="zh-cn_topic_0221482439_p1256885983116"></a><a name="zh-cn_topic_0221482439_p1256885983116"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p857419591310"><a name="zh-cn_topic_0221482439_p857419591310"></a><a name="zh-cn_topic_0221482439_p857419591310"></a>是否启用IAM用户。true为启用，false为停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row038555973118"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p158065963117"><a name="zh-cn_topic_0221482439_p158065963117"></a><a name="zh-cn_topic_0221482439_p158065963117"></a>pwd_status</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p75851859123120"><a name="zh-cn_topic_0221482439_p75851859123120"></a><a name="zh-cn_topic_0221482439_p75851859123120"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p45951859123116"><a name="zh-cn_topic_0221482439_p45951859123116"></a><a name="zh-cn_topic_0221482439_p45951859123116"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p1601959153118"><a name="zh-cn_topic_0221482439_p1601959153118"></a><a name="zh-cn_topic_0221482439_p1601959153118"></a>IAM用户密码状态。true：需要修改密码，false：正常。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row938515597315"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p4612135903117"><a name="zh-cn_topic_0221482439_p4612135903117"></a><a name="zh-cn_topic_0221482439_p4612135903117"></a>xuser_type</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p196179596318"><a name="zh-cn_topic_0221482439_p196179596318"></a><a name="zh-cn_topic_0221482439_p196179596318"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p962514596313"><a name="zh-cn_topic_0221482439_p962514596313"></a><a name="zh-cn_topic_0221482439_p962514596313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p1663125916315"><a name="zh-cn_topic_0221482439_p1663125916315"></a><a name="zh-cn_topic_0221482439_p1663125916315"></a>IAM用户在外部系统中的类型。长度小于等于64位。xuser_type如果存在，则需要与同一租户中的xaccount_type、xdomain_type校验，须与xuser_id同时存在。</p>
<div class="note" id="zh-cn_topic_0221482439_note186423592315"><a name="zh-cn_topic_0221482439_note186423592315"></a><a name="zh-cn_topic_0221482439_note186423592315"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0221482439_p3648259163114"><a name="zh-cn_topic_0221482439_p3648259163114"></a><a name="zh-cn_topic_0221482439_p3648259163114"></a>外部系统指与华为云对接的外部企业管理系统，xaccount_type、xaccount_id、xdomain_type、xdomain_id、xuser_type、xuser_id等参数值，无法在华为云获取，请咨询企业管理员。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row2038565917314"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p76530598319"><a name="zh-cn_topic_0221482439_p76530598319"></a><a name="zh-cn_topic_0221482439_p76530598319"></a>xuser_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p14658175973110"><a name="zh-cn_topic_0221482439_p14658175973110"></a><a name="zh-cn_topic_0221482439_p14658175973110"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p566315919317"><a name="zh-cn_topic_0221482439_p566315919317"></a><a name="zh-cn_topic_0221482439_p566315919317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p1066816599315"><a name="zh-cn_topic_0221482439_p1066816599315"></a><a name="zh-cn_topic_0221482439_p1066816599315"></a>IAM用户在外部系统中的ID。长度小于等于128位，必须与xuser_type同时存在。</p>
<div class="note" id="zh-cn_topic_0221482439_note1467865916315"><a name="zh-cn_topic_0221482439_note1467865916315"></a><a name="zh-cn_topic_0221482439_note1467865916315"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0221482439_p1068445983113"><a name="zh-cn_topic_0221482439_p1068445983113"></a><a name="zh-cn_topic_0221482439_p1068445983113"></a>外部系统指与华为云对接的外部企业管理系统，xaccount_type、xaccount_id、xdomain_type、xdomain_id、xuser_type、xuser_id等参数值，无法在华为云获取，请咨询企业管理员。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1238525913319"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p8688959153111"><a name="zh-cn_topic_0221482439_p8688959153111"></a><a name="zh-cn_topic_0221482439_p8688959153111"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p9693559113119"><a name="zh-cn_topic_0221482439_p9693559113119"></a><a name="zh-cn_topic_0221482439_p9693559113119"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p2697559173114"><a name="zh-cn_topic_0221482439_p2697559173114"></a><a name="zh-cn_topic_0221482439_p2697559173114"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p57011859103114"><a name="zh-cn_topic_0221482439_p57011859103114"></a><a name="zh-cn_topic_0221482439_p57011859103114"></a>IAM用户新描述信息。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482439_section7708135983114"></a>

**表 5**  响应Body参数

<a name="zh-cn_topic_0221482439_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482439_row971685953114"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482439_p37224590319"><a name="zh-cn_topic_0221482439_p37224590319"></a><a name="zh-cn_topic_0221482439_p37224590319"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482439_p87272590314"><a name="zh-cn_topic_0221482439_p87272590314"></a><a name="zh-cn_topic_0221482439_p87272590314"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482439_p1373185912310"><a name="zh-cn_topic_0221482439_p1373185912310"></a><a name="zh-cn_topic_0221482439_p1373185912310"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482439_row671611594311"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p197351159123110"><a name="zh-cn_topic_0221482439_p197351159123110"></a><a name="zh-cn_topic_0221482439_p197351159123110"></a><a href="#zh-cn_topic_0221482439_response_Rs810User">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p117401459143114"><a name="zh-cn_topic_0221482439_p117401459143114"></a><a name="zh-cn_topic_0221482439_p117401459143114"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p6744359193116"><a name="zh-cn_topic_0221482439_p6744359193116"></a><a name="zh-cn_topic_0221482439_p6744359193116"></a>IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  user

<a name="zh-cn_topic_0221482439_response_Rs810User"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482439_row1974825933119"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482439_p575335913311"><a name="zh-cn_topic_0221482439_p575335913311"></a><a name="zh-cn_topic_0221482439_p575335913311"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482439_p6757135963113"><a name="zh-cn_topic_0221482439_p6757135963113"></a><a name="zh-cn_topic_0221482439_p6757135963113"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482439_p0762059123118"><a name="zh-cn_topic_0221482439_p0762059123118"></a><a name="zh-cn_topic_0221482439_p0762059123118"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482439_row07484596312"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p1076615993116"><a name="zh-cn_topic_0221482439_p1076615993116"></a><a name="zh-cn_topic_0221482439_p1076615993116"></a>pwd_status</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p157701459123120"><a name="zh-cn_topic_0221482439_p157701459123120"></a><a name="zh-cn_topic_0221482439_p157701459123120"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p4776959203115"><a name="zh-cn_topic_0221482439_p4776959203115"></a><a name="zh-cn_topic_0221482439_p4776959203115"></a>IAM用户密码状态。true：需要修改密码，false：正常。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row19748135933114"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p17781105953113"><a name="zh-cn_topic_0221482439_p17781105953113"></a><a name="zh-cn_topic_0221482439_p17781105953113"></a>xuser_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p15785125917312"><a name="zh-cn_topic_0221482439_p15785125917312"></a><a name="zh-cn_topic_0221482439_p15785125917312"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p137901159123119"><a name="zh-cn_topic_0221482439_p137901159123119"></a><a name="zh-cn_topic_0221482439_p137901159123119"></a>IAM用户在外部系统中的ID。</p>
<div class="note" id="zh-cn_topic_0221482439_note0801115916318"><a name="zh-cn_topic_0221482439_note0801115916318"></a><a name="zh-cn_topic_0221482439_note0801115916318"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0221482439_p19808105983114"><a name="zh-cn_topic_0221482439_p19808105983114"></a><a name="zh-cn_topic_0221482439_p19808105983114"></a>外部系统指与华为云对接的外部企业管理系统，xaccount_type、xaccount_id、xdomain_type、xdomain_id、xuser_type、xuser_id等参数值，无法在华为云获取，请咨询企业管理员。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1748185912319"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p1081245973117"><a name="zh-cn_topic_0221482439_p1081245973117"></a><a name="zh-cn_topic_0221482439_p1081245973117"></a>xuser_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p4817175919312"><a name="zh-cn_topic_0221482439_p4817175919312"></a><a name="zh-cn_topic_0221482439_p4817175919312"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p982155993119"><a name="zh-cn_topic_0221482439_p982155993119"></a><a name="zh-cn_topic_0221482439_p982155993119"></a>IAM用户在外部系统中的类型。</p>
<div class="note" id="zh-cn_topic_0221482439_note28311259183118"><a name="zh-cn_topic_0221482439_note28311259183118"></a><a name="zh-cn_topic_0221482439_note28311259183118"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0221482439_p58371759103113"><a name="zh-cn_topic_0221482439_p58371759103113"></a><a name="zh-cn_topic_0221482439_p58371759103113"></a>外部系统指与华为云对接的外部企业管理系统，xaccount_type、xaccount_id、xdomain_type、xdomain_id、xuser_type、xuser_id等参数值，无法在华为云获取，请咨询企业管理员。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row174885993119"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p084125912310"><a name="zh-cn_topic_0221482439_p084125912310"></a><a name="zh-cn_topic_0221482439_p084125912310"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p19846195916315"><a name="zh-cn_topic_0221482439_p19846195916315"></a><a name="zh-cn_topic_0221482439_p19846195916315"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p2085195918319"><a name="zh-cn_topic_0221482439_p2085195918319"></a><a name="zh-cn_topic_0221482439_p2085195918319"></a>IAM用户的新描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1474814598317"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p1185725918312"><a name="zh-cn_topic_0221482439_p1185725918312"></a><a name="zh-cn_topic_0221482439_p1185725918312"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p13863105903117"><a name="zh-cn_topic_0221482439_p13863105903117"></a><a name="zh-cn_topic_0221482439_p13863105903117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p9868155983117"><a name="zh-cn_topic_0221482439_p9868155983117"></a><a name="zh-cn_topic_0221482439_p9868155983117"></a>IAM用户新用户名，长度5~32之间，首位不能为数字，特殊字符只能包含下划线“_”、中划线“-”和空格。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row77481559103112"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p1487410591318"><a name="zh-cn_topic_0221482439_p1487410591318"></a><a name="zh-cn_topic_0221482439_p1487410591318"></a>phone</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p487975910314"><a name="zh-cn_topic_0221482439_p487975910314"></a><a name="zh-cn_topic_0221482439_p487975910314"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p78841559123119"><a name="zh-cn_topic_0221482439_p78841559123119"></a><a name="zh-cn_topic_0221482439_p78841559123119"></a>IAM用户新手机号，纯数字，长度小于等于32位。必须与国家码同时存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row10748205933116"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p48911859133114"><a name="zh-cn_topic_0221482439_p48911859133114"></a><a name="zh-cn_topic_0221482439_p48911859133114"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p1989685983114"><a name="zh-cn_topic_0221482439_p1989685983114"></a><a name="zh-cn_topic_0221482439_p1989685983114"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p490175913318"><a name="zh-cn_topic_0221482439_p490175913318"></a><a name="zh-cn_topic_0221482439_p490175913318"></a>IAM用户所属账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row18748959143119"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p169064595314"><a name="zh-cn_topic_0221482439_p169064595314"></a><a name="zh-cn_topic_0221482439_p169064595314"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p491115973115"><a name="zh-cn_topic_0221482439_p491115973115"></a><a name="zh-cn_topic_0221482439_p491115973115"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p29161459133112"><a name="zh-cn_topic_0221482439_p29161459133112"></a><a name="zh-cn_topic_0221482439_p29161459133112"></a>是否启用IAM用户。true为启用，false为停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1874925913112"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p179221759163118"><a name="zh-cn_topic_0221482439_p179221759163118"></a><a name="zh-cn_topic_0221482439_p179221759163118"></a>areacode</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p17927165911319"><a name="zh-cn_topic_0221482439_p17927165911319"></a><a name="zh-cn_topic_0221482439_p17927165911319"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p18932205943113"><a name="zh-cn_topic_0221482439_p18932205943113"></a><a name="zh-cn_topic_0221482439_p18932205943113"></a>国家码。中国大陆为“0086”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row574965933120"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p179373592312"><a name="zh-cn_topic_0221482439_p179373592312"></a><a name="zh-cn_topic_0221482439_p179373592312"></a>email</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p994219592310"><a name="zh-cn_topic_0221482439_p994219592310"></a><a name="zh-cn_topic_0221482439_p994219592310"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p09471659173113"><a name="zh-cn_topic_0221482439_p09471659173113"></a><a name="zh-cn_topic_0221482439_p09471659173113"></a>IAM用户新邮箱。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1874920599310"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p795285916316"><a name="zh-cn_topic_0221482439_p795285916316"></a><a name="zh-cn_topic_0221482439_p795285916316"></a>default_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p095705912316"><a name="zh-cn_topic_0221482439_p095705912316"></a><a name="zh-cn_topic_0221482439_p095705912316"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p10961135918317"><a name="zh-cn_topic_0221482439_p10961135918317"></a><a name="zh-cn_topic_0221482439_p10961135918317"></a>IAM用户默认项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1774935915310"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p69681659103119"><a name="zh-cn_topic_0221482439_p69681659103119"></a><a name="zh-cn_topic_0221482439_p69681659103119"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p297325914317"><a name="zh-cn_topic_0221482439_p297325914317"></a><a name="zh-cn_topic_0221482439_p297325914317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p1981105933112"><a name="zh-cn_topic_0221482439_p1981105933112"></a><a name="zh-cn_topic_0221482439_p1981105933112"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1474920593315"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p49864596319"><a name="zh-cn_topic_0221482439_p49864596319"></a><a name="zh-cn_topic_0221482439_p49864596319"></a><a href="#zh-cn_topic_0221482439_response_Rs810UserLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p1699215915314"><a name="zh-cn_topic_0221482439_p1699215915314"></a><a name="zh-cn_topic_0221482439_p1699215915314"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p6999145918312"><a name="zh-cn_topic_0221482439_p6999145918312"></a><a name="zh-cn_topic_0221482439_p6999145918312"></a>IAM用户的资源链接信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row167492591310"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p14518093220"><a name="zh-cn_topic_0221482439_p14518093220"></a><a name="zh-cn_topic_0221482439_p14518093220"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p191019093212"><a name="zh-cn_topic_0221482439_p191019093212"></a><a name="zh-cn_topic_0221482439_p191019093212"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p4164010324"><a name="zh-cn_topic_0221482439_p4164010324"></a><a name="zh-cn_topic_0221482439_p4164010324"></a>密码过期时间（UTC时间），“null”表示密码不过期。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  user.links

<a name="zh-cn_topic_0221482439_response_Rs810UserLinks"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482439_row421709327"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482439_p10280014329"><a name="zh-cn_topic_0221482439_p10280014329"></a><a name="zh-cn_topic_0221482439_p10280014329"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482439_p4336073210"><a name="zh-cn_topic_0221482439_p4336073210"></a><a name="zh-cn_topic_0221482439_p4336073210"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482439_p1439150173213"><a name="zh-cn_topic_0221482439_p1439150173213"></a><a name="zh-cn_topic_0221482439_p1439150173213"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482439_row92115018324"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p12453018321"><a name="zh-cn_topic_0221482439_p12453018321"></a><a name="zh-cn_topic_0221482439_p12453018321"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p11504016328"><a name="zh-cn_topic_0221482439_p11504016328"></a><a name="zh-cn_topic_0221482439_p11504016328"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p105517063210"><a name="zh-cn_topic_0221482439_p105517063210"></a><a name="zh-cn_topic_0221482439_p105517063210"></a>资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482439_section206020203212"></a>

```
PUT https://iam.myhuaweicloud.com/v3.0/OS-USER/users/{user_id}
```

```
{
    "user": {
        "email": "IAMEmail@huawei.com",
        "areacode": "0086",
        "phone": "12345678910",
        "enabled": true,
        "name": "IAMUser",
        "password": "IAMPassword@",
        "pwd_status": false,
        "xuser_type": "",
        "xuser_id": "",
        "description": "IAMDescription"
    }
}
```

## 响应示例<a name="zh-cn_topic_0221482439_section41351204327"></a>

**状态码为 200 时:**

请求成功。

```
{
    "user": {
        "default_project_id": "",
        "description": "IAMDescription",
        "areacode": "0086",
        "enabled": true,
        "pwd_status": false,
        "xuser_id": "",
        "domain_id": "d78cbac186b744899480f25bd022f468",
        "phone": "12345678910",
        "name": "IAMUser",
        "links": {
            "self": "https://iam.huaweicloud.com/3.0/OS-USER/users/076934ff9f0010cd1f0bc0031019a7b7"
        },
        "id": "076934ff9f0010cd1f0bc0031019a7b7",
        "xuser_type": "",
        "email": "IAMEmail@huawei.com"
    }
}
```

## 返回值<a name="zh-cn_topic_0221482439_section458718019321"></a>

<a name="zh-cn_topic_0221482439_table2444"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482439_row152312093215"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482439_p459116018325"><a name="zh-cn_topic_0221482439_p459116018325"></a><a name="zh-cn_topic_0221482439_p459116018325"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482439_p959640163215"><a name="zh-cn_topic_0221482439_p959640163215"></a><a name="zh-cn_topic_0221482439_p959640163215"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482439_row823111017320"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482439_p12598170163210"><a name="zh-cn_topic_0221482439_p12598170163210"></a><a name="zh-cn_topic_0221482439_p12598170163210"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482439_p55991508324"><a name="zh-cn_topic_0221482439_p55991508324"></a><a name="zh-cn_topic_0221482439_p55991508324"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1232160153212"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482439_p18601502323"><a name="zh-cn_topic_0221482439_p18601502323"></a><a name="zh-cn_topic_0221482439_p18601502323"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482439_p136033033210"><a name="zh-cn_topic_0221482439_p136033033210"></a><a name="zh-cn_topic_0221482439_p136033033210"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row142328016321"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482439_p1660612016321"><a name="zh-cn_topic_0221482439_p1660612016321"></a><a name="zh-cn_topic_0221482439_p1660612016321"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482439_p1460810053215"><a name="zh-cn_topic_0221482439_p1460810053215"></a><a name="zh-cn_topic_0221482439_p1460810053215"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1923210113211"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482439_p176101103324"><a name="zh-cn_topic_0221482439_p176101103324"></a><a name="zh-cn_topic_0221482439_p176101103324"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482439_p1161270203213"><a name="zh-cn_topic_0221482439_p1161270203213"></a><a name="zh-cn_topic_0221482439_p1161270203213"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1123210023210"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482439_p661480103215"><a name="zh-cn_topic_0221482439_p661480103215"></a><a name="zh-cn_topic_0221482439_p661480103215"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482439_p19616180173213"><a name="zh-cn_topic_0221482439_p19616180173213"></a><a name="zh-cn_topic_0221482439_p19616180173213"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row9232130173214"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482439_p206183013213"><a name="zh-cn_topic_0221482439_p206183013213"></a><a name="zh-cn_topic_0221482439_p206183013213"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482439_p4620109329"><a name="zh-cn_topic_0221482439_p4620109329"></a><a name="zh-cn_topic_0221482439_p4620109329"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row6232160173219"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482439_p196221023212"><a name="zh-cn_topic_0221482439_p196221023212"></a><a name="zh-cn_topic_0221482439_p196221023212"></a>409</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482439_p1162413063211"><a name="zh-cn_topic_0221482439_p1162413063211"></a><a name="zh-cn_topic_0221482439_p1162413063211"></a>资源冲突。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row623218033214"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482439_p186263083212"><a name="zh-cn_topic_0221482439_p186263083212"></a><a name="zh-cn_topic_0221482439_p186263083212"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482439_p462717016325"><a name="zh-cn_topic_0221482439_p462717016325"></a><a name="zh-cn_topic_0221482439_p462717016325"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row11232110113212"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482439_p196293010324"><a name="zh-cn_topic_0221482439_p196293010324"></a><a name="zh-cn_topic_0221482439_p196293010324"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482439_p763111053212"><a name="zh-cn_topic_0221482439_p763111053212"></a><a name="zh-cn_topic_0221482439_p763111053212"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row2232209329"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482439_p166332013214"><a name="zh-cn_topic_0221482439_p166332013214"></a><a name="zh-cn_topic_0221482439_p166332013214"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482439_p1063514014320"><a name="zh-cn_topic_0221482439_p1063514014320"></a><a name="zh-cn_topic_0221482439_p1063514014320"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482439_section176379013214"></a>

<a name="zh-cn_topic_0221482439_table2445"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482439_row11291190203220"><th class="cellrowborder" valign="top" width="27.27272727272727%" id="mcps1.1.4.1.1"><p id="zh-cn_topic_0221482439_p6641809320"><a name="zh-cn_topic_0221482439_p6641809320"></a><a name="zh-cn_topic_0221482439_p6641809320"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="36.36363636363636%" id="mcps1.1.4.1.2"><p id="zh-cn_topic_0221482439_p564312017328"><a name="zh-cn_topic_0221482439_p564312017328"></a><a name="zh-cn_topic_0221482439_p564312017328"></a>错误码</p>
</th>
<th class="cellrowborder" valign="top" width="36.36363636363636%" id="mcps1.1.4.1.3"><p id="zh-cn_topic_0221482439_p176447012324"><a name="zh-cn_topic_0221482439_p176447012324"></a><a name="zh-cn_topic_0221482439_p176447012324"></a>错误信息</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482439_row112911309323"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p66501303322"><a name="zh-cn_topic_0221482439_p66501303322"></a><a name="zh-cn_topic_0221482439_p66501303322"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p1865220143216"><a name="zh-cn_topic_0221482439_p1865220143216"></a><a name="zh-cn_topic_0221482439_p1865220143216"></a>1100</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p4654707327"><a name="zh-cn_topic_0221482439_p4654707327"></a><a name="zh-cn_topic_0221482439_p4654707327"></a>缺失必选参数。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1429119015329"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p156601103324"><a name="zh-cn_topic_0221482439_p156601103324"></a><a name="zh-cn_topic_0221482439_p156601103324"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p1566290133216"><a name="zh-cn_topic_0221482439_p1566290133216"></a><a name="zh-cn_topic_0221482439_p1566290133216"></a>1101</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p36647073212"><a name="zh-cn_topic_0221482439_p36647073212"></a><a name="zh-cn_topic_0221482439_p36647073212"></a>用户名校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row62914017324"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p11670705321"><a name="zh-cn_topic_0221482439_p11670705321"></a><a name="zh-cn_topic_0221482439_p11670705321"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p46726018328"><a name="zh-cn_topic_0221482439_p46726018328"></a><a name="zh-cn_topic_0221482439_p46726018328"></a>1102</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p206741005321"><a name="zh-cn_topic_0221482439_p206741005321"></a><a name="zh-cn_topic_0221482439_p206741005321"></a>邮箱校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row029170183215"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p76797073211"><a name="zh-cn_topic_0221482439_p76797073211"></a><a name="zh-cn_topic_0221482439_p76797073211"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p126818018328"><a name="zh-cn_topic_0221482439_p126818018328"></a><a name="zh-cn_topic_0221482439_p126818018328"></a>1103</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p116831309326"><a name="zh-cn_topic_0221482439_p116831309326"></a><a name="zh-cn_topic_0221482439_p116831309326"></a>密码校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1129140163211"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p18689707324"><a name="zh-cn_topic_0221482439_p18689707324"></a><a name="zh-cn_topic_0221482439_p18689707324"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p969116053214"><a name="zh-cn_topic_0221482439_p969116053214"></a><a name="zh-cn_topic_0221482439_p969116053214"></a>1104</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p16693909328"><a name="zh-cn_topic_0221482439_p16693909328"></a><a name="zh-cn_topic_0221482439_p16693909328"></a>手机号校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row729119013322"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p969814019329"><a name="zh-cn_topic_0221482439_p969814019329"></a><a name="zh-cn_topic_0221482439_p969814019329"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p17701100173218"><a name="zh-cn_topic_0221482439_p17701100173218"></a><a name="zh-cn_topic_0221482439_p17701100173218"></a>1105</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p13703190103214"><a name="zh-cn_topic_0221482439_p13703190103214"></a><a name="zh-cn_topic_0221482439_p13703190103214"></a>xuser_type必须与xdomain_type相同。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row15291160123218"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p177081208324"><a name="zh-cn_topic_0221482439_p177081208324"></a><a name="zh-cn_topic_0221482439_p177081208324"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p14710180123218"><a name="zh-cn_topic_0221482439_p14710180123218"></a><a name="zh-cn_topic_0221482439_p14710180123218"></a>1106</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p471130163211"><a name="zh-cn_topic_0221482439_p471130163211"></a><a name="zh-cn_topic_0221482439_p471130163211"></a>国家码、手机号必须同时存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1229116014327"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p6717302324"><a name="zh-cn_topic_0221482439_p6717302324"></a><a name="zh-cn_topic_0221482439_p6717302324"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p57196018326"><a name="zh-cn_topic_0221482439_p57196018326"></a><a name="zh-cn_topic_0221482439_p57196018326"></a>1107</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p18720120163220"><a name="zh-cn_topic_0221482439_p18720120163220"></a><a name="zh-cn_topic_0221482439_p18720120163220"></a>账号管理员不能被删除。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row129116083215"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p67251606328"><a name="zh-cn_topic_0221482439_p67251606328"></a><a name="zh-cn_topic_0221482439_p67251606328"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p1727106326"><a name="zh-cn_topic_0221482439_p1727106326"></a><a name="zh-cn_topic_0221482439_p1727106326"></a>1108</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p147299018321"><a name="zh-cn_topic_0221482439_p147299018321"></a><a name="zh-cn_topic_0221482439_p147299018321"></a>新密码不能与原密码相同。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row16292190133214"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p67349003214"><a name="zh-cn_topic_0221482439_p67349003214"></a><a name="zh-cn_topic_0221482439_p67349003214"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p15735110163213"><a name="zh-cn_topic_0221482439_p15735110163213"></a><a name="zh-cn_topic_0221482439_p15735110163213"></a>1109</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p15737301321"><a name="zh-cn_topic_0221482439_p15737301321"></a><a name="zh-cn_topic_0221482439_p15737301321"></a>用户名已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row42921015325"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p11742150113212"><a name="zh-cn_topic_0221482439_p11742150113212"></a><a name="zh-cn_topic_0221482439_p11742150113212"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p147452018328"><a name="zh-cn_topic_0221482439_p147452018328"></a><a name="zh-cn_topic_0221482439_p147452018328"></a>1110</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p1874750133215"><a name="zh-cn_topic_0221482439_p1874750133215"></a><a name="zh-cn_topic_0221482439_p1874750133215"></a>邮箱已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row192921604322"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p175213013211"><a name="zh-cn_topic_0221482439_p175213013211"></a><a name="zh-cn_topic_0221482439_p175213013211"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p7753190193216"><a name="zh-cn_topic_0221482439_p7753190193216"></a><a name="zh-cn_topic_0221482439_p7753190193216"></a>1111</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p1575520103216"><a name="zh-cn_topic_0221482439_p1575520103216"></a><a name="zh-cn_topic_0221482439_p1575520103216"></a>手机号已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row152921309329"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p67613093213"><a name="zh-cn_topic_0221482439_p67613093213"></a><a name="zh-cn_topic_0221482439_p67613093213"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p17763309327"><a name="zh-cn_topic_0221482439_p17763309327"></a><a name="zh-cn_topic_0221482439_p17763309327"></a>1113</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p17765190143216"><a name="zh-cn_topic_0221482439_p17765190143216"></a><a name="zh-cn_topic_0221482439_p17765190143216"></a>xuser_id、xuser_type已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row172922010323"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p277020123214"><a name="zh-cn_topic_0221482439_p277020123214"></a><a name="zh-cn_topic_0221482439_p277020123214"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p5773307327"><a name="zh-cn_topic_0221482439_p5773307327"></a><a name="zh-cn_topic_0221482439_p5773307327"></a>1115</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p577520016321"><a name="zh-cn_topic_0221482439_p577520016321"></a><a name="zh-cn_topic_0221482439_p577520016321"></a>IAM用户数量达到最大限制。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row229218043218"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482439_p147832073211"><a name="zh-cn_topic_0221482439_p147832073211"></a><a name="zh-cn_topic_0221482439_p147832073211"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482439_p178520017323"><a name="zh-cn_topic_0221482439_p178520017323"></a><a name="zh-cn_topic_0221482439_p178520017323"></a>1117</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482439_p11787200123213"><a name="zh-cn_topic_0221482439_p11787200123213"></a><a name="zh-cn_topic_0221482439_p11787200123213"></a>用户描述校验失败。</p>
</td>
</tr>
</tbody>
</table>

