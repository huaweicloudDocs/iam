# 修改IAM用户信息（推荐）<a name="iam_08_0010"></a>

## 功能介绍<a name="zh-cn_topic_0221482381_section13972161463512"></a>

该接口可以用于IAM用户修改自己的用户信息。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section11300143214019"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=UpdateUserInformation)中调试该接口。

## URI<a name="zh-cn_topic_0221482381_section89741148351"></a>

PUT /v3.0/OS-USER/users/\{user\_id\}/info

**表 1**  路径参数

<a name="zh-cn_topic_0221482381_table797611493519"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482381_row10975714103519"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482381_p1597661415359"><a name="zh-cn_topic_0221482381_p1597661415359"></a><a name="zh-cn_topic_0221482381_p1597661415359"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482381_p697721453516"><a name="zh-cn_topic_0221482381_p697721453516"></a><a name="zh-cn_topic_0221482381_p697721453516"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482381_p17977214133510"><a name="zh-cn_topic_0221482381_p17977214133510"></a><a name="zh-cn_topic_0221482381_p17977214133510"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482381_p16978151433513"><a name="zh-cn_topic_0221482381_p16978151433513"></a><a name="zh-cn_topic_0221482381_p16978151433513"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482381_row15975111453517"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482381_p49785140357"><a name="zh-cn_topic_0221482381_p49785140357"></a><a name="zh-cn_topic_0221482381_p49785140357"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482381_p20979414183520"><a name="zh-cn_topic_0221482381_p20979414183520"></a><a name="zh-cn_topic_0221482381_p20979414183520"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482381_p297931493520"><a name="zh-cn_topic_0221482381_p297931493520"></a><a name="zh-cn_topic_0221482381_p297931493520"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482381_p197917146354"><a name="zh-cn_topic_0221482381_p197917146354"></a><a name="zh-cn_topic_0221482381_p197917146354"></a>待修改信息的IAM用户ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482381_section18980141419351"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482381_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482381_row109814147359"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482381_p19982121419355"><a name="zh-cn_topic_0221482381_p19982121419355"></a><a name="zh-cn_topic_0221482381_p19982121419355"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482381_p6982191416355"><a name="zh-cn_topic_0221482381_p6982191416355"></a><a name="zh-cn_topic_0221482381_p6982191416355"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482381_p7982814113517"><a name="zh-cn_topic_0221482381_p7982814113517"></a><a name="zh-cn_topic_0221482381_p7982814113517"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482381_p1983151443517"><a name="zh-cn_topic_0221482381_p1983151443517"></a><a name="zh-cn_topic_0221482381_p1983151443517"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482381_row69811714123520"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482381_p19983114183518"><a name="zh-cn_topic_0221482381_p19983114183518"></a><a name="zh-cn_topic_0221482381_p19983114183518"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482381_p169831814153519"><a name="zh-cn_topic_0221482381_p169831814153519"></a><a name="zh-cn_topic_0221482381_p169831814153519"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482381_p1498461463516"><a name="zh-cn_topic_0221482381_p1498461463516"></a><a name="zh-cn_topic_0221482381_p1498461463516"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482381_p1298413149357"><a name="zh-cn_topic_0221482381_p1298413149357"></a><a name="zh-cn_topic_0221482381_p1298413149357"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482381_row1198110148352"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482381_p69854146355"><a name="zh-cn_topic_0221482381_p69854146355"></a><a name="zh-cn_topic_0221482381_p69854146355"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482381_p1098511149357"><a name="zh-cn_topic_0221482381_p1098511149357"></a><a name="zh-cn_topic_0221482381_p1098511149357"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482381_p79856143352"><a name="zh-cn_topic_0221482381_p79856143352"></a><a name="zh-cn_topic_0221482381_p79856143352"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482381_p16986714163511"><a name="zh-cn_topic_0221482381_p16986714163511"></a><a name="zh-cn_topic_0221482381_p16986714163511"></a>URL中user_id所对应IAM用户的token（无需特殊权限）。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="zh-cn_topic_0221482381_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482381_row7986111414356"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482381_p1598710143357"><a name="zh-cn_topic_0221482381_p1598710143357"></a><a name="zh-cn_topic_0221482381_p1598710143357"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482381_p14987121463513"><a name="zh-cn_topic_0221482381_p14987121463513"></a><a name="zh-cn_topic_0221482381_p14987121463513"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482381_p13988014153516"><a name="zh-cn_topic_0221482381_p13988014153516"></a><a name="zh-cn_topic_0221482381_p13988014153516"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482381_p198891453515"><a name="zh-cn_topic_0221482381_p198891453515"></a><a name="zh-cn_topic_0221482381_p198891453515"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482381_row1986151483519"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482381_p8989181411358"><a name="zh-cn_topic_0221482381_p8989181411358"></a><a name="zh-cn_topic_0221482381_p8989181411358"></a><a href="#zh-cn_topic_0221482381_request_Rq89User">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482381_p8989614173515"><a name="zh-cn_topic_0221482381_p8989614173515"></a><a name="zh-cn_topic_0221482381_p8989614173515"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482381_p1899311483517"><a name="zh-cn_topic_0221482381_p1899311483517"></a><a name="zh-cn_topic_0221482381_p1899311483517"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482381_p1499381414356"><a name="zh-cn_topic_0221482381_p1499381414356"></a><a name="zh-cn_topic_0221482381_p1499381414356"></a>IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  user

<a name="zh-cn_topic_0221482381_request_Rq89User"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482381_row129941214193515"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482381_p899591493510"><a name="zh-cn_topic_0221482381_p899591493510"></a><a name="zh-cn_topic_0221482381_p899591493510"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482381_p99959145358"><a name="zh-cn_topic_0221482381_p99959145358"></a><a name="zh-cn_topic_0221482381_p99959145358"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482381_p99961714123517"><a name="zh-cn_topic_0221482381_p99961714123517"></a><a name="zh-cn_topic_0221482381_p99961714123517"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482381_p3996101473519"><a name="zh-cn_topic_0221482381_p3996101473519"></a><a name="zh-cn_topic_0221482381_p3996101473519"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482381_row119941114153513"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482381_p10997111414358"><a name="zh-cn_topic_0221482381_p10997111414358"></a><a name="zh-cn_topic_0221482381_p10997111414358"></a>email</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482381_p169972148350"><a name="zh-cn_topic_0221482381_p169972148350"></a><a name="zh-cn_topic_0221482381_p169972148350"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482381_p11997014113515"><a name="zh-cn_topic_0221482381_p11997014113515"></a><a name="zh-cn_topic_0221482381_p11997014113515"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482381_p29987144353"><a name="zh-cn_topic_0221482381_p29987144353"></a><a name="zh-cn_topic_0221482381_p29987144353"></a>IAM用户的新邮箱，符合邮箱格式，长度小于等于255位。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482381_row6994214193519"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482381_p699816148353"><a name="zh-cn_topic_0221482381_p699816148353"></a><a name="zh-cn_topic_0221482381_p699816148353"></a>mobile</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482381_p10998131493512"><a name="zh-cn_topic_0221482381_p10998131493512"></a><a name="zh-cn_topic_0221482381_p10998131493512"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482381_p899961414354"><a name="zh-cn_topic_0221482381_p899961414354"></a><a name="zh-cn_topic_0221482381_p899961414354"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482381_p199921413515"><a name="zh-cn_topic_0221482381_p199921413515"></a><a name="zh-cn_topic_0221482381_p199921413515"></a>IAM用户的国家码+新手机号，手机号为纯数字，长度小于等于32位。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482381_section179991914153514"></a>

无

## 请求示例<a name="zh-cn_topic_0221482381_section701015103517"></a>

```
PUT https://iam.myhuaweicloud.com/v3.0/OS-USER/users/{user_id}/info
```

```
{
    "user": {
        "email": "IAMEmail@huawei.com",
        "mobile": "0086-12345678910"
    }
}
```

## 响应示例<a name="zh-cn_topic_0221482381_section202101512353"></a>

无

## 返回值<a name="zh-cn_topic_0221482381_section93191523511"></a>

<a name="zh-cn_topic_0221482381_table2458"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482381_row2052015183513"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482381_p176111553515"><a name="zh-cn_topic_0221482381_p176111553515"></a><a name="zh-cn_topic_0221482381_p176111553515"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482381_p1571515163515"><a name="zh-cn_topic_0221482381_p1571515163515"></a><a name="zh-cn_topic_0221482381_p1571515163515"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482381_row2531512359"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482381_p510131573519"><a name="zh-cn_topic_0221482381_p510131573519"></a><a name="zh-cn_topic_0221482381_p510131573519"></a>204</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482381_p1610111515352"><a name="zh-cn_topic_0221482381_p1610111515352"></a><a name="zh-cn_topic_0221482381_p1610111515352"></a>修改成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482381_row951415133518"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482381_p4101715143514"><a name="zh-cn_topic_0221482381_p4101715143514"></a><a name="zh-cn_topic_0221482381_p4101715143514"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482381_p0111715193513"><a name="zh-cn_topic_0221482381_p0111715193513"></a><a name="zh-cn_topic_0221482381_p0111715193513"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482381_row18516153352"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482381_p01120158351"><a name="zh-cn_topic_0221482381_p01120158351"></a><a name="zh-cn_topic_0221482381_p01120158351"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482381_p811151533513"><a name="zh-cn_topic_0221482381_p811151533513"></a><a name="zh-cn_topic_0221482381_p811151533513"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482381_row145161513351"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482381_p201211158359"><a name="zh-cn_topic_0221482381_p201211158359"></a><a name="zh-cn_topic_0221482381_p201211158359"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482381_p21291519354"><a name="zh-cn_topic_0221482381_p21291519354"></a><a name="zh-cn_topic_0221482381_p21291519354"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482381_row35515133516"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482381_p141313156357"><a name="zh-cn_topic_0221482381_p141313156357"></a><a name="zh-cn_topic_0221482381_p141313156357"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482381_p12131915153519"><a name="zh-cn_topic_0221482381_p12131915153519"></a><a name="zh-cn_topic_0221482381_p12131915153519"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482381_row1553156353"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482381_p201491518351"><a name="zh-cn_topic_0221482381_p201491518351"></a><a name="zh-cn_topic_0221482381_p201491518351"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482381_p10143159357"><a name="zh-cn_topic_0221482381_p10143159357"></a><a name="zh-cn_topic_0221482381_p10143159357"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482381_row25171515350"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482381_p815161518354"><a name="zh-cn_topic_0221482381_p815161518354"></a><a name="zh-cn_topic_0221482381_p815161518354"></a>409</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482381_p12155156357"><a name="zh-cn_topic_0221482381_p12155156357"></a><a name="zh-cn_topic_0221482381_p12155156357"></a>资源冲突。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482381_row195815133511"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482381_p1716101512354"><a name="zh-cn_topic_0221482381_p1716101512354"></a><a name="zh-cn_topic_0221482381_p1716101512354"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482381_p12161715153510"><a name="zh-cn_topic_0221482381_p12161715153510"></a><a name="zh-cn_topic_0221482381_p12161715153510"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482381_row125101553519"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482381_p717131518358"><a name="zh-cn_topic_0221482381_p717131518358"></a><a name="zh-cn_topic_0221482381_p717131518358"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482381_p201831553515"><a name="zh-cn_topic_0221482381_p201831553515"></a><a name="zh-cn_topic_0221482381_p201831553515"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482381_row35201593520"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482381_p318101511355"><a name="zh-cn_topic_0221482381_p318101511355"></a><a name="zh-cn_topic_0221482381_p318101511355"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482381_p151921510356"><a name="zh-cn_topic_0221482381_p151921510356"></a><a name="zh-cn_topic_0221482381_p151921510356"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482381_section21911517356"></a>

请参考[错误码](错误码.md)。

