# 修改IAM用户的登录保护状态信息<a name="iam_08_0021"></a>

## 功能介绍<a name="section6273126173813"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)修改IAM用户的登录保护状态信息。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section1827692614384"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=UpdateLoginProtect)中调试该接口。

## URI<a name="section1427613263382"></a>

PUT /v3.0/OS-USER/users/\{user\_id\}/login-protect

**表 1**  路径参数

<a name="table10277192683817"></a>
<table><thead align="left"><tr id="row104101126103814"><th class="cellrowborder" valign="top" width="19.18%" id="mcps1.2.5.1.1"><p id="p74101126173819"><a name="p74101126173819"></a><a name="p74101126173819"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.9%" id="mcps1.2.5.1.2"><p id="p174102026153816"><a name="p174102026153816"></a><a name="p174102026153816"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="16.830000000000002%" id="mcps1.2.5.1.3"><p id="p144101026103813"><a name="p144101026103813"></a><a name="p144101026103813"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="53.09%" id="mcps1.2.5.1.4"><p id="p141082611381"><a name="p141082611381"></a><a name="p141082611381"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1841062610383"><td class="cellrowborder" valign="top" width="19.18%" headers="mcps1.2.5.1.1 "><p id="p841092611386"><a name="p841092611386"></a><a name="p841092611386"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10.9%" headers="mcps1.2.5.1.2 "><p id="p241013263383"><a name="p241013263383"></a><a name="p241013263383"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="16.830000000000002%" headers="mcps1.2.5.1.3 "><p id="p741032610381"><a name="p741032610381"></a><a name="p741032610381"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="53.09%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482404_p1141817101324"><a name="zh-cn_topic_0221482404_p1141817101324"></a><a name="zh-cn_topic_0221482404_p1141817101324"></a>待修改登录保护状态信息的IAM用户ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="section18284112614387"></a>

**表 2**  请求Header参数

<a name="table42843262380"></a>
<table><thead align="left"><tr id="row1141092614388"><th class="cellrowborder" valign="top" width="19.7%" id="mcps1.2.5.1.1"><p id="p4410192613815"><a name="p4410192613815"></a><a name="p4410192613815"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.459999999999999%" id="mcps1.2.5.1.2"><p id="p6410826123815"><a name="p6410826123815"></a><a name="p6410826123815"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="16.830000000000002%" id="mcps1.2.5.1.3"><p id="p194111826103812"><a name="p194111826103812"></a><a name="p194111826103812"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="53.010000000000005%" id="mcps1.2.5.1.4"><p id="p10411126143814"><a name="p10411126143814"></a><a name="p10411126143814"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1541132613383"><td class="cellrowborder" valign="top" width="19.7%" headers="mcps1.2.5.1.1 "><p id="p20411126123820"><a name="p20411126123820"></a><a name="p20411126123820"></a>X-Auth-token</p>
</td>
<td class="cellrowborder" valign="top" width="10.459999999999999%" headers="mcps1.2.5.1.2 "><p id="p1141172619385"><a name="p1141172619385"></a><a name="p1141172619385"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="16.830000000000002%" headers="mcps1.2.5.1.3 "><p id="p54111626123812"><a name="p54111626123812"></a><a name="p54111626123812"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="53.010000000000005%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482404_p1425111014328"><a name="zh-cn_topic_0221482404_p1425111014328"></a><a name="zh-cn_topic_0221482404_p1425111014328"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="table828862610381"></a>
<table><thead align="left"><tr id="row114114263388"><th class="cellrowborder" valign="top" width="20.05%" id="mcps1.2.5.1.1"><p id="p17411726123820"><a name="p17411726123820"></a><a name="p17411726123820"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.2%" id="mcps1.2.5.1.2"><p id="p174111426183812"><a name="p174111426183812"></a><a name="p174111426183812"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.09%" id="mcps1.2.5.1.3"><p id="p15411626163812"><a name="p15411626163812"></a><a name="p15411626163812"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.66%" id="mcps1.2.5.1.4"><p id="p6411192612383"><a name="p6411192612383"></a><a name="p6411192612383"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row12411826143812"><td class="cellrowborder" valign="top" width="20.05%" headers="mcps1.2.5.1.1 "><p id="p17411182643813"><a name="p17411182643813"></a><a name="p17411182643813"></a><a href="#table14291172683815">login_protect</a></p>
</td>
<td class="cellrowborder" valign="top" width="10.2%" headers="mcps1.2.5.1.2 "><p id="p20411172619386"><a name="p20411172619386"></a><a name="p20411172619386"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.09%" headers="mcps1.2.5.1.3 "><p id="p04111026173811"><a name="p04111026173811"></a><a name="p04111026173811"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="52.66%" headers="mcps1.2.5.1.4 "><p id="p124111026173817"><a name="p124111026173817"></a><a name="p124111026173817"></a>登录保护状态信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  Login\_project

<a name="table14291172683815"></a>
<table><thead align="left"><tr id="row11411626133814"><th class="cellrowborder" valign="top" width="20.23%" id="mcps1.2.5.1.1"><p id="p34111526103811"><a name="p34111526103811"></a><a name="p34111526103811"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.94%" id="mcps1.2.5.1.2"><p id="p3411132615389"><a name="p3411132615389"></a><a name="p3411132615389"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="17.52%" id="mcps1.2.5.1.3"><p id="p941162673817"><a name="p941162673817"></a><a name="p941162673817"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="52.31%" id="mcps1.2.5.1.4"><p id="p641162618382"><a name="p641162618382"></a><a name="p641162618382"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1641192693814"><td class="cellrowborder" valign="top" width="20.23%" headers="mcps1.2.5.1.1 "><p id="p0411142653811"><a name="p0411142653811"></a><a name="p0411142653811"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="9.94%" headers="mcps1.2.5.1.2 "><p id="p5411126193814"><a name="p5411126193814"></a><a name="p5411126193814"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.52%" headers="mcps1.2.5.1.3 "><p id="p341102611384"><a name="p341102611384"></a><a name="p341102611384"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="52.31%" headers="mcps1.2.5.1.4 "><p id="p35197507377"><a name="p35197507377"></a><a name="p35197507377"></a>IAM用户是否开启登录保护，开启为"true"，未开启为"false"。</p>
</td>
</tr>
<tr id="row10411112693816"><td class="cellrowborder" valign="top" width="20.23%" headers="mcps1.2.5.1.1 "><p id="p441162610389"><a name="p441162610389"></a><a name="p441162610389"></a>verification_method</p>
</td>
<td class="cellrowborder" valign="top" width="9.94%" headers="mcps1.2.5.1.2 "><p id="p15411726103817"><a name="p15411726103817"></a><a name="p15411726103817"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="17.52%" headers="mcps1.2.5.1.3 "><p id="p174115262382"><a name="p174115262382"></a><a name="p174115262382"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="52.31%" headers="mcps1.2.5.1.4 "><p id="p1411112614384"><a name="p1411112614384"></a><a name="p1411112614384"></a>IAM用户登录验证方式。手机验证为“sms”,邮箱验证为“email”,MFA验证为“vmfa”。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section629419260382"></a>

**状态码为 200 时：**

**表 5**  响应Body参数

<a name="table12295152616381"></a>
<table><thead align="left"><tr id="row9411132618385"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p194121126153817"><a name="p194121126153817"></a><a name="p194121126153817"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p6412152613388"><a name="p6412152613388"></a><a name="p6412152613388"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p5412112633813"><a name="p5412112633813"></a><a name="p5412112633813"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row141213266387"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p18412182653810"><a name="p18412182653810"></a><a name="p18412182653810"></a><a href="#table13297726203815">login_protect</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p2412152610389"><a name="p2412152610389"></a><a name="p2412152610389"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p13412152613816"><a name="p13412152613816"></a><a name="p13412152613816"></a>登录保护状态信息。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  login\_protect

<a name="table13297726203815"></a>
<table><thead align="left"><tr id="row104121626173811"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p124123262386"><a name="p124123262386"></a><a name="p124123262386"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p14412102614384"><a name="p14412102614384"></a><a name="p14412102614384"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1041214268381"><a name="p1041214268381"></a><a name="p1041214268381"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row19412192611382"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1341232613819"><a name="p1341232613819"></a><a name="p1341232613819"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p941292683812"><a name="p941292683812"></a><a name="p941292683812"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p242423014138"><a name="p242423014138"></a><a name="p242423014138"></a>待修改登录保护状态信息的IAM用户ID。</p>
</td>
</tr>
<tr id="row14121526193817"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p741222614383"><a name="p741222614383"></a><a name="p741222614383"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p144121265387"><a name="p144121265387"></a><a name="p144121265387"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p941114010137"><a name="p941114010137"></a><a name="p941114010137"></a>IAM用户是否开启登录保护，开启为"true"，不开启为"false"。</p>
</td>
</tr>
<tr id="row9412926163816"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p164124263383"><a name="p164124263383"></a><a name="p164124263383"></a>verification_method</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p84123262388"><a name="p84123262388"></a><a name="p84123262388"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p8411240121317"><a name="p8411240121317"></a><a name="p8411240121317"></a>IAM用户登录验证方式。手机验证为“sms”,邮箱验证为“email”,MFA验证为“vmfa”。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section11300926163818"></a>

```
PUT https://iam.myhuaweicloud.com/v3.0/OS-USER/users/{user_id}/login-protect
 
{ 
  "login_protect" : { 
    "enabled" : true, 
    "verification_method" : "vmfa" 
  } 
}
```

## 响应示例<a name="section1130262653820"></a>

**状态码：200**

请求成功。

```
{ 
  "login_protect" : { 
    "user_id": "16b26081f43d4c628c4bb88cf32e9...", 
    "enabled" : true, 
    "verification_method" : "vmfa" 
  } 
}
```

## 状态码<a name="section1830292623813"></a>

<a name="table1930214265381"></a>
<table><thead align="left"><tr id="row174121526153813"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p11412202614386"><a name="p11412202614386"></a><a name="p11412202614386"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p104121226133816"><a name="p104121226133816"></a><a name="p104121226133816"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6412112611387"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p631612369531"><a name="p631612369531"></a><a name="p631612369531"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p143161363537"><a name="p143161363537"></a><a name="p143161363537"></a>请求成功。</p>
</td>
</tr>
<tr id="row1415616282535"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1231615362535"><a name="p1231615362535"></a><a name="p1231615362535"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p53163363535"><a name="p53163363535"></a><a name="p53163363535"></a>请求校验异常。</p>
</td>
</tr>
<tr id="row145275353104"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p125271335151013"><a name="p125271335151013"></a><a name="p125271335151013"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p124389433103"><a name="p124389433103"></a><a name="p124389433103"></a>认证失败。</p>
</td>
</tr>
<tr id="row19763163010531"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p13165361534"><a name="p13165361534"></a><a name="p13165361534"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p1131663635310"><a name="p1131663635310"></a><a name="p1131663635310"></a>请求未授权。</p>
</td>
</tr>
<tr id="row4899185514013"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p4900125513015"><a name="p4900125513015"></a><a name="p4900125513015"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p18900855108"><a name="p18900855108"></a><a name="p18900855108"></a><span>未找到相应的资源。</span></p>
</td>
</tr>
<tr id="row7763113075317"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p12316336105313"><a name="p12316336105313"></a><a name="p12316336105313"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p16316113612532"><a name="p16316113612532"></a><a name="p16316113612532"></a>系统错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section103041226173814"></a>

请参见[错误码](错误码.md)。

