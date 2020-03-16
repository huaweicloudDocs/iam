# 添加IAM用户到用户组<a name="iam_09_0007"></a>

## 功能介绍<a name="zh-cn_topic_0221482401_section1466001413514"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)添加IAM用户到用户组。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="zh-cn_topic_0221482401_section966141493512"></a>

PUT /v3/groups/\{group\_id\}/users/\{user\_id\}

**表 1**  路径参数

<a name="zh-cn_topic_0221482401_table2664714123519"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482401_row866311493520"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482401_p1566481483516"><a name="zh-cn_topic_0221482401_p1566481483516"></a><a name="zh-cn_topic_0221482401_p1566481483516"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482401_p866501463511"><a name="zh-cn_topic_0221482401_p866501463511"></a><a name="zh-cn_topic_0221482401_p866501463511"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482401_p0665614173510"><a name="zh-cn_topic_0221482401_p0665614173510"></a><a name="zh-cn_topic_0221482401_p0665614173510"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482401_p2666201419351"><a name="zh-cn_topic_0221482401_p2666201419351"></a><a name="zh-cn_topic_0221482401_p2666201419351"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482401_row966319141352"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482401_p16667414133510"><a name="zh-cn_topic_0221482401_p16667414133510"></a><a name="zh-cn_topic_0221482401_p16667414133510"></a>group_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482401_p566714143358"><a name="zh-cn_topic_0221482401_p566714143358"></a><a name="zh-cn_topic_0221482401_p566714143358"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482401_p1266851433513"><a name="zh-cn_topic_0221482401_p1266851433513"></a><a name="zh-cn_topic_0221482401_p1266851433513"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482401_p3668514143511"><a name="zh-cn_topic_0221482401_p3668514143511"></a><a name="zh-cn_topic_0221482401_p3668514143511"></a>用户组ID，获取方式请参见：<a href="获取账号-IAM用户-项目-用户组-委托的名称和ID.md">获取账号、IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482401_row266317140355"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482401_p1166816142355"><a name="zh-cn_topic_0221482401_p1166816142355"></a><a name="zh-cn_topic_0221482401_p1166816142355"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482401_p96699143357"><a name="zh-cn_topic_0221482401_p96699143357"></a><a name="zh-cn_topic_0221482401_p96699143357"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482401_p0669414153510"><a name="zh-cn_topic_0221482401_p0669414153510"></a><a name="zh-cn_topic_0221482401_p0669414153510"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482401_p167081473513"><a name="zh-cn_topic_0221482401_p167081473513"></a><a name="zh-cn_topic_0221482401_p167081473513"></a>待添加的IAM用户ID，获取方式请参见：<a href="获取账号-IAM用户-项目-用户组-委托的名称和ID.md">获取账号、IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482401_section17670181413352"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482401_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482401_row106718143358"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482401_p8672914133514"><a name="zh-cn_topic_0221482401_p8672914133514"></a><a name="zh-cn_topic_0221482401_p8672914133514"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482401_p3672914173516"><a name="zh-cn_topic_0221482401_p3672914173516"></a><a name="zh-cn_topic_0221482401_p3672914173516"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482401_p567241414356"><a name="zh-cn_topic_0221482401_p567241414356"></a><a name="zh-cn_topic_0221482401_p567241414356"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482401_p1767361419354"><a name="zh-cn_topic_0221482401_p1767361419354"></a><a name="zh-cn_topic_0221482401_p1767361419354"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482401_row6671014173514"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482401_p6673171418353"><a name="zh-cn_topic_0221482401_p6673171418353"></a><a name="zh-cn_topic_0221482401_p6673171418353"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482401_p4674131423516"><a name="zh-cn_topic_0221482401_p4674131423516"></a><a name="zh-cn_topic_0221482401_p4674131423516"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482401_p1667461413513"><a name="zh-cn_topic_0221482401_p1667461413513"></a><a name="zh-cn_topic_0221482401_p1667461413513"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482401_p1767420148359"><a name="zh-cn_topic_0221482401_p1767420148359"></a><a name="zh-cn_topic_0221482401_p1767420148359"></a>该字段内容填为“application/json;charset=utf8”</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482401_row967117146351"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482401_p767581410358"><a name="zh-cn_topic_0221482401_p767581410358"></a><a name="zh-cn_topic_0221482401_p767581410358"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482401_p186756141354"><a name="zh-cn_topic_0221482401_p186756141354"></a><a name="zh-cn_topic_0221482401_p186756141354"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482401_p1767531410353"><a name="zh-cn_topic_0221482401_p1767531410353"></a><a name="zh-cn_topic_0221482401_p1767531410353"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482401_p867611463516"><a name="zh-cn_topic_0221482401_p867611463516"></a><a name="zh-cn_topic_0221482401_p867611463516"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482401_section1467691413517"></a>

无

## 请求示例<a name="zh-cn_topic_0221482401_section14677214203519"></a>

```
PUT https://iam.myhuaweicloud.com/v3/groups/{group_id}/users/{user_id}
```

## 响应示例<a name="zh-cn_topic_0221482401_section467911147354"></a>

无

## 返回值<a name="zh-cn_topic_0221482401_section36801714183511"></a>

<a name="zh-cn_topic_0221482401_table2465"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482401_row1968191483516"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482401_p186821614113513"><a name="zh-cn_topic_0221482401_p186821614113513"></a><a name="zh-cn_topic_0221482401_p186821614113513"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482401_p5682141411351"><a name="zh-cn_topic_0221482401_p5682141411351"></a><a name="zh-cn_topic_0221482401_p5682141411351"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482401_row368171412355"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482401_p568217145359"><a name="zh-cn_topic_0221482401_p568217145359"></a><a name="zh-cn_topic_0221482401_p568217145359"></a>204</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482401_p1868313144352"><a name="zh-cn_topic_0221482401_p1868313144352"></a><a name="zh-cn_topic_0221482401_p1868313144352"></a>添加成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482401_row2681014153519"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482401_p11683171411358"><a name="zh-cn_topic_0221482401_p11683171411358"></a><a name="zh-cn_topic_0221482401_p11683171411358"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482401_p176831714123520"><a name="zh-cn_topic_0221482401_p176831714123520"></a><a name="zh-cn_topic_0221482401_p176831714123520"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482401_row268116144357"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482401_p186841114173516"><a name="zh-cn_topic_0221482401_p186841114173516"></a><a name="zh-cn_topic_0221482401_p186841114173516"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482401_p12684191423512"><a name="zh-cn_topic_0221482401_p12684191423512"></a><a name="zh-cn_topic_0221482401_p12684191423512"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482401_row1681101417353"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482401_p468571483510"><a name="zh-cn_topic_0221482401_p468571483510"></a><a name="zh-cn_topic_0221482401_p468571483510"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482401_p1168591413514"><a name="zh-cn_topic_0221482401_p1168591413514"></a><a name="zh-cn_topic_0221482401_p1168591413514"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482401_row11681414143511"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482401_p56851714203519"><a name="zh-cn_topic_0221482401_p56851714203519"></a><a name="zh-cn_topic_0221482401_p56851714203519"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482401_p13686101403510"><a name="zh-cn_topic_0221482401_p13686101403510"></a><a name="zh-cn_topic_0221482401_p13686101403510"></a>未找到相应的资源。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482401_section168691418358"></a>

无

