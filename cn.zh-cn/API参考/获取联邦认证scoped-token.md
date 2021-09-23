# 获取联邦认证scoped token<a name="iam_13_0604"></a>

## 功能介绍<a name="zh-cn_topic_0224276934_section6449144595112"></a>

该接口可以用于通过联邦认证方式获取scoped token。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section8881038191618"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneCreateScopedToken)中调试该接口。

## URI<a name="zh-cn_topic_0224276934_section8449145135118"></a>

POST /v3/auth/tokens

## 请求参数<a name="zh-cn_topic_0224276934_section15450114520513"></a>

**表 1**  请求Header参数

<a name="zh-cn_topic_0224276934_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row4450194565118"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276934_p5451144517519"><a name="zh-cn_topic_0224276934_p5451144517519"></a><a name="zh-cn_topic_0224276934_p5451144517519"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="9.66%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276934_p11451445175115"><a name="zh-cn_topic_0224276934_p11451445175115"></a><a name="zh-cn_topic_0224276934_p11451445175115"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20.34%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276934_p24520450518"><a name="zh-cn_topic_0224276934_p24520450518"></a><a name="zh-cn_topic_0224276934_p24520450518"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276934_p1045254555118"><a name="zh-cn_topic_0224276934_p1045254555118"></a><a name="zh-cn_topic_0224276934_p1045254555118"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row5450245185113"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p245224515110"><a name="zh-cn_topic_0224276934_p245224515110"></a><a name="zh-cn_topic_0224276934_p245224515110"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="9.66%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p645214511518"><a name="zh-cn_topic_0224276934_p645214511518"></a><a name="zh-cn_topic_0224276934_p645214511518"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20.34%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p4452104555112"><a name="zh-cn_topic_0224276934_p4452104555112"></a><a name="zh-cn_topic_0224276934_p4452104555112"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p1345384595118"><a name="zh-cn_topic_0224276934_p1345384595118"></a><a name="zh-cn_topic_0224276934_p1345384595118"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  请求Body参数

<a name="zh-cn_topic_0224276934_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row6453154512517"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276934_p1345424585111"><a name="zh-cn_topic_0224276934_p1345424585111"></a><a name="zh-cn_topic_0224276934_p1345424585111"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276934_p14454745175112"><a name="zh-cn_topic_0224276934_p14454745175112"></a><a name="zh-cn_topic_0224276934_p14454745175112"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276934_p1345434518516"><a name="zh-cn_topic_0224276934_p1345434518516"></a><a name="zh-cn_topic_0224276934_p1345434518516"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276934_p7454945135115"><a name="zh-cn_topic_0224276934_p7454945135115"></a><a name="zh-cn_topic_0224276934_p7454945135115"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row18453184512514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p245574516513"><a name="zh-cn_topic_0224276934_p245574516513"></a><a name="zh-cn_topic_0224276934_p245574516513"></a><a href="#zh-cn_topic_0224276934_request_Rq1363Auth">auth</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p04551452517"><a name="zh-cn_topic_0224276934_p04551452517"></a><a name="zh-cn_topic_0224276934_p04551452517"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p1945574545115"><a name="zh-cn_topic_0224276934_p1945574545115"></a><a name="zh-cn_topic_0224276934_p1945574545115"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p745524515510"><a name="zh-cn_topic_0224276934_p745524515510"></a><a name="zh-cn_topic_0224276934_p745524515510"></a>认证信息。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  auth

<a name="zh-cn_topic_0224276934_request_Rq1363Auth"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row18456145155117"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276934_p745784510515"><a name="zh-cn_topic_0224276934_p745784510515"></a><a name="zh-cn_topic_0224276934_p745784510515"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276934_p545794555119"><a name="zh-cn_topic_0224276934_p545794555119"></a><a name="zh-cn_topic_0224276934_p545794555119"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276934_p1245714519512"><a name="zh-cn_topic_0224276934_p1245714519512"></a><a name="zh-cn_topic_0224276934_p1245714519512"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276934_p645712456515"><a name="zh-cn_topic_0224276934_p645712456515"></a><a name="zh-cn_topic_0224276934_p645712456515"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row144560453515"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p194588456516"><a name="zh-cn_topic_0224276934_p194588456516"></a><a name="zh-cn_topic_0224276934_p194588456516"></a><a href="#zh-cn_topic_0224276934_request_Rq1363AuthIdentity">identity</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p145864518516"><a name="zh-cn_topic_0224276934_p145864518516"></a><a name="zh-cn_topic_0224276934_p145864518516"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p84584458512"><a name="zh-cn_topic_0224276934_p84584458512"></a><a name="zh-cn_topic_0224276934_p84584458512"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p5458134513518"><a name="zh-cn_topic_0224276934_p5458134513518"></a><a name="zh-cn_topic_0224276934_p5458134513518"></a>认证参数。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row12456194505114"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p7458845115111"><a name="zh-cn_topic_0224276934_p7458845115111"></a><a name="zh-cn_topic_0224276934_p7458845115111"></a><a href="#zh-cn_topic_0224276934_request_Rq1363AuthScope">scope</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p9459104513513"><a name="zh-cn_topic_0224276934_p9459104513513"></a><a name="zh-cn_topic_0224276934_p9459104513513"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p145984595118"><a name="zh-cn_topic_0224276934_p145984595118"></a><a name="zh-cn_topic_0224276934_p145984595118"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p64591345135114"><a name="zh-cn_topic_0224276934_p64591345135114"></a><a name="zh-cn_topic_0224276934_p64591345135114"></a>token的使用范围，取值为project或domain，二选一即可。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  auth.identity

<a name="zh-cn_topic_0224276934_request_Rq1363AuthIdentity"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row0460114555116"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276934_p9460345135111"><a name="zh-cn_topic_0224276934_p9460345135111"></a><a name="zh-cn_topic_0224276934_p9460345135111"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276934_p20460194510516"><a name="zh-cn_topic_0224276934_p20460194510516"></a><a name="zh-cn_topic_0224276934_p20460194510516"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276934_p15461194525117"><a name="zh-cn_topic_0224276934_p15461194525117"></a><a name="zh-cn_topic_0224276934_p15461194525117"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276934_p1346164545116"><a name="zh-cn_topic_0224276934_p1346164545116"></a><a name="zh-cn_topic_0224276934_p1346164545116"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row1246054512518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p19461184545110"><a name="zh-cn_topic_0224276934_p19461184545110"></a><a name="zh-cn_topic_0224276934_p19461184545110"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p1846164555112"><a name="zh-cn_topic_0224276934_p1846164555112"></a><a name="zh-cn_topic_0224276934_p1846164555112"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p17462144505119"><a name="zh-cn_topic_0224276934_p17462144505119"></a><a name="zh-cn_topic_0224276934_p17462144505119"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p4462194518515"><a name="zh-cn_topic_0224276934_p4462194518515"></a><a name="zh-cn_topic_0224276934_p4462194518515"></a>认证方法，该字段内容为“token”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row1046012454511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p64621145115119"><a name="zh-cn_topic_0224276934_p64621145115119"></a><a name="zh-cn_topic_0224276934_p64621145115119"></a><a href="#zh-cn_topic_0224276934_request_Rq1363AuthIdentityToken">token</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p0462194515516"><a name="zh-cn_topic_0224276934_p0462194515516"></a><a name="zh-cn_topic_0224276934_p0462194515516"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p94627459513"><a name="zh-cn_topic_0224276934_p94627459513"></a><a name="zh-cn_topic_0224276934_p94627459513"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p14629458516"><a name="zh-cn_topic_0224276934_p14629458516"></a><a name="zh-cn_topic_0224276934_p14629458516"></a>联邦unscoped token的信息。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  auth.identity.token

<a name="zh-cn_topic_0224276934_request_Rq1363AuthIdentityToken"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row144631245115115"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276934_p114631145135111"><a name="zh-cn_topic_0224276934_p114631145135111"></a><a name="zh-cn_topic_0224276934_p114631145135111"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276934_p11464545175111"><a name="zh-cn_topic_0224276934_p11464545175111"></a><a name="zh-cn_topic_0224276934_p11464545175111"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276934_p1546410454518"><a name="zh-cn_topic_0224276934_p1546410454518"></a><a name="zh-cn_topic_0224276934_p1546410454518"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276934_p17464124505110"><a name="zh-cn_topic_0224276934_p17464124505110"></a><a name="zh-cn_topic_0224276934_p17464124505110"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row246316454518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p134648457515"><a name="zh-cn_topic_0224276934_p134648457515"></a><a name="zh-cn_topic_0224276934_p134648457515"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p24641454517"><a name="zh-cn_topic_0224276934_p24641454517"></a><a name="zh-cn_topic_0224276934_p24641454517"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p10465124518518"><a name="zh-cn_topic_0224276934_p10465124518518"></a><a name="zh-cn_topic_0224276934_p10465124518518"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p24654456517"><a name="zh-cn_topic_0224276934_p24654456517"></a><a name="zh-cn_topic_0224276934_p24654456517"></a>联邦unscoped token的ID。</p>
</td>
</tr>
</tbody>
</table>

**表 6**  auth.scope

<a name="zh-cn_topic_0224276934_request_Rq1363AuthScope"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row1646514458513"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276934_p10466194555115"><a name="zh-cn_topic_0224276934_p10466194555115"></a><a name="zh-cn_topic_0224276934_p10466194555115"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276934_p18466845165112"><a name="zh-cn_topic_0224276934_p18466845165112"></a><a name="zh-cn_topic_0224276934_p18466845165112"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276934_p9467145205112"><a name="zh-cn_topic_0224276934_p9467145205112"></a><a name="zh-cn_topic_0224276934_p9467145205112"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276934_p14467174575115"><a name="zh-cn_topic_0224276934_p14467174575115"></a><a name="zh-cn_topic_0224276934_p14467174575115"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row74661345165112"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p2467245195116"><a name="zh-cn_topic_0224276934_p2467245195116"></a><a name="zh-cn_topic_0224276934_p2467245195116"></a><a href="#zh-cn_topic_0224276934_request_Rq1363AuthScopeDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p19467645195114"><a name="zh-cn_topic_0224276934_p19467645195114"></a><a name="zh-cn_topic_0224276934_p19467645195114"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p1946784519512"><a name="zh-cn_topic_0224276934_p1946784519512"></a><a name="zh-cn_topic_0224276934_p1946784519512"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p8468124517517"><a name="zh-cn_topic_0224276934_p8468124517517"></a><a name="zh-cn_topic_0224276934_p8468124517517"></a>取值为domain时，表示获取的token可以跨区域使用，domain支持id和name，二选一即可。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row0466174513516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p184681545195114"><a name="zh-cn_topic_0224276934_p184681545195114"></a><a name="zh-cn_topic_0224276934_p184681545195114"></a><a href="#zh-cn_topic_0224276934_request_Rq1363AuthScopeProject">project</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p1746864545114"><a name="zh-cn_topic_0224276934_p1746864545114"></a><a name="zh-cn_topic_0224276934_p1746864545114"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p1446820450512"><a name="zh-cn_topic_0224276934_p1446820450512"></a><a name="zh-cn_topic_0224276934_p1446820450512"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p154681045105111"><a name="zh-cn_topic_0224276934_p154681045105111"></a><a name="zh-cn_topic_0224276934_p154681045105111"></a>取值为project时，表示获取的token仅能访问指定project下的资源，project支持id和name，二选一即可。</p>
</td>
</tr>
</tbody>
</table>

**表 7**  auth.scope.domain

<a name="zh-cn_topic_0224276934_request_Rq1363AuthScopeDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row11469144519512"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276934_p1747010459513"><a name="zh-cn_topic_0224276934_p1747010459513"></a><a name="zh-cn_topic_0224276934_p1747010459513"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276934_p64705451514"><a name="zh-cn_topic_0224276934_p64705451514"></a><a name="zh-cn_topic_0224276934_p64705451514"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276934_p1047010458510"><a name="zh-cn_topic_0224276934_p1047010458510"></a><a name="zh-cn_topic_0224276934_p1047010458510"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276934_p2470124511518"><a name="zh-cn_topic_0224276934_p2470124511518"></a><a name="zh-cn_topic_0224276934_p2470124511518"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row1546994535110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p847019455513"><a name="zh-cn_topic_0224276934_p847019455513"></a><a name="zh-cn_topic_0224276934_p847019455513"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p64715458516"><a name="zh-cn_topic_0224276934_p64715458516"></a><a name="zh-cn_topic_0224276934_p64715458516"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p1247110457517"><a name="zh-cn_topic_0224276934_p1247110457517"></a><a name="zh-cn_topic_0224276934_p1247110457517"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p1447120457517"><a name="zh-cn_topic_0224276934_p1447120457517"></a><a name="zh-cn_topic_0224276934_p1447120457517"></a>帐号ID，id与name二选一即可。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row84692045105113"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p3471194545111"><a name="zh-cn_topic_0224276934_p3471194545111"></a><a name="zh-cn_topic_0224276934_p3471194545111"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p9471745135113"><a name="zh-cn_topic_0224276934_p9471745135113"></a><a name="zh-cn_topic_0224276934_p9471745135113"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p247294565120"><a name="zh-cn_topic_0224276934_p247294565120"></a><a name="zh-cn_topic_0224276934_p247294565120"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p114724450517"><a name="zh-cn_topic_0224276934_p114724450517"></a><a name="zh-cn_topic_0224276934_p114724450517"></a>帐号名，id与name二选一即可。</p>
</td>
</tr>
</tbody>
</table>

**表 8**  auth.scope.project

<a name="zh-cn_topic_0224276934_request_Rq1363AuthScopeProject"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row12473174595117"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276934_p124745456515"><a name="zh-cn_topic_0224276934_p124745456515"></a><a name="zh-cn_topic_0224276934_p124745456515"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276934_p1447484513516"><a name="zh-cn_topic_0224276934_p1447484513516"></a><a name="zh-cn_topic_0224276934_p1447484513516"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276934_p94741545155119"><a name="zh-cn_topic_0224276934_p94741545155119"></a><a name="zh-cn_topic_0224276934_p94741545155119"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276934_p17474134516515"><a name="zh-cn_topic_0224276934_p17474134516515"></a><a name="zh-cn_topic_0224276934_p17474134516515"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row5690125213228"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p8761143117242"><a name="p8761143117242"></a><a name="p8761143117242"></a><a href="#table11966185019243">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p376153172419"><a name="p376153172419"></a><a name="p376153172419"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p177611331182414"><a name="p177611331182414"></a><a name="p177611331182414"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p076173112417"><a name="p076173112417"></a><a name="p076173112417"></a>项目所属帐号，使用name时必填。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row447394516516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p11475545175116"><a name="zh-cn_topic_0224276934_p11475545175116"></a><a name="zh-cn_topic_0224276934_p11475545175116"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p20475134511519"><a name="zh-cn_topic_0224276934_p20475134511519"></a><a name="zh-cn_topic_0224276934_p20475134511519"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p7475184510517"><a name="zh-cn_topic_0224276934_p7475184510517"></a><a name="zh-cn_topic_0224276934_p7475184510517"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p447564535117"><a name="zh-cn_topic_0224276934_p447564535117"></a><a name="zh-cn_topic_0224276934_p447564535117"></a>项目ID，id与name二选一即可。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row15473104545116"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276934_p18476845125113"><a name="zh-cn_topic_0224276934_p18476845125113"></a><a name="zh-cn_topic_0224276934_p18476845125113"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276934_p16476124595119"><a name="zh-cn_topic_0224276934_p16476124595119"></a><a name="zh-cn_topic_0224276934_p16476124595119"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276934_p20476164525118"><a name="zh-cn_topic_0224276934_p20476164525118"></a><a name="zh-cn_topic_0224276934_p20476164525118"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276934_p9476204545120"><a name="zh-cn_topic_0224276934_p9476204545120"></a><a name="zh-cn_topic_0224276934_p9476204545120"></a>项目名，id与name二选一即可。</p>
</td>
</tr>
</tbody>
</table>

**表 9**  auth.scope.project.domain

<a name="table11966185019243"></a>
<table><thead align="left"><tr id="row1996695032410"><th class="cellrowborder" valign="top" width="19.89%" id="mcps1.2.5.1.1"><p id="p110174410253"><a name="p110174410253"></a><a name="p110174410253"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.5%" id="mcps1.2.5.1.2"><p id="p605444250"><a name="p605444250"></a><a name="p605444250"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.89%" id="mcps1.2.5.1.3"><p id="p1601544112514"><a name="p1601544112514"></a><a name="p1601544112514"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="49.72%" id="mcps1.2.5.1.4"><p id="p2013449256"><a name="p2013449256"></a><a name="p2013449256"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1996614501246"><td class="cellrowborder" valign="top" width="19.89%" headers="mcps1.2.5.1.1 "><p id="p1250223914259"><a name="p1250223914259"></a><a name="p1250223914259"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="10.5%" headers="mcps1.2.5.1.2 "><p id="p35021939102510"><a name="p35021939102510"></a><a name="p35021939102510"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.89%" headers="mcps1.2.5.1.3 "><p id="p6502153920250"><a name="p6502153920250"></a><a name="p6502153920250"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="49.72%" headers="mcps1.2.5.1.4 "><p id="p15021339152520"><a name="p15021339152520"></a><a name="p15021339152520"></a>帐号ID，id与name二选一即可。</p>
</td>
</tr>
<tr id="row3967155019249"><td class="cellrowborder" valign="top" width="19.89%" headers="mcps1.2.5.1.1 "><p id="p950213912520"><a name="p950213912520"></a><a name="p950213912520"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="10.5%" headers="mcps1.2.5.1.2 "><p id="p1235511127264"><a name="p1235511127264"></a><a name="p1235511127264"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="19.89%" headers="mcps1.2.5.1.3 "><p id="p1850223915254"><a name="p1850223915254"></a><a name="p1850223915254"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="49.72%" headers="mcps1.2.5.1.4 "><p id="p185024397257"><a name="p185024397257"></a><a name="p185024397257"></a>帐号名，id与name二选一即可。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0224276934_section20480545145114"></a>

**表 10**  响应Header参数

<a name="zh-cn_topic_0224276934_ResponseHeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row1548118457515"><th class="cellrowborder" valign="top" width="30%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p8481164515117"><a name="zh-cn_topic_0224276934_p8481164515117"></a><a name="zh-cn_topic_0224276934_p8481164515117"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p124817454511"><a name="zh-cn_topic_0224276934_p124817454511"></a><a name="zh-cn_topic_0224276934_p124817454511"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p14482194515516"><a name="zh-cn_topic_0224276934_p14482194515516"></a><a name="zh-cn_topic_0224276934_p14482194515516"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row12481194519515"><td class="cellrowborder" valign="top" width="30%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p448294565111"><a name="zh-cn_topic_0224276934_p448294565111"></a><a name="zh-cn_topic_0224276934_p448294565111"></a>X-Subject-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p948214514515"><a name="zh-cn_topic_0224276934_p948214514515"></a><a name="zh-cn_topic_0224276934_p948214514515"></a>string</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p84820457512"><a name="zh-cn_topic_0224276934_p84820457512"></a><a name="zh-cn_topic_0224276934_p84820457512"></a>签名后的scoped token。</p>
</td>
</tr>
</tbody>
</table>

**表 11**  响应Body参数

<a name="zh-cn_topic_0224276934_responseParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row148318453517"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p148354517513"><a name="zh-cn_topic_0224276934_p148354517513"></a><a name="zh-cn_topic_0224276934_p148354517513"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p94831453516"><a name="zh-cn_topic_0224276934_p94831453516"></a><a name="zh-cn_topic_0224276934_p94831453516"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p448314535119"><a name="zh-cn_topic_0224276934_p448314535119"></a><a name="zh-cn_topic_0224276934_p448314535119"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row1848304519519"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p1648424515119"><a name="zh-cn_topic_0224276934_p1648424515119"></a><a name="zh-cn_topic_0224276934_p1648424515119"></a><a href="#zh-cn_topic_0224276934_response_Rs1363Token">token</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p8484174517515"><a name="zh-cn_topic_0224276934_p8484174517515"></a><a name="zh-cn_topic_0224276934_p8484174517515"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p8484154535111"><a name="zh-cn_topic_0224276934_p8484154535111"></a><a name="zh-cn_topic_0224276934_p8484154535111"></a>联邦认证的scoped token信息。</p>
</td>
</tr>
</tbody>
</table>

**表 12**  token

<a name="zh-cn_topic_0224276934_response_Rs1363Token"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row10485194513510"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p548594535116"><a name="zh-cn_topic_0224276934_p548594535116"></a><a name="zh-cn_topic_0224276934_p548594535116"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p10486184505120"><a name="zh-cn_topic_0224276934_p10486184505120"></a><a name="zh-cn_topic_0224276934_p10486184505120"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p15486194515110"><a name="zh-cn_topic_0224276934_p15486194515110"></a><a name="zh-cn_topic_0224276934_p15486194515110"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row348574514512"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p6486194515519"><a name="zh-cn_topic_0224276934_p6486194515519"></a><a name="zh-cn_topic_0224276934_p6486194515519"></a>methods</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p1448684535117"><a name="zh-cn_topic_0224276934_p1448684535117"></a><a name="zh-cn_topic_0224276934_p1448684535117"></a>Array of strings</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p134864458515"><a name="zh-cn_topic_0224276934_p134864458515"></a><a name="zh-cn_topic_0224276934_p134864458515"></a>获取token的方式。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row248512455513"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p15487945165116"><a name="zh-cn_topic_0224276934_p15487945165116"></a><a name="zh-cn_topic_0224276934_p15487945165116"></a>expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p84871545155115"><a name="zh-cn_topic_0224276934_p84871545155115"></a><a name="zh-cn_topic_0224276934_p84871545155115"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p548718451519"><a name="zh-cn_topic_0224276934_p548718451519"></a><a name="zh-cn_topic_0224276934_p548718451519"></a>token过期时间。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row19485164595115"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p1487345145116"><a name="zh-cn_topic_0224276934_p1487345145116"></a><a name="zh-cn_topic_0224276934_p1487345145116"></a><a href="#zh-cn_topic_0224276934_response_Rs1363TokenCatalogArritem">catalog</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p1487124585113"><a name="zh-cn_topic_0224276934_p1487124585113"></a><a name="zh-cn_topic_0224276934_p1487124585113"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p1948734517515"><a name="zh-cn_topic_0224276934_p1948734517515"></a><a name="zh-cn_topic_0224276934_p1948734517515"></a>服务目录信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row1448518457513"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p1488124545110"><a name="zh-cn_topic_0224276934_p1488124545110"></a><a name="zh-cn_topic_0224276934_p1488124545110"></a><a href="#zh-cn_topic_0224276934_response_Rs1363TokenDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p74884455517"><a name="zh-cn_topic_0224276934_p74884455517"></a><a name="zh-cn_topic_0224276934_p74884455517"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p134881245185119"><a name="zh-cn_topic_0224276934_p134881245185119"></a><a name="zh-cn_topic_0224276934_p134881245185119"></a>获取token的用户所属的帐号信息。如果获取token时请求体中scope参数设置为domain，则返回该字段。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row15485144575110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p2048814452513"><a name="zh-cn_topic_0224276934_p2048814452513"></a><a name="zh-cn_topic_0224276934_p2048814452513"></a><a href="#zh-cn_topic_0224276934_response_Rs1363TokenProject">project</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p94881459510"><a name="zh-cn_topic_0224276934_p94881459510"></a><a name="zh-cn_topic_0224276934_p94881459510"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p1488164510517"><a name="zh-cn_topic_0224276934_p1488164510517"></a><a name="zh-cn_topic_0224276934_p1488164510517"></a>获取token的用户所属帐号的项目信息。如果获取token时请求体中scope参数设置为project，则返回该字段。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row948504515517"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p13489194545114"><a name="zh-cn_topic_0224276934_p13489194545114"></a><a name="zh-cn_topic_0224276934_p13489194545114"></a><a href="#zh-cn_topic_0224276934_response_Rs1363TokenRolesArritem">roles</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p24891645155114"><a name="zh-cn_topic_0224276934_p24891645155114"></a><a name="zh-cn_topic_0224276934_p24891645155114"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p7489154514514"><a name="zh-cn_topic_0224276934_p7489154514514"></a><a name="zh-cn_topic_0224276934_p7489154514514"></a>token的权限信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row1648594516511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p248954511513"><a name="zh-cn_topic_0224276934_p248954511513"></a><a name="zh-cn_topic_0224276934_p248954511513"></a><a href="#zh-cn_topic_0224276934_response_Rs1363TokenUser">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p4490194520514"><a name="zh-cn_topic_0224276934_p4490194520514"></a><a name="zh-cn_topic_0224276934_p4490194520514"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p1049064565111"><a name="zh-cn_topic_0224276934_p1049064565111"></a><a name="zh-cn_topic_0224276934_p1049064565111"></a>获取token的用户信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row1648564511518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p184901945115114"><a name="zh-cn_topic_0224276934_p184901945115114"></a><a name="zh-cn_topic_0224276934_p184901945115114"></a>issued_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p194904451519"><a name="zh-cn_topic_0224276934_p194904451519"></a><a name="zh-cn_topic_0224276934_p194904451519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p204907455511"><a name="zh-cn_topic_0224276934_p204907455511"></a><a name="zh-cn_topic_0224276934_p204907455511"></a>token下发时间。</p>
</td>
</tr>
</tbody>
</table>

**表 13**  token.catalog

<a name="zh-cn_topic_0224276934_response_Rs1363TokenCatalogArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row1549104516513"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p049413459516"><a name="zh-cn_topic_0224276934_p049413459516"></a><a name="zh-cn_topic_0224276934_p049413459516"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p1649434555118"><a name="zh-cn_topic_0224276934_p1649434555118"></a><a name="zh-cn_topic_0224276934_p1649434555118"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p1149404525117"><a name="zh-cn_topic_0224276934_p1149404525117"></a><a name="zh-cn_topic_0224276934_p1149404525117"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row16491124565113"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p1549418457517"><a name="zh-cn_topic_0224276934_p1549418457517"></a><a name="zh-cn_topic_0224276934_p1549418457517"></a>type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p16495144545116"><a name="zh-cn_topic_0224276934_p16495144545116"></a><a name="zh-cn_topic_0224276934_p16495144545116"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p849511457516"><a name="zh-cn_topic_0224276934_p849511457516"></a><a name="zh-cn_topic_0224276934_p849511457516"></a>该接口所属服务。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row8493164518515"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p3495104515112"><a name="zh-cn_topic_0224276934_p3495104515112"></a><a name="zh-cn_topic_0224276934_p3495104515112"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p649524510517"><a name="zh-cn_topic_0224276934_p649524510517"></a><a name="zh-cn_topic_0224276934_p649524510517"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p1049512455513"><a name="zh-cn_topic_0224276934_p1049512455513"></a><a name="zh-cn_topic_0224276934_p1049512455513"></a>服务ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row11493174513516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p34951945105117"><a name="zh-cn_topic_0224276934_p34951945105117"></a><a name="zh-cn_topic_0224276934_p34951945105117"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p16495144517519"><a name="zh-cn_topic_0224276934_p16495144517519"></a><a name="zh-cn_topic_0224276934_p16495144517519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p1349664595116"><a name="zh-cn_topic_0224276934_p1349664595116"></a><a name="zh-cn_topic_0224276934_p1349664595116"></a>服务名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row1493174516511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p174961445105112"><a name="zh-cn_topic_0224276934_p174961445105112"></a><a name="zh-cn_topic_0224276934_p174961445105112"></a><a href="#zh-cn_topic_0224276934_response_Rs1363TokenCatalogArritemEndpointsArritem">endpoints</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p549618458517"><a name="zh-cn_topic_0224276934_p549618458517"></a><a name="zh-cn_topic_0224276934_p549618458517"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p104961445175112"><a name="zh-cn_topic_0224276934_p104961445175112"></a><a name="zh-cn_topic_0224276934_p104961445175112"></a>终端节点。</p>
</td>
</tr>
</tbody>
</table>

**表 14**  token.catalog.endpoints

<a name="zh-cn_topic_0224276934_response_Rs1363TokenCatalogArritemEndpointsArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row549784545119"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p1749894575117"><a name="zh-cn_topic_0224276934_p1749894575117"></a><a name="zh-cn_topic_0224276934_p1749894575117"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p94982452512"><a name="zh-cn_topic_0224276934_p94982452512"></a><a name="zh-cn_topic_0224276934_p94982452512"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p20498174512512"><a name="zh-cn_topic_0224276934_p20498174512512"></a><a name="zh-cn_topic_0224276934_p20498174512512"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row19497184518513"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p1249812455513"><a name="zh-cn_topic_0224276934_p1249812455513"></a><a name="zh-cn_topic_0224276934_p1249812455513"></a>url</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p34988453510"><a name="zh-cn_topic_0224276934_p34988453510"></a><a name="zh-cn_topic_0224276934_p34988453510"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p8499184545118"><a name="zh-cn_topic_0224276934_p8499184545118"></a><a name="zh-cn_topic_0224276934_p8499184545118"></a>终端节点的URL。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row84971145145110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p124999451516"><a name="zh-cn_topic_0224276934_p124999451516"></a><a name="zh-cn_topic_0224276934_p124999451516"></a>region</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p849913450511"><a name="zh-cn_topic_0224276934_p849913450511"></a><a name="zh-cn_topic_0224276934_p849913450511"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p849954595113"><a name="zh-cn_topic_0224276934_p849954595113"></a><a name="zh-cn_topic_0224276934_p849954595113"></a>终端节点所属区域。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row13497445165119"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p1260274505111"><a name="zh-cn_topic_0224276934_p1260274505111"></a><a name="zh-cn_topic_0224276934_p1260274505111"></a>region_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p660217459517"><a name="zh-cn_topic_0224276934_p660217459517"></a><a name="zh-cn_topic_0224276934_p660217459517"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p1860204535114"><a name="zh-cn_topic_0224276934_p1860204535114"></a><a name="zh-cn_topic_0224276934_p1860204535114"></a>终端节点所属区域ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row15497134565114"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p1960218457514"><a name="zh-cn_topic_0224276934_p1960218457514"></a><a name="zh-cn_topic_0224276934_p1960218457514"></a>interface</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p19602194545117"><a name="zh-cn_topic_0224276934_p19602194545117"></a><a name="zh-cn_topic_0224276934_p19602194545117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p06021453514"><a name="zh-cn_topic_0224276934_p06021453514"></a><a name="zh-cn_topic_0224276934_p06021453514"></a>接口类型，描述接口在该终端节点的可见性。值为“public”，表示该接口为公开接口。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row549764595117"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p56028451518"><a name="zh-cn_topic_0224276934_p56028451518"></a><a name="zh-cn_topic_0224276934_p56028451518"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p860244518514"><a name="zh-cn_topic_0224276934_p860244518514"></a><a name="zh-cn_topic_0224276934_p860244518514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p13602114575115"><a name="zh-cn_topic_0224276934_p13602114575115"></a><a name="zh-cn_topic_0224276934_p13602114575115"></a>终端节点ID。</p>
</td>
</tr>
</tbody>
</table>

**表 15**  token.domain

<a name="zh-cn_topic_0224276934_response_Rs1363TokenDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row1750184513511"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p9602945165114"><a name="zh-cn_topic_0224276934_p9602945165114"></a><a name="zh-cn_topic_0224276934_p9602945165114"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p36031345125119"><a name="zh-cn_topic_0224276934_p36031345125119"></a><a name="zh-cn_topic_0224276934_p36031345125119"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p166034451513"><a name="zh-cn_topic_0224276934_p166034451513"></a><a name="zh-cn_topic_0224276934_p166034451513"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row950114455518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p060314516516"><a name="zh-cn_topic_0224276934_p060314516516"></a><a name="zh-cn_topic_0224276934_p060314516516"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p26031345125110"><a name="zh-cn_topic_0224276934_p26031345125110"></a><a name="zh-cn_topic_0224276934_p26031345125110"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p1660324555110"><a name="zh-cn_topic_0224276934_p1660324555110"></a><a name="zh-cn_topic_0224276934_p1660324555110"></a>帐号名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row7501104515510"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p1660314555119"><a name="zh-cn_topic_0224276934_p1660314555119"></a><a name="zh-cn_topic_0224276934_p1660314555119"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p0603194545113"><a name="zh-cn_topic_0224276934_p0603194545113"></a><a name="zh-cn_topic_0224276934_p0603194545113"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p9603144515114"><a name="zh-cn_topic_0224276934_p9603144515114"></a><a name="zh-cn_topic_0224276934_p9603144515114"></a>帐号ID。</p>
</td>
</tr>
</tbody>
</table>

**表 16**  token.project

<a name="zh-cn_topic_0224276934_response_Rs1363TokenProject"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row150317458518"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p1060314515515"><a name="zh-cn_topic_0224276934_p1060314515515"></a><a name="zh-cn_topic_0224276934_p1060314515515"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p1603345125110"><a name="zh-cn_topic_0224276934_p1603345125110"></a><a name="zh-cn_topic_0224276934_p1603345125110"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p16037451519"><a name="zh-cn_topic_0224276934_p16037451519"></a><a name="zh-cn_topic_0224276934_p16037451519"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row750314545111"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p76038451513"><a name="zh-cn_topic_0224276934_p76038451513"></a><a name="zh-cn_topic_0224276934_p76038451513"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p1460314585113"><a name="zh-cn_topic_0224276934_p1460314585113"></a><a name="zh-cn_topic_0224276934_p1460314585113"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p176031245175117"><a name="zh-cn_topic_0224276934_p176031245175117"></a><a name="zh-cn_topic_0224276934_p176031245175117"></a>项目名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row050374565115"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p15603154515110"><a name="zh-cn_topic_0224276934_p15603154515110"></a><a name="zh-cn_topic_0224276934_p15603154515110"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p1260320456515"><a name="zh-cn_topic_0224276934_p1260320456515"></a><a name="zh-cn_topic_0224276934_p1260320456515"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p17603134585113"><a name="zh-cn_topic_0224276934_p17603134585113"></a><a name="zh-cn_topic_0224276934_p17603134585113"></a>项目ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row14503184514511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p96031745175118"><a name="zh-cn_topic_0224276934_p96031745175118"></a><a name="zh-cn_topic_0224276934_p96031745175118"></a><a href="#zh-cn_topic_0224276934_response_Rs1363TokenProjectDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p26035458516"><a name="zh-cn_topic_0224276934_p26035458516"></a><a name="zh-cn_topic_0224276934_p26035458516"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p186031452519"><a name="zh-cn_topic_0224276934_p186031452519"></a><a name="zh-cn_topic_0224276934_p186031452519"></a>项目所属帐号信息。</p>
</td>
</tr>
</tbody>
</table>

**表 17**  token.project.domain

<a name="zh-cn_topic_0224276934_response_Rs1363TokenProjectDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row1750874535111"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p26031545175117"><a name="zh-cn_topic_0224276934_p26031545175117"></a><a name="zh-cn_topic_0224276934_p26031545175117"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p1360312454510"><a name="zh-cn_topic_0224276934_p1360312454510"></a><a name="zh-cn_topic_0224276934_p1360312454510"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p1160311450518"><a name="zh-cn_topic_0224276934_p1160311450518"></a><a name="zh-cn_topic_0224276934_p1160311450518"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row150824515118"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p260394585110"><a name="zh-cn_topic_0224276934_p260394585110"></a><a name="zh-cn_topic_0224276934_p260394585110"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p10603645165115"><a name="zh-cn_topic_0224276934_p10603645165115"></a><a name="zh-cn_topic_0224276934_p10603645165115"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p1660394595117"><a name="zh-cn_topic_0224276934_p1660394595117"></a><a name="zh-cn_topic_0224276934_p1660394595117"></a>帐号名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row1750804510511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p8603845205110"><a name="zh-cn_topic_0224276934_p8603845205110"></a><a name="zh-cn_topic_0224276934_p8603845205110"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p18603114519511"><a name="zh-cn_topic_0224276934_p18603114519511"></a><a name="zh-cn_topic_0224276934_p18603114519511"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p2604204555116"><a name="zh-cn_topic_0224276934_p2604204555116"></a><a name="zh-cn_topic_0224276934_p2604204555116"></a>帐号ID。</p>
</td>
</tr>
</tbody>
</table>

**表 18**  token.roles

<a name="zh-cn_topic_0224276934_response_Rs1363TokenRolesArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row7511164514519"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p16045459512"><a name="zh-cn_topic_0224276934_p16045459512"></a><a name="zh-cn_topic_0224276934_p16045459512"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p1160454512519"><a name="zh-cn_topic_0224276934_p1160454512519"></a><a name="zh-cn_topic_0224276934_p1160454512519"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p3604154516519"><a name="zh-cn_topic_0224276934_p3604154516519"></a><a name="zh-cn_topic_0224276934_p3604154516519"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row051115459510"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p1360411459519"><a name="zh-cn_topic_0224276934_p1360411459519"></a><a name="zh-cn_topic_0224276934_p1360411459519"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p8604174535116"><a name="zh-cn_topic_0224276934_p8604174535116"></a><a name="zh-cn_topic_0224276934_p8604174535116"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p260444525112"><a name="zh-cn_topic_0224276934_p260444525112"></a><a name="zh-cn_topic_0224276934_p260444525112"></a>权限名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row1451111458517"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p1960444545112"><a name="zh-cn_topic_0224276934_p1960444545112"></a><a name="zh-cn_topic_0224276934_p1960444545112"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p2604134585113"><a name="zh-cn_topic_0224276934_p2604134585113"></a><a name="zh-cn_topic_0224276934_p2604134585113"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p5604104519511"><a name="zh-cn_topic_0224276934_p5604104519511"></a><a name="zh-cn_topic_0224276934_p5604104519511"></a>权限ID。默认显示为0，非真实权限ID。</p>
</td>
</tr>
</tbody>
</table>

**表 19**  token.user

<a name="zh-cn_topic_0224276934_response_Rs1363TokenUser"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row25143455516"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p16604184511516"><a name="zh-cn_topic_0224276934_p16604184511516"></a><a name="zh-cn_topic_0224276934_p16604184511516"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p5604164513514"><a name="zh-cn_topic_0224276934_p5604164513514"></a><a name="zh-cn_topic_0224276934_p5604164513514"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p1060419458517"><a name="zh-cn_topic_0224276934_p1060419458517"></a><a name="zh-cn_topic_0224276934_p1060419458517"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row115141245115114"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p4604845115119"><a name="zh-cn_topic_0224276934_p4604845115119"></a><a name="zh-cn_topic_0224276934_p4604845115119"></a><a href="#zh-cn_topic_0224276934_response_Rs1363TokenUserDomain">domain</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p360454512510"><a name="zh-cn_topic_0224276934_p360454512510"></a><a name="zh-cn_topic_0224276934_p360454512510"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p206041945135114"><a name="zh-cn_topic_0224276934_p206041945135114"></a><a name="zh-cn_topic_0224276934_p206041945135114"></a>用户所属帐号信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row1851414455517"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p13604945125114"><a name="zh-cn_topic_0224276934_p13604945125114"></a><a name="zh-cn_topic_0224276934_p13604945125114"></a><a href="#zh-cn_topic_0224276934_response_Rs1363TokenUserOsfederation">OS-FEDERATION</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p0604114575118"><a name="zh-cn_topic_0224276934_p0604114575118"></a><a name="zh-cn_topic_0224276934_p0604114575118"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p196044458515"><a name="zh-cn_topic_0224276934_p196044458515"></a><a name="zh-cn_topic_0224276934_p196044458515"></a>联邦身份认证信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row351414595116"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p2604134519512"><a name="zh-cn_topic_0224276934_p2604134519512"></a><a name="zh-cn_topic_0224276934_p2604134519512"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p17604045105117"><a name="zh-cn_topic_0224276934_p17604045105117"></a><a name="zh-cn_topic_0224276934_p17604045105117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p66041345155118"><a name="zh-cn_topic_0224276934_p66041345155118"></a><a name="zh-cn_topic_0224276934_p66041345155118"></a>用户ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row35141245155119"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p960474595118"><a name="zh-cn_topic_0224276934_p960474595118"></a><a name="zh-cn_topic_0224276934_p960474595118"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p1060419459519"><a name="zh-cn_topic_0224276934_p1060419459519"></a><a name="zh-cn_topic_0224276934_p1060419459519"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p860412454518"><a name="zh-cn_topic_0224276934_p860412454518"></a><a name="zh-cn_topic_0224276934_p860412454518"></a>用户名。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row19514174514518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p116042045145113"><a name="zh-cn_topic_0224276934_p116042045145113"></a><a name="zh-cn_topic_0224276934_p116042045145113"></a>password_expires_at</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p8604114515118"><a name="zh-cn_topic_0224276934_p8604114515118"></a><a name="zh-cn_topic_0224276934_p8604114515118"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p11604045145117"><a name="zh-cn_topic_0224276934_p11604045145117"></a><a name="zh-cn_topic_0224276934_p11604045145117"></a>密码过期时间（UTC时间），“”表示密码不过期。</p>
</td>
</tr>
</tbody>
</table>

**表 20**  token.user.domain

<a name="zh-cn_topic_0224276934_response_Rs1363TokenUserDomain"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row1651813457511"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p15605645115113"><a name="zh-cn_topic_0224276934_p15605645115113"></a><a name="zh-cn_topic_0224276934_p15605645115113"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p17605174515511"><a name="zh-cn_topic_0224276934_p17605174515511"></a><a name="zh-cn_topic_0224276934_p17605174515511"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p6605174525118"><a name="zh-cn_topic_0224276934_p6605174525118"></a><a name="zh-cn_topic_0224276934_p6605174525118"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row155181145105113"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p16054451514"><a name="zh-cn_topic_0224276934_p16054451514"></a><a name="zh-cn_topic_0224276934_p16054451514"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p15605845165114"><a name="zh-cn_topic_0224276934_p15605845165114"></a><a name="zh-cn_topic_0224276934_p15605845165114"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p860514450516"><a name="zh-cn_topic_0224276934_p860514450516"></a><a name="zh-cn_topic_0224276934_p860514450516"></a>用户所属帐号名称。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row18519545115114"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p1760510453511"><a name="zh-cn_topic_0224276934_p1760510453511"></a><a name="zh-cn_topic_0224276934_p1760510453511"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p6605134535117"><a name="zh-cn_topic_0224276934_p6605134535117"></a><a name="zh-cn_topic_0224276934_p6605134535117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p56051745145119"><a name="zh-cn_topic_0224276934_p56051745145119"></a><a name="zh-cn_topic_0224276934_p56051745145119"></a>用户所属帐号ID。</p>
</td>
</tr>
</tbody>
</table>

**表 21**  token.user.OS-FEDERATION

<a name="zh-cn_topic_0224276934_response_Rs1363TokenUserOsfederation"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row852014516514"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p260594510514"><a name="zh-cn_topic_0224276934_p260594510514"></a><a name="zh-cn_topic_0224276934_p260594510514"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p1605945115113"><a name="zh-cn_topic_0224276934_p1605945115113"></a><a name="zh-cn_topic_0224276934_p1605945115113"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p186059450518"><a name="zh-cn_topic_0224276934_p186059450518"></a><a name="zh-cn_topic_0224276934_p186059450518"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row25211545165114"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p1605545185117"><a name="zh-cn_topic_0224276934_p1605545185117"></a><a name="zh-cn_topic_0224276934_p1605545185117"></a><a href="#zh-cn_topic_0224276934_response_Rs1363TokenUserOsfederationGroupsArritem">groups</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p260519455514"><a name="zh-cn_topic_0224276934_p260519455514"></a><a name="zh-cn_topic_0224276934_p260519455514"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p36051445135110"><a name="zh-cn_topic_0224276934_p36051445135110"></a><a name="zh-cn_topic_0224276934_p36051445135110"></a>用户组信息列表。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row152119451518"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p116051945135114"><a name="zh-cn_topic_0224276934_p116051945135114"></a><a name="zh-cn_topic_0224276934_p116051945135114"></a><a href="#zh-cn_topic_0224276934_response_Rs1363TokenUserOsfederationIdentityprovider">identity_provider</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p1360554525110"><a name="zh-cn_topic_0224276934_p1360554525110"></a><a name="zh-cn_topic_0224276934_p1360554525110"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p360574535114"><a name="zh-cn_topic_0224276934_p360574535114"></a><a name="zh-cn_topic_0224276934_p360574535114"></a>身份提供商信息。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row65214452516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p12605114515513"><a name="zh-cn_topic_0224276934_p12605114515513"></a><a name="zh-cn_topic_0224276934_p12605114515513"></a><a href="#zh-cn_topic_0224276934_response_Rs1363TokenUserOsfederationProtocol">protocol</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p1360510456514"><a name="zh-cn_topic_0224276934_p1360510456514"></a><a name="zh-cn_topic_0224276934_p1360510456514"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p760516455516"><a name="zh-cn_topic_0224276934_p760516455516"></a><a name="zh-cn_topic_0224276934_p760516455516"></a>协议信息。</p>
</td>
</tr>
</tbody>
</table>

**表 22**  token.user.OS-FEDERATION.groups

<a name="zh-cn_topic_0224276934_response_Rs1363TokenUserOsfederationGroupsArritem"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row75232045125115"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p186053458515"><a name="zh-cn_topic_0224276934_p186053458515"></a><a name="zh-cn_topic_0224276934_p186053458515"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p6605545195119"><a name="zh-cn_topic_0224276934_p6605545195119"></a><a name="zh-cn_topic_0224276934_p6605545195119"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p76061545195117"><a name="zh-cn_topic_0224276934_p76061545195117"></a><a name="zh-cn_topic_0224276934_p76061545195117"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row2052319455512"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p146061545175112"><a name="zh-cn_topic_0224276934_p146061545175112"></a><a name="zh-cn_topic_0224276934_p146061545175112"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p8606154520514"><a name="zh-cn_topic_0224276934_p8606154520514"></a><a name="zh-cn_topic_0224276934_p8606154520514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p16606124555114"><a name="zh-cn_topic_0224276934_p16606124555114"></a><a name="zh-cn_topic_0224276934_p16606124555114"></a>用户组ID。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row17523134515110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p76061345155110"><a name="zh-cn_topic_0224276934_p76061345155110"></a><a name="zh-cn_topic_0224276934_p76061345155110"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p7606134595114"><a name="zh-cn_topic_0224276934_p7606134595114"></a><a name="zh-cn_topic_0224276934_p7606134595114"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p186061945125119"><a name="zh-cn_topic_0224276934_p186061945125119"></a><a name="zh-cn_topic_0224276934_p186061945125119"></a>用户组名称。</p>
</td>
</tr>
</tbody>
</table>

**表 23**  token.user.OS-FEDERATION.identity\_provider

<a name="zh-cn_topic_0224276934_response_Rs1363TokenUserOsfederationIdentityprovider"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row152614555115"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p4606645155112"><a name="zh-cn_topic_0224276934_p4606645155112"></a><a name="zh-cn_topic_0224276934_p4606645155112"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p1360616453517"><a name="zh-cn_topic_0224276934_p1360616453517"></a><a name="zh-cn_topic_0224276934_p1360616453517"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p16606104545116"><a name="zh-cn_topic_0224276934_p16606104545116"></a><a name="zh-cn_topic_0224276934_p16606104545116"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row13526184515519"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p166061745135113"><a name="zh-cn_topic_0224276934_p166061745135113"></a><a name="zh-cn_topic_0224276934_p166061745135113"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p17606345165116"><a name="zh-cn_topic_0224276934_p17606345165116"></a><a name="zh-cn_topic_0224276934_p17606345165116"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p12606184519515"><a name="zh-cn_topic_0224276934_p12606184519515"></a><a name="zh-cn_topic_0224276934_p12606184519515"></a>身份提供商ID。</p>
</td>
</tr>
</tbody>
</table>

**表 24**  token.user.OS-FEDERATION.protocol

<a name="zh-cn_topic_0224276934_response_Rs1363TokenUserOsfederationProtocol"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row352734516518"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="zh-cn_topic_0224276934_p9606445185114"><a name="zh-cn_topic_0224276934_p9606445185114"></a><a name="zh-cn_topic_0224276934_p9606445185114"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="zh-cn_topic_0224276934_p1360616456511"><a name="zh-cn_topic_0224276934_p1360616456511"></a><a name="zh-cn_topic_0224276934_p1360616456511"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="zh-cn_topic_0224276934_p10606245145112"><a name="zh-cn_topic_0224276934_p10606245145112"></a><a name="zh-cn_topic_0224276934_p10606245145112"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row18527184575110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="zh-cn_topic_0224276934_p17606144575115"><a name="zh-cn_topic_0224276934_p17606144575115"></a><a name="zh-cn_topic_0224276934_p17606144575115"></a>id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0224276934_p176064454514"><a name="zh-cn_topic_0224276934_p176064454514"></a><a name="zh-cn_topic_0224276934_p176064454514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="zh-cn_topic_0224276934_p1360618450516"><a name="zh-cn_topic_0224276934_p1360618450516"></a><a name="zh-cn_topic_0224276934_p1360618450516"></a>协议ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="zh-cn_topic_0224276934_section360715450514"></a>

```
POST https://iam.myhuaweicloud.com/v3/auth/tokens
```

```
{
    "auth": {
        "identity": {
            "methods": [
                "token"
            ],
            "token": {
                "id": "MIIatAYJKoZIhvcNAQcCoIIapTCCGqECAQExDTALB..."
            }
        },
        "scope": {
            "domain": {
                "id": "063bb260a480cecc0f36c0086bb6c..."
            }
        }
    }
}
```

## 响应示例<a name="zh-cn_topic_0224276934_section16607184515515"></a>

**状态码为 201 时:**

创建成功。

```
响应Header参数：
X-Subject-Token:MIIatAYJKoZIhvcNAQcCoIIapTCCGqECAQExDTALB...
```

```
响应Body参数：
{
    "token": {
        "expires_at": "2020-02-13T14:21:34.042000Z",
        "methods": [
            "token"
        ],
        "catalog": [
            {
                "endpoints": [
                    {
                        "id": "d2983f677ce14f1e81cbb6a9345a107a",
                        "interface": "public",
                        "region": "*",
                        "region_id": "*",
                        "url": "https://iam.cn-north-1.myhuaweicloud.com/v3"
                    }
                ],
                "id": "fd631b3426cb40f0919091d5861d8fea",
                "name": "keystone",
                "type": "identity"
            }
        ],
        "domain": {
            "id": "06aa2260a480cecc0f36c0086bb6cfe0",
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
            }
        ],
        "issued_at": "2020-02-12T14:21:34.042000Z",
        "user": {
            "OS-FEDERATION": {
                "groups": [
                    {
                        "id": "06aa2260bb00cecc3f3ac0084a74038f",
                        "name": "admin"
                    }
                ],
                "identity_provider": {
                    "id": "ACME"
                },
                "protocol": {
                    "id": "saml"
                }
            },
            "domain": {
                "id": "06aa2260a480cecc0f36c0086bb6cfe0",
                "name": "IAMDomain"
            },
            "id": "LdQTDSC7zmJVIic3yaCbLBXDxPAdDxLg",
            "name": "FederationUser",
            "password_expires_at": ""
        }
    }
}
```

## 返回值<a name="zh-cn_topic_0224276934_section560911453517"></a>

<a name="zh-cn_topic_0224276934_table4331"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276934_row6536145105117"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0224276934_p1609134518512"><a name="zh-cn_topic_0224276934_p1609134518512"></a><a name="zh-cn_topic_0224276934_p1609134518512"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0224276934_p5609164510514"><a name="zh-cn_topic_0224276934_p5609164510514"></a><a name="zh-cn_topic_0224276934_p5609164510514"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276934_row853694585116"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276934_p176098453518"><a name="zh-cn_topic_0224276934_p176098453518"></a><a name="zh-cn_topic_0224276934_p176098453518"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276934_p1960912452514"><a name="zh-cn_topic_0224276934_p1960912452514"></a><a name="zh-cn_topic_0224276934_p1960912452514"></a>创建成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row17536645135119"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276934_p160916451517"><a name="zh-cn_topic_0224276934_p160916451517"></a><a name="zh-cn_topic_0224276934_p160916451517"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276934_p260934512511"><a name="zh-cn_topic_0224276934_p260934512511"></a><a name="zh-cn_topic_0224276934_p260934512511"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row195368458516"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276934_p26091445125112"><a name="zh-cn_topic_0224276934_p26091445125112"></a><a name="zh-cn_topic_0224276934_p26091445125112"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276934_p3609114518517"><a name="zh-cn_topic_0224276934_p3609114518517"></a><a name="zh-cn_topic_0224276934_p3609114518517"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row1753604512513"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276934_p9609184515116"><a name="zh-cn_topic_0224276934_p9609184515116"></a><a name="zh-cn_topic_0224276934_p9609184515116"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276934_p1060924513511"><a name="zh-cn_topic_0224276934_p1060924513511"></a><a name="zh-cn_topic_0224276934_p1060924513511"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row19536154511516"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276934_p12609164520511"><a name="zh-cn_topic_0224276934_p12609164520511"></a><a name="zh-cn_topic_0224276934_p12609164520511"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276934_p06091045125111"><a name="zh-cn_topic_0224276934_p06091045125111"></a><a name="zh-cn_topic_0224276934_p06091045125111"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row2536104575110"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276934_p060994514518"><a name="zh-cn_topic_0224276934_p060994514518"></a><a name="zh-cn_topic_0224276934_p060994514518"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276934_p26094453515"><a name="zh-cn_topic_0224276934_p26094453515"></a><a name="zh-cn_topic_0224276934_p26094453515"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276934_row17536124545112"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276934_p660984515516"><a name="zh-cn_topic_0224276934_p660984515516"></a><a name="zh-cn_topic_0224276934_p660984515516"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276934_p1360934517515"><a name="zh-cn_topic_0224276934_p1360934517515"></a><a name="zh-cn_topic_0224276934_p1360934517515"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0224276934_section460994518518"></a>

无

