# 导入Metadata文件<a name="ZH-CN_TOPIC_0110485118"></a>

## 功能介绍<a name="section60756004163916"></a>

租户使用联邦认证功能时，需要先将Metadata文件导入IAM中，该接口用于导入租户的Metadata文件。

该接口仅适用于全局区域（ALL），全局区域的域名为iam.myhuaweicloud.com。

## URI<a name="section66385700163916"></a>

-   URI格式

    POST /v3-ext/OS-FEDERATION/identity\_providers/\{idp\_id\}/protocols/\{protocol\_id\}/metadata


-   参数说明

    <a name="table55329861163916"></a>
    <table><thead align="left"><tr id="row25801157163916"><th class="cellrowborder" valign="top" width="20.48795120487951%" id="mcps1.1.5.1.1"><p id="p9518943163916"><a name="p9518943163916"></a><a name="p9518943163916"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.008299170082992%" id="mcps1.1.5.1.2"><p id="p32836901163916"><a name="p32836901163916"></a><a name="p32836901163916"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.958204179582044%" id="mcps1.1.5.1.3"><p id="p42543361163916"><a name="p42543361163916"></a><a name="p42543361163916"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.54554544545545%" id="mcps1.1.5.1.4"><p id="p23460184163916"><a name="p23460184163916"></a><a name="p23460184163916"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row21226772163916"><td class="cellrowborder" valign="top" width="20.48795120487951%" headers="mcps1.1.5.1.1 "><p id="p41647005163916"><a name="p41647005163916"></a><a name="p41647005163916"></a>idp_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.008299170082992%" headers="mcps1.1.5.1.2 "><p id="p17964250163916"><a name="p17964250163916"></a><a name="p17964250163916"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.958204179582044%" headers="mcps1.1.5.1.3 "><p id="p45818164163916"><a name="p45818164163916"></a><a name="p45818164163916"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54554544545545%" headers="mcps1.1.5.1.4 "><p id="p20283794163916"><a name="p20283794163916"></a><a name="p20283794163916"></a>已经注册的身份提供商的ID。</p>
    </td>
    </tr>
    <tr id="row48336422163916"><td class="cellrowborder" valign="top" width="20.48795120487951%" headers="mcps1.1.5.1.1 "><p id="p22936134163916"><a name="p22936134163916"></a><a name="p22936134163916"></a>protocol _id</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.008299170082992%" headers="mcps1.1.5.1.2 "><p id="p45887583163916"><a name="p45887583163916"></a><a name="p45887583163916"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.958204179582044%" headers="mcps1.1.5.1.3 "><p id="p25906712163916"><a name="p25906712163916"></a><a name="p25906712163916"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54554544545545%" headers="mcps1.1.5.1.4 "><p id="p18068889163916"><a name="p18068889163916"></a><a name="p18068889163916"></a>已经注册的Protocol的ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section54293899163916"></a>

-   Request Header参数说明

    <a name="table8423392163916"></a>
    <table><thead align="left"><tr id="row19381879163916"><th class="cellrowborder" valign="top" width="20.31%" id="mcps1.1.5.1.1"><p id="p26428347163916"><a name="p26428347163916"></a><a name="p26428347163916"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.24%" id="mcps1.1.5.1.2"><p id="p60321356163916"><a name="p60321356163916"></a><a name="p60321356163916"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.91%" id="mcps1.1.5.1.3"><p id="p54191633163916"><a name="p54191633163916"></a><a name="p54191633163916"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.54%" id="mcps1.1.5.1.4"><p id="p27446130163916"><a name="p27446130163916"></a><a name="p27446130163916"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row8544089163916"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.1.5.1.1 "><p id="p20982571163916"><a name="p20982571163916"></a><a name="p20982571163916"></a>Content-Type</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.1.5.1.2 "><p id="p21866706163916"><a name="p21866706163916"></a><a name="p21866706163916"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.91%" headers="mcps1.1.5.1.3 "><p id="p26372790163916"><a name="p26372790163916"></a><a name="p26372790163916"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54%" headers="mcps1.1.5.1.4 "><p id="p55821246163916"><a name="p55821246163916"></a><a name="p55821246163916"></a>该字段内容填为<span class="parmvalue" id="parmvalue1823317483242"><a name="parmvalue1823317483242"></a><a name="parmvalue1823317483242"></a>“application/json;charset=utf8”</span>。</p>
    </td>
    </tr>
    <tr id="row32629171163916"><td class="cellrowborder" valign="top" width="20.31%" headers="mcps1.1.5.1.1 "><p id="p25717229163916"><a name="p25717229163916"></a><a name="p25717229163916"></a>X-Auth-Token</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24%" headers="mcps1.1.5.1.2 "><p id="p2720832163916"><a name="p2720832163916"></a><a name="p2720832163916"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.91%" headers="mcps1.1.5.1.3 "><p id="p19060819163916"><a name="p19060819163916"></a><a name="p19060819163916"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54%" headers="mcps1.1.5.1.4 "><p id="p19047553144032"><a name="p19047553144032"></a><a name="p19047553144032"></a>已认证的拥有Security Administrator权限的token。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   Request Body参数说明

    <a name="table20418334163916"></a>
    <table><thead align="left"><tr id="row21228487163916"><th class="cellrowborder" valign="top" width="20.549999999999997%" id="mcps1.1.5.1.1"><p id="p41785905163916"><a name="p41785905163916"></a><a name="p41785905163916"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.82%" id="mcps1.1.5.1.2"><p id="p29215135163916"><a name="p29215135163916"></a><a name="p29215135163916"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.26%" id="mcps1.1.5.1.3"><p id="p17615738163916"><a name="p17615738163916"></a><a name="p17615738163916"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.37%" id="mcps1.1.5.1.4"><p id="p17588649163916"><a name="p17588649163916"></a><a name="p17588649163916"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row15394453163916"><td class="cellrowborder" valign="top" width="20.549999999999997%" headers="mcps1.1.5.1.1 "><p id="p38991141163916"><a name="p38991141163916"></a><a name="p38991141163916"></a>xaccount_type</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.82%" headers="mcps1.1.5.1.2 "><p id="p4165825163916"><a name="p4165825163916"></a><a name="p4165825163916"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.26%" headers="mcps1.1.5.1.3 "><p id="p1887570163916"><a name="p1887570163916"></a><a name="p1887570163916"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.37%" headers="mcps1.1.5.1.4 "><p id="p18675520163916"><a name="p18675520163916"></a><a name="p18675520163916"></a>该字段为标识租户来源字段，默认为空。</p>
    </td>
    </tr>
    <tr id="row33861957163916"><td class="cellrowborder" valign="top" width="20.549999999999997%" headers="mcps1.1.5.1.1 "><p id="p58464009163916"><a name="p58464009163916"></a><a name="p58464009163916"></a>metadata</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.82%" headers="mcps1.1.5.1.2 "><p id="p37964252163916"><a name="p37964252163916"></a><a name="p37964252163916"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.26%" headers="mcps1.1.5.1.3 "><p id="p55205609163916"><a name="p55205609163916"></a><a name="p55205609163916"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.37%" headers="mcps1.1.5.1.4 "><p id="p42469334163916"><a name="p42469334163916"></a><a name="p42469334163916"></a>该字段为用户IdP服务器的Metadata文件的内容。</p>
    </td>
    </tr>
    <tr id="row46679688163916"><td class="cellrowborder" valign="top" width="20.549999999999997%" headers="mcps1.1.5.1.1 "><p id="p22958377163916"><a name="p22958377163916"></a><a name="p22958377163916"></a>domain_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.82%" headers="mcps1.1.5.1.2 "><p id="p47689214163916"><a name="p47689214163916"></a><a name="p47689214163916"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.26%" headers="mcps1.1.5.1.3 "><p id="p37621103163916"><a name="p37621103163916"></a><a name="p37621103163916"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.37%" headers="mcps1.1.5.1.4 "><p id="p27410534163916"><a name="p27410534163916"></a><a name="p27410534163916"></a>用户所属domain的ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    curl -i -k -H 'Accept:application/json' -H 'Content-Type:application/json;charset=utf8' -H "X-Auth-Token:$token" -X POST -d '{"xaccount_type":"","domain_id":"ed7a77d365304f458f7d0a7909c6d889","metadata":"$metadataContent"}' https://10.185.190.118:31943/v3-ext/OS-FEDERATION/identity_providers/ACME/protocols/saml/metadata
    ```


## 响应<a name="section62771979163916"></a>

响应样例

```
{ "message": "Import metadata successful"}
```

## 状态码<a name="section64646211163916"></a>

<a name="table1851743163916"></a>
<table><thead align="left"><tr id="row23259822163916"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="p4997463163916"><a name="p4997463163916"></a><a name="p4997463163916"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="p2141364163916"><a name="p2141364163916"></a><a name="p2141364163916"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row39232814163916"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p23741356163916"><a name="p23741356163916"></a><a name="p23741356163916"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p44001687163916"><a name="p44001687163916"></a><a name="p44001687163916"></a>导入成功。</p>
</td>
</tr>
<tr id="row60470864163916"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p66301833163916"><a name="p66301833163916"></a><a name="p66301833163916"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p1739362163916"><a name="p1739362163916"></a><a name="p1739362163916"></a>请求错误。</p>
</td>
</tr>
<tr id="row15654258163916"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p60035358163916"><a name="p60035358163916"></a><a name="p60035358163916"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p31025855163916"><a name="p31025855163916"></a><a name="p31025855163916"></a>认证失败。</p>
</td>
</tr>
<tr id="row10797247163916"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p2161834163916"><a name="p2161834163916"></a><a name="p2161834163916"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p40890878163916"><a name="p40890878163916"></a><a name="p40890878163916"></a>鉴权失败。</p>
</td>
</tr>
<tr id="row32473582163916"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p13114481163916"><a name="p13114481163916"></a><a name="p13114481163916"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p55640049163916"><a name="p55640049163916"></a><a name="p55640049163916"></a>内部服务错误。</p>
</td>
</tr>
</tbody>
</table>

