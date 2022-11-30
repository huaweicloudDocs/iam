# 创建OpenID Connect身份提供商配置<a name="iam_13_0207"></a>

## 功能介绍<a name="section093472073113"></a>

该接口可以用于<u>[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)</u><u></u>  在[创建身份提供商](创建身份提供商.md)，并[注册协议](注册协议.md)（OIDC协议）后，创建OpenID Connect身份提供商配置。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section2485151619141"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=CreateOpenIdConnectConfig)中调试该接口。

## URI<a name="section1693712205313"></a>

POST /v3.0/OS-FEDERATION/identity-providers/\{idp\_id\}/openid-connect-config

**表 1**  路径参数

<a name="table293802015318"></a>
<table><thead align="left"><tr id="row19144172183118"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p111447211311"><a name="p111447211311"></a><a name="p111447211311"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p11447213313"><a name="p11447213313"></a><a name="p11447213313"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p314418213313"><a name="p314418213313"></a><a name="p314418213313"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p414415214312"><a name="p414415214312"></a><a name="p414415214312"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row51442214311"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1414412219316"><a name="p1414412219316"></a><a name="p1414412219316"></a>idp_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p12144202123117"><a name="p12144202123117"></a><a name="p12144202123117"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1144192116317"><a name="p1144192116317"></a><a name="p1144192116317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p2144112173116"><a name="p2144112173116"></a><a name="p2144112173116"></a>身份提供商名称。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="section694752033115"></a>

**表 2**  请求Header参数

<a name="table1094862012315"></a>
<table><thead align="left"><tr id="row21441121203110"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p414462113319"><a name="p414462113319"></a><a name="p414462113319"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p1314442193111"><a name="p1314442193111"></a><a name="p1314442193111"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p13144102112319"><a name="p13144102112319"></a><a name="p13144102112319"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p814432113318"><a name="p814432113318"></a><a name="p814432113318"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row3144122119310"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p7144132133111"><a name="p7144132133111"></a><a name="p7144132133111"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p6144221133110"><a name="p6144221133110"></a><a name="p6144221133110"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p714414213315"><a name="p714414213315"></a><a name="p714414213315"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p141441221163120"><a name="p141441221163120"></a><a name="p141441221163120"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="row6144121163110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p514462133112"><a name="p514462133112"></a><a name="p514462133112"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p114442153117"><a name="p114442153117"></a><a name="p114442153117"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p81449217317"><a name="p81449217317"></a><a name="p81449217317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p18144142115312"><a name="p18144142115312"></a><a name="p18144142115312"></a>请参见<a href="授权项.md">授权项</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="table3954102011317"></a>
<table><thead align="left"><tr id="row114442118315"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p1314462112319"><a name="p1314462112319"></a><a name="p1314462112319"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p214462173115"><a name="p214462173115"></a><a name="p214462173115"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1414482118313"><a name="p1414482118313"></a><a name="p1414482118313"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p1144192111318"><a name="p1144192111318"></a><a name="p1144192111318"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row2144172110312"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1144162116319"><a name="p1144162116319"></a><a name="p1144162116319"></a><a href="#table15957142011312">openid_connect_config</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p11144821103116"><a name="p11144821103116"></a><a name="p11144821103116"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p61445215313"><a name="p61445215313"></a><a name="p61445215313"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1144202113117"><a name="p1144202113117"></a><a name="p1144202113117"></a>OpenID Connect配置详情。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  CreateOpenIDConnectConfig

<a name="table15957142011312"></a>
<table><thead align="left"><tr id="row2144152123112"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p3144421143114"><a name="p3144421143114"></a><a name="p3144421143114"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p51441321113117"><a name="p51441321113117"></a><a name="p51441321113117"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p21441121113116"><a name="p21441121113116"></a><a name="p21441121113116"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p2014492118318"><a name="p2014492118318"></a><a name="p2014492118318"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row161441021163112"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p14144621193111"><a name="p14144621193111"></a><a name="p14144621193111"></a>access_mode</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p81449213311"><a name="p81449213311"></a><a name="p81449213311"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p191441821123118"><a name="p191441821123118"></a><a name="p191441821123118"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p611593517328"><a name="p611593517328"></a><a name="p611593517328"></a>访问方式。</p>
<a name="ul1166237163218"></a><a name="ul1166237163218"></a><ul id="ul1166237163218"><li>program_console: 支持编程访问和管理控制台访问方式。</li><li>program: 支持编程访问方式</li></ul>
</td>
</tr>
<tr id="row014412117311"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1714412143112"><a name="p1714412143112"></a><a name="p1714412143112"></a>idp_url</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p15144182123115"><a name="p15144182123115"></a><a name="p15144182123115"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p61441221123117"><a name="p61441221123117"></a><a name="p61441221123117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1514462119318"><a name="p1514462119318"></a><a name="p1514462119318"></a>OpenID Connect身份提供商标识, 对应ID token 中 iss字段。</p>
<p id="p413564920525"><a name="p413564920525"></a><a name="p413564920525"></a>最小长度：10。最大长度：255。</p>
</td>
</tr>
<tr id="row81446218311"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1914572113311"><a name="p1914572113311"></a><a name="p1914572113311"></a>client_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p12145421183117"><a name="p12145421183117"></a><a name="p12145421183117"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1014518212311"><a name="p1014518212311"></a><a name="p1014518212311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p111454219316"><a name="p111454219316"></a><a name="p111454219316"></a>在OpenID Connect身份提供商注册的客户端ID。</p>
<p id="p34251044175219"><a name="p34251044175219"></a><a name="p34251044175219"></a>最小长度：5。最大长度：255。</p>
</td>
</tr>
<tr id="row4145102114315"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p81451921143110"><a name="p81451921143110"></a><a name="p81451921143110"></a>authorization_endpoint</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p2145132114314"><a name="p2145132114314"></a><a name="p2145132114314"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p81455216313"><a name="p81455216313"></a><a name="p81455216313"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1427416283317"><a name="p1427416283317"></a><a name="p1427416283317"></a>OpenID Connect身份提供商授权地址。</p>
<p id="p714514217312"><a name="p714514217312"></a><a name="p714514217312"></a><strong id="b1117016683311"><a name="b1117016683311"></a><a name="b1117016683311"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选</strong>。</p>
<p id="p1851121112535"><a name="p1851121112535"></a><a name="p1851121112535"></a>最小长度：10。最大长度：255。</p>
</td>
</tr>
<tr id="row1914512123110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p12145921113113"><a name="p12145921113113"></a><a name="p12145921113113"></a>scope</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p3145172119318"><a name="p3145172119318"></a><a name="p3145172119318"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p4145102163116"><a name="p4145102163116"></a><a name="p4145102163116"></a>String</p>
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
<tr id="row214522153113"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p714532115310"><a name="p714532115310"></a><a name="p714532115310"></a>response_type</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p12145192143110"><a name="p12145192143110"></a><a name="p12145192143110"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1114518210316"><a name="p1114518210316"></a><a name="p1114518210316"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1841811576348"><a name="p1841811576348"></a><a name="p1841811576348"></a>授权请求返回的类型。</p>
<p id="p15291049103419"><a name="p15291049103419"></a><a name="p15291049103419"></a><strong id="b15138452103414"><a name="b15138452103414"></a><a name="b15138452103414"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选</strong>。</p>
<p id="p3145192183119"><a name="p3145192183119"></a><a name="p3145192183119"></a>枚举值：</p>
<a name="ul71451221133119"></a><a name="ul71451221133119"></a><ul id="ul71451221133119"><li>id_token</li></ul>
</td>
</tr>
<tr id="row18145152173117"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1414562123113"><a name="p1414562123113"></a><a name="p1414562123113"></a>response_mode</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p141458217310"><a name="p141458217310"></a><a name="p141458217310"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p7145112163113"><a name="p7145112163113"></a><a name="p7145112163113"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1155410285350"><a name="p1155410285350"></a><a name="p1155410285350"></a>授权请求返回方式。</p>
<p id="p914520214311"><a name="p914520214311"></a><a name="p914520214311"></a><strong id="b16519331113510"><a name="b16519331113510"></a><a name="b16519331113510"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选。</strong></p>
<p id="p01451621113115"><a name="p01451621113115"></a><a name="p01451621113115"></a>枚举值：</p>
<a name="ul914502123116"></a><a name="ul914502123116"></a><ul id="ul914502123116"><li>fragment</li><li>form_post</li></ul>
</td>
</tr>
<tr id="row3145202114317"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p214572153112"><a name="p214572153112"></a><a name="p214572153112"></a>signing_key</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p11145121183118"><a name="p11145121183118"></a><a name="p11145121183118"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p91451521193115"><a name="p91451521193115"></a><a name="p91451521193115"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p414552115316"><a name="p414552115316"></a><a name="p414552115316"></a>OpenID Connect身份提供商ID Token签名的公钥。</p>
<p id="p14891429613"><a name="p14891429613"></a><a name="p14891429613"></a>最小长度：10。最大长度：30000。</p>
<p id="p1217527174916"><a name="p1217527174916"></a><a name="p1217527174916"></a>格式示例：</p>
<pre class="screen" id="screen152894895118"><a name="screen152894895118"></a><a name="screen152894895118"></a>{
  "keys":[
     {
        "kid":"d05ef20c4512645vv1..." ,
        "n":"cws_cnjiwsbvweolwn_-vnl...",
        "e":"AQAB",
        "kty":"RSA",
        "use":"sig",
        "alg":"RS256"
      }
   ]
} </pre>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section11977720193119"></a>

**状态码为 201 时:**

**表 5**  响应Body参数

<a name="table20977122003112"></a>
<table><thead align="left"><tr id="row151459217317"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p4145021113113"><a name="p4145021113113"></a><a name="p4145021113113"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p5145162117314"><a name="p5145162117314"></a><a name="p5145162117314"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p2014518215310"><a name="p2014518215310"></a><a name="p2014518215310"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row7145421173119"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p7145021103119"><a name="p7145021103119"></a><a name="p7145021103119"></a><a href="#table6981112015312">openid_connect_config</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p71451621183112"><a name="p71451621183112"></a><a name="p71451621183112"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p8145152143111"><a name="p8145152143111"></a><a name="p8145152143111"></a>OpenID Connect配置详情。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  openid\_connect\_config

<a name="table6981112015312"></a>
<table><thead align="left"><tr id="row6145112112316"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p15145221123114"><a name="p15145221123114"></a><a name="p15145221123114"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p814516218315"><a name="p814516218315"></a><a name="p814516218315"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p19145921193116"><a name="p19145921193116"></a><a name="p19145921193116"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6145172116319"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p214502113118"><a name="p214502113118"></a><a name="p214502113118"></a>access_mode</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1914582116311"><a name="p1914582116311"></a><a name="p1914582116311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p111775195365"><a name="p111775195365"></a><a name="p111775195365"></a>访问方式。</p>
<a name="ul981662033612"></a><a name="ul981662033612"></a><ul id="ul981662033612"><li>program_console: 支持编程访问和管理控制台访问方式。</li><li>program: 支持编程访问方式。</li></ul>
</td>
</tr>
<tr id="row914519212318"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p11453212318"><a name="p11453212318"></a><a name="p11453212318"></a>idp_url</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1614515212316"><a name="p1614515212316"></a><a name="p1614515212316"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1814532183114"><a name="p1814532183114"></a><a name="p1814532183114"></a>OpenID Connect身份提供商标识。对应ID token 中 iss字段。</p>
</td>
</tr>
<tr id="row7145172173110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1414512193119"><a name="p1414512193119"></a><a name="p1414512193119"></a>client_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p151451121183115"><a name="p151451121183115"></a><a name="p151451121183115"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p3145122117313"><a name="p3145122117313"></a><a name="p3145122117313"></a>在OpenID Connect身份提供商注册的客户端ID。</p>
</td>
</tr>
<tr id="row1914562133114"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p10145121193111"><a name="p10145121193111"></a><a name="p10145121193111"></a>authorization_endpoint</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p71451021123113"><a name="p71451021123113"></a><a name="p71451021123113"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1796284518363"><a name="p1796284518363"></a><a name="p1796284518363"></a>OpenID Connect身份提供商授权地址。</p>
<p id="p1814513215311"><a name="p1814513215311"></a><a name="p1814513215311"></a><strong id="b20611253173611"><a name="b20611253173611"></a><a name="b20611253173611"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选。</strong></p>
</td>
</tr>
<tr id="row61451521113114"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p101451721163110"><a name="p101451721163110"></a><a name="p101451721163110"></a>scope</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p41451221173118"><a name="p41451221173118"></a><a name="p41451221173118"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p382010207373"><a name="p382010207373"></a><a name="p382010207373"></a>授权请求信息范围。</p>
<p id="p1182116201378"><a name="p1182116201378"></a><a name="p1182116201378"></a><strong id="b20821122011378"><a name="b20821122011378"></a><a name="b20821122011378"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选。</strong></p>
<p id="p882192012373"><a name="p882192012373"></a><a name="p882192012373"></a>枚举值：</p>
<a name="ul10821720143716"></a><a name="ul10821720143716"></a><ul id="ul10821720143716"><li>openid</li><li>email</li><li>profile<div class="note" id="note55238419115"><a name="note55238419115"></a><a name="note55238419115"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul1352313420120"></a><a name="ul1352313420120"></a><ul id="ul1352313420120"><li>此字段必选值“openid”。</li><li>最少1个值，最多10个值，之间使用空格分割。</li></ul>
<p id="p165236411111"><a name="p165236411111"></a><a name="p165236411111"></a>例如： "openid" 、"openid email"、 "openid profile"、 "openid email profile"。</p>
</div></div>
</li></ul>
</td>
</tr>
<tr id="row1414562163119"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1614552123115"><a name="p1614552123115"></a><a name="p1614552123115"></a>response_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1314592113116"><a name="p1314592113116"></a><a name="p1314592113116"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1082115201371"><a name="p1082115201371"></a><a name="p1082115201371"></a>授权请求返回的类型。</p>
<p id="p9821720123711"><a name="p9821720123711"></a><a name="p9821720123711"></a><strong id="b8821162019376"><a name="b8821162019376"></a><a name="b8821162019376"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选</strong>。</p>
<p id="p10821620133711"><a name="p10821620133711"></a><a name="p10821620133711"></a>枚举值：</p>
<a name="ul148210206375"></a><a name="ul148210206375"></a><ul id="ul148210206375"><li>id_token</li></ul>
</td>
</tr>
<tr id="row31451521103118"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p514510213311"><a name="p514510213311"></a><a name="p514510213311"></a>response_mode</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1914572113110"><a name="p1914572113110"></a><a name="p1914572113110"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1082112023711"><a name="p1082112023711"></a><a name="p1082112023711"></a>授权请求返回方式。</p>
<p id="p48211920173711"><a name="p48211920173711"></a><a name="p48211920173711"></a><strong id="b982102083718"><a name="b982102083718"></a><a name="b982102083718"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选。</strong></p>
<p id="p128211720173719"><a name="p128211720173719"></a><a name="p128211720173719"></a>枚举值：</p>
<a name="ul98215206373"></a><a name="ul98215206373"></a><ul id="ul98215206373"><li>fragment</li><li>form_post</li></ul>
</td>
</tr>
<tr id="row914692173114"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p114672143114"><a name="p114672143114"></a><a name="p114672143114"></a>signing_key</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p414672113315"><a name="p414672113315"></a><a name="p414672113315"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p68211320153712"><a name="p68211320153712"></a><a name="p68211320153712"></a>OpenID Connect身份提供商ID Token签名的公钥。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section1399672014314"></a>

-   创建支持编程访问配置

    ```
    POST /v3.0/OS-FEDERATION/identity-providers/{idp_id}/openid-connect-config 
      
     { 
       "openid_connect_config" : { 
         "access_mode" : "program", 
         "idp_url" : "https://accounts.example.com", 
         "client_id" : "client_id_example", 
         "signing_key" : "{\"keys\":[{\"kty\":\"RSA\",\"e\":\"AQAB\",\"use\":\"sig\",\"n\":\"example\",\"kid\":\"kid_example\",\"alg\":\"RS256\"}]}" 
       } 
     }
    ```

-   创建支持编程访问和管理控制台访问配置

    ```
    POST /v3.0/OS-FEDERATION/identity-providers/{idp_id}/openid-connect-config 
      
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


## 响应示例<a name="section499813201314"></a>

**状态码为 201 时:**

创建成功。

-   示例 1

    ```
    { 
       "openid_connect_config" : { 
         "access_mode" : "program", 
         "idp_url" : "https://accounts.example.com", 
         "client_id" : "client_id_example", 
         "signing_key" : "{\"keys\":[{\"kty\":\"RSA\",\"e\":\"AQAB\",\"use\":\"sig\",\"n\":\"example\",\"kid\":\"kid_example\",\"alg\":\"RS256\"}]}" 
       } 
     }
    ```

-   示例 2

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


## 状态码<a name="section26821103118"></a>

<a name="table77321143119"></a>
<table><thead align="left"><tr id="row61461021123115"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p141461221183117"><a name="p141461221183117"></a><a name="p141461221183117"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p181469210316"><a name="p181469210316"></a><a name="p181469210316"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row414616219312"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p15146132111315"><a name="p15146132111315"></a><a name="p15146132111315"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p41460211313"><a name="p41460211313"></a><a name="p41460211313"></a>创建成功。</p>
</td>
</tr>
<tr id="row514610214315"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p31461721143118"><a name="p31461721143118"></a><a name="p31461721143118"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p814612119314"><a name="p814612119314"></a><a name="p814612119314"></a>参数无效。</p>
</td>
</tr>
<tr id="row1914692112319"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p18146152173112"><a name="p18146152173112"></a><a name="p18146152173112"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p1414612115318"><a name="p1414612115318"></a><a name="p1414612115318"></a>认证失败。</p>
</td>
</tr>
<tr id="row15146102113118"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p171461221173117"><a name="p171461221173117"></a><a name="p171461221173117"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p6147112116312"><a name="p6147112116312"></a><a name="p6147112116312"></a>没有操作权限。</p>
</td>
</tr>
<tr id="row1614715219314"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p121477217319"><a name="p121477217319"></a><a name="p121477217319"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p151472218318"><a name="p151472218318"></a><a name="p151472218318"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="row1214715219310"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p2147182115314"><a name="p2147182115314"></a><a name="p2147182115314"></a>409</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p2147321103117"><a name="p2147321103117"></a><a name="p2147321103117"></a>资源已存在。</p>
</td>
</tr>
<tr id="row11147621153110"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p11147192116312"><a name="p11147192116312"></a><a name="p11147192116312"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p714792103115"><a name="p714792103115"></a><a name="p714792103115"></a>系统内部错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section6121621193111"></a>

请参见[错误码](错误码.md)。

