# 通过委托获取临时访问密钥和securitytoken<a name="iam_04_0101"></a>

## 功能介绍<a name="zh-cn_topic_0221482378_section4164107182010"></a>

该接口可以用于通过委托来获取临时访问密钥（临时AK/SK）和securitytoken。

临时AK/SK和securitytoken是系统颁发给IAM用户的临时访问令牌，有效期可在15分钟至24小时范围内设置，过期后需要重新获取。临时AK/SK和securitytoken遵循权限最小化原则。鉴权时，临时AK/SK和securitytoken必须同时使用，请求头中需要添加“x-security-token”字段，使用方法详情请参考：[使用临时AK/SK做签名](https://support.huaweicloud.com/devg-apisign/api-sign-securetoken.html)。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section11353191120537"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=CreateTemporaryAccessKeyByAgency)中调试该接口。

## URI<a name="zh-cn_topic_0221482378_section2164117192016"></a>

POST /v3.0/OS-CREDENTIAL/securitytokens

## 请求参数<a name="zh-cn_topic_0221482378_section21646752019"></a>

**表 1**  请求Header参数

<a name="zh-cn_topic_0221482378_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482378_row1816567122017"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482378_p19165187132020"><a name="zh-cn_topic_0221482378_p19165187132020"></a><a name="zh-cn_topic_0221482378_p19165187132020"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.33%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482378_p191651271209"><a name="zh-cn_topic_0221482378_p191651271209"></a><a name="zh-cn_topic_0221482378_p191651271209"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20.669999999999998%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482378_p0165127122019"><a name="zh-cn_topic_0221482378_p0165127122019"></a><a name="zh-cn_topic_0221482378_p0165127122019"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482378_p3166478206"><a name="zh-cn_topic_0221482378_p3166478206"></a><a name="zh-cn_topic_0221482378_p3166478206"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482378_row3165977204"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p71661278205"><a name="zh-cn_topic_0221482378_p71661278205"></a><a name="zh-cn_topic_0221482378_p71661278205"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="9.33%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p716616710209"><a name="zh-cn_topic_0221482378_p716616710209"></a><a name="zh-cn_topic_0221482378_p716616710209"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.669999999999998%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p61664722011"><a name="zh-cn_topic_0221482378_p61664722011"></a><a name="zh-cn_topic_0221482378_p61664722011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p01666718203"><a name="zh-cn_topic_0221482378_p01666718203"></a><a name="zh-cn_topic_0221482378_p01666718203"></a>该字段填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row161651713204"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p716687162018"><a name="zh-cn_topic_0221482378_p716687162018"></a><a name="zh-cn_topic_0221482378_p716687162018"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="9.33%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p1216617162017"><a name="zh-cn_topic_0221482378_p1216617162017"></a><a name="zh-cn_topic_0221482378_p1216617162017"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.669999999999998%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p16166197122014"><a name="zh-cn_topic_0221482378_p16166197122014"></a><a name="zh-cn_topic_0221482378_p16166197122014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p1616719762010"><a name="zh-cn_topic_0221482378_p1616719762010"></a><a name="zh-cn_topic_0221482378_p1616719762010"></a>拥有Agent Operator权限的token。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  请求Body参数

<a name="zh-cn_topic_0221482378_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482378_row61676742019"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482378_p18167373207"><a name="zh-cn_topic_0221482378_p18167373207"></a><a name="zh-cn_topic_0221482378_p18167373207"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482378_p15167972204"><a name="zh-cn_topic_0221482378_p15167972204"></a><a name="zh-cn_topic_0221482378_p15167972204"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482378_p6167207102017"><a name="zh-cn_topic_0221482378_p6167207102017"></a><a name="zh-cn_topic_0221482378_p6167207102017"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482378_p1416820710200"><a name="zh-cn_topic_0221482378_p1416820710200"></a><a name="zh-cn_topic_0221482378_p1416820710200"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482378_row17167157172015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p13168375205"><a name="zh-cn_topic_0221482378_p13168375205"></a><a name="zh-cn_topic_0221482378_p13168375205"></a><a href="#zh-cn_topic_0221482378_request_Rq41Auth">auth</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p12168107112016"><a name="zh-cn_topic_0221482378_p12168107112016"></a><a name="zh-cn_topic_0221482378_p12168107112016"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p8168172202"><a name="zh-cn_topic_0221482378_p8168172202"></a><a name="zh-cn_topic_0221482378_p8168172202"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p41681676208"><a name="zh-cn_topic_0221482378_p41681676208"></a><a name="zh-cn_topic_0221482378_p41681676208"></a>认证信息。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  auth

<a name="zh-cn_topic_0221482378_request_Rq41Auth"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482378_row316815711201"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482378_p116987182010"><a name="zh-cn_topic_0221482378_p116987182010"></a><a name="zh-cn_topic_0221482378_p116987182010"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482378_p16169107192014"><a name="zh-cn_topic_0221482378_p16169107192014"></a><a name="zh-cn_topic_0221482378_p16169107192014"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482378_p9169377204"><a name="zh-cn_topic_0221482378_p9169377204"></a><a name="zh-cn_topic_0221482378_p9169377204"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482378_p1216913782016"><a name="zh-cn_topic_0221482378_p1216913782016"></a><a name="zh-cn_topic_0221482378_p1216913782016"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482378_row616887112018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p141693718208"><a name="zh-cn_topic_0221482378_p141693718208"></a><a name="zh-cn_topic_0221482378_p141693718208"></a><a href="#zh-cn_topic_0221482378_request_Rq41AuthIdentity">identity</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p11169873206"><a name="zh-cn_topic_0221482378_p11169873206"></a><a name="zh-cn_topic_0221482378_p11169873206"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p19170673208"><a name="zh-cn_topic_0221482378_p19170673208"></a><a name="zh-cn_topic_0221482378_p19170673208"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p171709717202"><a name="zh-cn_topic_0221482378_p171709717202"></a><a name="zh-cn_topic_0221482378_p171709717202"></a>认证参数。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  auth.identity

<a name="zh-cn_topic_0221482378_request_Rq41AuthIdentity"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482378_row181708792018"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482378_p141711776209"><a name="zh-cn_topic_0221482378_p141711776209"></a><a name="zh-cn_topic_0221482378_p141711776209"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482378_p217127182018"><a name="zh-cn_topic_0221482378_p217127182018"></a><a name="zh-cn_topic_0221482378_p217127182018"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482378_p1317116710208"><a name="zh-cn_topic_0221482378_p1317116710208"></a><a name="zh-cn_topic_0221482378_p1317116710208"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482378_p11711372209"><a name="zh-cn_topic_0221482378_p11711372209"></a><a name="zh-cn_topic_0221482378_p11711372209"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482378_row1617012762010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p817197152019"><a name="zh-cn_topic_0221482378_p817197152019"></a><a name="zh-cn_topic_0221482378_p817197152019"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p4171197172016"><a name="zh-cn_topic_0221482378_p4171197172016"></a><a name="zh-cn_topic_0221482378_p4171197172016"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p71719742013"><a name="zh-cn_topic_0221482378_p71719742013"></a><a name="zh-cn_topic_0221482378_p71719742013"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p81712782010"><a name="zh-cn_topic_0221482378_p81712782010"></a><a name="zh-cn_topic_0221482378_p81712782010"></a>认证方法，该字段内容为["assume_role"]。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row1917017717204"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p1317215742015"><a name="zh-cn_topic_0221482378_p1317215742015"></a><a name="zh-cn_topic_0221482378_p1317215742015"></a><a href="#zh-cn_topic_0221482378_request_Rq41AuthIdentityAssumerole">assume_role</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p21721272201"><a name="zh-cn_topic_0221482378_p21721272201"></a><a name="zh-cn_topic_0221482378_p21721272201"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p817218712208"><a name="zh-cn_topic_0221482378_p817218712208"></a><a name="zh-cn_topic_0221482378_p817218712208"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p171734714204"><a name="zh-cn_topic_0221482378_p171734714204"></a><a name="zh-cn_topic_0221482378_p171734714204"></a>assume_role的具体信息。</p>
</td>
</tr>
<tr id="row155916652116"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p15560563213"><a name="p15560563213"></a><a name="p15560563213"></a><a href="#zh-cn_topic_0222037452_request_Rq113RolePolicy">policy</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p3560669212"><a name="p3560669212"></a><a name="p3560669212"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1256012682116"><a name="p1256012682116"></a><a name="p1256012682116"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1520617581232"><a name="p1520617581232"></a><a name="p1520617581232"></a>用户自定义策略的信息，用于限制获取到的临时访问密钥和securitytoken的权限（当前仅适用限制OBS服务的权限）。</p>
<p id="p14933929171915"><a name="p14933929171915"></a><a name="p14933929171915"></a>如果填写此参数，则临时访问密钥和securitytoken的权限为：委托具有的权限和policy参数限制的权限交集。</p>
<p id="p940710389714"><a name="p940710389714"></a><a name="p940710389714"></a>关于IAM策略的格式和语法，请参考：<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0017.html" target="_blank" rel="noopener noreferrer">策略</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  auth.identity.assume\_role

<a name="zh-cn_topic_0221482378_request_Rq41AuthIdentityAssumerole"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482378_row141731079202"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482378_p017410717207"><a name="zh-cn_topic_0221482378_p017410717207"></a><a name="zh-cn_topic_0221482378_p017410717207"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482378_p13174127162010"><a name="zh-cn_topic_0221482378_p13174127162010"></a><a name="zh-cn_topic_0221482378_p13174127162010"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482378_p7174107122014"><a name="zh-cn_topic_0221482378_p7174107122014"></a><a name="zh-cn_topic_0221482378_p7174107122014"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482378_p141742719203"><a name="zh-cn_topic_0221482378_p141742719203"></a><a name="zh-cn_topic_0221482378_p141742719203"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482378_row117314772010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p91743717202"><a name="zh-cn_topic_0221482378_p91743717202"></a><a name="zh-cn_topic_0221482378_p91743717202"></a>agency_name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p91743772012"><a name="zh-cn_topic_0221482378_p91743772012"></a><a name="zh-cn_topic_0221482378_p91743772012"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p217414762018"><a name="zh-cn_topic_0221482378_p217414762018"></a><a name="zh-cn_topic_0221482378_p217414762018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p1617414714203"><a name="zh-cn_topic_0221482378_p1617414714203"></a><a name="zh-cn_topic_0221482378_p1617414714203"></a>委托名称，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row191731174205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p817513718202"><a name="zh-cn_topic_0221482378_p817513718202"></a><a name="zh-cn_topic_0221482378_p817513718202"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p14175770200"><a name="zh-cn_topic_0221482378_p14175770200"></a><a name="zh-cn_topic_0221482378_p14175770200"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p617517732014"><a name="zh-cn_topic_0221482378_p617517732014"></a><a name="zh-cn_topic_0221482378_p617517732014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p017517182013"><a name="zh-cn_topic_0221482378_p017517182013"></a><a name="zh-cn_topic_0221482378_p017517182013"></a>委托方的帐号ID。“domain_id”与“domain_name”至少填写一个，建议选择“domain_id”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row131738718209"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p181754782014"><a name="zh-cn_topic_0221482378_p181754782014"></a><a name="zh-cn_topic_0221482378_p181754782014"></a>domain_name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p17175673202"><a name="zh-cn_topic_0221482378_p17175673202"></a><a name="zh-cn_topic_0221482378_p17175673202"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p917514714206"><a name="zh-cn_topic_0221482378_p917514714206"></a><a name="zh-cn_topic_0221482378_p917514714206"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p517577182012"><a name="zh-cn_topic_0221482378_p517577182012"></a><a name="zh-cn_topic_0221482378_p517577182012"></a>委托方的帐号名。“domain_id”与“domain_name”至少填写一个，建议选择“domain_id”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row9173107182015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p8176157172016"><a name="zh-cn_topic_0221482378_p8176157172016"></a><a name="zh-cn_topic_0221482378_p8176157172016"></a>duration_seconds</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p2176167122011"><a name="zh-cn_topic_0221482378_p2176167122011"></a><a name="zh-cn_topic_0221482378_p2176167122011"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p191766772013"><a name="zh-cn_topic_0221482378_p191766772013"></a><a name="zh-cn_topic_0221482378_p191766772013"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p111767732018"><a name="zh-cn_topic_0221482378_p111767732018"></a><a name="zh-cn_topic_0221482378_p111767732018"></a>AK/SK和securitytoken的有效期，时间单位为秒。取值范围：15分钟 ~ 24小时 ，默认为15分钟。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row1517319718205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p917613782016"><a name="zh-cn_topic_0221482378_p917613782016"></a><a name="zh-cn_topic_0221482378_p917613782016"></a><a href="#zh-cn_topic_0221482378_request_Rq41AuthIdentityAssumeroleSessionuser">session_user</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p21761973207"><a name="zh-cn_topic_0221482378_p21761973207"></a><a name="zh-cn_topic_0221482378_p21761973207"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p117618718201"><a name="zh-cn_topic_0221482378_p117618718201"></a><a name="zh-cn_topic_0221482378_p117618718201"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p171765782017"><a name="zh-cn_topic_0221482378_p171765782017"></a><a name="zh-cn_topic_0221482378_p171765782017"></a>委托方对应的企业用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  auth.identity.assume\_role.session\_user

<a name="zh-cn_topic_0221482378_request_Rq41AuthIdentityAssumeroleSessionuser"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482378_row1317787112014"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482378_p141771702015"><a name="zh-cn_topic_0221482378_p141771702015"></a><a name="zh-cn_topic_0221482378_p141771702015"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482378_p017715718208"><a name="zh-cn_topic_0221482378_p017715718208"></a><a name="zh-cn_topic_0221482378_p017715718208"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482378_p151777742019"><a name="zh-cn_topic_0221482378_p151777742019"></a><a name="zh-cn_topic_0221482378_p151777742019"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482378_p9178137202013"><a name="zh-cn_topic_0221482378_p9178137202013"></a><a name="zh-cn_topic_0221482378_p9178137202013"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482378_row91773712010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p817816714202"><a name="zh-cn_topic_0221482378_p817816714202"></a><a name="zh-cn_topic_0221482378_p817816714202"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p101782712010"><a name="zh-cn_topic_0221482378_p101782712010"></a><a name="zh-cn_topic_0221482378_p101782712010"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p61788782018"><a name="zh-cn_topic_0221482378_p61788782018"></a><a name="zh-cn_topic_0221482378_p61788782018"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p19296131131619"><a name="p19296131131619"></a><a name="p19296131131619"></a>委托方对应的企业用户名。</p>
<p id="zh-cn_topic_0221482378_p1517814772015"><a name="zh-cn_topic_0221482378_p1517814772015"></a><a name="zh-cn_topic_0221482378_p1517814772015"></a>用户名需满足如下规则：长度1~32之间，只能包含如下字符：大小写字母、空格、数字或特殊字符（-_.）且只能以字母开头。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  auth.identity.policy

<a name="zh-cn_topic_0222037452_request_Rq113RolePolicy"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037452_row1942418501331"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0222037452_p64251350330"><a name="zh-cn_topic_0222037452_p64251350330"></a><a name="zh-cn_topic_0222037452_p64251350330"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0222037452_p642518501933"><a name="zh-cn_topic_0222037452_p642518501933"></a><a name="zh-cn_topic_0222037452_p642518501933"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0222037452_p1425250434"><a name="zh-cn_topic_0222037452_p1425250434"></a><a name="zh-cn_topic_0222037452_p1425250434"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0222037452_p64256507310"><a name="zh-cn_topic_0222037452_p64256507310"></a><a name="zh-cn_topic_0222037452_p64256507310"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037452_row194251950530"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0222037452_p24254501635"><a name="zh-cn_topic_0222037452_p24254501635"></a><a name="zh-cn_topic_0222037452_p24254501635"></a>Version</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0222037452_p24251350437"><a name="zh-cn_topic_0222037452_p24251350437"></a><a name="zh-cn_topic_0222037452_p24251350437"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0222037452_p542611507311"><a name="zh-cn_topic_0222037452_p542611507311"></a><a name="zh-cn_topic_0222037452_p542611507311"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0222037452_p3427950739"><a name="zh-cn_topic_0222037452_p3427950739"></a><a name="zh-cn_topic_0222037452_p3427950739"></a>权限版本号，创建自定义策略时，该字段值填为“1.1”。</p>
<div class="note" id="zh-cn_topic_0222037452_note124277504318"><a name="zh-cn_topic_0222037452_note124277504318"></a><a name="zh-cn_topic_0222037452_note124277504318"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1784903783218"><a name="p1784903783218"></a><a name="p1784903783218"></a>1.1：策略。IAM最新提供的一种细粒度授权的能力，可以精确到具体服务的操作、资源以及请求条件等。</p>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0222037452_row94251650038"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0222037452_p104274504313"><a name="zh-cn_topic_0222037452_p104274504313"></a><a name="zh-cn_topic_0222037452_p104274504313"></a><a href="#zh-cn_topic_0222037452_request_Rq113RolePolicyStatementArritem">Statement</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0222037452_p6427850033"><a name="zh-cn_topic_0222037452_p6427850033"></a><a name="zh-cn_topic_0222037452_p6427850033"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0222037452_p1442711505311"><a name="zh-cn_topic_0222037452_p1442711505311"></a><a name="zh-cn_topic_0222037452_p1442711505311"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0222037452_p174282501536"><a name="zh-cn_topic_0222037452_p174282501536"></a><a name="zh-cn_topic_0222037452_p174282501536"></a>授权语句，描述自定义策略的具体内容，不超过8个。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  auth.identity.policy.Statement

<a name="zh-cn_topic_0222037452_request_Rq113RolePolicyStatementArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037452_row194281150539"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0222037452_p142865019318"><a name="zh-cn_topic_0222037452_p142865019318"></a><a name="zh-cn_topic_0222037452_p142865019318"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0222037452_p6428175016317"><a name="zh-cn_topic_0222037452_p6428175016317"></a><a name="zh-cn_topic_0222037452_p6428175016317"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0222037452_p5429750336"><a name="zh-cn_topic_0222037452_p5429750336"></a><a name="zh-cn_topic_0222037452_p5429750336"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0222037452_p1342945017311"><a name="zh-cn_topic_0222037452_p1342945017311"></a><a name="zh-cn_topic_0222037452_p1342945017311"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037452_row24281450534"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0222037452_p5429165016320"><a name="zh-cn_topic_0222037452_p5429165016320"></a><a name="zh-cn_topic_0222037452_p5429165016320"></a>Action</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0222037452_p5429165016314"><a name="zh-cn_topic_0222037452_p5429165016314"></a><a name="zh-cn_topic_0222037452_p5429165016314"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0222037452_p1543016509316"><a name="zh-cn_topic_0222037452_p1543016509316"></a><a name="zh-cn_topic_0222037452_p1543016509316"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0222037452_p9430175011313"><a name="zh-cn_topic_0222037452_p9430175011313"></a><a name="zh-cn_topic_0222037452_p9430175011313"></a>授权项，指对资源的具体操作权限，不超过100个。</p>
<div class="note" id="zh-cn_topic_0222037452_note1743113501237"><a name="zh-cn_topic_0222037452_note1743113501237"></a><a name="zh-cn_topic_0222037452_note1743113501237"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0222037452_ul1743145019314"></a><a name="zh-cn_topic_0222037452_ul1743145019314"></a><ul id="zh-cn_topic_0222037452_ul1743145019314"><li>格式为：服务名:资源类型:操作，例：vpc:ports:create。</li><li>服务名为产品名称，例如ecs、evs和vpc等，服务名仅支持小写。 资源类型和操作没有大小写，要求支持通配符号*，无需罗列全部授权项。</li></ul>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0222037452_row18428185014319"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0222037452_p184316501337"><a name="zh-cn_topic_0222037452_p184316501337"></a><a name="zh-cn_topic_0222037452_p184316501337"></a>Effect</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0222037452_p24311150832"><a name="zh-cn_topic_0222037452_p24311150832"></a><a name="zh-cn_topic_0222037452_p24311150832"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0222037452_p1443111501317"><a name="zh-cn_topic_0222037452_p1443111501317"></a><a name="zh-cn_topic_0222037452_p1443111501317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0222037452_p54316501734"><a name="zh-cn_topic_0222037452_p54316501734"></a><a name="zh-cn_topic_0222037452_p54316501734"></a>作用。包含两种：允许（Allow）和拒绝（Deny），既有Allow又有Deny的授权语句时，遵循Deny优先的原则。</p>
<p id="zh-cn_topic_0222037452_p7431145016317"><a name="zh-cn_topic_0222037452_p7431145016317"></a><a name="zh-cn_topic_0222037452_p7431145016317"></a>取值范围：</p>
<a name="zh-cn_topic_0222037452_ul1843113505315"></a><a name="zh-cn_topic_0222037452_ul1843113505315"></a><ul id="zh-cn_topic_0222037452_ul1843113505315"><li>Allow</li><li>Deny</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0222037452_row174281850633"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0222037452_p943218502313"><a name="zh-cn_topic_0222037452_p943218502313"></a><a name="zh-cn_topic_0222037452_p943218502313"></a>Condition</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0222037452_p1943220501933"><a name="zh-cn_topic_0222037452_p1943220501933"></a><a name="zh-cn_topic_0222037452_p1943220501933"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0222037452_p174321501311"><a name="zh-cn_topic_0222037452_p174321501311"></a><a name="zh-cn_topic_0222037452_p174321501311"></a>Map&lt;String,Map&lt;String,Array&lt;String&gt;&gt;&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p139313435469"><a name="p139313435469"></a><a name="p139313435469"></a>限制条件。不超过10个。了解更多相关参数，请参考：<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0605.html#section1" target="_blank" rel="noopener noreferrer">配置自定义策略</a>。</p>
<div class="note" id="note122334794612"><a name="note122334794612"></a><a name="note122334794612"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1276712344919"><a name="p1276712344919"></a><a name="p1276712344919"></a>以请求示例中的Condition为例：条件键（obs:prefix）和字符串（public）需相等（StringEquals）。</p>
<pre class="screen" id="screen18948143318464"><a name="screen18948143318464"></a><a name="screen18948143318464"></a> "Condition": {
              "StringEquals": {
                "obs:prefix": [
                  "public"
                ]
              }
            }</pre>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0222037452_row54281350835"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0222037452_p164335501635"><a name="zh-cn_topic_0222037452_p164335501635"></a><a name="zh-cn_topic_0222037452_p164335501635"></a>Resource</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0222037452_p194331450436"><a name="zh-cn_topic_0222037452_p194331450436"></a><a name="zh-cn_topic_0222037452_p194331450436"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0222037452_p8433195017317"><a name="zh-cn_topic_0222037452_p8433195017317"></a><a name="zh-cn_topic_0222037452_p8433195017317"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0222037452_p343318501535"><a name="zh-cn_topic_0222037452_p343318501535"></a><a name="zh-cn_topic_0222037452_p343318501535"></a>资源。数组长度不超过10，每个字符串长度不超过128，规则如下：</p>
<div class="note" id="zh-cn_topic_0222037452_note04331650133"><a name="zh-cn_topic_0222037452_note04331650133"></a><a name="zh-cn_topic_0222037452_note04331650133"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul323415619329"></a><a name="ul323415619329"></a><ul id="ul323415619329"><li>格式为“服务名:region:domainId:资源类型:资源路径”, 资源类型支持通配符号*，通配符号*表示所有。如"obs:*:*:bucket:*": 表示所有的OBS桶。</li></ul>
<a name="zh-cn_topic_0222037452_ul2433185011318"></a><a name="zh-cn_topic_0222037452_ul2433185011318"></a><ul id="zh-cn_topic_0222037452_ul2433185011318"><li>region字段为*或用户可访问的region。service必须存在且resource属于对应service。</li></ul>
</div></div>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482378_section317818742015"></a>

**表 9**  响应Body参数

<a name="zh-cn_topic_0221482378_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482378_row91794714205"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482378_p117916716202"><a name="zh-cn_topic_0221482378_p117916716202"></a><a name="zh-cn_topic_0221482378_p117916716202"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482378_p15179074206"><a name="zh-cn_topic_0221482378_p15179074206"></a><a name="zh-cn_topic_0221482378_p15179074206"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482378_p1817912732014"><a name="zh-cn_topic_0221482378_p1817912732014"></a><a name="zh-cn_topic_0221482378_p1817912732014"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482378_row14179270209"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482378_p8180197182015"><a name="zh-cn_topic_0221482378_p8180197182015"></a><a name="zh-cn_topic_0221482378_p8180197182015"></a><a href="#zh-cn_topic_0221482378_response_Rs41Credential">credential</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482378_p918017711203"><a name="zh-cn_topic_0221482378_p918017711203"></a><a name="zh-cn_topic_0221482378_p918017711203"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482378_p91801877208"><a name="zh-cn_topic_0221482378_p91801877208"></a><a name="zh-cn_topic_0221482378_p91801877208"></a>认证结果信息。</p>
</td>
</tr>
</tbody>
</table>

**表 10**  credential

<a name="zh-cn_topic_0221482378_response_Rs41Credential"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482378_row71806711202"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482378_p1518127182011"><a name="zh-cn_topic_0221482378_p1518127182011"></a><a name="zh-cn_topic_0221482378_p1518127182011"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482378_p81814719206"><a name="zh-cn_topic_0221482378_p81814719206"></a><a name="zh-cn_topic_0221482378_p81814719206"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482378_p418110714209"><a name="zh-cn_topic_0221482378_p418110714209"></a><a name="zh-cn_topic_0221482378_p418110714209"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482378_row61803742018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482378_p918197102012"><a name="zh-cn_topic_0221482378_p918197102012"></a><a name="zh-cn_topic_0221482378_p918197102012"></a>expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482378_p1218110782020"><a name="zh-cn_topic_0221482378_p1218110782020"></a><a name="zh-cn_topic_0221482378_p1218110782020"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482378_p91813714205"><a name="zh-cn_topic_0221482378_p91813714205"></a><a name="zh-cn_topic_0221482378_p91813714205"></a>AK/SK和securitytoken的过期时间。响应参数为UTC时间格式，北京时间为UTC+8小时。</p>
<p id="p765214113919"><a name="p765214113919"></a><a name="p765214113919"></a>如返回：</p>
<pre class="screen" id="screen1965014116391"><a name="screen1965014116391"></a><a name="screen1965014116391"></a>"expires_at": "2020-01-08T02:56:19.587000Z"</pre>
<p id="p17393151111394"><a name="p17393151111394"></a><a name="p17393151111394"></a>北京时间：2020-01-08 10:56:19.587</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row1318017142014"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482378_p718267122014"><a name="zh-cn_topic_0221482378_p718267122014"></a><a name="zh-cn_topic_0221482378_p718267122014"></a>access</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482378_p20182197182016"><a name="zh-cn_topic_0221482378_p20182197182016"></a><a name="zh-cn_topic_0221482378_p20182197182016"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482378_p31821074206"><a name="zh-cn_topic_0221482378_p31821074206"></a><a name="zh-cn_topic_0221482378_p31821074206"></a>获取的AK。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row1818018742018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482378_p618210722013"><a name="zh-cn_topic_0221482378_p618210722013"></a><a name="zh-cn_topic_0221482378_p618210722013"></a>secret</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482378_p1318219710206"><a name="zh-cn_topic_0221482378_p1318219710206"></a><a name="zh-cn_topic_0221482378_p1318219710206"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482378_p818287102013"><a name="zh-cn_topic_0221482378_p818287102013"></a><a name="zh-cn_topic_0221482378_p818287102013"></a>获取的SK。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row81801372200"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482378_p1618318718201"><a name="zh-cn_topic_0221482378_p1618318718201"></a><a name="zh-cn_topic_0221482378_p1618318718201"></a>securitytoken</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482378_p12183147202019"><a name="zh-cn_topic_0221482378_p12183147202019"></a><a name="zh-cn_topic_0221482378_p12183147202019"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482378_p91834713204"><a name="zh-cn_topic_0221482378_p91834713204"></a><a name="zh-cn_topic_0221482378_p91834713204"></a>securitytoken是将所获的AK、SK等信息进行加密后的字符串。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482378_section1418315792013"></a>

-   填写"session\_user"参数。

    ```
    POST https://iam.myhuaweicloud.com/v3.0/OS-CREDENTIAL/securitytokens
    ```

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "assume_role"
                ],
                "assume_role": {
                    "domain_name": "IAMDomainA",
                    "agency_name": "IAMAgency",
                    "duration_seconds": 3600,
                    "session_user": {
                        "name": "SessionUserName"
                    }
                }
            }
        }
    }
    ```

-   填写"policy"参数。

    ```
    POST https://iam.myhuaweicloud.com/v3.0/OS-CREDENTIAL/securitytokens
    ```

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "assume_role"
                ],
                "policy": {
                          "Version": "1.1",
    		       "Statement": [{
    			 "Effect": "allow",
    			 "Action": [
                             "obs:object:*"
                             ],
    			 "Resource": ["obs:*:*:object:*"],
    			 "Condition": {
    			    "StringEquals": {
    				"obs:prefix": ["public"]
    				}
    			}
    		}]
                 },
                "assume_role": {
                    "domain_name": "IAMDomainA",
                    "agency_name": "IAMAgency",
                    "duration_seconds": 3600
    
                }
            }
        }
    }
    ```


-   不填写"session\_user"和policy参数。

    ```
    POST https://iam.myhuaweicloud.com/v3.0/OS-CREDENTIAL/securitytokens
    ```

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "assume_role"
                ],
                "assume_role": {
                    "domain_name": "IAMDomainA",
                    "agency_name": "IAMAgency",
                    "duration_seconds": 3600
                }
            }
        }
    }
    ```


## 响应示例<a name="zh-cn_topic_0221482378_section101861574204"></a>

**状态码为 201 时:**

创建成功。

无论session\_user填写与否，返回都是相同的。若填写了session\_user，则在securitytoken中包含了所填写的session\_user信息。

```
{
    "credential": {
        "access": "E6DX0TF2ZREQ4Z...",
        "expires_at": "2020-01-08T02:56:19.587000Z",
        "secret": "w9ePum0qdfac39ErLD0UdjofYkqort6Iw....",
        "securitytoken": "gQpjbi1ub3J0aC0..."
    }
}
```

## 返回值<a name="zh-cn_topic_0221482378_section31871770206"></a>

<a name="zh-cn_topic_0221482378_table2420"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482378_row101871078202"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482378_p71884715200"><a name="zh-cn_topic_0221482378_p71884715200"></a><a name="zh-cn_topic_0221482378_p71884715200"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482378_p818811792011"><a name="zh-cn_topic_0221482378_p818811792011"></a><a name="zh-cn_topic_0221482378_p818811792011"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482378_row7187778207"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482378_p2188976202"><a name="zh-cn_topic_0221482378_p2188976202"></a><a name="zh-cn_topic_0221482378_p2188976202"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482378_p91882722015"><a name="zh-cn_topic_0221482378_p91882722015"></a><a name="zh-cn_topic_0221482378_p91882722015"></a>创建成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row1218727202016"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482378_p111881676201"><a name="zh-cn_topic_0221482378_p111881676201"></a><a name="zh-cn_topic_0221482378_p111881676201"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482378_p41881673209"><a name="zh-cn_topic_0221482378_p41881673209"></a><a name="zh-cn_topic_0221482378_p41881673209"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row191871771207"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482378_p161881710202"><a name="zh-cn_topic_0221482378_p161881710202"></a><a name="zh-cn_topic_0221482378_p161881710202"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482378_p1218912792014"><a name="zh-cn_topic_0221482378_p1218912792014"></a><a name="zh-cn_topic_0221482378_p1218912792014"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row21871071205"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482378_p8189117172013"><a name="zh-cn_topic_0221482378_p8189117172013"></a><a name="zh-cn_topic_0221482378_p8189117172013"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482378_p818916752020"><a name="zh-cn_topic_0221482378_p818916752020"></a><a name="zh-cn_topic_0221482378_p818916752020"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row161871278202"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482378_p9189107112010"><a name="zh-cn_topic_0221482378_p9189107112010"></a><a name="zh-cn_topic_0221482378_p9189107112010"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482378_p161896719207"><a name="zh-cn_topic_0221482378_p161896719207"></a><a name="zh-cn_topic_0221482378_p161896719207"></a>内部服务错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482378_section218919715203"></a>

无

