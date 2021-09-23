# 创建MFA设备<a name="iam_08_0019"></a>

## 功能介绍<a name="section1681425414513"></a>

该接口可以用于IAM用户为自己创建MFA设备。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section1681416549452"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=CreateMfaDevice)中调试该接口。

## URI<a name="section4814454194518"></a>

POST /v3.0/OS-MFA/virtual-mfa-devices

## 请求参数<a name="section381416548457"></a>

**表 1**  请求Header参数

<a name="table19815754194511"></a>
<table><thead align="left"><tr id="row1287575424520"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p68751654114515"><a name="p68751654114515"></a><a name="p68751654114515"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="p19875195484512"><a name="p19875195484512"></a><a name="p19875195484512"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1687518549458"><a name="p1687518549458"></a><a name="p1687518549458"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.4"><p id="p887525419455"><a name="p887525419455"></a><a name="p887525419455"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row587525434510"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p287545418452"><a name="p287545418452"></a><a name="p287545418452"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p1187565417453"><a name="p1187565417453"></a><a name="p1187565417453"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p9875654144517"><a name="p9875654144517"></a><a name="p9875654144517"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p695537131415"><a name="p695537131415"></a><a name="p695537131415"></a>请求Body中user_id所对应IAM用户的token（无需特殊权限）。</p>
</td>
</tr>
</tbody>
</table>

**表 2**  请求Body参数

<a name="table16818554124518"></a>
<table><thead align="left"><tr id="row8875145414515"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p1387575434519"><a name="p1387575434519"></a><a name="p1387575434519"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="p19875155484513"><a name="p19875155484513"></a><a name="p19875155484513"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1687595434512"><a name="p1687595434512"></a><a name="p1687595434512"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.4"><p id="p16875105419458"><a name="p16875105419458"></a><a name="p16875105419458"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row88751154114511"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p10875125411457"><a name="p10875125411457"></a><a name="p10875125411457"></a><a href="#table12820145444514">virtual_mfa_device</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p13875454204510"><a name="p13875454204510"></a><a name="p13875454204510"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p3875105417452"><a name="p3875105417452"></a><a name="p3875105417452"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p4875054204517"><a name="p4875054204517"></a><a name="p4875054204517"></a>创建的MFA设备信息。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  virtual\_mfa\_device

<a name="table12820145444514"></a>
<table><thead align="left"><tr id="row18751454184511"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p1875954174511"><a name="p1875954174511"></a><a name="p1875954174511"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="p16875125415456"><a name="p16875125415456"></a><a name="p16875125415456"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p1887665415459"><a name="p1887665415459"></a><a name="p1887665415459"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="40%" id="mcps1.2.5.1.4"><p id="p15876205417452"><a name="p15876205417452"></a><a name="p15876205417452"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row78762548452"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p20876154184515"><a name="p20876154184515"></a><a name="p20876154184515"></a>name</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p178762543450"><a name="p178762543450"></a><a name="p178762543450"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p1287675494512"><a name="p1287675494512"></a><a name="p1287675494512"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p8876195414459"><a name="p8876195414459"></a><a name="p8876195414459"></a>设备名称。</p>
<p id="p11876135484516"><a name="p11876135484516"></a><a name="p11876135484516"></a>最小长度：1</p>
<p id="p48761554144517"><a name="p48761554144517"></a><a name="p48761554144517"></a>最大长度：64</p>
</td>
</tr>
<tr id="row14876145411453"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p987695412452"><a name="p987695412452"></a><a name="p987695412452"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="p18762542459"><a name="p18762542459"></a><a name="p18762542459"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p587610545451"><a name="p587610545451"></a><a name="p587610545451"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="40%" headers="mcps1.2.5.1.4 "><p id="p1987645424511"><a name="p1987645424511"></a><a name="p1987645424511"></a>创建MFA设备的IAM用户ID。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section18824254144511"></a>

**状态码为 201 时：**

**表 4**  响应Body参数

<a name="table178241354144519"></a>
<table><thead align="left"><tr id="row487611549453"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p58769541452"><a name="p58769541452"></a><a name="p58769541452"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p11876054184510"><a name="p11876054184510"></a><a name="p11876054184510"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p187685410455"><a name="p187685410455"></a><a name="p187685410455"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1287675410454"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1787605464519"><a name="p1787605464519"></a><a name="p1787605464519"></a><a href="#table782775454511">virtual_mfa_device</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p58761054104513"><a name="p58761054104513"></a><a name="p58761054104513"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p9876175415452"><a name="p9876175415452"></a><a name="p9876175415452"></a>创建的MFA设备。</p>
</td>
</tr>
</tbody>
</table>

**表 5**  virtual\_mfa\_device

<a name="table782775454511"></a>
<table><thead align="left"><tr id="row4876125484515"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p3876175415458"><a name="p3876175415458"></a><a name="p3876175415458"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p4876135410456"><a name="p4876135410456"></a><a name="p4876135410456"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1587615413452"><a name="p1587615413452"></a><a name="p1587615413452"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row58765549458"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p10876454124519"><a name="p10876454124519"></a><a name="p10876454124519"></a>serial_number</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1087614548452"><a name="p1087614548452"></a><a name="p1087614548452"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p138764547453"><a name="p138764547453"></a><a name="p138764547453"></a>MFA设备序列号。</p>
</td>
</tr>
<tr id="row17876145410452"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p4876754144513"><a name="p4876754144513"></a><a name="p4876754144513"></a>base32_string_seed</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p11876454144520"><a name="p11876454144520"></a><a name="p11876454144520"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1387625415457"><a name="p1387625415457"></a><a name="p1387625415457"></a>密钥信息，用于第三方生成图片验证码。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section5830205434511"></a>

```
POST https://iam.myhuaweicloud.com/v3.0/OS-MFA/virtual-mfa-devices 
 
{ 
  "virtual_mfa_device" : { 
    "name" : "{device_name}", 
    "user_id" : "09f99d8f6a001d4f1f01c00c31968..." 
  } 
}
```

## 响应示例<a name="section283265417454"></a>

**状态码：201**

请求成功。

```
{
  "virtual_mfa_device": {
    "serial_number": "iam:09f6bd6a96801de40f01c00c85691...:mfa/{device_name}",
    "base32_string_seed": "{string}"
  }
}
```

## 状态码<a name="section10832454134519"></a>

<a name="table1156113351521"></a>
<table><thead align="left"><tr id="row16077351226"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p1260719351728"><a name="p1260719351728"></a><a name="p1260719351728"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p76071235922"><a name="p76071235922"></a><a name="p76071235922"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row176078352216"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p260793515220"><a name="p260793515220"></a><a name="p260793515220"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p56071535121"><a name="p56071535121"></a><a name="p56071535121"></a>请求成功。</p>
</td>
</tr>
<tr id="row196076351427"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1560719355219"><a name="p1560719355219"></a><a name="p1560719355219"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p19607143515214"><a name="p19607143515214"></a><a name="p19607143515214"></a>请求校验异常。</p>
</td>
</tr>
<tr id="row198481131111810"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1284817313180"><a name="p1284817313180"></a><a name="p1284817313180"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p1406133810185"><a name="p1406133810185"></a><a name="p1406133810185"></a>认证失败。</p>
</td>
</tr>
<tr id="row176073357217"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p13607193520215"><a name="p13607193520215"></a><a name="p13607193520215"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p116075351625"><a name="p116075351625"></a><a name="p116075351625"></a>请求未授权。</p>
</td>
</tr>
<tr id="row160712352215"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1760712351628"><a name="p1760712351628"></a><a name="p1760712351628"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p36078353214"><a name="p36078353214"></a><a name="p36078353214"></a>系统错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section9833185434510"></a>

请参见[错误码](错误码.md)。

