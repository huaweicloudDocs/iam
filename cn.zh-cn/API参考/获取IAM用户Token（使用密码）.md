# 获取IAM用户Token（使用密码）<a name="iam_30_0001"></a>

## 功能介绍<a name="zh-cn_topic_0221482476_section537119534412"></a>

该接口可以用于通过用户名/密码的方式进行认证来获取IAM用户token。

token是系统颁发给IAM用户的访问令牌，承载用户的身份、权限等信息。调用IAM以及其他云服务的接口时，可以使用本接口获取的IAM用户token进行鉴权。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。如果使用全局区域的Endpoint调用，该token可以在所有区域使用；如果使用非全局区域的Endpoint调用，则该token仅在该区域生效，不能跨区域使用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   token的有效期为24小时，建议进行缓存，避免频繁调用。  
>-   通过Postman获取用户token示例请参见：[如何通过Postman获取用户Token](https://support.huaweicloud.com/iam_faq/iam_01_034.html)。  
>-   如果需要获取具有Security Administrator权限的token，请参见：[IAM 常见问题](https://support.huaweicloud.com/iam_faq/iam_01_0608.html)。  

## URI<a name="zh-cn_topic_0221482476_section6373155310419"></a>

POST /v3/auth/tokens

**表 1**  Query参数

<a name="zh-cn_topic_0221482476_table537411533416"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row5374205313414"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482476_p43748531747"><a name="zh-cn_topic_0221482476_p43748531747"></a><a name="zh-cn_topic_0221482476_p43748531747"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482476_p937514535419"><a name="zh-cn_topic_0221482476_p937514535419"></a><a name="zh-cn_topic_0221482476_p937514535419"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482476_p163751053443"><a name="zh-cn_topic_0221482476_p163751053443"></a><a name="zh-cn_topic_0221482476_p163751053443"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482476_p1737595310418"><a name="zh-cn_topic_0221482476_p1737595310418"></a><a name="zh-cn_topic_0221482476_p1737595310418"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row1737485313419"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p1637513531543"><a name="zh-cn_topic_0221482476_p1637513531543"></a><a name="zh-cn_topic_0221482476_p1637513531543"></a>nocatalog</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p123751853946"><a name="zh-cn_topic_0221482476_p123751853946"></a><a name="zh-cn_topic_0221482476_p123751853946"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p037513531545"><a name="zh-cn_topic_0221482476_p037513531545"></a><a name="zh-cn_topic_0221482476_p037513531545"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p63762532412"><a name="zh-cn_topic_0221482476_p63762532412"></a><a name="zh-cn_topic_0221482476_p63762532412"></a>如果设置该参数，返回的响应体中将不显示catalog信息。任何非空字符串都将解释为true，并使该字段生效。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482476_section1537611531541"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482476_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row133769539414"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482476_p137712539412"><a name="zh-cn_topic_0221482476_p137712539412"></a><a name="zh-cn_topic_0221482476_p137712539412"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482476_p4377153842"><a name="zh-cn_topic_0221482476_p4377153842"></a><a name="zh-cn_topic_0221482476_p4377153842"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482476_p1337713533418"><a name="zh-cn_topic_0221482476_p1337713533418"></a><a name="zh-cn_topic_0221482476_p1337713533418"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482476_p183771153544"><a name="zh-cn_topic_0221482476_p183771153544"></a><a name="zh-cn_topic_0221482476_p183771153544"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row183769531246"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p737714535411"><a name="zh-cn_topic_0221482476_p737714535411"></a><a name="zh-cn_topic_0221482476_p737714535411"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p2037835319411"><a name="zh-cn_topic_0221482476_p2037835319411"></a><a name="zh-cn_topic_0221482476_p2037835319411"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p1037895318411"><a name="zh-cn_topic_0221482476_p1037895318411"></a><a name="zh-cn_topic_0221482476_p1037895318411"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p1437819538420"><a name="zh-cn_topic_0221482476_p1437819538420"></a><a name="zh-cn_topic_0221482476_p1437819538420"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="zh-cn_topic_0221482476_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row1537855317412"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482476_p1337918536415"><a name="zh-cn_topic_0221482476_p1337918536415"></a><a name="zh-cn_topic_0221482476_p1337918536415"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482476_p15379135319411"><a name="zh-cn_topic_0221482476_p15379135319411"></a><a name="zh-cn_topic_0221482476_p15379135319411"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482476_p13798532420"><a name="zh-cn_topic_0221482476_p13798532420"></a><a name="zh-cn_topic_0221482476_p13798532420"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482476_p437919538417"><a name="zh-cn_topic_0221482476_p437919538417"></a><a name="zh-cn_topic_0221482476_p437919538417"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row163789535420"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p93790538414"><a name="zh-cn_topic_0221482476_p93790538414"></a><a name="zh-cn_topic_0221482476_p93790538414"></a><a href="#zh-cn_topic_0221482476_request_Rq31Auth">auth</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p1738020531842"><a name="zh-cn_topic_0221482476_p1738020531842"></a><a name="zh-cn_topic_0221482476_p1738020531842"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p13801853448"><a name="zh-cn_topic_0221482476_p13801853448"></a><a name="zh-cn_topic_0221482476_p13801853448"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p10380155311416"><a name="zh-cn_topic_0221482476_p10380155311416"></a><a name="zh-cn_topic_0221482476_p10380155311416"></a>认证信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  auth

<a name="zh-cn_topic_0221482476_request_Rq31Auth"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row338035320414"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482476_p4381125314420"><a name="zh-cn_topic_0221482476_p4381125314420"></a><a name="zh-cn_topic_0221482476_p4381125314420"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482476_p143816535413"><a name="zh-cn_topic_0221482476_p143816535413"></a><a name="zh-cn_topic_0221482476_p143816535413"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482476_p43811530415"><a name="zh-cn_topic_0221482476_p43811530415"></a><a name="zh-cn_topic_0221482476_p43811530415"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482476_p4381553443"><a name="zh-cn_topic_0221482476_p4381553443"></a><a name="zh-cn_topic_0221482476_p4381553443"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row63801553146"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p133811453946"><a name="zh-cn_topic_0221482476_p133811453946"></a><a name="zh-cn_topic_0221482476_p133811453946"></a><a href="#zh-cn_topic_0221482476_request_Rq31AuthIdentity">identity</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p1381115320414"><a name="zh-cn_topic_0221482476_p1381115320414"></a><a name="zh-cn_topic_0221482476_p1381115320414"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p15382155314419"><a name="zh-cn_topic_0221482476_p15382155314419"></a><a name="zh-cn_topic_0221482476_p15382155314419"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p1438225310419"><a name="zh-cn_topic_0221482476_p1438225310419"></a><a name="zh-cn_topic_0221482476_p1438225310419"></a>认证参数。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row83806531449"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p138220531849"><a name="zh-cn_topic_0221482476_p138220531849"></a><a name="zh-cn_topic_0221482476_p138220531849"></a><a href="#zh-cn_topic_0221482476_request_Rq31AuthScope">scope</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p538217531948"><a name="zh-cn_topic_0221482476_p538217531948"></a><a name="zh-cn_topic_0221482476_p538217531948"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p338219531045"><a name="zh-cn_topic_0221482476_p338219531045"></a><a name="zh-cn_topic_0221482476_p338219531045"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p193821453842"><a name="zh-cn_topic_0221482476_p193821453842"></a><a name="zh-cn_topic_0221482476_p193821453842"></a>token的使用范围，取值为project或domain，二选一即可。</p>
<div class="note" id="zh-cn_topic_0221482476_note1838311531442"><a name="zh-cn_topic_0221482476_note1838311531442"></a><a name="zh-cn_topic_0221482476_note1838311531442"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="zh-cn_topic_0221482476_p538375314415"><a name="zh-cn_topic_0221482476_p538375314415"></a><a name="zh-cn_topic_0221482476_p538375314415"></a>使用全局区域的Endpoint调用该接口时，推荐您将scope设置为domain，该token可以跨区域使用。如果将scope设置为project，该token仅能在指定的project中使用。</p>
</div></div>
</td>
</tr>
</tbody>
</table>

**表 5**  auth.identity

<a name="zh-cn_topic_0221482476_request_Rq31AuthIdentity"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row338315313411"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482476_p63842531746"><a name="zh-cn_topic_0221482476_p63842531746"></a><a name="zh-cn_topic_0221482476_p63842531746"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482476_p1138415532048"><a name="zh-cn_topic_0221482476_p1138415532048"></a><a name="zh-cn_topic_0221482476_p1138415532048"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482476_p123841853342"><a name="zh-cn_topic_0221482476_p123841853342"></a><a name="zh-cn_topic_0221482476_p123841853342"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482476_p113847537419"><a name="zh-cn_topic_0221482476_p113847537419"></a><a name="zh-cn_topic_0221482476_p113847537419"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row133831053643"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p15384753546"><a name="zh-cn_topic_0221482476_p15384753546"></a><a name="zh-cn_topic_0221482476_p15384753546"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p338411534410"><a name="zh-cn_topic_0221482476_p338411534410"></a><a name="zh-cn_topic_0221482476_p338411534410"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p1385165317416"><a name="zh-cn_topic_0221482476_p1385165317416"></a><a name="zh-cn_topic_0221482476_p1385165317416"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p1385753345"><a name="zh-cn_topic_0221482476_p1385753345"></a><a name="zh-cn_topic_0221482476_p1385753345"></a>认证方法，该字段内容为["password"]。</p>
<p id="zh-cn_topic_0221482476_p738516531043"><a name="zh-cn_topic_0221482476_p738516531043"></a><a name="zh-cn_topic_0221482476_p738516531043"></a>取值范围：</p>
<a name="zh-cn_topic_0221482476_ul93853534418"></a><a name="zh-cn_topic_0221482476_ul93853534418"></a><ul id="zh-cn_topic_0221482476_ul93853534418"><li>password</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row238317533420"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p5385155319410"><a name="zh-cn_topic_0221482476_p5385155319410"></a><a name="zh-cn_topic_0221482476_p5385155319410"></a><a href="#zh-cn_topic_0221482476_request_Rq31AuthIdentityPwd">password</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p123851253544"><a name="zh-cn_topic_0221482476_p123851253544"></a><a name="zh-cn_topic_0221482476_p123851253544"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p23861753243"><a name="zh-cn_topic_0221482476_p23861753243"></a><a name="zh-cn_topic_0221482476_p23861753243"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p2386553143"><a name="zh-cn_topic_0221482476_p2386553143"></a><a name="zh-cn_topic_0221482476_p2386553143"></a>IAM用户密码认证信息。</p>
<div class="note" id="zh-cn_topic_0221482476_note738613539417"><a name="zh-cn_topic_0221482476_note738613539417"></a><a name="zh-cn_topic_0221482476_note738613539417"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0221482476_ul03863531042"></a><a name="zh-cn_topic_0221482476_ul03863531042"></a><ul id="zh-cn_topic_0221482476_ul03863531042"><li>user.name和user.domain.name可以在界面控制台“我的凭证”中查看，具体获取方法请参见：<a href="获取账号-IAM用户-项目-用户组-委托的名称和ID.md">获取账号、IAM用户、项目、用户组、委托的名称和ID</a>。</li><li>如果是第三方系统用户，直接使用联邦认证的用户名和密码获取token，系统会提示密码错误。需要在华为云的登录页面，通过“忘记密码” 功能，在华为云中设置登录密码，并在password中输入新设置的密码。</li><li>该接口提供了锁定机制用于防止暴力破解，调用时，请确保用户名密码正确，输错一定次数（<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>可设置该规则，方法请参见：<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0704.html" target="_blank" rel="noopener noreferrer">账号锁定策略</a>）将被锁定。</li></ul>
</div></div>
</td>
</tr>
</tbody>
</table>

**表 6**  auth.identity.password

<a name="zh-cn_topic_0221482476_request_Rq31AuthIdentityPwd"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row1538719537411"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482476_p1238711535418"><a name="zh-cn_topic_0221482476_p1238711535418"></a><a name="zh-cn_topic_0221482476_p1238711535418"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482476_p1388185313410"><a name="zh-cn_topic_0221482476_p1388185313410"></a><a name="zh-cn_topic_0221482476_p1388185313410"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482476_p73881753143"><a name="zh-cn_topic_0221482476_p73881753143"></a><a name="zh-cn_topic_0221482476_p73881753143"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482476_p03884531045"><a name="zh-cn_topic_0221482476_p03884531045"></a><a name="zh-cn_topic_0221482476_p03884531045"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row1938719535411"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p173881853048"><a name="zh-cn_topic_0221482476_p173881853048"></a><a name="zh-cn_topic_0221482476_p173881853048"></a><a href="#zh-cn_topic_0221482476_request_Rq31AuthIdentityPwdUser">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p2038865312413"><a name="zh-cn_topic_0221482476_p2038865312413"></a><a name="zh-cn_topic_0221482476_p2038865312413"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p23891653345"><a name="zh-cn_topic_0221482476_p23891653345"></a><a name="zh-cn_topic_0221482476_p23891653345"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p238955313416"><a name="zh-cn_topic_0221482476_p238955313416"></a><a name="zh-cn_topic_0221482476_p238955313416"></a>需要获取token的IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  auth.identity.password.user

<a name="zh-cn_topic_0221482476_request_Rq31AuthIdentityPwdUser"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row10389253346"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482476_p1039018538411"><a name="zh-cn_topic_0221482476_p1039018538411"></a><a name="zh-cn_topic_0221482476_p1039018538411"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482476_p15390115318417"><a name="zh-cn_topic_0221482476_p15390115318417"></a><a name="zh-cn_topic_0221482476_p15390115318417"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482476_p163901253943"><a name="zh-cn_topic_0221482476_p163901253943"></a><a name="zh-cn_topic_0221482476_p163901253943"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482476_p439016531047"><a name="zh-cn_topic_0221482476_p439016531047"></a><a name="zh-cn_topic_0221482476_p439016531047"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row938905311415"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p123902531941"><a name="zh-cn_topic_0221482476_p123902531941"></a><a name="zh-cn_topic_0221482476_p123902531941"></a><a href="#zh-cn_topic_0221482476_request_Rq31AuthIdentityPwdUserDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p53904536417"><a name="zh-cn_topic_0221482476_p53904536417"></a><a name="zh-cn_topic_0221482476_p53904536417"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p12391853945"><a name="zh-cn_topic_0221482476_p12391853945"></a><a name="zh-cn_topic_0221482476_p12391853945"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p1639185317419"><a name="zh-cn_topic_0221482476_p1639185317419"></a><a name="zh-cn_topic_0221482476_p1639185317419"></a>IAM用户所属账号信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row143898536410"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p13915533416"><a name="zh-cn_topic_0221482476_p13915533416"></a><a name="zh-cn_topic_0221482476_p13915533416"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p13391253948"><a name="zh-cn_topic_0221482476_p13391253948"></a><a name="zh-cn_topic_0221482476_p13391253948"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p7391453444"><a name="zh-cn_topic_0221482476_p7391453444"></a><a name="zh-cn_topic_0221482476_p7391453444"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p53911953744"><a name="zh-cn_topic_0221482476_p53911953744"></a><a name="zh-cn_topic_0221482476_p53911953744"></a>IAM用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row15389853944"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p1339275310414"><a name="zh-cn_topic_0221482476_p1339275310414"></a><a name="zh-cn_topic_0221482476_p1339275310414"></a>password</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p193922053941"><a name="zh-cn_topic_0221482476_p193922053941"></a><a name="zh-cn_topic_0221482476_p193922053941"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p339265320413"><a name="zh-cn_topic_0221482476_p339265320413"></a><a name="zh-cn_topic_0221482476_p339265320413"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p1439213531646"><a name="zh-cn_topic_0221482476_p1439213531646"></a><a name="zh-cn_topic_0221482476_p1439213531646"></a>IAM用户的登录密码。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  auth.identity.password.user.domain

<a name="zh-cn_topic_0221482476_request_Rq31AuthIdentityPwdUserDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row53923531146"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482476_p439319539411"><a name="zh-cn_topic_0221482476_p439319539411"></a><a name="zh-cn_topic_0221482476_p439319539411"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482476_p93937532418"><a name="zh-cn_topic_0221482476_p93937532418"></a><a name="zh-cn_topic_0221482476_p93937532418"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482476_p18393753548"><a name="zh-cn_topic_0221482476_p18393753548"></a><a name="zh-cn_topic_0221482476_p18393753548"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482476_p10393185312412"><a name="zh-cn_topic_0221482476_p10393185312412"></a><a name="zh-cn_topic_0221482476_p10393185312412"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row103921753048"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p139319531247"><a name="zh-cn_topic_0221482476_p139319531247"></a><a name="zh-cn_topic_0221482476_p139319531247"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p14393155317413"><a name="zh-cn_topic_0221482476_p14393155317413"></a><a name="zh-cn_topic_0221482476_p14393155317413"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p1039419531949"><a name="zh-cn_topic_0221482476_p1039419531949"></a><a name="zh-cn_topic_0221482476_p1039419531949"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p7394853545"><a name="zh-cn_topic_0221482476_p7394853545"></a><a name="zh-cn_topic_0221482476_p7394853545"></a>IAM用户所属账号名。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  auth.scope

<a name="zh-cn_topic_0221482476_request_Rq31AuthScope"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row193940531942"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482476_p203958531749"><a name="zh-cn_topic_0221482476_p203958531749"></a><a name="zh-cn_topic_0221482476_p203958531749"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482476_p03952535417"><a name="zh-cn_topic_0221482476_p03952535417"></a><a name="zh-cn_topic_0221482476_p03952535417"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482476_p7395155310413"><a name="zh-cn_topic_0221482476_p7395155310413"></a><a name="zh-cn_topic_0221482476_p7395155310413"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482476_p173953531646"><a name="zh-cn_topic_0221482476_p173953531646"></a><a name="zh-cn_topic_0221482476_p173953531646"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row139416531440"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p1539516533419"><a name="zh-cn_topic_0221482476_p1539516533419"></a><a name="zh-cn_topic_0221482476_p1539516533419"></a><a href="#zh-cn_topic_0221482476_request_Rq31AuthScopeDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p9395165315417"><a name="zh-cn_topic_0221482476_p9395165315417"></a><a name="zh-cn_topic_0221482476_p9395165315417"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p43961532044"><a name="zh-cn_topic_0221482476_p43961532044"></a><a name="zh-cn_topic_0221482476_p43961532044"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p193963531941"><a name="zh-cn_topic_0221482476_p193963531941"></a><a name="zh-cn_topic_0221482476_p193963531941"></a>取值为domain时，表示获取的token可以跨区域使用，domain支持id和name，二选一即可。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row639435316411"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p43964539410"><a name="zh-cn_topic_0221482476_p43964539410"></a><a name="zh-cn_topic_0221482476_p43964539410"></a><a href="#zh-cn_topic_0221482476_request_Rq31AuthScopeProject">project</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p1139618531545"><a name="zh-cn_topic_0221482476_p1139618531545"></a><a name="zh-cn_topic_0221482476_p1139618531545"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p339635317420"><a name="zh-cn_topic_0221482476_p339635317420"></a><a name="zh-cn_topic_0221482476_p339635317420"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p13979534417"><a name="zh-cn_topic_0221482476_p13979534417"></a><a name="zh-cn_topic_0221482476_p13979534417"></a>取值为project时，表示获取的token仅能访问指定project下的资源，project支持id和name，二选一即可。</p>
</td>
</tr>
</tbody>
</table>

**表 10**  auth.scope.domain

<a name="zh-cn_topic_0221482476_request_Rq31AuthScopeDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row13976538419"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482476_p23981353141"><a name="zh-cn_topic_0221482476_p23981353141"></a><a name="zh-cn_topic_0221482476_p23981353141"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482476_p1239814531144"><a name="zh-cn_topic_0221482476_p1239814531144"></a><a name="zh-cn_topic_0221482476_p1239814531144"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482476_p8398115313411"><a name="zh-cn_topic_0221482476_p8398115313411"></a><a name="zh-cn_topic_0221482476_p8398115313411"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482476_p739812535413"><a name="zh-cn_topic_0221482476_p739812535413"></a><a name="zh-cn_topic_0221482476_p739812535413"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row239775316411"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p1039818536411"><a name="zh-cn_topic_0221482476_p1039818536411"></a><a name="zh-cn_topic_0221482476_p1039818536411"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p1139813532411"><a name="zh-cn_topic_0221482476_p1139813532411"></a><a name="zh-cn_topic_0221482476_p1139813532411"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p939925318413"><a name="zh-cn_topic_0221482476_p939925318413"></a><a name="zh-cn_topic_0221482476_p939925318413"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p93991853947"><a name="zh-cn_topic_0221482476_p93991853947"></a><a name="zh-cn_topic_0221482476_p93991853947"></a>IAM用户所属账号ID，获取方式请参见：<a href="获取账号-IAM用户-项目-用户组-委托的名称和ID.md">获取账号、IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row139725314420"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p339955319413"><a name="zh-cn_topic_0221482476_p339955319413"></a><a name="zh-cn_topic_0221482476_p339955319413"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p1639920531841"><a name="zh-cn_topic_0221482476_p1639920531841"></a><a name="zh-cn_topic_0221482476_p1639920531841"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p14399165311418"><a name="zh-cn_topic_0221482476_p14399165311418"></a><a name="zh-cn_topic_0221482476_p14399165311418"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p19399165312413"><a name="zh-cn_topic_0221482476_p19399165312413"></a><a name="zh-cn_topic_0221482476_p19399165312413"></a>IAM用户所属账号名称，获取方式请参见：<a href="获取账号-IAM用户-项目-用户组-委托的名称和ID.md">获取账号、IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 11**  auth.scope.project

<a name="zh-cn_topic_0221482476_request_Rq31AuthScopeProject"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row2400195317412"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482476_p540095316412"><a name="zh-cn_topic_0221482476_p540095316412"></a><a name="zh-cn_topic_0221482476_p540095316412"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482476_p1440013538411"><a name="zh-cn_topic_0221482476_p1440013538411"></a><a name="zh-cn_topic_0221482476_p1440013538411"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482476_p104006531041"><a name="zh-cn_topic_0221482476_p104006531041"></a><a name="zh-cn_topic_0221482476_p104006531041"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482476_p54017531644"><a name="zh-cn_topic_0221482476_p54017531644"></a><a name="zh-cn_topic_0221482476_p54017531644"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row1040019531944"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p154019532415"><a name="zh-cn_topic_0221482476_p154019532415"></a><a name="zh-cn_topic_0221482476_p154019532415"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p640112531841"><a name="zh-cn_topic_0221482476_p640112531841"></a><a name="zh-cn_topic_0221482476_p640112531841"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p24012531649"><a name="zh-cn_topic_0221482476_p24012531649"></a><a name="zh-cn_topic_0221482476_p24012531649"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p204011553847"><a name="zh-cn_topic_0221482476_p204011553847"></a><a name="zh-cn_topic_0221482476_p204011553847"></a>IAM用户所属账号的项目ID，获取方式请参见：<a href="获取账号-IAM用户-项目-用户组-委托的名称和ID.md">获取账号、IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row140055320419"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482476_p1140165311414"><a name="zh-cn_topic_0221482476_p1140165311414"></a><a name="zh-cn_topic_0221482476_p1140165311414"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482476_p0402753744"><a name="zh-cn_topic_0221482476_p0402753744"></a><a name="zh-cn_topic_0221482476_p0402753744"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482476_p184026538418"><a name="zh-cn_topic_0221482476_p184026538418"></a><a name="zh-cn_topic_0221482476_p184026538418"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p1940275314412"><a name="zh-cn_topic_0221482476_p1940275314412"></a><a name="zh-cn_topic_0221482476_p1940275314412"></a>IAM用户所属账号的项目名称，获取方式请参见：<a href="获取账号-IAM用户-项目-用户组-委托的名称和ID.md">获取账号、IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482476_section20402185311418"></a>

**表 12**  响应Header参数

<a name="zh-cn_topic_0221482476_ResponseHeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row134025531244"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482476_p13403853843"><a name="zh-cn_topic_0221482476_p13403853843"></a><a name="zh-cn_topic_0221482476_p13403853843"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482476_p940313537414"><a name="zh-cn_topic_0221482476_p940313537414"></a><a name="zh-cn_topic_0221482476_p940313537414"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482476_p8403953444"><a name="zh-cn_topic_0221482476_p8403953444"></a><a name="zh-cn_topic_0221482476_p8403953444"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row1640211531541"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p240355319417"><a name="zh-cn_topic_0221482476_p240355319417"></a><a name="zh-cn_topic_0221482476_p240355319417"></a>X-Subject-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p84032535412"><a name="zh-cn_topic_0221482476_p84032535412"></a><a name="zh-cn_topic_0221482476_p84032535412"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p240312531542"><a name="zh-cn_topic_0221482476_p240312531542"></a><a name="zh-cn_topic_0221482476_p240312531542"></a>签名后的token。</p>
</td>
</tr>
</tbody>
</table>

**表 13**  响应Body参数

<a name="zh-cn_topic_0221482476_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row16404145315411"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482476_p340455319417"><a name="zh-cn_topic_0221482476_p340455319417"></a><a name="zh-cn_topic_0221482476_p340455319417"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482476_p16404195313412"><a name="zh-cn_topic_0221482476_p16404195313412"></a><a name="zh-cn_topic_0221482476_p16404195313412"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482476_p104051053447"><a name="zh-cn_topic_0221482476_p104051053447"></a><a name="zh-cn_topic_0221482476_p104051053447"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row340414531947"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p8405953146"><a name="zh-cn_topic_0221482476_p8405953146"></a><a name="zh-cn_topic_0221482476_p8405953146"></a><a href="#zh-cn_topic_0221482476_response_Rs31Token">token</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p104054531744"><a name="zh-cn_topic_0221482476_p104054531744"></a><a name="zh-cn_topic_0221482476_p104054531744"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p140595315411"><a name="zh-cn_topic_0221482476_p140595315411"></a><a name="zh-cn_topic_0221482476_p140595315411"></a>获取到的token信息。</p>
</td>
</tr>
</tbody>
</table>

**表 14**  token

<a name="zh-cn_topic_0221482476_response_Rs31Token"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row114051153446"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482476_p5406653243"><a name="zh-cn_topic_0221482476_p5406653243"></a><a name="zh-cn_topic_0221482476_p5406653243"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482476_p14065531547"><a name="zh-cn_topic_0221482476_p14065531547"></a><a name="zh-cn_topic_0221482476_p14065531547"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482476_p64065531840"><a name="zh-cn_topic_0221482476_p64065531840"></a><a name="zh-cn_topic_0221482476_p64065531840"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row1240565314417"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p1440715531244"><a name="zh-cn_topic_0221482476_p1440715531244"></a><a name="zh-cn_topic_0221482476_p1440715531244"></a><a href="#zh-cn_topic_0221482476_response_Rs31TokenCatalogArritem">catalog</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p34073531545"><a name="zh-cn_topic_0221482476_p34073531545"></a><a name="zh-cn_topic_0221482476_p34073531545"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p2040715532414"><a name="zh-cn_topic_0221482476_p2040715532414"></a><a name="zh-cn_topic_0221482476_p2040715532414"></a>服务目录信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row1840513531242"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p1240715531947"><a name="zh-cn_topic_0221482476_p1240715531947"></a><a name="zh-cn_topic_0221482476_p1240715531947"></a><a href="#zh-cn_topic_0221482476_response_Rs31TokenDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p194071653943"><a name="zh-cn_topic_0221482476_p194071653943"></a><a name="zh-cn_topic_0221482476_p194071653943"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p184071353849"><a name="zh-cn_topic_0221482476_p184071353849"></a><a name="zh-cn_topic_0221482476_p184071353849"></a>获取token的IAM用户所属的账号信息。如果获取token时请求体中scope参数设置为domain，则返回该字段。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row74065533416"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p140755318417"><a name="zh-cn_topic_0221482476_p140755318417"></a><a name="zh-cn_topic_0221482476_p140755318417"></a>expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1940816531349"><a name="zh-cn_topic_0221482476_p1940816531349"></a><a name="zh-cn_topic_0221482476_p1940816531349"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p840818534410"><a name="zh-cn_topic_0221482476_p840818534410"></a><a name="zh-cn_topic_0221482476_p840818534410"></a>token过期时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row174063534418"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p8408553347"><a name="zh-cn_topic_0221482476_p8408553347"></a><a name="zh-cn_topic_0221482476_p8408553347"></a>issued_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1440819531041"><a name="zh-cn_topic_0221482476_p1440819531041"></a><a name="zh-cn_topic_0221482476_p1440819531041"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p840819531843"><a name="zh-cn_topic_0221482476_p840819531843"></a><a name="zh-cn_topic_0221482476_p840819531843"></a>token下发时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row540635317411"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p174081531149"><a name="zh-cn_topic_0221482476_p174081531149"></a><a name="zh-cn_topic_0221482476_p174081531149"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p134083531644"><a name="zh-cn_topic_0221482476_p134083531644"></a><a name="zh-cn_topic_0221482476_p134083531644"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p12409195314416"><a name="zh-cn_topic_0221482476_p12409195314416"></a><a name="zh-cn_topic_0221482476_p12409195314416"></a>获取token的方式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row74062531149"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p1340915530412"><a name="zh-cn_topic_0221482476_p1340915530412"></a><a name="zh-cn_topic_0221482476_p1340915530412"></a><a href="#zh-cn_topic_0221482476_response_Rs31TokenProject">project</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1140935318419"><a name="zh-cn_topic_0221482476_p1140935318419"></a><a name="zh-cn_topic_0221482476_p1140935318419"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p164098531344"><a name="zh-cn_topic_0221482476_p164098531344"></a><a name="zh-cn_topic_0221482476_p164098531344"></a>获取token的IAM用户所属账号的项目信息。如果获取token时请求体中scope参数设置为project，则返回该字段。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row134061534410"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p14096533412"><a name="zh-cn_topic_0221482476_p14096533412"></a><a name="zh-cn_topic_0221482476_p14096533412"></a><a href="#zh-cn_topic_0221482476_response_Rs31TokenRolesArritem">roles</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1251185317418"><a name="zh-cn_topic_0221482476_p1251185317418"></a><a name="zh-cn_topic_0221482476_p1251185317418"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p1651120532414"><a name="zh-cn_topic_0221482476_p1651120532414"></a><a name="zh-cn_topic_0221482476_p1651120532414"></a>token的权限信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row1340605317420"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p15511105315418"><a name="zh-cn_topic_0221482476_p15511105315418"></a><a name="zh-cn_topic_0221482476_p15511105315418"></a><a href="#zh-cn_topic_0221482476_response_Rs31TokenUser">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1451120531442"><a name="zh-cn_topic_0221482476_p1451120531442"></a><a name="zh-cn_topic_0221482476_p1451120531442"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p165114531144"><a name="zh-cn_topic_0221482476_p165114531144"></a><a name="zh-cn_topic_0221482476_p165114531144"></a>获取token的IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 15**  token.catalog

<a name="zh-cn_topic_0221482476_response_Rs31TokenCatalogArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row84118531646"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482476_p1851105311415"><a name="zh-cn_topic_0221482476_p1851105311415"></a><a name="zh-cn_topic_0221482476_p1851105311415"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482476_p75115532416"><a name="zh-cn_topic_0221482476_p75115532416"></a><a name="zh-cn_topic_0221482476_p75115532416"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482476_p15119531749"><a name="zh-cn_topic_0221482476_p15119531749"></a><a name="zh-cn_topic_0221482476_p15119531749"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row174111853241"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p12511105319416"><a name="zh-cn_topic_0221482476_p12511105319416"></a><a name="zh-cn_topic_0221482476_p12511105319416"></a><a href="#zh-cn_topic_0221482476_response_Rs31TokenCatalogArritemEndpointsArritem">endpoints</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p851115531942"><a name="zh-cn_topic_0221482476_p851115531942"></a><a name="zh-cn_topic_0221482476_p851115531942"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p145116531142"><a name="zh-cn_topic_0221482476_p145116531142"></a><a name="zh-cn_topic_0221482476_p145116531142"></a>终端节点。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row6411195310413"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p1651225311417"><a name="zh-cn_topic_0221482476_p1651225311417"></a><a name="zh-cn_topic_0221482476_p1651225311417"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1051218533418"><a name="zh-cn_topic_0221482476_p1051218533418"></a><a name="zh-cn_topic_0221482476_p1051218533418"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p1151219531846"><a name="zh-cn_topic_0221482476_p1151219531846"></a><a name="zh-cn_topic_0221482476_p1151219531846"></a>服务ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row1641110536414"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p35126531241"><a name="zh-cn_topic_0221482476_p35126531241"></a><a name="zh-cn_topic_0221482476_p35126531241"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p8512853642"><a name="zh-cn_topic_0221482476_p8512853642"></a><a name="zh-cn_topic_0221482476_p8512853642"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p25128530414"><a name="zh-cn_topic_0221482476_p25128530414"></a><a name="zh-cn_topic_0221482476_p25128530414"></a>服务名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row341185319415"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p1351220539419"><a name="zh-cn_topic_0221482476_p1351220539419"></a><a name="zh-cn_topic_0221482476_p1351220539419"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p115128531743"><a name="zh-cn_topic_0221482476_p115128531743"></a><a name="zh-cn_topic_0221482476_p115128531743"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p15512153847"><a name="zh-cn_topic_0221482476_p15512153847"></a><a name="zh-cn_topic_0221482476_p15512153847"></a>该接口所属服务。</p>
</td>
</tr>
</tbody>
</table>

**表 16**  token.catalog.endpoints

<a name="zh-cn_topic_0221482476_response_Rs31TokenCatalogArritemEndpointsArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row641315535417"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482476_p175125531442"><a name="zh-cn_topic_0221482476_p175125531442"></a><a name="zh-cn_topic_0221482476_p175125531442"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482476_p1451255315415"><a name="zh-cn_topic_0221482476_p1451255315415"></a><a name="zh-cn_topic_0221482476_p1451255315415"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482476_p155121153444"><a name="zh-cn_topic_0221482476_p155121153444"></a><a name="zh-cn_topic_0221482476_p155121153444"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row6413155318419"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p2051255318410"><a name="zh-cn_topic_0221482476_p2051255318410"></a><a name="zh-cn_topic_0221482476_p2051255318410"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1251245310412"><a name="zh-cn_topic_0221482476_p1251245310412"></a><a name="zh-cn_topic_0221482476_p1251245310412"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p1851225316418"><a name="zh-cn_topic_0221482476_p1851225316418"></a><a name="zh-cn_topic_0221482476_p1851225316418"></a>终端节点ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row15413553243"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p2051216536411"><a name="zh-cn_topic_0221482476_p2051216536411"></a><a name="zh-cn_topic_0221482476_p2051216536411"></a>interface</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1651205317418"><a name="zh-cn_topic_0221482476_p1651205317418"></a><a name="zh-cn_topic_0221482476_p1651205317418"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p15122053845"><a name="zh-cn_topic_0221482476_p15122053845"></a><a name="zh-cn_topic_0221482476_p15122053845"></a>接口类型，描述接口在该终端节点的可见性。值为“public”，表示该接口为公开接口。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row9413753540"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p7512175313416"><a name="zh-cn_topic_0221482476_p7512175313416"></a><a name="zh-cn_topic_0221482476_p7512175313416"></a>region</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p251218536418"><a name="zh-cn_topic_0221482476_p251218536418"></a><a name="zh-cn_topic_0221482476_p251218536418"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p14512185310418"><a name="zh-cn_topic_0221482476_p14512185310418"></a><a name="zh-cn_topic_0221482476_p14512185310418"></a>终端节点所属区域。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row2413195318420"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p11512155317415"><a name="zh-cn_topic_0221482476_p11512155317415"></a><a name="zh-cn_topic_0221482476_p11512155317415"></a>region_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p55123531842"><a name="zh-cn_topic_0221482476_p55123531842"></a><a name="zh-cn_topic_0221482476_p55123531842"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p95126531349"><a name="zh-cn_topic_0221482476_p95126531349"></a><a name="zh-cn_topic_0221482476_p95126531349"></a>终端节点所属区域ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row541313532411"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p16512553542"><a name="zh-cn_topic_0221482476_p16512553542"></a><a name="zh-cn_topic_0221482476_p16512553542"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p12512175311419"><a name="zh-cn_topic_0221482476_p12512175311419"></a><a name="zh-cn_topic_0221482476_p12512175311419"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p11512125318418"><a name="zh-cn_topic_0221482476_p11512125318418"></a><a name="zh-cn_topic_0221482476_p11512125318418"></a>终端节点的URL。</p>
</td>
</tr>
</tbody>
</table>

**表 17**  token.domain

<a name="zh-cn_topic_0221482476_response_Rs31TokenDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row941617531743"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482476_p551212531145"><a name="zh-cn_topic_0221482476_p551212531145"></a><a name="zh-cn_topic_0221482476_p551212531145"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482476_p1951245319410"><a name="zh-cn_topic_0221482476_p1951245319410"></a><a name="zh-cn_topic_0221482476_p1951245319410"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482476_p25128534414"><a name="zh-cn_topic_0221482476_p25128534414"></a><a name="zh-cn_topic_0221482476_p25128534414"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row144161253346"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p95121453949"><a name="zh-cn_topic_0221482476_p95121453949"></a><a name="zh-cn_topic_0221482476_p95121453949"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p951216535412"><a name="zh-cn_topic_0221482476_p951216535412"></a><a name="zh-cn_topic_0221482476_p951216535412"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p1251214536413"><a name="zh-cn_topic_0221482476_p1251214536413"></a><a name="zh-cn_topic_0221482476_p1251214536413"></a>账号名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row18416135318413"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p85126531948"><a name="zh-cn_topic_0221482476_p85126531948"></a><a name="zh-cn_topic_0221482476_p85126531948"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1251285316414"><a name="zh-cn_topic_0221482476_p1251285316414"></a><a name="zh-cn_topic_0221482476_p1251285316414"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p05121553847"><a name="zh-cn_topic_0221482476_p05121553847"></a><a name="zh-cn_topic_0221482476_p05121553847"></a>账号ID。</p>
</td>
</tr>
</tbody>
</table>

**表 18**  token.project

<a name="zh-cn_topic_0221482476_response_Rs31TokenProject"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row14171253841"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482476_p1551215533411"><a name="zh-cn_topic_0221482476_p1551215533411"></a><a name="zh-cn_topic_0221482476_p1551215533411"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482476_p2512105313418"><a name="zh-cn_topic_0221482476_p2512105313418"></a><a name="zh-cn_topic_0221482476_p2512105313418"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482476_p051275314418"><a name="zh-cn_topic_0221482476_p051275314418"></a><a name="zh-cn_topic_0221482476_p051275314418"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row841718531946"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p1251214531412"><a name="zh-cn_topic_0221482476_p1251214531412"></a><a name="zh-cn_topic_0221482476_p1251214531412"></a><a href="#zh-cn_topic_0221482476_response_Rs31TokenProjectDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p16512195315420"><a name="zh-cn_topic_0221482476_p16512195315420"></a><a name="zh-cn_topic_0221482476_p16512195315420"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p165124536417"><a name="zh-cn_topic_0221482476_p165124536417"></a><a name="zh-cn_topic_0221482476_p165124536417"></a>项目所属账号信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row11418175318412"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p051219536414"><a name="zh-cn_topic_0221482476_p051219536414"></a><a name="zh-cn_topic_0221482476_p051219536414"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1513553843"><a name="zh-cn_topic_0221482476_p1513553843"></a><a name="zh-cn_topic_0221482476_p1513553843"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p2513115313413"><a name="zh-cn_topic_0221482476_p2513115313413"></a><a name="zh-cn_topic_0221482476_p2513115313413"></a>项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row74182532046"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p165131553141"><a name="zh-cn_topic_0221482476_p165131553141"></a><a name="zh-cn_topic_0221482476_p165131553141"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p165137539412"><a name="zh-cn_topic_0221482476_p165137539412"></a><a name="zh-cn_topic_0221482476_p165137539412"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p6513105316410"><a name="zh-cn_topic_0221482476_p6513105316410"></a><a name="zh-cn_topic_0221482476_p6513105316410"></a>项目名称。</p>
</td>
</tr>
</tbody>
</table>

**表 19**  token.project.domain

<a name="zh-cn_topic_0221482476_response_Rs31TokenProjectDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row7419205312412"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482476_p105139532414"><a name="zh-cn_topic_0221482476_p105139532414"></a><a name="zh-cn_topic_0221482476_p105139532414"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482476_p951355315420"><a name="zh-cn_topic_0221482476_p951355315420"></a><a name="zh-cn_topic_0221482476_p951355315420"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482476_p451312531547"><a name="zh-cn_topic_0221482476_p451312531547"></a><a name="zh-cn_topic_0221482476_p451312531547"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row64191953244"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p4513105312416"><a name="zh-cn_topic_0221482476_p4513105312416"></a><a name="zh-cn_topic_0221482476_p4513105312416"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p145136536411"><a name="zh-cn_topic_0221482476_p145136536411"></a><a name="zh-cn_topic_0221482476_p145136536411"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p75131953345"><a name="zh-cn_topic_0221482476_p75131953345"></a><a name="zh-cn_topic_0221482476_p75131953345"></a>账号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row144194531846"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p16513185316415"><a name="zh-cn_topic_0221482476_p16513185316415"></a><a name="zh-cn_topic_0221482476_p16513185316415"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p11513175311416"><a name="zh-cn_topic_0221482476_p11513175311416"></a><a name="zh-cn_topic_0221482476_p11513175311416"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p1251311538418"><a name="zh-cn_topic_0221482476_p1251311538418"></a><a name="zh-cn_topic_0221482476_p1251311538418"></a>账号名称。</p>
</td>
</tr>
</tbody>
</table>

**表 20**  token.roles

<a name="zh-cn_topic_0221482476_response_Rs31TokenRolesArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row194211953548"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482476_p1451317531248"><a name="zh-cn_topic_0221482476_p1451317531248"></a><a name="zh-cn_topic_0221482476_p1451317531248"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482476_p651316531644"><a name="zh-cn_topic_0221482476_p651316531644"></a><a name="zh-cn_topic_0221482476_p651316531644"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482476_p195131753341"><a name="zh-cn_topic_0221482476_p195131753341"></a><a name="zh-cn_topic_0221482476_p195131753341"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row142175312410"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p11513175313410"><a name="zh-cn_topic_0221482476_p11513175313410"></a><a name="zh-cn_topic_0221482476_p11513175313410"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p451385318413"><a name="zh-cn_topic_0221482476_p451385318413"></a><a name="zh-cn_topic_0221482476_p451385318413"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p1151311536413"><a name="zh-cn_topic_0221482476_p1151311536413"></a><a name="zh-cn_topic_0221482476_p1151311536413"></a>权限名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row11421453643"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p951315315412"><a name="zh-cn_topic_0221482476_p951315315412"></a><a name="zh-cn_topic_0221482476_p951315315412"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p115131553945"><a name="zh-cn_topic_0221482476_p115131553945"></a><a name="zh-cn_topic_0221482476_p115131553945"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p1451317531041"><a name="zh-cn_topic_0221482476_p1451317531041"></a><a name="zh-cn_topic_0221482476_p1451317531041"></a>权限ID。默认显示为0，非真实权限ID。</p>
</td>
</tr>
</tbody>
</table>

**表 21**  token.user

<a name="zh-cn_topic_0221482476_response_Rs31TokenUser"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row642375319413"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482476_p1151310534416"><a name="zh-cn_topic_0221482476_p1151310534416"></a><a name="zh-cn_topic_0221482476_p1151310534416"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482476_p851314532413"><a name="zh-cn_topic_0221482476_p851314532413"></a><a name="zh-cn_topic_0221482476_p851314532413"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482476_p16513185312413"><a name="zh-cn_topic_0221482476_p16513185312413"></a><a name="zh-cn_topic_0221482476_p16513185312413"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row34235532415"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p10513115311413"><a name="zh-cn_topic_0221482476_p10513115311413"></a><a name="zh-cn_topic_0221482476_p10513115311413"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1351395317414"><a name="zh-cn_topic_0221482476_p1351395317414"></a><a name="zh-cn_topic_0221482476_p1351395317414"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p105131531147"><a name="zh-cn_topic_0221482476_p105131531147"></a><a name="zh-cn_topic_0221482476_p105131531147"></a>IAM用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row2423153843"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p7513145319411"><a name="zh-cn_topic_0221482476_p7513145319411"></a><a name="zh-cn_topic_0221482476_p7513145319411"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1513353442"><a name="zh-cn_topic_0221482476_p1513353442"></a><a name="zh-cn_topic_0221482476_p1513353442"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p1151375310418"><a name="zh-cn_topic_0221482476_p1151375310418"></a><a name="zh-cn_topic_0221482476_p1151375310418"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row542310531345"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p8513105319419"><a name="zh-cn_topic_0221482476_p8513105319419"></a><a name="zh-cn_topic_0221482476_p8513105319419"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p1051316531745"><a name="zh-cn_topic_0221482476_p1051316531745"></a><a name="zh-cn_topic_0221482476_p1051316531745"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p7513105314410"><a name="zh-cn_topic_0221482476_p7513105314410"></a><a name="zh-cn_topic_0221482476_p7513105314410"></a>密码过期时间（UTC时间），“”表示密码不过期。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row942355312413"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p205131453441"><a name="zh-cn_topic_0221482476_p205131453441"></a><a name="zh-cn_topic_0221482476_p205131453441"></a><a href="#zh-cn_topic_0221482476_response_Rs31TokenUserDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p65131653746"><a name="zh-cn_topic_0221482476_p65131653746"></a><a name="zh-cn_topic_0221482476_p65131653746"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p851345310415"><a name="zh-cn_topic_0221482476_p851345310415"></a><a name="zh-cn_topic_0221482476_p851345310415"></a>IAM用户所属的账号信息。</p>
</td>
</tr>
</tbody>
</table>

**表 22**  token.user.domain

<a name="zh-cn_topic_0221482476_response_Rs31TokenUserDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row842635317414"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482476_p65137531345"><a name="zh-cn_topic_0221482476_p65137531345"></a><a name="zh-cn_topic_0221482476_p65137531345"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482476_p05131653843"><a name="zh-cn_topic_0221482476_p05131653843"></a><a name="zh-cn_topic_0221482476_p05131653843"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482476_p1151315532417"><a name="zh-cn_topic_0221482476_p1151315532417"></a><a name="zh-cn_topic_0221482476_p1151315532417"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row15426125312417"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p2051410531241"><a name="zh-cn_topic_0221482476_p2051410531241"></a><a name="zh-cn_topic_0221482476_p2051410531241"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p155144531848"><a name="zh-cn_topic_0221482476_p155144531848"></a><a name="zh-cn_topic_0221482476_p155144531848"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p05141853746"><a name="zh-cn_topic_0221482476_p05141853746"></a><a name="zh-cn_topic_0221482476_p05141853746"></a>IAM用户所属账号名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row94261653343"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482476_p115141253048"><a name="zh-cn_topic_0221482476_p115141253048"></a><a name="zh-cn_topic_0221482476_p115141253048"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482476_p45145531847"><a name="zh-cn_topic_0221482476_p45145531847"></a><a name="zh-cn_topic_0221482476_p45145531847"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482476_p1051419536411"><a name="zh-cn_topic_0221482476_p1051419536411"></a><a name="zh-cn_topic_0221482476_p1051419536411"></a>IAM用户所属账号ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482476_section1251410537412"></a>

-   获取IAM用户名为“IAMUser”，密码为“IAMPassword”，所属账号名为“IAMDomain”，作用范围为项目“cn-north-1”，且返回的响应体中将不显示catalog信息的token。

    ```
    POST https://iam.myhuaweicloud.com/v3/auth/tokens?nocatalog=true
    ```

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "password"
                ],
                "password": {
                    "user": {
                        "domain": {
                            "name": "IAMDomain"
                        },
                        "name": "IAMUser",
                        "password": "IAMPassword"
                    }
                }
            },
            "scope": {
                "project": {
                    "name": "cn-north-1"
                }
            }
        }
    }
    ```

-   获取IAM用户名为“IAMUser”，密码为“IAMPassword”，所属账号名为“IAMDomain”，作用范围为整个账号的token。

    ```
    POST https://iam.myhuaweicloud.com/v3/auth/tokens
    ```

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "password"
                ],
                "password": {
                    "user": {
                        "domain": {
                            "name": "IAMDomain"
                        },
                        "name": "IAMUser",
                        "password": "IAMPassword"
                    }
                }
            },
            "scope": {
                "domain": {
                    "name": "IAMDomain"
                }
            }
        }
    }
    ```


## 响应示例<a name="zh-cn_topic_0221482476_section451411531646"></a>

**状态码为 201 时:**

创建成功。

示例1：获取IAM用户名为“IAMUser”，密码为“IAMPassword”，所属账号名为“IAMDomain”，作用范围为项目“cn-north-1”，且返回的响应体中将不显示catalog信息的token。

示例2：获取IAM用户名为“IAMUser”，密码为“IAMPassword”，所属账号名为“IAMDomain”，作用范围为整个账号的token。

-   示例 1

    ```
    响应Header参数：
    X-Subject-Token:MIIatAYJKoZIhvcNAQcCoIIapTCCGqECAQExDTALB...
    ```

    ```
    响应Body参数：
    {
        "token": {
            "catalog": [],
            "expires_at": "2020-01-04T09:05:22.701000Z",
            "issued_at": "2020-01-03T09:05:22.701000Z",
            "methods": [
                "password"
            ],
            "project": {
                "domain": {
                    "id": "d78cbac186b744899480f25bd022f468",
                    "name": "IAMDomain"
                },
                "id": "aa2d97d7e62c4b7da3ffdfc11551f878",
                "name": "cn-north-1"
            },
            "roles": [
                {
                    "id": "0",
                    "name": "te_admin"
                },
                {
                    "id": "0",
                    "name": "op_gated_OBS_file_protocol"
                },
                {
                    "id": "0",
                    "name": "op_gated_Video_Campus"
                }
            ],
            "user": {
                "domain": {
                    "id": "d78cbac186b744899480f25bd022f468",
                    "name": "IAMDomain"
                },
                "id": "7116d09f88fa41908676fdd4b039e95b",
                "name": "IAMUser",
                "password_expires_at": ""
            }
        }
    }
    ```

-   示例 2

    ```
    响应Header参数：
    X-Subject-Token:MIIatAYJKoZIhvcNAQcCoIIapTCCGqECAQExDTALB...
    ```

    ```
    响应Body参数：
    {
        "token": {
            "catalog": [
                {
                    "endpoints": [
                        {
                            "id": "33e1cbdd86d34e89a63cf8ad16a5f49f",
                            "interface": "public",
                            "region": "*",
                            "region_id": "*",
                            "url": "https://iam.myhuaweicloud.com/v3.0"
                        }
                    ],
                    "id": "100a6a3477f1495286579b819d399e36",
                    "name": "iam",
                    "type": "iam"
                },
                {
                    "endpoints": [
                        {
                            "id": "29319cf2052d4e94bcf438b55d143832",
                            "interface": "public",
                            "region": "*",
                            "region_id": "*",
                            "url": "https://bss.myhuaweicloud.com/v1.0"
                        }
                    ],
                    "id": "c6db69fabbd549908adcb861c7e47ca4",
                    "name": "bssv1",
                    "type": "bssv1"
                }
            ],
            "domain": {
                "id": "d78cbac186b744899480f25bd022f468",
                "name": "IAMDomain"
            },
            "expires_at": "2020-01-04T09:08:49.965000Z",
            "issued_at": "2020-01-03T09:08:49.965000Z",
            "methods": [
                "password"
            ],
            "roles": [
                {
                    "id": "0",
                    "name": "te_admin"
                },
                {
                    "id": "0",
                    "name": "secu_admin"
                },
                {
                    "id": "0",
                    "name": "te_agency"
                }
            ],
            "user": {
                "domain": {
                    "id": "d78cbac186b744899480f25bd022f468",
                    "name": "IAMDomain"
                },
                "id": "7116d09f88fa41908676fdd4b039e95b",
                "name": "IAMUser",
                "password_expires_at": ""
            }
        }
    }
    ```


**状态码为 400 时:**

参数无效。

```
{
    "error": {
        "code": 400,
        "message": "The request body is invalid",
        "title": "Bad Request"
    }
}
```

**状态码为 401 时:**

认证失败。

```
{
    "error": {
        "code": 401,
        "message": "The username or password is wrong.",
        "title": "Unauthorized"
    }
}
```

## 返回值<a name="zh-cn_topic_0221482476_section195178534414"></a>

<a name="zh-cn_topic_0221482476_table2416"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482476_row14442353747"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482476_p1551718532043"><a name="zh-cn_topic_0221482476_p1551718532043"></a><a name="zh-cn_topic_0221482476_p1551718532043"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482476_p1451712535413"><a name="zh-cn_topic_0221482476_p1451712535413"></a><a name="zh-cn_topic_0221482476_p1451712535413"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482476_row2044255310413"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482476_p9517953446"><a name="zh-cn_topic_0221482476_p9517953446"></a><a name="zh-cn_topic_0221482476_p9517953446"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482476_p13517115312416"><a name="zh-cn_topic_0221482476_p13517115312416"></a><a name="zh-cn_topic_0221482476_p13517115312416"></a>创建成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row1644214537412"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482476_p145175530410"><a name="zh-cn_topic_0221482476_p145175530410"></a><a name="zh-cn_topic_0221482476_p145175530410"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482476_p75171053247"><a name="zh-cn_topic_0221482476_p75171053247"></a><a name="zh-cn_topic_0221482476_p75171053247"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row1644217531349"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482476_p155179531949"><a name="zh-cn_topic_0221482476_p155179531949"></a><a name="zh-cn_topic_0221482476_p155179531949"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482476_p175171853542"><a name="zh-cn_topic_0221482476_p175171853542"></a><a name="zh-cn_topic_0221482476_p175171853542"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row1944285318419"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482476_p185172531347"><a name="zh-cn_topic_0221482476_p185172531347"></a><a name="zh-cn_topic_0221482476_p185172531347"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482476_p135175531947"><a name="zh-cn_topic_0221482476_p135175531947"></a><a name="zh-cn_topic_0221482476_p135175531947"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row174421353544"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482476_p651715531249"><a name="zh-cn_topic_0221482476_p651715531249"></a><a name="zh-cn_topic_0221482476_p651715531249"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482476_p1451719531749"><a name="zh-cn_topic_0221482476_p1451719531749"></a><a name="zh-cn_topic_0221482476_p1451719531749"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row1844218532415"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482476_p115179539419"><a name="zh-cn_topic_0221482476_p115179539419"></a><a name="zh-cn_topic_0221482476_p115179539419"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482476_p551715532048"><a name="zh-cn_topic_0221482476_p551715532048"></a><a name="zh-cn_topic_0221482476_p551715532048"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482476_row174421553542"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482476_p55176532045"><a name="zh-cn_topic_0221482476_p55176532045"></a><a name="zh-cn_topic_0221482476_p55176532045"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482476_p551710531545"><a name="zh-cn_topic_0221482476_p551710531545"></a><a name="zh-cn_topic_0221482476_p551710531545"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482476_section18517105310420"></a>

无

