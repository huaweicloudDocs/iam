# 查询Metadata文件<a name="zh-cn_topic_0057845553"></a>

## 功能介绍<a name="section46001270164832"></a>

该接口用于查询身份提供商导入到IAM中的Metadata文件内容。

该接口可以使用全局区域的域名和其他区域的域名调用，全局区域的域名为iam.myhuaweicloud.com。

## URI<a name="section47602695164832"></a>

-   URI格式

    GET /v3-ext/OS-FEDERATION/identity\_providers/\{idp\_id\}/protocols/\{protocol\_id\}/metadata


-   参数说明

    <a name="table45982210164832"></a>
    <table><thead align="left"><tr id="row34412857164832"><th class="cellrowborder" valign="top" width="20.49%" id="mcps1.1.5.1.1"><p id="p35978026164832"><a name="p35978026164832"></a><a name="p35978026164832"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.09%" id="mcps1.1.5.1.2"><p id="p28538959164832"><a name="p28538959164832"></a><a name="p28538959164832"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.11%" id="mcps1.1.5.1.3"><p id="p29954320164832"><a name="p29954320164832"></a><a name="p29954320164832"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.31%" id="mcps1.1.5.1.4"><p id="p10380887164832"><a name="p10380887164832"></a><a name="p10380887164832"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row35545481164832"><td class="cellrowborder" valign="top" width="20.49%" headers="mcps1.1.5.1.1 "><p id="p60611728164832"><a name="p60611728164832"></a><a name="p60611728164832"></a>idp_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.09%" headers="mcps1.1.5.1.2 "><p id="p10602964164832"><a name="p10602964164832"></a><a name="p10602964164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.11%" headers="mcps1.1.5.1.3 "><p id="p53533756164832"><a name="p53533756164832"></a><a name="p53533756164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.31%" headers="mcps1.1.5.1.4 "><p id="p41266993164832"><a name="p41266993164832"></a><a name="p41266993164832"></a>身份提供商的ID。</p>
    </td>
    </tr>
    <tr id="row35858619164832"><td class="cellrowborder" valign="top" width="20.49%" headers="mcps1.1.5.1.1 "><p id="p18867054164832"><a name="p18867054164832"></a><a name="p18867054164832"></a>protocol _id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.09%" headers="mcps1.1.5.1.2 "><p id="p51836385164832"><a name="p51836385164832"></a><a name="p51836385164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.11%" headers="mcps1.1.5.1.3 "><p id="p37997628164832"><a name="p37997628164832"></a><a name="p37997628164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.31%" headers="mcps1.1.5.1.4 "><p id="p57909032164832"><a name="p57909032164832"></a><a name="p57909032164832"></a>Protocol的ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section60120012164832"></a>

-   Request Header参数说明

    <a name="table48610655164832"></a>
    <table><thead align="left"><tr id="row34035357164832"><th class="cellrowborder" valign="top" width="20.22%" id="mcps1.1.5.1.1"><p id="p5400536164832"><a name="p5400536164832"></a><a name="p5400536164832"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.46%" id="mcps1.1.5.1.2"><p id="p34790247164832"><a name="p34790247164832"></a><a name="p34790247164832"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.82%" id="mcps1.1.5.1.3"><p id="p66546611164832"><a name="p66546611164832"></a><a name="p66546611164832"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.5%" id="mcps1.1.5.1.4"><p id="p21566371164832"><a name="p21566371164832"></a><a name="p21566371164832"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row2045599164832"><td class="cellrowborder" valign="top" width="20.22%" headers="mcps1.1.5.1.1 "><p id="p31475856164832"><a name="p31475856164832"></a><a name="p31475856164832"></a>Content-Type</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.46%" headers="mcps1.1.5.1.2 "><p id="p66516446164832"><a name="p66516446164832"></a><a name="p66516446164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.82%" headers="mcps1.1.5.1.3 "><p id="p19123056164832"><a name="p19123056164832"></a><a name="p19123056164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.5%" headers="mcps1.1.5.1.4 "><p id="p5463727164832"><a name="p5463727164832"></a><a name="p5463727164832"></a>该字段内容填为<span class="parmvalue" id="parmvalue1823317483242"><a name="parmvalue1823317483242"></a><a name="parmvalue1823317483242"></a>“application/json;charset=utf8”</span>。</p>
    </td>
    </tr>
    <tr id="row49173546164832"><td class="cellrowborder" valign="top" width="20.22%" headers="mcps1.1.5.1.1 "><p id="p23634327164832"><a name="p23634327164832"></a><a name="p23634327164832"></a>X-Auth-Token</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.46%" headers="mcps1.1.5.1.2 "><p id="p35332324164832"><a name="p35332324164832"></a><a name="p35332324164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.82%" headers="mcps1.1.5.1.3 "><p id="p43345977164832"><a name="p43345977164832"></a><a name="p43345977164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.5%" headers="mcps1.1.5.1.4 "><p id="p64412052143925"><a name="p64412052143925"></a><a name="p64412052143925"></a>已认证的拥有Security Administrator权限的token。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    curl -i -k -H 'Accept:application/json' -H 'Content-Type:application/json;charset=utf8' -H "X-Auth-Token:$token" -X GET https://10.185.190.118:31943/v3-ext/OS-FEDERATION/identity_providers/ACME/protocols/saml/metadata
    ```


## 响应<a name="section34034532164832"></a>

-   Response Body参数说明

    <a name="table29374141164832"></a>
    <table><thead align="left"><tr id="row48948992164832"><th class="cellrowborder" valign="top" width="20.22%" id="mcps1.1.5.1.1"><p id="p5445443164832"><a name="p5445443164832"></a><a name="p5445443164832"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.5%" id="mcps1.1.5.1.2"><p id="p38427718164832"><a name="p38427718164832"></a><a name="p38427718164832"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.04%" id="mcps1.1.5.1.3"><p id="p25637425164832"><a name="p25637425164832"></a><a name="p25637425164832"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.239999999999995%" id="mcps1.1.5.1.4"><p id="p63365549164832"><a name="p63365549164832"></a><a name="p63365549164832"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row32335841164832"><td class="cellrowborder" valign="top" width="20.22%" headers="mcps1.1.5.1.1 "><p id="p1957494164832"><a name="p1957494164832"></a><a name="p1957494164832"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.5%" headers="mcps1.1.5.1.2 "><p id="p24339348164832"><a name="p24339348164832"></a><a name="p24339348164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.04%" headers="mcps1.1.5.1.3 "><p id="p25330146164832"><a name="p25330146164832"></a><a name="p25330146164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.239999999999995%" headers="mcps1.1.5.1.4 "><p id="p38475912164832"><a name="p38475912164832"></a><a name="p38475912164832"></a>Metadata的ID。</p>
    </td>
    </tr>
    <tr id="row10738892164832"><td class="cellrowborder" valign="top" width="20.22%" headers="mcps1.1.5.1.1 "><p id="p64543914164832"><a name="p64543914164832"></a><a name="p64543914164832"></a>idp_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.5%" headers="mcps1.1.5.1.2 "><p id="p60674549164832"><a name="p60674549164832"></a><a name="p60674549164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.04%" headers="mcps1.1.5.1.3 "><p id="p15691412164832"><a name="p15691412164832"></a><a name="p15691412164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.239999999999995%" headers="mcps1.1.5.1.4 "><p id="p63044848164832"><a name="p63044848164832"></a><a name="p63044848164832"></a>身份提供商的ID。</p>
    </td>
    </tr>
    <tr id="row30532720164832"><td class="cellrowborder" valign="top" width="20.22%" headers="mcps1.1.5.1.1 "><p id="p57231217164832"><a name="p57231217164832"></a><a name="p57231217164832"></a>entity_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.5%" headers="mcps1.1.5.1.2 "><p id="p5216995164832"><a name="p5216995164832"></a><a name="p5216995164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.04%" headers="mcps1.1.5.1.3 "><p id="p19923437164832"><a name="p19923437164832"></a><a name="p19923437164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.239999999999995%" headers="mcps1.1.5.1.4 "><p id="p3185720164832"><a name="p3185720164832"></a><a name="p3185720164832"></a>Metadata文件中的entityID字段。</p>
    </td>
    </tr>
    <tr id="row28671485164832"><td class="cellrowborder" valign="top" width="20.22%" headers="mcps1.1.5.1.1 "><p id="p40688972164832"><a name="p40688972164832"></a><a name="p40688972164832"></a>protocol_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.5%" headers="mcps1.1.5.1.2 "><p id="p7472431164832"><a name="p7472431164832"></a><a name="p7472431164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.04%" headers="mcps1.1.5.1.3 "><p id="p1287183164832"><a name="p1287183164832"></a><a name="p1287183164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.239999999999995%" headers="mcps1.1.5.1.4 "><p id="p37152979164832"><a name="p37152979164832"></a><a name="p37152979164832"></a>Protocol的ID。</p>
    </td>
    </tr>
    <tr id="row65941358164832"><td class="cellrowborder" valign="top" width="20.22%" headers="mcps1.1.5.1.1 "><p id="p39649796164832"><a name="p39649796164832"></a><a name="p39649796164832"></a>domain_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.5%" headers="mcps1.1.5.1.2 "><p id="p57516914164832"><a name="p57516914164832"></a><a name="p57516914164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.04%" headers="mcps1.1.5.1.3 "><p id="p28358497164832"><a name="p28358497164832"></a><a name="p28358497164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.239999999999995%" headers="mcps1.1.5.1.4 "><p id="p15336953164832"><a name="p15336953164832"></a><a name="p15336953164832"></a>用户所属domain的ID。</p>
    </td>
    </tr>
    <tr id="row3814851164832"><td class="cellrowborder" valign="top" width="20.22%" headers="mcps1.1.5.1.1 "><p id="p40567530164832"><a name="p40567530164832"></a><a name="p40567530164832"></a>xaccount_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.5%" headers="mcps1.1.5.1.2 "><p id="p64744526164832"><a name="p64744526164832"></a><a name="p64744526164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.04%" headers="mcps1.1.5.1.3 "><p id="p9815254164832"><a name="p9815254164832"></a><a name="p9815254164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.239999999999995%" headers="mcps1.1.5.1.4 "><p id="p56838123164832"><a name="p56838123164832"></a><a name="p56838123164832"></a>租户来源，默认为空。</p>
    </td>
    </tr>
    <tr id="row41781061164832"><td class="cellrowborder" valign="top" width="20.22%" headers="mcps1.1.5.1.1 "><p id="p28822808164832"><a name="p28822808164832"></a><a name="p28822808164832"></a>update_time</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.5%" headers="mcps1.1.5.1.2 "><p id="p52946091164832"><a name="p52946091164832"></a><a name="p52946091164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.04%" headers="mcps1.1.5.1.3 "><p id="p60774950164832"><a name="p60774950164832"></a><a name="p60774950164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.239999999999995%" headers="mcps1.1.5.1.4 "><p id="p23823922164832"><a name="p23823922164832"></a><a name="p23823922164832"></a>导入或更新Metadata文件的时间。</p>
    </td>
    </tr>
    <tr id="row13088710164832"><td class="cellrowborder" valign="top" width="20.22%" headers="mcps1.1.5.1.1 "><p id="p53552557164832"><a name="p53552557164832"></a><a name="p53552557164832"></a>data</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.5%" headers="mcps1.1.5.1.2 "><p id="p42789881164832"><a name="p42789881164832"></a><a name="p42789881164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.04%" headers="mcps1.1.5.1.3 "><p id="p43428370164832"><a name="p43428370164832"></a><a name="p43428370164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.239999999999995%" headers="mcps1.1.5.1.4 "><p id="p28037087164832"><a name="p28037087164832"></a><a name="p28037087164832"></a>Metadata文件的内容。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例

    ```
    {
    "id": "40c174f35ff94e31b8257ad4991bce8b",
    "idp_id": "ACME",
    "entity_id": "https://idp.test.com/idp/shibboleth",
    "protocol_id": "saml",
    "domain_id": "ed7a77d365304f458f7d0a7909c6d889",
    "xaccount_type": "",
    "update_time": "2016-10-26T09:26:23.000000",
    "data": "$data"}
    ```


## 状态码<a name="section5936311164832"></a>

<a name="table11079186164832"></a>
<table><thead align="left"><tr id="row37659029164832"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="p30482470164832"><a name="p30482470164832"></a><a name="p30482470164832"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="p53161000164832"><a name="p53161000164832"></a><a name="p53161000164832"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row11073730164832"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p24556957164832"><a name="p24556957164832"></a><a name="p24556957164832"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p42956513164832"><a name="p42956513164832"></a><a name="p42956513164832"></a>获取成功。</p>
</td>
</tr>
<tr id="row51064297164832"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p42567388164832"><a name="p42567388164832"></a><a name="p42567388164832"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p25406412164832"><a name="p25406412164832"></a><a name="p25406412164832"></a>请求错误。</p>
</td>
</tr>
<tr id="row27331118164832"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p66336931164832"><a name="p66336931164832"></a><a name="p66336931164832"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p4582345164832"><a name="p4582345164832"></a><a name="p4582345164832"></a>认证失败。</p>
</td>
</tr>
<tr id="row41241110164832"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p52195591164832"><a name="p52195591164832"></a><a name="p52195591164832"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p67093374164832"><a name="p67093374164832"></a><a name="p67093374164832"></a>鉴权失败。</p>
</td>
</tr>
<tr id="row66969454164832"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p55816678164832"><a name="p55816678164832"></a><a name="p55816678164832"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p24857046164832"><a name="p24857046164832"></a><a name="p24857046164832"></a>内部服务错误。</p>
</td>
</tr>
</tbody>
</table>

