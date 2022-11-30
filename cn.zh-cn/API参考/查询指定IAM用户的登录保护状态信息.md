# 查询指定IAM用户的登录保护状态信息<a name="iam_08_0016"></a>

## 功能介绍<a name="section4392175003714"></a>

该接口可以用于<u>[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)</u><u></u>查询指定IAM用户的登录保护状态信息，或IAM用户查询自己的登录保护状态信息。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section99983300597"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=ShowUserLoginProtect)中调试该接口。

## URI<a name="section12393135033711"></a>

GET /v3.0/OS-USER/users/\{user\_id\}/login-protect

**表 1**  路径参数

<a name="table3394165014373"></a>
<table><thead align="left"><tr id="row3518145023712"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p65185509375"><a name="p65185509375"></a><a name="p65185509375"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p11518175018373"><a name="p11518175018373"></a><a name="p11518175018373"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="p35194506378"><a name="p35194506378"></a><a name="p35194506378"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="p951965043714"><a name="p951965043714"></a><a name="p951965043714"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row11519250203711"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p1519050143711"><a name="p1519050143711"></a><a name="p1519050143711"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p10519165010377"><a name="p10519165010377"></a><a name="p10519165010377"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="p9519135083711"><a name="p9519135083711"></a><a name="p9519135083711"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482366_p4739184912254"><a name="zh-cn_topic_0221482366_p4739184912254"></a><a name="zh-cn_topic_0221482366_p4739184912254"></a>待查询的IAM用户ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="section24001250133716"></a>

**表 2**  请求Header参数

<a name="table14401195013373"></a>
<table><thead align="left"><tr id="row10519050143718"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="p18519650173714"><a name="p18519650173714"></a><a name="p18519650173714"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="p651917504372"><a name="p651917504372"></a><a name="p651917504372"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="19.98%" id="mcps1.2.5.1.3"><p id="p7519165010379"><a name="p7519165010379"></a><a name="p7519165010379"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50.019999999999996%" id="mcps1.2.5.1.4"><p id="p1519205093717"><a name="p1519205093717"></a><a name="p1519205093717"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row45197503377"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="p195199501373"><a name="p195199501373"></a><a name="p195199501373"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="p751965015378"><a name="p751965015378"></a><a name="p751965015378"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="19.98%" headers="mcps1.2.5.1.3 "><p id="p205191550193718"><a name="p205191550193718"></a><a name="p205191550193718"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50.019999999999996%" headers="mcps1.2.5.1.4 "><p id="p15290161835512"><a name="p15290161835512"></a><a name="p15290161835512"></a><u id="u54331933756"><a name="u54331933756"></a><a name="u54331933756"></a><a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a></u><u id="u1433533657"><a name="u1433533657"></a><a name="u1433533657"></a></u>查询IAM用户的登录保护状态信息：请参见<a href="授权项.md">授权项</a>。</p>
<p id="p175199501375"><a name="p175199501375"></a><a name="p175199501375"></a>IAM用户查询自己的登录保护状态信息：URL中user_id所对应IAM用户的token（无需特殊权限）。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="section540805043710"></a>

**状态码为 200 时:**

**表 3**  响应Body参数

<a name="table1240935063711"></a>
<table><thead align="left"><tr id="row195197506378"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p20519125073715"><a name="p20519125073715"></a><a name="p20519125073715"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p15194507376"><a name="p15194507376"></a><a name="p15194507376"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p251985093710"><a name="p251985093710"></a><a name="p251985093710"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row14519175053710"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p451945011378"><a name="p451945011378"></a><a name="p451945011378"></a><a href="#table7414450103712">login_protect</a></p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p17519145033715"><a name="p17519145033715"></a><a name="p17519145033715"></a>object</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1351935023713"><a name="p1351935023713"></a><a name="p1351935023713"></a>登录状态保护信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  login\_protect

<a name="table7414450103712"></a>
<table><thead align="left"><tr id="row19519105017376"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.1"><p id="p12519115053714"><a name="p12519115053714"></a><a name="p12519115053714"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.4.1.2"><p id="p1751945017371"><a name="p1751945017371"></a><a name="p1751945017371"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="60%" id="mcps1.2.4.1.3"><p id="p1051920505371"><a name="p1051920505371"></a><a name="p1051920505371"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row351912506373"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p451975063715"><a name="p451975063715"></a><a name="p451975063715"></a>enabled</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p19519165063712"><a name="p19519165063712"></a><a name="p19519165063712"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p35197507377"><a name="p35197507377"></a><a name="p35197507377"></a>IAM用户是否开启登录保护，开启为"true"，未开启为"false"。</p>
</td>
</tr>
<tr id="row15191500379"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p11519550153715"><a name="p11519550153715"></a><a name="p11519550153715"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p951915073714"><a name="p951915073714"></a><a name="p951915073714"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p1519165020376"><a name="p1519165020376"></a><a name="p1519165020376"></a>IAM用户ID。</p>
</td>
</tr>
<tr id="row9519195013717"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.1 "><p id="p1351912505377"><a name="p1351912505377"></a><a name="p1351912505377"></a>verification_method</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.4.1.2 "><p id="p1551945018378"><a name="p1551945018378"></a><a name="p1551945018378"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="60%" headers="mcps1.2.4.1.3 "><p id="p851915013714"><a name="p851915013714"></a><a name="p851915013714"></a>IAM用户登录验证方式。</p>
</td>
</tr>
</tbody>
</table>

## 请求示例<a name="section10420950163717"></a>

```
GET https://iam.myhuaweicloud.com/v3.0/OS-USER/users/{user_id}/login-protect
```

## 响应示例<a name="section242245003714"></a>

**状态码为 200 时:**

请求成功。

```
{ 
  "login_protect" : { 
    "user_id" : "16b26081f43d4c628c4bb88cf32e9...", 
    "enabled" : true, 
    "verification_method" : "vmfa" 
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
  "error_code" : "Iam.0004" 
}
```

>![](public_sys-resources/icon-note.gif) **说明：** 
>对于从未开启过登录保护的IAM用户，该接口无法获取到其登录保护状态信息，会返回IAM.0004错误码。

**状态码为 500 时:**

内部服务错误。

```
{ 
  "error_msg" : "An unexpected error prevented the server from fulfilling your request.", 
  "error_code" : "IAM.0006" 
}
```

## 状态码<a name="section18441450143712"></a>

<a name="table17441550113718"></a>
<table><thead align="left"><tr id="row252015509375"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="p20520165033710"><a name="p20520165033710"></a><a name="p20520165033710"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="p6520175018375"><a name="p6520175018375"></a><a name="p6520175018375"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="row1652055013712"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1052016507375"><a name="p1052016507375"></a><a name="p1052016507375"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p352095014373"><a name="p352095014373"></a><a name="p352095014373"></a>请求成功。</p>
</td>
</tr>
<tr id="row1952014506379"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p1652019501377"><a name="p1652019501377"></a><a name="p1652019501377"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p552075016378"><a name="p552075016378"></a><a name="p552075016378"></a>认证失败。</p>
</td>
</tr>
<tr id="row2052085011370"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p17520155083710"><a name="p17520155083710"></a><a name="p17520155083710"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p2520165043715"><a name="p2520165043715"></a><a name="p2520165043715"></a>没有操作权限。</p>
</td>
</tr>
<tr id="row205201850173717"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p352012503370"><a name="p352012503370"></a><a name="p352012503370"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p352018509370"><a name="p352018509370"></a><a name="p352018509370"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="row1752015013718"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="p652015012379"><a name="p652015012379"></a><a name="p652015012379"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="p152019507376"><a name="p152019507376"></a><a name="p152019507376"></a>内部服务错误。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="section74482050143716"></a>

请参见[错误码](错误码.md)。

