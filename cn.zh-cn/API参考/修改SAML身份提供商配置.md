# 修改SAML身份提供商配置<a name="iam_13_0205"></a>

## 功能介绍<a name="zh-cn_topic_0224276697_section1084513466455"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)修改基于SAML协议的身份提供商配置。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section01813361319"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneUpdateIdentityProvider)中调试该接口。

## URI<a name="zh-cn_topic_0224276697_section138467463456"></a>

PATCH /v3/OS-FEDERATION/identity\_providers/\{id\}

**表 1**  路径参数

<a name="zh-cn_topic_0224276697_table18847144619453"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276697_row19846104610456"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276697_p784794654520"><a name="zh-cn_topic_0224276697_p784794654520"></a><a name="zh-cn_topic_0224276697_p784794654520"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276697_p108488463455"><a name="zh-cn_topic_0224276697_p108488463455"></a><a name="zh-cn_topic_0224276697_p108488463455"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276697_p10848446164513"><a name="zh-cn_topic_0224276697_p10848446164513"></a><a name="zh-cn_topic_0224276697_p10848446164513"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276697_p78481946144510"><a name="zh-cn_topic_0224276697_p78481946144510"></a><a name="zh-cn_topic_0224276697_p78481946144510"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276697_row18846546124515"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276697_p1784964613454"><a name="zh-cn_topic_0224276697_p1784964613454"></a><a name="zh-cn_topic_0224276697_p1784964613454"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276697_p198492463457"><a name="zh-cn_topic_0224276697_p198492463457"></a><a name="zh-cn_topic_0224276697_p198492463457"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276697_p6849164664511"><a name="zh-cn_topic_0224276697_p6849164664511"></a><a name="zh-cn_topic_0224276697_p6849164664511"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276697_p13849174664518"><a name="zh-cn_topic_0224276697_p13849174664518"></a><a name="zh-cn_topic_0224276697_p13849174664518"></a>待更新的身份提供商ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0224276697_section16849134612458"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0224276697_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276697_row985015468455"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276697_p485115464454"><a name="zh-cn_topic_0224276697_p485115464454"></a><a name="zh-cn_topic_0224276697_p485115464454"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276697_p108511746114510"><a name="zh-cn_topic_0224276697_p108511746114510"></a><a name="zh-cn_topic_0224276697_p108511746114510"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276697_p1185134620451"><a name="zh-cn_topic_0224276697_p1185134620451"></a><a name="zh-cn_topic_0224276697_p1185134620451"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276697_p1485216466459"><a name="zh-cn_topic_0224276697_p1485216466459"></a><a name="zh-cn_topic_0224276697_p1485216466459"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276697_row4850174654511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276697_p178521646174510"><a name="zh-cn_topic_0224276697_p178521646174510"></a><a name="zh-cn_topic_0224276697_p178521646174510"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276697_p128531246134517"><a name="zh-cn_topic_0224276697_p128531246134517"></a><a name="zh-cn_topic_0224276697_p128531246134517"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276697_p15853946134517"><a name="zh-cn_topic_0224276697_p15853946134517"></a><a name="zh-cn_topic_0224276697_p15853946134517"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276697_p19853134619454"><a name="zh-cn_topic_0224276697_p19853134619454"></a><a name="zh-cn_topic_0224276697_p19853134619454"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row985017462452"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276697_p1854194664517"><a name="zh-cn_topic_0224276697_p1854194664517"></a><a name="zh-cn_topic_0224276697_p1854194664517"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276697_p9854346164510"><a name="zh-cn_topic_0224276697_p9854346164510"></a><a name="zh-cn_topic_0224276697_p9854346164510"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276697_p085564694515"><a name="zh-cn_topic_0224276697_p085564694515"></a><a name="zh-cn_topic_0224276697_p085564694515"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276697_p18855124634516"><a name="zh-cn_topic_0224276697_p18855124634516"></a><a name="zh-cn_topic_0224276697_p18855124634516"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="zh-cn_topic_0224276697_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276697_row10743114604511"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276697_p374464684514"><a name="zh-cn_topic_0224276697_p374464684514"></a><a name="zh-cn_topic_0224276697_p374464684514"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276697_p774474616453"><a name="zh-cn_topic_0224276697_p774474616453"></a><a name="zh-cn_topic_0224276697_p774474616453"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276697_p187451546114515"><a name="zh-cn_topic_0224276697_p187451546114515"></a><a name="zh-cn_topic_0224276697_p187451546114515"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276697_p137451646114510"><a name="zh-cn_topic_0224276697_p137451646114510"></a><a name="zh-cn_topic_0224276697_p137451646114510"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276697_row1574314644510"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276697_p11745446104512"><a name="zh-cn_topic_0224276697_p11745446104512"></a><a name="zh-cn_topic_0224276697_p11745446104512"></a><a href="#zh-cn_topic_0224276697_request_Rq1323Identityprovider">identity_provider</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276697_p674544664512"><a name="zh-cn_topic_0224276697_p674544664512"></a><a name="zh-cn_topic_0224276697_p674544664512"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276697_p12746446104520"><a name="zh-cn_topic_0224276697_p12746446104520"></a><a name="zh-cn_topic_0224276697_p12746446104520"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276697_p574624624518"><a name="zh-cn_topic_0224276697_p574624624518"></a><a name="zh-cn_topic_0224276697_p574624624518"></a>身份提供商信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  identity\_provider

<a name="zh-cn_topic_0224276697_request_Rq1323Identityprovider"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276697_row374634616456"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276697_p1174784613456"><a name="zh-cn_topic_0224276697_p1174784613456"></a><a name="zh-cn_topic_0224276697_p1174784613456"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276697_p77471246174512"><a name="zh-cn_topic_0224276697_p77471246174512"></a><a name="zh-cn_topic_0224276697_p77471246174512"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276697_p574844614512"><a name="zh-cn_topic_0224276697_p574844614512"></a><a name="zh-cn_topic_0224276697_p574844614512"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276697_p8748246154514"><a name="zh-cn_topic_0224276697_p8748246154514"></a><a name="zh-cn_topic_0224276697_p8748246154514"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276697_row9746164634511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276697_p3748046144511"><a name="zh-cn_topic_0224276697_p3748046144511"></a><a name="zh-cn_topic_0224276697_p3748046144511"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276697_p14748184604515"><a name="zh-cn_topic_0224276697_p14748184604515"></a><a name="zh-cn_topic_0224276697_p14748184604515"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276697_p19748746154518"><a name="zh-cn_topic_0224276697_p19748746154518"></a><a name="zh-cn_topic_0224276697_p19748746154518"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276697_p18749154634516"><a name="zh-cn_topic_0224276697_p18749154634516"></a><a name="zh-cn_topic_0224276697_p18749154634516"></a>身份提供商描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row207466467457"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276697_p8749746174515"><a name="zh-cn_topic_0224276697_p8749746174515"></a><a name="zh-cn_topic_0224276697_p8749746174515"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276697_p274964664517"><a name="zh-cn_topic_0224276697_p274964664517"></a><a name="zh-cn_topic_0224276697_p274964664517"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276697_p274910466450"><a name="zh-cn_topic_0224276697_p274910466450"></a><a name="zh-cn_topic_0224276697_p274910466450"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276697_p275024616452"><a name="zh-cn_topic_0224276697_p275024616452"></a><a name="zh-cn_topic_0224276697_p275024616452"></a>身份提供商是否启用，true为启用，false为停用，默认为false。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0224276697_section1386224634519"></a>

**表 5**  响应Body参数

<a name="zh-cn_topic_0224276697_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276697_row1854754624512"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276697_p1854820469451"><a name="zh-cn_topic_0224276697_p1854820469451"></a><a name="zh-cn_topic_0224276697_p1854820469451"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276697_p1554814462455"><a name="zh-cn_topic_0224276697_p1554814462455"></a><a name="zh-cn_topic_0224276697_p1554814462455"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276697_p954824654513"><a name="zh-cn_topic_0224276697_p954824654513"></a><a name="zh-cn_topic_0224276697_p954824654513"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276697_row5547446204513"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276697_p195497463454"><a name="zh-cn_topic_0224276697_p195497463454"></a><a name="zh-cn_topic_0224276697_p195497463454"></a><a href="#zh-cn_topic_0224276697_response_Rs1321IdentityprovidersArritem">identity_provider</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276697_p17549546124519"><a name="zh-cn_topic_0224276697_p17549546124519"></a><a name="zh-cn_topic_0224276697_p17549546124519"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276697_p165491446134519"><a name="zh-cn_topic_0224276697_p165491446134519"></a><a name="zh-cn_topic_0224276697_p165491446134519"></a>身份提供商信息。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  identity\_provider

<a name="zh-cn_topic_0224276697_response_Rs1321IdentityprovidersArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276697_row13551194674518"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276697_p1855212466451"><a name="zh-cn_topic_0224276697_p1855212466451"></a><a name="zh-cn_topic_0224276697_p1855212466451"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276697_p1855317461453"><a name="zh-cn_topic_0224276697_p1855317461453"></a><a name="zh-cn_topic_0224276697_p1855317461453"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276697_p18554144624513"><a name="zh-cn_topic_0224276697_p18554144624513"></a><a name="zh-cn_topic_0224276697_p18554144624513"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1585415505378"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p14291856203710"><a name="p14291856203710"></a><a name="p14291856203710"></a>sso_type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p19291165673711"><a name="p19291165673711"></a><a name="p19291165673711"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1285417504372"><a name="p1285417504372"></a><a name="p1285417504372"></a><span>身份提供商类型。当前支持virtual_user_sso和iam_user_sso两种。当返回为空字符串或者null时，默认为缺省类型virtual_user_sso类型。</span></p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row1055113468457"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276697_p14555154615457"><a name="zh-cn_topic_0224276697_p14555154615457"></a><a name="zh-cn_topic_0224276697_p14555154615457"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276697_p1255614612459"><a name="zh-cn_topic_0224276697_p1255614612459"></a><a name="zh-cn_topic_0224276697_p1255614612459"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276697_p15561146154517"><a name="zh-cn_topic_0224276697_p15561146154517"></a><a name="zh-cn_topic_0224276697_p15561146154517"></a>身份提供商ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row1055184616451"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276697_p15571146124512"><a name="zh-cn_topic_0224276697_p15571146124512"></a><a name="zh-cn_topic_0224276697_p15571146124512"></a>description</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276697_p1955824674513"><a name="zh-cn_topic_0224276697_p1955824674513"></a><a name="zh-cn_topic_0224276697_p1955824674513"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276697_p255964634520"><a name="zh-cn_topic_0224276697_p255964634520"></a><a name="zh-cn_topic_0224276697_p255964634520"></a>身份提供商描述信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row14551146154520"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276697_p15605462453"><a name="zh-cn_topic_0224276697_p15605462453"></a><a name="zh-cn_topic_0224276697_p15605462453"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276697_p10560184684510"><a name="zh-cn_topic_0224276697_p10560184684510"></a><a name="zh-cn_topic_0224276697_p10560184684510"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276697_p12560124654514"><a name="zh-cn_topic_0224276697_p12560124654514"></a><a name="zh-cn_topic_0224276697_p12560124654514"></a>身份提供商是否启用，true为启用，false为停用，默认为false。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row6551946124516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276697_p19560846104514"><a name="zh-cn_topic_0224276697_p19560846104514"></a><a name="zh-cn_topic_0224276697_p19560846104514"></a>remote_ids</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276697_p185600467455"><a name="zh-cn_topic_0224276697_p185600467455"></a><a name="zh-cn_topic_0224276697_p185600467455"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276697_p75611346164519"><a name="zh-cn_topic_0224276697_p75611346164519"></a><a name="zh-cn_topic_0224276697_p75611346164519"></a>身份提供商的联邦用户ID列表。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row19551446114516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276697_p1256194664518"><a name="zh-cn_topic_0224276697_p1256194664518"></a><a name="zh-cn_topic_0224276697_p1256194664518"></a><a href="#zh-cn_topic_0224276697_response_Rs1321IdentityprovidersArritemLinks">links</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276697_p115611146134515"><a name="zh-cn_topic_0224276697_p115611146134515"></a><a name="zh-cn_topic_0224276697_p115611146134515"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276697_p1856194616459"><a name="zh-cn_topic_0224276697_p1856194616459"></a><a name="zh-cn_topic_0224276697_p1856194616459"></a>身份提供商的资源链接信息。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  identity\_provider.links

<a name="zh-cn_topic_0224276697_response_Rs1321IdentityprovidersArritemLinks"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276697_row056210464456"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276697_p1356213463458"><a name="zh-cn_topic_0224276697_p1356213463458"></a><a name="zh-cn_topic_0224276697_p1356213463458"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276697_p656384684515"><a name="zh-cn_topic_0224276697_p656384684515"></a><a name="zh-cn_topic_0224276697_p656384684515"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276697_p25631746194516"><a name="zh-cn_topic_0224276697_p25631746194516"></a><a name="zh-cn_topic_0224276697_p25631746194516"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276697_row0562646184512"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276697_p1956334615457"><a name="zh-cn_topic_0224276697_p1956334615457"></a><a name="zh-cn_topic_0224276697_p1956334615457"></a>self</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276697_p115641546144515"><a name="zh-cn_topic_0224276697_p115641546144515"></a><a name="zh-cn_topic_0224276697_p115641546144515"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276697_p1156464634517"><a name="zh-cn_topic_0224276697_p1156464634517"></a><a name="zh-cn_topic_0224276697_p1156464634517"></a>身份提供商的资源链接地址。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row2562204654510"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276697_p135640468454"><a name="zh-cn_topic_0224276697_p135640468454"></a><a name="zh-cn_topic_0224276697_p135640468454"></a>protocols</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276697_p85647469450"><a name="zh-cn_topic_0224276697_p85647469450"></a><a name="zh-cn_topic_0224276697_p85647469450"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276697_p195641946184510"><a name="zh-cn_topic_0224276697_p195641946184510"></a><a name="zh-cn_topic_0224276697_p195641946184510"></a>协议的资源链接地址。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0224276697_section1387320462457"></a>

```
PATCH https://iam.myhuaweicloud.com/v3/OS-FEDERATION/identity_providers/{id}
```

```
{
    "identity_provider": {
        "description": "Stores ACME identities.",
        "enabled": false
    }
}
```

## 响应示例<a name="zh-cn_topic_0224276697_section187474610456"></a>

**状态码为 200 时:**

请求成功。

```
{
    "identity_provider": {
        "remote_ids": [],
        "enabled": false,
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

## 返回值<a name="zh-cn_topic_0224276697_section1087613463454"></a>

<a name="zh-cn_topic_0224276697_table4313"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276697_row887754610451"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0224276697_p1687915469454"><a name="zh-cn_topic_0224276697_p1687915469454"></a><a name="zh-cn_topic_0224276697_p1687915469454"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0224276697_p187911463455"><a name="zh-cn_topic_0224276697_p187911463455"></a><a name="zh-cn_topic_0224276697_p187911463455"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276697_row5877154616452"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276697_p18879114613450"><a name="zh-cn_topic_0224276697_p18879114613450"></a><a name="zh-cn_topic_0224276697_p18879114613450"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276697_p17879194614453"><a name="zh-cn_topic_0224276697_p17879194614453"></a><a name="zh-cn_topic_0224276697_p17879194614453"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row38771546204519"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276697_p1387964615454"><a name="zh-cn_topic_0224276697_p1387964615454"></a><a name="zh-cn_topic_0224276697_p1387964615454"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276697_p5880346144514"><a name="zh-cn_topic_0224276697_p5880346144514"></a><a name="zh-cn_topic_0224276697_p5880346144514"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row987719468457"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276697_p788024644512"><a name="zh-cn_topic_0224276697_p788024644512"></a><a name="zh-cn_topic_0224276697_p788024644512"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276697_p1088012467450"><a name="zh-cn_topic_0224276697_p1088012467450"></a><a name="zh-cn_topic_0224276697_p1088012467450"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row3877124614513"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276697_p38803464450"><a name="zh-cn_topic_0224276697_p38803464450"></a><a name="zh-cn_topic_0224276697_p38803464450"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276697_p0880104610451"><a name="zh-cn_topic_0224276697_p0880104610451"></a><a name="zh-cn_topic_0224276697_p0880104610451"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row88774468452"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276697_p1188124614454"><a name="zh-cn_topic_0224276697_p1188124614454"></a><a name="zh-cn_topic_0224276697_p1188124614454"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276697_p2088113466456"><a name="zh-cn_topic_0224276697_p2088113466456"></a><a name="zh-cn_topic_0224276697_p2088113466456"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row1877846184511"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276697_p17881204613452"><a name="zh-cn_topic_0224276697_p17881204613452"></a><a name="zh-cn_topic_0224276697_p17881204613452"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276697_p188813463456"><a name="zh-cn_topic_0224276697_p188813463456"></a><a name="zh-cn_topic_0224276697_p188813463456"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row15877164654513"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276697_p108827462454"><a name="zh-cn_topic_0224276697_p108827462454"></a><a name="zh-cn_topic_0224276697_p108827462454"></a>409</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276697_p198821446194517"><a name="zh-cn_topic_0224276697_p198821446194517"></a><a name="zh-cn_topic_0224276697_p198821446194517"></a>资源冲突。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row887711461455"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276697_p1188214461459"><a name="zh-cn_topic_0224276697_p1188214461459"></a><a name="zh-cn_topic_0224276697_p1188214461459"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276697_p208825463456"><a name="zh-cn_topic_0224276697_p208825463456"></a><a name="zh-cn_topic_0224276697_p208825463456"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row9877246144518"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276697_p11882164684511"><a name="zh-cn_topic_0224276697_p11882164684511"></a><a name="zh-cn_topic_0224276697_p11882164684511"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276697_p28833465457"><a name="zh-cn_topic_0224276697_p28833465457"></a><a name="zh-cn_topic_0224276697_p28833465457"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276697_row18772046164514"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276697_p16883194617452"><a name="zh-cn_topic_0224276697_p16883194617452"></a><a name="zh-cn_topic_0224276697_p16883194617452"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276697_p20883246204517"><a name="zh-cn_topic_0224276697_p20883246204517"></a><a name="zh-cn_topic_0224276697_p20883246204517"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0224276697_section11883174612459"></a>

无

