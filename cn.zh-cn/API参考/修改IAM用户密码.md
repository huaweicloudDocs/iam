# 修改IAM用户密码<a name="iam_08_0007"></a>

## 功能介绍<a name="zh-cn_topic_0221482361_section75278217363"></a>

该接口可以用于IAM用户修改自己的密码。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## 调试<a name="section16597324201"></a>

您可以在[API Explorer](https://apiexplorer.developer.huaweicloud.com/apiexplorer/doc?product=IAM&api=KeystoneUpdateUserPassword)中调试该接口。

## URI<a name="zh-cn_topic_0221482361_section1533421163611"></a>

POST /v3/users/\{user\_id\}/password

**表 1**  路径参数

<a name="zh-cn_topic_0221482361_table11538182114367"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482361_row16536321113618"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482361_p8539122173620"><a name="zh-cn_topic_0221482361_p8539122173620"></a><a name="zh-cn_topic_0221482361_p8539122173620"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482361_p1254017218361"><a name="zh-cn_topic_0221482361_p1254017218361"></a><a name="zh-cn_topic_0221482361_p1254017218361"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482361_p1154232116368"><a name="zh-cn_topic_0221482361_p1154232116368"></a><a name="zh-cn_topic_0221482361_p1154232116368"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482361_p1454310214367"><a name="zh-cn_topic_0221482361_p1454310214367"></a><a name="zh-cn_topic_0221482361_p1454310214367"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482361_row11536142110362"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482361_p65452214366"><a name="zh-cn_topic_0221482361_p65452214366"></a><a name="zh-cn_topic_0221482361_p65452214366"></a>user_id</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482361_p19547721163619"><a name="zh-cn_topic_0221482361_p19547721163619"></a><a name="zh-cn_topic_0221482361_p19547721163619"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482361_p1754812218369"><a name="zh-cn_topic_0221482361_p1754812218369"></a><a name="zh-cn_topic_0221482361_p1754812218369"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482361_p655082173616"><a name="zh-cn_topic_0221482361_p655082173616"></a><a name="zh-cn_topic_0221482361_p655082173616"></a>待修改密码的IAM用户ID，获取方式请参见：<a href="获取帐号-IAM用户-项目-用户组-区域-委托的名称和ID.md">获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID</a>。</p>
</td>
</tr>
</tbody>
</table>

## 请求参数<a name="zh-cn_topic_0221482361_section5553102193611"></a>

**表 2**  请求Header参数

<a name="zh-cn_topic_0221482361_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482361_row6555321133611"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482361_p155571921143614"><a name="zh-cn_topic_0221482361_p155571921143614"></a><a name="zh-cn_topic_0221482361_p155571921143614"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482361_p855812216363"><a name="zh-cn_topic_0221482361_p855812216363"></a><a name="zh-cn_topic_0221482361_p855812216363"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482361_p756015214366"><a name="zh-cn_topic_0221482361_p756015214366"></a><a name="zh-cn_topic_0221482361_p756015214366"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482361_p9561521103620"><a name="zh-cn_topic_0221482361_p9561521103620"></a><a name="zh-cn_topic_0221482361_p9561521103620"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482361_row055592116361"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482361_p14563821153616"><a name="zh-cn_topic_0221482361_p14563821153616"></a><a name="zh-cn_topic_0221482361_p14563821153616"></a>Content-Type</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482361_p956520214366"><a name="zh-cn_topic_0221482361_p956520214366"></a><a name="zh-cn_topic_0221482361_p956520214366"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482361_p356672113367"><a name="zh-cn_topic_0221482361_p356672113367"></a><a name="zh-cn_topic_0221482361_p356672113367"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482361_p856812117363"><a name="zh-cn_topic_0221482361_p856812117363"></a><a name="zh-cn_topic_0221482361_p856812117363"></a>该字段内容填为“application/json;charset=utf8”。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482361_row1055542153615"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482361_p1556942117366"><a name="zh-cn_topic_0221482361_p1556942117366"></a><a name="zh-cn_topic_0221482361_p1556942117366"></a>X-Auth-Token</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482361_p757172117368"><a name="zh-cn_topic_0221482361_p757172117368"></a><a name="zh-cn_topic_0221482361_p757172117368"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482361_p157213213366"><a name="zh-cn_topic_0221482361_p157213213366"></a><a name="zh-cn_topic_0221482361_p157213213366"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482361_p55749213363"><a name="zh-cn_topic_0221482361_p55749213363"></a><a name="zh-cn_topic_0221482361_p55749213363"></a>URL中user_id所对应IAM用户的token（无需特殊权限）。</p>
</td>
</tr>
</tbody>
</table>

**表 3**  请求Body参数

<a name="zh-cn_topic_0221482361_requestParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482361_row257542193617"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482361_p1557818218365"><a name="zh-cn_topic_0221482361_p1557818218365"></a><a name="zh-cn_topic_0221482361_p1557818218365"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482361_p5579122103619"><a name="zh-cn_topic_0221482361_p5579122103619"></a><a name="zh-cn_topic_0221482361_p5579122103619"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482361_p95811421203618"><a name="zh-cn_topic_0221482361_p95811421203618"></a><a name="zh-cn_topic_0221482361_p95811421203618"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482361_p195829215365"><a name="zh-cn_topic_0221482361_p195829215365"></a><a name="zh-cn_topic_0221482361_p195829215365"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482361_row11576192119364"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482361_p10584112117365"><a name="zh-cn_topic_0221482361_p10584112117365"></a><a name="zh-cn_topic_0221482361_p10584112117365"></a><a href="#zh-cn_topic_0221482361_request_Rq88User">user</a></p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482361_p1858572123614"><a name="zh-cn_topic_0221482361_p1858572123614"></a><a name="zh-cn_topic_0221482361_p1858572123614"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482361_p11587152111361"><a name="zh-cn_topic_0221482361_p11587152111361"></a><a name="zh-cn_topic_0221482361_p11587152111361"></a>Object</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482361_p1358872173618"><a name="zh-cn_topic_0221482361_p1358872173618"></a><a name="zh-cn_topic_0221482361_p1358872173618"></a>IAM用户信息。</p>
</td>
</tr>
</tbody>
</table>

**表 4**  user

<a name="zh-cn_topic_0221482361_request_Rq88User"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482361_row205901921183612"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0221482361_p3592142113361"><a name="zh-cn_topic_0221482361_p3592142113361"></a><a name="zh-cn_topic_0221482361_p3592142113361"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0221482361_p1459362116365"><a name="zh-cn_topic_0221482361_p1459362116365"></a><a name="zh-cn_topic_0221482361_p1459362116365"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0221482361_p759512183614"><a name="zh-cn_topic_0221482361_p759512183614"></a><a name="zh-cn_topic_0221482361_p759512183614"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0221482361_p1659612219368"><a name="zh-cn_topic_0221482361_p1659612219368"></a><a name="zh-cn_topic_0221482361_p1659612219368"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482361_row205905216366"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482361_p18598102117362"><a name="zh-cn_topic_0221482361_p18598102117362"></a><a name="zh-cn_topic_0221482361_p18598102117362"></a>password</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482361_p12599142113611"><a name="zh-cn_topic_0221482361_p12599142113611"></a><a name="zh-cn_topic_0221482361_p12599142113611"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482361_p1360172117360"><a name="zh-cn_topic_0221482361_p1360172117360"></a><a name="zh-cn_topic_0221482361_p1360172117360"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482361_p660212112360"><a name="zh-cn_topic_0221482361_p660212112360"></a><a name="zh-cn_topic_0221482361_p660212112360"></a>IAM用户的新密码。</p>
<a name="zh-cn_topic_0221482361_ul860417213363"></a><a name="zh-cn_topic_0221482361_ul860417213363"></a><ul id="zh-cn_topic_0221482361_ul860417213363"><li>系统默认密码最小长度为6位字符，在6-32位之间支持用户自定义密码长度。</li><li>至少包含以下四种字符中的两种： 大写字母、小写字母、数字和特殊字符。</li><li>不能包含手机号和邮箱。</li><li>必须满足用户所属帐号的<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0607.html" target="_blank" rel="noopener noreferrer">密码策略</a>要求。</li><li>新密码不能与当前密码相同。</li></ul>
</td>
</tr>
<tr id="zh-cn_topic_0221482361_row15907218367"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0221482361_p1461442112363"><a name="zh-cn_topic_0221482361_p1461442112363"></a><a name="zh-cn_topic_0221482361_p1461442112363"></a>original_password</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0221482361_p1261602110361"><a name="zh-cn_topic_0221482361_p1261602110361"></a><a name="zh-cn_topic_0221482361_p1261602110361"></a>是</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0221482361_p156176216362"><a name="zh-cn_topic_0221482361_p156176216362"></a><a name="zh-cn_topic_0221482361_p156176216362"></a>String</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0221482361_p206191221123610"><a name="zh-cn_topic_0221482361_p206191221123610"></a><a name="zh-cn_topic_0221482361_p206191221123610"></a>IAM用户的原密码。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0221482361_section8620121153617"></a>

无

## 请求示例<a name="zh-cn_topic_0221482361_section12624122123616"></a>

```
POST https://iam.myhuaweicloud.com/v3/users/{user_id}/password
```

```
{
    "user": {
        "password": "IAMNewPassword@",
        "original_password": "IAMOriginalPassword@"
    }
}
```

## 响应示例<a name="zh-cn_topic_0221482361_section206351221183616"></a>

无

## 返回值<a name="zh-cn_topic_0221482361_section15638192173614"></a>

<a name="zh-cn_topic_0221482361_table2456"></a>
<table><thead align="left"><tr id="zh-cn_topic_0221482361_row1764013217367"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0221482361_p8642192110366"><a name="zh-cn_topic_0221482361_p8642192110366"></a><a name="zh-cn_topic_0221482361_p8642192110366"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0221482361_p7643132123615"><a name="zh-cn_topic_0221482361_p7643132123615"></a><a name="zh-cn_topic_0221482361_p7643132123615"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0221482361_row14640152143614"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482361_p116459217365"><a name="zh-cn_topic_0221482361_p116459217365"></a><a name="zh-cn_topic_0221482361_p116459217365"></a>204</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482361_p564622123618"><a name="zh-cn_topic_0221482361_p564622123618"></a><a name="zh-cn_topic_0221482361_p564622123618"></a>修改成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482361_row18640321103615"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482361_p36483216362"><a name="zh-cn_topic_0221482361_p36483216362"></a><a name="zh-cn_topic_0221482361_p36483216362"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482361_p166501821123614"><a name="zh-cn_topic_0221482361_p166501821123614"></a><a name="zh-cn_topic_0221482361_p166501821123614"></a>参数无效。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482361_row1064019214368"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482361_p1465212143614"><a name="zh-cn_topic_0221482361_p1465212143614"></a><a name="zh-cn_topic_0221482361_p1465212143614"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482361_p265372112360"><a name="zh-cn_topic_0221482361_p265372112360"></a><a name="zh-cn_topic_0221482361_p265372112360"></a>认证失败。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482361_row2064018217365"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482361_p1465542114365"><a name="zh-cn_topic_0221482361_p1465542114365"></a><a name="zh-cn_topic_0221482361_p1465542114365"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482361_p765613219368"><a name="zh-cn_topic_0221482361_p765613219368"></a><a name="zh-cn_topic_0221482361_p765613219368"></a>没有操作权限。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482361_row4640192110361"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482361_p156571821153612"><a name="zh-cn_topic_0221482361_p156571821153612"></a><a name="zh-cn_topic_0221482361_p156571821153612"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482361_p13659821183611"><a name="zh-cn_topic_0221482361_p13659821183611"></a><a name="zh-cn_topic_0221482361_p13659821183611"></a>未找到相应的资源。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482361_row19640192110369"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482361_p1166015212369"><a name="zh-cn_topic_0221482361_p1166015212369"></a><a name="zh-cn_topic_0221482361_p1166015212369"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482361_p1266219213363"><a name="zh-cn_topic_0221482361_p1266219213363"></a><a name="zh-cn_topic_0221482361_p1266219213363"></a>不允许的方法。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482361_row1764012183611"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482361_p36641221113617"><a name="zh-cn_topic_0221482361_p36641221113617"></a><a name="zh-cn_topic_0221482361_p36641221113617"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482361_p15665122112362"><a name="zh-cn_topic_0221482361_p15665122112362"></a><a name="zh-cn_topic_0221482361_p15665122112362"></a>请求体过大。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482361_row1964013217363"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482361_p066752112362"><a name="zh-cn_topic_0221482361_p066752112362"></a><a name="zh-cn_topic_0221482361_p066752112362"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482361_p9668621163615"><a name="zh-cn_topic_0221482361_p9668621163615"></a><a name="zh-cn_topic_0221482361_p9668621163615"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0221482361_row1464022120361"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0221482361_p14670421173618"><a name="zh-cn_topic_0221482361_p14670421173618"></a><a name="zh-cn_topic_0221482361_p14670421173618"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482361_p4671821153619"><a name="zh-cn_topic_0221482361_p4671821153619"></a><a name="zh-cn_topic_0221482361_p4671821153619"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0221482361_section9678921183611"></a>

无

