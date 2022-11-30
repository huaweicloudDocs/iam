# 获取IAM用户Token（使用密码+虚拟MFA）<a name="iam_03_0006"></a>

## 功能介绍<a name="zh-cn_topic_0221482385_section365913610201"></a>

该接口可以用于**通过用户名/密码+虚拟MFA**的方式进行认证，在IAM用户**开启了的登录保护功能，并选择通过虚拟MFA验证时**获取IAM用户Token。Token是系统颁发给用户的访问令牌，承载用户的身份、权限等信息。调用IAM以及其他云服务的接口时，可以使用本接口获取的Token进行鉴权。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

接口使用导航：

[IAM用户获取Token](#li195948474711)

[判断当前帐号是华为帐号还是华为云帐号](#li1259418424719)

[华为帐号获取Token](#li459416444716)

[华为云帐号获取Token](#li1559494164710)

[第三方系统用户获取Token](#li39831231144816)

[Token有效期说明](#li1959414494712)

[获取Token常见问题](#li14578141615014)

[其他相关操作](#li1997694715497)

-   <a name="li195948474711"></a>**IAM用户获取Token**

    无特殊要求，请按照[请求参数](#zh-cn_topic_0221482385_section15662126152010)说明获取Token。

-   <a name="li1259418424719"></a>**判断当前帐号是华为帐号还是华为云帐号**

    华为帐号不支持直接获取帐号Token，排查是否为华为帐号请参见：[怎么知道当前登录华为云使用的是“华为帐号” 还是“华为云账号”？](https://support.huaweicloud.com/account_faq/faq_id_0009.html)

-   <a name="li459416444716"></a>**华为帐号获取Token**

    华为账号获取token请参加以下步骤：[创建一个IAM用户](https://support.huaweicloud.com/usermanual-iam/iam_02_0001.html)，[授予该用户必要的权限](https://support.huaweicloud.com/usermanual-iam/iam_03_0001.html)，使用创建的IAM用户，获取IAM用户Token。

-   <a name="li1559494164710"></a>**华为云帐号获取Token**

    无特殊要求，请按照[请求参数](#zh-cn_topic_0221482385_section15662126152010)说明获取Token。

-   <a name="li39831231144816"></a>**第三方系统用户获取Token**

    如果您是第三方系统用户，直接使用联邦认证的用户名和密码获取Token，系统会提示密码错误。请先在华为云的登录页面，通过“忘记密码”功能，设置**华为云帐号密码**。

-   <a name="li1959414494712"></a>**Token有效期说明**
    -   Token的有效期为**24小时**。建议进行缓存，避免频繁调用。使用Token前请确保Token离过期有足够的时间，防止调用API的过程中Token过期导致调用API失败。重新获取Token，不影响已有Token有效性。
    -   如果在Token有效期内进行如下操作，**当前Token将立即失效。**
        -   删除/停用IAM用户。
        -   修改IAM用户密码、访问密钥。
        -   IAM用户权限发生变化（如帐号欠费无法访问云服务、申请公测通过、IAM用户权限被修改等）。

    -   使用Token调用云服务API时， 返回“**The token must be updated**”，则Token过期，需要客户端重新获取Token。

-   <a name="li14578141615014"></a>**获取Token常见问题**

    用户名或密码错误：请排查输入的用户名和密码是否正确。用户名密码正确但是仍旧报错，请排查[当前获取Token的帐号是否为华为帐号](#li1259418424719)，华为帐号不支持直接获取Token，请新建IAM用户并授权，使用IAM用户获取Token。

    没有API访问权限：调用API前，请确保已[开启编程访问](https://support.huaweicloud.com/usermanual-iam/iam_02_0002.html#section0)。


-   <a name="li1997694715497"></a>**相关操作**
    -   如果需要获取具有Security Administrator权限的Token，请参见：[如何获取Security Administrator权限的Token](https://support.huaweicloud.com/iam_faq/iam_01_0608.html)。
    -   通过Postman获取用户Token示例请参见：[如何通过Postman获取用户Token](https://support.huaweicloud.com/iam_faq/iam_01_034.html)。


## 调试<a name="section4819151065317"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneCreateUserTokenByPasswordAndMfa)中调试该接口。

## URI<a name="zh-cn_topic_0221482385_section20660262206"></a>

POST /v3/auth/tokens

**表 1**  Query参数

<a name="zh-cn_topic_0221482385_table166116614206"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row26614618203"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p1966196192018"><a name="zh-cn_topic_0221482385_p1966196192018"></a><a name="zh-cn_topic_0221482385_p1966196192018"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p1166119662017"><a name="zh-cn_topic_0221482385_p1166119662017"></a><a name="zh-cn_topic_0221482385_p1166119662017"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p16662661205"><a name="zh-cn_topic_0221482385_p16662661205"></a><a name="zh-cn_topic_0221482385_p16662661205"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p1666211612204"><a name="zh-cn_topic_0221482385_p1666211612204"></a><a name="zh-cn_topic_0221482385_p1666211612204"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row26618652012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p1666214616202"><a name="zh-cn_topic_0221482385_p1666214616202"></a><a name="zh-cn_topic_0221482385_p1666214616202"></a>nocatalog</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p116627618205"><a name="zh-cn_topic_0221482385_p116627618205"></a><a name="zh-cn_topic_0221482385_p116627618205"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p146620672020"><a name="zh-cn_topic_0221482385_p146620672020"></a><a name="zh-cn_topic_0221482385_p146620672020"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p176621662202"><a name="zh-cn_topic_0221482385_p176621662202"></a><a name="zh-cn_topic_0221482385_p176621662202"></a>如果设置该参数，返回的响应体中将不显示catalog信息。任何非空字符串都将解释为true，并使该字段生效。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482385_section15662126152010"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482385_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row9663262206"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p1166317652010"><a name="zh-cn_topic_0221482385_p1166317652010"></a><a name="zh-cn_topic_0221482385_p1166317652010"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p56636620202"><a name="zh-cn_topic_0221482385_p56636620202"></a><a name="zh-cn_topic_0221482385_p56636620202"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p1666317612011"><a name="zh-cn_topic_0221482385_p1666317612011"></a><a name="zh-cn_topic_0221482385_p1666317612011"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p666456102011"><a name="zh-cn_topic_0221482385_p666456102011"></a><a name="zh-cn_topic_0221482385_p666456102011"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row146631467202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p966410622011"><a name="zh-cn_topic_0221482385_p966410622011"></a><a name="zh-cn_topic_0221482385_p966410622011"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p16641063202"><a name="zh-cn_topic_0221482385_p16641063202"></a><a name="zh-cn_topic_0221482385_p16641063202"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p26648617206"><a name="zh-cn_topic_0221482385_p26648617206"></a><a name="zh-cn_topic_0221482385_p26648617206"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p1366412662013"><a name="zh-cn_topic_0221482385_p1366412662013"></a><a name="zh-cn_topic_0221482385_p1366412662013"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="zh-cn_topic_0221482385_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row66656652011"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p156650610205"><a name="zh-cn_topic_0221482385_p156650610205"></a><a name="zh-cn_topic_0221482385_p156650610205"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p166656692013"><a name="zh-cn_topic_0221482385_p166656692013"></a><a name="zh-cn_topic_0221482385_p166656692013"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p86669616204"><a name="zh-cn_topic_0221482385_p86669616204"></a><a name="zh-cn_topic_0221482385_p86669616204"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p14666563203"><a name="zh-cn_topic_0221482385_p14666563203"></a><a name="zh-cn_topic_0221482385_p14666563203"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row76654616209"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p76667622010"><a name="zh-cn_topic_0221482385_p76667622010"></a><a name="zh-cn_topic_0221482385_p76667622010"></a><a href="#zh-cn_topic_0221482385_request_Rq3100Auth">auth</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p1466612617202"><a name="zh-cn_topic_0221482385_p1466612617202"></a><a name="zh-cn_topic_0221482385_p1466612617202"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p466626202011"><a name="zh-cn_topic_0221482385_p466626202011"></a><a name="zh-cn_topic_0221482385_p466626202011"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p106667662015"><a name="zh-cn_topic_0221482385_p106667662015"></a><a name="zh-cn_topic_0221482385_p106667662015"></a>认证信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  auth

<a name="zh-cn_topic_0221482385_request_Rq3100Auth"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row16667136142013"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p136673632017"><a name="zh-cn_topic_0221482385_p136673632017"></a><a name="zh-cn_topic_0221482385_p136673632017"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p166685617201"><a name="zh-cn_topic_0221482385_p166685617201"></a><a name="zh-cn_topic_0221482385_p166685617201"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p17668106142014"><a name="zh-cn_topic_0221482385_p17668106142014"></a><a name="zh-cn_topic_0221482385_p17668106142014"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p0668196112020"><a name="zh-cn_topic_0221482385_p0668196112020"></a><a name="zh-cn_topic_0221482385_p0668196112020"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row76671162202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p12668164201"><a name="zh-cn_topic_0221482385_p12668164201"></a><a name="zh-cn_topic_0221482385_p12668164201"></a><a href="#zh-cn_topic_0221482385_request_Rq3100AuthIdentity">identity</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p966812642018"><a name="zh-cn_topic_0221482385_p966812642018"></a><a name="zh-cn_topic_0221482385_p966812642018"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p1668186132010"><a name="zh-cn_topic_0221482385_p1668186132010"></a><a name="zh-cn_topic_0221482385_p1668186132010"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p96681369202"><a name="zh-cn_topic_0221482385_p96681369202"></a><a name="zh-cn_topic_0221482385_p96681369202"></a>认证参数。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row1667176122016"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p16691564204"><a name="zh-cn_topic_0221482385_p16691564204"></a><a name="zh-cn_topic_0221482385_p16691564204"></a><a href="#zh-cn_topic_0221482385_request_Rq31AuthScope">scope</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p206695615205"><a name="zh-cn_topic_0221482385_p206695615205"></a><a name="zh-cn_topic_0221482385_p206695615205"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p466910617206"><a name="zh-cn_topic_0221482385_p466910617206"></a><a name="zh-cn_topic_0221482385_p466910617206"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p2669666201"><a name="zh-cn_topic_0221482385_p2669666201"></a><a name="zh-cn_topic_0221482385_p2669666201"></a>Token的使用范围，取值为project或domain，二选一即可。</p>
<div class="note" id="zh-cn_topic_0221482385_note96691665204"><a name="zh-cn_topic_0221482385_note96691665204"></a><a name="zh-cn_topic_0221482385_note96691665204"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul5202151812299"></a><a name="ul5202151812299"></a><ul id="ul5202151812299"><li><strong id="b019019355911"><a name="b019019355911"></a><a name="b019019355911"></a>如果您将scope设置为domain，该Token适用于全局级服务；如果将scope设置为project，该Token适用于项目级服务。</strong></li><li><strong id="b1619683514911"><a name="b1619683514911"></a><a name="b1619683514911"></a>如果您将scope同时设置为project和domain，将以project参数为准，获取到项目级服务的Token。</strong></li><li><strong id="b517718469334"><a name="b517718469334"></a><a name="b517718469334"></a>如果您将scope置空，将获取到全局级服务的Token。建议您按需要填写Token使用范围。</strong></li></ul>
</div></div>
</td>
</tr>
</tbody>
</table>

**表 5**  auth.identity

<a name="zh-cn_topic_0221482385_request_Rq3100AuthIdentity"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row13670266202"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p1267013662013"><a name="zh-cn_topic_0221482385_p1267013662013"></a><a name="zh-cn_topic_0221482385_p1267013662013"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p1767086162013"><a name="zh-cn_topic_0221482385_p1767086162013"></a><a name="zh-cn_topic_0221482385_p1767086162013"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p1767015615209"><a name="zh-cn_topic_0221482385_p1767015615209"></a><a name="zh-cn_topic_0221482385_p1767015615209"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p767015611204"><a name="zh-cn_topic_0221482385_p767015611204"></a><a name="zh-cn_topic_0221482385_p767015611204"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row1670116112012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p567115613208"><a name="zh-cn_topic_0221482385_p567115613208"></a><a name="zh-cn_topic_0221482385_p567115613208"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p567120614202"><a name="zh-cn_topic_0221482385_p567120614202"></a><a name="zh-cn_topic_0221482385_p567120614202"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p267113662017"><a name="zh-cn_topic_0221482385_p267113662017"></a><a name="zh-cn_topic_0221482385_p267113662017"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p167114662013"><a name="zh-cn_topic_0221482385_p167114662013"></a><a name="zh-cn_topic_0221482385_p167114662013"></a>认证方法，该字段内容为["password", "totp"]。</p>
<p id="zh-cn_topic_0221482385_p967186172017"><a name="zh-cn_topic_0221482385_p967186172017"></a><a name="zh-cn_topic_0221482385_p967186172017"></a>取值范围：</p>
<a name="zh-cn_topic_0221482385_ul1867110613208"></a><a name="zh-cn_topic_0221482385_ul1867110613208"></a><ul id="zh-cn_topic_0221482385_ul1867110613208"><li>password</li><li>totp</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row1667011682016"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p86717632016"><a name="zh-cn_topic_0221482385_p86717632016"></a><a name="zh-cn_topic_0221482385_p86717632016"></a><a href="#zh-cn_topic_0221482385_request_Rq31AuthIdentityPwd">password</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p18672262207"><a name="zh-cn_topic_0221482385_p18672262207"></a><a name="zh-cn_topic_0221482385_p18672262207"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p467215692014"><a name="zh-cn_topic_0221482385_p467215692014"></a><a name="zh-cn_topic_0221482385_p467215692014"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p467217612209"><a name="zh-cn_topic_0221482385_p467217612209"></a><a name="zh-cn_topic_0221482385_p467217612209"></a>用户密码认证信息。</p>
<div class="note" id="zh-cn_topic_0221482385_note767219614205"><a name="zh-cn_topic_0221482385_note767219614205"></a><a name="zh-cn_topic_0221482385_note767219614205"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0221482385_ul1867212612011"></a><a name="zh-cn_topic_0221482385_ul1867212612011"></a><ul id="zh-cn_topic_0221482385_ul1867212612011"><li>user.name和user.domain.name可以在界面控制台“我的凭证”中查看，具体获取方法请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</li><li>该接口提供了锁定机制用于防止暴力破解，调用时，请确保用户名密码正确，输错一定次数（<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>可设置该规则，方法请参见：<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0704.html" target="_blank" rel="noopener noreferrer">帐号锁定策略</a>）将被锁定。</li></ul>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row86702616200"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p767316615206"><a name="zh-cn_topic_0221482385_p767316615206"></a><a name="zh-cn_topic_0221482385_p767316615206"></a><a href="#zh-cn_topic_0221482385_request_Rq3100AuthIdentityTotp">totp</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p667396152015"><a name="zh-cn_topic_0221482385_p667396152015"></a><a name="zh-cn_topic_0221482385_p667396152015"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p116739613207"><a name="zh-cn_topic_0221482385_p116739613207"></a><a name="zh-cn_topic_0221482385_p116739613207"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p1567319612016"><a name="zh-cn_topic_0221482385_p1567319612016"></a><a name="zh-cn_topic_0221482385_p1567319612016"></a>totp认证信息，仅在您已开启虚拟MFA方式的登录保护功能时需要填写该参数。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  auth.identity.password

<a name="zh-cn_topic_0221482385_request_Rq31AuthIdentityPwd"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row367346132019"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p46746619209"><a name="zh-cn_topic_0221482385_p46746619209"></a><a name="zh-cn_topic_0221482385_p46746619209"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p12674564207"><a name="zh-cn_topic_0221482385_p12674564207"></a><a name="zh-cn_topic_0221482385_p12674564207"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p26741366206"><a name="zh-cn_topic_0221482385_p26741366206"></a><a name="zh-cn_topic_0221482385_p26741366206"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p17674966206"><a name="zh-cn_topic_0221482385_p17674966206"></a><a name="zh-cn_topic_0221482385_p17674966206"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row156732611208"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p8674365200"><a name="zh-cn_topic_0221482385_p8674365200"></a><a name="zh-cn_topic_0221482385_p8674365200"></a><a href="#zh-cn_topic_0221482385_request_Rq31AuthIdentityPwdUser">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p0674206192014"><a name="zh-cn_topic_0221482385_p0674206192014"></a><a name="zh-cn_topic_0221482385_p0674206192014"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p12675462207"><a name="zh-cn_topic_0221482385_p12675462207"></a><a name="zh-cn_topic_0221482385_p12675462207"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p146753619204"><a name="zh-cn_topic_0221482385_p146753619204"></a><a name="zh-cn_topic_0221482385_p146753619204"></a>需要获取Token的IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  auth.identity.password.user

<a name="zh-cn_topic_0221482385_request_Rq31AuthIdentityPwdUser"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row1667506172018"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p166764618201"><a name="zh-cn_topic_0221482385_p166764618201"></a><a name="zh-cn_topic_0221482385_p166764618201"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p767618611209"><a name="zh-cn_topic_0221482385_p767618611209"></a><a name="zh-cn_topic_0221482385_p767618611209"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p46767652010"><a name="zh-cn_topic_0221482385_p46767652010"></a><a name="zh-cn_topic_0221482385_p46767652010"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p14676186172014"><a name="zh-cn_topic_0221482385_p14676186172014"></a><a name="zh-cn_topic_0221482385_p14676186172014"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row1467510662013"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p16676963204"><a name="zh-cn_topic_0221482385_p16676963204"></a><a name="zh-cn_topic_0221482385_p16676963204"></a><a href="#zh-cn_topic_0221482385_request_Rq31AuthIdentityPwdUserDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p7676116122014"><a name="zh-cn_topic_0221482385_p7676116122014"></a><a name="zh-cn_topic_0221482385_p7676116122014"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p267617620207"><a name="zh-cn_topic_0221482385_p267617620207"></a><a name="zh-cn_topic_0221482385_p267617620207"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p167715611205"><a name="zh-cn_topic_0221482385_p167715611205"></a><a name="zh-cn_topic_0221482385_p167715611205"></a>IAM用户所属帐号信息。了解<a href="https://support.huaweicloud.com/productdesc-iam/iam_01_0023.html#section2" target="_blank" rel="noopener noreferrer">帐号与IAM用户的关系</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row967514672017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p20677186132013"><a name="zh-cn_topic_0221482385_p20677186132013"></a><a name="zh-cn_topic_0221482385_p20677186132013"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p9677126162016"><a name="zh-cn_topic_0221482385_p9677126162016"></a><a name="zh-cn_topic_0221482385_p9677126162016"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p116770672020"><a name="zh-cn_topic_0221482385_p116770672020"></a><a name="zh-cn_topic_0221482385_p116770672020"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p7677268202"><a name="zh-cn_topic_0221482385_p7677268202"></a><a name="zh-cn_topic_0221482385_p7677268202"></a>IAM用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row367514612016"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p156777622013"><a name="zh-cn_topic_0221482385_p156777622013"></a><a name="zh-cn_topic_0221482385_p156777622013"></a>password</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p567714652017"><a name="zh-cn_topic_0221482385_p567714652017"></a><a name="zh-cn_topic_0221482385_p567714652017"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p2067810618208"><a name="zh-cn_topic_0221482385_p2067810618208"></a><a name="zh-cn_topic_0221482385_p2067810618208"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p8678196152010"><a name="zh-cn_topic_0221482385_p8678196152010"></a><a name="zh-cn_topic_0221482385_p8678196152010"></a>IAM用户的登录密码。</p>
<div class="note" id="note1890710512544"><a name="note1890710512544"></a><a name="note1890710512544"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul817215473474"></a><a name="ul817215473474"></a><ul id="ul817215473474"><li>务必保证密码输入正确，避免获取Token失败。</li><li>如果您是第三方系统用户，直接使用联邦认证的用户名和密码获取Token，系统会提示密码错误。请在华为云的登录页面，通过“忘记密码”功能，设置<strong id="b10344113918147"><a name="b10344113918147"></a><a name="b10344113918147"></a>华为云帐号密码</strong>，并在password中输入新设置的密码。</li></ul>
</div></div>
</td>
</tr>
</tbody>
</table>

**表 8**  auth.identity.password.user.domain

<a name="zh-cn_topic_0221482385_request_Rq31AuthIdentityPwdUserDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row126781682012"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p206785622015"><a name="zh-cn_topic_0221482385_p206785622015"></a><a name="zh-cn_topic_0221482385_p206785622015"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p9678468207"><a name="zh-cn_topic_0221482385_p9678468207"></a><a name="zh-cn_topic_0221482385_p9678468207"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p1367917619203"><a name="zh-cn_topic_0221482385_p1367917619203"></a><a name="zh-cn_topic_0221482385_p1367917619203"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p16792632016"><a name="zh-cn_topic_0221482385_p16792632016"></a><a name="zh-cn_topic_0221482385_p16792632016"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row1767815611202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p6679564208"><a name="zh-cn_topic_0221482385_p6679564208"></a><a name="zh-cn_topic_0221482385_p6679564208"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p9679365207"><a name="zh-cn_topic_0221482385_p9679365207"></a><a name="zh-cn_topic_0221482385_p9679365207"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p1968086182013"><a name="zh-cn_topic_0221482385_p1968086182013"></a><a name="zh-cn_topic_0221482385_p1968086182013"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p7680363205"><a name="zh-cn_topic_0221482385_p7680363205"></a><a name="zh-cn_topic_0221482385_p7680363205"></a>IAM用户所属帐号名称，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  auth.identity.totp

<a name="zh-cn_topic_0221482385_request_Rq3100AuthIdentityTotp"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row16801264205"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p156812612018"><a name="zh-cn_topic_0221482385_p156812612018"></a><a name="zh-cn_topic_0221482385_p156812612018"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p1268196192012"><a name="zh-cn_topic_0221482385_p1268196192012"></a><a name="zh-cn_topic_0221482385_p1268196192012"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p26811564205"><a name="zh-cn_topic_0221482385_p26811564205"></a><a name="zh-cn_topic_0221482385_p26811564205"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p168120672016"><a name="zh-cn_topic_0221482385_p168120672016"></a><a name="zh-cn_topic_0221482385_p168120672016"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row7680962206"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p2068113642018"><a name="zh-cn_topic_0221482385_p2068113642018"></a><a name="zh-cn_topic_0221482385_p2068113642018"></a><a href="#zh-cn_topic_0221482385_request_Rq3100AuthIdentityTotpUser">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p46815615203"><a name="zh-cn_topic_0221482385_p46815615203"></a><a name="zh-cn_topic_0221482385_p46815615203"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p368119619205"><a name="zh-cn_topic_0221482385_p368119619205"></a><a name="zh-cn_topic_0221482385_p368119619205"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p66821267209"><a name="zh-cn_topic_0221482385_p66821267209"></a><a name="zh-cn_topic_0221482385_p66821267209"></a>IAM用户信息。该IAM用户已开启登录保护，并选择以虚拟MFA方式进行身份验证，开启/关闭登录保护方法请参见：<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0704.html" target="_blank" rel="noopener noreferrer">敏感操作</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 10**  auth.identity.totp.user

<a name="zh-cn_topic_0221482385_request_Rq3100AuthIdentityTotpUser"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row1868215611201"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p19682186182013"><a name="zh-cn_topic_0221482385_p19682186182013"></a><a name="zh-cn_topic_0221482385_p19682186182013"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p1168296122018"><a name="zh-cn_topic_0221482385_p1168296122018"></a><a name="zh-cn_topic_0221482385_p1168296122018"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p14683186192015"><a name="zh-cn_topic_0221482385_p14683186192015"></a><a name="zh-cn_topic_0221482385_p14683186192015"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p76831614208"><a name="zh-cn_topic_0221482385_p76831614208"></a><a name="zh-cn_topic_0221482385_p76831614208"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row96821664203"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p56839614207"><a name="zh-cn_topic_0221482385_p56839614207"></a><a name="zh-cn_topic_0221482385_p56839614207"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p186831263205"><a name="zh-cn_topic_0221482385_p186831263205"></a><a name="zh-cn_topic_0221482385_p186831263205"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p6683126152013"><a name="zh-cn_topic_0221482385_p6683126152013"></a><a name="zh-cn_topic_0221482385_p6683126152013"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p06832611207"><a name="zh-cn_topic_0221482385_p06832611207"></a><a name="zh-cn_topic_0221482385_p06832611207"></a>已开启虚拟MFA方式的登录保护的IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row368216682013"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p368313612010"><a name="zh-cn_topic_0221482385_p368313612010"></a><a name="zh-cn_topic_0221482385_p368313612010"></a>passcode</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p156847619206"><a name="zh-cn_topic_0221482385_p156847619206"></a><a name="zh-cn_topic_0221482385_p156847619206"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p1268417682016"><a name="zh-cn_topic_0221482385_p1268417682016"></a><a name="zh-cn_topic_0221482385_p1268417682016"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_p206841165200"><a name="zh-cn_topic_0221482385_p206841165200"></a><a name="zh-cn_topic_0221482385_p206841165200"></a>虚拟MFA验证码，在MFA应用程序中获取动态验证码，获取方法请参见：<a href="https://support.huaweicloud.com/iam_faq/iam_01_0001.html" target="_blank" rel="noopener noreferrer">如何获取虚拟MFA验证码</a>。</p>
<div class="note" id="note4971125905415"><a name="note4971125905415"></a><a name="note4971125905415"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p208369095519"><a name="p208369095519"></a><a name="p208369095519"></a>务必保证验证码输入正确，避免获取Token失败。</p>
</div></div>
</td>
</tr>
</tbody>
</table>

**表 11**  auth.scope

<a name="zh-cn_topic_0221482385_request_Rq31AuthScope"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row19684865209"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p36859619202"><a name="zh-cn_topic_0221482385_p36859619202"></a><a name="zh-cn_topic_0221482385_p36859619202"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p16685116182012"><a name="zh-cn_topic_0221482385_p16685116182012"></a><a name="zh-cn_topic_0221482385_p16685116182012"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p14685663202"><a name="zh-cn_topic_0221482385_p14685663202"></a><a name="zh-cn_topic_0221482385_p14685663202"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p1768536182014"><a name="zh-cn_topic_0221482385_p1768536182014"></a><a name="zh-cn_topic_0221482385_p1768536182014"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row46844652017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p76852672010"><a name="zh-cn_topic_0221482385_p76852672010"></a><a name="zh-cn_topic_0221482385_p76852672010"></a><a href="#zh-cn_topic_0221482385_request_Rq31AuthScopeDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p968546172010"><a name="zh-cn_topic_0221482385_p968546172010"></a><a name="zh-cn_topic_0221482385_p968546172010"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p1268666142012"><a name="zh-cn_topic_0221482385_p1268666142012"></a><a name="zh-cn_topic_0221482385_p1268666142012"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p193963531941"><a name="zh-cn_topic_0221482476_p193963531941"></a><a name="zh-cn_topic_0221482476_p193963531941"></a>取值为domain时，表示获取的Token可以作用于全局服务，全局服务不区分项目或区域，如OBS服务。如需了解服务作用范围，请参考<strong id="b18450101362919"><a name="b18450101362919"></a><a name="b18450101362919"></a><a href="https://support.huaweicloud.com/usermanual-permissions/iam_01_0001.html" target="_blank" rel="noopener noreferrer">系统权限</a></strong>。domain支持id和name，二选一即可，建议选择“domain_id”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row1568426172012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p176868614205"><a name="zh-cn_topic_0221482385_p176868614205"></a><a name="zh-cn_topic_0221482385_p176868614205"></a><a href="#zh-cn_topic_0221482385_request_Rq31AuthScopeProject">project</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p1368646152011"><a name="zh-cn_topic_0221482385_p1368646152011"></a><a name="zh-cn_topic_0221482385_p1368646152011"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p96861616202"><a name="zh-cn_topic_0221482385_p96861616202"></a><a name="zh-cn_topic_0221482385_p96861616202"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482476_p13979534417"><a name="zh-cn_topic_0221482476_p13979534417"></a><a name="zh-cn_topic_0221482476_p13979534417"></a>取值为project时，表示获取的Token可以作用于项目级服务，仅能访问指定project下的资源，如ECS服务。如需了解服务作用范围，请参考<strong id="b197581448203512"><a name="b197581448203512"></a><a name="b197581448203512"></a><a href="https://support.huaweicloud.com/usermanual-permissions/iam_01_0001.html" target="_blank" rel="noopener noreferrer">系统权限</a></strong>。project支持id和name，二选一即可。</p>
</td>
</tr>
</tbody>
</table>

**表 12**  auth.scope.domain

<a name="zh-cn_topic_0221482385_request_Rq31AuthScopeDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row1568656142010"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p1668715602013"><a name="zh-cn_topic_0221482385_p1668715602013"></a><a name="zh-cn_topic_0221482385_p1668715602013"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p268716632011"><a name="zh-cn_topic_0221482385_p268716632011"></a><a name="zh-cn_topic_0221482385_p268716632011"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p0687464208"><a name="zh-cn_topic_0221482385_p0687464208"></a><a name="zh-cn_topic_0221482385_p0687464208"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p1868715610208"><a name="zh-cn_topic_0221482385_p1868715610208"></a><a name="zh-cn_topic_0221482385_p1868715610208"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row66870618201"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p16688196112019"><a name="zh-cn_topic_0221482385_p16688196112019"></a><a name="zh-cn_topic_0221482385_p16688196112019"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p468826142012"><a name="zh-cn_topic_0221482385_p468826142012"></a><a name="zh-cn_topic_0221482385_p468826142012"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p368815615209"><a name="zh-cn_topic_0221482385_p368815615209"></a><a name="zh-cn_topic_0221482385_p368815615209"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_zh-cn_topic_0221460195_p46112337149"><a name="zh-cn_topic_0221482385_zh-cn_topic_0221460195_p46112337149"></a><a name="zh-cn_topic_0221482385_zh-cn_topic_0221460195_p46112337149"></a>IAM用户所属帐号ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row12687156122010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p868826102015"><a name="zh-cn_topic_0221482385_p868826102015"></a><a name="zh-cn_topic_0221482385_p868826102015"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p116881468206"><a name="zh-cn_topic_0221482385_p116881468206"></a><a name="zh-cn_topic_0221482385_p116881468206"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p17689156162015"><a name="zh-cn_topic_0221482385_p17689156162015"></a><a name="zh-cn_topic_0221482385_p17689156162015"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_zh-cn_topic_0221460195_p36121733121417"><a name="zh-cn_topic_0221482385_zh-cn_topic_0221460195_p36121733121417"></a><a name="zh-cn_topic_0221482385_zh-cn_topic_0221460195_p36121733121417"></a>IAM用户所属帐号名称，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 13**  auth.scope.project

<a name="zh-cn_topic_0221482385_request_Rq31AuthScopeProject"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row166899692017"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482385_p1768910642019"><a name="zh-cn_topic_0221482385_p1768910642019"></a><a name="zh-cn_topic_0221482385_p1768910642019"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482385_p56909613209"><a name="zh-cn_topic_0221482385_p56909613209"></a><a name="zh-cn_topic_0221482385_p56909613209"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482385_p1669076152015"><a name="zh-cn_topic_0221482385_p1669076152015"></a><a name="zh-cn_topic_0221482385_p1669076152015"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482385_p6690669208"><a name="zh-cn_topic_0221482385_p6690669208"></a><a name="zh-cn_topic_0221482385_p6690669208"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row1368918652019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p13690961209"><a name="zh-cn_topic_0221482385_p13690961209"></a><a name="zh-cn_topic_0221482385_p13690961209"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p136901468204"><a name="zh-cn_topic_0221482385_p136901468204"></a><a name="zh-cn_topic_0221482385_p136901468204"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p12690186192016"><a name="zh-cn_topic_0221482385_p12690186192016"></a><a name="zh-cn_topic_0221482385_p12690186192016"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_zh-cn_topic_0221460195_p86161233151410"><a name="zh-cn_topic_0221482385_zh-cn_topic_0221460195_p86161233151410"></a><a name="zh-cn_topic_0221482385_zh-cn_topic_0221460195_p86161233151410"></a>IAM用户所属帐号的项目id，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row1368946112020"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482385_p669114613203"><a name="zh-cn_topic_0221482385_p669114613203"></a><a name="zh-cn_topic_0221482385_p669114613203"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482385_p66914622012"><a name="zh-cn_topic_0221482385_p66914622012"></a><a name="zh-cn_topic_0221482385_p66914622012"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482385_p06911461200"><a name="zh-cn_topic_0221482385_p06911461200"></a><a name="zh-cn_topic_0221482385_p06911461200"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482385_zh-cn_topic_0221460195_p761723312149"><a name="zh-cn_topic_0221482385_zh-cn_topic_0221460195_p761723312149"></a><a name="zh-cn_topic_0221482385_zh-cn_topic_0221460195_p761723312149"></a>IAM用户所属帐号的项目名称，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482385_section1087706192012"></a>

-   示例1：获取IAM用户名为“IAMUser”，密码为“IAMPassword”，所属帐号名为“IAMDomain”，作用范围为整个帐号的Token。

    ```
    POST https://iam.myhuaweicloud.com/v3/auth/tokens
    ```

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "password",
                    "totp"
                ],
                "password": {
                    "user": {
                        "name": "IAMUser",                            //IAM用户名
                        "password": "IAMPassword",                   //IAM用户密码
                        "domain": {
                            "name": "IAMDomain"                      //IAM用户所属帐号名
                        }
                    }
                },
                "totp": {
                    "user": {
                        "id": "7116d09f88fa41908676fdd4b039e...",  //IAM用户ID
                        "passcode": "******"                           //虚拟MFA验证码
                    }
                }
            },
            "scope": {
                "domain": {
                    "name": "IAMDomain"                                 //IAM用户所属帐号名
                }
            }
        }
    }
    ```

-   示例2：获取IAM用户名为“IAMUser”，密码为“IAMPassword”，所属帐号名为“IAMDomain”，作用范围为项目“cn-north-1”，且返回的响应体中将不显示catalog信息的Token。

    ```
    POST https://iam.myhuaweicloud.com/v3/auth/tokens?nocatalog=true
    ```

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "password",
                    "totp"
                ],
                "password": {
                    "user": {
                        "name": "IAMUser",                            //IAM用户名
                        "password": "IAMPassword",                   //IAM用户密码
                        "domain": {
                            "name": "IAMDomain"                      //IAM用户所属帐号名
                        }
                    }
                },
                "totp": {
                    "user": {
                        "id": "7116d09f88fa41908676fdd4b039e...",  //IAM用户ID
                        "passcode": "******"                           //虚拟MFA验证码
                    }
                }
            },
            "scope": {
                "project": {
                    "name": "cn-north-1"                                //项目名称
                }
            }
        }
    }
    ```


## 响应参数<a name="zh-cn_topic_0221482385_section136919632018"></a>

**表 14**  响应Header参数

<a name="zh-cn_topic_0221482385_ResponseHeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row13692166172014"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482385_p4692168201"><a name="zh-cn_topic_0221482385_p4692168201"></a><a name="zh-cn_topic_0221482385_p4692168201"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482385_p1069215682014"><a name="zh-cn_topic_0221482385_p1069215682014"></a><a name="zh-cn_topic_0221482385_p1069215682014"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482385_p1969215652011"><a name="zh-cn_topic_0221482385_p1969215652011"></a><a name="zh-cn_topic_0221482385_p1969215652011"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row66921163208"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p169214612013"><a name="zh-cn_topic_0221482385_p169214612013"></a><a name="zh-cn_topic_0221482385_p169214612013"></a>X-Subject-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p1469314610200"><a name="zh-cn_topic_0221482385_p1469314610200"></a><a name="zh-cn_topic_0221482385_p1469314610200"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p12693146202011"><a name="zh-cn_topic_0221482385_p12693146202011"></a><a name="zh-cn_topic_0221482385_p12693146202011"></a>签名后的Token。</p>
</td>
</tr>
</tbody>
</table>

**表 15**  响应Body参数

<a name="zh-cn_topic_0221482385_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row106938672012"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482385_p669386182010"><a name="zh-cn_topic_0221482385_p669386182010"></a><a name="zh-cn_topic_0221482385_p669386182010"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482385_p386976162011"><a name="zh-cn_topic_0221482385_p386976162011"></a><a name="zh-cn_topic_0221482385_p386976162011"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482385_p158691263201"><a name="zh-cn_topic_0221482385_p158691263201"></a><a name="zh-cn_topic_0221482385_p158691263201"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row146931692017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p586918612015"><a name="zh-cn_topic_0221482385_p586918612015"></a><a name="zh-cn_topic_0221482385_p586918612015"></a><a href="#zh-cn_topic_0221482385_response_Rs31Token">token</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p1486912614201"><a name="zh-cn_topic_0221482385_p1486912614201"></a><a name="zh-cn_topic_0221482385_p1486912614201"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p188695682017"><a name="zh-cn_topic_0221482385_p188695682017"></a><a name="zh-cn_topic_0221482385_p188695682017"></a>获取到的Token信息。</p>
</td>
</tr>
</tbody>
</table>

**表 16**  token

<a name="zh-cn_topic_0221482385_response_Rs31Token"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row2069516602010"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482385_p2870146152018"><a name="zh-cn_topic_0221482385_p2870146152018"></a><a name="zh-cn_topic_0221482385_p2870146152018"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482385_p1870156142010"><a name="zh-cn_topic_0221482385_p1870156142010"></a><a name="zh-cn_topic_0221482385_p1870156142010"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482385_p3870763204"><a name="zh-cn_topic_0221482385_p3870763204"></a><a name="zh-cn_topic_0221482385_p3870763204"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row06955611209"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p18870366207"><a name="zh-cn_topic_0221482385_p18870366207"></a><a name="zh-cn_topic_0221482385_p18870366207"></a><a href="#zh-cn_topic_0221482385_response_Rs31TokenCatalogArritem">catalog</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p1287018682010"><a name="zh-cn_topic_0221482385_p1287018682010"></a><a name="zh-cn_topic_0221482385_p1287018682010"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p7870367208"><a name="zh-cn_topic_0221482385_p7870367208"></a><a name="zh-cn_topic_0221482385_p7870367208"></a>服务目录信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row126959615208"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p7870156142019"><a name="zh-cn_topic_0221482385_p7870156142019"></a><a name="zh-cn_topic_0221482385_p7870156142019"></a><a href="#zh-cn_topic_0221482385_response_Rs31TokenDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p98701610205"><a name="zh-cn_topic_0221482385_p98701610205"></a><a name="zh-cn_topic_0221482385_p98701610205"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p1870206192016"><a name="zh-cn_topic_0221482385_p1870206192016"></a><a name="zh-cn_topic_0221482385_p1870206192016"></a>获取Token的IAM用户所属的帐号信息。如果获取Token时请求体中scope参数设置为domain，则返回该字段。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row136959662011"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p16870186172015"><a name="zh-cn_topic_0221482385_p16870186172015"></a><a name="zh-cn_topic_0221482385_p16870186172015"></a>expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p68702652012"><a name="zh-cn_topic_0221482385_p68702652012"></a><a name="zh-cn_topic_0221482385_p68702652012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p158706602015"><a name="zh-cn_topic_0221482385_p158706602015"></a><a name="zh-cn_topic_0221482385_p158706602015"></a>Token过期时间。</p>
</td>
</tr>
<tr id="row15805152614116"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p380513263410"><a name="p380513263410"></a><a name="p380513263410"></a>mfa_authn_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p380542654117"><a name="p380542654117"></a><a name="p380542654117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p48058264417"><a name="p48058264417"></a><a name="p48058264417"></a>MFA验证时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row569515642017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p1787019619208"><a name="zh-cn_topic_0221482385_p1787019619208"></a><a name="zh-cn_topic_0221482385_p1787019619208"></a>issued_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p88707682014"><a name="zh-cn_topic_0221482385_p88707682014"></a><a name="zh-cn_topic_0221482385_p88707682014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p158702642012"><a name="zh-cn_topic_0221482385_p158702642012"></a><a name="zh-cn_topic_0221482385_p158702642012"></a>Token下发时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row46955642015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p98701614209"><a name="zh-cn_topic_0221482385_p98701614209"></a><a name="zh-cn_topic_0221482385_p98701614209"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p12870156142016"><a name="zh-cn_topic_0221482385_p12870156142016"></a><a name="zh-cn_topic_0221482385_p12870156142016"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p4870768204"><a name="zh-cn_topic_0221482385_p4870768204"></a><a name="zh-cn_topic_0221482385_p4870768204"></a>获取Token的方式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row156955612017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p10870169201"><a name="zh-cn_topic_0221482385_p10870169201"></a><a name="zh-cn_topic_0221482385_p10870169201"></a><a href="#zh-cn_topic_0221482385_response_Rs31TokenProject">project</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p16870106152014"><a name="zh-cn_topic_0221482385_p16870106152014"></a><a name="zh-cn_topic_0221482385_p16870106152014"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p987017612202"><a name="zh-cn_topic_0221482385_p987017612202"></a><a name="zh-cn_topic_0221482385_p987017612202"></a>获取Token的IAM用户所属帐号的项目信息。如果获取Token时请求体中scope参数设置为project，则返回该字段。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row196951064201"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p118708619202"><a name="zh-cn_topic_0221482385_p118708619202"></a><a name="zh-cn_topic_0221482385_p118708619202"></a><a href="#zh-cn_topic_0221482385_response_Rs31TokenRolesArritem">roles</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p58700617209"><a name="zh-cn_topic_0221482385_p58700617209"></a><a name="zh-cn_topic_0221482385_p58700617209"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p487016610202"><a name="zh-cn_topic_0221482385_p487016610202"></a><a name="zh-cn_topic_0221482385_p487016610202"></a>Token的权限信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row369556132010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p10870186172010"><a name="zh-cn_topic_0221482385_p10870186172010"></a><a name="zh-cn_topic_0221482385_p10870186172010"></a><a href="#zh-cn_topic_0221482385_response_Rs31TokenUser">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p787019613208"><a name="zh-cn_topic_0221482385_p787019613208"></a><a name="zh-cn_topic_0221482385_p787019613208"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p128701865203"><a name="zh-cn_topic_0221482385_p128701865203"></a><a name="zh-cn_topic_0221482385_p128701865203"></a>获取Token的IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 17**  token.catalog

<a name="zh-cn_topic_0221482385_response_Rs31TokenCatalogArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row2069846202011"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482385_p28711660208"><a name="zh-cn_topic_0221482385_p28711660208"></a><a name="zh-cn_topic_0221482385_p28711660208"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482385_p7871562200"><a name="zh-cn_topic_0221482385_p7871562200"></a><a name="zh-cn_topic_0221482385_p7871562200"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482385_p9871265203"><a name="zh-cn_topic_0221482385_p9871265203"></a><a name="zh-cn_topic_0221482385_p9871265203"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row14698663201"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p58711632012"><a name="zh-cn_topic_0221482385_p58711632012"></a><a name="zh-cn_topic_0221482385_p58711632012"></a><a href="#zh-cn_topic_0221482385_response_Rs31TokenCatalogArritemEndpointsArritem">endpoints</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p4871166182013"><a name="zh-cn_topic_0221482385_p4871166182013"></a><a name="zh-cn_topic_0221482385_p4871166182013"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p4871126112020"><a name="zh-cn_topic_0221482385_p4871126112020"></a><a name="zh-cn_topic_0221482385_p4871126112020"></a>终端节点。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row136981460203"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p1787118622017"><a name="zh-cn_topic_0221482385_p1787118622017"></a><a name="zh-cn_topic_0221482385_p1787118622017"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p16871764202"><a name="zh-cn_topic_0221482385_p16871764202"></a><a name="zh-cn_topic_0221482385_p16871764202"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p387518615203"><a name="zh-cn_topic_0221482385_p387518615203"></a><a name="zh-cn_topic_0221482385_p387518615203"></a>服务ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row166981567202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p287510618200"><a name="zh-cn_topic_0221482385_p287510618200"></a><a name="zh-cn_topic_0221482385_p287510618200"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p128751615208"><a name="zh-cn_topic_0221482385_p128751615208"></a><a name="zh-cn_topic_0221482385_p128751615208"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p8875368203"><a name="zh-cn_topic_0221482385_p8875368203"></a><a name="zh-cn_topic_0221482385_p8875368203"></a>服务名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row9698160207"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p0875146112012"><a name="zh-cn_topic_0221482385_p0875146112012"></a><a name="zh-cn_topic_0221482385_p0875146112012"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p687610652016"><a name="zh-cn_topic_0221482385_p687610652016"></a><a name="zh-cn_topic_0221482385_p687610652016"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p98761261203"><a name="zh-cn_topic_0221482385_p98761261203"></a><a name="zh-cn_topic_0221482385_p98761261203"></a>该接口所属服务。</p>
</td>
</tr>
</tbody>
</table>

**表 18**  token.catalog.endpoints

<a name="zh-cn_topic_0221482385_response_Rs31TokenCatalogArritemEndpointsArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row270116672015"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482385_p208768692016"><a name="zh-cn_topic_0221482385_p208768692016"></a><a name="zh-cn_topic_0221482385_p208768692016"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482385_p188761667206"><a name="zh-cn_topic_0221482385_p188761667206"></a><a name="zh-cn_topic_0221482385_p188761667206"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482385_p38761682015"><a name="zh-cn_topic_0221482385_p38761682015"></a><a name="zh-cn_topic_0221482385_p38761682015"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row270111642017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p168768613208"><a name="zh-cn_topic_0221482385_p168768613208"></a><a name="zh-cn_topic_0221482385_p168768613208"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p1687606162014"><a name="zh-cn_topic_0221482385_p1687606162014"></a><a name="zh-cn_topic_0221482385_p1687606162014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p16876262204"><a name="zh-cn_topic_0221482385_p16876262204"></a><a name="zh-cn_topic_0221482385_p16876262204"></a>终端节点ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row127010672013"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p5876767205"><a name="zh-cn_topic_0221482385_p5876767205"></a><a name="zh-cn_topic_0221482385_p5876767205"></a>interface</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p14876166162011"><a name="zh-cn_topic_0221482385_p14876166162011"></a><a name="zh-cn_topic_0221482385_p14876166162011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p17876186122010"><a name="zh-cn_topic_0221482385_p17876186122010"></a><a name="zh-cn_topic_0221482385_p17876186122010"></a>接口类型，描述接口在该终端节点的可见性。值为“public”，表示该接口为公开接口。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row1670115612202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p6876667205"><a name="zh-cn_topic_0221482385_p6876667205"></a><a name="zh-cn_topic_0221482385_p6876667205"></a>region</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p1887619692014"><a name="zh-cn_topic_0221482385_p1887619692014"></a><a name="zh-cn_topic_0221482385_p1887619692014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p1787620618207"><a name="zh-cn_topic_0221482385_p1787620618207"></a><a name="zh-cn_topic_0221482385_p1787620618207"></a>终端节点所属区域。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row147018642014"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p208767662015"><a name="zh-cn_topic_0221482385_p208767662015"></a><a name="zh-cn_topic_0221482385_p208767662015"></a>region_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p16876869203"><a name="zh-cn_topic_0221482385_p16876869203"></a><a name="zh-cn_topic_0221482385_p16876869203"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p187696152013"><a name="zh-cn_topic_0221482385_p187696152013"></a><a name="zh-cn_topic_0221482385_p187696152013"></a>终端节点所属区域ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row127018617207"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p68761569200"><a name="zh-cn_topic_0221482385_p68761569200"></a><a name="zh-cn_topic_0221482385_p68761569200"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p18876268202"><a name="zh-cn_topic_0221482385_p18876268202"></a><a name="zh-cn_topic_0221482385_p18876268202"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p1287616616205"><a name="zh-cn_topic_0221482385_p1287616616205"></a><a name="zh-cn_topic_0221482385_p1287616616205"></a>终端节点的URL。</p>
</td>
</tr>
</tbody>
</table>

**表 19**  token.domain

<a name="zh-cn_topic_0221482385_response_Rs31TokenDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row57031264206"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482385_p18762065201"><a name="zh-cn_topic_0221482385_p18762065201"></a><a name="zh-cn_topic_0221482385_p18762065201"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482385_p18761365204"><a name="zh-cn_topic_0221482385_p18761365204"></a><a name="zh-cn_topic_0221482385_p18761365204"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482385_p198765682016"><a name="zh-cn_topic_0221482385_p198765682016"></a><a name="zh-cn_topic_0221482385_p198765682016"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row1870316122016"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p11876763207"><a name="zh-cn_topic_0221482385_p11876763207"></a><a name="zh-cn_topic_0221482385_p11876763207"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p68760652018"><a name="zh-cn_topic_0221482385_p68760652018"></a><a name="zh-cn_topic_0221482385_p68760652018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p128761161201"><a name="zh-cn_topic_0221482385_p128761161201"></a><a name="zh-cn_topic_0221482385_p128761161201"></a>帐号名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row570318620201"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p0876116152015"><a name="zh-cn_topic_0221482385_p0876116152015"></a><a name="zh-cn_topic_0221482385_p0876116152015"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p188763613204"><a name="zh-cn_topic_0221482385_p188763613204"></a><a name="zh-cn_topic_0221482385_p188763613204"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p987613642019"><a name="zh-cn_topic_0221482385_p987613642019"></a><a name="zh-cn_topic_0221482385_p987613642019"></a>帐号ID。</p>
</td>
</tr>
</tbody>
</table>

**表 20**  token.project

<a name="zh-cn_topic_0221482385_response_Rs31TokenProject"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row127056615205"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482385_p38760682016"><a name="zh-cn_topic_0221482385_p38760682016"></a><a name="zh-cn_topic_0221482385_p38760682016"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482385_p48765615208"><a name="zh-cn_topic_0221482385_p48765615208"></a><a name="zh-cn_topic_0221482385_p48765615208"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482385_p687618617208"><a name="zh-cn_topic_0221482385_p687618617208"></a><a name="zh-cn_topic_0221482385_p687618617208"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row1670514612203"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p198766613203"><a name="zh-cn_topic_0221482385_p198766613203"></a><a name="zh-cn_topic_0221482385_p198766613203"></a><a href="#zh-cn_topic_0221482385_response_Rs31TokenProjectDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p1187656122012"><a name="zh-cn_topic_0221482385_p1187656122012"></a><a name="zh-cn_topic_0221482385_p1187656122012"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p087616617208"><a name="zh-cn_topic_0221482385_p087616617208"></a><a name="zh-cn_topic_0221482385_p087616617208"></a>项目所属帐号信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row1170513682017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p08767662010"><a name="zh-cn_topic_0221482385_p08767662010"></a><a name="zh-cn_topic_0221482385_p08767662010"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p178761360202"><a name="zh-cn_topic_0221482385_p178761360202"></a><a name="zh-cn_topic_0221482385_p178761360202"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p14876867201"><a name="zh-cn_topic_0221482385_p14876867201"></a><a name="zh-cn_topic_0221482385_p14876867201"></a>项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row97051561202"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p208761612204"><a name="zh-cn_topic_0221482385_p208761612204"></a><a name="zh-cn_topic_0221482385_p208761612204"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p15876163203"><a name="zh-cn_topic_0221482385_p15876163203"></a><a name="zh-cn_topic_0221482385_p15876163203"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p1287614613203"><a name="zh-cn_topic_0221482385_p1287614613203"></a><a name="zh-cn_topic_0221482385_p1287614613203"></a>项目名称。</p>
</td>
</tr>
</tbody>
</table>

**表 21**  token.project.domain

<a name="zh-cn_topic_0221482385_response_Rs31TokenProjectDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row147076619207"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482385_p48777617204"><a name="zh-cn_topic_0221482385_p48777617204"></a><a name="zh-cn_topic_0221482385_p48777617204"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482385_p8877168203"><a name="zh-cn_topic_0221482385_p8877168203"></a><a name="zh-cn_topic_0221482385_p8877168203"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482385_p98772063201"><a name="zh-cn_topic_0221482385_p98772063201"></a><a name="zh-cn_topic_0221482385_p98772063201"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row197071160204"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p198772632013"><a name="zh-cn_topic_0221482385_p198772632013"></a><a name="zh-cn_topic_0221482385_p198772632013"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p1187766132014"><a name="zh-cn_topic_0221482385_p1187766132014"></a><a name="zh-cn_topic_0221482385_p1187766132014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p787719617207"><a name="zh-cn_topic_0221482385_p787719617207"></a><a name="zh-cn_topic_0221482385_p787719617207"></a>帐号ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row147075632019"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p168772622016"><a name="zh-cn_topic_0221482385_p168772622016"></a><a name="zh-cn_topic_0221482385_p168772622016"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p1587710620201"><a name="zh-cn_topic_0221482385_p1587710620201"></a><a name="zh-cn_topic_0221482385_p1587710620201"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p1987746152019"><a name="zh-cn_topic_0221482385_p1987746152019"></a><a name="zh-cn_topic_0221482385_p1987746152019"></a>帐号名称。</p>
</td>
</tr>
</tbody>
</table>

**表 22**  token.roles

<a name="zh-cn_topic_0221482385_response_Rs31TokenRolesArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row77081632015"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482385_p12877116172018"><a name="zh-cn_topic_0221482385_p12877116172018"></a><a name="zh-cn_topic_0221482385_p12877116172018"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482385_p187719615206"><a name="zh-cn_topic_0221482385_p187719615206"></a><a name="zh-cn_topic_0221482385_p187719615206"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482385_p38771766209"><a name="zh-cn_topic_0221482385_p38771766209"></a><a name="zh-cn_topic_0221482385_p38771766209"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row137081768207"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p48776614209"><a name="zh-cn_topic_0221482385_p48776614209"></a><a name="zh-cn_topic_0221482385_p48776614209"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p3877369204"><a name="zh-cn_topic_0221482385_p3877369204"></a><a name="zh-cn_topic_0221482385_p3877369204"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p168776613207"><a name="zh-cn_topic_0221482385_p168776613207"></a><a name="zh-cn_topic_0221482385_p168776613207"></a>权限名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row070856152010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p68773619201"><a name="zh-cn_topic_0221482385_p68773619201"></a><a name="zh-cn_topic_0221482385_p68773619201"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p20877106172015"><a name="zh-cn_topic_0221482385_p20877106172015"></a><a name="zh-cn_topic_0221482385_p20877106172015"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p3877166132015"><a name="zh-cn_topic_0221482385_p3877166132015"></a><a name="zh-cn_topic_0221482385_p3877166132015"></a>权限ID。默认显示为0，非真实权限ID。</p>
</td>
</tr>
</tbody>
</table>

**表 23**  token.user

<a name="zh-cn_topic_0221482385_response_Rs31TokenUser"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row147110612201"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482385_p168777662011"><a name="zh-cn_topic_0221482385_p168777662011"></a><a name="zh-cn_topic_0221482385_p168777662011"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482385_p287710692014"><a name="zh-cn_topic_0221482385_p287710692014"></a><a name="zh-cn_topic_0221482385_p287710692014"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482385_p158775618205"><a name="zh-cn_topic_0221482385_p158775618205"></a><a name="zh-cn_topic_0221482385_p158775618205"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row177119618208"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p168771566205"><a name="zh-cn_topic_0221482385_p168771566205"></a><a name="zh-cn_topic_0221482385_p168771566205"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p887716192018"><a name="zh-cn_topic_0221482385_p887716192018"></a><a name="zh-cn_topic_0221482385_p887716192018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p387796122018"><a name="zh-cn_topic_0221482385_p387796122018"></a><a name="zh-cn_topic_0221482385_p387796122018"></a>IAM用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row1971119672018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p17877460208"><a name="zh-cn_topic_0221482385_p17877460208"></a><a name="zh-cn_topic_0221482385_p17877460208"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p387716612013"><a name="zh-cn_topic_0221482385_p387716612013"></a><a name="zh-cn_topic_0221482385_p387716612013"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p1787711652012"><a name="zh-cn_topic_0221482385_p1787711652012"></a><a name="zh-cn_topic_0221482385_p1787711652012"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row3711196182017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p7877116142017"><a name="zh-cn_topic_0221482385_p7877116142017"></a><a name="zh-cn_topic_0221482385_p7877116142017"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p1687713616207"><a name="zh-cn_topic_0221482385_p1687713616207"></a><a name="zh-cn_topic_0221482385_p1687713616207"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p18877136142014"><a name="zh-cn_topic_0221482385_p18877136142014"></a><a name="zh-cn_topic_0221482385_p18877136142014"></a>密码过期时间（UTC时间），“”表示密码不过期。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row5711116132012"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p9877461208"><a name="zh-cn_topic_0221482385_p9877461208"></a><a name="zh-cn_topic_0221482385_p9877461208"></a><a href="#zh-cn_topic_0221482385_response_Rs31TokenUserDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p15877186122014"><a name="zh-cn_topic_0221482385_p15877186122014"></a><a name="zh-cn_topic_0221482385_p15877186122014"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p1087796182014"><a name="zh-cn_topic_0221482385_p1087796182014"></a><a name="zh-cn_topic_0221482385_p1087796182014"></a>IAM用户所属的帐号信息。</p>
</td>
</tr>
</tbody>
</table>

**表 24**  token.user.domain

<a name="zh-cn_topic_0221482385_response_Rs31TokenUserDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row571416622010"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482385_p20877136182010"><a name="zh-cn_topic_0221482385_p20877136182010"></a><a name="zh-cn_topic_0221482385_p20877136182010"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482385_p19877762201"><a name="zh-cn_topic_0221482385_p19877762201"></a><a name="zh-cn_topic_0221482385_p19877762201"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482385_p38776616204"><a name="zh-cn_topic_0221482385_p38776616204"></a><a name="zh-cn_topic_0221482385_p38776616204"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row371412611204"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p18776619205"><a name="zh-cn_topic_0221482385_p18776619205"></a><a name="zh-cn_topic_0221482385_p18776619205"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p1487710642012"><a name="zh-cn_topic_0221482385_p1487710642012"></a><a name="zh-cn_topic_0221482385_p1487710642012"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p68771462207"><a name="zh-cn_topic_0221482385_p68771462207"></a><a name="zh-cn_topic_0221482385_p68771462207"></a>IAM用户所属帐号名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row47146611200"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482385_p1387736142011"><a name="zh-cn_topic_0221482385_p1387736142011"></a><a name="zh-cn_topic_0221482385_p1387736142011"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482385_p58774617207"><a name="zh-cn_topic_0221482385_p58774617207"></a><a name="zh-cn_topic_0221482385_p58774617207"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482385_p38771066207"><a name="zh-cn_topic_0221482385_p38771066207"></a><a name="zh-cn_topic_0221482385_p38771066207"></a>IAM用户所属帐号ID。</p>
</td>
</tr>
</tbody>
</table>

## 响应示例<a name="zh-cn_topic_0221482385_section198786612202"></a>

**状态码为 201 时:**

创建成功。

-   示例 1：获取IAM用户名为“IAMUser”，密码为“IAMPassword”，所属帐号名为“IAMDomain”，作用范围为整个帐号的Token。

    ```
    响应Header参数（获取到的Token）：
    X-Subject-Token:MIIatAYJKoZIhvcNAQcCoIIapTCCGqECAQExDTALB...
    ```

    ```
    响应Body参数：
    {
        "token": {
            "expires_at": "2020-01-04T09:08:49.965000Z",
            "mfa_authn_at": "2020-01-03T09:08:49.965000Z",
            "methods": [
                "password",
                "totp"
            ],
            "catalog": [
                {
                    "endpoints": [
                        {
                            "id": "33e1cbdd86d34e89a63cf8ad16a5f...",
                            "interface": "public",
                            "region": "*",
                            "region_id": "*",
                            "url": "https://iam.myhuaweicloud.com/v3.0"
                        }
                    ],
                    "id": "100a6a3477f1495286579b819d399...",
                    "name": "iam",
                    "type": "iam"
                },
                {
                    "endpoints": [
                        {
                            "id": "29319cf2052d4e94bcf438b55d143...",
                            "interface": "public",
                            "region": "*",
                            "region_id": "*",
                            "url": "https://bss.sample.domain.com/v1.0"
                        }
                    ],
                    "id": "c6db69fabbd549908adcb861c7e47...",
                    "name": "bssv1",
                    "type": "bssv1"
                }
            ],
            "domain": {
                "id": "d78cbac186b744899480f25bd022f...",
                "name": "IAMDomain"
            },
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
            "issued_at": "2020-01-03T09:08:49.965000Z",
            "user": {
                "domain": {
                    "id": "d78cbac186b744899480f25bd022f...",
                    "name": "IAMDomain"
                },
                "id": "7116d09f88fa41908676fdd4b039e...",
                "name": "IAMUser",
                "password_expires_at": ""
            }
        }
    }
    ```


-   示例 2：获取IAM用户名为“IAMUser”，密码为“IAMPassword”，所属帐号名为“IAMDomain”，作用范围为项目“cn-north-1”，且返回的响应体中将不显示catalog信息的Token。

    ```
    响应Header参数（获取到的Token）：
    X-Subject-Token:MIIatAYJKoZIhvcNAQcCoIIapTCCGqECAQExDTALB...
    ```

    ```
    响应Body参数：
    {
        "token": {
            "expires_at": "2020-01-04T09:05:22.701000Z",
            "mfa_authn_at": "2020-01-03T09:05:22.701000Z",
            "methods": [
                "password",
                "totp"
            ],
            "catalog": [],
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
            "project": {
                "domain": {
                    "id": "d78cbac186b744899480f25bd022f...",
                    "name": "IAMDomain"
                },
                "id": "aa2d97d7e62c4b7da3ffdfc11551f...",
                "name": "cn-north-1"
            },
            "issued_at": "2020-01-03T09:05:22.701000Z",
            "user": {
                "domain": {
                    "id": "d78cbac186b744899480f25bd022f...",
                    "name": "IAMDomain"
                },
                "id": "7116d09f88fa41908676fdd4b039e...",
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

-   如果您是第三方系统用户，直接使用联邦认证的用户名和密码获取Token，系统会提示密码错误。请在华为云的登录页面，通过“忘记密码”功能，设置**华为云帐号密码**，并在password中输入新设置的密码。
-   如果您的华为云帐号已升级为华为帐号，直接使用华为帐号名和密码获取Token，系统会提示密码错误。建议您为自己创建一个IAM用户，授予该用户必要的权限，获取IAM用户Token。

```
{
    "error": {
        "code": 401,
        "message": "The username or password is wrong.",
        "title": "Unauthorized"
    }
}
```

## 返回值<a name="zh-cn_topic_0221482385_section588112611208"></a>

<a name="zh-cn_topic_0221482385_table2418"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482385_row0727126102015"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482385_p13881867200"><a name="zh-cn_topic_0221482385_p13881867200"></a><a name="zh-cn_topic_0221482385_p13881867200"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482385_p208815622016"><a name="zh-cn_topic_0221482385_p208815622016"></a><a name="zh-cn_topic_0221482385_p208815622016"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482385_row1872706122010"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482385_p19881165204"><a name="zh-cn_topic_0221482385_p19881165204"></a><a name="zh-cn_topic_0221482385_p19881165204"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482385_p11881166192018"><a name="zh-cn_topic_0221482385_p11881166192018"></a><a name="zh-cn_topic_0221482385_p11881166192018"></a>创建成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row1472786122017"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482385_p98811566207"><a name="zh-cn_topic_0221482385_p98811566207"></a><a name="zh-cn_topic_0221482385_p98811566207"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482385_p488115616207"><a name="zh-cn_topic_0221482385_p488115616207"></a><a name="zh-cn_topic_0221482385_p488115616207"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row1372711692020"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482385_p188818620208"><a name="zh-cn_topic_0221482385_p188818620208"></a><a name="zh-cn_topic_0221482385_p188818620208"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482385_p1288112682010"><a name="zh-cn_topic_0221482385_p1288112682010"></a><a name="zh-cn_topic_0221482385_p1288112682010"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row87271265202"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482385_p11881156122013"><a name="zh-cn_topic_0221482385_p11881156122013"></a><a name="zh-cn_topic_0221482385_p11881156122013"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482385_p158819682014"><a name="zh-cn_topic_0221482385_p158819682014"></a><a name="zh-cn_topic_0221482385_p158819682014"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row372756182015"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482385_p138818692010"><a name="zh-cn_topic_0221482385_p138818692010"></a><a name="zh-cn_topic_0221482385_p138818692010"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482385_p148812622020"><a name="zh-cn_topic_0221482385_p148812622020"></a><a name="zh-cn_topic_0221482385_p148812622020"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row87278613208"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482385_p18811466201"><a name="zh-cn_topic_0221482385_p18811466201"></a><a name="zh-cn_topic_0221482385_p18811466201"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482385_p148811617201"><a name="zh-cn_topic_0221482385_p148811617201"></a><a name="zh-cn_topic_0221482385_p148811617201"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482385_row472786102018"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482385_p1888112662014"><a name="zh-cn_topic_0221482385_p1888112662014"></a><a name="zh-cn_topic_0221482385_p1888112662014"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482385_p14881176102013"><a name="zh-cn_topic_0221482385_p14881176102013"></a><a name="zh-cn_topic_0221482385_p14881176102013"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482385_section208811692014"></a>

无

