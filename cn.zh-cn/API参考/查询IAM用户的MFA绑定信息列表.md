# 查询IAM用户的MFA绑定信息列表<a name="iam_08_0012"></a>

## 功能介绍<a name="section127695529365"></a>

该接口可以用于<u>[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)</u><u></u>查询IAM用户的MFA绑定信息列表。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section208601812145917"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=ListUserMfaDevices)中调试该接口。

## URI<a name="section4772205220365"></a>

GET /v3.0/OS-MFA/virtual-mfa-devices

## 请求参数<a name="section677245203611"></a>

**表 1**  请求Header参数

<a name="table877395263619"></a>
<table><thead align="left"><tr id="row585605215369"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p185616522369"><a name="p185616522369"></a><a name="p185616522369"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p98561252163613"><a name="p98561252163613"></a><a name="p98561252163613"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p28561952103613"><a name="p28561952103613"></a><a name="p28561952103613"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p1385625223610"><a name="p1385625223610"></a><a name="p1385625223610"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row128561521365"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p08567521369"><a name="p08567521369"></a><a name="p08567521369"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p14856952113610"><a name="p14856952113610"></a><a name="p14856952113610"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p6856145214366"><a name="p6856145214366"></a><a name="p6856145214366"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p9856152143613"><a name="p9856152143613"></a><a name="p9856152143613"></a>请参见<a href="授权项.md">授权项</a>。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section57801752113615"></a>

**表 2**  响应Body参数

<a name="table1578115211360"></a>
<table><thead align="left"><tr id="row12856152143611"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p1185617528362"><a name="p1185617528362"></a><a name="p1185617528362"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.15%" id="mcps1.2.4.1.2"><p id="p28561452183616"><a name="p28561452183616"></a><a name="p28561452183616"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="55.85%" id="mcps1.2.4.1.3"><p id="p198561952143619"><a name="p198561952143619"></a><a name="p198561952143619"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row185616526363"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p785645211367"><a name="p785645211367"></a><a name="p785645211367"></a><a href="#table578318529362">virtual_mfa_devices</a></p>
</td>
<td class="cellrowborder" valign="top" width="24.15%" headers="mcps1.2.4.1.2 "><p id="p168561529369"><a name="p168561529369"></a><a name="p168561529369"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="55.85%" headers="mcps1.2.4.1.3 "><p id="p17856135210369"><a name="p17856135210369"></a><a name="p17856135210369"></a>虚拟MFA设备信息列表。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  virtual\_mfa\_devices

<a name="table578318529362"></a>
<table><thead align="left"><tr id="row158561525360"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p18856155213619"><a name="p18856155213619"></a><a name="p18856155213619"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="24.15%" id="mcps1.2.4.1.2"><p id="p14856135263618"><a name="p14856135263618"></a><a name="p14856135263618"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="55.85%" id="mcps1.2.4.1.3"><p id="p1085611524364"><a name="p1085611524364"></a><a name="p1085611524364"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row485675214368"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1885613521369"><a name="p1885613521369"></a><a name="p1885613521369"></a>serial_number</p>
</td>
<td class="cellrowborder" valign="top" width="24.15%" headers="mcps1.2.4.1.2 "><p id="p4856145243611"><a name="p4856145243611"></a><a name="p4856145243611"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.85%" headers="mcps1.2.4.1.3 "><p id="p1385616523366"><a name="p1385616523366"></a><a name="p1385616523366"></a>虚拟MFA的设备序列号。</p>
</td>
</tr>
<tr id="row168561952103618"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p13856195211368"><a name="p13856195211368"></a><a name="p13856195211368"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="24.15%" headers="mcps1.2.4.1.2 "><p id="p585685210367"><a name="p585685210367"></a><a name="p585685210367"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="55.85%" headers="mcps1.2.4.1.3 "><p id="p15856152173618"><a name="p15856152173618"></a><a name="p15856152173618"></a>IAM用户ID。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section5786175216364"></a>

```
GET https://iam.myhuaweicloud.com/v3.0/OS-MFA/virtual-mfa-devices
```

## 响应示例<a name="section8787165233611"></a>

**状态码为 200 时:**

请求成功。

```
{ 
  "virtual_mfa_devices" : [ 
          { 
              "user_id" : "16b26081f43d4c628c4bb88cf32e9...", 
              "serial_number" : "iam/mfa/16b26081f43d4c628c4bb88cf32e9..." 
            }, 
           { 
              "user_id" : "47026081f43d4c628c4bb88cf32e9...", 
              "serial_number" : "iam/mfa/75226081f43d4c628c4bb88cf32e9..." 
             } 
          ] 
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

## 状态码<a name="section1879275213615"></a>

<a name="table07921452193618"></a>
<table><thead align="left"><tr id="row1285775212365"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p17857105263613"><a name="p17857105263613"></a><a name="p17857105263613"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p138573528362"><a name="p138573528362"></a><a name="p138573528362"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1785745223617"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p485745283614"><a name="p485745283614"></a><a name="p485745283614"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p16857115211367"><a name="p16857115211367"></a><a name="p16857115211367"></a>请求成功。</p>
</td>
</tr>
<tr id="row108577522366"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p28574528360"><a name="p28574528360"></a><a name="p28574528360"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p38571852123613"><a name="p38571852123613"></a><a name="p38571852123613"></a>认证失败。</p>
</td>
</tr>
<tr id="row5857185213618"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p8857552153619"><a name="p8857552153619"></a><a name="p8857552153619"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p58571052193617"><a name="p58571052193617"></a><a name="p58571052193617"></a>没有操作权限。</p>
</td>
</tr>
<tr id="row16857205215368"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p2857185243613"><a name="p2857185243613"></a><a name="p2857185243613"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p208577526367"><a name="p208577526367"></a><a name="p208577526367"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="row108574529360"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1485745212361"><a name="p1485745212361"></a><a name="p1485745212361"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p2857155215368"><a name="p2857155215368"></a><a name="p2857155215368"></a>内部服务错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section379519522369"></a>

请参见[错误码](错误码.md)。

