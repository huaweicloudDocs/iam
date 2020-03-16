# 查询IAM用户是否在用户组中<a name="iam_09_0006"></a>

## 功能介绍<a name="zh-cn_topic_0221482432_section9344174810413"></a>

该接口可以用于[管理员](https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html)查询IAM用户是否在用户组中。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="zh-cn_topic_0221482432_section4349124824119"></a>

HEAD /v3/groups/\{group\_id\}/users/\{user\_id\}

**表 1**  路径参数

<a name="zh-cn_topic_0221482432_table2035324874111"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482432_row173528481411"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482432_p1835444810413"><a name="zh-cn_topic_0221482432_p1835444810413"></a><a name="zh-cn_topic_0221482432_p1835444810413"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482432_p133565487414"><a name="zh-cn_topic_0221482432_p133565487414"></a><a name="zh-cn_topic_0221482432_p133565487414"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482432_p14357124816411"><a name="zh-cn_topic_0221482432_p14357124816411"></a><a name="zh-cn_topic_0221482432_p14357124816411"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482432_p335824813410"><a name="zh-cn_topic_0221482432_p335824813410"></a><a name="zh-cn_topic_0221482432_p335824813410"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482432_row835214818415"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482432_p635914485418"><a name="zh-cn_topic_0221482432_p635914485418"></a><a name="zh-cn_topic_0221482432_p635914485418"></a>group_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482432_p1360648164112"><a name="zh-cn_topic_0221482432_p1360648164112"></a><a name="zh-cn_topic_0221482432_p1360648164112"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482432_p143611848204113"><a name="zh-cn_topic_0221482432_p143611848204113"></a><a name="zh-cn_topic_0221482432_p143611848204113"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482432_p163632048134119"><a name="zh-cn_topic_0221482432_p163632048134119"></a><a name="zh-cn_topic_0221482432_p163632048134119"></a>用户组ID，获取方式请参见：<a href="获取账号-IAM用户-项目-用户组-委托的名称和ID.md">获取账号、IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482432_row113524484418"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482432_p17364164834111"><a name="zh-cn_topic_0221482432_p17364164834111"></a><a name="zh-cn_topic_0221482432_p17364164834111"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482432_p1836614487419"><a name="zh-cn_topic_0221482432_p1836614487419"></a><a name="zh-cn_topic_0221482432_p1836614487419"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482432_p3367164814417"><a name="zh-cn_topic_0221482432_p3367164814417"></a><a name="zh-cn_topic_0221482432_p3367164814417"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482432_p1036874844117"><a name="zh-cn_topic_0221482432_p1036874844117"></a><a name="zh-cn_topic_0221482432_p1036874844117"></a>待查询的IAM用户ID，获取方式请参见：<a href="获取账号-IAM用户-项目-用户组-委托的名称和ID.md">获取账号、IAM用户、项目、用户组、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482432_section1369648134117"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482432_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482432_row8371134815412"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482432_p1137214844117"><a name="zh-cn_topic_0221482432_p1137214844117"></a><a name="zh-cn_topic_0221482432_p1137214844117"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482432_p4373114819416"><a name="zh-cn_topic_0221482432_p4373114819416"></a><a name="zh-cn_topic_0221482432_p4373114819416"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482432_p1937410485416"><a name="zh-cn_topic_0221482432_p1937410485416"></a><a name="zh-cn_topic_0221482432_p1937410485416"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482432_p2037524810415"><a name="zh-cn_topic_0221482432_p2037524810415"></a><a name="zh-cn_topic_0221482432_p2037524810415"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482432_row16371948184110"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482432_p4376194816411"><a name="zh-cn_topic_0221482432_p4376194816411"></a><a name="zh-cn_topic_0221482432_p4376194816411"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482432_p1378134824112"><a name="zh-cn_topic_0221482432_p1378134824112"></a><a name="zh-cn_topic_0221482432_p1378134824112"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482432_p16379184813417"><a name="zh-cn_topic_0221482432_p16379184813417"></a><a name="zh-cn_topic_0221482432_p16379184813417"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482432_p038034816416"><a name="zh-cn_topic_0221482432_p038034816416"></a><a name="zh-cn_topic_0221482432_p038034816416"></a>该字段内容填为“application/json;charset=utf8”</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482432_row183718489417"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482432_p6381154810411"><a name="zh-cn_topic_0221482432_p6381154810411"></a><a name="zh-cn_topic_0221482432_p6381154810411"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482432_p1538204894117"><a name="zh-cn_topic_0221482432_p1538204894117"></a><a name="zh-cn_topic_0221482432_p1538204894117"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482432_p438304854110"><a name="zh-cn_topic_0221482432_p438304854110"></a><a name="zh-cn_topic_0221482432_p438304854110"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482432_p10384134815414"><a name="zh-cn_topic_0221482432_p10384134815414"></a><a name="zh-cn_topic_0221482432_p10384134815414"></a>拥有Security Administrator权限的token。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482432_section63851748144111"></a>

无

## 请求示例<a name="zh-cn_topic_0221482432_section2038710482416"></a>

```
HEAD https://iam.myhuaweicloud.com/v3/groups/{group_id}/users/{user_id}
```

## 响应示例<a name="zh-cn_topic_0221482432_section164011248134117"></a>

无

## 返回值<a name="zh-cn_topic_0221482432_section194033488417"></a>

<a name="zh-cn_topic_0221482432_table2467"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482432_row10405204874115"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482432_p140684819413"><a name="zh-cn_topic_0221482432_p140684819413"></a><a name="zh-cn_topic_0221482432_p140684819413"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482432_p11407174874113"><a name="zh-cn_topic_0221482432_p11407174874113"></a><a name="zh-cn_topic_0221482432_p11407174874113"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482432_row174056481415"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482432_p940874814417"><a name="zh-cn_topic_0221482432_p940874814417"></a><a name="zh-cn_topic_0221482432_p940874814417"></a>204</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482432_p11410194819412"><a name="zh-cn_topic_0221482432_p11410194819412"></a><a name="zh-cn_topic_0221482432_p11410194819412"></a>查询成功。（该IAM用户在此用户组中）</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482432_row1840554814413"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482432_p941117488417"><a name="zh-cn_topic_0221482432_p941117488417"></a><a name="zh-cn_topic_0221482432_p941117488417"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482432_p20412748154117"><a name="zh-cn_topic_0221482432_p20412748154117"></a><a name="zh-cn_topic_0221482432_p20412748154117"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482432_row124052048194117"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482432_p5413248154117"><a name="zh-cn_topic_0221482432_p5413248154117"></a><a name="zh-cn_topic_0221482432_p5413248154117"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482432_p1441424813419"><a name="zh-cn_topic_0221482432_p1441424813419"></a><a name="zh-cn_topic_0221482432_p1441424813419"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482432_row5405144818416"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482432_p184151548174112"><a name="zh-cn_topic_0221482432_p184151548174112"></a><a name="zh-cn_topic_0221482432_p184151548174112"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482432_p1441611483414"><a name="zh-cn_topic_0221482432_p1441611483414"></a><a name="zh-cn_topic_0221482432_p1441611483414"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482432_row14405184884116"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482432_p12417134894119"><a name="zh-cn_topic_0221482432_p12417134894119"></a><a name="zh-cn_topic_0221482432_p12417134894119"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482432_p18418134884116"><a name="zh-cn_topic_0221482432_p18418134884116"></a><a name="zh-cn_topic_0221482432_p18418134884116"></a>未找到相应的资源。（该IAM用户不在此用户组中）</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482432_section64191848164114"></a>

无

