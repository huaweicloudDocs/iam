# 修改OpenID Connect身份提供商配置<a name="iam_13_0208"></a>

## 功能介绍<a name="section8465839203813"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)  修改OpenID Connect身份提供商配置。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="section54671939193820"></a>

PUT /v3.0/OS-FEDERATION/identity-providers/\{idp\_id\}/openid-connect-config

**表 1**  路径参数

<a name="table20468123903812"></a>
<table><thead align="left"><tr id="row4617133913819"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p136172391386"><a name="p136172391386"></a><a name="p136172391386"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p1061783913380"><a name="p1061783913380"></a><a name="p1061783913380"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1361718392380"><a name="p1361718392380"></a><a name="p1361718392380"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p96171239193812"><a name="p96171239193812"></a><a name="p96171239193812"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row261793993815"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p18617439133813"><a name="p18617439133813"></a><a name="p18617439133813"></a>idp_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p861713918382"><a name="p861713918382"></a><a name="p861713918382"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1761719395389"><a name="p1761719395389"></a><a name="p1761719395389"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1161793911385"><a name="p1161793911385"></a><a name="p1161793911385"></a>身份提供商ID。</p>
<p id="p276416271028"><a name="p276416271028"></a><a name="p276416271028"></a>最小长度：1。最大长度：64。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="section1047314394387"></a>

**表 2**  请求Header参数

<a name="table947416399386"></a>
<table><thead align="left"><tr id="row16617839123820"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p186171039193819"><a name="p186171039193819"></a><a name="p186171039193819"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p56179398382"><a name="p56179398382"></a><a name="p56179398382"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1561716395387"><a name="p1561716395387"></a><a name="p1561716395387"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p15617539123815"><a name="p15617539123815"></a><a name="p15617539123815"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row14617183953814"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1761743916387"><a name="p1761743916387"></a><a name="p1761743916387"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p4617339143813"><a name="p4617339143813"></a><a name="p4617339143813"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p9617143914388"><a name="p9617143914388"></a><a name="p9617143914388"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p10617143914384"><a name="p10617143914384"></a><a name="p10617143914384"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="row17617163903810"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p961793918386"><a name="p961793918386"></a><a name="p961793918386"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p6617439183812"><a name="p6617439183812"></a><a name="p6617439183812"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p8617103916385"><a name="p8617103916385"></a><a name="p8617103916385"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p12617113918388"><a name="p12617113918388"></a><a name="p12617113918388"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="table164791339133814"></a>
<table><thead align="left"><tr id="row16617153973813"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p13617143910382"><a name="p13617143910382"></a><a name="p13617143910382"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p146171639133819"><a name="p146171639133819"></a><a name="p146171639133819"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1661712394387"><a name="p1661712394387"></a><a name="p1661712394387"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p1617039163814"><a name="p1617039163814"></a><a name="p1617039163814"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row061793933817"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p96171839153815"><a name="p96171839153815"></a><a name="p96171839153815"></a><a href="#table1648243993811">openid_connect_config</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p3617839163820"><a name="p3617839163820"></a><a name="p3617839163820"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p17617163913812"><a name="p17617163913812"></a><a name="p17617163913812"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p66172397381"><a name="p66172397381"></a><a name="p66172397381"></a>OpenID Connect配置详情。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  openid\_connect\_config

<a name="table1648243993811"></a>
<table><thead align="left"><tr id="row15617139103812"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p161753943817"><a name="p161753943817"></a><a name="p161753943817"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p11617639193818"><a name="p11617639193818"></a><a name="p11617639193818"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p17617039173816"><a name="p17617039173816"></a><a name="p17617039173816"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p96171839163812"><a name="p96171839163812"></a><a name="p96171839163812"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row161710393388"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p861773953817"><a name="p861773953817"></a><a name="p861773953817"></a>access_mode</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p106171539193811"><a name="p106171539193811"></a><a name="p106171539193811"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p861712394388"><a name="p861712394388"></a><a name="p861712394388"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p611593517328"><a name="p611593517328"></a><a name="p611593517328"></a>访问方式。</p>
<a name="ul1166237163218"></a><a name="ul1166237163218"></a><ul id="ul1166237163218"><li>program_console: 支持编程访问和管理控制台访问方式。</li><li>program: 支持编程访问方式</li></ul>
</td>
</tr>
<tr id="row10617133983819"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p16617539143815"><a name="p16617539143815"></a><a name="p16617539143815"></a>idp_url</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p861773918381"><a name="p861773918381"></a><a name="p861773918381"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p15617183916386"><a name="p15617183916386"></a><a name="p15617183916386"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1514462119318"><a name="p1514462119318"></a><a name="p1514462119318"></a>OpenID Connect身份提供商标识, 对应ID token 中 iss字段。</p>
<p id="p413564920525"><a name="p413564920525"></a><a name="p413564920525"></a>最小长度：10。最大长度：255。</p>
</td>
</tr>
<tr id="row7617839103817"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p86172397381"><a name="p86172397381"></a><a name="p86172397381"></a>client_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p161713393383"><a name="p161713393383"></a><a name="p161713393383"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p66181239113814"><a name="p66181239113814"></a><a name="p66181239113814"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p111454219316"><a name="p111454219316"></a><a name="p111454219316"></a>在OpenID Connect身份提供商注册的客户端ID。</p>
<p id="p34251044175219"><a name="p34251044175219"></a><a name="p34251044175219"></a>最小长度：5。最大长度：255。</p>
</td>
</tr>
<tr id="row136189392388"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p5618123911381"><a name="p5618123911381"></a><a name="p5618123911381"></a>authorization_endpoint</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p2618133913389"><a name="p2618133913389"></a><a name="p2618133913389"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p3618173917388"><a name="p3618173917388"></a><a name="p3618173917388"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1427416283317"><a name="p1427416283317"></a><a name="p1427416283317"></a>OpenID Connect身份提供商授权地址。</p>
<p id="p714514217312"><a name="p714514217312"></a><a name="p714514217312"></a><strong id="b1117016683311"><a name="b1117016683311"></a><a name="b1117016683311"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选</strong>。</p>
<p id="p1851121112535"><a name="p1851121112535"></a><a name="p1851121112535"></a>最小长度：10。最大长度：255。</p>
</td>
</tr>
<tr id="row861813903810"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p16618339193813"><a name="p16618339193813"></a><a name="p16618339193813"></a>scope</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p11618173903819"><a name="p11618173903819"></a><a name="p11618173903819"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p261823963817"><a name="p261823963817"></a><a name="p261823963817"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1460272123315"><a name="p1460272123315"></a><a name="p1460272123315"></a>授权请求信息范围。</p>
<p id="p217382453312"><a name="p217382453312"></a><a name="p217382453312"></a><strong id="b0654172615333"><a name="b0654172615333"></a><a name="b0654172615333"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选。</strong></p>
<p id="p137881118173510"><a name="p137881118173510"></a><a name="p137881118173510"></a>枚举值：</p>
<a name="ul182672313510"></a><a name="ul182672313510"></a><ul id="ul182672313510"><li>openid</li><li>email</li><li>profile<div class="note" id="note78171434125310"><a name="note78171434125310"></a><a name="note78171434125310"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul940272714014"></a><a name="ul940272714014"></a><ul id="ul940272714014"><li>此字段必选值“openid”。</li><li>最少1个值，最多10个值，之间使用空格分割。</li></ul>
<p id="p457525410018"><a name="p457525410018"></a><a name="p457525410018"></a>例如： "openid" 、"openid email"、 "openid profile"、 "openid email profile"。</p>
</div></div>
</li></ul>
</td>
</tr>
<tr id="row761814395384"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p9618133913383"><a name="p9618133913383"></a><a name="p9618133913383"></a>response_type</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p166181439113813"><a name="p166181439113813"></a><a name="p166181439113813"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1861893911384"><a name="p1861893911384"></a><a name="p1861893911384"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1841811576348"><a name="p1841811576348"></a><a name="p1841811576348"></a>授权请求返回的类型。</p>
<p id="p15291049103419"><a name="p15291049103419"></a><a name="p15291049103419"></a><strong id="b15138452103414"><a name="b15138452103414"></a><a name="b15138452103414"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选</strong>。</p>
<p id="p3145192183119"><a name="p3145192183119"></a><a name="p3145192183119"></a>枚举值：</p>
<a name="ul71451221133119"></a><a name="ul71451221133119"></a><ul id="ul71451221133119"><li>id_token</li></ul>
</td>
</tr>
<tr id="row20618173918386"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p561883918385"><a name="p561883918385"></a><a name="p561883918385"></a>response_mode</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p2618133923813"><a name="p2618133923813"></a><a name="p2618133923813"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p8618193915383"><a name="p8618193915383"></a><a name="p8618193915383"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1155410285350"><a name="p1155410285350"></a><a name="p1155410285350"></a>授权请求返回方式。</p>
<p id="p914520214311"><a name="p914520214311"></a><a name="p914520214311"></a><strong id="b16519331113510"><a name="b16519331113510"></a><a name="b16519331113510"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选。</strong></p>
<p id="p01451621113115"><a name="p01451621113115"></a><a name="p01451621113115"></a>枚举值：</p>
<a name="ul914502123116"></a><a name="ul914502123116"></a><ul id="ul914502123116"><li>fragment</li><li>form_post</li></ul>
</td>
</tr>
<tr id="row36183395382"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1761843913387"><a name="p1761843913387"></a><a name="p1761843913387"></a>signing_key</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p1361814391381"><a name="p1361814391381"></a><a name="p1361814391381"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p166181839183818"><a name="p166181839183818"></a><a name="p166181839183818"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p414552115316"><a name="p414552115316"></a><a name="p414552115316"></a>OpenID Connect身份提供商ID Token签名的公钥。</p>
<p id="p14891429613"><a name="p14891429613"></a><a name="p14891429613"></a>最小长度：10。最大长度：30000。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section14497193983812"></a>

**状态码为 200 时:**

**表 5**  响应Body参数

<a name="table24971039143812"></a>
<table><thead align="left"><tr id="row36186398382"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p19618039123811"><a name="p19618039123811"></a><a name="p19618039123811"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p561813910381"><a name="p561813910381"></a><a name="p561813910381"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1061843933819"><a name="p1061843933819"></a><a name="p1061843933819"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1361823973812"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p5618113914388"><a name="p5618113914388"></a><a name="p5618113914388"></a><a href="#table1750018395381">openid_connect_config</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p7618113973812"><a name="p7618113973812"></a><a name="p7618113973812"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p46181397386"><a name="p46181397386"></a><a name="p46181397386"></a>OpenID Connect配置详情。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  OpenIDConnectConfig

<a name="table1750018395381"></a>
<table><thead align="left"><tr id="row1261813943813"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p10618539123818"><a name="p10618539123818"></a><a name="p10618539123818"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p1261853917386"><a name="p1261853917386"></a><a name="p1261853917386"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1761833973812"><a name="p1761833973812"></a><a name="p1761833973812"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row166181139113818"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p061843983814"><a name="p061843983814"></a><a name="p061843983814"></a>access_mode</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p19618839183816"><a name="p19618839183816"></a><a name="p19618839183816"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p15988115824014"><a name="p15988115824014"></a><a name="p15988115824014"></a>访问方式。</p>
<a name="ul3988195817407"></a><a name="ul3988195817407"></a><ul id="ul3988195817407"><li>program_console: 支持编程访问和管理控制台访问方式。</li><li>program: 支持编程访问方式</li></ul>
</td>
</tr>
<tr id="row661819395389"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p9618173913384"><a name="p9618173913384"></a><a name="p9618173913384"></a>idp_url</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p2061833919389"><a name="p2061833919389"></a><a name="p2061833919389"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p18988195874017"><a name="p18988195874017"></a><a name="p18988195874017"></a>OpenID Connect身份提供商标识, 对应ID token 中 iss字段。</p>
</td>
</tr>
<tr id="row196186394389"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p11618153915387"><a name="p11618153915387"></a><a name="p11618153915387"></a>client_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p176181239173813"><a name="p176181239173813"></a><a name="p176181239173813"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p16989158184015"><a name="p16989158184015"></a><a name="p16989158184015"></a>在OpenID Connect身份提供商注册的客户端ID。</p>
</td>
</tr>
<tr id="row9618539103811"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p861873916380"><a name="p861873916380"></a><a name="p861873916380"></a>authorization_endpoint</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1861863912382"><a name="p1861863912382"></a><a name="p1861863912382"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p9989135814013"><a name="p9989135814013"></a><a name="p9989135814013"></a>OpenID Connect身份提供商授权地址。</p>
<p id="p6989658184012"><a name="p6989658184012"></a><a name="p6989658184012"></a><strong id="b1298955874010"><a name="b1298955874010"></a><a name="b1298955874010"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选</strong></p>
</td>
</tr>
<tr id="row76189397381"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p14618123933812"><a name="p14618123933812"></a><a name="p14618123933812"></a>scope</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p196181939163818"><a name="p196181939163818"></a><a name="p196181939163818"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p29891858134012"><a name="p29891858134012"></a><a name="p29891858134012"></a>授权请求信息范围。</p>
<p id="p11989135864011"><a name="p11989135864011"></a><a name="p11989135864011"></a><strong id="b12989185824012"><a name="b12989185824012"></a><a name="b12989185824012"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选。</strong></p>
<p id="p199892589401"><a name="p199892589401"></a><a name="p199892589401"></a>枚举值：</p>
<a name="ul12989258164017"></a><a name="ul12989258164017"></a><ul id="ul12989258164017"><li>openid</li><li>email</li><li>profile<div class="note" id="note16822102012120"><a name="note16822102012120"></a><a name="note16822102012120"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul138228201714"></a><a name="ul138228201714"></a><ul id="ul138228201714"><li>此字段必选值“openid”。</li><li>最少1个值，最多10个值，之间使用空格分割。</li></ul>
<p id="p78221520316"><a name="p78221520316"></a><a name="p78221520316"></a>例如： "openid" 、"openid email"、 "openid profile"、 "openid email profile"。</p>
</div></div>
</li></ul>
</td>
</tr>
<tr id="row56181039183814"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p7618173919382"><a name="p7618173919382"></a><a name="p7618173919382"></a>response_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1461813923811"><a name="p1461813923811"></a><a name="p1461813923811"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p398925816406"><a name="p398925816406"></a><a name="p398925816406"></a>授权请求返回的类型。</p>
<p id="p898935864013"><a name="p898935864013"></a><a name="p898935864013"></a><strong id="b15989145804011"><a name="b15989145804011"></a><a name="b15989145804011"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选</strong>。</p>
<p id="p1098975817409"><a name="p1098975817409"></a><a name="p1098975817409"></a>枚举值：</p>
<a name="ul298915818408"></a><a name="ul298915818408"></a><ul id="ul298915818408"><li>id_token</li></ul>
</td>
</tr>
<tr id="row11619183912380"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p5619939203813"><a name="p5619939203813"></a><a name="p5619939203813"></a>response_mode</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p166193391388"><a name="p166193391388"></a><a name="p166193391388"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1798905894011"><a name="p1798905894011"></a><a name="p1798905894011"></a>授权请求返回方式。</p>
<p id="p169893584407"><a name="p169893584407"></a><a name="p169893584407"></a><strong id="b1798920589403"><a name="b1798920589403"></a><a name="b1798920589403"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选。</strong></p>
<p id="p19989105813405"><a name="p19989105813405"></a><a name="p19989105813405"></a>枚举值：</p>
<a name="ul20989195864018"></a><a name="ul20989195864018"></a><ul id="ul20989195864018"><li>fragment</li><li>form_post</li></ul>
</td>
</tr>
<tr id="row96191839203816"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1161913912382"><a name="p1161913912382"></a><a name="p1161913912382"></a>signing_key</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p20619639143817"><a name="p20619639143817"></a><a name="p20619639143817"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p12989258104013"><a name="p12989258104013"></a><a name="p12989258104013"></a>OpenID Connect身份提供商ID Token签名的公钥。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section7511133963810"></a>

-   修改编程访问配置

    ```
    PUT /v3.0/OS-FEDERATION/identity-providers/{idp_id}/openid-connect-config 
      
     { 
       "openid_connect_config" : { 
         "access_mode" : "program", 
         "idp_url" : "https://accounts.example.com", 
         "client_id" : "client_id_example", 
         "signing_key" : "{\"keys\":[{\"kty\":\"RSA\",\"e\":\"AQAB\",\"use\":\"sig\",\"n\":\"example\",\"kid\":\"kid_example\",\"alg\":\"RS256\"}]}" 
       } 
     }
    ```

-   修改编程访问和管理控制台访问配置

    ```
    PUT /v3.0/OS-FEDERATION/identity-providers/{idp_id}/openid-connect-config 
      
     { 
       "openid_connect_config" : { 
         "access_mode" : "program_console", 
         "idp_url" : "https://accounts.example.com", 
         "client_id" : "client_id_example", 
         "authorization_endpoint" : "https://accounts.example.com/o/oauth2/v2/auth", 
         "scope" : "openid", 
         "response_type" : "id_token", 
         "response_mode" : "form_post", 
         "signing_key" : "{\"keys\":[{\"kty\":\"RSA\",\"e\":\"AQAB\",\"use\":\"sig\",\"n\":\"example\",\"kid\":\"kid_example\",\"alg\":\"RS256\"}]}" 
       } 
     }
    ```


## 响应示例<a name="section1151363912381"></a>

**状态码为 200 时:**

请求成功。

```
{ 
  "openid_connect_config" : { 
    "access_mode" : "program_console", 
    "idp_url" : "https://accounts.example.com", 
    "client_id" : "client_id_example", 
    "authorization_endpoint" : "https://accounts.example.com/o/oauth2/v2/auth", 
    "scope" : "openid", 
    "response_type" : "id_token", 
    "response_mode" : "form_post", 
    "signing_key" : "{\"keys\":[{\"kty\":\"RSA\",\"e\":\"AQAB\",\"use\":\"sig\",\"n\":\"example\",\"kid\":\"kid_example\",\"alg\":\"RS256\"}]}" 
  } 
}
```

## 状态码<a name="section951873923814"></a>

<a name="table3518339193818"></a>
<table><thead align="left"><tr id="row461903916384"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p8619143917382"><a name="p8619143917382"></a><a name="p8619143917382"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p86199393382"><a name="p86199393382"></a><a name="p86199393382"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row19619173910382"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p116191539143815"><a name="p116191539143815"></a><a name="p116191539143815"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p1961963918382"><a name="p1961963918382"></a><a name="p1961963918382"></a>请求成功。</p>
</td>
</tr>
<tr id="row66191239143811"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p12619133918386"><a name="p12619133918386"></a><a name="p12619133918386"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p361943953818"><a name="p361943953818"></a><a name="p361943953818"></a>参数无效。</p>
</td>
</tr>
<tr id="row1361910397384"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p46191739133817"><a name="p46191739133817"></a><a name="p46191739133817"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p166192039123815"><a name="p166192039123815"></a><a name="p166192039123815"></a>认证失败。</p>
</td>
</tr>
<tr id="row9619143911381"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p76195391380"><a name="p76195391380"></a><a name="p76195391380"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p136192039103815"><a name="p136192039103815"></a><a name="p136192039103815"></a>没有操作权限。</p>
</td>
</tr>
<tr id="row561973914387"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p19620133913384"><a name="p19620133913384"></a><a name="p19620133913384"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p15620163933812"><a name="p15620163933812"></a><a name="p15620163933812"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="row196203392387"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p13620153943810"><a name="p13620153943810"></a><a name="p13620153943810"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p15620939203813"><a name="p15620939203813"></a><a name="p15620939203813"></a>系统内部错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section7522113910383"></a>

请参见[错误码](错误码.md)。

