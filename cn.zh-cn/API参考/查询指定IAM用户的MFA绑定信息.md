# 查询指定IAM用户的MFA绑定信息<a name="iam_08_0013"></a>

## 功能介绍<a name="section1846415183370"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)查询指定IAM用户的MFA绑定信息，或IAM用户查询自己的MFA绑定信息。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section208601812145917"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=ShowUserMfaDevice)中调试该接口。

## URI<a name="section846551803716"></a>

GET /v3.0/OS-MFA/users/\{user\_id\}/virtual-mfa-device

**表 1**  路径参数

<a name="table1446518184371"></a>
<table><thead align="left"><tr id="row9539141863717"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p18539618173713"><a name="p18539618173713"></a><a name="p18539618173713"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p35391218163711"><a name="p35391218163711"></a><a name="p35391218163711"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1053920189375"><a name="p1053920189375"></a><a name="p1053920189375"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p653901853710"><a name="p653901853710"></a><a name="p653901853710"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row35398183373"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p105391318183711"><a name="p105391318183711"></a><a name="p105391318183711"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p2053921814377"><a name="p2053921814377"></a><a name="p2053921814377"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p253919186372"><a name="p253919186372"></a><a name="p253919186372"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p1453981817371"><a name="p1453981817371"></a><a name="p1453981817371"></a>待查询的IAM用户ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="section1446991883716"></a>

**表 2**  请求Header参数

<a name="table19469131813376"></a>
<table><thead align="left"><tr id="row6539191813371"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p75391618203718"><a name="p75391618203718"></a><a name="p75391618203718"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p1653931812370"><a name="p1653931812370"></a><a name="p1653931812370"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p0539131811378"><a name="p0539131811378"></a><a name="p0539131811378"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p15540518123714"><a name="p15540518123714"></a><a name="p15540518123714"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1754091815377"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p3540191823716"><a name="p3540191823716"></a><a name="p3540191823716"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p19540151883720"><a name="p19540151883720"></a><a name="p19540151883720"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p254041814370"><a name="p254041814370"></a><a name="p254041814370"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p12540171819379"><a name="p12540171819379"></a><a name="p12540171819379"></a><a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询IAM用户的MFA绑定信息：拥有Security Administrator权限的token。</p>
<p id="p165401188378"><a name="p165401188378"></a><a name="p165401188378"></a>IAM用户查询自己的MFA绑定信息：URL中user_id所对应IAM用户的token（无需特殊权限）。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section6474318103711"></a>

**表 3**  响应Body参数

<a name="table947571883710"></a>
<table><thead align="left"><tr id="row1540518133716"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p3540161883714"><a name="p3540161883714"></a><a name="p3540161883714"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p7540518143717"><a name="p7540518143717"></a><a name="p7540518143717"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p16540151853715"><a name="p16540151853715"></a><a name="p16540151853715"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row8540818203715"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p18540161853711"><a name="p18540161853711"></a><a name="p18540161853711"></a><a href="#table64771918103713">virtual_mfa_device</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1954001883710"><a name="p1954001883710"></a><a name="p1954001883710"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p13540191873718"><a name="p13540191873718"></a><a name="p13540191873718"></a>虚拟MFA设备信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  virtual\_mfa\_device

<a name="table64771918103713"></a>
<table><thead align="left"><tr id="row12540518123715"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p10540111817377"><a name="p10540111817377"></a><a name="p10540111817377"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p2540118103714"><a name="p2540118103714"></a><a name="p2540118103714"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p75401618173712"><a name="p75401618173712"></a><a name="p75401618173712"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row854012181377"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p954011843711"><a name="p954011843711"></a><a name="p954011843711"></a>serial_number</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p185407185371"><a name="p185407185371"></a><a name="p185407185371"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p854091863717"><a name="p854091863717"></a><a name="p854091863717"></a>虚拟MFA的设备序列号。</p>
</td>
</tr>
<tr id="row354061843717"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p155401818163711"><a name="p155401818163711"></a><a name="p155401818163711"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p6540161812370"><a name="p6540161812370"></a><a name="p6540161812370"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1054061813373"><a name="p1054061813373"></a><a name="p1054061813373"></a>IAM用户ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section5480318193718"></a>

```
GET https://iam.myhuaweicloud.com/v3.0/OS-MFA/users/{user_id}/virtual-mfa-device
```

## 响应示例<a name="section1748091810373"></a>

**状态码为 200 时:**

请求成功。

```
{ 
  "virtual_mfa_device" :
    { 
      "user_id" : "16b26081f43d4c628c4bb88cf32e9...", 
      "serial_number" : "iam/mfa/16b26081f43d4c628c4bb88cf32e9..." 
     } 
}
```

**状态码为 403 时:**

没有操作权限。

-   示例 1

```
{ 
   "error_msg" : "You are not authorized to perform the requested action.", 
   "error_code" : "IAM.0002" 
 }
```

-   示例 2

```
{ 
   "error_msg" : "Policy doesn't allow %(actions)s to be performed.", 
   "error_code" : "IAM.0003" 
 }
```

**状态码为 404 时:**

未找到相应的资源。

```
{ 
  "error_msg" : "Could not find %(target)s: %(target_id)s.", 
  "error_code" : "IAM.0004" 
}
```

**状态码为 500 时:**

内部服务错误。

```
{ 
  "error_msg" : "An unexpected error prevented the server from fulfilling your request.", 
  "error_code" : "IAM.0006" 
}
```

## 状态码<a name="section1348331893719"></a>

<a name="table194836186370"></a>
<table><thead align="left"><tr id="row2540181814377"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p195402187374"><a name="p195402187374"></a><a name="p195402187374"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p0540131819373"><a name="p0540131819373"></a><a name="p0540131819373"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row9540121893718"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p4540318193712"><a name="p4540318193712"></a><a name="p4540318193712"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p1854019180374"><a name="p1854019180374"></a><a name="p1854019180374"></a>请求成功。</p>
</td>
</tr>
<tr id="row115401418163713"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p65407183374"><a name="p65407183374"></a><a name="p65407183374"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p4540121817374"><a name="p4540121817374"></a><a name="p4540121817374"></a>认证失败。</p>
</td>
</tr>
<tr id="row165401318173712"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p75408184372"><a name="p75408184372"></a><a name="p75408184372"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p6540131812373"><a name="p6540131812373"></a><a name="p6540131812373"></a>没有操作权限。</p>
</td>
</tr>
<tr id="row25400184373"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p75412184374"><a name="p75412184374"></a><a name="p75412184374"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p25411118203711"><a name="p25411118203711"></a><a name="p25411118203711"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="row20541418193718"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p954118188372"><a name="p954118188372"></a><a name="p954118188372"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p185411218153711"><a name="p185411218153711"></a><a name="p185411218153711"></a>内部服务错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section1948716183378"></a>

请参见[错误码](错误码.md)。

