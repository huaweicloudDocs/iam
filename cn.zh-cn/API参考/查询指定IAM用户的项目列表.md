# 查询指定IAM用户的项目列表<a name="iam_06_0002"></a>

## 功能介绍<a name="zh-cn_topic_0221482392_section167891320114010"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)查询指定IAM用户的项目列表，或IAM用户查询自己的项目列表。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="zh-cn_topic_0221482392_section147912207407"></a>

GET /v3/users/\{user\_id\}/projects

**表 1**  路径参数

<a name="zh-cn_topic_0221482392_table16793520164019"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482392_row1679272016407"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482392_p17793102014014"><a name="zh-cn_topic_0221482392_p17793102014014"></a><a name="zh-cn_topic_0221482392_p17793102014014"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482392_p1079372014408"><a name="zh-cn_topic_0221482392_p1079372014408"></a><a name="zh-cn_topic_0221482392_p1079372014408"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482392_p3794112014403"><a name="zh-cn_topic_0221482392_p3794112014403"></a><a name="zh-cn_topic_0221482392_p3794112014403"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482392_p5795120184016"><a name="zh-cn_topic_0221482392_p5795120184016"></a><a name="zh-cn_topic_0221482392_p5795120184016"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482392_row17792112014020"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482392_p57951820184014"><a name="zh-cn_topic_0221482392_p57951820184014"></a><a name="zh-cn_topic_0221482392_p57951820184014"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482392_p20796182014014"><a name="zh-cn_topic_0221482392_p20796182014014"></a><a name="zh-cn_topic_0221482392_p20796182014014"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482392_p979616208401"><a name="zh-cn_topic_0221482392_p979616208401"></a><a name="zh-cn_topic_0221482392_p979616208401"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482392_p197971520124018"><a name="zh-cn_topic_0221482392_p197971520124018"></a><a name="zh-cn_topic_0221482392_p197971520124018"></a>待查询的IAM用户ID，获取方式请参见：<a href="获取账号-IAM用户-项目-用户组-委托的名称和ID.md">获取账号、IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482392_section11797152054014"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482392_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482392_row1779813209403"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482392_p9799162012406"><a name="zh-cn_topic_0221482392_p9799162012406"></a><a name="zh-cn_topic_0221482392_p9799162012406"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482392_p67992020174010"><a name="zh-cn_topic_0221482392_p67992020174010"></a><a name="zh-cn_topic_0221482392_p67992020174010"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482392_p1180072024012"><a name="zh-cn_topic_0221482392_p1180072024012"></a><a name="zh-cn_topic_0221482392_p1180072024012"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482392_p080112011402"><a name="zh-cn_topic_0221482392_p080112011402"></a><a name="zh-cn_topic_0221482392_p080112011402"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482392_row137981920204012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482392_p1280122012408"><a name="zh-cn_topic_0221482392_p1280122012408"></a><a name="zh-cn_topic_0221482392_p1280122012408"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482392_p2080212205402"><a name="zh-cn_topic_0221482392_p2080212205402"></a><a name="zh-cn_topic_0221482392_p2080212205402"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482392_p1980216209401"><a name="zh-cn_topic_0221482392_p1980216209401"></a><a name="zh-cn_topic_0221482392_p1980216209401"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482392_p38031420164012"><a name="zh-cn_topic_0221482392_p38031420164012"></a><a name="zh-cn_topic_0221482392_p38031420164012"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row57981202404"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482392_p380317203404"><a name="zh-cn_topic_0221482392_p380317203404"></a><a name="zh-cn_topic_0221482392_p380317203404"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482392_p7804202014011"><a name="zh-cn_topic_0221482392_p7804202014011"></a><a name="zh-cn_topic_0221482392_p7804202014011"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482392_p1580410206405"><a name="zh-cn_topic_0221482392_p1580410206405"></a><a name="zh-cn_topic_0221482392_p1580410206405"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482392_p58051820144016"><a name="zh-cn_topic_0221482392_p58051820144016"></a><a name="zh-cn_topic_0221482392_p58051820144016"></a><a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询指定IAM用户的项目列表：拥有Security Administrator权限的token。</p>
<p id="zh-cn_topic_0221482392_p7805122011406"><a name="zh-cn_topic_0221482392_p7805122011406"></a><a name="zh-cn_topic_0221482392_p7805122011406"></a>IAM用户查询自身项目列表：URL中user_id所对应IAM用户的token（无需特殊权限）。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482392_section128061420114011"></a>

**表 3**  响应Body参数

<a name="zh-cn_topic_0221482392_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482392_row128070207407"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482392_p198085209401"><a name="zh-cn_topic_0221482392_p198085209401"></a><a name="zh-cn_topic_0221482392_p198085209401"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482392_p380842024015"><a name="zh-cn_topic_0221482392_p380842024015"></a><a name="zh-cn_topic_0221482392_p380842024015"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482392_p2809152014011"><a name="zh-cn_topic_0221482392_p2809152014011"></a><a name="zh-cn_topic_0221482392_p2809152014011"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482392_row1680782024011"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p381015203409"><a name="zh-cn_topic_0221482392_p381015203409"></a><a name="zh-cn_topic_0221482392_p381015203409"></a><a href="#zh-cn_topic_0221482392_response_Rs62Links">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p5810192016407"><a name="zh-cn_topic_0221482392_p5810192016407"></a><a name="zh-cn_topic_0221482392_p5810192016407"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p1081111209405"><a name="zh-cn_topic_0221482392_p1081111209405"></a><a name="zh-cn_topic_0221482392_p1081111209405"></a>资源链接信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row11807220124017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p10811720184017"><a name="zh-cn_topic_0221482392_p10811720184017"></a><a name="zh-cn_topic_0221482392_p10811720184017"></a><a href="#zh-cn_topic_0221482392_response_Rs61ProjectsArritem">projects</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p6812102044017"><a name="zh-cn_topic_0221482392_p6812102044017"></a><a name="zh-cn_topic_0221482392_p6812102044017"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p8813020194015"><a name="zh-cn_topic_0221482392_p8813020194015"></a><a name="zh-cn_topic_0221482392_p8813020194015"></a>项目信息列表。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  links

<a name="zh-cn_topic_0221482392_response_Rs62Links"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482392_row381320202405"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482392_p11814192014406"><a name="zh-cn_topic_0221482392_p11814192014406"></a><a name="zh-cn_topic_0221482392_p11814192014406"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482392_p781511201407"><a name="zh-cn_topic_0221482392_p781511201407"></a><a name="zh-cn_topic_0221482392_p781511201407"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482392_p3815122016406"><a name="zh-cn_topic_0221482392_p3815122016406"></a><a name="zh-cn_topic_0221482392_p3815122016406"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482392_row2813202064012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p1481612019401"><a name="zh-cn_topic_0221482392_p1481612019401"></a><a name="zh-cn_topic_0221482392_p1481612019401"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p138164206408"><a name="zh-cn_topic_0221482392_p138164206408"></a><a name="zh-cn_topic_0221482392_p138164206408"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p1881762018404"><a name="zh-cn_topic_0221482392_p1881762018404"></a><a name="zh-cn_topic_0221482392_p1881762018404"></a>资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row88131020114016"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p381716205406"><a name="zh-cn_topic_0221482392_p381716205406"></a><a name="zh-cn_topic_0221482392_p381716205406"></a>previous</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p881812201405"><a name="zh-cn_topic_0221482392_p881812201405"></a><a name="zh-cn_topic_0221482392_p881812201405"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p14819132044018"><a name="zh-cn_topic_0221482392_p14819132044018"></a><a name="zh-cn_topic_0221482392_p14819132044018"></a>前一邻接资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row15813152013406"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p1581932019404"><a name="zh-cn_topic_0221482392_p1581932019404"></a><a name="zh-cn_topic_0221482392_p1581932019404"></a>next</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p1182022074012"><a name="zh-cn_topic_0221482392_p1182022074012"></a><a name="zh-cn_topic_0221482392_p1182022074012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p582082020407"><a name="zh-cn_topic_0221482392_p582082020407"></a><a name="zh-cn_topic_0221482392_p582082020407"></a>后一邻接资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  projects

<a name="zh-cn_topic_0221482392_response_Rs61ProjectsArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482392_row10821920134010"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482392_p1382202014018"><a name="zh-cn_topic_0221482392_p1382202014018"></a><a name="zh-cn_topic_0221482392_p1382202014018"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482392_p188221920144013"><a name="zh-cn_topic_0221482392_p188221920144013"></a><a name="zh-cn_topic_0221482392_p188221920144013"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482392_p17823720144017"><a name="zh-cn_topic_0221482392_p17823720144017"></a><a name="zh-cn_topic_0221482392_p17823720144017"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482392_row20821620164019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p48231120154019"><a name="zh-cn_topic_0221482392_p48231120154019"></a><a name="zh-cn_topic_0221482392_p48231120154019"></a>is_domain</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p682412094013"><a name="zh-cn_topic_0221482392_p682412094013"></a><a name="zh-cn_topic_0221482392_p682412094013"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p1282410201407"><a name="zh-cn_topic_0221482392_p1282410201407"></a><a name="zh-cn_topic_0221482392_p1282410201407"></a>false.</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row38214206401"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p2082562034017"><a name="zh-cn_topic_0221482392_p2082562034017"></a><a name="zh-cn_topic_0221482392_p2082562034017"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p1082562013409"><a name="zh-cn_topic_0221482392_p1082562013409"></a><a name="zh-cn_topic_0221482392_p1082562013409"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p3826220164013"><a name="zh-cn_topic_0221482392_p3826220164013"></a><a name="zh-cn_topic_0221482392_p3826220164013"></a>项目描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row482142054019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p1782720202406"><a name="zh-cn_topic_0221482392_p1782720202406"></a><a name="zh-cn_topic_0221482392_p1782720202406"></a><a href="#zh-cn_topic_0221482392_response_Rs61ProjectsArritemLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p3827120134016"><a name="zh-cn_topic_0221482392_p3827120134016"></a><a name="zh-cn_topic_0221482392_p3827120134016"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p1282842013401"><a name="zh-cn_topic_0221482392_p1282842013401"></a><a name="zh-cn_topic_0221482392_p1282842013401"></a>项目的资源链接。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row13821102020401"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p1828192074010"><a name="zh-cn_topic_0221482392_p1828192074010"></a><a name="zh-cn_topic_0221482392_p1828192074010"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p19829102054014"><a name="zh-cn_topic_0221482392_p19829102054014"></a><a name="zh-cn_topic_0221482392_p19829102054014"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p118291020124013"><a name="zh-cn_topic_0221482392_p118291020124013"></a><a name="zh-cn_topic_0221482392_p118291020124013"></a>项目是否可用。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row482111206405"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p883010209402"><a name="zh-cn_topic_0221482392_p883010209402"></a><a name="zh-cn_topic_0221482392_p883010209402"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p883062015403"><a name="zh-cn_topic_0221482392_p883062015403"></a><a name="zh-cn_topic_0221482392_p883062015403"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p0831172094013"><a name="zh-cn_topic_0221482392_p0831172094013"></a><a name="zh-cn_topic_0221482392_p0831172094013"></a>项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row14821112004011"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p108311320184020"><a name="zh-cn_topic_0221482392_p108311320184020"></a><a name="zh-cn_topic_0221482392_p108311320184020"></a>parent_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p18832020194015"><a name="zh-cn_topic_0221482392_p18832020194015"></a><a name="zh-cn_topic_0221482392_p18832020194015"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p983313209400"><a name="zh-cn_topic_0221482392_p983313209400"></a><a name="zh-cn_topic_0221482392_p983313209400"></a>如果查询自己创建的项目，则此处返回所属区域的项目ID。</p>
<p id="zh-cn_topic_0221482392_p28334204403"><a name="zh-cn_topic_0221482392_p28334204403"></a><a name="zh-cn_topic_0221482392_p28334204403"></a>如果查询的是系统内置项目，如cn-north-4，则此处返回账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row198212020154012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p7834182012407"><a name="zh-cn_topic_0221482392_p7834182012407"></a><a name="zh-cn_topic_0221482392_p7834182012407"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p10834202011405"><a name="zh-cn_topic_0221482392_p10834202011405"></a><a name="zh-cn_topic_0221482392_p10834202011405"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p583532054015"><a name="zh-cn_topic_0221482392_p583532054015"></a><a name="zh-cn_topic_0221482392_p583532054015"></a>项目所属账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row082112094016"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p158351220114020"><a name="zh-cn_topic_0221482392_p158351220114020"></a><a name="zh-cn_topic_0221482392_p158351220114020"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p10836120164018"><a name="zh-cn_topic_0221482392_p10836120164018"></a><a name="zh-cn_topic_0221482392_p10836120164018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p1836152004011"><a name="zh-cn_topic_0221482392_p1836152004011"></a><a name="zh-cn_topic_0221482392_p1836152004011"></a>项目名称。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  projects.links

<a name="zh-cn_topic_0221482392_response_Rs61ProjectsArritemLinks"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482392_row7837720194018"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482392_p683882034012"><a name="zh-cn_topic_0221482392_p683882034012"></a><a name="zh-cn_topic_0221482392_p683882034012"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482392_p0838112054015"><a name="zh-cn_topic_0221482392_p0838112054015"></a><a name="zh-cn_topic_0221482392_p0838112054015"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482392_p983918203405"><a name="zh-cn_topic_0221482392_p983918203405"></a><a name="zh-cn_topic_0221482392_p983918203405"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482392_row20837102074010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p9839320104020"><a name="zh-cn_topic_0221482392_p9839320104020"></a><a name="zh-cn_topic_0221482392_p9839320104020"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p484042074018"><a name="zh-cn_topic_0221482392_p484042074018"></a><a name="zh-cn_topic_0221482392_p484042074018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p13840162012403"><a name="zh-cn_topic_0221482392_p13840162012403"></a><a name="zh-cn_topic_0221482392_p13840162012403"></a>资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row3837182034020"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p13841152012405"><a name="zh-cn_topic_0221482392_p13841152012405"></a><a name="zh-cn_topic_0221482392_p13841152012405"></a>previous</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p1284212203407"><a name="zh-cn_topic_0221482392_p1284212203407"></a><a name="zh-cn_topic_0221482392_p1284212203407"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p1684292074019"><a name="zh-cn_topic_0221482392_p1684292074019"></a><a name="zh-cn_topic_0221482392_p1684292074019"></a>前一邻接资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row7837172012403"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482392_p198431920144010"><a name="zh-cn_topic_0221482392_p198431920144010"></a><a name="zh-cn_topic_0221482392_p198431920144010"></a>next</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482392_p108438207402"><a name="zh-cn_topic_0221482392_p108438207402"></a><a name="zh-cn_topic_0221482392_p108438207402"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482392_p28445200400"><a name="zh-cn_topic_0221482392_p28445200400"></a><a name="zh-cn_topic_0221482392_p28445200400"></a>后一邻接资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482392_section14844192018405"></a>

```
GET https://iam.myhuaweicloud.com/v3/users/{user_id}/projects
```

## 响应示例<a name="zh-cn_topic_0221482392_section118471920104012"></a>

**状态码为 200 时:**

请求成功。

```
{
    "projects": [
        {
            "domain_id": "d78cbac186b744899480f25bd02...",
            "is_domain": false,
            "parent_id": "d78cbac186b744899480f25bd0...",
            "name": "cn-southwest-2",
            "description": "",
            "links": {
                "next": null,
                "previous": null,
                "self": "https://iam.huaweicloud.com/v3/projects/06f1cd8ea9800ff02f26c003d93..."
            },
            "id": "06f1cd8ea9800ff02f26c003d93...",
            "enabled": true
        },
        {
            "domain_id": "d78cbac186b744899480f25bd02...",
            "is_domain": false,
            "parent_id": "d78cbac186b744899480f25bd0...",
            "name": "MOS",
            "description": "",
            "links": {
                "next": null,
                "previous": null,
                "self": "https://iam.huaweicloud.com/v3/projects/babf0605d15b4f9fbcacc6a8ee0f8d84"
            },
            "id": "babf0605d15b4f9fbcacc6a8ee0f8d84",
            "enabled": true
        }
    ],
    "links": {
        "next": null,
        "previous": null,
        "self": "https://iam.huaweicloud.com/v3/users/7116d09f88fa41908676fdd4b039e95b/projects"
    }
}
```

## 返回值<a name="zh-cn_topic_0221482392_section986342074014"></a>

<a name="zh-cn_topic_0221482392_table2437"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482392_row1864132084019"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482392_p188641320204019"><a name="zh-cn_topic_0221482392_p188641320204019"></a><a name="zh-cn_topic_0221482392_p188641320204019"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482392_p17865720194015"><a name="zh-cn_topic_0221482392_p17865720194015"></a><a name="zh-cn_topic_0221482392_p17865720194015"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482392_row14864172014014"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482392_p128651320184019"><a name="zh-cn_topic_0221482392_p128651320184019"></a><a name="zh-cn_topic_0221482392_p128651320184019"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482392_p386615201406"><a name="zh-cn_topic_0221482392_p386615201406"></a><a name="zh-cn_topic_0221482392_p386615201406"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row1386417201404"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482392_p886752014011"><a name="zh-cn_topic_0221482392_p886752014011"></a><a name="zh-cn_topic_0221482392_p886752014011"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482392_p0867122024011"><a name="zh-cn_topic_0221482392_p0867122024011"></a><a name="zh-cn_topic_0221482392_p0867122024011"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row1286482094011"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482392_p158685203400"><a name="zh-cn_topic_0221482392_p158685203400"></a><a name="zh-cn_topic_0221482392_p158685203400"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482392_p986862064010"><a name="zh-cn_topic_0221482392_p986862064010"></a><a name="zh-cn_topic_0221482392_p986862064010"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row1086414204406"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482392_p1286922012408"><a name="zh-cn_topic_0221482392_p1286922012408"></a><a name="zh-cn_topic_0221482392_p1286922012408"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482392_p17869112012404"><a name="zh-cn_topic_0221482392_p17869112012404"></a><a name="zh-cn_topic_0221482392_p17869112012404"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row1886472044010"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482392_p787012209407"><a name="zh-cn_topic_0221482392_p787012209407"></a><a name="zh-cn_topic_0221482392_p787012209407"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482392_p178706202402"><a name="zh-cn_topic_0221482392_p178706202402"></a><a name="zh-cn_topic_0221482392_p178706202402"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row118641420134012"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482392_p18871102019406"><a name="zh-cn_topic_0221482392_p18871102019406"></a><a name="zh-cn_topic_0221482392_p18871102019406"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482392_p2871122094019"><a name="zh-cn_topic_0221482392_p2871122094019"></a><a name="zh-cn_topic_0221482392_p2871122094019"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row13864142094017"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482392_p10872020114012"><a name="zh-cn_topic_0221482392_p10872020114012"></a><a name="zh-cn_topic_0221482392_p10872020114012"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482392_p13874620164018"><a name="zh-cn_topic_0221482392_p13874620164018"></a><a name="zh-cn_topic_0221482392_p13874620164018"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row68646208404"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482392_p9874920104014"><a name="zh-cn_topic_0221482392_p9874920104014"></a><a name="zh-cn_topic_0221482392_p9874920104014"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482392_p2087592044020"><a name="zh-cn_topic_0221482392_p2087592044020"></a><a name="zh-cn_topic_0221482392_p2087592044020"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482392_row15864102013408"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482392_p187582016407"><a name="zh-cn_topic_0221482392_p187582016407"></a><a name="zh-cn_topic_0221482392_p187582016407"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482392_p787682064015"><a name="zh-cn_topic_0221482392_p787682064015"></a><a name="zh-cn_topic_0221482392_p787682064015"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482392_section58761820184012"></a>

无

