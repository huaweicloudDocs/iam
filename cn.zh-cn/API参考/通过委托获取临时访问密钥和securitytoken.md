# 通过委托获取临时访问密钥和securitytoken<a name="iam_04_0101"></a>

## 功能介绍<a name="zh-cn_topic_0221482378_section4164107182010"></a>

该接口可以用于通过委托来获取临时访问密钥（临时AK/SK）和securitytoken。

临时AK/SK和securitytoken是系统颁发给IAM用户的临时访问令牌，有效期为15分钟至24小时，过期后需要重新获取。临时AK/SK和securitytoken遵循权限最小化原则。鉴权时，临时AK/SK和securitytoken必须同时使用，请求头中需要添加“x-security-token”字段，使用方法详情请参考：[API签名参考](https://support.huaweicloud.com/devg-apisign/api-sign-provide.html)  。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="zh-cn_topic_0221482378_section2164117192016"></a>

POST /v3.0/OS-CREDENTIAL/securitytokens

## 请求参数<a name="zh-cn_topic_0221482378_section21646752019"></a>

**表 1**  请求Header参数

<a name="zh-cn_topic_0221482378_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482378_row1816567122017"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482378_p19165187132020"><a name="zh-cn_topic_0221482378_p19165187132020"></a><a name="zh-cn_topic_0221482378_p19165187132020"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482378_p191651271209"><a name="zh-cn_topic_0221482378_p191651271209"></a><a name="zh-cn_topic_0221482378_p191651271209"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482378_p0165127122019"><a name="zh-cn_topic_0221482378_p0165127122019"></a><a name="zh-cn_topic_0221482378_p0165127122019"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482378_p3166478206"><a name="zh-cn_topic_0221482378_p3166478206"></a><a name="zh-cn_topic_0221482378_p3166478206"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482378_row3165977204"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p71661278205"><a name="zh-cn_topic_0221482378_p71661278205"></a><a name="zh-cn_topic_0221482378_p71661278205"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p716616710209"><a name="zh-cn_topic_0221482378_p716616710209"></a><a name="zh-cn_topic_0221482378_p716616710209"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p61664722011"><a name="zh-cn_topic_0221482378_p61664722011"></a><a name="zh-cn_topic_0221482378_p61664722011"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p01666718203"><a name="zh-cn_topic_0221482378_p01666718203"></a><a name="zh-cn_topic_0221482378_p01666718203"></a>该字段填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row161651713204"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p716687162018"><a name="zh-cn_topic_0221482378_p716687162018"></a><a name="zh-cn_topic_0221482378_p716687162018"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p1216617162017"><a name="zh-cn_topic_0221482378_p1216617162017"></a><a name="zh-cn_topic_0221482378_p1216617162017"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p16166197122014"><a name="zh-cn_topic_0221482378_p16166197122014"></a><a name="zh-cn_topic_0221482378_p16166197122014"></a>String</p>
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
<p id="zh-cn_topic_0221482378_p71729772012"><a name="zh-cn_topic_0221482378_p71729772012"></a><a name="zh-cn_topic_0221482378_p71729772012"></a>取值范围：</p>
<a name="zh-cn_topic_0221482378_ul2172157192019"></a><a name="zh-cn_topic_0221482378_ul2172157192019"></a><ul id="zh-cn_topic_0221482378_ul2172157192019"><li>assume_role</li></ul>
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
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p1617414714203"><a name="zh-cn_topic_0221482378_p1617414714203"></a><a name="zh-cn_topic_0221482378_p1617414714203"></a>委托名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row191731174205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p817513718202"><a name="zh-cn_topic_0221482378_p817513718202"></a><a name="zh-cn_topic_0221482378_p817513718202"></a>domain_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p14175770200"><a name="zh-cn_topic_0221482378_p14175770200"></a><a name="zh-cn_topic_0221482378_p14175770200"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p617517732014"><a name="zh-cn_topic_0221482378_p617517732014"></a><a name="zh-cn_topic_0221482378_p617517732014"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p017517182013"><a name="zh-cn_topic_0221482378_p017517182013"></a><a name="zh-cn_topic_0221482378_p017517182013"></a>委托方的账号ID。“domain_id”与“domain_name”至少填写一个。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row131738718209"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p181754782014"><a name="zh-cn_topic_0221482378_p181754782014"></a><a name="zh-cn_topic_0221482378_p181754782014"></a>domain_name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p17175673202"><a name="zh-cn_topic_0221482378_p17175673202"></a><a name="zh-cn_topic_0221482378_p17175673202"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p917514714206"><a name="zh-cn_topic_0221482378_p917514714206"></a><a name="zh-cn_topic_0221482378_p917514714206"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p517577182012"><a name="zh-cn_topic_0221482378_p517577182012"></a><a name="zh-cn_topic_0221482378_p517577182012"></a>委托方的账号名。“domain_id”与“domain_name”至少填写一个。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482378_row9173107182015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482378_p8176157172016"><a name="zh-cn_topic_0221482378_p8176157172016"></a><a name="zh-cn_topic_0221482378_p8176157172016"></a>duration-seconds</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482378_p2176167122011"><a name="zh-cn_topic_0221482378_p2176167122011"></a><a name="zh-cn_topic_0221482378_p2176167122011"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482378_p191766772013"><a name="zh-cn_topic_0221482378_p191766772013"></a><a name="zh-cn_topic_0221482378_p191766772013"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p111767732018"><a name="zh-cn_topic_0221482378_p111767732018"></a><a name="zh-cn_topic_0221482378_p111767732018"></a>AK/SK和securitytoken的有效期，时间单位为秒。取值范围：15min ~ 24h ，默认为15min。</p>
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
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482378_p1517814772015"><a name="zh-cn_topic_0221482378_p1517814772015"></a><a name="zh-cn_topic_0221482378_p1517814772015"></a>委托方对应的企业用户名。用户名需满足如下规则：长度5~32，只能包含大写字母、小写字母、数字（0-9）、特殊字符（"-"与"_"）且只能以字母开头。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482378_section317818742015"></a>

**表 7**  响应Body参数

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

**表 8**  credential

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
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482378_p91813714205"><a name="zh-cn_topic_0221482378_p91813714205"></a><a name="zh-cn_topic_0221482378_p91813714205"></a>AK/SK和securitytoken的过期时间。</p>
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
                    "duration-seconds": 3600,
                    "session_user": {
                        "name": "SessionUserName"
                    }
                }
            }
        }
    }
    ```

-   不填写"session\_user"参数。

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
                    "duration-seconds": 3600
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
        "access": "E6DX0TF2ZREQ4ZAVM5CS",
        "expires_at": "2020-01-08T02:56:19.587000Z",
        "secret": "w9ePum0qdfac39ErLD0UdjofYkqort6Iw2bmR6Si",
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

