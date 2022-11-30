# 获取联邦认证unscoped token\(OpenID Connect ID token方式\)<a name="iam_13_0606"></a>

## 功能介绍<a name="section1623114500505"></a>

该接口可以用于通过OpenID Connect ID token方式获取联邦认证unscoped token。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section8881038191618"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=CreateUnscopedTokenWithIdToken)中调试该接口。

## URI<a name="section4233750175014"></a>

POST /v3/OS-FEDERATION/identity\_providers/\{idp\_id\}/protocols/\{protocol\_id\}/auth

**表 1**  路径参数

<a name="table2234195015509"></a>
<table><thead align="left"><tr id="row145125065019"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p4451850145015"><a name="p4451850145015"></a><a name="p4451850145015"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p3451195014508"><a name="p3451195014508"></a><a name="p3451195014508"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p10451195010508"><a name="p10451195010508"></a><a name="p10451195010508"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p174511250205016"><a name="p174511250205016"></a><a name="p174511250205016"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row245195020506"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p5451195013503"><a name="p5451195013503"></a><a name="p5451195013503"></a>idp_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p19451115020505"><a name="p19451115020505"></a><a name="p19451115020505"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p34511350165011"><a name="p34511350165011"></a><a name="p34511350165011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276985_p134475234912"><a name="zh-cn_topic_0224276985_p134475234912"></a><a name="zh-cn_topic_0224276985_p134475234912"></a>身份提供商名称。</p>
</td>
</tr>
<tr id="row3451185019501"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p84511350145010"><a name="p84511350145010"></a><a name="p84511350145010"></a>protocol_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p17451155075020"><a name="p17451155075020"></a><a name="p17451155075020"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1245110505500"><a name="p1245110505500"></a><a name="p1245110505500"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1845125010502"><a name="p1845125010502"></a><a name="p1845125010502"></a>协议id。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="section1924417505508"></a>

**表 2**  请求Header参数

<a name="table62449504503"></a>
<table><thead align="left"><tr id="row11451165065017"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p14451105019503"><a name="p14451105019503"></a><a name="p14451105019503"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p114516502506"><a name="p114516502506"></a><a name="p114516502506"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p124511150135012"><a name="p124511150135012"></a><a name="p124511150135012"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p145175065017"><a name="p145175065017"></a><a name="p145175065017"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1645145014507"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p14451750105010"><a name="p14451750105010"></a><a name="p14451750105010"></a>Authorization</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p145165018502"><a name="p145165018502"></a><a name="p145165018502"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1745145018502"><a name="p1745145018502"></a><a name="p1745145018502"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p7451145065011"><a name="p7451145065011"></a><a name="p7451145065011"></a>OpenID Connect身份提供商的ID Token，格式为Bearer {ID Token}。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section6250450135016"></a>

**状态码为 201 时:**

**表 3**  响应Header参数

<a name="table1425216502504"></a>
<table><thead align="left"><tr id="row64511750165011"><th class="cellrowborder" valign="top" width="19.6%" id="mcps1.2.4.1.1"><p id="p1451195018509"><a name="p1451195018509"></a><a name="p1451195018509"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.44%" id="mcps1.2.4.1.2"><p id="p345195013500"><a name="p345195013500"></a><a name="p345195013500"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="59.96%" id="mcps1.2.4.1.3"><p id="p124511505504"><a name="p124511505504"></a><a name="p124511505504"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row445165011503"><td class="cellrowborder" valign="top" width="19.6%" headers="mcps1.2.4.1.1 "><p id="p1545185015012"><a name="p1545185015012"></a><a name="p1545185015012"></a>X-Subject-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20.44%" headers="mcps1.2.4.1.2 "><p id="p8451175018505"><a name="p8451175018505"></a><a name="p8451175018505"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="59.96%" headers="mcps1.2.4.1.3 "><p id="p4451050135017"><a name="p4451050135017"></a><a name="p4451050135017"></a>签名后的Token。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  响应Body参数

<a name="table1926113500501"></a>
<table><thead align="left"><tr id="row1845118502508"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p16451650155014"><a name="p16451650155014"></a><a name="p16451650155014"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p1245125016506"><a name="p1245125016506"></a><a name="p1245125016506"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p6451155045015"><a name="p6451155045015"></a><a name="p6451155045015"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row74511650175012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p14513509507"><a name="p14513509507"></a><a name="p14513509507"></a><a href="#table1026565014509">token</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p145175065016"><a name="p145175065016"></a><a name="p145175065016"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1745115085011"><a name="p1745115085011"></a><a name="p1745115085011"></a>获取的token详情。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  UnscopedTokenInfo

<a name="table1026565014509"></a>
<table><thead align="left"><tr id="row74517502504"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p1645145075016"><a name="p1645145075016"></a><a name="p1645145075016"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p15451185015509"><a name="p15451185015509"></a><a name="p15451185015509"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p94511509503"><a name="p94511509503"></a><a name="p94511509503"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1645115017501"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p164513505503"><a name="p164513505503"></a><a name="p164513505503"></a>expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p245205085018"><a name="p245205085018"></a><a name="p245205085018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p845219507503"><a name="p845219507503"></a><a name="p845219507503"></a>过期时间。</p>
</td>
</tr>
<tr id="row945212507502"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p045211509502"><a name="p045211509502"></a><a name="p045211509502"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p745265016506"><a name="p745265016506"></a><a name="p745265016506"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p0452145055019"><a name="p0452145055019"></a><a name="p0452145055019"></a>token获取方式，联邦认证默认为mapped。</p>
</td>
</tr>
<tr id="row7452105016509"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p0452450175013"><a name="p0452450175013"></a><a name="p0452450175013"></a>issued_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p74522050185014"><a name="p74522050185014"></a><a name="p74522050185014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p12452115018506"><a name="p12452115018506"></a><a name="p12452115018506"></a>生成时间。</p>
</td>
</tr>
<tr id="row745225016509"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p3452950185014"><a name="p3452950185014"></a><a name="p3452950185014"></a><a href="#table1727255020503">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p7452165045020"><a name="p7452165045020"></a><a name="p7452165045020"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p545211501509"><a name="p545211501509"></a><a name="p545211501509"></a>用户详情。</p>
</td>
</tr>
<tr id="row1643615323484"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p255265620438"><a name="p255265620438"></a><a name="p255265620438"></a><a href="#table13291150195018">roles</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p185521456104316"><a name="p185521456104316"></a><a name="p185521456104316"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1955255664314"><a name="p1955255664314"></a><a name="p1955255664314"></a>角色/策略详情。</p>
</td>
</tr>
<tr id="row443623211484"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p6552135614437"><a name="p6552135614437"></a><a name="p6552135614437"></a><a href="#table3886164919497">catalog</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p195526568439"><a name="p195526568439"></a><a name="p195526568439"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p7552115644313"><a name="p7552115644313"></a><a name="p7552115644313"></a>catalog详情。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  FederationUserBody

<a name="table1727255020503"></a>
<table><thead align="left"><tr id="row11452185085019"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p1745295018500"><a name="p1745295018500"></a><a name="p1745295018500"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p545235017500"><a name="p545235017500"></a><a name="p545235017500"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p945245019509"><a name="p945245019509"></a><a name="p945245019509"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row144521550155012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p94521050175011"><a name="p94521050175011"></a><a name="p94521050175011"></a><a href="#table10275125045010">OS-FEDERATION</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p18452950145019"><a name="p18452950145019"></a><a name="p18452950145019"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1545211502504"><a name="p1545211502504"></a><a name="p1545211502504"></a>联邦用户user详情。</p>
</td>
</tr>
<tr id="row1640573523614"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1465165134811"><a name="p1465165134811"></a><a name="p1465165134811"></a><a href="#table2280252184911">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p646535134817"><a name="p646535134817"></a><a name="p646535134817"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p546535114816"><a name="p546535114816"></a><a name="p546535114816"></a>租户详情。</p>
</td>
</tr>
<tr id="row172771738103618"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p184651451134818"><a name="p184651451134818"></a><a name="p184651451134818"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p144651651124814"><a name="p144651651124814"></a><a name="p144651651124814"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1846505114811"><a name="p1846505114811"></a><a name="p1846505114811"></a>用户id。</p>
</td>
</tr>
<tr id="row1527853843611"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p194661451104816"><a name="p194661451104816"></a><a name="p194661451104816"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p646605110484"><a name="p646605110484"></a><a name="p646605110484"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p194667511488"><a name="p194667511488"></a><a name="p194667511488"></a>用户名。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  OSFederationInfo

<a name="table10275125045010"></a>
<table><thead align="left"><tr id="row7452155019502"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p184521508508"><a name="p184521508508"></a><a name="p184521508508"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p19452155020509"><a name="p19452155020509"></a><a name="p19452155020509"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p184521450135019"><a name="p184521450135019"></a><a name="p184521450135019"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row64521350195018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p345275065017"><a name="p345275065017"></a><a name="p345275065017"></a><a href="#table328505075012">identity_provider</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p5452165019505"><a name="p5452165019505"></a><a name="p5452165019505"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p9452105017508"><a name="p9452105017508"></a><a name="p9452105017508"></a>身份提供商详情。</p>
</td>
</tr>
<tr id="row20452150185020"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p154526509509"><a name="p154526509509"></a><a name="p154526509509"></a><a href="#table52881350195012">protocol</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1545210500508"><a name="p1545210500508"></a><a name="p1545210500508"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p145295014502"><a name="p145295014502"></a><a name="p145295014502"></a>协议详情。</p>
</td>
</tr>
<tr id="row24521650125018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p184527505503"><a name="p184527505503"></a><a name="p184527505503"></a><a href="#table295115413111">groups</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p544619415363"><a name="p544619415363"></a><a name="p544619415363"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1045285014508"><a name="p1045285014508"></a><a name="p1045285014508"></a>用户组详情。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  IdpIdInfo

<a name="table328505075012"></a>
<table><thead align="left"><tr id="row19452650165015"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p445275016504"><a name="p445275016504"></a><a name="p445275016504"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p164521506504"><a name="p164521506504"></a><a name="p164521506504"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p34522503507"><a name="p34522503507"></a><a name="p34522503507"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row12452105020509"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p545295013505"><a name="p545295013505"></a><a name="p545295013505"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p7452165035016"><a name="p7452165035016"></a><a name="p7452165035016"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p2045285025016"><a name="p2045285025016"></a><a name="p2045285025016"></a>身份提供商id。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  ProtocolIdInfo

<a name="table52881350195012"></a>
<table><thead align="left"><tr id="row94525508505"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p2452850145014"><a name="p2452850145014"></a><a name="p2452850145014"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p10452850155018"><a name="p10452850155018"></a><a name="p10452850155018"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p34521050105017"><a name="p34521050105017"></a><a name="p34521050105017"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1452175017500"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p5452150195014"><a name="p5452150195014"></a><a name="p5452150195014"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p154521250115017"><a name="p154521250115017"></a><a name="p154521250115017"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p74522050125013"><a name="p74522050125013"></a><a name="p74522050125013"></a>协议id。</p>
</td>
</tr>
</tbody>
</table>

**表 10**  token.user.OS-FEDERATION.groups

<a name="table295115413111"></a>
<table><thead align="left"><tr id="row995115541414"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p1095120541519"><a name="p1095120541519"></a><a name="p1095120541519"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p179517541815"><a name="p179517541815"></a><a name="p179517541815"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p5951154215"><a name="p5951154215"></a><a name="p5951154215"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1295118543118"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p16655261324"><a name="p16655261324"></a><a name="p16655261324"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p156551161021"><a name="p156551161021"></a><a name="p156551161021"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p206551261529"><a name="p206551261529"></a><a name="p206551261529"></a>用户组id。</p>
</td>
</tr>
<tr id="row83669313217"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1365512617218"><a name="p1365512617218"></a><a name="p1365512617218"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p965526723"><a name="p965526723"></a><a name="p965526723"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p19655662026"><a name="p19655662026"></a><a name="p19655662026"></a>用户组名。</p>
</td>
</tr>
</tbody>
</table>

**表 11**  DomainInfo

<a name="table2280252184911"></a>
<table><thead align="left"><tr id="row14280252134915"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p1128010524498"><a name="p1128010524498"></a><a name="p1128010524498"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p17280652154911"><a name="p17280652154911"></a><a name="p17280652154911"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p7280752164918"><a name="p7280752164918"></a><a name="p7280752164918"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row82801952164914"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p16280952134915"><a name="p16280952134915"></a><a name="p16280952134915"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p72803525495"><a name="p72803525495"></a><a name="p72803525495"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p122806524494"><a name="p122806524494"></a><a name="p122806524494"></a>租户id。</p>
</td>
</tr>
<tr id="row02806529491"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p16280252124911"><a name="p16280252124911"></a><a name="p16280252124911"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p172801352164918"><a name="p172801352164918"></a><a name="p172801352164918"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p928045215495"><a name="p928045215495"></a><a name="p928045215495"></a>租户名。</p>
</td>
</tr>
</tbody>
</table>

**表 12**  token.roles

<a name="table13291150195018"></a>
<table><thead align="left"><tr id="row245215025019"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p144521550205019"><a name="p144521550205019"></a><a name="p144521550205019"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p5452105012501"><a name="p5452105012501"></a><a name="p5452105012501"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p164521750195018"><a name="p164521750195018"></a><a name="p164521750195018"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row445275095010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1845215010509"><a name="p1845215010509"></a><a name="p1845215010509"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p845265085011"><a name="p845265085011"></a><a name="p845265085011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p5452205035016"><a name="p5452205035016"></a><a name="p5452205035016"></a>权限id。</p>
</td>
</tr>
<tr id="row1945255010509"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p045265025011"><a name="p045265025011"></a><a name="p045265025011"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p194524502508"><a name="p194524502508"></a><a name="p194524502508"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p34520500509"><a name="p34520500509"></a><a name="p34520500509"></a>权限名。</p>
</td>
</tr>
</tbody>
</table>

**表 13**  token.catalog

<a name="table3886164919497"></a>
<table><thead align="left"><tr id="row78867492499"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p3886949104913"><a name="p3886949104913"></a><a name="p3886949104913"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p158861849184911"><a name="p158861849184911"></a><a name="p158861849184911"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1288619497495"><a name="p1288619497495"></a><a name="p1288619497495"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row108861149104914"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1488694913495"><a name="p1488694913495"></a><a name="p1488694913495"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p7886114916491"><a name="p7886114916491"></a><a name="p7886114916491"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p13886164910491"><a name="p13886164910491"></a><a name="p13886164910491"></a>终端节点ID。</p>
</td>
</tr>
<tr id="row288644914491"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1498017615527"><a name="p1498017615527"></a><a name="p1498017615527"></a>interface</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p186420653718"><a name="p186420653718"></a><a name="p186420653718"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1198015615522"><a name="p1198015615522"></a><a name="p1198015615522"></a>接口类型,描述接口在该终端节点的可见性。值为“public”,表示该接口为公开接口。</p>
</td>
</tr>
<tr id="row564223417505"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p179801562528"><a name="p179801562528"></a><a name="p179801562528"></a>region</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p37211603712"><a name="p37211603712"></a><a name="p37211603712"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p199808655210"><a name="p199808655210"></a><a name="p199808655210"></a>终端节点所属区域。</p>
</td>
</tr>
<tr id="row264323412504"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p199806618525"><a name="p199806618525"></a><a name="p199806618525"></a>region_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p16790683716"><a name="p16790683716"></a><a name="p16790683716"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p149801369527"><a name="p149801369527"></a><a name="p149801369527"></a>终端节点所属区域ID。</p>
</td>
</tr>
<tr id="row564343414504"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p89802615525"><a name="p89802615525"></a><a name="p89802615525"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1285465372"><a name="p1285465372"></a><a name="p1285465372"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p6980461524"><a name="p6980461524"></a><a name="p6980461524"></a>终端节点的URL。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section1129765025015"></a>

```
POST https://{address}/v3/OS-FEDERATION/identity_providers/{idp_id}/protocols/{protocol_id}/auth
```

## 响应示例<a name="section529805017508"></a>

**状态码为 201 时:**

创建成功。

```
{ 
  "token" : { 
    "expires_at" : "2018-03-13T03:00:01.168000Z", 
    "methods" : [ "mapped" ], 
    "issued_at" : "2018-03-12T03:00:01.168000Z", 
    "user" : { 
      "OS-FEDERATION" : { 
        "identity_provider" : { 
          "id" : "idptest" 
        }, 
        "protocol" : { 
          "id" : "oidc" 
        }, 
        "groups" : [ { 
          "name" : "admin", 
          "id" : "45a8c8f..." 
        } ] 
      }, 
      "domain" : { 
        "id" : "063bb260a480...", 
        "name" : "IAMDomain" 
      }, 
      "name" : "FederationUser", 
      "id" : "suvmgvUZc4PaCOEc..." 
    } 
  } 
}
```

**状态码为 400 时:**

参数无效。

```
{ 
  "error" : { 
    "code" : 400, 
    "message" : "Request parameter 'idp id' is invalid.", 
    "title" : "Bad Request" 
  } 
}
```

**状态码为 401 时:**

认证失败。

```
{ 
  "error" : { 
    "code" : 401, 
    "message" : "The request you have made requires authentication.", 
    "title" : "Unauthorized" 
  } 
}
```

**状态码为 403 时:**

没有操作权限。

```
{ 
  "error" : { 
    "code" : 403, 
    "message" : "You are not authorized to perform the requested action.", 
    "title" : "Forbidden" 
  } 
}
```

**状态码为 404 时:**

未找到相应资源。

```
{ 
  "error" : { 
    "code" : 404, 
    "message" : "Could not find %(target)s: %(target_id)s.", 
    "title" : "Not Found" 
  } 
}
```

**状态码为 500 时:**

系统内部异常。

```
{ 
  "error" : { 
    "code" : 500, 
    "message" : "An unexpected error prevented the server from fulfilling your request.", 
    "title" : "Internal Server Error" 
  } 
}
```

## 状态码<a name="section7334195075015"></a>

<a name="table1833419505508"></a>
<table><thead align="left"><tr id="row12453165013501"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p17453250175014"><a name="p17453250175014"></a><a name="p17453250175014"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p1445315509509"><a name="p1445315509509"></a><a name="p1445315509509"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row18453150115013"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1745335025010"><a name="p1745335025010"></a><a name="p1745335025010"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p1453205095018"><a name="p1453205095018"></a><a name="p1453205095018"></a>创建成功。</p>
</td>
</tr>
<tr id="row124531550125020"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p945315503506"><a name="p945315503506"></a><a name="p945315503506"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p4453105055012"><a name="p4453105055012"></a><a name="p4453105055012"></a>参数无效。</p>
</td>
</tr>
<tr id="row9453950145011"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p3453950105017"><a name="p3453950105017"></a><a name="p3453950105017"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p1745355017508"><a name="p1745355017508"></a><a name="p1745355017508"></a>认证失败。</p>
</td>
</tr>
<tr id="row0453175095015"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p10453195095015"><a name="p10453195095015"></a><a name="p10453195095015"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p8453550135013"><a name="p8453550135013"></a><a name="p8453550135013"></a>没有操作权限。</p>
</td>
</tr>
<tr id="row8453125045018"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p8453175014502"><a name="p8453175014502"></a><a name="p8453175014502"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p7453550205017"><a name="p7453550205017"></a><a name="p7453550205017"></a>未找到相应资源。</p>
</td>
</tr>
<tr id="row845320504503"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p645310504507"><a name="p645310504507"></a><a name="p645310504507"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p20453950145019"><a name="p20453950145019"></a><a name="p20453950145019"></a>系统内部异常。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section6341175012509"></a>

请参见[错误码](错误码.md)。

