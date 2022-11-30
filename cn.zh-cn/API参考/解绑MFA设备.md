# 解绑MFA设备<a name="iam_08_0018"></a>

## 功能介绍<a name="section698451634412"></a>

该接口可以用于管理员为IAM用户解绑MFA设备，或IAM用户为自己解绑MFA设备。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section298618166442"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=DeleteBindingDevice)中调试该接口。

## URI<a name="section1998681664419"></a>

PUT /v3.0/OS-MFA/mfa-devices/unbind

## 请求参数<a name="section39875160445"></a>

**表 1**  请求Header参数

<a name="table17988131611449"></a>
<table><thead align="left"><tr id="row65141784411"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p0513171446"><a name="p0513171446"></a><a name="p0513171446"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="p852181794414"><a name="p852181794414"></a><a name="p852181794414"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p25220171448"><a name="p25220171448"></a><a name="p25220171448"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.4"><p id="p10524177445"><a name="p10524177445"></a><a name="p10524177445"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row175251754412"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p452191720448"><a name="p452191720448"></a><a name="p452191720448"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p185281754419"><a name="p185281754419"></a><a name="p185281754419"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p16521417164411"><a name="p16521417164411"></a><a name="p16521417164411"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><a name="ul1948614712363"></a><a name="ul1948614712363"></a><ul id="ul1948614712363"><li><u id="u39439113483"><a name="u39439113483"></a><a name="u39439113483"></a><a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a></u><u id="u199449111482"><a name="u199449111482"></a><a name="u199449111482"></a></u>为IAM用户解绑MFA设备：请参见<a href="授权项.md">授权项</a>。</li><li>IAM用户为自己解绑MFA设备：请求Body中user_id所对应IAM用户的token（无需特殊权限）。</li></ul>
</td>
</tr>
</tbody>
</table>

**表 2**  请求Body参数

<a name="table999581614449"></a>
<table><thead align="left"><tr id="row45271784415"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p15217174442"><a name="p15217174442"></a><a name="p15217174442"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="p652181713444"><a name="p652181713444"></a><a name="p652181713444"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p8522017104416"><a name="p8522017104416"></a><a name="p8522017104416"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.4"><p id="p105231794417"><a name="p105231794417"></a><a name="p105231794417"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row352201794410"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p16527172448"><a name="p16527172448"></a><a name="p16527172448"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p452191717443"><a name="p452191717443"></a><a name="p452191717443"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1952917104419"><a name="p1952917104419"></a><a name="p1952917104419"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p252171734418"><a name="p252171734418"></a><a name="p252171734418"></a>待解绑MFA设备的IAM用户ID。</p>
</td>
</tr>
<tr id="row135281718446"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p652141713443"><a name="p652141713443"></a><a name="p652141713443"></a>authentication_code</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p18521417184416"><a name="p18521417184416"></a><a name="p18521417184416"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p252717174419"><a name="p252717174419"></a><a name="p252717174419"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><a name="ul1426718376208"></a><a name="ul1426718376208"></a><ul id="ul1426718376208"><li><u id="u9346113623012"><a name="u9346113623012"></a><a name="u9346113623012"></a><a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a></u><u id="u034693613014"><a name="u034693613014"></a><a name="u034693613014"></a></u>为IAM用户解绑MFA设备：填写6位任意验证码，不做校验。</li><li>IAM用户为自己解绑MFA设备：填写虚拟MFA验证码。</li></ul>
</td>
</tr>
<tr id="row95211714447"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p952171794415"><a name="p952171794415"></a><a name="p952171794415"></a>serial_number</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p9521217154415"><a name="p9521217154415"></a><a name="p9521217154415"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p115219174441"><a name="p115219174441"></a><a name="p115219174441"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p65211714447"><a name="p65211714447"></a><a name="p65211714447"></a>MFA设备序列号。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section72117164415"></a>

无

## 请求示例<a name="section162161764418"></a>

```
PUT https://iam.myhuaweicloud.com/v3.0/OS-MFA/mfa-devices/unbind 

{ 
  "user_id" : "09f99d8f6a001d4f1f01c00c31968...", 
  "authentication_code" : "373658", 
  "serial_number" : "iam:09f6bd6a96801de40f01c00c85691...:mfa/{device_name}" 
}
```

## 响应示例<a name="section174151715447"></a>

**状态码：204**

请求成功。

## 状态码<a name="section174151734417"></a>

<a name="table281471411116"></a>
<table><thead align="left"><tr id="row284112140110"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p138410141513"><a name="p138410141513"></a><a name="p138410141513"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p128413148118"><a name="p128413148118"></a><a name="p128413148118"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row138418143110"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p584115142116"><a name="p584115142116"></a><a name="p584115142116"></a>204</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p1084115141615"><a name="p1084115141615"></a><a name="p1084115141615"></a>请求成功。</p>
</td>
</tr>
<tr id="row1384119141719"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p158411914210"><a name="p158411914210"></a><a name="p158411914210"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p884131417111"><a name="p884131417111"></a><a name="p884131417111"></a>请求校验异常。</p>
</td>
</tr>
<tr id="row89391858121712"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p893975841710"><a name="p893975841710"></a><a name="p893975841710"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p841510618185"><a name="p841510618185"></a><a name="p841510618185"></a>认证失败。</p>
</td>
</tr>
<tr id="row5841191419119"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p684116149115"><a name="p684116149115"></a><a name="p684116149115"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p984119141014"><a name="p984119141014"></a><a name="p984119141014"></a>请求未授权。</p>
</td>
</tr>
<tr id="row1584115141619"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p584141413112"><a name="p584141413112"></a><a name="p584141413112"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p0841181418112"><a name="p0841181418112"></a><a name="p0841181418112"></a>无法找到请求资源。</p>
</td>
</tr>
<tr id="row1584191414115"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p158414141015"><a name="p158414141015"></a><a name="p158414141015"></a>409</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p48415141012"><a name="p48415141012"></a><a name="p48415141012"></a>保存请求资源时发生冲突。</p>
</td>
</tr>
<tr id="row168412142114"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p88419141411"><a name="p88419141411"></a><a name="p88419141411"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p1784151411111"><a name="p1784151411111"></a><a name="p1784151411111"></a>系统错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section051417124413"></a>

请参见[错误码](错误码.md)。

