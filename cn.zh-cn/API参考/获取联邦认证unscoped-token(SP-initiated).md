# 获取联邦认证unscoped token\(SP initiated\)<a name="zh-cn_topic_0057845629"></a>

## 功能介绍<a name="section42991548164730"></a>

该接口用于通过SP initiated的联邦认证方式获取unscoped token。

Unscoped token不能用来鉴权，若联邦用户需要使用token进行鉴权，请参考[获取联邦认证scoped token](获取联邦认证scoped-token.md)获取scoped token。

该接口可以使用全局区域的域名和其他区域的域名调用，全局区域的域名为iam.myhuaweicloud.com。

## URI<a name="section999597164730"></a>

-   URI格式

    GET /v3/OS-FEDERATION/identity\_providers/\{idp\_id\}/protocols/\{protocol\_id\}/auth


-   参数说明

    <a name="table45982210164832"></a>
    <table><thead align="left"><tr id="row34412857164832"><th class="cellrowborder" valign="top" width="17.16828317168283%" id="mcps1.1.5.1.1"><p id="p35978026164832"><a name="p35978026164832"></a><a name="p35978026164832"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.538046195380463%" id="mcps1.1.5.1.2"><p id="p28538959164832"><a name="p28538959164832"></a><a name="p28538959164832"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.308169183081695%" id="mcps1.1.5.1.3"><p id="p29954320164832"><a name="p29954320164832"></a><a name="p29954320164832"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.98550144985502%" id="mcps1.1.5.1.4"><p id="p10380887164832"><a name="p10380887164832"></a><a name="p10380887164832"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row35545481164832"><td class="cellrowborder" valign="top" width="17.16828317168283%" headers="mcps1.1.5.1.1 "><p id="p60611728164832"><a name="p60611728164832"></a><a name="p60611728164832"></a>idp_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.538046195380463%" headers="mcps1.1.5.1.2 "><p id="p10602964164832"><a name="p10602964164832"></a><a name="p10602964164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.308169183081695%" headers="mcps1.1.5.1.3 "><p id="p53533756164832"><a name="p53533756164832"></a><a name="p53533756164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.98550144985502%" headers="mcps1.1.5.1.4 "><p id="p41266993164832"><a name="p41266993164832"></a><a name="p41266993164832"></a>身份提供商的ID。</p>
    </td>
    </tr>
    <tr id="row35858619164832"><td class="cellrowborder" valign="top" width="17.16828317168283%" headers="mcps1.1.5.1.1 "><p id="p18867054164832"><a name="p18867054164832"></a><a name="p18867054164832"></a>protocol _id</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.538046195380463%" headers="mcps1.1.5.1.2 "><p id="p51836385164832"><a name="p51836385164832"></a><a name="p51836385164832"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.308169183081695%" headers="mcps1.1.5.1.3 "><p id="p37997628164832"><a name="p37997628164832"></a><a name="p37997628164832"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.98550144985502%" headers="mcps1.1.5.1.4 "><p id="p57909032164832"><a name="p57909032164832"></a><a name="p57909032164832"></a>Protocol的ID。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section30144898164730"></a>

-   Request Header参数说明

    <a name="table56458564164645"></a>
    <table><thead align="left"><tr id="row38321014164645"><th class="cellrowborder" valign="top" width="17%" id="mcps1.1.5.1.1"><p id="p4891467164645"><a name="p4891467164645"></a><a name="p4891467164645"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="19%" id="mcps1.1.5.1.2"><p id="p60664507164645"><a name="p60664507164645"></a><a name="p60664507164645"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="14.000000000000002%" id="mcps1.1.5.1.3"><p id="p14878007164645"><a name="p14878007164645"></a><a name="p14878007164645"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="50%" id="mcps1.1.5.1.4"><p id="p64267944164645"><a name="p64267944164645"></a><a name="p64267944164645"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row47522392164645"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.1 "><p id="p22387518164645"><a name="p22387518164645"></a><a name="p22387518164645"></a>Accept</p>
    </td>
    <td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.2 "><p id="p1449685164645"><a name="p1449685164645"></a><a name="p1449685164645"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.1.5.1.3 "><p id="p50315689164645"><a name="p50315689164645"></a><a name="p50315689164645"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.5.1.4 "><a name="ul2066821281118"></a><a name="ul2066821281118"></a><ul id="ul2066821281118"><li>通过页面单点认证 （WebSSO）方式获取token时，不需要该参数。</li><li>通过增强客户端代理（ECP）方式获取token时，该字段需取值如下：<p id="p585112176116"><a name="p585112176116"></a><a name="p585112176116"></a>application/vnd.paos+xml</p>
    </li></ul>
    </td>
    </tr>
    <tr id="row45829305164645"><td class="cellrowborder" valign="top" width="17%" headers="mcps1.1.5.1.1 "><p id="p25048351164645"><a name="p25048351164645"></a><a name="p25048351164645"></a>PAOS</p>
    </td>
    <td class="cellrowborder" valign="top" width="19%" headers="mcps1.1.5.1.2 "><p id="p15650549164645"><a name="p15650549164645"></a><a name="p15650549164645"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="14.000000000000002%" headers="mcps1.1.5.1.3 "><p id="p59734927164645"><a name="p59734927164645"></a><a name="p59734927164645"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.5.1.4 "><a name="ul10681123417114"></a><a name="ul10681123417114"></a><ul id="ul10681123417114"><li>通过页面单点认证 （WebSSO）方式获取token时，不需要该参数。</li><li>增强客户端代理（ECP）获取token时，该字段需取值如下：<p id="p60218117164645"><a name="p60218117164645"></a><a name="p60218117164645"></a>urn:oasis:names:tc:SAML:2.0:profiles:SSO:ecp</p>
    </li></ul>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >1.  该接口支持通过页面单点认证 （WebSSO）和增强客户端代理（ECP）两种方式获取token。通过不同的请求header区分，具体使用请参考Request Header参数说明。  
    >2.  不建议直接调用该接口，请使用openstackclient获取token。  

-   请求样例

    ```
    GET /v3/OS-FEDERATION/identity_providers/idptest/protocols/saml/auth
    ```


## 响应<a name="section5167254164730"></a>

-   Response Body参数说明

    <a name="table30197476165124"></a>
    <table><thead align="left"><tr id="row25190343165124"><th class="cellrowborder" valign="top" width="16.951695169516952%" id="mcps1.1.5.1.1"><p id="p63550324165124"><a name="p63550324165124"></a><a name="p63550324165124"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.51195119511951%" id="mcps1.1.5.1.2"><p id="p47302590165124"><a name="p47302590165124"></a><a name="p47302590165124"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.941894189418942%" id="mcps1.1.5.1.3"><p id="p6304564165124"><a name="p6304564165124"></a><a name="p6304564165124"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.594459445944594%" id="mcps1.1.5.1.4"><p id="p40907712165124"><a name="p40907712165124"></a><a name="p40907712165124"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row15598896165124"><td class="cellrowborder" valign="top" width="16.951695169516952%" headers="mcps1.1.5.1.1 "><p id="p16586493165124"><a name="p16586493165124"></a><a name="p16586493165124"></a>token</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.51195119511951%" headers="mcps1.1.5.1.2 "><p id="p1328717165124"><a name="p1328717165124"></a><a name="p1328717165124"></a>body</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.941894189418942%" headers="mcps1.1.5.1.3 "><p id="p40517270165124"><a name="p40517270165124"></a><a name="p40517270165124"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.594459445944594%" headers="mcps1.1.5.1.4 "><p id="p60673407165124"><a name="p60673407165124"></a><a name="p60673407165124"></a>联邦认证的unscoped token，包含methods和用户信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   Response Header参数说明

    <a name="table1559217555257"></a>
    <table><thead align="left"><tr id="row1639165552510"><th class="cellrowborder" valign="top" width="22.222222222222225%" id="mcps1.1.5.1.1"><p id="p463919553252"><a name="p463919553252"></a><a name="p463919553252"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.19191919191919%" id="mcps1.1.5.1.2"><p id="p12639165518259"><a name="p12639165518259"></a><a name="p12639165518259"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.18181818181818%" id="mcps1.1.5.1.3"><p id="p0639175518255"><a name="p0639175518255"></a><a name="p0639175518255"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="40.40404040404041%" id="mcps1.1.5.1.4"><p id="p86391855122510"><a name="p86391855122510"></a><a name="p86391855122510"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row166394552257"><td class="cellrowborder" valign="top" width="22.222222222222225%" headers="mcps1.1.5.1.1 "><p id="p176393559255"><a name="p176393559255"></a><a name="p176393559255"></a>X-Subject-Token</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.19191919191919%" headers="mcps1.1.5.1.2 "><p id="p46391955152513"><a name="p46391955152513"></a><a name="p46391955152513"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.18181818181818%" headers="mcps1.1.5.1.3 "><p id="p663945522510"><a name="p663945522510"></a><a name="p663945522510"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.40404040404041%" headers="mcps1.1.5.1.4 "><p id="p166391255132519"><a name="p166391255132519"></a><a name="p166391255132519"></a>签名后的token。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例

    ```
    {
        "token": {
            "issued_at": "2017-05-23T06:54:51.763000Z",
            "expires_at": "2017-05-24T06:54:51.763000Z",
            "methods": [
                "mapped"
            ],
            "user": {
                "domain": {
                    "id": "e31ac82d778b4d128cb6fed37fd72cdb",
                    "name": "exampledomain"
                },
                "id": "RMQTgtjjSNGDcKy7oUmI3AZg7GgsWG0Z",
                "name": "exampleuser",
                "OS-FEDERATION": {
                    "identity_provider": {
                        "id": "exampleuser"
                    },
                    "protocol": {
                        "id": "saml"
                    },
                    "groups": [
                        {
                            "id": "b40189e26ea44f959877621b4b298db5"
                        }
                    ]
                }
            }
        }
    }
    ```


## 状态码<a name="section33762092164730"></a>

<a name="table50374951164730"></a>
<table><thead align="left"><tr id="row57231606164730"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="p5248518164730"><a name="p5248518164730"></a><a name="p5248518164730"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="p22476794164730"><a name="p22476794164730"></a><a name="p22476794164730"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row8681019164730"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p32073904164730"><a name="p32073904164730"></a><a name="p32073904164730"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p47849409164730"><a name="p47849409164730"></a><a name="p47849409164730"></a>请求成功，需进一步获取用户信息。</p>
</td>
</tr>
<tr id="row27991504164730"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p52719384164730"><a name="p52719384164730"></a><a name="p52719384164730"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p42411696164730"><a name="p42411696164730"></a><a name="p42411696164730"></a>请求成功，返回token。</p>
</td>
</tr>
<tr id="row46160945164730"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p48049093164730"><a name="p48049093164730"></a><a name="p48049093164730"></a>302</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p66771325164730"><a name="p66771325164730"></a><a name="p66771325164730"></a>请求未携带Identity Provider用户信息时，跳转到Identity Provider认证页面。</p>
</td>
</tr>
<tr id="row64071018164730"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p22370004164730"><a name="p22370004164730"></a><a name="p22370004164730"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p31063164730"><a name="p31063164730"></a><a name="p31063164730"></a>请求错误。</p>
</td>
</tr>
<tr id="row279569164730"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p22645099164730"><a name="p22645099164730"></a><a name="p22645099164730"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p22313713164730"><a name="p22313713164730"></a><a name="p22313713164730"></a>认证失败。</p>
</td>
</tr>
<tr id="row66605697164730"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p26352373164730"><a name="p26352373164730"></a><a name="p26352373164730"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p54167498164730"><a name="p54167498164730"></a><a name="p54167498164730"></a>鉴权失败。</p>
</td>
</tr>
<tr id="row17745440164730"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p28094569164730"><a name="p28094569164730"></a><a name="p28094569164730"></a>405</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p61067622164730"><a name="p61067622164730"></a><a name="p61067622164730"></a>不允许的方法。</p>
</td>
</tr>
<tr id="row12737692164730"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p25120131164730"><a name="p25120131164730"></a><a name="p25120131164730"></a>413</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p21464722164730"><a name="p21464722164730"></a><a name="p21464722164730"></a>请求体过大。</p>
</td>
</tr>
<tr id="row58964777164730"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p11417608164730"><a name="p11417608164730"></a><a name="p11417608164730"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p52411044164730"><a name="p52411044164730"></a><a name="p52411044164730"></a>内部服务错误。</p>
</td>
</tr>
<tr id="row1937348164730"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p22707461164730"><a name="p22707461164730"></a><a name="p22707461164730"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p27365047164730"><a name="p27365047164730"></a><a name="p27365047164730"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

