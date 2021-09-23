# 绑定MFA设备<a name="iam_08_0017"></a>

## 功能介绍<a name="section147128110526"></a>

该接口可以用于IAM用户为自己绑定MFA设备。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section10947910105418"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=CreateBindingDevice)中调试该接口。

## URI<a name="section15147105435411"></a>

PUT /v3.0/OS-MFA/mfa-devices/bind

## 请求参数<a name="section1724151510553"></a>

**表 1**  请求Header参数

<a name="table2069611019558"></a>
<table><thead align="left"><tr id="row1474681013553"><th class="cellrowborder" valign="top" width="22.07%" id="mcps1.2.5.1.1"><p id="p11746101065515"><a name="p11746101065515"></a><a name="p11746101065515"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.620000000000001%" id="mcps1.2.5.1.2"><p id="p87467103555"><a name="p87467103555"></a><a name="p87467103555"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10.59%" id="mcps1.2.5.1.3"><p id="p1074691020553"><a name="p1074691020553"></a><a name="p1074691020553"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="56.720000000000006%" id="mcps1.2.5.1.4"><p id="p174651035517"><a name="p174651035517"></a><a name="p174651035517"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row20746610145519"><td class="cellrowborder" valign="top" width="22.07%" headers="mcps1.2.5.1.1 "><p id="p10746131015552"><a name="p10746131015552"></a><a name="p10746131015552"></a>X-Auth-token</p>
</td>
<td class="cellrowborder" valign="top" width="10.620000000000001%" headers="mcps1.2.5.1.2 "><p id="p674621014551"><a name="p674621014551"></a><a name="p674621014551"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10.59%" headers="mcps1.2.5.1.3 "><p id="p197468100553"><a name="p197468100553"></a><a name="p197468100553"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.720000000000006%" headers="mcps1.2.5.1.4 "><p id="p8271444161917"><a name="p8271444161917"></a><a name="p8271444161917"></a>请求Body中user_id所对应IAM用户的token（无需特殊权限）。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  请求Body参数

<a name="table86822147567"></a>
<table><thead align="left"><tr id="row368217141563"><th class="cellrowborder" valign="top" width="22.16%" id="mcps1.2.5.1.1"><p id="p53866413183"><a name="p53866413183"></a><a name="p53866413183"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10.81%" id="mcps1.2.5.1.2"><p id="p4386144110180"><a name="p4386144110180"></a><a name="p4386144110180"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10.71%" id="mcps1.2.5.1.3"><p id="p10386941161812"><a name="p10386941161812"></a><a name="p10386941161812"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="56.32%" id="mcps1.2.5.1.4"><p id="p5386164114188"><a name="p5386164114188"></a><a name="p5386164114188"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row196821143566"><td class="cellrowborder" valign="top" width="22.16%" headers="mcps1.2.5.1.1 "><p id="p538684191811"><a name="p538684191811"></a><a name="p538684191811"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10.81%" headers="mcps1.2.5.1.2 "><p id="p103861941121820"><a name="p103861941121820"></a><a name="p103861941121820"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10.71%" headers="mcps1.2.5.1.3 "><p id="p1238684101812"><a name="p1238684101812"></a><a name="p1238684101812"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.32%" headers="mcps1.2.5.1.4 "><p id="p153865419183"><a name="p153865419183"></a><a name="p153865419183"></a>待绑定MFA设备的IAM用户ID。</p>
</td>
</tr>
<tr id="row15682314185610"><td class="cellrowborder" valign="top" width="22.16%" headers="mcps1.2.5.1.1 "><p id="p2386141141816"><a name="p2386141141816"></a><a name="p2386141141816"></a>serial_number</p>
</td>
<td class="cellrowborder" valign="top" width="10.81%" headers="mcps1.2.5.1.2 "><p id="p8386154114184"><a name="p8386154114184"></a><a name="p8386154114184"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10.71%" headers="mcps1.2.5.1.3 "><p id="p11386941101818"><a name="p11386941101818"></a><a name="p11386941101818"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.32%" headers="mcps1.2.5.1.4 "><p id="p73868418187"><a name="p73868418187"></a><a name="p73868418187"></a>MFA设备序列号。</p>
</td>
</tr>
<tr id="row12682914165614"><td class="cellrowborder" valign="top" width="22.16%" headers="mcps1.2.5.1.1 "><p id="p538674113186"><a name="p538674113186"></a><a name="p538674113186"></a>authentication_code_first</p>
</td>
<td class="cellrowborder" valign="top" width="10.81%" headers="mcps1.2.5.1.2 "><p id="p103871441191817"><a name="p103871441191817"></a><a name="p103871441191817"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10.71%" headers="mcps1.2.5.1.3 "><p id="p11387141161812"><a name="p11387141161812"></a><a name="p11387141161812"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.32%" headers="mcps1.2.5.1.4 "><p id="p153877416184"><a name="p153877416184"></a><a name="p153877416184"></a>第一组验证码。</p>
</td>
</tr>
<tr id="row131971924161815"><td class="cellrowborder" valign="top" width="22.16%" headers="mcps1.2.5.1.1 "><p id="p738711416181"><a name="p738711416181"></a><a name="p738711416181"></a>authentication_code_second</p>
</td>
<td class="cellrowborder" valign="top" width="10.81%" headers="mcps1.2.5.1.2 "><p id="p1638764121817"><a name="p1638764121817"></a><a name="p1638764121817"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10.71%" headers="mcps1.2.5.1.3 "><p id="p7387114112186"><a name="p7387114112186"></a><a name="p7387114112186"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="56.32%" headers="mcps1.2.5.1.4 "><p id="p103871441151811"><a name="p103871441151811"></a><a name="p103871441151811"></a>第二组验证码。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section118661551121812"></a>

无

## 请求示例<a name="section11724811191910"></a>

```
PUT https://iam.myhuaweicloud.com/v3.0/OS-MFA/mfa-devices/bind 
 
{ 
  "user_id" : "09f99d8f6a001d4f1f01c00c31968...", 
  "authentication_code_first" : "977931", 
  "authentication_code_second" : "527347", 
  "serial_number" : "iam:09f6bd6a96801de40f01c00c85691...:mfa/{device_name}" 
}
```

## 响应示例<a name="section335322115197"></a>

**状态码：204。**

请求成功。

## 状态码<a name="section4531524171910"></a>

<a name="table4183132655719"></a>
<table><thead align="left"><tr id="row6237126205714"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p2237192645713"><a name="p2237192645713"></a><a name="p2237192645713"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p3237122612574"><a name="p3237122612574"></a><a name="p3237122612574"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row5237122612573"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p192371626155715"><a name="p192371626155715"></a><a name="p192371626155715"></a>204</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p11237162613578"><a name="p11237162613578"></a><a name="p11237162613578"></a>请求成功。</p>
</td>
</tr>
<tr id="row152371226125718"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1423772612573"><a name="p1423772612573"></a><a name="p1423772612573"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p1723782635716"><a name="p1723782635716"></a><a name="p1723782635716"></a>请求校验异常。</p>
</td>
</tr>
<tr id="row1422153871120"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1442353812119"><a name="p1442353812119"></a><a name="p1442353812119"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p841014469113"><a name="p841014469113"></a><a name="p841014469113"></a>认证失败。</p>
</td>
</tr>
<tr id="row623719266576"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p62371326115714"><a name="p62371326115714"></a><a name="p62371326115714"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p4237152635713"><a name="p4237152635713"></a><a name="p4237152635713"></a>请求未授权。</p>
</td>
</tr>
<tr id="row192372261579"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p16237126145710"><a name="p16237126145710"></a><a name="p16237126145710"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p2023702635717"><a name="p2023702635717"></a><a name="p2023702635717"></a>无法找到请求资源。</p>
</td>
</tr>
<tr id="row1323782616571"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p723742618577"><a name="p723742618577"></a><a name="p723742618577"></a>409</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p4237326145711"><a name="p4237326145711"></a><a name="p4237326145711"></a>保存请求资源时发生冲突。</p>
</td>
</tr>
<tr id="row1823718260576"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p2023722618576"><a name="p2023722618576"></a><a name="p2023722618576"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p102378265571"><a name="p102378265571"></a><a name="p102378265571"></a>系统错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section12453193014199"></a>

请参见[错误码](错误码.md)。

