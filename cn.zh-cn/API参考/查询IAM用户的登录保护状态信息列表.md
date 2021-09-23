# 查询IAM用户的登录保护状态信息列表<a name="iam_08_0014"></a>

## 功能介绍<a name="section11479143317372"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)查询IAM用户的登录保护状态列表。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section20899173065913"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=ListUserLoginProtects)中调试该接口。

## URI<a name="section1547914332370"></a>

GET /v3.0/OS-USER/login-protects

## 请求参数<a name="section1747943313720"></a>

**表 1**  请求Header参数

<a name="table1480103393713"></a>
<table><thead align="left"><tr id="row153843343710"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p1753811337372"><a name="p1753811337372"></a><a name="p1753811337372"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p1353893393713"><a name="p1353893393713"></a><a name="p1353893393713"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p11538163310379"><a name="p11538163310379"></a><a name="p11538163310379"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p453810333376"><a name="p453810333376"></a><a name="p453810333376"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1753816337379"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p16538183353717"><a name="p16538183353717"></a><a name="p16538183353717"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p17538193363715"><a name="p17538193363715"></a><a name="p17538193363715"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p3538133317375"><a name="p3538133317375"></a><a name="p3538133317375"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p953853315377"><a name="p953853315377"></a><a name="p953853315377"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section2482123311375"></a>

**表 2**  响应Body参数

<a name="table1548263312379"></a>
<table><thead align="left"><tr id="row25381433153712"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p12538163310373"><a name="p12538163310373"></a><a name="p12538163310373"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p105389334371"><a name="p105389334371"></a><a name="p105389334371"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p185387338371"><a name="p185387338371"></a><a name="p185387338371"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row153893323718"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p10538193383720"><a name="p10538193383720"></a><a name="p10538193383720"></a><a href="#table12484173313717">login_protects</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="zh-cn_topic_0221482398_p1780653742313"><a name="zh-cn_topic_0221482398_p1780653742313"></a><a name="zh-cn_topic_0221482398_p1780653742313"></a>Array of objects</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1053883393718"><a name="p1053883393718"></a><a name="p1053883393718"></a>登录状态保护信息列表。</p>
<div class="note" id="note5470185314417"><a name="note5470185314417"></a><a name="note5470185314417"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p124704534413"><a name="p124704534413"></a><a name="p124704534413"></a>只返回开启过登录保护的用户状态信息。</p>
</div></div>
</td>
</tr>
</tbody>
</table>

**表 3**  login\_protects

<a name="table12484173313717"></a>
<table><thead align="left"><tr id="row175381433193717"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p6538173303720"><a name="p6538173303720"></a><a name="p6538173303720"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p10538733113715"><a name="p10538733113715"></a><a name="p10538733113715"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p12538143323716"><a name="p12538143323716"></a><a name="p12538143323716"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row153813310373"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p45381833123711"><a name="p45381833123711"></a><a name="p45381833123711"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p253813332371"><a name="p253813332371"></a><a name="p253813332371"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1653873313716"><a name="p1653873313716"></a><a name="p1653873313716"></a>IAM用户是否开启登录保护，开启为"true"，未开启为"false"。</p>
</td>
</tr>
<tr id="row1053823313720"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p14538433143720"><a name="p14538433143720"></a><a name="p14538433143720"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p18538333153720"><a name="p18538333153720"></a><a name="p18538333153720"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p175387339379"><a name="p175387339379"></a><a name="p175387339379"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="row4538103311375"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p15538163343710"><a name="p15538163343710"></a><a name="p15538163343710"></a>verification_method</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p195386339374"><a name="p195386339374"></a><a name="p195386339374"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p16538933113714"><a name="p16538933113714"></a><a name="p16538933113714"></a>IAM用户登录验证方式。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section134881533163720"></a>

```
GET https://iam.myhuaweicloud.com/v3.0/OS-USER/login-protects
```

## 响应示例<a name="section12488103313717"></a>

**状态码为 200 时:**

请求成功。

```
{ 
  "login_protects" : [
          { 
            "user_id" : "75226081f43d4c628c4bb88cf32e9...", 
            "enabled" : true, 
            "verification_method" : "email" 
            }, 
          { 
            "user_id" : "16b26081f43d4c628c4bb88cf32e9...", 
            "enabled" : true, 
            "verification_method" : "vmfa" 
            },
          { 
            "user_id" : "56b26081f43d4c628c4bb88cf32e9...", 
            "enabled" : true, 
            "verification_method" : "sms" 
            }
       ] 
}
```

>![](public_sys-resources/icon-note.gif) **说明：** 
>对于从未开启过登录保护的IAM用户，该接口无法获取到其登录保护状态信息，只返回开启过登录保护的用户状态信息。

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

## 状态码<a name="section949293313371"></a>

<a name="table349212337371"></a>
<table><thead align="left"><tr id="row175391533113720"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p19539183363710"><a name="p19539183363710"></a><a name="p19539183363710"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p653914337371"><a name="p653914337371"></a><a name="p653914337371"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row15392033133711"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p353993312372"><a name="p353993312372"></a><a name="p353993312372"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p19539193315373"><a name="p19539193315373"></a><a name="p19539193315373"></a>请求成功。</p>
</td>
</tr>
<tr id="row153915335371"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p15391733143713"><a name="p15391733143713"></a><a name="p15391733143713"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p5539113353720"><a name="p5539113353720"></a><a name="p5539113353720"></a>认证失败。</p>
</td>
</tr>
<tr id="row165391633133713"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p16539143363711"><a name="p16539143363711"></a><a name="p16539143363711"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p75391133163717"><a name="p75391133163717"></a><a name="p75391133163717"></a>没有操作权限。</p>
</td>
</tr>
<tr id="row653913316373"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p155391333173720"><a name="p155391333173720"></a><a name="p155391333173720"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p11539103313712"><a name="p11539103313712"></a><a name="p11539103313712"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="row1553973318376"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p16539143314373"><a name="p16539143314373"></a><a name="p16539143314373"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p165397331379"><a name="p165397331379"></a><a name="p165397331379"></a>内部服务错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section84941133203717"></a>

请参见[错误码](错误码.md)。

