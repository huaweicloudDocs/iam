# 通过token获取临时访问密钥和securitytoken<a name="zh-cn_topic_0097949518"></a>

## 功能介绍<a name="zh-cn_topic_0221482424_section1524018722012"></a>

该接口可以用于通过token来获取临时AK/SK和securitytoken。

临时AK/SK和securitytoken是系统颁发给IAM用户的临时访问令牌，有效期为15分钟至24小时，过期后需要重新获取。临时AK/SK和securitytoken遵循权限最小化原则。鉴权时，临时AK/SK和securitytoken必须同时使用，请求头中需要添加“x-security-token”字段，使用方法详情请参考：[API签名参考](https://support.huaweicloud.com/devg-apisign/api-sign-provide.html)  。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="zh-cn_topic_0221482424_section524077132016"></a>

POST /v3.0/OS-CREDENTIAL/securitytokens

## 请求参数<a name="zh-cn_topic_0221482424_section1824112714203"></a>

**表 1**  请求Header参数

<a name="zh-cn_topic_0221482424_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482424_row824177142018"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482424_p13242671208"><a name="zh-cn_topic_0221482424_p13242671208"></a><a name="zh-cn_topic_0221482424_p13242671208"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482424_p1424227152018"><a name="zh-cn_topic_0221482424_p1424227152018"></a><a name="zh-cn_topic_0221482424_p1424227152018"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482424_p1324237132014"><a name="zh-cn_topic_0221482424_p1324237132014"></a><a name="zh-cn_topic_0221482424_p1324237132014"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482424_p10242107202011"><a name="zh-cn_topic_0221482424_p10242107202011"></a><a name="zh-cn_topic_0221482424_p10242107202011"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482424_row1924116717204"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482424_p12421711209"><a name="zh-cn_topic_0221482424_p12421711209"></a><a name="zh-cn_topic_0221482424_p12421711209"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482424_p32421072200"><a name="zh-cn_topic_0221482424_p32421072200"></a><a name="zh-cn_topic_0221482424_p32421072200"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482424_p72430719208"><a name="zh-cn_topic_0221482424_p72430719208"></a><a name="zh-cn_topic_0221482424_p72430719208"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482424_p132432722010"><a name="zh-cn_topic_0221482424_p132432722010"></a><a name="zh-cn_topic_0221482424_p132432722010"></a>该字段填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482424_row192419772018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482424_p1124315712208"><a name="zh-cn_topic_0221482424_p1124315712208"></a><a name="zh-cn_topic_0221482424_p1124315712208"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482424_p1424397162011"><a name="zh-cn_topic_0221482424_p1424397162011"></a><a name="zh-cn_topic_0221482424_p1424397162011"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482424_p152430710202"><a name="zh-cn_topic_0221482424_p152430710202"></a><a name="zh-cn_topic_0221482424_p152430710202"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482424_p824310714204"><a name="zh-cn_topic_0221482424_p824310714204"></a><a name="zh-cn_topic_0221482424_p824310714204"></a>IAM用户token或联邦用户的token或委托token，该参数与请求体中的“auth.token.id”填写其一即可，若都填写，优先校验X-Auth-Token。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  请求Body参数

<a name="zh-cn_topic_0221482424_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482424_row42431672201"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482424_p1244377206"><a name="zh-cn_topic_0221482424_p1244377206"></a><a name="zh-cn_topic_0221482424_p1244377206"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482424_p11244107102020"><a name="zh-cn_topic_0221482424_p11244107102020"></a><a name="zh-cn_topic_0221482424_p11244107102020"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482424_p72443714203"><a name="zh-cn_topic_0221482424_p72443714203"></a><a name="zh-cn_topic_0221482424_p72443714203"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482424_p10244972206"><a name="zh-cn_topic_0221482424_p10244972206"></a><a name="zh-cn_topic_0221482424_p10244972206"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482424_row92431973203"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482424_p1124412710203"><a name="zh-cn_topic_0221482424_p1124412710203"></a><a name="zh-cn_topic_0221482424_p1124412710203"></a><a href="#zh-cn_topic_0221482424_request_Rq4100Auth">auth</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482424_p122448711206"><a name="zh-cn_topic_0221482424_p122448711206"></a><a name="zh-cn_topic_0221482424_p122448711206"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482424_p824511719209"><a name="zh-cn_topic_0221482424_p824511719209"></a><a name="zh-cn_topic_0221482424_p824511719209"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482424_p1524517102018"><a name="zh-cn_topic_0221482424_p1524517102018"></a><a name="zh-cn_topic_0221482424_p1524517102018"></a>认证信息。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  auth

<a name="zh-cn_topic_0221482424_request_Rq4100Auth"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482424_row1245575209"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482424_p1824597152020"><a name="zh-cn_topic_0221482424_p1824597152020"></a><a name="zh-cn_topic_0221482424_p1824597152020"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482424_p924613711202"><a name="zh-cn_topic_0221482424_p924613711202"></a><a name="zh-cn_topic_0221482424_p924613711202"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482424_p12466782010"><a name="zh-cn_topic_0221482424_p12466782010"></a><a name="zh-cn_topic_0221482424_p12466782010"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482424_p2246178206"><a name="zh-cn_topic_0221482424_p2246178206"></a><a name="zh-cn_topic_0221482424_p2246178206"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482424_row124567132011"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482424_p15246976204"><a name="zh-cn_topic_0221482424_p15246976204"></a><a name="zh-cn_topic_0221482424_p15246976204"></a><a href="#zh-cn_topic_0221482424_request_Rq4100AuthIdentity">identity</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482424_p1224613732011"><a name="zh-cn_topic_0221482424_p1224613732011"></a><a name="zh-cn_topic_0221482424_p1224613732011"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482424_p72461674202"><a name="zh-cn_topic_0221482424_p72461674202"></a><a name="zh-cn_topic_0221482424_p72461674202"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482424_p82474792016"><a name="zh-cn_topic_0221482424_p82474792016"></a><a name="zh-cn_topic_0221482424_p82474792016"></a>认证参数。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  auth.identity

<a name="zh-cn_topic_0221482424_request_Rq4100AuthIdentity"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482424_row1624716720201"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482424_p42483762019"><a name="zh-cn_topic_0221482424_p42483762019"></a><a name="zh-cn_topic_0221482424_p42483762019"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482424_p19248177132014"><a name="zh-cn_topic_0221482424_p19248177132014"></a><a name="zh-cn_topic_0221482424_p19248177132014"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482424_p13248370208"><a name="zh-cn_topic_0221482424_p13248370208"></a><a name="zh-cn_topic_0221482424_p13248370208"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482424_p1024817712203"><a name="zh-cn_topic_0221482424_p1024817712203"></a><a name="zh-cn_topic_0221482424_p1024817712203"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482424_row132472722010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482424_p924812762015"><a name="zh-cn_topic_0221482424_p924812762015"></a><a name="zh-cn_topic_0221482424_p924812762015"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482424_p16248107142010"><a name="zh-cn_topic_0221482424_p16248107142010"></a><a name="zh-cn_topic_0221482424_p16248107142010"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482424_p132481779206"><a name="zh-cn_topic_0221482424_p132481779206"></a><a name="zh-cn_topic_0221482424_p132481779206"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482424_p82496772019"><a name="zh-cn_topic_0221482424_p82496772019"></a><a name="zh-cn_topic_0221482424_p82496772019"></a>认证方法，该字段内容为["token"]。</p>
<p id="zh-cn_topic_0221482424_p1424919742015"><a name="zh-cn_topic_0221482424_p1424919742015"></a><a name="zh-cn_topic_0221482424_p1424919742015"></a>取值范围：</p>
<a name="zh-cn_topic_0221482424_ul102498772018"></a><a name="zh-cn_topic_0221482424_ul102498772018"></a><ul id="zh-cn_topic_0221482424_ul102498772018"><li>token</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0221482424_row1247373205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482424_p324957132015"><a name="zh-cn_topic_0221482424_p324957132015"></a><a name="zh-cn_topic_0221482424_p324957132015"></a><a href="#zh-cn_topic_0221482424_request_Rq4100AuthIdentityToken">token</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482424_p225020716201"><a name="zh-cn_topic_0221482424_p225020716201"></a><a name="zh-cn_topic_0221482424_p225020716201"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482424_p1925087192012"><a name="zh-cn_topic_0221482424_p1925087192012"></a><a name="zh-cn_topic_0221482424_p1925087192012"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482424_p62503716201"><a name="zh-cn_topic_0221482424_p62503716201"></a><a name="zh-cn_topic_0221482424_p62503716201"></a>IAM用户token或联邦用户的token或委托token，该参数中的“id”与请求头中的X-Auth-Token填写其一即可，若都填写，优先校验X-Auth-Token。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  auth.identity.token

<a name="zh-cn_topic_0221482424_request_Rq4100AuthIdentityToken"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482424_row2025018715206"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482424_p725057162014"><a name="zh-cn_topic_0221482424_p725057162014"></a><a name="zh-cn_topic_0221482424_p725057162014"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482424_p1725137182016"><a name="zh-cn_topic_0221482424_p1725137182016"></a><a name="zh-cn_topic_0221482424_p1725137182016"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482424_p1225114713204"><a name="zh-cn_topic_0221482424_p1225114713204"></a><a name="zh-cn_topic_0221482424_p1225114713204"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482424_p172519720200"><a name="zh-cn_topic_0221482424_p172519720200"></a><a name="zh-cn_topic_0221482424_p172519720200"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482424_row18250378205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482424_p825117720202"><a name="zh-cn_topic_0221482424_p825117720202"></a><a name="zh-cn_topic_0221482424_p825117720202"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482424_p3251117142016"><a name="zh-cn_topic_0221482424_p3251117142016"></a><a name="zh-cn_topic_0221482424_p3251117142016"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482424_p16251177172013"><a name="zh-cn_topic_0221482424_p16251177172013"></a><a name="zh-cn_topic_0221482424_p16251177172013"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482424_p525247132015"><a name="zh-cn_topic_0221482424_p525247132015"></a><a name="zh-cn_topic_0221482424_p525247132015"></a>token的ID。与请求头中的X-Auth-Token填写其一即可，若都填写，优先校验X-Auth-Token。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482424_row3250207142014"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482424_p1225219712016"><a name="zh-cn_topic_0221482424_p1225219712016"></a><a name="zh-cn_topic_0221482424_p1225219712016"></a>duration-seconds</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482424_p9252127162014"><a name="zh-cn_topic_0221482424_p9252127162014"></a><a name="zh-cn_topic_0221482424_p9252127162014"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482424_p162521273205"><a name="zh-cn_topic_0221482424_p162521273205"></a><a name="zh-cn_topic_0221482424_p162521273205"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482424_p1125211792015"><a name="zh-cn_topic_0221482424_p1125211792015"></a><a name="zh-cn_topic_0221482424_p1125211792015"></a>AK/SK和securitytoken的有效期，时间单位为秒。取值范围：15min ~ 24h ，默认为15min。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482424_section12522718206"></a>

**表 6**  响应Body参数

<a name="zh-cn_topic_0221482424_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482424_row13253476207"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482424_p2253207102017"><a name="zh-cn_topic_0221482424_p2253207102017"></a><a name="zh-cn_topic_0221482424_p2253207102017"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482424_p825318772018"><a name="zh-cn_topic_0221482424_p825318772018"></a><a name="zh-cn_topic_0221482424_p825318772018"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482424_p425316742019"><a name="zh-cn_topic_0221482424_p425316742019"></a><a name="zh-cn_topic_0221482424_p425316742019"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482424_row32534782017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482424_p10254771203"><a name="zh-cn_topic_0221482424_p10254771203"></a><a name="zh-cn_topic_0221482424_p10254771203"></a><a href="#zh-cn_topic_0221482424_response_Rs41Credential">credential</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482424_p925417172016"><a name="zh-cn_topic_0221482424_p925417172016"></a><a name="zh-cn_topic_0221482424_p925417172016"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482424_p425413718204"><a name="zh-cn_topic_0221482424_p425413718204"></a><a name="zh-cn_topic_0221482424_p425413718204"></a>认证结果信息。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  credential

<a name="zh-cn_topic_0221482424_response_Rs41Credential"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482424_row17254177102010"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0221482424_p4255478206"><a name="zh-cn_topic_0221482424_p4255478206"></a><a name="zh-cn_topic_0221482424_p4255478206"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0221482424_p92550732018"><a name="zh-cn_topic_0221482424_p92550732018"></a><a name="zh-cn_topic_0221482424_p92550732018"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0221482424_p22553711201"><a name="zh-cn_topic_0221482424_p22553711201"></a><a name="zh-cn_topic_0221482424_p22553711201"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482424_row18254127132015"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482424_p4255572201"><a name="zh-cn_topic_0221482424_p4255572201"></a><a name="zh-cn_topic_0221482424_p4255572201"></a>expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482424_p1625511772016"><a name="zh-cn_topic_0221482424_p1625511772016"></a><a name="zh-cn_topic_0221482424_p1625511772016"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482424_p2255207132010"><a name="zh-cn_topic_0221482424_p2255207132010"></a><a name="zh-cn_topic_0221482424_p2255207132010"></a>AK/SK和securitytoken的过期时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482424_row22541971201"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482424_p1525513713206"><a name="zh-cn_topic_0221482424_p1525513713206"></a><a name="zh-cn_topic_0221482424_p1525513713206"></a>access</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482424_p72561719209"><a name="zh-cn_topic_0221482424_p72561719209"></a><a name="zh-cn_topic_0221482424_p72561719209"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482424_p1025617792013"><a name="zh-cn_topic_0221482424_p1025617792013"></a><a name="zh-cn_topic_0221482424_p1025617792013"></a>获取的AK。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482424_row1125419742017"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482424_p1425618742018"><a name="zh-cn_topic_0221482424_p1425618742018"></a><a name="zh-cn_topic_0221482424_p1425618742018"></a>secret</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482424_p1425637102017"><a name="zh-cn_topic_0221482424_p1425637102017"></a><a name="zh-cn_topic_0221482424_p1425637102017"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482424_p72561574207"><a name="zh-cn_topic_0221482424_p72561574207"></a><a name="zh-cn_topic_0221482424_p72561574207"></a>获取的SK。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482424_row132545716204"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0221482424_p202562718205"><a name="zh-cn_topic_0221482424_p202562718205"></a><a name="zh-cn_topic_0221482424_p202562718205"></a>securitytoken</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482424_p1425618716206"><a name="zh-cn_topic_0221482424_p1425618716206"></a><a name="zh-cn_topic_0221482424_p1425618716206"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482424_p425617714203"><a name="zh-cn_topic_0221482424_p425617714203"></a><a name="zh-cn_topic_0221482424_p425617714203"></a>securitytoken是将所获的AK、SK等信息进行加密后的字符串。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0221482424_section425610752013"></a>

-   不填写“token”参数。

    ```
    POST https://iam.myhuaweicloud.com/v3.0/OS-CREDENTIAL/securitytokens
    ```

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "token"
                ]
            }
        }
    }
    ```

-   填写"token"参数。

    ```
    POST https://iam.myhuaweicloud.com/v3.0/OS-CREDENTIAL/securitytokens
    ```

    ```
    {
        "auth": {
            "identity": {
                "methods": [
                    "token"
                ],
                "token": {
                    "id": "MIIamwYJKoZIhvcNAQcCoIIajDCC...",
                    "duration-seconds": 900
                }
            }
        }
    }
    ```


## 响应示例<a name="zh-cn_topic_0221482424_section1625915719207"></a>

**状态码为 201 时:**

创建成功。

```
{
    "credential": {
        "access": "NZFAT5VNWEJDGZ4PZ8CG",
        "expires_at": "2020-01-08T03:50:07.574000Z",
        "secret": "riEoWsy3qO0BvgwfkoLVgCUvzgpjBBcvdqM0hbk0",
        "securitytoken": "gQpjbi1ub3J0aC00jD4Ej..."
    }
}
```

## 返回值<a name="zh-cn_topic_0221482424_section13261576209"></a>

<a name="zh-cn_topic_0221482424_table2421"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482424_row22611373203"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482424_p72617742012"><a name="zh-cn_topic_0221482424_p72617742012"></a><a name="zh-cn_topic_0221482424_p72617742012"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482424_p14261679202"><a name="zh-cn_topic_0221482424_p14261679202"></a><a name="zh-cn_topic_0221482424_p14261679202"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482424_row52611779208"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482424_p152621971204"><a name="zh-cn_topic_0221482424_p152621971204"></a><a name="zh-cn_topic_0221482424_p152621971204"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482424_p1026215782012"><a name="zh-cn_topic_0221482424_p1026215782012"></a><a name="zh-cn_topic_0221482424_p1026215782012"></a>创建成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482424_row13261127112013"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482424_p32621073205"><a name="zh-cn_topic_0221482424_p32621073205"></a><a name="zh-cn_topic_0221482424_p32621073205"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482424_p5262879205"><a name="zh-cn_topic_0221482424_p5262879205"></a><a name="zh-cn_topic_0221482424_p5262879205"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482424_row192617712014"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482424_p1226297192014"><a name="zh-cn_topic_0221482424_p1226297192014"></a><a name="zh-cn_topic_0221482424_p1226297192014"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482424_p1626357142020"><a name="zh-cn_topic_0221482424_p1626357142020"></a><a name="zh-cn_topic_0221482424_p1626357142020"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482424_row926117122016"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482424_p32631978206"><a name="zh-cn_topic_0221482424_p32631978206"></a><a name="zh-cn_topic_0221482424_p32631978206"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482424_p16263157162018"><a name="zh-cn_topic_0221482424_p16263157162018"></a><a name="zh-cn_topic_0221482424_p16263157162018"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482424_row19261167142016"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482424_p32631678208"><a name="zh-cn_topic_0221482424_p32631678208"></a><a name="zh-cn_topic_0221482424_p32631678208"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482424_p1826311713206"><a name="zh-cn_topic_0221482424_p1826311713206"></a><a name="zh-cn_topic_0221482424_p1826311713206"></a>内部服务错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482424_section182631277204"></a>

无

