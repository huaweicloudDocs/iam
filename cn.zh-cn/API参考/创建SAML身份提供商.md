# 创建SAML身份提供商<a name="iam_13_0204"></a>

## 功能介绍<a name="zh-cn_topic_0224276933_section773274616456"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)创建基于SAML协议的身份提供商。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section794063213138"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneCreateIdentityProvider)中调试该接口。

## URI<a name="zh-cn_topic_0224276933_section2073264618454"></a>

PUT /v3/OS-FEDERATION/identity\_providers/\{id\}

**表 1**  路径参数

<a name="zh-cn_topic_0224276933_table14733114684518"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276933_row197331546134512"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276933_p187347462455"><a name="zh-cn_topic_0224276933_p187347462455"></a><a name="zh-cn_topic_0224276933_p187347462455"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276933_p137341462458"><a name="zh-cn_topic_0224276933_p137341462458"></a><a name="zh-cn_topic_0224276933_p137341462458"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276933_p16734946104517"><a name="zh-cn_topic_0224276933_p16734946104517"></a><a name="zh-cn_topic_0224276933_p16734946104517"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276933_p107341046194518"><a name="zh-cn_topic_0224276933_p107341046194518"></a><a name="zh-cn_topic_0224276933_p107341046194518"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276933_row373394644513"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276933_p1773514610451"><a name="zh-cn_topic_0224276933_p1773514610451"></a><a name="zh-cn_topic_0224276933_p1773514610451"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276933_p073512462451"><a name="zh-cn_topic_0224276933_p073512462451"></a><a name="zh-cn_topic_0224276933_p073512462451"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276933_p773515466451"><a name="zh-cn_topic_0224276933_p773515466451"></a><a name="zh-cn_topic_0224276933_p773515466451"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276933_p14735144604511"><a name="zh-cn_topic_0224276933_p14735144604511"></a><a name="zh-cn_topic_0224276933_p14735144604511"></a>待注册的身份提供商ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0224276933_section10736446194519"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0224276933_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276933_row17737134614510"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276933_p873914469451"><a name="zh-cn_topic_0224276933_p873914469451"></a><a name="zh-cn_topic_0224276933_p873914469451"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276933_p8739646194514"><a name="zh-cn_topic_0224276933_p8739646194514"></a><a name="zh-cn_topic_0224276933_p8739646194514"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276933_p197391846124517"><a name="zh-cn_topic_0224276933_p197391846124517"></a><a name="zh-cn_topic_0224276933_p197391846124517"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276933_p273918466454"><a name="zh-cn_topic_0224276933_p273918466454"></a><a name="zh-cn_topic_0224276933_p273918466454"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276933_row57373468452"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276933_p3740646144511"><a name="zh-cn_topic_0224276933_p3740646144511"></a><a name="zh-cn_topic_0224276933_p3740646144511"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276933_p5740164610451"><a name="zh-cn_topic_0224276933_p5740164610451"></a><a name="zh-cn_topic_0224276933_p5740164610451"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276933_p19740646164517"><a name="zh-cn_topic_0224276933_p19740646164517"></a><a name="zh-cn_topic_0224276933_p19740646164517"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276933_p274017460451"><a name="zh-cn_topic_0224276933_p274017460451"></a><a name="zh-cn_topic_0224276933_p274017460451"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row2073712460455"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276933_p1674110468456"><a name="zh-cn_topic_0224276933_p1674110468456"></a><a name="zh-cn_topic_0224276933_p1674110468456"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276933_p7741346194518"><a name="zh-cn_topic_0224276933_p7741346194518"></a><a name="zh-cn_topic_0224276933_p7741346194518"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276933_p1474114674515"><a name="zh-cn_topic_0224276933_p1474114674515"></a><a name="zh-cn_topic_0224276933_p1474114674515"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276933_p17742114619454"><a name="zh-cn_topic_0224276933_p17742114619454"></a><a name="zh-cn_topic_0224276933_p17742114619454"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="zh-cn_topic_0224276933_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276933_row10743114604511"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276933_p374464684514"><a name="zh-cn_topic_0224276933_p374464684514"></a><a name="zh-cn_topic_0224276933_p374464684514"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276933_p774474616453"><a name="zh-cn_topic_0224276933_p774474616453"></a><a name="zh-cn_topic_0224276933_p774474616453"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276933_p187451546114515"><a name="zh-cn_topic_0224276933_p187451546114515"></a><a name="zh-cn_topic_0224276933_p187451546114515"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276933_p137451646114510"><a name="zh-cn_topic_0224276933_p137451646114510"></a><a name="zh-cn_topic_0224276933_p137451646114510"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276933_row1574314644510"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276933_p11745446104512"><a name="zh-cn_topic_0224276933_p11745446104512"></a><a name="zh-cn_topic_0224276933_p11745446104512"></a><a href="#zh-cn_topic_0224276933_request_Rq1323Identityprovider">identity_provider</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276933_p674544664512"><a name="zh-cn_topic_0224276933_p674544664512"></a><a name="zh-cn_topic_0224276933_p674544664512"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276933_p12746446104520"><a name="zh-cn_topic_0224276933_p12746446104520"></a><a name="zh-cn_topic_0224276933_p12746446104520"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276933_p574624624518"><a name="zh-cn_topic_0224276933_p574624624518"></a><a name="zh-cn_topic_0224276933_p574624624518"></a>身份提供商信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  identity\_provider

<a name="zh-cn_topic_0224276933_request_Rq1323Identityprovider"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276933_row374634616456"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276933_p1174784613456"><a name="zh-cn_topic_0224276933_p1174784613456"></a><a name="zh-cn_topic_0224276933_p1174784613456"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276933_p77471246174512"><a name="zh-cn_topic_0224276933_p77471246174512"></a><a name="zh-cn_topic_0224276933_p77471246174512"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276933_p574844614512"><a name="zh-cn_topic_0224276933_p574844614512"></a><a name="zh-cn_topic_0224276933_p574844614512"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276933_p8748246154514"><a name="zh-cn_topic_0224276933_p8748246154514"></a><a name="zh-cn_topic_0224276933_p8748246154514"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row63772198275"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p337819193273"><a name="p337819193273"></a><a name="p337819193273"></a><span>sso_type</span></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p153783192272"><a name="p153783192272"></a><a name="p153783192272"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p3378121911273"><a name="p3378121911273"></a><a name="p3378121911273"></a><span>string</span></p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p237814192278"><a name="p237814192278"></a><a name="p237814192278"></a><span>身份提供商类型。当前支持virtual_user_sso和iam_user_sso两种，缺省配置默认为virtual_user_sso类型。</span></p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row9746164634511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276933_p3748046144511"><a name="zh-cn_topic_0224276933_p3748046144511"></a><a name="zh-cn_topic_0224276933_p3748046144511"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276933_p14748184604515"><a name="zh-cn_topic_0224276933_p14748184604515"></a><a name="zh-cn_topic_0224276933_p14748184604515"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276933_p19748746154518"><a name="zh-cn_topic_0224276933_p19748746154518"></a><a name="zh-cn_topic_0224276933_p19748746154518"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276933_p18749154634516"><a name="zh-cn_topic_0224276933_p18749154634516"></a><a name="zh-cn_topic_0224276933_p18749154634516"></a>身份提供商描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row207466467457"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276933_p8749746174515"><a name="zh-cn_topic_0224276933_p8749746174515"></a><a name="zh-cn_topic_0224276933_p8749746174515"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276933_p274964664517"><a name="zh-cn_topic_0224276933_p274964664517"></a><a name="zh-cn_topic_0224276933_p274964664517"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276933_p274910466450"><a name="zh-cn_topic_0224276933_p274910466450"></a><a name="zh-cn_topic_0224276933_p274910466450"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276933_p275024616452"><a name="zh-cn_topic_0224276933_p275024616452"></a><a name="zh-cn_topic_0224276933_p275024616452"></a>身份提供商是否启用，true为启用，false为停用，默认为false。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0224276933_section77501246204520"></a>

**表 5**  响应Body参数

<a name="zh-cn_topic_0224276933_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276933_row1854754624512"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276933_p1854820469451"><a name="zh-cn_topic_0224276933_p1854820469451"></a><a name="zh-cn_topic_0224276933_p1854820469451"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276933_p1554814462455"><a name="zh-cn_topic_0224276933_p1554814462455"></a><a name="zh-cn_topic_0224276933_p1554814462455"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276933_p954824654513"><a name="zh-cn_topic_0224276933_p954824654513"></a><a name="zh-cn_topic_0224276933_p954824654513"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276933_row5547446204513"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276933_p195497463454"><a name="zh-cn_topic_0224276933_p195497463454"></a><a name="zh-cn_topic_0224276933_p195497463454"></a><a href="#zh-cn_topic_0224276933_response_Rs1321IdentityprovidersArritem">identity_provider</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276933_p17549546124519"><a name="zh-cn_topic_0224276933_p17549546124519"></a><a name="zh-cn_topic_0224276933_p17549546124519"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276933_p165491446134519"><a name="zh-cn_topic_0224276933_p165491446134519"></a><a name="zh-cn_topic_0224276933_p165491446134519"></a>身份提供商信息。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  identity\_provider

<a name="zh-cn_topic_0224276933_response_Rs1321IdentityprovidersArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276933_row13551194674518"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276933_p1855212466451"><a name="zh-cn_topic_0224276933_p1855212466451"></a><a name="zh-cn_topic_0224276933_p1855212466451"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276933_p1855317461453"><a name="zh-cn_topic_0224276933_p1855317461453"></a><a name="zh-cn_topic_0224276933_p1855317461453"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276933_p18554144624513"><a name="zh-cn_topic_0224276933_p18554144624513"></a><a name="zh-cn_topic_0224276933_p18554144624513"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row6736307349"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p104900703412"><a name="p104900703412"></a><a name="p104900703412"></a>sso_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p449012715343"><a name="p449012715343"></a><a name="p449012715343"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1373615013342"><a name="p1373615013342"></a><a name="p1373615013342"></a><span>身份提供商类型。当前支持virtual_user_sso和iam_user_sso两种。当返回为空字符串或者null时，默认为缺省类型virtual_user_sso类型。</span></p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row1055113468457"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276933_p14555154615457"><a name="zh-cn_topic_0224276933_p14555154615457"></a><a name="zh-cn_topic_0224276933_p14555154615457"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276933_p1255614612459"><a name="zh-cn_topic_0224276933_p1255614612459"></a><a name="zh-cn_topic_0224276933_p1255614612459"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276933_p15561146154517"><a name="zh-cn_topic_0224276933_p15561146154517"></a><a name="zh-cn_topic_0224276933_p15561146154517"></a>身份提供商ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row1055184616451"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276933_p15571146124512"><a name="zh-cn_topic_0224276933_p15571146124512"></a><a name="zh-cn_topic_0224276933_p15571146124512"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276933_p1955824674513"><a name="zh-cn_topic_0224276933_p1955824674513"></a><a name="zh-cn_topic_0224276933_p1955824674513"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276933_p255964634520"><a name="zh-cn_topic_0224276933_p255964634520"></a><a name="zh-cn_topic_0224276933_p255964634520"></a>身份提供商描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row14551146154520"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276933_p15605462453"><a name="zh-cn_topic_0224276933_p15605462453"></a><a name="zh-cn_topic_0224276933_p15605462453"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276933_p10560184684510"><a name="zh-cn_topic_0224276933_p10560184684510"></a><a name="zh-cn_topic_0224276933_p10560184684510"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276933_p12560124654514"><a name="zh-cn_topic_0224276933_p12560124654514"></a><a name="zh-cn_topic_0224276933_p12560124654514"></a>身份提供商是否启用，true为启用，false为停用，默认为false。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row6551946124516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276933_p19560846104514"><a name="zh-cn_topic_0224276933_p19560846104514"></a><a name="zh-cn_topic_0224276933_p19560846104514"></a>remote_ids</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276933_p185600467455"><a name="zh-cn_topic_0224276933_p185600467455"></a><a name="zh-cn_topic_0224276933_p185600467455"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276933_p75611346164519"><a name="zh-cn_topic_0224276933_p75611346164519"></a><a name="zh-cn_topic_0224276933_p75611346164519"></a>身份提供商的联邦用户ID列表。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row19551446114516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276933_p1256194664518"><a name="zh-cn_topic_0224276933_p1256194664518"></a><a name="zh-cn_topic_0224276933_p1256194664518"></a><a href="#zh-cn_topic_0224276933_response_Rs1321IdentityprovidersArritemLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276933_p115611146134515"><a name="zh-cn_topic_0224276933_p115611146134515"></a><a name="zh-cn_topic_0224276933_p115611146134515"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276933_p1856194616459"><a name="zh-cn_topic_0224276933_p1856194616459"></a><a name="zh-cn_topic_0224276933_p1856194616459"></a>身份提供商的资源链接信息。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  identity\_provider.links

<a name="zh-cn_topic_0224276933_response_Rs1321IdentityprovidersArritemLinks"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276933_row056210464456"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276933_p1356213463458"><a name="zh-cn_topic_0224276933_p1356213463458"></a><a name="zh-cn_topic_0224276933_p1356213463458"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276933_p656384684515"><a name="zh-cn_topic_0224276933_p656384684515"></a><a name="zh-cn_topic_0224276933_p656384684515"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276933_p25631746194516"><a name="zh-cn_topic_0224276933_p25631746194516"></a><a name="zh-cn_topic_0224276933_p25631746194516"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276933_row0562646184512"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276933_p1956334615457"><a name="zh-cn_topic_0224276933_p1956334615457"></a><a name="zh-cn_topic_0224276933_p1956334615457"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276933_p115641546144515"><a name="zh-cn_topic_0224276933_p115641546144515"></a><a name="zh-cn_topic_0224276933_p115641546144515"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276933_p1156464634517"><a name="zh-cn_topic_0224276933_p1156464634517"></a><a name="zh-cn_topic_0224276933_p1156464634517"></a>身份提供商的资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row2562204654510"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276933_p135640468454"><a name="zh-cn_topic_0224276933_p135640468454"></a><a name="zh-cn_topic_0224276933_p135640468454"></a>protocols</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276933_p85647469450"><a name="zh-cn_topic_0224276933_p85647469450"></a><a name="zh-cn_topic_0224276933_p85647469450"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276933_p195641946184510"><a name="zh-cn_topic_0224276933_p195641946184510"></a><a name="zh-cn_topic_0224276933_p195641946184510"></a>协议的资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0224276933_section076104610458"></a>

```
PUT https://iam.myhuaweicloud.com/v3/OS-FEDERATION/identity_providers/{id}
```

```
{
    "identity_provider": {
        "description": "Stores ACME identities.",
        "enabled": true
    }
}
```

## 响应示例<a name="zh-cn_topic_0224276933_section157621846174518"></a>

**状态码为 201 时:**

请求成功。

```
{
    "identity_provider": {
        "remote_ids": [],
        "enabled": true,
        "id": "ACME",
        "sso_type": "iam_user_sso",
        "links": {
            "self": "https://iam.myhuaweicloud.com/v3/OS-FEDERATION/identity_providers/ACME",
            "protocols": "https://iam.myhuaweicloud.com/v3/OS-FEDERATION/identity_providers/ACME/protocols"
        },
        "description": "Stores ACME identities."
    }
}
```

## 返回值<a name="zh-cn_topic_0224276933_section11765174614511"></a>

<a name="zh-cn_topic_0224276933_table4312"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276933_row9766174634517"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0224276933_p11766114684513"><a name="zh-cn_topic_0224276933_p11766114684513"></a><a name="zh-cn_topic_0224276933_p11766114684513"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0224276933_p7766346124511"><a name="zh-cn_topic_0224276933_p7766346124511"></a><a name="zh-cn_topic_0224276933_p7766346124511"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276933_row1776664614457"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276933_p1076724616453"><a name="zh-cn_topic_0224276933_p1076724616453"></a><a name="zh-cn_topic_0224276933_p1076724616453"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276933_p17767446154510"><a name="zh-cn_topic_0224276933_p17767446154510"></a><a name="zh-cn_topic_0224276933_p17767446154510"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row276615466453"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276933_p1176774620458"><a name="zh-cn_topic_0224276933_p1176774620458"></a><a name="zh-cn_topic_0224276933_p1176774620458"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276933_p376784664517"><a name="zh-cn_topic_0224276933_p376784664517"></a><a name="zh-cn_topic_0224276933_p376784664517"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row1676674619458"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276933_p14768946104510"><a name="zh-cn_topic_0224276933_p14768946104510"></a><a name="zh-cn_topic_0224276933_p14768946104510"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276933_p5768104618458"><a name="zh-cn_topic_0224276933_p5768104618458"></a><a name="zh-cn_topic_0224276933_p5768104618458"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row10766144694516"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276933_p976844614516"><a name="zh-cn_topic_0224276933_p976844614516"></a><a name="zh-cn_topic_0224276933_p976844614516"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276933_p87681346164516"><a name="zh-cn_topic_0224276933_p87681346164516"></a><a name="zh-cn_topic_0224276933_p87681346164516"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row1176624614458"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276933_p19769154614514"><a name="zh-cn_topic_0224276933_p19769154614514"></a><a name="zh-cn_topic_0224276933_p19769154614514"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276933_p6769046134519"><a name="zh-cn_topic_0224276933_p6769046134519"></a><a name="zh-cn_topic_0224276933_p6769046134519"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row157663465453"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276933_p976964613451"><a name="zh-cn_topic_0224276933_p976964613451"></a><a name="zh-cn_topic_0224276933_p976964613451"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276933_p11769124618452"><a name="zh-cn_topic_0224276933_p11769124618452"></a><a name="zh-cn_topic_0224276933_p11769124618452"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row57662046174516"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276933_p117691346114514"><a name="zh-cn_topic_0224276933_p117691346114514"></a><a name="zh-cn_topic_0224276933_p117691346114514"></a>409</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276933_p57701046194515"><a name="zh-cn_topic_0224276933_p57701046194515"></a><a name="zh-cn_topic_0224276933_p57701046194515"></a>资源冲突。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row17661464451"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276933_p11770144614453"><a name="zh-cn_topic_0224276933_p11770144614453"></a><a name="zh-cn_topic_0224276933_p11770144614453"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276933_p0770194684514"><a name="zh-cn_topic_0224276933_p0770194684514"></a><a name="zh-cn_topic_0224276933_p0770194684514"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row37661246124520"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276933_p167711746194514"><a name="zh-cn_topic_0224276933_p167711746194514"></a><a name="zh-cn_topic_0224276933_p167711746194514"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276933_p37711146114517"><a name="zh-cn_topic_0224276933_p37711146114517"></a><a name="zh-cn_topic_0224276933_p37711146114517"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276933_row8766184614457"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276933_p167719469450"><a name="zh-cn_topic_0224276933_p167719469450"></a><a name="zh-cn_topic_0224276933_p167719469450"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276933_p37719463451"><a name="zh-cn_topic_0224276933_p37719463451"></a><a name="zh-cn_topic_0224276933_p37719463451"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0224276933_section7772946104520"></a>

无

