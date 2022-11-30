# 查询OpenID Connect身份提供商配置<a name="iam_13_0209"></a>

## 功能介绍<a name="section155844154423"></a>

该接口可以用于<u>[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)</u><u></u>  查询OpenID Connect身份提供商配置。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section2485151619141"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=ShowOpenIdConnectConfig)中调试该接口。

## URI<a name="section185871615134210"></a>

GET /v3.0/OS-FEDERATION/identity-providers/\{idp\_id\}/openid-connect-config

**表 1**  路径参数

<a name="table858951512424"></a>
<table><thead align="left"><tr id="row108151156429"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p20815315134215"><a name="p20815315134215"></a><a name="p20815315134215"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p1581581518420"><a name="p1581581518420"></a><a name="p1581581518420"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p581511574216"><a name="p581511574216"></a><a name="p581511574216"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p581551594211"><a name="p581551594211"></a><a name="p581551594211"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row3815131510427"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1181521514213"><a name="p1181521514213"></a><a name="p1181521514213"></a>idp_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p1081501516428"><a name="p1081501516428"></a><a name="p1081501516428"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p981511544215"><a name="p981511544215"></a><a name="p981511544215"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p481521511428"><a name="p481521511428"></a><a name="p481521511428"></a>身份提供商ID。</p>
<p id="p010713391029"><a name="p010713391029"></a><a name="p010713391029"></a>最小长度：1。最大长度：64。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="section3600215104218"></a>

**表 2**  请求Header参数

<a name="table17601315104214"></a>
<table><thead align="left"><tr id="row1981521516422"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p5815615154214"><a name="p5815615154214"></a><a name="p5815615154214"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p6815315184218"><a name="p6815315184218"></a><a name="p6815315184218"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1981591519423"><a name="p1981591519423"></a><a name="p1981591519423"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p12815181574213"><a name="p12815181574213"></a><a name="p12815181574213"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row14815915114210"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p581571512429"><a name="p581571512429"></a><a name="p581571512429"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p1381517156429"><a name="p1381517156429"></a><a name="p1381517156429"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1081521515421"><a name="p1081521515421"></a><a name="p1081521515421"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1381591516424"><a name="p1381591516424"></a><a name="p1381591516424"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="row1981518151423"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p8815131574219"><a name="p8815131574219"></a><a name="p8815131574219"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p11815171564219"><a name="p11815171564219"></a><a name="p11815171564219"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p188151915204212"><a name="p188151915204212"></a><a name="p188151915204212"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p081515154426"><a name="p081515154426"></a><a name="p081515154426"></a>请参见<a href="授权项.md">授权项</a>。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section761391511424"></a>

**状态码为 200 时:**

**表 3**  响应Body参数

<a name="table1615131514216"></a>
<table><thead align="left"><tr id="row5815201513425"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p2081541512426"><a name="p2081541512426"></a><a name="p2081541512426"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p88155151425"><a name="p88155151425"></a><a name="p88155151425"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p4815111513429"><a name="p4815111513429"></a><a name="p4815111513429"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row0815161516425"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p48158152426"><a name="p48158152426"></a><a name="p48158152426"></a><a href="#table106271415184212">openid_connect_config</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1781561516426"><a name="p1781561516426"></a><a name="p1781561516426"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p7815111524213"><a name="p7815111524213"></a><a name="p7815111524213"></a>OpenID Connect配置详情。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  OpenIDConnectConfig

<a name="table106271415184212"></a>
<table><thead align="left"><tr id="row158156159428"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p1815715194210"><a name="p1815715194210"></a><a name="p1815715194210"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p1281541554218"><a name="p1281541554218"></a><a name="p1281541554218"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1815515144219"><a name="p1815515144219"></a><a name="p1815515144219"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row281511554216"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p17815915114213"><a name="p17815915114213"></a><a name="p17815915114213"></a>access_mode</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p10815191574212"><a name="p10815191574212"></a><a name="p10815191574212"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p611593517328"><a name="p611593517328"></a><a name="p611593517328"></a>访问方式。</p>
<a name="ul1166237163218"></a><a name="ul1166237163218"></a><ul id="ul1166237163218"><li>program_console: 支持编程访问和管理控制台访问方式。</li><li>program: 支持编程访问方式</li></ul>
</td>
</tr>
<tr id="row198158157427"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1381561514219"><a name="p1381561514219"></a><a name="p1381561514219"></a>idp_url</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p138154151424"><a name="p138154151424"></a><a name="p138154151424"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1514462119318"><a name="p1514462119318"></a><a name="p1514462119318"></a>OpenID Connect身份提供商标识, 对应ID token 中 iss字段。</p>
</td>
</tr>
<tr id="row1481621514425"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p6816161511423"><a name="p6816161511423"></a><a name="p6816161511423"></a>client_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1816181574216"><a name="p1816181574216"></a><a name="p1816181574216"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p111454219316"><a name="p111454219316"></a><a name="p111454219316"></a>在OpenID Connect身份提供商注册的客户端ID。</p>
</td>
</tr>
<tr id="row1681681517424"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p20816161564210"><a name="p20816161564210"></a><a name="p20816161564210"></a>authorization_endpoint</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p188168157422"><a name="p188168157422"></a><a name="p188168157422"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1427416283317"><a name="p1427416283317"></a><a name="p1427416283317"></a>OpenID Connect身份提供商授权地址。</p>
<p id="p714514217312"><a name="p714514217312"></a><a name="p714514217312"></a><strong id="b1117016683311"><a name="b1117016683311"></a><a name="b1117016683311"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选</strong></p>
</td>
</tr>
<tr id="row3816141519424"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p981621574219"><a name="p981621574219"></a><a name="p981621574219"></a>scope</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p7816121512421"><a name="p7816121512421"></a><a name="p7816121512421"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1460272123315"><a name="p1460272123315"></a><a name="p1460272123315"></a>授权请求信息范围。</p>
<p id="p217382453312"><a name="p217382453312"></a><a name="p217382453312"></a><strong id="b0654172615333"><a name="b0654172615333"></a><a name="b0654172615333"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选。</strong></p>
<p id="p137881118173510"><a name="p137881118173510"></a><a name="p137881118173510"></a>枚举值：</p>
<a name="ul182672313510"></a><a name="ul182672313510"></a><ul id="ul182672313510"><li>openid</li><li>email</li><li>profile</li></ul>
<div class="note" id="note78171434125310"><a name="note78171434125310"></a><a name="note78171434125310"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul940272714014"></a><a name="ul940272714014"></a><ul id="ul940272714014"><li>此字段必选值“openid”。</li><li>最少1个值，最多10个值，之间使用空格分割。</li></ul>
<p id="p457525410018"><a name="p457525410018"></a><a name="p457525410018"></a>例如： "openid" 、"openid email"、 "openid profile"、 "openid email profile"。</p>
</div></div>
</td>
</tr>
<tr id="row681641518428"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p58161915124214"><a name="p58161915124214"></a><a name="p58161915124214"></a>response_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1781611155420"><a name="p1781611155420"></a><a name="p1781611155420"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1841811576348"><a name="p1841811576348"></a><a name="p1841811576348"></a>授权请求返回的类型。</p>
<p id="p15291049103419"><a name="p15291049103419"></a><a name="p15291049103419"></a><strong id="b15138452103414"><a name="b15138452103414"></a><a name="b15138452103414"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选</strong>。</p>
<p id="p3145192183119"><a name="p3145192183119"></a><a name="p3145192183119"></a>枚举值：</p>
<a name="ul71451221133119"></a><a name="ul71451221133119"></a><ul id="ul71451221133119"><li>id_token</li></ul>
</td>
</tr>
<tr id="row178161715124216"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p11816101518423"><a name="p11816101518423"></a><a name="p11816101518423"></a>response_mode</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p981613151427"><a name="p981613151427"></a><a name="p981613151427"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1155410285350"><a name="p1155410285350"></a><a name="p1155410285350"></a>授权请求返回方式。</p>
<p id="p914520214311"><a name="p914520214311"></a><a name="p914520214311"></a><strong id="b16519331113510"><a name="b16519331113510"></a><a name="b16519331113510"></a>编程访问和管理控制台访问方式必选，编程访问方式不可选。</strong></p>
<p id="p01451621113115"><a name="p01451621113115"></a><a name="p01451621113115"></a>枚举值：</p>
<a name="ul914502123116"></a><a name="ul914502123116"></a><ul id="ul914502123116"><li>fragment</li><li>form_post</li></ul>
</td>
</tr>
<tr id="row158161615124211"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p9816171519421"><a name="p9816171519421"></a><a name="p9816171519421"></a>signing_key</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1881611155422"><a name="p1881611155422"></a><a name="p1881611155422"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p414552115316"><a name="p414552115316"></a><a name="p414552115316"></a>OpenID Connect身份提供商ID Token签名的公钥。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section76561415104211"></a>

```
GET https://{address}/v3.0/OS-FEDERATION/identity-providers/{idp_id}/openid-connect-config
```

## 响应示例<a name="section196571215184212"></a>

**状态码为 200 时:**

创建成功。

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
  "error_msg" : "Request parameter %(key)s is invalid.", 
  "error_code" : "IAM.0007" 
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

## 状态码<a name="section14696415124219"></a>

<a name="table12697201511420"></a>
<table><thead align="left"><tr id="row16816151512424"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p6816415194211"><a name="p6816415194211"></a><a name="p6816415194211"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p9816171574220"><a name="p9816171574220"></a><a name="p9816171574220"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row118162151429"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p381631510426"><a name="p381631510426"></a><a name="p381631510426"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p11816315184217"><a name="p11816315184217"></a><a name="p11816315184217"></a>请求成功。</p>
</td>
</tr>
<tr id="row58168157424"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1081615152426"><a name="p1081615152426"></a><a name="p1081615152426"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p15816315154212"><a name="p15816315154212"></a><a name="p15816315154212"></a>参数无效。</p>
</td>
</tr>
<tr id="row118161415124212"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p88161015144215"><a name="p88161015144215"></a><a name="p88161015144215"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p981691514421"><a name="p981691514421"></a><a name="p981691514421"></a>认证失败。</p>
</td>
</tr>
<tr id="row14817151514420"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p15817141524213"><a name="p15817141524213"></a><a name="p15817141524213"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p18817121514423"><a name="p18817121514423"></a><a name="p18817121514423"></a>没有操作权限。</p>
</td>
</tr>
<tr id="row16817141594214"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1881714156424"><a name="p1881714156424"></a><a name="p1881714156424"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p178179151428"><a name="p178179151428"></a><a name="p178179151428"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="row58171915164216"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p14817171504218"><a name="p14817171504218"></a><a name="p14817171504218"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p11817171534219"><a name="p11817171534219"></a><a name="p11817171534219"></a>系统内部异常。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section157071615104215"></a>

请参见[错误码](错误码.md)。

