# 管理员修改IAM用户信息<a name="iam_08_0008"></a>

## 功能介绍<a name="zh-cn_topic_0221482404_section8411201017329"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)修改IAM用户信息。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 接口约束<a name="zh-cn_topic_0221482404_section941251011326"></a>

该接口无法修改手机号、邮箱等信息。如需修改手机号、邮箱等信息，请使用接口：[管理员修改IAM用户信息（推荐）](管理员修改IAM用户信息（推荐）.md)。

## URI<a name="zh-cn_topic_0221482404_section1341210105328"></a>

PATCH /v3/users/\{user\_id\}

**表 1**  路径参数

<a name="zh-cn_topic_0221482404_table841451063210"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482404_row104136103325"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482404_p114141210153216"><a name="zh-cn_topic_0221482404_p114141210153216"></a><a name="zh-cn_topic_0221482404_p114141210153216"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482404_p7414181017325"><a name="zh-cn_topic_0221482404_p7414181017325"></a><a name="zh-cn_topic_0221482404_p7414181017325"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482404_p144151104327"><a name="zh-cn_topic_0221482404_p144151104327"></a><a name="zh-cn_topic_0221482404_p144151104327"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482404_p124151107325"><a name="zh-cn_topic_0221482404_p124151107325"></a><a name="zh-cn_topic_0221482404_p124151107325"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482404_row13413141093219"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482404_p1441671023217"><a name="zh-cn_topic_0221482404_p1441671023217"></a><a name="zh-cn_topic_0221482404_p1441671023217"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482404_p1941621010320"><a name="zh-cn_topic_0221482404_p1941621010320"></a><a name="zh-cn_topic_0221482404_p1941621010320"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482404_p14417610163217"><a name="zh-cn_topic_0221482404_p14417610163217"></a><a name="zh-cn_topic_0221482404_p14417610163217"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482404_p1141817101324"><a name="zh-cn_topic_0221482404_p1141817101324"></a><a name="zh-cn_topic_0221482404_p1141817101324"></a>待修改信息的IAM用户ID，获取方式请参见：<a href="获取账号-IAM用户-项目-用户组-委托的名称和ID.md">获取账号、IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482404_section54181410163213"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482404_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482404_row2041917108324"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482404_p142010108324"><a name="zh-cn_topic_0221482404_p142010108324"></a><a name="zh-cn_topic_0221482404_p142010108324"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482404_p7421111043218"><a name="zh-cn_topic_0221482404_p7421111043218"></a><a name="zh-cn_topic_0221482404_p7421111043218"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482404_p8421131011324"><a name="zh-cn_topic_0221482404_p8421131011324"></a><a name="zh-cn_topic_0221482404_p8421131011324"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482404_p642181012324"><a name="zh-cn_topic_0221482404_p642181012324"></a><a name="zh-cn_topic_0221482404_p642181012324"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482404_row441915104329"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482404_p3422151012324"><a name="zh-cn_topic_0221482404_p3422151012324"></a><a name="zh-cn_topic_0221482404_p3422151012324"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482404_p042281033212"><a name="zh-cn_topic_0221482404_p042281033212"></a><a name="zh-cn_topic_0221482404_p042281033212"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482404_p0423121019322"><a name="zh-cn_topic_0221482404_p0423121019322"></a><a name="zh-cn_topic_0221482404_p0423121019322"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482404_p1423510173210"><a name="zh-cn_topic_0221482404_p1423510173210"></a><a name="zh-cn_topic_0221482404_p1423510173210"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row64196100325"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482404_p18424610153218"><a name="zh-cn_topic_0221482404_p18424610153218"></a><a name="zh-cn_topic_0221482404_p18424610153218"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482404_p1742481043211"><a name="zh-cn_topic_0221482404_p1742481043211"></a><a name="zh-cn_topic_0221482404_p1742481043211"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482404_p194241710103213"><a name="zh-cn_topic_0221482404_p194241710103213"></a><a name="zh-cn_topic_0221482404_p194241710103213"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482404_p1425111014328"><a name="zh-cn_topic_0221482404_p1425111014328"></a><a name="zh-cn_topic_0221482404_p1425111014328"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="zh-cn_topic_0221482404_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482404_row16426111073218"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482404_p3427810163216"><a name="zh-cn_topic_0221482404_p3427810163216"></a><a name="zh-cn_topic_0221482404_p3427810163216"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482404_p9427141010325"><a name="zh-cn_topic_0221482404_p9427141010325"></a><a name="zh-cn_topic_0221482404_p9427141010325"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482404_p9427141018321"><a name="zh-cn_topic_0221482404_p9427141018321"></a><a name="zh-cn_topic_0221482404_p9427141018321"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482404_p442831013212"><a name="zh-cn_topic_0221482404_p442831013212"></a><a name="zh-cn_topic_0221482404_p442831013212"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482404_row542661053214"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482404_p1428110133219"><a name="zh-cn_topic_0221482404_p1428110133219"></a><a name="zh-cn_topic_0221482404_p1428110133219"></a><a href="#zh-cn_topic_0221482404_request_Rq811User">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482404_p942916104326"><a name="zh-cn_topic_0221482404_p942916104326"></a><a name="zh-cn_topic_0221482404_p942916104326"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482404_p164291010133217"><a name="zh-cn_topic_0221482404_p164291010133217"></a><a name="zh-cn_topic_0221482404_p164291010133217"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482404_p154303108327"><a name="zh-cn_topic_0221482404_p154303108327"></a><a name="zh-cn_topic_0221482404_p154303108327"></a>IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  user

<a name="zh-cn_topic_0221482404_request_Rq811User"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482404_row443119102329"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482404_p7434161053212"><a name="zh-cn_topic_0221482404_p7434161053212"></a><a name="zh-cn_topic_0221482404_p7434161053212"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482404_p17435141016321"><a name="zh-cn_topic_0221482404_p17435141016321"></a><a name="zh-cn_topic_0221482404_p17435141016321"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482404_p4435510183220"><a name="zh-cn_topic_0221482404_p4435510183220"></a><a name="zh-cn_topic_0221482404_p4435510183220"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482404_p1043514101328"><a name="zh-cn_topic_0221482404_p1043514101328"></a><a name="zh-cn_topic_0221482404_p1043514101328"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482404_row9432131011329"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482404_p3436131020324"><a name="zh-cn_topic_0221482404_p3436131020324"></a><a name="zh-cn_topic_0221482404_p3436131020324"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482404_p18436810193216"><a name="zh-cn_topic_0221482404_p18436810193216"></a><a name="zh-cn_topic_0221482404_p18436810193216"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482404_p743681033215"><a name="zh-cn_topic_0221482404_p743681033215"></a><a name="zh-cn_topic_0221482404_p743681033215"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482404_p34366104324"><a name="zh-cn_topic_0221482404_p34366104324"></a><a name="zh-cn_topic_0221482404_p34366104324"></a>IAM用户所属账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row17433131023214"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482404_p643701093212"><a name="zh-cn_topic_0221482404_p643701093212"></a><a name="zh-cn_topic_0221482404_p643701093212"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482404_p1643717105324"><a name="zh-cn_topic_0221482404_p1643717105324"></a><a name="zh-cn_topic_0221482404_p1643717105324"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482404_p18437710133220"><a name="zh-cn_topic_0221482404_p18437710133220"></a><a name="zh-cn_topic_0221482404_p18437710133220"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482404_p1443811102326"><a name="zh-cn_topic_0221482404_p1443811102326"></a><a name="zh-cn_topic_0221482404_p1443811102326"></a>IAM用户新用户名，长度5~32之间，首位不能为数字，特殊字符只能包含下划线“_”、中划线“-”和空格。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row17433111083218"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482404_p24381510203210"><a name="zh-cn_topic_0221482404_p24381510203210"></a><a name="zh-cn_topic_0221482404_p24381510203210"></a>password</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482404_p843811018327"><a name="zh-cn_topic_0221482404_p843811018327"></a><a name="zh-cn_topic_0221482404_p843811018327"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482404_p143871018325"><a name="zh-cn_topic_0221482404_p143871018325"></a><a name="zh-cn_topic_0221482404_p143871018325"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482404_p44392010123213"><a name="zh-cn_topic_0221482404_p44392010123213"></a><a name="zh-cn_topic_0221482404_p44392010123213"></a>IAM用户密码。</p>
<a name="zh-cn_topic_0221482404_ul124395107329"></a><a name="zh-cn_topic_0221482404_ul124395107329"></a><ul id="zh-cn_topic_0221482404_ul124395107329"><li>系统默认密码最小长度为6位字符，在6-32位之间支持用户自定义密码长度。</li><li>至少包含以下四种字符中的两种： 大写字母、小写字母、数字和特殊字符。</li><li>不能包含手机号和邮箱。</li><li>必须满足账户设置中<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0607.html" target="_blank" rel="noopener noreferrer">密码策略</a>的要求。</li><li>新密码不能与当前密码相同。</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row114331610153213"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482404_p13440131003215"><a name="zh-cn_topic_0221482404_p13440131003215"></a><a name="zh-cn_topic_0221482404_p13440131003215"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482404_p13441810173220"><a name="zh-cn_topic_0221482404_p13441810173220"></a><a name="zh-cn_topic_0221482404_p13441810173220"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482404_p1044141014326"><a name="zh-cn_topic_0221482404_p1044141014326"></a><a name="zh-cn_topic_0221482404_p1044141014326"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482404_p174413101329"><a name="zh-cn_topic_0221482404_p174413101329"></a><a name="zh-cn_topic_0221482404_p174413101329"></a>是否启用IAM用户。true为启用，false为停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row104334107323"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482404_p1044210106325"><a name="zh-cn_topic_0221482404_p1044210106325"></a><a name="zh-cn_topic_0221482404_p1044210106325"></a>default_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482404_p044213107324"><a name="zh-cn_topic_0221482404_p044213107324"></a><a name="zh-cn_topic_0221482404_p044213107324"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482404_p1644271073217"><a name="zh-cn_topic_0221482404_p1644271073217"></a><a name="zh-cn_topic_0221482404_p1644271073217"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482404_p1044213106326"><a name="zh-cn_topic_0221482404_p1044213106326"></a><a name="zh-cn_topic_0221482404_p1044213106326"></a>IAM用户默认项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row1943391093212"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482404_p944311003212"><a name="zh-cn_topic_0221482404_p944311003212"></a><a name="zh-cn_topic_0221482404_p944311003212"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482404_p144430108327"><a name="zh-cn_topic_0221482404_p144430108327"></a><a name="zh-cn_topic_0221482404_p144430108327"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482404_p1444316109326"><a name="zh-cn_topic_0221482404_p1444316109326"></a><a name="zh-cn_topic_0221482404_p1444316109326"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482404_p24432100321"><a name="zh-cn_topic_0221482404_p24432100321"></a><a name="zh-cn_topic_0221482404_p24432100321"></a>IAM用户新描述信息。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482404_section10444131053215"></a>

**表 5**  响应Body参数

<a name="zh-cn_topic_0221482404_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482404_row9444161043217"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482404_p24451310133217"><a name="zh-cn_topic_0221482404_p24451310133217"></a><a name="zh-cn_topic_0221482404_p24451310133217"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482404_p044621018322"><a name="zh-cn_topic_0221482404_p044621018322"></a><a name="zh-cn_topic_0221482404_p044621018322"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482404_p2446510193213"><a name="zh-cn_topic_0221482404_p2446510193213"></a><a name="zh-cn_topic_0221482404_p2446510193213"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482404_row4445141016323"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p204468105322"><a name="zh-cn_topic_0221482404_p204468105322"></a><a name="zh-cn_topic_0221482404_p204468105322"></a><a href="#zh-cn_topic_0221482404_response_Rs811User">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p2447161073215"><a name="zh-cn_topic_0221482404_p2447161073215"></a><a name="zh-cn_topic_0221482404_p2447161073215"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p8448710183214"><a name="zh-cn_topic_0221482404_p8448710183214"></a><a name="zh-cn_topic_0221482404_p8448710183214"></a>IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  user

<a name="zh-cn_topic_0221482404_response_Rs811User"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482404_row13449610113213"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482404_p10451510103218"><a name="zh-cn_topic_0221482404_p10451510103218"></a><a name="zh-cn_topic_0221482404_p10451510103218"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482404_p1045211019329"><a name="zh-cn_topic_0221482404_p1045211019329"></a><a name="zh-cn_topic_0221482404_p1045211019329"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482404_p154521010163216"><a name="zh-cn_topic_0221482404_p154521010163216"></a><a name="zh-cn_topic_0221482404_p154521010163216"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482404_row1945012101327"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p645241003210"><a name="zh-cn_topic_0221482404_p645241003210"></a><a name="zh-cn_topic_0221482404_p645241003210"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p11453201011326"><a name="zh-cn_topic_0221482404_p11453201011326"></a><a name="zh-cn_topic_0221482404_p11453201011326"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p3453121013329"><a name="zh-cn_topic_0221482404_p3453121013329"></a><a name="zh-cn_topic_0221482404_p3453121013329"></a>IAM用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row94501210143210"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p4453111020324"><a name="zh-cn_topic_0221482404_p4453111020324"></a><a name="zh-cn_topic_0221482404_p4453111020324"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p114541910103218"><a name="zh-cn_topic_0221482404_p114541910103218"></a><a name="zh-cn_topic_0221482404_p114541910103218"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p10454181023213"><a name="zh-cn_topic_0221482404_p10454181023213"></a><a name="zh-cn_topic_0221482404_p10454181023213"></a>IAM用户所属账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row1345021013210"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p10454101033215"><a name="zh-cn_topic_0221482404_p10454101033215"></a><a name="zh-cn_topic_0221482404_p10454101033215"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p18454191012321"><a name="zh-cn_topic_0221482404_p18454191012321"></a><a name="zh-cn_topic_0221482404_p18454191012321"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p6455110183217"><a name="zh-cn_topic_0221482404_p6455110183217"></a><a name="zh-cn_topic_0221482404_p6455110183217"></a>IAM用户是否启用。true表示启用，false表示停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row945016103326"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p174551510103211"><a name="zh-cn_topic_0221482404_p174551510103211"></a><a name="zh-cn_topic_0221482404_p174551510103211"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p345541053216"><a name="zh-cn_topic_0221482404_p345541053216"></a><a name="zh-cn_topic_0221482404_p345541053216"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p11456161012329"><a name="zh-cn_topic_0221482404_p11456161012329"></a><a name="zh-cn_topic_0221482404_p11456161012329"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row3450121063219"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p945631016320"><a name="zh-cn_topic_0221482404_p945631016320"></a><a name="zh-cn_topic_0221482404_p945631016320"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p2456710103213"><a name="zh-cn_topic_0221482404_p2456710103213"></a><a name="zh-cn_topic_0221482404_p2456710103213"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p94561710163212"><a name="zh-cn_topic_0221482404_p94561710163212"></a><a name="zh-cn_topic_0221482404_p94561710163212"></a>密码过期时间（UTC时间），“null”表示密码不过期。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row1450310143211"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p645791014328"><a name="zh-cn_topic_0221482404_p645791014328"></a><a name="zh-cn_topic_0221482404_p645791014328"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p1045831015324"><a name="zh-cn_topic_0221482404_p1045831015324"></a><a name="zh-cn_topic_0221482404_p1045831015324"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p1458141014324"><a name="zh-cn_topic_0221482404_p1458141014324"></a><a name="zh-cn_topic_0221482404_p1458141014324"></a>IAM用户描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row1845021015328"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p1445891033212"><a name="zh-cn_topic_0221482404_p1445891033212"></a><a name="zh-cn_topic_0221482404_p1445891033212"></a>pwd_status</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p545916106324"><a name="zh-cn_topic_0221482404_p545916106324"></a><a name="zh-cn_topic_0221482404_p545916106324"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p204591010123216"><a name="zh-cn_topic_0221482404_p204591010123216"></a><a name="zh-cn_topic_0221482404_p204591010123216"></a>IAM用户密码状态。true：需要修改密码，false：正常。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row104501010183216"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p6459141093212"><a name="zh-cn_topic_0221482404_p6459141093212"></a><a name="zh-cn_topic_0221482404_p6459141093212"></a>forceResetPwd</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p346041016326"><a name="zh-cn_topic_0221482404_p346041016326"></a><a name="zh-cn_topic_0221482404_p346041016326"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p9460111012323"><a name="zh-cn_topic_0221482404_p9460111012323"></a><a name="zh-cn_topic_0221482404_p9460111012323"></a>IAM用户下次登录是否强制重置密码。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row7450111063210"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p194601410173210"><a name="zh-cn_topic_0221482404_p194601410173210"></a><a name="zh-cn_topic_0221482404_p194601410173210"></a>default_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p246181073213"><a name="zh-cn_topic_0221482404_p246181073213"></a><a name="zh-cn_topic_0221482404_p246181073213"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p104611310113218"><a name="zh-cn_topic_0221482404_p104611310113218"></a><a name="zh-cn_topic_0221482404_p104611310113218"></a>IAM用户登录控制台后默认跳转的项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row445041073214"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p1946181063217"><a name="zh-cn_topic_0221482404_p1946181063217"></a><a name="zh-cn_topic_0221482404_p1946181063217"></a>last_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p6461610123215"><a name="zh-cn_topic_0221482404_p6461610123215"></a><a name="zh-cn_topic_0221482404_p6461610123215"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p8462610123215"><a name="zh-cn_topic_0221482404_p8462610123215"></a><a name="zh-cn_topic_0221482404_p8462610123215"></a>IAM用户退出系统前，在控制台最后访问的项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row4450121033212"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p1546201033212"><a name="zh-cn_topic_0221482404_p1546201033212"></a><a name="zh-cn_topic_0221482404_p1546201033212"></a><a href="#zh-cn_topic_0221482404_response_Rs811UserExtra">extra</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p64637104323"><a name="zh-cn_topic_0221482404_p64637104323"></a><a name="zh-cn_topic_0221482404_p64637104323"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p1846318107327"><a name="zh-cn_topic_0221482404_p1846318107327"></a><a name="zh-cn_topic_0221482404_p1846318107327"></a>IAM用户的其他信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row144501210103215"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p16464161019326"><a name="zh-cn_topic_0221482404_p16464161019326"></a><a name="zh-cn_topic_0221482404_p16464161019326"></a><a href="#zh-cn_topic_0221482404_response_Rs811UserLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p10465141016328"><a name="zh-cn_topic_0221482404_p10465141016328"></a><a name="zh-cn_topic_0221482404_p10465141016328"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p18465171023220"><a name="zh-cn_topic_0221482404_p18465171023220"></a><a name="zh-cn_topic_0221482404_p18465171023220"></a>IAM用户的资源链接信息。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  user.extra

<a name="zh-cn_topic_0221482404_response_Rs811UserExtra"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482404_row1466510183215"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482404_p0467110103214"><a name="zh-cn_topic_0221482404_p0467110103214"></a><a name="zh-cn_topic_0221482404_p0467110103214"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482404_p1446816104325"><a name="zh-cn_topic_0221482404_p1446816104325"></a><a name="zh-cn_topic_0221482404_p1446816104325"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482404_p17468191083213"><a name="zh-cn_topic_0221482404_p17468191083213"></a><a name="zh-cn_topic_0221482404_p17468191083213"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482404_row18466111083215"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p946818105324"><a name="zh-cn_topic_0221482404_p946818105324"></a><a name="zh-cn_topic_0221482404_p946818105324"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p74691910173211"><a name="zh-cn_topic_0221482404_p74691910173211"></a><a name="zh-cn_topic_0221482404_p74691910173211"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p1346915107321"><a name="zh-cn_topic_0221482404_p1346915107321"></a><a name="zh-cn_topic_0221482404_p1346915107321"></a>IAM用户描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row11466111019320"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p546971013211"><a name="zh-cn_topic_0221482404_p546971013211"></a><a name="zh-cn_topic_0221482404_p546971013211"></a>pwd_status</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p04702010103210"><a name="zh-cn_topic_0221482404_p04702010103210"></a><a name="zh-cn_topic_0221482404_p04702010103210"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p647001033210"><a name="zh-cn_topic_0221482404_p647001033210"></a><a name="zh-cn_topic_0221482404_p647001033210"></a>IAM用户密码状态。true：需要修改密码，false：正常。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row16466181063219"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p194702101327"><a name="zh-cn_topic_0221482404_p194702101327"></a><a name="zh-cn_topic_0221482404_p194702101327"></a>forceResetPwd</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p114719100320"><a name="zh-cn_topic_0221482404_p114719100320"></a><a name="zh-cn_topic_0221482404_p114719100320"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p20471201043213"><a name="zh-cn_topic_0221482404_p20471201043213"></a><a name="zh-cn_topic_0221482404_p20471201043213"></a>IAM用户下次登录是否强制重置密码。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row746691033220"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p247191019329"><a name="zh-cn_topic_0221482404_p247191019329"></a><a name="zh-cn_topic_0221482404_p247191019329"></a>last_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p144711106327"><a name="zh-cn_topic_0221482404_p144711106327"></a><a name="zh-cn_topic_0221482404_p144711106327"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p04722109323"><a name="zh-cn_topic_0221482404_p04722109323"></a><a name="zh-cn_topic_0221482404_p04722109323"></a>IAM用户退出系统前，在控制台最后访问的项目ID。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  user.links

<a name="zh-cn_topic_0221482404_response_Rs811UserLinks"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482404_row147213100323"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482404_p8473171043218"><a name="zh-cn_topic_0221482404_p8473171043218"></a><a name="zh-cn_topic_0221482404_p8473171043218"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482404_p114732109322"><a name="zh-cn_topic_0221482404_p114732109322"></a><a name="zh-cn_topic_0221482404_p114732109322"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482404_p11474141014326"><a name="zh-cn_topic_0221482404_p11474141014326"></a><a name="zh-cn_topic_0221482404_p11474141014326"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482404_row8472910163210"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482404_p147451063216"><a name="zh-cn_topic_0221482404_p147451063216"></a><a name="zh-cn_topic_0221482404_p147451063216"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482404_p147471014323"><a name="zh-cn_topic_0221482404_p147471014323"></a><a name="zh-cn_topic_0221482404_p147471014323"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482404_p847516108327"><a name="zh-cn_topic_0221482404_p847516108327"></a><a name="zh-cn_topic_0221482404_p847516108327"></a>资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482404_section1247581015322"></a>

```
PATCH https://iam.myhuaweicloud.com/v3/users/{user_id}
```

```
{
    "user": {
        "name": "IAMUser",
        "password": "IAMPassword@",
        "enabled": true,
        "pwd_status": false,
        "default_project_id": "aa2d97d7e62c4b7da3ffdfc11551f878",
        "description": "IAMDescription"
    }
}
```

## 响应示例<a name="zh-cn_topic_0221482404_section547791010329"></a>

**状态码为 200 时:**

请求成功。

```
{
    "user": {
        "pwd_status": false,
        "description": "IAMDescription",
        "name": "IAMUser",
        "extra": {
            "pwd_status": false,
            "forceResetPwd": false,
            "description": "IAMDescription",
            "last_project_id": "065a7c66da0010992ff7c0031e5a5e7d"
        },
        "forceResetPwd": false,
        "enabled": true,
        "links": {
            "self": "https://iam.myhuaweicloud.com/v3/users/07609fb9358010e21f7bc003751c7c32"
        },
        "last_project_id": "065a7c66da0010992ff7c0031e5a5e7d",
        "default_project_id": "aa2d97d7e62c4b7da3ffdfc11551f878",
        "id": "07609fb9358010e21f7bc003751c7c32",
        "domain_id": "d78cbac186b744899480f25bd02..."
    }
}
```

## 返回值<a name="zh-cn_topic_0221482404_section8484131053218"></a>

<a name="zh-cn_topic_0221482404_table2447"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482404_row94851410193212"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482404_p748613104322"><a name="zh-cn_topic_0221482404_p748613104322"></a><a name="zh-cn_topic_0221482404_p748613104322"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482404_p18486410103213"><a name="zh-cn_topic_0221482404_p18486410103213"></a><a name="zh-cn_topic_0221482404_p18486410103213"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482404_row7485121010327"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482404_p248718102327"><a name="zh-cn_topic_0221482404_p248718102327"></a><a name="zh-cn_topic_0221482404_p248718102327"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482404_p19487510103211"><a name="zh-cn_topic_0221482404_p19487510103211"></a><a name="zh-cn_topic_0221482404_p19487510103211"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row1448501017327"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482404_p748791018326"><a name="zh-cn_topic_0221482404_p748791018326"></a><a name="zh-cn_topic_0221482404_p748791018326"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482404_p14488121012325"><a name="zh-cn_topic_0221482404_p14488121012325"></a><a name="zh-cn_topic_0221482404_p14488121012325"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row14485171033219"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482404_p19488151018324"><a name="zh-cn_topic_0221482404_p19488151018324"></a><a name="zh-cn_topic_0221482404_p19488151018324"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482404_p1597110123212"><a name="zh-cn_topic_0221482404_p1597110123212"></a><a name="zh-cn_topic_0221482404_p1597110123212"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row9485171013327"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482404_p9597151013328"><a name="zh-cn_topic_0221482404_p9597151013328"></a><a name="zh-cn_topic_0221482404_p9597151013328"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482404_p1159791003217"><a name="zh-cn_topic_0221482404_p1159791003217"></a><a name="zh-cn_topic_0221482404_p1159791003217"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row1148561017328"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482404_p3597181083217"><a name="zh-cn_topic_0221482404_p3597181083217"></a><a name="zh-cn_topic_0221482404_p3597181083217"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482404_p8597141093217"><a name="zh-cn_topic_0221482404_p8597141093217"></a><a name="zh-cn_topic_0221482404_p8597141093217"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row1248514104322"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482404_p1459719104322"><a name="zh-cn_topic_0221482404_p1459719104322"></a><a name="zh-cn_topic_0221482404_p1459719104322"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482404_p1659811105327"><a name="zh-cn_topic_0221482404_p1659811105327"></a><a name="zh-cn_topic_0221482404_p1659811105327"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row44851010113217"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482404_p35981710163211"><a name="zh-cn_topic_0221482404_p35981710163211"></a><a name="zh-cn_topic_0221482404_p35981710163211"></a>409</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482404_p10598810143211"><a name="zh-cn_topic_0221482404_p10598810143211"></a><a name="zh-cn_topic_0221482404_p10598810143211"></a>资源冲突。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row5486101083214"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482404_p35981310103218"><a name="zh-cn_topic_0221482404_p35981310103218"></a><a name="zh-cn_topic_0221482404_p35981310103218"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482404_p135981210173218"><a name="zh-cn_topic_0221482404_p135981210173218"></a><a name="zh-cn_topic_0221482404_p135981210173218"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row24868106327"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482404_p1259881011325"><a name="zh-cn_topic_0221482404_p1259881011325"></a><a name="zh-cn_topic_0221482404_p1259881011325"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482404_p1359851043211"><a name="zh-cn_topic_0221482404_p1359851043211"></a><a name="zh-cn_topic_0221482404_p1359851043211"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row184861910153213"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482404_p18598161011322"><a name="zh-cn_topic_0221482404_p18598161011322"></a><a name="zh-cn_topic_0221482404_p18598161011322"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482404_p0598410163212"><a name="zh-cn_topic_0221482404_p0598410163212"></a><a name="zh-cn_topic_0221482404_p0598410163212"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482404_section75981510203216"></a>

<a name="zh-cn_topic_0221482404_table2448"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482404_row1649721013217"><th class="cellrowborder" valign="top" width="27.27272727272727%" id="mcps1.1.4.1.1"><p id="zh-cn_topic_0221482404_p759919106326"><a name="zh-cn_topic_0221482404_p759919106326"></a><a name="zh-cn_topic_0221482404_p759919106326"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="36.36363636363636%" id="mcps1.1.4.1.2"><p id="zh-cn_topic_0221482404_p10599141033217"><a name="zh-cn_topic_0221482404_p10599141033217"></a><a name="zh-cn_topic_0221482404_p10599141033217"></a>错误码</p>
</th>
<th class="cellrowborder" valign="top" width="36.36363636363636%" id="mcps1.1.4.1.3"><p id="zh-cn_topic_0221482404_p1959991010327"><a name="zh-cn_topic_0221482404_p1959991010327"></a><a name="zh-cn_topic_0221482404_p1959991010327"></a>错误信息</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482404_row164971410183216"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p85996103329"><a name="zh-cn_topic_0221482404_p85996103329"></a><a name="zh-cn_topic_0221482404_p85996103329"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p145991910133212"><a name="zh-cn_topic_0221482404_p145991910133212"></a><a name="zh-cn_topic_0221482404_p145991910133212"></a>1100</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p459971053212"><a name="zh-cn_topic_0221482404_p459971053212"></a><a name="zh-cn_topic_0221482404_p459971053212"></a>缺失必选参数。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row1049711013216"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p1659991093216"><a name="zh-cn_topic_0221482404_p1659991093216"></a><a name="zh-cn_topic_0221482404_p1659991093216"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p45991310143211"><a name="zh-cn_topic_0221482404_p45991310143211"></a><a name="zh-cn_topic_0221482404_p45991310143211"></a>1101</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p1559971019327"><a name="zh-cn_topic_0221482404_p1559971019327"></a><a name="zh-cn_topic_0221482404_p1559971019327"></a>用户名校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row549781073213"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p13600510193216"><a name="zh-cn_topic_0221482404_p13600510193216"></a><a name="zh-cn_topic_0221482404_p13600510193216"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p46007102323"><a name="zh-cn_topic_0221482404_p46007102323"></a><a name="zh-cn_topic_0221482404_p46007102323"></a>1102</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p16600171010322"><a name="zh-cn_topic_0221482404_p16600171010322"></a><a name="zh-cn_topic_0221482404_p16600171010322"></a>邮箱校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row1949731023220"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p1160071014327"><a name="zh-cn_topic_0221482404_p1160071014327"></a><a name="zh-cn_topic_0221482404_p1160071014327"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p136001910113219"><a name="zh-cn_topic_0221482404_p136001910113219"></a><a name="zh-cn_topic_0221482404_p136001910113219"></a>1103</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p9600111019327"><a name="zh-cn_topic_0221482404_p9600111019327"></a><a name="zh-cn_topic_0221482404_p9600111019327"></a>密码校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row0497310193218"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p11600151016325"><a name="zh-cn_topic_0221482404_p11600151016325"></a><a name="zh-cn_topic_0221482404_p11600151016325"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p360014101320"><a name="zh-cn_topic_0221482404_p360014101320"></a><a name="zh-cn_topic_0221482404_p360014101320"></a>1104</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p2060021003217"><a name="zh-cn_topic_0221482404_p2060021003217"></a><a name="zh-cn_topic_0221482404_p2060021003217"></a>手机号校验失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row10497101073210"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p760001043211"><a name="zh-cn_topic_0221482404_p760001043211"></a><a name="zh-cn_topic_0221482404_p760001043211"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p126011710113210"><a name="zh-cn_topic_0221482404_p126011710113210"></a><a name="zh-cn_topic_0221482404_p126011710113210"></a>1105</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p76011710163217"><a name="zh-cn_topic_0221482404_p76011710163217"></a><a name="zh-cn_topic_0221482404_p76011710163217"></a>xuser_type必须与xdomain_type相同。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row749711017325"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p46011310203220"><a name="zh-cn_topic_0221482404_p46011310203220"></a><a name="zh-cn_topic_0221482404_p46011310203220"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p26017107322"><a name="zh-cn_topic_0221482404_p26017107322"></a><a name="zh-cn_topic_0221482404_p26017107322"></a>1106</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p2601151019325"><a name="zh-cn_topic_0221482404_p2601151019325"></a><a name="zh-cn_topic_0221482404_p2601151019325"></a>国家码、手机号必须同时存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row9497171019322"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p1360151013323"><a name="zh-cn_topic_0221482404_p1360151013323"></a><a name="zh-cn_topic_0221482404_p1360151013323"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p1560118101325"><a name="zh-cn_topic_0221482404_p1560118101325"></a><a name="zh-cn_topic_0221482404_p1560118101325"></a>1107</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p56011610123211"><a name="zh-cn_topic_0221482404_p56011610123211"></a><a name="zh-cn_topic_0221482404_p56011610123211"></a>账号管理员不能被删除。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row8497161063215"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p8601151019326"><a name="zh-cn_topic_0221482404_p8601151019326"></a><a name="zh-cn_topic_0221482404_p8601151019326"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p12601510183211"><a name="zh-cn_topic_0221482404_p12601510183211"></a><a name="zh-cn_topic_0221482404_p12601510183211"></a>1108</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p1560141011321"><a name="zh-cn_topic_0221482404_p1560141011321"></a><a name="zh-cn_topic_0221482404_p1560141011321"></a>新密码不能与原密码相同。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row1498210153212"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p20602101017323"><a name="zh-cn_topic_0221482404_p20602101017323"></a><a name="zh-cn_topic_0221482404_p20602101017323"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p19602310113213"><a name="zh-cn_topic_0221482404_p19602310113213"></a><a name="zh-cn_topic_0221482404_p19602310113213"></a>1109</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p13602101018328"><a name="zh-cn_topic_0221482404_p13602101018328"></a><a name="zh-cn_topic_0221482404_p13602101018328"></a>用户名已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row949811083210"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p9602810153215"><a name="zh-cn_topic_0221482404_p9602810153215"></a><a name="zh-cn_topic_0221482404_p9602810153215"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p460281016326"><a name="zh-cn_topic_0221482404_p460281016326"></a><a name="zh-cn_topic_0221482404_p460281016326"></a>1110</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p116022108320"><a name="zh-cn_topic_0221482404_p116022108320"></a><a name="zh-cn_topic_0221482404_p116022108320"></a>邮箱已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row18498610193219"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p1960291033212"><a name="zh-cn_topic_0221482404_p1960291033212"></a><a name="zh-cn_topic_0221482404_p1960291033212"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p1560241073218"><a name="zh-cn_topic_0221482404_p1560241073218"></a><a name="zh-cn_topic_0221482404_p1560241073218"></a>1111</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p19602171043220"><a name="zh-cn_topic_0221482404_p19602171043220"></a><a name="zh-cn_topic_0221482404_p19602171043220"></a>手机号已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row12498151073220"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p1060261013212"><a name="zh-cn_topic_0221482404_p1060261013212"></a><a name="zh-cn_topic_0221482404_p1060261013212"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p17602161013322"><a name="zh-cn_topic_0221482404_p17602161013322"></a><a name="zh-cn_topic_0221482404_p17602161013322"></a>1113</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p4602910163215"><a name="zh-cn_topic_0221482404_p4602910163215"></a><a name="zh-cn_topic_0221482404_p4602910163215"></a>xuser_id、xuser_type已存在。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row10498141073214"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p11603141083216"><a name="zh-cn_topic_0221482404_p11603141083216"></a><a name="zh-cn_topic_0221482404_p11603141083216"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p860391011321"><a name="zh-cn_topic_0221482404_p860391011321"></a><a name="zh-cn_topic_0221482404_p860391011321"></a>1115</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p560331015321"><a name="zh-cn_topic_0221482404_p560331015321"></a><a name="zh-cn_topic_0221482404_p560331015321"></a>IAM用户数量达到最大限制。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482404_row10498131083219"><td class="cellrowborder" valign="top" width="27.27272727272727%" headers="mcps1.1.4.1.1 "><p id="zh-cn_topic_0221482404_p86041810163210"><a name="zh-cn_topic_0221482404_p86041810163210"></a><a name="zh-cn_topic_0221482404_p86041810163210"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.2 "><p id="zh-cn_topic_0221482404_p960412105329"><a name="zh-cn_topic_0221482404_p960412105329"></a><a name="zh-cn_topic_0221482404_p960412105329"></a>1117</p>
</td>
<td class="cellrowborder" valign="top" width="36.36363636363636%" headers="mcps1.1.4.1.3 "><p id="zh-cn_topic_0221482404_p17604171010327"><a name="zh-cn_topic_0221482404_p17604171010327"></a><a name="zh-cn_topic_0221482404_p17604171010327"></a>用户描述校验失败。</p>
</td>
</tr>
</tbody>
</table>

