# 查询IAM用户详情（推荐）<a name="iam_08_0003"></a>

## 功能介绍<a name="zh-cn_topic_0221482423_section1691123718235"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)查询IAM用户详情，或IAM用户查询自己的详情。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section41422113590"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=ShowUser)中调试该接口。

## URI<a name="zh-cn_topic_0221482423_section9913153762311"></a>

GET /v3.0/OS-USER/users/\{user\_id\}

**表 1**  路径参数

<a name="zh-cn_topic_0221482423_table091410375231"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482423_row1091483719231"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482423_p0915133713239"><a name="zh-cn_topic_0221482423_p0915133713239"></a><a name="zh-cn_topic_0221482423_p0915133713239"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482423_p8915153712238"><a name="zh-cn_topic_0221482423_p8915153712238"></a><a name="zh-cn_topic_0221482423_p8915153712238"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482423_p59168379233"><a name="zh-cn_topic_0221482423_p59168379233"></a><a name="zh-cn_topic_0221482423_p59168379233"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482423_p11916143732318"><a name="zh-cn_topic_0221482423_p11916143732318"></a><a name="zh-cn_topic_0221482423_p11916143732318"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482423_row14914183742317"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482423_p1291723718238"><a name="zh-cn_topic_0221482423_p1291723718238"></a><a name="zh-cn_topic_0221482423_p1291723718238"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482423_p13917163742317"><a name="zh-cn_topic_0221482423_p13917163742317"></a><a name="zh-cn_topic_0221482423_p13917163742317"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482423_p16918183762311"><a name="zh-cn_topic_0221482423_p16918183762311"></a><a name="zh-cn_topic_0221482423_p16918183762311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482423_p1391813377230"><a name="zh-cn_topic_0221482423_p1391813377230"></a><a name="zh-cn_topic_0221482423_p1391813377230"></a>待查询的IAM用户ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482423_section791923722312"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482423_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482423_row1892015371237"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482423_p13920143716234"><a name="zh-cn_topic_0221482423_p13920143716234"></a><a name="zh-cn_topic_0221482423_p13920143716234"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.18%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482423_p189211737192318"><a name="zh-cn_topic_0221482423_p189211737192318"></a><a name="zh-cn_topic_0221482423_p189211737192318"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.82%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482423_p1892163711238"><a name="zh-cn_topic_0221482423_p1892163711238"></a><a name="zh-cn_topic_0221482423_p1892163711238"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482423_p11922103714238"><a name="zh-cn_topic_0221482423_p11922103714238"></a><a name="zh-cn_topic_0221482423_p11922103714238"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482423_row9920193752315"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482423_p179241137182315"><a name="zh-cn_topic_0221482423_p179241137182315"></a><a name="zh-cn_topic_0221482423_p179241137182315"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="10.18%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482423_p692513717237"><a name="zh-cn_topic_0221482423_p692513717237"></a><a name="zh-cn_topic_0221482423_p692513717237"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.82%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482423_p19252037202318"><a name="zh-cn_topic_0221482423_p19252037202318"></a><a name="zh-cn_topic_0221482423_p19252037202318"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482423_p2926123720236"><a name="zh-cn_topic_0221482423_p2926123720236"></a><a name="zh-cn_topic_0221482423_p2926123720236"></a><u id="u39439113483"><a name="u39439113483"></a><a name="u39439113483"></a><a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a></u><u id="u199449111482"><a name="u199449111482"></a><a name="u199449111482"></a></u>查询IAM用户详情：请参见<a href="授权项.md">授权项</a>。</p>
<p id="zh-cn_topic_0221482423_p8926837102318"><a name="zh-cn_topic_0221482423_p8926837102318"></a><a name="zh-cn_topic_0221482423_p8926837102318"></a>IAM用户查询自己的详情：URL中user_id所对应IAM用户的token（无需特殊权限）。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482423_section492773762310"></a>

**表 3**  响应Body参数

<a name="zh-cn_topic_0221482423_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482423_row11928193732313"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482423_p9929103772311"><a name="zh-cn_topic_0221482423_p9929103772311"></a><a name="zh-cn_topic_0221482423_p9929103772311"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482423_p69291937112312"><a name="zh-cn_topic_0221482423_p69291937112312"></a><a name="zh-cn_topic_0221482423_p69291937112312"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482423_p1893019373235"><a name="zh-cn_topic_0221482423_p1893019373235"></a><a name="zh-cn_topic_0221482423_p1893019373235"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482423_row392893719236"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p169309375239"><a name="zh-cn_topic_0221482423_p169309375239"></a><a name="zh-cn_topic_0221482423_p169309375239"></a><a href="#zh-cn_topic_0221482423_response_Rs82User">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p49316374234"><a name="zh-cn_topic_0221482423_p49316374234"></a><a name="zh-cn_topic_0221482423_p49316374234"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p5931143792312"><a name="zh-cn_topic_0221482423_p5931143792312"></a><a name="zh-cn_topic_0221482423_p5931143792312"></a>IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  user

<a name="zh-cn_topic_0221482423_response_Rs82User"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482423_row39327374235"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482423_p69334374238"><a name="zh-cn_topic_0221482423_p69334374238"></a><a name="zh-cn_topic_0221482423_p69334374238"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482423_p6934237162311"><a name="zh-cn_topic_0221482423_p6934237162311"></a><a name="zh-cn_topic_0221482423_p6934237162311"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482423_p39341637112312"><a name="zh-cn_topic_0221482423_p39341637112312"></a><a name="zh-cn_topic_0221482423_p39341637112312"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482423_row193219379231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p1593543732313"><a name="zh-cn_topic_0221482423_p1593543732313"></a><a name="zh-cn_topic_0221482423_p1593543732313"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p8935637142318"><a name="zh-cn_topic_0221482423_p8935637142318"></a><a name="zh-cn_topic_0221482423_p8935637142318"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p1393612379235"><a name="zh-cn_topic_0221482423_p1393612379235"></a><a name="zh-cn_topic_0221482423_p1393612379235"></a>IAM用户是否启用。true表示启用，false表示停用，默认为true。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row193283782316"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p19936237142313"><a name="zh-cn_topic_0221482423_p19936237142313"></a><a name="zh-cn_topic_0221482423_p19936237142313"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p179377371235"><a name="zh-cn_topic_0221482423_p179377371235"></a><a name="zh-cn_topic_0221482423_p179377371235"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p18938937192316"><a name="zh-cn_topic_0221482423_p18938937192316"></a><a name="zh-cn_topic_0221482423_p18938937192316"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row199325378231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p2938237142311"><a name="zh-cn_topic_0221482423_p2938237142311"></a><a name="zh-cn_topic_0221482423_p2938237142311"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p119391537102315"><a name="zh-cn_topic_0221482423_p119391537102315"></a><a name="zh-cn_topic_0221482423_p119391537102315"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p129402377232"><a name="zh-cn_topic_0221482423_p129402377232"></a><a name="zh-cn_topic_0221482423_p129402377232"></a>IAM用户所属帐号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row12932183717232"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p194033792319"><a name="zh-cn_topic_0221482423_p194033792319"></a><a name="zh-cn_topic_0221482423_p194033792319"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p13941937112310"><a name="zh-cn_topic_0221482423_p13941937112310"></a><a name="zh-cn_topic_0221482423_p13941937112310"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p194110376230"><a name="zh-cn_topic_0221482423_p194110376230"></a><a name="zh-cn_topic_0221482423_p194110376230"></a>IAM用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row0932143732314"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p16942163712314"><a name="zh-cn_topic_0221482423_p16942163712314"></a><a name="zh-cn_topic_0221482423_p16942163712314"></a><a href="#zh-cn_topic_0221482423_response_Rs82UserLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p199428372233"><a name="zh-cn_topic_0221482423_p199428372233"></a><a name="zh-cn_topic_0221482423_p199428372233"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p12943537142313"><a name="zh-cn_topic_0221482423_p12943537142313"></a><a name="zh-cn_topic_0221482423_p12943537142313"></a>IAM用户的资源链接信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row893219374231"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p1894373792314"><a name="zh-cn_topic_0221482423_p1894373792314"></a><a name="zh-cn_topic_0221482423_p1894373792314"></a>xuser_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p7944123712316"><a name="zh-cn_topic_0221482423_p7944123712316"></a><a name="zh-cn_topic_0221482423_p7944123712316"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p9944037162318"><a name="zh-cn_topic_0221482423_p9944037162318"></a><a name="zh-cn_topic_0221482423_p9944037162318"></a>IAM用户在外部系统中的ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row189321837162310"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p189451537152317"><a name="zh-cn_topic_0221482423_p189451537152317"></a><a name="zh-cn_topic_0221482423_p189451537152317"></a>xuser_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p129451537122310"><a name="zh-cn_topic_0221482423_p129451537122310"></a><a name="zh-cn_topic_0221482423_p129451537122310"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p1494615379232"><a name="zh-cn_topic_0221482423_p1494615379232"></a><a name="zh-cn_topic_0221482423_p1494615379232"></a>IAM用户在外部系统中的类型。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row193253732310"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p794712377238"><a name="zh-cn_topic_0221482423_p794712377238"></a><a name="zh-cn_topic_0221482423_p794712377238"></a>areacode</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p894713782314"><a name="zh-cn_topic_0221482423_p894713782314"></a><a name="zh-cn_topic_0221482423_p894713782314"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p1494823717233"><a name="zh-cn_topic_0221482423_p1494823717233"></a><a name="zh-cn_topic_0221482423_p1494823717233"></a>IAM用户手机号的国家码。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row993273716236"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p1194833722311"><a name="zh-cn_topic_0221482423_p1194833722311"></a><a name="zh-cn_topic_0221482423_p1194833722311"></a>email</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p79491137192314"><a name="zh-cn_topic_0221482423_p79491137192314"></a><a name="zh-cn_topic_0221482423_p79491137192314"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p1094933718236"><a name="zh-cn_topic_0221482423_p1094933718236"></a><a name="zh-cn_topic_0221482423_p1094933718236"></a>IAM用户邮箱。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row1693213371234"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p2950193722316"><a name="zh-cn_topic_0221482423_p2950193722316"></a><a name="zh-cn_topic_0221482423_p2950193722316"></a>phone</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p395073710230"><a name="zh-cn_topic_0221482423_p395073710230"></a><a name="zh-cn_topic_0221482423_p395073710230"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p17951183718231"><a name="zh-cn_topic_0221482423_p17951183718231"></a><a name="zh-cn_topic_0221482423_p17951183718231"></a>IAM用户手机号。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row2093218376232"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p1395143718234"><a name="zh-cn_topic_0221482423_p1395143718234"></a><a name="zh-cn_topic_0221482423_p1395143718234"></a>pwd_status</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p89521337142311"><a name="zh-cn_topic_0221482423_p89521337142311"></a><a name="zh-cn_topic_0221482423_p89521337142311"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p129521737192310"><a name="zh-cn_topic_0221482423_p129521737192310"></a><a name="zh-cn_topic_0221482423_p129521737192310"></a>IAM用户密码状态。true：需要修改密码，false：正常。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row5932193772316"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482423_p139531337182312"><a name="zh-cn_topic_0221482423_p139531337182312"></a><a name="zh-cn_topic_0221482423_p139531337182312"></a>update_time</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482423_p9953637182317"><a name="zh-cn_topic_0221482423_p9953637182317"></a><a name="zh-cn_topic_0221482423_p9953637182317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482423_p1995443710237"><a name="zh-cn_topic_0221482423_p1995443710237"></a><a name="zh-cn_topic_0221482423_p1995443710237"></a>IAM用户更新时间。</p>
</td>
</tr>
<tr id="row1461843453112"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p450816435318"><a name="p450816435318"></a><a name="p450816435318"></a>create_time</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1450812436312"><a name="p1450812436312"></a><a name="p1450812436312"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p14508194313314"><a name="p14508194313314"></a><a name="p14508194313314"></a>IAM用户创建时间。</p>
</td>
</tr>
<tr id="row12619113443111"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p7508104333119"><a name="p7508104333119"></a><a name="p7508104333119"></a>last_login_time</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p850814363116"><a name="p850814363116"></a><a name="p850814363116"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p4508154383114"><a name="p4508154383114"></a><a name="p4508154383114"></a>IAM用户最后登录时间。</p>
</td>
</tr>
<tr id="row2619334113111"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p050874373114"><a name="p050874373114"></a><a name="p050874373114"></a>pwd_strength</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p10508543173117"><a name="p10508543173117"></a><a name="p10508543173117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p150810436316"><a name="p150810436316"></a><a name="p150810436316"></a>IAM用户密码强度。结果为Low/Medium/Strong/None，分别表示密码强度低/中/高/无。</p>
</td>
</tr>
<tr id="row17871132282219"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p780093110228"><a name="p780093110228"></a><a name="p780093110228"></a>is_domain_owner</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p12800431152217"><a name="p12800431152217"></a><a name="p12800431152217"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1880014313229"><a name="p1880014313229"></a><a name="p1880014313229"></a>IAM用户是否为帐号。</p>
</td>
</tr>
<tr id="row9189115912545"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1258313510498"><a name="p1258313510498"></a><a name="p1258313510498"></a>access_mode</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p185832513490"><a name="p185832513490"></a><a name="p185832513490"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p17583125114912"><a name="p17583125114912"></a><a name="p17583125114912"></a>IAM用户访问方式。</p>
<a name="ul101759371511"></a><a name="ul101759371511"></a><ul id="ul101759371511"><li>default：默认访问模式，编程访问和管理控制台访问。</li><li>programmatic：编程访问。</li><li>console：管理控制台访问。</li></ul>
</td>
</tr>
<tr id="row17872172232218"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p7800731142212"><a name="p7800731142212"></a><a name="p7800731142212"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p17800631102215"><a name="p17800631102215"></a><a name="p17800631102215"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p38005318220"><a name="p38005318220"></a><a name="p38005318220"></a>IAM用户描述信息。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  user.links

<a name="zh-cn_topic_0221482423_response_Rs82UserLinks"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482423_row79549370238"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p375364594614"><a name="p375364594614"></a><a name="p375364594614"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p17531545104615"><a name="p17531545104615"></a><a name="p17531545104615"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p157541845184611"><a name="p157541845184611"></a><a name="p157541845184611"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482423_row17954237142310"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1275474517468"><a name="p1275474517468"></a><a name="p1275474517468"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p9754164594610"><a name="p9754164594610"></a><a name="p9754164594610"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p127545455461"><a name="p127545455461"></a><a name="p127545455461"></a>资源链接地址。</p>
</td>
</tr>
<tr id="row16439145418508"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p275413459466"><a name="p275413459466"></a><a name="p275413459466"></a>previous</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1775484513469"><a name="p1775484513469"></a><a name="p1775484513469"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1675464534619"><a name="p1675464534619"></a><a name="p1675464534619"></a>前一邻接资源链接地址。</p>
</td>
</tr>
<tr id="row11439125485020"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p8755745144610"><a name="p8755745144610"></a><a name="p8755745144610"></a>next</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p8755194513468"><a name="p8755194513468"></a><a name="p8755194513468"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p207551645174617"><a name="p207551645174617"></a><a name="p207551645174617"></a>后一邻接资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482423_section395883715237"></a>

```
GET https://iam.myhuaweicloud.com/v3.0/OS-USER/users/{user_id}
```

## 响应示例<a name="zh-cn_topic_0221482423_section6961137162313"></a>

**状态码为 200 时:**

请求成功。

```
{
  "user" : {
    "pwd_strength" : "Strong",
    "create_time" : "2020-07-08 02:19:03.0",
    "last_login_time" : null,
    "areacode" : "",
    "enabled" : true,
    "domain_id" : "086ba757f90089cf0fe5c000dbe7f...",
    "xuser_id" : "",
    "pwd_status" : false,
    "update_time" : null,
    "phone" : "-",
    "is_domain_owner" : false, 
    "access_mode" : "default",
    "name" : "autotest1",
    "links" : {
      "next" : null,
      "previous" : null,
      "self" : "https://iam.myhuaweicloud.com/v3.0/OS-USER/users/093f75808b8089ba1f6dc000c7cac..."
    },
    "id" : "093f75808b8089ba1f6dc000c7cac...",
    "xuser_type" : "",
    "email" : "",
    "description" : "aaa" 
  }
}
```

## 返回值<a name="zh-cn_topic_0221482423_section99707375232"></a>

<a name="zh-cn_topic_0221482423_table2446"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482423_row397193792320"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482423_p29721437152316"><a name="zh-cn_topic_0221482423_p29721437152316"></a><a name="zh-cn_topic_0221482423_p29721437152316"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482423_p7972143715238"><a name="zh-cn_topic_0221482423_p7972143715238"></a><a name="zh-cn_topic_0221482423_p7972143715238"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482423_row139711837122311"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482423_p79739371238"><a name="zh-cn_topic_0221482423_p79739371238"></a><a name="zh-cn_topic_0221482423_p79739371238"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482423_p6973153715238"><a name="zh-cn_topic_0221482423_p6973153715238"></a><a name="zh-cn_topic_0221482423_p6973153715238"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row169714376234"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482423_p4976183782315"><a name="zh-cn_topic_0221482423_p4976183782315"></a><a name="zh-cn_topic_0221482423_p4976183782315"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482423_p1097619374232"><a name="zh-cn_topic_0221482423_p1097619374232"></a><a name="zh-cn_topic_0221482423_p1097619374232"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row16971113782313"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482423_p997715375236"><a name="zh-cn_topic_0221482423_p997715375236"></a><a name="zh-cn_topic_0221482423_p997715375236"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482423_p1197763702310"><a name="zh-cn_topic_0221482423_p1197763702310"></a><a name="zh-cn_topic_0221482423_p1197763702310"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row797103792316"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482423_p2978537152313"><a name="zh-cn_topic_0221482423_p2978537152313"></a><a name="zh-cn_topic_0221482423_p2978537152313"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482423_p6978133792316"><a name="zh-cn_topic_0221482423_p6978133792316"></a><a name="zh-cn_topic_0221482423_p6978133792316"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482423_row1797163719230"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482423_p10981133752316"><a name="zh-cn_topic_0221482423_p10981133752316"></a><a name="zh-cn_topic_0221482423_p10981133752316"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482423_p798153732316"><a name="zh-cn_topic_0221482423_p798153732316"></a><a name="zh-cn_topic_0221482423_p798153732316"></a>内部服务错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482423_section1698317379234"></a>

请参考[错误码](错误码.md)。

