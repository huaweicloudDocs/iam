# 管理员删除IAM用户<a name="iam_08_0009"></a>

## 功能介绍<a name="zh-cn_topic_0221482480_section134281915113213"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)删除指定IAM用户。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section1345811561200"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneDeleteUser)中调试该接口。

## URI<a name="zh-cn_topic_0221482480_section164303153323"></a>

DELETE /v3/users/\{user\_id\}

**表 1**  路径参数

<a name="zh-cn_topic_0221482480_table1743371511326"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482480_row2043211517322"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482480_p84341715203215"><a name="zh-cn_topic_0221482480_p84341715203215"></a><a name="zh-cn_topic_0221482480_p84341715203215"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482480_p19435615103214"><a name="zh-cn_topic_0221482480_p19435615103214"></a><a name="zh-cn_topic_0221482480_p19435615103214"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482480_p44362156324"><a name="zh-cn_topic_0221482480_p44362156324"></a><a name="zh-cn_topic_0221482480_p44362156324"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482480_p043691523212"><a name="zh-cn_topic_0221482480_p043691523212"></a><a name="zh-cn_topic_0221482480_p043691523212"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482480_row4433171553211"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482480_p0437101523210"><a name="zh-cn_topic_0221482480_p0437101523210"></a><a name="zh-cn_topic_0221482480_p0437101523210"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482480_p154381215123210"><a name="zh-cn_topic_0221482480_p154381215123210"></a><a name="zh-cn_topic_0221482480_p154381215123210"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482480_p543971510323"><a name="zh-cn_topic_0221482480_p543971510323"></a><a name="zh-cn_topic_0221482480_p543971510323"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482480_p543911518325"><a name="zh-cn_topic_0221482480_p543911518325"></a><a name="zh-cn_topic_0221482480_p543911518325"></a>待删除的IAM用户ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482480_section74401515103212"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482480_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482480_row944191513215"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482480_p13443201515323"><a name="zh-cn_topic_0221482480_p13443201515323"></a><a name="zh-cn_topic_0221482480_p13443201515323"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482480_p14443515183218"><a name="zh-cn_topic_0221482480_p14443515183218"></a><a name="zh-cn_topic_0221482480_p14443515183218"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482480_p104441159323"><a name="zh-cn_topic_0221482480_p104441159323"></a><a name="zh-cn_topic_0221482480_p104441159323"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482480_p8445151520325"><a name="zh-cn_topic_0221482480_p8445151520325"></a><a name="zh-cn_topic_0221482480_p8445151520325"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482480_row444281563210"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482480_p15446121514320"><a name="zh-cn_topic_0221482480_p15446121514320"></a><a name="zh-cn_topic_0221482480_p15446121514320"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482480_p5446111593212"><a name="zh-cn_topic_0221482480_p5446111593212"></a><a name="zh-cn_topic_0221482480_p5446111593212"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482480_p20447715193212"><a name="zh-cn_topic_0221482480_p20447715193212"></a><a name="zh-cn_topic_0221482480_p20447715193212"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482480_p1744871511328"><a name="zh-cn_topic_0221482480_p1744871511328"></a><a name="zh-cn_topic_0221482480_p1744871511328"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482480_row5442141510324"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482480_p6449171543214"><a name="zh-cn_topic_0221482480_p6449171543214"></a><a name="zh-cn_topic_0221482480_p6449171543214"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482480_p11449915173212"><a name="zh-cn_topic_0221482480_p11449915173212"></a><a name="zh-cn_topic_0221482480_p11449915173212"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482480_p6450111514322"><a name="zh-cn_topic_0221482480_p6450111514322"></a><a name="zh-cn_topic_0221482480_p6450111514322"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482480_p945151523214"><a name="zh-cn_topic_0221482480_p945151523214"></a><a name="zh-cn_topic_0221482480_p945151523214"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482480_section19451181523214"></a>

无

## 请求示例<a name="zh-cn_topic_0221482480_section445231517326"></a>

```
DELETE https://iam.myhuaweicloud.com/v3/users/{user_id}
```

## 响应示例<a name="zh-cn_topic_0221482480_section54551115163219"></a>

无

## 返回值<a name="zh-cn_topic_0221482480_section545641517327"></a>

<a name="zh-cn_topic_0221482480_table2449"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482480_row16458151523214"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482480_p204591715193213"><a name="zh-cn_topic_0221482480_p204591715193213"></a><a name="zh-cn_topic_0221482480_p204591715193213"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482480_p14601157327"><a name="zh-cn_topic_0221482480_p14601157327"></a><a name="zh-cn_topic_0221482480_p14601157327"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482480_row2458415183214"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482480_p12460151543216"><a name="zh-cn_topic_0221482480_p12460151543216"></a><a name="zh-cn_topic_0221482480_p12460151543216"></a>204</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482480_p194617155321"><a name="zh-cn_topic_0221482480_p194617155321"></a><a name="zh-cn_topic_0221482480_p194617155321"></a>删除成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482480_row1458715173214"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482480_p1246241516324"><a name="zh-cn_topic_0221482480_p1246241516324"></a><a name="zh-cn_topic_0221482480_p1246241516324"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482480_p204622159325"><a name="zh-cn_topic_0221482480_p204622159325"></a><a name="zh-cn_topic_0221482480_p204622159325"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482480_row1145831515325"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482480_p5463181523219"><a name="zh-cn_topic_0221482480_p5463181523219"></a><a name="zh-cn_topic_0221482480_p5463181523219"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482480_p64645155323"><a name="zh-cn_topic_0221482480_p64645155323"></a><a name="zh-cn_topic_0221482480_p64645155323"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482480_row4458101517320"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482480_p54656153324"><a name="zh-cn_topic_0221482480_p54656153324"></a><a name="zh-cn_topic_0221482480_p54656153324"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482480_p34664150322"><a name="zh-cn_topic_0221482480_p34664150322"></a><a name="zh-cn_topic_0221482480_p34664150322"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482480_row1145819151326"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482480_p4467191563217"><a name="zh-cn_topic_0221482480_p4467191563217"></a><a name="zh-cn_topic_0221482480_p4467191563217"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482480_p20468615123220"><a name="zh-cn_topic_0221482480_p20468615123220"></a><a name="zh-cn_topic_0221482480_p20468615123220"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482480_row1945814158324"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482480_p2468151514327"><a name="zh-cn_topic_0221482480_p2468151514327"></a><a name="zh-cn_topic_0221482480_p2468151514327"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482480_p646991543213"><a name="zh-cn_topic_0221482480_p646991543213"></a><a name="zh-cn_topic_0221482480_p646991543213"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482480_row144586156321"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482480_p13470111553216"><a name="zh-cn_topic_0221482480_p13470111553216"></a><a name="zh-cn_topic_0221482480_p13470111553216"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482480_p1447013156324"><a name="zh-cn_topic_0221482480_p1447013156324"></a><a name="zh-cn_topic_0221482480_p1447013156324"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482480_row1945821518322"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482480_p44711615193211"><a name="zh-cn_topic_0221482480_p44711615193211"></a><a name="zh-cn_topic_0221482480_p44711615193211"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482480_p2047201510321"><a name="zh-cn_topic_0221482480_p2047201510321"></a><a name="zh-cn_topic_0221482480_p2047201510321"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482480_row945818157323"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482480_p104722154323"><a name="zh-cn_topic_0221482480_p104722154323"></a><a name="zh-cn_topic_0221482480_p104722154323"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482480_p44736156323"><a name="zh-cn_topic_0221482480_p44736156323"></a><a name="zh-cn_topic_0221482480_p44736156323"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482480_section1647481563212"></a>

请参考[错误码](错误码.md)。

