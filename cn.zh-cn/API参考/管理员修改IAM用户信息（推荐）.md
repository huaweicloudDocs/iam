# 管理员修改IAM用户信息（推荐）<a name="iam_08_0011"></a>

## 功能介绍<a name="zh-cn_topic_0221482439_section13155155913310"></a>

该接口可以用于<u>[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)</u><u></u>修改IAM用户信息 。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section105550391405"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=UpdateUser)中调试该接口。

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
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p32391559143119"><a name="zh-cn_topic_0221482439_p32391559143119"></a><a name="zh-cn_topic_0221482439_p32391559143119"></a>待修改信息的IAM用户ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482439_section13247135953113"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482439_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482439_row1625917593318"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482439_p6267165943111"><a name="zh-cn_topic_0221482439_p6267165943111"></a><a name="zh-cn_topic_0221482439_p6267165943111"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.2%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482439_p427285913314"><a name="zh-cn_topic_0221482439_p427285913314"></a><a name="zh-cn_topic_0221482439_p427285913314"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.8%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482439_p1727765910315"><a name="zh-cn_topic_0221482439_p1727765910315"></a><a name="zh-cn_topic_0221482439_p1727765910315"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482439_p92822595319"><a name="zh-cn_topic_0221482439_p92822595319"></a><a name="zh-cn_topic_0221482439_p92822595319"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482439_row13260859193110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p182871459183117"><a name="zh-cn_topic_0221482439_p182871459183117"></a><a name="zh-cn_topic_0221482439_p182871459183117"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p1129175933111"><a name="zh-cn_topic_0221482439_p1129175933111"></a><a name="zh-cn_topic_0221482439_p1129175933111"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.8%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p129875915319"><a name="zh-cn_topic_0221482439_p129875915319"></a><a name="zh-cn_topic_0221482439_p129875915319"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p16303159163113"><a name="zh-cn_topic_0221482439_p16303159163113"></a><a name="zh-cn_topic_0221482439_p16303159163113"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row11260115973117"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p73101259153116"><a name="zh-cn_topic_0221482439_p73101259153116"></a><a name="zh-cn_topic_0221482439_p73101259153116"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p113151859113118"><a name="zh-cn_topic_0221482439_p113151859113118"></a><a name="zh-cn_topic_0221482439_p113151859113118"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.8%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p33201859173118"><a name="zh-cn_topic_0221482439_p33201859173118"></a><a name="zh-cn_topic_0221482439_p33201859173118"></a>String</p>
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
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p13425125913111"><a name="zh-cn_topic_0221482439_p13425125913111"></a><a name="zh-cn_topic_0221482439_p13425125913111"></a>新IAM用户名，长度1~32之间，只能包含如下字符：大小写字母、空格、数字或特殊字符（-_.）且不能以数字或空格开头。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row83841859133112"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p12429959113118"><a name="zh-cn_topic_0221482439_p12429959113118"></a><a name="zh-cn_topic_0221482439_p12429959113118"></a>password</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p13435195993117"><a name="zh-cn_topic_0221482439_p13435195993117"></a><a name="zh-cn_topic_0221482439_p13435195993117"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p144401759103111"><a name="zh-cn_topic_0221482439_p144401759103111"></a><a name="zh-cn_topic_0221482439_p144401759103111"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p1144510594314"><a name="zh-cn_topic_0221482439_p1144510594314"></a><a name="zh-cn_topic_0221482439_p1144510594314"></a>IAM用户新密码。</p>
<a name="zh-cn_topic_0221482439_ul14452559183112"></a><a name="zh-cn_topic_0221482439_ul14452559183112"></a><ul id="zh-cn_topic_0221482439_ul14452559183112"><li>系统默认密码最小长度为6位字符，在6-32位之间支持用户自定义密码长度。</li><li>至少包含以下四种字符中的两种： 大写字母、小写字母、数字和特殊字符。</li><li>必须满足账户设置中<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0607.html" target="_blank" rel="noopener noreferrer">密码策略</a>的要求。</li><li>新密码不能与当前密码相同。</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row11384145913316"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482439_p7485759203119"><a name="zh-cn_topic_0221482439_p7485759203119"></a><a name="zh-cn_topic_0221482439_p7485759203119"></a>email</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482439_p2490115993113"><a name="zh-cn_topic_0221482439_p2490115993113"></a><a name="zh-cn_topic_0221482439_p2490115993113"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482439_p249805917313"><a name="zh-cn_topic_0221482439_p249805917313"></a><a name="zh-cn_topic_0221482439_p249805917313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482439_p5502145963118"><a name="zh-cn_topic_0221482439_p5502145963118"></a><a name="zh-cn_topic_0221482439_p5502145963118"></a>IAM用户新邮箱，需符合邮箱格式，长度小于等于255字符。</p>
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
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p178511019193011"><a name="p178511019193011"></a><a name="p178511019193011"></a>Boolean</p>
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
<tr id="row7551547195817"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1258313510498"><a name="p1258313510498"></a><a name="p1258313510498"></a>access_mode</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p10475229114611"><a name="p10475229114611"></a><a name="p10475229114611"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p185832513490"><a name="p185832513490"></a><a name="p185832513490"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p203061940231"><a name="p203061940231"></a><a name="p203061940231"></a>IAM用户访问方式。</p>
<a name="ul101759371511"></a><a name="ul101759371511"></a><ul id="ul101759371511"><li>default：默认访问模式，编程访问和管理控制台访问。</li><li>programmatic：编程访问。</li><li>console：管理控制台访问。</li></ul>
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
<table><thead align="left"><tr id="zh-cn_topic_0221482439_row1974825933119"><th class="cellrowborder" valign="top" width="20.05%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482439_p575335913311"><a name="zh-cn_topic_0221482439_p575335913311"></a><a name="zh-cn_topic_0221482439_p575335913311"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="19.97%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482439_p6757135963113"><a name="zh-cn_topic_0221482439_p6757135963113"></a><a name="zh-cn_topic_0221482439_p6757135963113"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="59.98%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482439_p0762059123118"><a name="zh-cn_topic_0221482439_p0762059123118"></a><a name="zh-cn_topic_0221482439_p0762059123118"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482439_row07484596312"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p1076615993116"><a name="zh-cn_topic_0221482439_p1076615993116"></a><a name="zh-cn_topic_0221482439_p1076615993116"></a>pwd_status</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p157701459123120"><a name="zh-cn_topic_0221482439_p157701459123120"></a><a name="zh-cn_topic_0221482439_p157701459123120"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p4776959203115"><a name="zh-cn_topic_0221482439_p4776959203115"></a><a name="zh-cn_topic_0221482439_p4776959203115"></a>IAM用户密码状态。true：需要修改密码，false：正常。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row19748135933114"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p17781105953113"><a name="zh-cn_topic_0221482439_p17781105953113"></a><a name="zh-cn_topic_0221482439_p17781105953113"></a>xuser_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p15785125917312"><a name="zh-cn_topic_0221482439_p15785125917312"></a><a name="zh-cn_topic_0221482439_p15785125917312"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p137901159123119"><a name="zh-cn_topic_0221482439_p137901159123119"></a><a name="zh-cn_topic_0221482439_p137901159123119"></a>IAM用户在外部系统中的ID。</p>
<div class="note" id="zh-cn_topic_0221482439_note0801115916318"><a name="zh-cn_topic_0221482439_note0801115916318"></a><a name="zh-cn_topic_0221482439_note0801115916318"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0221482439_p19808105983114"><a name="zh-cn_topic_0221482439_p19808105983114"></a><a name="zh-cn_topic_0221482439_p19808105983114"></a>外部系统指与华为云对接的外部企业管理系统，xaccount_type、xaccount_id、xdomain_type、xdomain_id、xuser_type、xuser_id等参数值，无法在华为云获取，请咨询企业管理员。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1748185912319"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p1081245973117"><a name="zh-cn_topic_0221482439_p1081245973117"></a><a name="zh-cn_topic_0221482439_p1081245973117"></a>xuser_type</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p4817175919312"><a name="zh-cn_topic_0221482439_p4817175919312"></a><a name="zh-cn_topic_0221482439_p4817175919312"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p982155993119"><a name="zh-cn_topic_0221482439_p982155993119"></a><a name="zh-cn_topic_0221482439_p982155993119"></a>IAM用户在外部系统中的类型。</p>
<div class="note" id="zh-cn_topic_0221482439_note28311259183118"><a name="zh-cn_topic_0221482439_note28311259183118"></a><a name="zh-cn_topic_0221482439_note28311259183118"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0221482439_p58371759103113"><a name="zh-cn_topic_0221482439_p58371759103113"></a><a name="zh-cn_topic_0221482439_p58371759103113"></a>外部系统指与华为云对接的外部企业管理系统，xaccount_type、xaccount_id、xdomain_type、xdomain_id、xuser_type、xuser_id等参数值，无法在华为云获取，请咨询企业管理员。</p>
</div></div>
</td>
</tr>
<tr id="row116751211195912"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="p2511132595"><a name="p2511132595"></a><a name="p2511132595"></a>access_mode</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="p131132415920"><a name="p131132415920"></a><a name="p131132415920"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="p17583125114912"><a name="p17583125114912"></a><a name="p17583125114912"></a>IAM用户访问方式。</p>
<a name="ul114842442319"></a><a name="ul114842442319"></a><ul id="ul114842442319"><li>default：默认访问模式，编程访问和管理控制台访问。</li><li>programmatic：编程访问。</li><li>console：管理控制台访问。</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row174885993119"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p084125912310"><a name="zh-cn_topic_0221482439_p084125912310"></a><a name="zh-cn_topic_0221482439_p084125912310"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p19846195916315"><a name="zh-cn_topic_0221482439_p19846195916315"></a><a name="zh-cn_topic_0221482439_p19846195916315"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p2085195918319"><a name="zh-cn_topic_0221482439_p2085195918319"></a><a name="zh-cn_topic_0221482439_p2085195918319"></a>IAM用户的新描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1474814598317"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p1185725918312"><a name="zh-cn_topic_0221482439_p1185725918312"></a><a name="zh-cn_topic_0221482439_p1185725918312"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p13863105903117"><a name="zh-cn_topic_0221482439_p13863105903117"></a><a name="zh-cn_topic_0221482439_p13863105903117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p9868155983117"><a name="zh-cn_topic_0221482439_p9868155983117"></a><a name="zh-cn_topic_0221482439_p9868155983117"></a>IAM用户新用户名，长度1~32之间，只能包含如下字符：大小写字母、空格、数字或特殊字符（-_.）且不能以数字或空格开头。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row77481559103112"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p1487410591318"><a name="zh-cn_topic_0221482439_p1487410591318"></a><a name="zh-cn_topic_0221482439_p1487410591318"></a>phone</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p487975910314"><a name="zh-cn_topic_0221482439_p487975910314"></a><a name="zh-cn_topic_0221482439_p487975910314"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p78841559123119"><a name="zh-cn_topic_0221482439_p78841559123119"></a><a name="zh-cn_topic_0221482439_p78841559123119"></a>IAM用户新手机号，纯数字，长度小于等于32位。必须与国家码同时存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row10748205933116"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p48911859133114"><a name="zh-cn_topic_0221482439_p48911859133114"></a><a name="zh-cn_topic_0221482439_p48911859133114"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p1989685983114"><a name="zh-cn_topic_0221482439_p1989685983114"></a><a name="zh-cn_topic_0221482439_p1989685983114"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p490175913318"><a name="zh-cn_topic_0221482439_p490175913318"></a><a name="zh-cn_topic_0221482439_p490175913318"></a>IAM用户所属帐号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row18748959143119"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p169064595314"><a name="zh-cn_topic_0221482439_p169064595314"></a><a name="zh-cn_topic_0221482439_p169064595314"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p491115973115"><a name="zh-cn_topic_0221482439_p491115973115"></a><a name="zh-cn_topic_0221482439_p491115973115"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p29161459133112"><a name="zh-cn_topic_0221482439_p29161459133112"></a><a name="zh-cn_topic_0221482439_p29161459133112"></a>是否启用IAM用户。true为启用，false为停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1874925913112"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p179221759163118"><a name="zh-cn_topic_0221482439_p179221759163118"></a><a name="zh-cn_topic_0221482439_p179221759163118"></a>areacode</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p17927165911319"><a name="zh-cn_topic_0221482439_p17927165911319"></a><a name="zh-cn_topic_0221482439_p17927165911319"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p18932205943113"><a name="zh-cn_topic_0221482439_p18932205943113"></a><a name="zh-cn_topic_0221482439_p18932205943113"></a>国家码。中国大陆为“0086”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row574965933120"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p179373592312"><a name="zh-cn_topic_0221482439_p179373592312"></a><a name="zh-cn_topic_0221482439_p179373592312"></a>email</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p994219592310"><a name="zh-cn_topic_0221482439_p994219592310"></a><a name="zh-cn_topic_0221482439_p994219592310"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p09471659173113"><a name="zh-cn_topic_0221482439_p09471659173113"></a><a name="zh-cn_topic_0221482439_p09471659173113"></a>IAM用户新邮箱。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1774935915310"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p69681659103119"><a name="zh-cn_topic_0221482439_p69681659103119"></a><a name="zh-cn_topic_0221482439_p69681659103119"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p297325914317"><a name="zh-cn_topic_0221482439_p297325914317"></a><a name="zh-cn_topic_0221482439_p297325914317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p1981105933112"><a name="zh-cn_topic_0221482439_p1981105933112"></a><a name="zh-cn_topic_0221482439_p1981105933112"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row1474920593315"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p49864596319"><a name="zh-cn_topic_0221482439_p49864596319"></a><a name="zh-cn_topic_0221482439_p49864596319"></a><a href="#zh-cn_topic_0221482439_response_Rs810UserLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p1699215915314"><a name="zh-cn_topic_0221482439_p1699215915314"></a><a name="zh-cn_topic_0221482439_p1699215915314"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p6999145918312"><a name="zh-cn_topic_0221482439_p6999145918312"></a><a name="zh-cn_topic_0221482439_p6999145918312"></a>IAM用户的资源链接信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482439_row167492591310"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482439_p14518093220"><a name="zh-cn_topic_0221482439_p14518093220"></a><a name="zh-cn_topic_0221482439_p14518093220"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482439_p191019093212"><a name="zh-cn_topic_0221482439_p191019093212"></a><a name="zh-cn_topic_0221482439_p191019093212"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.98%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482439_p4164010324"><a name="zh-cn_topic_0221482439_p4164010324"></a><a name="zh-cn_topic_0221482439_p4164010324"></a>密码过期时间（UTC时间）。当值为“null”时，不返回。</p>
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
        "access_mode" : "default",
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
        "description": "IAMDescription",
        "areacode": "0086",
        "enabled": true,
        "pwd_status": false,
        "xuser_id": "",
        "access_mode" : "default",
        "domain_id": "d78cbac186b744899480f25bd0...",
        "phone": "12345678910",
        "name": "IAMUser",
        "links": {
            "self": "https://iam.myhuaweicloud.com/3.0/OS-USER/users/076934ff9f0010cd1f0bc003..."
        },
        "id": "076934ff9f0010cd1f0bc0031019...",
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

请参考[错误码](错误码.md)。

