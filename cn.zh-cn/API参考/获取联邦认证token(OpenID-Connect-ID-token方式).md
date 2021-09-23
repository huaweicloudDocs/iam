# 获取联邦认证token\(OpenID Connect ID token方式\)<a name="iam_13_0605"></a>

## 功能介绍<a name="section2362256104318"></a>

该接口可以用于通过OpenID Connect ID token方式获取联邦认证token。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section8881038191618"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=CreateTokenWithIdToken)中调试该接口。

## URI<a name="section8363155664310"></a>

POST /v3.0/OS-AUTH/id-token/tokens

## 请求参数<a name="section1936317562438"></a>

**表 1**  请求Header参数

<a name="table183641556104314"></a>
<table><thead align="left"><tr id="row855013565432"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p955175618433"><a name="p955175618433"></a><a name="p955175618433"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p15551256114317"><a name="p15551256114317"></a><a name="p15551256114317"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p955125614434"><a name="p955125614434"></a><a name="p955125614434"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p655119562433"><a name="p655119562433"></a><a name="p655119562433"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row05511156124320"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p85511356134310"><a name="p85511356134310"></a><a name="p85511356134310"></a>X-Idp-Id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p5551856154312"><a name="p5551856154312"></a><a name="p5551856154312"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p5551195634311"><a name="p5551195634311"></a><a name="p5551195634311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p115517565437"><a name="p115517565437"></a><a name="p115517565437"></a>身份提供商ID。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  请求Body参数

<a name="table10368155610434"></a>
<table><thead align="left"><tr id="row1655105664315"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p155511756164315"><a name="p155511756164315"></a><a name="p155511756164315"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p555135674319"><a name="p555135674319"></a><a name="p555135674319"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1455125611437"><a name="p1455125611437"></a><a name="p1455125611437"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p355125654316"><a name="p355125654316"></a><a name="p355125654316"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row3551356194314"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p14551125644319"><a name="p14551125644319"></a><a name="p14551125644319"></a><a href="#table2037015569431">auth</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p655185610430"><a name="p655185610430"></a><a name="p655185610430"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1155115674318"><a name="p1155115674318"></a><a name="p1155115674318"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p165511356164320"><a name="p165511356164320"></a><a name="p165511356164320"></a>请求auth参数详情。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  GetIdTokenAuthParams

<a name="table2037015569431"></a>
<table><thead align="left"><tr id="row75516566439"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p35519563439"><a name="p35519563439"></a><a name="p35519563439"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.01%" id="mcps1.2.5.1.2"><p id="p255117563431"><a name="p255117563431"></a><a name="p255117563431"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.99%" id="mcps1.2.5.1.3"><p id="p6551856184315"><a name="p6551856184315"></a><a name="p6551856184315"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p1455115654317"><a name="p1455115654317"></a><a name="p1455115654317"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row955165664316"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1755116563438"><a name="p1755116563438"></a><a name="p1755116563438"></a><a href="#table18374185617432">id_token</a></p>
</td>
<td class="cellrowborder" valign="top" width="10.01%" headers="mcps1.2.5.1.2 "><p id="p2551165613430"><a name="p2551165613430"></a><a name="p2551165613430"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.5.1.3 "><p id="p8551456144318"><a name="p8551456144318"></a><a name="p8551456144318"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p15551556204310"><a name="p15551556204310"></a><a name="p15551556204310"></a>请求id token参数详情。</p>
</td>
</tr>
<tr id="row2551856104311"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p20551456184316"><a name="p20551456184316"></a><a name="p20551456184316"></a><a href="#table203761056124311">scope</a></p>
</td>
<td class="cellrowborder" valign="top" width="10.01%" headers="mcps1.2.5.1.2 "><p id="p1055185674317"><a name="p1055185674317"></a><a name="p1055185674317"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.2.5.1.3 "><p id="p955110568432"><a name="p955110568432"></a><a name="p955110568432"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p6551195694318"><a name="p6551195694318"></a><a name="p6551195694318"></a>请求scope参数详情，限制获取token的权限范围。不传此字段，获取unscoped toke。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  GetIdTokenIdTokenBody

<a name="table18374185617432"></a>
<table><thead align="left"><tr id="row955165614313"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p1755165615433"><a name="p1755165615433"></a><a name="p1755165615433"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p12551205617435"><a name="p12551205617435"></a><a name="p12551205617435"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p755113564438"><a name="p755113564438"></a><a name="p755113564438"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p2551165674311"><a name="p2551165674311"></a><a name="p2551165674311"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row19551056154316"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p18551165619433"><a name="p18551165619433"></a><a name="p18551165619433"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p755135613435"><a name="p755135613435"></a><a name="p755135613435"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p355115568430"><a name="p355115568430"></a><a name="p355115568430"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p95511567434"><a name="p95511567434"></a><a name="p95511567434"></a>id_token的值。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  GetIdTokenIdScopeBody

<a name="table203761056124311"></a>
<table><thead align="left"><tr id="row9551656144316"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p255110568434"><a name="p255110568434"></a><a name="p255110568434"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p7551115664319"><a name="p7551115664319"></a><a name="p7551115664319"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1855125604313"><a name="p1855125604313"></a><a name="p1855125604313"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p455111563435"><a name="p455111563435"></a><a name="p455111563435"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row255115664320"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p105511056154311"><a name="p105511056154311"></a><a name="p105511056154311"></a><a href="#table1379356134320">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p1255111564431"><a name="p1255111564431"></a><a name="p1255111564431"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1955145615431"><a name="p1955145615431"></a><a name="p1955145615431"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p13551115654319"><a name="p13551115654319"></a><a name="p13551115654319"></a>domain scope详情，与project二选一。</p>
</td>
</tr>
<tr id="row11551115612433"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1551156154313"><a name="p1551156154313"></a><a name="p1551156154313"></a><a href="#table1379356134320">project</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p20551256124316"><a name="p20551256124316"></a><a name="p20551256124316"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p135511456164315"><a name="p135511456164315"></a><a name="p135511456164315"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p11551135614314"><a name="p11551135614314"></a><a name="p11551135614314"></a>project scope详情，与domain二选一。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  GetIdTokenScopeDomainOrProjectBody

<a name="table1379356134320"></a>
<table><thead align="left"><tr id="row45518569433"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p1455175614317"><a name="p1455175614317"></a><a name="p1455175614317"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p1055155616433"><a name="p1055155616433"></a><a name="p1055155616433"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p155105613438"><a name="p155105613438"></a><a name="p155105613438"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p1055225604320"><a name="p1055225604320"></a><a name="p1055225604320"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1655225674318"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p15521156174311"><a name="p15521156174311"></a><a name="p15521156174311"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p19552175613433"><a name="p19552175613433"></a><a name="p19552175613433"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p135521556124312"><a name="p135521556124312"></a><a name="p135521556124312"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p75521056104312"><a name="p75521056104312"></a><a name="p75521056104312"></a>domain id 或者 project id，与name字段至少存在一个。</p>
</td>
</tr>
<tr id="row12552256164314"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1155213561436"><a name="p1155213561436"></a><a name="p1155213561436"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p2552105610433"><a name="p2552105610433"></a><a name="p2552105610433"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p255245644311"><a name="p255245644311"></a><a name="p255245644311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p195521956154312"><a name="p195521956154312"></a><a name="p195521956154312"></a>domain name 或者 project name，与id字段至少存在一个。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section1438335617433"></a>

**状态码为 201 时:**

**表 7**  响应Header参数

<a name="table1338435654314"></a>
<table><thead align="left"><tr id="row1455245614316"><th class="cellrowborder" valign="top" width="19.81%" id="mcps1.2.4.1.1"><p id="p855275654312"><a name="p855275654312"></a><a name="p855275654312"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="30.19%" id="mcps1.2.4.1.2"><p id="p055245644313"><a name="p055245644313"></a><a name="p055245644313"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="p1555255694315"><a name="p1555255694315"></a><a name="p1555255694315"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row165527561434"><td class="cellrowborder" valign="top" width="19.81%" headers="mcps1.2.4.1.1 "><p id="p1555235604310"><a name="p1555235604310"></a><a name="p1555235604310"></a>X-Subject-Token</p>
</td>
<td class="cellrowborder" valign="top" width="30.19%" headers="mcps1.2.4.1.2 "><p id="p65521556184313"><a name="p65521556184313"></a><a name="p65521556184313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="p17552656124313"><a name="p17552656124313"></a><a name="p17552656124313"></a>签名后的Token。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  响应Body参数

<a name="table138695604315"></a>
<table><thead align="left"><tr id="row1455218569433"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p65526561436"><a name="p65526561436"></a><a name="p65526561436"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p75522566434"><a name="p75522566434"></a><a name="p75522566434"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p11552195619439"><a name="p11552195619439"></a><a name="p11552195619439"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row14552756204312"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p13552756174316"><a name="p13552756174316"></a><a name="p13552756174316"></a><a href="#table103881956114312">token</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p175523565439"><a name="p175523565439"></a><a name="p175523565439"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p9552156134310"><a name="p9552156134310"></a><a name="p9552156134310"></a>获取的token详情。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  ScopedTokenInfo

<a name="table103881956114312"></a>
<table><thead align="left"><tr id="row185527563436"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p6552145614315"><a name="p6552145614315"></a><a name="p6552145614315"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p13552125624315"><a name="p13552125624315"></a><a name="p13552125624315"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p13552155616433"><a name="p13552155616433"></a><a name="p13552155616433"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row20552175610434"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p11552135619432"><a name="p11552135619432"></a><a name="p11552135619432"></a>expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p855225615430"><a name="p855225615430"></a><a name="p855225615430"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1455218563434"><a name="p1455218563434"></a><a name="p1455218563434"></a>过期时间。</p>
</td>
</tr>
<tr id="row355217567436"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p17552185674313"><a name="p17552185674313"></a><a name="p17552185674313"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p955245624311"><a name="p955245624311"></a><a name="p955245624311"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p18552456114314"><a name="p18552456114314"></a><a name="p18552456114314"></a>获取token的方式，联邦用户默认为mapped。</p>
</td>
</tr>
<tr id="row145521556184318"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p8552356134316"><a name="p8552356134316"></a><a name="p8552356134316"></a>issued_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1455217568432"><a name="p1455217568432"></a><a name="p1455217568432"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p65526561433"><a name="p65526561433"></a><a name="p65526561433"></a>生成时间。</p>
</td>
</tr>
<tr id="row17552356144318"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p155521656104316"><a name="p155521656104316"></a><a name="p155521656104316"></a><a href="#table63957566436">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p846119513483"><a name="p846119513483"></a><a name="p846119513483"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p10552456154313"><a name="p10552456154313"></a><a name="p10552456154313"></a>用户详情。</p>
</td>
</tr>
<tr id="row1055285624312"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p8552556174313"><a name="p8552556174313"></a><a name="p8552556174313"></a><a href="#table104051456104311">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p2461451134813"><a name="p2461451134813"></a><a name="p2461451134813"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p555215619437"><a name="p555215619437"></a><a name="p555215619437"></a>租户详情。</p>
</td>
</tr>
<tr id="row4552175674315"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p5552956134317"><a name="p5552956134317"></a><a name="p5552956134317"></a><a href="#table18407115614438">project</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p15462051154814"><a name="p15462051154814"></a><a name="p15462051154814"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1655245616437"><a name="p1655245616437"></a><a name="p1655245616437"></a>项目详情。</p>
</td>
</tr>
<tr id="row19552756134310"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p255265620438"><a name="p255265620438"></a><a name="p255265620438"></a><a href="#table58096291249">roles</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p12462351134815"><a name="p12462351134815"></a><a name="p12462351134815"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1955255664314"><a name="p1955255664314"></a><a name="p1955255664314"></a>角色/策略详情。</p>
</td>
</tr>
<tr id="row1855225664314"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p6552135614437"><a name="p6552135614437"></a><a name="p6552135614437"></a><a href="#table14410115674311">catalog</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p18463145111488"><a name="p18463145111488"></a><a name="p18463145111488"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p7552115644313"><a name="p7552115644313"></a><a name="p7552115644313"></a>catalog详情。</p>
</td>
</tr>
</tbody>
</table>

**表 10**  FederationUserBody

<a name="table63957566436"></a>
<table><thead align="left"><tr id="row1655295654312"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p655217567435"><a name="p655217567435"></a><a name="p655217567435"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p11552145610431"><a name="p11552145610431"></a><a name="p11552145610431"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p14552105624314"><a name="p14552105624314"></a><a name="p14552105624314"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1455275617431"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p12552156134314"><a name="p12552156134314"></a><a name="p12552156134314"></a><a href="#table1739620561434">OS-FEDERATION</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1955216569437"><a name="p1955216569437"></a><a name="p1955216569437"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p65523566431"><a name="p65523566431"></a><a name="p65523566431"></a>联邦用户user详情。</p>
</td>
</tr>
<tr id="row10214184731711"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1465165134811"><a name="p1465165134811"></a><a name="p1465165134811"></a><a href="#table143381947129">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p646535134817"><a name="p646535134817"></a><a name="p646535134817"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p546535114816"><a name="p546535114816"></a><a name="p546535114816"></a>租户详情。</p>
</td>
</tr>
<tr id="row61581751181716"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p184651451134818"><a name="p184651451134818"></a><a name="p184651451134818"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p144651651124814"><a name="p144651651124814"></a><a name="p144651651124814"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1846505114811"><a name="p1846505114811"></a><a name="p1846505114811"></a>用户id。</p>
</td>
</tr>
<tr id="row1158195131714"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p194661451104816"><a name="p194661451104816"></a><a name="p194661451104816"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p646605110484"><a name="p646605110484"></a><a name="p646605110484"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p194667511488"><a name="p194667511488"></a><a name="p194667511488"></a>用户名。</p>
</td>
</tr>
</tbody>
</table>

**表 11**  OSFederationInfo

<a name="table1739620561434"></a>
<table><thead align="left"><tr id="row2553156104311"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p16553115614316"><a name="p16553115614316"></a><a name="p16553115614316"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p85531956174312"><a name="p85531956174312"></a><a name="p85531956174312"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p05531956134310"><a name="p05531956134310"></a><a name="p05531956134310"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row19553356184319"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p855315569432"><a name="p855315569432"></a><a name="p855315569432"></a><a href="#table1401155654314">identity_provider</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1955316561431"><a name="p1955316561431"></a><a name="p1955316561431"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p155531656144319"><a name="p155531656144319"></a><a name="p155531656144319"></a>身份提供商详情。</p>
</td>
</tr>
<tr id="row5553165684312"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p15553135619430"><a name="p15553135619430"></a><a name="p15553135619430"></a><a href="#table1440310561432">protocol</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1955375654313"><a name="p1955375654313"></a><a name="p1955375654313"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p7553155618434"><a name="p7553155618434"></a><a name="p7553155618434"></a>协议详情。</p>
</td>
</tr>
<tr id="row755325617433"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p7553145694310"><a name="p7553145694310"></a><a name="p7553145694310"></a><a href="#table19591527161315">groups</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p85794401407"><a name="p85794401407"></a><a name="p85794401407"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p7553115664314"><a name="p7553115664314"></a><a name="p7553115664314"></a>用户组详情。</p>
</td>
</tr>
</tbody>
</table>

**表 12**  IdpIdInfo

<a name="table1401155654314"></a>
<table><thead align="left"><tr id="row855395634311"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p05531456134314"><a name="p05531456134314"></a><a name="p05531456134314"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p755375613433"><a name="p755375613433"></a><a name="p755375613433"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p16553145611431"><a name="p16553145611431"></a><a name="p16553145611431"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row5553155604311"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1855385674312"><a name="p1855385674312"></a><a name="p1855385674312"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p5553185613437"><a name="p5553185613437"></a><a name="p5553185613437"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p135531956134315"><a name="p135531956134315"></a><a name="p135531956134315"></a>身份提供商id。</p>
</td>
</tr>
</tbody>
</table>

**表 13**  ProtocolIdInfo

<a name="table1440310561432"></a>
<table><thead align="left"><tr id="row55531756154317"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p45532056164319"><a name="p45532056164319"></a><a name="p45532056164319"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p755385620433"><a name="p755385620433"></a><a name="p755385620433"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p20553125617439"><a name="p20553125617439"></a><a name="p20553125617439"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row11553356144315"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p95531156134314"><a name="p95531156134314"></a><a name="p95531156134314"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1155385664316"><a name="p1155385664316"></a><a name="p1155385664316"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p255345654311"><a name="p255345654311"></a><a name="p255345654311"></a>协议id。</p>
</td>
</tr>
</tbody>
</table>

**表 14**  token.user.OS-FEDERATION.groups

<a name="table19591527161315"></a>
<table><thead align="left"><tr id="row96052781318"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p160727191316"><a name="p160727191316"></a><a name="p160727191316"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p36032731318"><a name="p36032731318"></a><a name="p36032731318"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p76062771318"><a name="p76062771318"></a><a name="p76062771318"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row26019273134"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p56072761313"><a name="p56072761313"></a><a name="p56072761313"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p360202712139"><a name="p360202712139"></a><a name="p360202712139"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p760627201315"><a name="p760627201315"></a><a name="p760627201315"></a>用户组id。</p>
</td>
</tr>
<tr id="row36072719137"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p3602279131"><a name="p3602279131"></a><a name="p3602279131"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p660102711139"><a name="p660102711139"></a><a name="p660102711139"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p9601327191312"><a name="p9601327191312"></a><a name="p9601327191312"></a>用户组名。</p>
</td>
</tr>
</tbody>
</table>

**表 15**  token.user.domain

<a name="table143381947129"></a>
<table><thead align="left"><tr id="row173380441220"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p13381421215"><a name="p13381421215"></a><a name="p13381421215"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p2338134151210"><a name="p2338134151210"></a><a name="p2338134151210"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1333814131213"><a name="p1333814131213"></a><a name="p1333814131213"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row203381343122"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p143384418125"><a name="p143384418125"></a><a name="p143384418125"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p20338114131214"><a name="p20338114131214"></a><a name="p20338114131214"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p153381544127"><a name="p153381544127"></a><a name="p153381544127"></a>租户id。</p>
</td>
</tr>
<tr id="row533824131217"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p03381411219"><a name="p03381411219"></a><a name="p03381411219"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p133816411216"><a name="p133816411216"></a><a name="p133816411216"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p73386451218"><a name="p73386451218"></a><a name="p73386451218"></a>租户名。</p>
</td>
</tr>
</tbody>
</table>

**表 16**  DomainInfo

<a name="table104051456104311"></a>
<table><thead align="left"><tr id="row20553105620437"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p155531956154316"><a name="p155531956154316"></a><a name="p155531956154316"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p1755395619437"><a name="p1755395619437"></a><a name="p1755395619437"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1555365644315"><a name="p1555365644315"></a><a name="p1555365644315"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row175536561434"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1955355614433"><a name="p1955355614433"></a><a name="p1955355614433"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p9553356144313"><a name="p9553356144313"></a><a name="p9553356144313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p555325624311"><a name="p555325624311"></a><a name="p555325624311"></a>租户id。</p>
</td>
</tr>
<tr id="row195531356144311"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1755335610433"><a name="p1755335610433"></a><a name="p1755335610433"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p3553115618430"><a name="p3553115618430"></a><a name="p3553115618430"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p20553105614433"><a name="p20553105614433"></a><a name="p20553105614433"></a>租户名。</p>
</td>
</tr>
</tbody>
</table>

**表 17**  ProjectInfo

<a name="table18407115614438"></a>
<table><thead align="left"><tr id="row155531756124315"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p1055355664313"><a name="p1055355664313"></a><a name="p1055355664313"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p1055375619435"><a name="p1055375619435"></a><a name="p1055375619435"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p7553165634314"><a name="p7553165634314"></a><a name="p7553165634314"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row115531356114311"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p14553165634312"><a name="p14553165634312"></a><a name="p14553165634312"></a><a href="#table1157911019217">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p125531656154317"><a name="p125531656154317"></a><a name="p125531656154317"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p15553556164319"><a name="p15553556164319"></a><a name="p15553556164319"></a>租户详情。</p>
</td>
</tr>
<tr id="row1855312563430"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p17553165614434"><a name="p17553165614434"></a><a name="p17553165614434"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p155325654317"><a name="p155325654317"></a><a name="p155325654317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p7553115674313"><a name="p7553115674313"></a><a name="p7553115674313"></a>项目id。</p>
</td>
</tr>
<tr id="row7553165610438"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p14553175684312"><a name="p14553175684312"></a><a name="p14553175684312"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p25531056104312"><a name="p25531056104312"></a><a name="p25531056104312"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p175531556104317"><a name="p175531556104317"></a><a name="p175531556104317"></a>项目名。</p>
</td>
</tr>
</tbody>
</table>

**表 18**  token.project.domain

<a name="table1157911019217"></a>
<table><thead align="left"><tr id="row1257950192112"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p4579160182119"><a name="p4579160182119"></a><a name="p4579160182119"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p18579120162112"><a name="p18579120162112"></a><a name="p18579120162112"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1957960152113"><a name="p1957960152113"></a><a name="p1957960152113"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row957915082119"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1857919014219"><a name="p1857919014219"></a><a name="p1857919014219"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1457912072118"><a name="p1457912072118"></a><a name="p1457912072118"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p557940122115"><a name="p557940122115"></a><a name="p557940122115"></a>租户id。</p>
</td>
</tr>
<tr id="row1257911082118"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1657960102111"><a name="p1657960102111"></a><a name="p1657960102111"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p17579808216"><a name="p17579808216"></a><a name="p17579808216"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1457900152113"><a name="p1457900152113"></a><a name="p1457900152113"></a>租户名。</p>
</td>
</tr>
</tbody>
</table>

**表 19**  roles

<a name="table58096291249"></a>
<table><thead align="left"><tr id="row1280952915247"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p17809192913245"><a name="p17809192913245"></a><a name="p17809192913245"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p1380920298245"><a name="p1380920298245"></a><a name="p1380920298245"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p8809229112419"><a name="p8809229112419"></a><a name="p8809229112419"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row280915299249"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p2810162932414"><a name="p2810162932414"></a><a name="p2810162932414"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p188105292245"><a name="p188105292245"></a><a name="p188105292245"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p8810172918244"><a name="p8810172918244"></a><a name="p8810172918244"></a>权限id。</p>
</td>
</tr>
<tr id="row8810629192417"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p3810829132418"><a name="p3810829132418"></a><a name="p3810829132418"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p681032912249"><a name="p681032912249"></a><a name="p681032912249"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p11810112920243"><a name="p11810112920243"></a><a name="p11810112920243"></a>权限名。</p>
</td>
</tr>
</tbody>
</table>

**表 20**  CatalogInfo

<a name="table14410115674311"></a>
<table><thead align="left"><tr id="row255305674311"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p1155405624310"><a name="p1155405624310"></a><a name="p1155405624310"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p255495610439"><a name="p255495610439"></a><a name="p255495610439"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p55541656114316"><a name="p55541656114316"></a><a name="p55541656114316"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row455419560430"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p105541856164310"><a name="p105541856164310"></a><a name="p105541856164310"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p10554165617438"><a name="p10554165617438"></a><a name="p10554165617438"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p10554175614314"><a name="p10554175614314"></a><a name="p10554175614314"></a>终端节点ID。</p>
</td>
</tr>
<tr id="row5554165644320"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p3554115612438"><a name="p3554115612438"></a><a name="p3554115612438"></a>interface</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1455412563434"><a name="p1455412563434"></a><a name="p1455412563434"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p655420567435"><a name="p655420567435"></a><a name="p655420567435"></a>接口类型，描述接口在该终端节点的可见性。值为“public”，表示该接口为公开接口。</p>
</td>
</tr>
<tr id="row355413569433"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p14554125611438"><a name="p14554125611438"></a><a name="p14554125611438"></a>region</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p195541456124314"><a name="p195541456124314"></a><a name="p195541456124314"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p95541256154313"><a name="p95541256154313"></a><a name="p95541256154313"></a>终端节点所属区域。</p>
</td>
</tr>
<tr id="row1655445610430"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1455475624318"><a name="p1455475624318"></a><a name="p1455475624318"></a>region_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1155418562431"><a name="p1155418562431"></a><a name="p1155418562431"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p16554556174313"><a name="p16554556174313"></a><a name="p16554556174313"></a>终端节点所属区域ID。</p>
</td>
</tr>
<tr id="row2055425634315"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p19554205684313"><a name="p19554205684313"></a><a name="p19554205684313"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p3554135617438"><a name="p3554135617438"></a><a name="p3554135617438"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1555125611439"><a name="p1555125611439"></a><a name="p1555125611439"></a>终端节点的URL。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section2414185619435"></a>

-   获取联邦认证project scoped token

    ```
    POST /v3.0/OS-AUTH/id-token/tokens 
      
     { 
       "auth" : { 
         "id_token" : { 
           "id" : "eyJhbGciOiJSU..." 
         }, 
         "scope" : { 
           "project" : { 
             "id" : "46419baef4324...", 
             "name" : "cn-north-4" 
           } 
         } 
       } 
     }
    ```

-   获取联邦认证domain scoped token

    ```
    POST /v3.0/OS-AUTH/id-token/tokens 
      
     { 
       "auth" : { 
         "id_token" : { 
           "id" : "eyJhbGciOiJSU..." 
         }, 
         "scope" : { 
           "domain" : { 
             "id" : "063bb260a480...", 
             "name" : "IAMDomain" 
           } 
         } 
       } 
     }
    ```

-   获取unscoped token

    ```
    POST /v3.0/OS-AUTH/id-token/tokens 
      
     { 
       "auth" : { 
         "id_token" : { 
           "id" : "eyJhbGciOiJSU..." 
         } 
       } 
     }
    ```


## 响应示例<a name="section144171756164316"></a>

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
  "error_msg" : "Request body is invalid.", 
  "error_code" : "IAM.0011" 
}
```

**状态码为 401 时:**

认证失败。

```
{ 
  "error_msg" : "The request you have made requires authentication.", 
  "error_code" : "IAM.0001" 
}
```

**状态码为 403 时:**

没有操作权限。

```
{ 
  "error_msg" : "Policy doesn't allow %(actions)s to be performed.", 
  "error_code" : "IAM.0003" 
}
```

**状态码为 404 时:**

未找到相应的资源。

```
{ 
  "error_msg" : "Could not find %(target)s: %(target_id)s.", 
  "error_code" : "IAM.0004" 
}
```

**状态码为 500 时:**

系统内部异常。

```
{ 
  "error_msg" : "An unexpected error prevented the server from fulfilling your request.", 
  "error_code" : "IAM.0006" 
}
```

## 状态码<a name="section5422195614432"></a>

<a name="table13422205664311"></a>
<table><thead align="left"><tr id="row9556105624310"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p145561256174317"><a name="p145561256174317"></a><a name="p145561256174317"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p655611561434"><a name="p655611561434"></a><a name="p655611561434"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1755675604312"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p10556175684313"><a name="p10556175684313"></a><a name="p10556175684313"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p355612565437"><a name="p355612565437"></a><a name="p355612565437"></a>创建成功。</p>
</td>
</tr>
<tr id="row175561256104314"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p6556175616432"><a name="p6556175616432"></a><a name="p6556175616432"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p18556175612432"><a name="p18556175612432"></a><a name="p18556175612432"></a>参数无效。</p>
</td>
</tr>
<tr id="row13556175604315"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1556656144312"><a name="p1556656144312"></a><a name="p1556656144312"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p9556175616432"><a name="p9556175616432"></a><a name="p9556175616432"></a>认证失败。</p>
</td>
</tr>
<tr id="row45561856154318"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1755610566434"><a name="p1755610566434"></a><a name="p1755610566434"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p35561156194316"><a name="p35561156194316"></a><a name="p35561156194316"></a>没有操作权限。</p>
</td>
</tr>
<tr id="row13556195615436"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1955675616433"><a name="p1955675616433"></a><a name="p1955675616433"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p1556115615439"><a name="p1556115615439"></a><a name="p1556115615439"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="row11556256104319"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1855675634313"><a name="p1855675634313"></a><a name="p1855675634313"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p17556256164313"><a name="p17556256164313"></a><a name="p17556256164313"></a>系统内部异常。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section144261156184318"></a>

请参见[错误码](错误码.md)。

