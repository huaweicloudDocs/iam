# 通过token获取临时访问密钥和securitytoken<a name="iam_04_0002"></a>

## 功能介绍<a name="zh-cn_topic_0221482424_section1524018722012"></a>

该接口可以用于通过token来获取临时AK/SK和securitytoken。临时AK/SK和securitytoken是系统颁发给IAM用户的临时访问令牌，有效期可在15分钟至24小时范围内设置，过期后需要重新获取。临时AK/SK和securitytoken遵循权限最小化原则。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

使用获取到的临时AK/SK和securitytoken作为凭证访问云服务，临时AK/SK和securitytoken两者必须**同时使用**，请求头中需要添加“x-security-token”字段，使用方法详情请参考：[使用临时AK/SK做签名](https://support.huaweicloud.com/devg-apisign/api-sign-securetoken.html)。

## 调试<a name="section155551711165315"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=CreateTemporaryAccessKeyByToken)中调试该接口。

## URI<a name="zh-cn_topic_0221482424_section524077132016"></a>

POST /v3.0/OS-CREDENTIAL/securitytokens

## 请求参数<a name="zh-cn_topic_0221482424_section1824112714203"></a>

**表 1**  请求Header参数

<a name="zh-cn_topic_0221482424_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482424_row824177142018"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482424_p13242671208"><a name="zh-cn_topic_0221482424_p13242671208"></a><a name="zh-cn_topic_0221482424_p13242671208"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.68%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482424_p1424227152018"><a name="zh-cn_topic_0221482424_p1424227152018"></a><a name="zh-cn_topic_0221482424_p1424227152018"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20.26%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482424_p1324237132014"><a name="zh-cn_topic_0221482424_p1324237132014"></a><a name="zh-cn_topic_0221482424_p1324237132014"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50.06%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482424_p10242107202011"><a name="zh-cn_topic_0221482424_p10242107202011"></a><a name="zh-cn_topic_0221482424_p10242107202011"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482424_row1924116717204"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482424_p12421711209"><a name="zh-cn_topic_0221482424_p12421711209"></a><a name="zh-cn_topic_0221482424_p12421711209"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="9.68%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482424_p32421072200"><a name="zh-cn_topic_0221482424_p32421072200"></a><a name="zh-cn_topic_0221482424_p32421072200"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.26%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482424_p72430719208"><a name="zh-cn_topic_0221482424_p72430719208"></a><a name="zh-cn_topic_0221482424_p72430719208"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.06%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482424_p132432722010"><a name="zh-cn_topic_0221482424_p132432722010"></a><a name="zh-cn_topic_0221482424_p132432722010"></a>该字段填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482424_row192419772018"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482424_p1124315712208"><a name="zh-cn_topic_0221482424_p1124315712208"></a><a name="zh-cn_topic_0221482424_p1124315712208"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="9.68%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482424_p1424397162011"><a name="zh-cn_topic_0221482424_p1424397162011"></a><a name="zh-cn_topic_0221482424_p1424397162011"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20.26%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482424_p152430710202"><a name="zh-cn_topic_0221482424_p152430710202"></a><a name="zh-cn_topic_0221482424_p152430710202"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.06%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482424_p824310714204"><a name="zh-cn_topic_0221482424_p824310714204"></a><a name="zh-cn_topic_0221482424_p824310714204"></a>IAM用户token或联邦用户的token或委托token。</p>
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
</td>
</tr>
<tr id="zh-cn_topic_0221482424_row1247373205"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482424_p324957132015"><a name="zh-cn_topic_0221482424_p324957132015"></a><a name="zh-cn_topic_0221482424_p324957132015"></a><a href="#zh-cn_topic_0221482424_request_Rq4100AuthIdentityToken">token</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482424_p225020716201"><a name="zh-cn_topic_0221482424_p225020716201"></a><a name="zh-cn_topic_0221482424_p225020716201"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482424_p1925087192012"><a name="zh-cn_topic_0221482424_p1925087192012"></a><a name="zh-cn_topic_0221482424_p1925087192012"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482424_p62503716201"><a name="zh-cn_topic_0221482424_p62503716201"></a><a name="zh-cn_topic_0221482424_p62503716201"></a>临时访问密钥和securitytoken的有效期。</p>
</td>
</tr>
<tr id="row18244323173415"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p12452231340"><a name="p12452231340"></a><a name="p12452231340"></a><a href="#zh-cn_topic_0222037452_request_Rq113RolePolicy">policy</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p202451223123419"><a name="p202451223123419"></a><a name="p202451223123419"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p824513234340"><a name="p824513234340"></a><a name="p824513234340"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1520617581232"><a name="p1520617581232"></a><a name="p1520617581232"></a>用户自定义策略的信息，用于限制获取到的临时访问密钥和securitytoken的权限（当前仅适用限制OBS服务的权限）。</p>
<p id="p14933929171915"><a name="p14933929171915"></a><a name="p14933929171915"></a>如果填写此参数，则临时访问密钥和securitytoken的权限为：原token具有的权限和policy参数限制的权限交集。</p>
<p id="p20354724261"><a name="p20354724261"></a><a name="p20354724261"></a>关于IAM策略的格式和语法，请参考：<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0017.html" target="_blank" rel="noopener noreferrer">策略</a>。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  auth.identity.policy

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
<div class="note" id="zh-cn_topic_0222037452_note124277504318"><a name="zh-cn_topic_0222037452_note124277504318"></a><a name="zh-cn_topic_0222037452_note124277504318"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p55422339324"><a name="p55422339324"></a><a name="p55422339324"></a>1.1：策略。IAM最新提供的一种细粒度授权的能力，可以精确到具体服务的操作、资源以及请求条件等。</p>
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

**表 6**  auth.identity.policy.Statement

<a name="zh-cn_topic_0222037452_request_Rq113RolePolicyStatementArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0222037452_row194281150539"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0222037452_p142865019318"><a name="zh-cn_topic_0222037452_p142865019318"></a><a name="zh-cn_topic_0222037452_p142865019318"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0222037452_p6428175016317"><a name="zh-cn_topic_0222037452_p6428175016317"></a><a name="zh-cn_topic_0222037452_p6428175016317"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.97%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0222037452_p5429750336"><a name="zh-cn_topic_0222037452_p5429750336"></a><a name="zh-cn_topic_0222037452_p5429750336"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50.029999999999994%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0222037452_p1342945017311"><a name="zh-cn_topic_0222037452_p1342945017311"></a><a name="zh-cn_topic_0222037452_p1342945017311"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0222037452_row24281450534"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0222037452_p5429165016320"><a name="zh-cn_topic_0222037452_p5429165016320"></a><a name="zh-cn_topic_0222037452_p5429165016320"></a>Action</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0222037452_p5429165016314"><a name="zh-cn_topic_0222037452_p5429165016314"></a><a name="zh-cn_topic_0222037452_p5429165016314"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0222037452_p1543016509316"><a name="zh-cn_topic_0222037452_p1543016509316"></a><a name="zh-cn_topic_0222037452_p1543016509316"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50.029999999999994%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0222037452_p9430175011313"><a name="zh-cn_topic_0222037452_p9430175011313"></a><a name="zh-cn_topic_0222037452_p9430175011313"></a>授权项，指对资源的具体操作权限，不超过100个。</p>
<div class="note" id="zh-cn_topic_0222037452_note1743113501237"><a name="zh-cn_topic_0222037452_note1743113501237"></a><a name="zh-cn_topic_0222037452_note1743113501237"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0222037452_ul1743145019314"></a><a name="zh-cn_topic_0222037452_ul1743145019314"></a><ul id="zh-cn_topic_0222037452_ul1743145019314"><li>格式为：服务名:资源类型:操作，例：vpc:ports:create。</li><li>服务名为产品名称，例如ecs、evs和vpc等，服务名仅支持小写。 资源类型和操作没有大小写，要求支持通配符号*，无需罗列全部授权项。</li></ul>
</div></div>
</td>
</tr>
<tr id="zh-cn_topic_0222037452_row18428185014319"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0222037452_p184316501337"><a name="zh-cn_topic_0222037452_p184316501337"></a><a name="zh-cn_topic_0222037452_p184316501337"></a>Effect</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0222037452_p24311150832"><a name="zh-cn_topic_0222037452_p24311150832"></a><a name="zh-cn_topic_0222037452_p24311150832"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0222037452_p1443111501317"><a name="zh-cn_topic_0222037452_p1443111501317"></a><a name="zh-cn_topic_0222037452_p1443111501317"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.029999999999994%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0222037452_p54316501734"><a name="zh-cn_topic_0222037452_p54316501734"></a><a name="zh-cn_topic_0222037452_p54316501734"></a>作用。包含两种：允许（Allow）和拒绝（Deny），既有Allow又有Deny的授权语句时，遵循Deny优先的原则。</p>
<p id="zh-cn_topic_0222037452_p7431145016317"><a name="zh-cn_topic_0222037452_p7431145016317"></a><a name="zh-cn_topic_0222037452_p7431145016317"></a>取值范围：</p>
<a name="zh-cn_topic_0222037452_ul1843113505315"></a><a name="zh-cn_topic_0222037452_ul1843113505315"></a><ul id="zh-cn_topic_0222037452_ul1843113505315"><li>Allow</li><li>Deny</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0222037452_row174281850633"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0222037452_p943218502313"><a name="zh-cn_topic_0222037452_p943218502313"></a><a name="zh-cn_topic_0222037452_p943218502313"></a>Condition</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0222037452_p1943220501933"><a name="zh-cn_topic_0222037452_p1943220501933"></a><a name="zh-cn_topic_0222037452_p1943220501933"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0222037452_p174321501311"><a name="zh-cn_topic_0222037452_p174321501311"></a><a name="zh-cn_topic_0222037452_p174321501311"></a>Map&lt;String,Map&lt;String,Array&lt;String&gt;&gt;&gt;</p>
</td>
<td class="cellrowborder" valign="top" width="50.029999999999994%" headers="mcps1.2.5.1.4 "><p id="p139313435469"><a name="p139313435469"></a><a name="p139313435469"></a>限制条件。不超过10个。了解更多相关参数，请参考：<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0605.html#section1" target="_blank" rel="noopener noreferrer">配置自定义策略</a>。</p>
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
<td class="cellrowborder" valign="top" width="19.97%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0222037452_p8433195017317"><a name="zh-cn_topic_0222037452_p8433195017317"></a><a name="zh-cn_topic_0222037452_p8433195017317"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50.029999999999994%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0222037452_p343318501535"><a name="zh-cn_topic_0222037452_p343318501535"></a><a name="zh-cn_topic_0222037452_p343318501535"></a>资源。数组长度不超过10，每个字符串长度不超过128，规则如下：</p>
<div class="note" id="zh-cn_topic_0222037452_note04331650133"><a name="zh-cn_topic_0222037452_note04331650133"></a><a name="zh-cn_topic_0222037452_note04331650133"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="zh-cn_topic_0222037452_ul2433185011318"></a><a name="zh-cn_topic_0222037452_ul2433185011318"></a><ul id="zh-cn_topic_0222037452_ul2433185011318"><li>格式为“服务名:region:domainId:资源类型:资源路径”, 资源类型支持通配符号*，通配符号*表示所有。如"obs:*:*:bucket:*": 表示所有的OBS桶。</li><li>region字段为*或用户可访问的region。service必须存在且resource属于对应service。</li></ul>
</div></div>
</td>
</tr>
</tbody>
</table>

**表 7**  auth.identity.token

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
<tbody><tr id="zh-cn_topic_0221482424_row3250207142014"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482424_p1225219712016"><a name="zh-cn_topic_0221482424_p1225219712016"></a><a name="zh-cn_topic_0221482424_p1225219712016"></a>duration_seconds</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482424_p9252127162014"><a name="zh-cn_topic_0221482424_p9252127162014"></a><a name="zh-cn_topic_0221482424_p9252127162014"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482424_p162521273205"><a name="zh-cn_topic_0221482424_p162521273205"></a><a name="zh-cn_topic_0221482424_p162521273205"></a>Integer</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p92151436103218"><a name="p92151436103218"></a><a name="p92151436103218"></a>临时访问密钥和securitytoken的有效期，时间单位为秒。</p>
<p id="zh-cn_topic_0221482424_p1125211792015"><a name="zh-cn_topic_0221482424_p1125211792015"></a><a name="zh-cn_topic_0221482424_p1125211792015"></a>取值范围：15分钟 ~ 24小时 ，默认为15分钟。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482424_section12522718206"></a>

**表 8**  响应Body参数

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

**表 9**  credential

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
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0221482378_p91813714205"><a name="zh-cn_topic_0221482378_p91813714205"></a><a name="zh-cn_topic_0221482378_p91813714205"></a>AK/SK和securitytoken的过期时间。响应参数为UTC时间格式，北京时间为UTC+8小时。</p>
<p id="p765214113919"><a name="p765214113919"></a><a name="p765214113919"></a>如返回：</p>
<pre class="screen" id="screen1965014116391"><a name="screen1965014116391"></a><a name="screen1965014116391"></a>"expires_at": "2020-01-08T02:56:19.587000Z"</pre>
<p id="p17393151111394"><a name="p17393151111394"></a><a name="p17393151111394"></a>北京时间：2020-01-08 10:56:19.587</p>
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
                    "duration_seconds": 900
                }
            }
        }
    }
    ```

-   不填写“token”参数（请求头中需要X-Auth-Token）。

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

-   填写“policy”参数。

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
          "policy": {
            "Version": "1.1",
            "Statement": [
              {
                "Effect": "Allow",
                "Action": [
                  "obs:object:*"
                ],
                "Resource": [
                  "obs:*:*:object:*"
                ],
                "Condition": {
                  "StringEquals": {
                    "obs:prefix": [
                      "public"
                    ]
                  }
                }
              }
            ]
          },
          "token": {
            "duration_seconds": 900
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
        "access": "NZFAT5VNWEJDGZ4PZ...",
        "expires_at": "2020-01-08T03:50:07.574000Z",
        "secret": "riEoWsy3qO0BvgwfkoLVgCUvzgpjBBcvdq...",
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

