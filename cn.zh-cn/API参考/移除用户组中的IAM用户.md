# 移除用户组中的IAM用户<a name="iam_09_0008"></a>

## 功能介绍<a name="zh-cn_topic_0221482365_section13176175054113"></a>

该接口可以用于<u>[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)</u><u></u>移除用户组中的IAM用户。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section19686164211"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneRemoveUserFromGroup)中调试该接口。

## URI<a name="zh-cn_topic_0221482365_section181829507417"></a>

DELETE /v3/groups/\{group\_id\}/users/\{user\_id\}

**表 1**  路径参数

<a name="zh-cn_topic_0221482365_table3185125020412"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482365_row018535054113"><th class="cellrowborder" valign="top" width="9.59%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482365_p8186165010417"><a name="zh-cn_topic_0221482365_p8186165010417"></a><a name="zh-cn_topic_0221482365_p8186165010417"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20.41%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482365_p61881350124110"><a name="zh-cn_topic_0221482365_p61881350124110"></a><a name="zh-cn_topic_0221482365_p61881350124110"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482365_p16189105074118"><a name="zh-cn_topic_0221482365_p16189105074118"></a><a name="zh-cn_topic_0221482365_p16189105074118"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482365_p619012500419"><a name="zh-cn_topic_0221482365_p619012500419"></a><a name="zh-cn_topic_0221482365_p619012500419"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482365_row11185750164114"><td class="cellrowborder" valign="top" width="9.59%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482365_p18192165012414"><a name="zh-cn_topic_0221482365_p18192165012414"></a><a name="zh-cn_topic_0221482365_p18192165012414"></a>group_id</p>
</td>
<td class="cellrowborder" valign="top" width="20.41%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482365_p141931350114115"><a name="zh-cn_topic_0221482365_p141931350114115"></a><a name="zh-cn_topic_0221482365_p141931350114115"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482365_p9195950134117"><a name="zh-cn_topic_0221482365_p9195950134117"></a><a name="zh-cn_topic_0221482365_p9195950134117"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482365_p61961508412"><a name="zh-cn_topic_0221482365_p61961508412"></a><a name="zh-cn_topic_0221482365_p61961508412"></a>用户组ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482365_row31857501417"><td class="cellrowborder" valign="top" width="9.59%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482365_p6198135017410"><a name="zh-cn_topic_0221482365_p6198135017410"></a><a name="zh-cn_topic_0221482365_p6198135017410"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="20.41%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482365_p519975044119"><a name="zh-cn_topic_0221482365_p519975044119"></a><a name="zh-cn_topic_0221482365_p519975044119"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482365_p2020110501415"><a name="zh-cn_topic_0221482365_p2020110501415"></a><a name="zh-cn_topic_0221482365_p2020110501415"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482365_p1203135015418"><a name="zh-cn_topic_0221482365_p1203135015418"></a><a name="zh-cn_topic_0221482365_p1203135015418"></a>待从用户组中移除的IAM用户ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482365_section320512500415"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482365_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482365_row7209115018419"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482365_p82111850144116"><a name="zh-cn_topic_0221482365_p82111850144116"></a><a name="zh-cn_topic_0221482365_p82111850144116"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482365_p14213155024114"><a name="zh-cn_topic_0221482365_p14213155024114"></a><a name="zh-cn_topic_0221482365_p14213155024114"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482365_p52147509410"><a name="zh-cn_topic_0221482365_p52147509410"></a><a name="zh-cn_topic_0221482365_p52147509410"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482365_p121515014114"><a name="zh-cn_topic_0221482365_p121515014114"></a><a name="zh-cn_topic_0221482365_p121515014114"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482365_row22097503418"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482365_p821714502419"><a name="zh-cn_topic_0221482365_p821714502419"></a><a name="zh-cn_topic_0221482365_p821714502419"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482365_p72182503412"><a name="zh-cn_topic_0221482365_p72182503412"></a><a name="zh-cn_topic_0221482365_p72182503412"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482365_p142227502411"><a name="zh-cn_topic_0221482365_p142227502411"></a><a name="zh-cn_topic_0221482365_p142227502411"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482365_p0224115015419"><a name="zh-cn_topic_0221482365_p0224115015419"></a><a name="zh-cn_topic_0221482365_p0224115015419"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482365_row120925004117"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482365_p4226050194113"><a name="zh-cn_topic_0221482365_p4226050194113"></a><a name="zh-cn_topic_0221482365_p4226050194113"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482365_p0228115019412"><a name="zh-cn_topic_0221482365_p0228115019412"></a><a name="zh-cn_topic_0221482365_p0228115019412"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482365_p1523017502413"><a name="zh-cn_topic_0221482365_p1523017502413"></a><a name="zh-cn_topic_0221482365_p1523017502413"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="p169317457455"><a name="p169317457455"></a><a name="p169317457455"></a>访问令牌，承载用户的身份、权限等信息。</p>
<p id="p1893164544511"><a name="p1893164544511"></a><a name="p1893164544511"></a>token所需权限请参见<a href="授权项.md">授权项</a>。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482365_section9235550154117"></a>

无

## 请求示例<a name="zh-cn_topic_0221482365_section6277195064114"></a>

```
DELETE https://iam.myhuaweicloud.com/v3/groups/{group_id}/users/{user_id}
```

## 响应示例<a name="zh-cn_topic_0221482365_section1628915014419"></a>

无

## 返回值<a name="zh-cn_topic_0221482365_section1330616509413"></a>

<a name="zh-cn_topic_0221482365_table2466"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482365_row1730835013418"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482365_p133101350144111"><a name="zh-cn_topic_0221482365_p133101350144111"></a><a name="zh-cn_topic_0221482365_p133101350144111"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482365_p9311145019419"><a name="zh-cn_topic_0221482365_p9311145019419"></a><a name="zh-cn_topic_0221482365_p9311145019419"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482365_row123088506416"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482365_p1131225014419"><a name="zh-cn_topic_0221482365_p1131225014419"></a><a name="zh-cn_topic_0221482365_p1131225014419"></a>204</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482365_p173178500410"><a name="zh-cn_topic_0221482365_p173178500410"></a><a name="zh-cn_topic_0221482365_p173178500410"></a>移除成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482365_row153081550174111"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482365_p1318750134119"><a name="zh-cn_topic_0221482365_p1318750134119"></a><a name="zh-cn_topic_0221482365_p1318750134119"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482365_p1831912500411"><a name="zh-cn_topic_0221482365_p1831912500411"></a><a name="zh-cn_topic_0221482365_p1831912500411"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482365_row1308195094118"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482365_p932012504415"><a name="zh-cn_topic_0221482365_p932012504415"></a><a name="zh-cn_topic_0221482365_p932012504415"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482365_p10321115011412"><a name="zh-cn_topic_0221482365_p10321115011412"></a><a name="zh-cn_topic_0221482365_p10321115011412"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482365_row1130855024119"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482365_p16322175013419"><a name="zh-cn_topic_0221482365_p16322175013419"></a><a name="zh-cn_topic_0221482365_p16322175013419"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482365_p163247507414"><a name="zh-cn_topic_0221482365_p163247507414"></a><a name="zh-cn_topic_0221482365_p163247507414"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482365_row6308850134117"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482365_p232535034119"><a name="zh-cn_topic_0221482365_p232535034119"></a><a name="zh-cn_topic_0221482365_p232535034119"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482365_p17326155014118"><a name="zh-cn_topic_0221482365_p17326155014118"></a><a name="zh-cn_topic_0221482365_p17326155014118"></a>未找到相应的资源。（该IAM用户不在此用户组中）</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482365_section143271250154118"></a>

无

