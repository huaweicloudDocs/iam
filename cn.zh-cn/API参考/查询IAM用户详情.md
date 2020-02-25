# 查询IAM用户详情<a name="zh-cn_topic_0057845652"></a>

## 功能介绍<a name="zh-cn_topic_0221482415_section18572114919254"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/zh-cn_topic_0079496985.html)查询IAM用户详情，或IAM用户查询自己的用户详情。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 接口约束<a name="zh-cn_topic_0221482415_section205737498250"></a>

该接口无法查询IAM用户的手机号、邮箱等信息。如需查询上述信息，请参见：[查询IAM用户详情（推荐）](查询IAM用户详情（推荐）.md)。

## URI<a name="zh-cn_topic_0221482415_section95741449122516"></a>

GET /v3/users/\{user\_id\}

**表 1**  路径参数

<a name="zh-cn_topic_0221482415_table1857674915259"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482415_row15576174916256"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482415_p65771749182510"><a name="zh-cn_topic_0221482415_p65771749182510"></a><a name="zh-cn_topic_0221482415_p65771749182510"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482415_p7577184917256"><a name="zh-cn_topic_0221482415_p7577184917256"></a><a name="zh-cn_topic_0221482415_p7577184917256"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482415_p1578114932513"><a name="zh-cn_topic_0221482415_p1578114932513"></a><a name="zh-cn_topic_0221482415_p1578114932513"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482415_p65781849172519"><a name="zh-cn_topic_0221482415_p65781849172519"></a><a name="zh-cn_topic_0221482415_p65781849172519"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482415_row1757624902511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482415_p3579949122520"><a name="zh-cn_topic_0221482415_p3579949122520"></a><a name="zh-cn_topic_0221482415_p3579949122520"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482415_p10579349122511"><a name="zh-cn_topic_0221482415_p10579349122511"></a><a name="zh-cn_topic_0221482415_p10579349122511"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482415_p125801149132516"><a name="zh-cn_topic_0221482415_p125801149132516"></a><a name="zh-cn_topic_0221482415_p125801149132516"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482415_p18580204915256"><a name="zh-cn_topic_0221482415_p18580204915256"></a><a name="zh-cn_topic_0221482415_p18580204915256"></a>待查询的IAM用户ID，获取方式请参见：<a href="获取IAM用户-项目-用户组-委托的名称和ID.md">获取IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482415_section13581124914257"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482415_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482415_row0582194972519"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482415_p85837494258"><a name="zh-cn_topic_0221482415_p85837494258"></a><a name="zh-cn_topic_0221482415_p85837494258"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482415_p158344932514"><a name="zh-cn_topic_0221482415_p158344932514"></a><a name="zh-cn_topic_0221482415_p158344932514"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482415_p8584154910255"><a name="zh-cn_topic_0221482415_p8584154910255"></a><a name="zh-cn_topic_0221482415_p8584154910255"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482415_p658444952516"><a name="zh-cn_topic_0221482415_p658444952516"></a><a name="zh-cn_topic_0221482415_p658444952516"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482415_row15582174913255"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482415_p5585164962520"><a name="zh-cn_topic_0221482415_p5585164962520"></a><a name="zh-cn_topic_0221482415_p5585164962520"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482415_p7585204912517"><a name="zh-cn_topic_0221482415_p7585204912517"></a><a name="zh-cn_topic_0221482415_p7585204912517"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482415_p19586749102514"><a name="zh-cn_topic_0221482415_p19586749102514"></a><a name="zh-cn_topic_0221482415_p19586749102514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482415_p1058612492251"><a name="zh-cn_topic_0221482415_p1058612492251"></a><a name="zh-cn_topic_0221482415_p1058612492251"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row13582204917250"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482415_p145871049162519"><a name="zh-cn_topic_0221482415_p145871049162519"></a><a name="zh-cn_topic_0221482415_p145871049162519"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482415_p18587124942518"><a name="zh-cn_topic_0221482415_p18587124942518"></a><a name="zh-cn_topic_0221482415_p18587124942518"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482415_p1858894972519"><a name="zh-cn_topic_0221482415_p1858894972519"></a><a name="zh-cn_topic_0221482415_p1858894972519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482415_p115881549192514"><a name="zh-cn_topic_0221482415_p115881549192514"></a><a name="zh-cn_topic_0221482415_p115881549192514"></a><a href="https://support.huaweicloud.com/usermanual-iam/zh-cn_topic_0079496985.html" target="_blank" rel="noopener noreferrer">管理员</a>查询IAM用户详情：拥有Security Administrator权限的token。</p>
<p id="zh-cn_topic_0221482415_p13589449152511"><a name="zh-cn_topic_0221482415_p13589449152511"></a><a name="zh-cn_topic_0221482415_p13589449152511"></a>IAM用户查询自己的详情：URL中user_id所对应IAM用户的token（无需特殊权限）。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482415_section10589184932516"></a>

**表 3**  响应Body参数

<a name="zh-cn_topic_0221482415_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482415_row25901496254"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482415_p959154911250"><a name="zh-cn_topic_0221482415_p959154911250"></a><a name="zh-cn_topic_0221482415_p959154911250"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482415_p1559215495258"><a name="zh-cn_topic_0221482415_p1559215495258"></a><a name="zh-cn_topic_0221482415_p1559215495258"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482415_p659294952516"><a name="zh-cn_topic_0221482415_p659294952516"></a><a name="zh-cn_topic_0221482415_p659294952516"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482415_row18590949172516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p15593134910257"><a name="zh-cn_topic_0221482415_p15593134910257"></a><a name="zh-cn_topic_0221482415_p15593134910257"></a><a href="#zh-cn_topic_0221482415_response_Rs83User">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p195944494257"><a name="zh-cn_topic_0221482415_p195944494257"></a><a name="zh-cn_topic_0221482415_p195944494257"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p105941949172511"><a name="zh-cn_topic_0221482415_p105941949172511"></a><a name="zh-cn_topic_0221482415_p105941949172511"></a>IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  user

<a name="zh-cn_topic_0221482415_response_Rs83User"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482415_row13595649172516"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482415_p6597174952514"><a name="zh-cn_topic_0221482415_p6597174952514"></a><a name="zh-cn_topic_0221482415_p6597174952514"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482415_p16597134910253"><a name="zh-cn_topic_0221482415_p16597134910253"></a><a name="zh-cn_topic_0221482415_p16597134910253"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482415_p1559874972519"><a name="zh-cn_topic_0221482415_p1559874972519"></a><a name="zh-cn_topic_0221482415_p1559874972519"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482415_row3595749132514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p1598124992512"><a name="zh-cn_topic_0221482415_p1598124992512"></a><a name="zh-cn_topic_0221482415_p1598124992512"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p55991949152519"><a name="zh-cn_topic_0221482415_p55991949152519"></a><a name="zh-cn_topic_0221482415_p55991949152519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p959911496254"><a name="zh-cn_topic_0221482415_p959911496254"></a><a name="zh-cn_topic_0221482415_p959911496254"></a>IAM用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row05951049112520"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p1060094962518"><a name="zh-cn_topic_0221482415_p1060094962518"></a><a name="zh-cn_topic_0221482415_p1060094962518"></a><a href="#zh-cn_topic_0221482415_response_Rs83UserLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p136001449162518"><a name="zh-cn_topic_0221482415_p136001449162518"></a><a name="zh-cn_topic_0221482415_p136001449162518"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p6601154962517"><a name="zh-cn_topic_0221482415_p6601154962517"></a><a name="zh-cn_topic_0221482415_p6601154962517"></a>IAM用户的资源链接信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row65951149172515"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p136011249112517"><a name="zh-cn_topic_0221482415_p136011249112517"></a><a name="zh-cn_topic_0221482415_p136011249112517"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p156021349102515"><a name="zh-cn_topic_0221482415_p156021349102515"></a><a name="zh-cn_topic_0221482415_p156021349102515"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p1560311492259"><a name="zh-cn_topic_0221482415_p1560311492259"></a><a name="zh-cn_topic_0221482415_p1560311492259"></a>IAM用户所属账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row165950492252"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p3603194972514"><a name="zh-cn_topic_0221482415_p3603194972514"></a><a name="zh-cn_topic_0221482415_p3603194972514"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p1260484914254"><a name="zh-cn_topic_0221482415_p1260484914254"></a><a name="zh-cn_topic_0221482415_p1260484914254"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p1460454962512"><a name="zh-cn_topic_0221482415_p1460454962512"></a><a name="zh-cn_topic_0221482415_p1460454962512"></a>IAM用户是否启用。true表示启用，false表示停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row35957499253"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p7605184916257"><a name="zh-cn_topic_0221482415_p7605184916257"></a><a name="zh-cn_topic_0221482415_p7605184916257"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p8605124914259"><a name="zh-cn_topic_0221482415_p8605124914259"></a><a name="zh-cn_topic_0221482415_p8605124914259"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p10606114902515"><a name="zh-cn_topic_0221482415_p10606114902515"></a><a name="zh-cn_topic_0221482415_p10606114902515"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row45952049182519"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p116061849202519"><a name="zh-cn_topic_0221482415_p116061849202519"></a><a name="zh-cn_topic_0221482415_p116061849202519"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p1360734932513"><a name="zh-cn_topic_0221482415_p1360734932513"></a><a name="zh-cn_topic_0221482415_p1360734932513"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p9607164918253"><a name="zh-cn_topic_0221482415_p9607164918253"></a><a name="zh-cn_topic_0221482415_p9607164918253"></a>IAM用户密码过期时间（UTC时间），“null”表示密码不过期。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row659564962520"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p360817495253"><a name="zh-cn_topic_0221482415_p360817495253"></a><a name="zh-cn_topic_0221482415_p360817495253"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p20608104942519"><a name="zh-cn_topic_0221482415_p20608104942519"></a><a name="zh-cn_topic_0221482415_p20608104942519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p460974917258"><a name="zh-cn_topic_0221482415_p460974917258"></a><a name="zh-cn_topic_0221482415_p460974917258"></a>IAM用户描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row1359644912512"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p36091549122514"><a name="zh-cn_topic_0221482415_p36091549122514"></a><a name="zh-cn_topic_0221482415_p36091549122514"></a>pwd_status</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p7609194919255"><a name="zh-cn_topic_0221482415_p7609194919255"></a><a name="zh-cn_topic_0221482415_p7609194919255"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p361013493257"><a name="zh-cn_topic_0221482415_p361013493257"></a><a name="zh-cn_topic_0221482415_p361013493257"></a>IAM用户密码状态。true：需要修改密码，false：正常。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row7596104902518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p12610144962516"><a name="zh-cn_topic_0221482415_p12610144962516"></a><a name="zh-cn_topic_0221482415_p12610144962516"></a>forceResetPwd</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p8611149122510"><a name="zh-cn_topic_0221482415_p8611149122510"></a><a name="zh-cn_topic_0221482415_p8611149122510"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p1361174915251"><a name="zh-cn_topic_0221482415_p1361174915251"></a><a name="zh-cn_topic_0221482415_p1361174915251"></a>IAM用户下次登录是否强制重置密码。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row25961949102517"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p10612849192512"><a name="zh-cn_topic_0221482415_p10612849192512"></a><a name="zh-cn_topic_0221482415_p10612849192512"></a>default_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p16121249192518"><a name="zh-cn_topic_0221482415_p16121249192518"></a><a name="zh-cn_topic_0221482415_p16121249192518"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p1961304912515"><a name="zh-cn_topic_0221482415_p1961304912515"></a><a name="zh-cn_topic_0221482415_p1961304912515"></a>IAM用户登录控制台后默认跳转的项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row1259618497256"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p1661324952510"><a name="zh-cn_topic_0221482415_p1661324952510"></a><a name="zh-cn_topic_0221482415_p1661324952510"></a>last_project_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p5614154915255"><a name="zh-cn_topic_0221482415_p5614154915255"></a><a name="zh-cn_topic_0221482415_p5614154915255"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p12614154932515"><a name="zh-cn_topic_0221482415_p12614154932515"></a><a name="zh-cn_topic_0221482415_p12614154932515"></a>IAM用户退出系统前，在控制台最后访问的项目ID。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  user.links

<a name="zh-cn_topic_0221482415_response_Rs83UserLinks"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482415_row1461524922518"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482415_p161644910254"><a name="zh-cn_topic_0221482415_p161644910254"></a><a name="zh-cn_topic_0221482415_p161644910254"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482415_p361774982517"><a name="zh-cn_topic_0221482415_p361774982517"></a><a name="zh-cn_topic_0221482415_p361774982517"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482415_p19617144912251"><a name="zh-cn_topic_0221482415_p19617144912251"></a><a name="zh-cn_topic_0221482415_p19617144912251"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482415_row76153490251"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p196181549132511"><a name="zh-cn_topic_0221482415_p196181549132511"></a><a name="zh-cn_topic_0221482415_p196181549132511"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p761910498254"><a name="zh-cn_topic_0221482415_p761910498254"></a><a name="zh-cn_topic_0221482415_p761910498254"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p961914992517"><a name="zh-cn_topic_0221482415_p961914992517"></a><a name="zh-cn_topic_0221482415_p961914992517"></a>资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row761511498253"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p17620104919254"><a name="zh-cn_topic_0221482415_p17620104919254"></a><a name="zh-cn_topic_0221482415_p17620104919254"></a>previous</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p262194912519"><a name="zh-cn_topic_0221482415_p262194912519"></a><a name="zh-cn_topic_0221482415_p262194912519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p14621194912511"><a name="zh-cn_topic_0221482415_p14621194912511"></a><a name="zh-cn_topic_0221482415_p14621194912511"></a>前一邻接资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row461544982518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482415_p10622144982516"><a name="zh-cn_topic_0221482415_p10622144982516"></a><a name="zh-cn_topic_0221482415_p10622144982516"></a>next</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482415_p4622114932511"><a name="zh-cn_topic_0221482415_p4622114932511"></a><a name="zh-cn_topic_0221482415_p4622114932511"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482415_p6623349152510"><a name="zh-cn_topic_0221482415_p6623349152510"></a><a name="zh-cn_topic_0221482415_p6623349152510"></a>后一邻接资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482415_section14623204910257"></a>

```
GET https://iam.myhuaweicloud.com/v3/users/{user_id}
```

## 响应示例<a name="zh-cn_topic_0221482415_section196251549122512"></a>

**状态码为 200 时:**

请求成功。

```
{
    "user": {
        "pwd_status": true,
        "domain_id": "d78cbac186b744899480f25bd022f468",
        "last_project_id": "065a7c66da0010992ff7c0031e5a5e7d",
        "forceResetPwd": false,
        "name": "IAMUser",
        "description": "--",
        "password_expires_at": null,
        "links": {
            "next": null,
            "previous": null,
            "self": "https://iam.huaweicloud.com/v3/users/07609fb9358010e21f7bc003751c7c32"
        },
        "id": "7116d09f88fa41908676fdd4b039e95b",
        "enabled": true
    }
}
```

## 返回值<a name="zh-cn_topic_0221482415_section1963414917252"></a>

<a name="zh-cn_topic_0221482415_table2451"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482415_row06352498258"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482415_p19636194911250"><a name="zh-cn_topic_0221482415_p19636194911250"></a><a name="zh-cn_topic_0221482415_p19636194911250"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482415_p56371498257"><a name="zh-cn_topic_0221482415_p56371498257"></a><a name="zh-cn_topic_0221482415_p56371498257"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482415_row19635154992513"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482415_p663814493253"><a name="zh-cn_topic_0221482415_p663814493253"></a><a name="zh-cn_topic_0221482415_p663814493253"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482415_p15638114920252"><a name="zh-cn_topic_0221482415_p15638114920252"></a><a name="zh-cn_topic_0221482415_p15638114920252"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row12636749192517"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482415_p10639249192517"><a name="zh-cn_topic_0221482415_p10639249192517"></a><a name="zh-cn_topic_0221482415_p10639249192517"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482415_p8639124922516"><a name="zh-cn_topic_0221482415_p8639124922516"></a><a name="zh-cn_topic_0221482415_p8639124922516"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row1163612495256"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482415_p364024917256"><a name="zh-cn_topic_0221482415_p364024917256"></a><a name="zh-cn_topic_0221482415_p364024917256"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482415_p156403499259"><a name="zh-cn_topic_0221482415_p156403499259"></a><a name="zh-cn_topic_0221482415_p156403499259"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row11636449172517"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482415_p6641174920253"><a name="zh-cn_topic_0221482415_p6641174920253"></a><a name="zh-cn_topic_0221482415_p6641174920253"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482415_p15641949132512"><a name="zh-cn_topic_0221482415_p15641949132512"></a><a name="zh-cn_topic_0221482415_p15641949132512"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row11636104914252"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482415_p136424496259"><a name="zh-cn_topic_0221482415_p136424496259"></a><a name="zh-cn_topic_0221482415_p136424496259"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482415_p1764254919256"><a name="zh-cn_topic_0221482415_p1764254919256"></a><a name="zh-cn_topic_0221482415_p1764254919256"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row1063674912259"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482415_p166423494257"><a name="zh-cn_topic_0221482415_p166423494257"></a><a name="zh-cn_topic_0221482415_p166423494257"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482415_p1164384912512"><a name="zh-cn_topic_0221482415_p1164384912512"></a><a name="zh-cn_topic_0221482415_p1164384912512"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row66361498252"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482415_p13644349162514"><a name="zh-cn_topic_0221482415_p13644349162514"></a><a name="zh-cn_topic_0221482415_p13644349162514"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482415_p0644144913256"><a name="zh-cn_topic_0221482415_p0644144913256"></a><a name="zh-cn_topic_0221482415_p0644144913256"></a>资源冲突。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row26364496256"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482415_p116454492252"><a name="zh-cn_topic_0221482415_p116454492252"></a><a name="zh-cn_topic_0221482415_p116454492252"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482415_p8645124942510"><a name="zh-cn_topic_0221482415_p8645124942510"></a><a name="zh-cn_topic_0221482415_p8645124942510"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482415_row763694916254"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482415_p166461949122517"><a name="zh-cn_topic_0221482415_p166461949122517"></a><a name="zh-cn_topic_0221482415_p166461949122517"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482415_p96461949182510"><a name="zh-cn_topic_0221482415_p96461949182510"></a><a name="zh-cn_topic_0221482415_p96461949182510"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482415_section7646114912510"></a>

无

