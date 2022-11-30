# 删除MFA设备<a name="iam_08_0020"></a>

## 功能介绍<a name="section13815375453"></a>

该接口可以用于<u>[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)</u><u></u>删除自己的MFA设备。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section210113711459"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=DeleteMfaDevice)中调试该接口。

## URI<a name="section61113734514"></a>

DELETE /v3.0/OS-MFA/virtual-mfa-devices

**表 1**  Query参数

<a name="table8115376457"></a>
<table><thead align="left"><tr id="row1457113714454"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p35714371453"><a name="p35714371453"></a><a name="p35714371453"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="p157193712456"><a name="p157193712456"></a><a name="p157193712456"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1457173774515"><a name="p1457173774515"></a><a name="p1457173774515"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.4"><p id="p157437184511"><a name="p157437184511"></a><a name="p157437184511"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row8571337194510"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p195715371454"><a name="p195715371454"></a><a name="p195715371454"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p165793784515"><a name="p165793784515"></a><a name="p165793784515"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p9578374455"><a name="p9578374455"></a><a name="p9578374455"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p1057113794510"><a name="p1057113794510"></a><a name="p1057113794510"></a>待删除MFA设备的IAM用户ID，即管理员自己的用户ID。获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a></p>
</td>
</tr>
<tr id="row1757173715458"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p15714371459"><a name="p15714371459"></a><a name="p15714371459"></a>serial_number</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p2571379452"><a name="p2571379452"></a><a name="p2571379452"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p155711375458"><a name="p155711375458"></a><a name="p155711375458"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p75716371452"><a name="p75716371452"></a><a name="p75716371452"></a>MFA设备序列号。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="section151913704512"></a>

**表 2**  请求Header参数

<a name="table1219143713456"></a>
<table><thead align="left"><tr id="row185719375453"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p1257837144514"><a name="p1257837144514"></a><a name="p1257837144514"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="p10571637154512"><a name="p10571637154512"></a><a name="p10571637154512"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p17571637204519"><a name="p17571637204519"></a><a name="p17571637204519"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.4"><p id="p165723715459"><a name="p165723715459"></a><a name="p165723715459"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1257837154516"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p10579376455"><a name="p10579376455"></a><a name="p10579376455"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p2571137184511"><a name="p2571137184511"></a><a name="p2571137184511"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p85783714514"><a name="p85783714514"></a><a name="p85783714514"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p105783714519"><a name="p105783714519"></a><a name="p105783714519"></a>请求Body中user_id所对应IAM用户且拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section2022123774519"></a>

无

## 请求示例<a name="section5221237124519"></a>

```
DELETE https://iam.myhuaweicloud.com/v3.0/OS-MFA/virtual-mfa-devices?user_id=09f6bd85fc801de41f0cc00ce9172...&serial_number=iam:09f6bd6a96801de40f01c00c85691...:mfa/{device_name}
```

## 响应示例<a name="section182311375454"></a>

**状态码：204**

请求成功。

## 状态码<a name="section1724337184510"></a>

<a name="table179395257320"></a>
<table><thead align="left"><tr id="row109795251437"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p19979625432"><a name="p19979625432"></a><a name="p19979625432"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p1397913251130"><a name="p1397913251130"></a><a name="p1397913251130"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row697919251439"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p29791257310"><a name="p29791257310"></a><a name="p29791257310"></a>204</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p097917255318"><a name="p097917255318"></a><a name="p097917255318"></a>请求成功。</p>
</td>
</tr>
<tr id="row145617152192"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p10457715161911"><a name="p10457715161911"></a><a name="p10457715161911"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p1260142361911"><a name="p1260142361911"></a><a name="p1260142361911"></a>认证失败。</p>
</td>
</tr>
<tr id="row897932520311"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p159791253316"><a name="p159791253316"></a><a name="p159791253316"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p14979122516316"><a name="p14979122516316"></a><a name="p14979122516316"></a>请求未授权。</p>
</td>
</tr>
<tr id="row597917251316"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p897919256313"><a name="p897919256313"></a><a name="p897919256313"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p179799251734"><a name="p179799251734"></a><a name="p179799251734"></a>系统错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section132553710451"></a>

请参见[错误码](错误码.md)。

