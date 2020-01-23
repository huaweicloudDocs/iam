# 获取联邦认证unscoped token\(IdP initiated\)<a name="iam_02_0003"></a>

## 功能介绍<a name="section42991548164730"></a>

该接口用于通过IdP initiated的联邦认证方式获取unscoped token。

Unscoped token不能用来鉴权，若联邦用户需要使用token进行鉴权，请参考[获取联邦认证scoped token](获取联邦认证scoped-token.md)获取scoped token。

该接口可以使用全局区域的域名和其他区域的域名调用，全局区域的域名为iam.myhuaweicloud.com。

## URI<a name="section999597164730"></a>

URI格式

POST /v3.0/OS-FEDERATION/tokens

## 请求<a name="section30144898164730"></a>

-   Request Header参数说明

    <a name="table56458564164645"></a>
    <table><thead align="left"><tr id="row38321014164645"><th class="cellrowborder" valign="top" width="20.76%" id="mcps1.1.5.1.1"><p id="p4891467164645"><a name="p4891467164645"></a><a name="p4891467164645"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.299999999999997%" id="mcps1.1.5.1.2"><p id="p60664507164645"><a name="p60664507164645"></a><a name="p60664507164645"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.48%" id="mcps1.1.5.1.3"><p id="p14878007164645"><a name="p14878007164645"></a><a name="p14878007164645"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.46%" id="mcps1.1.5.1.4"><p id="p64267944164645"><a name="p64267944164645"></a><a name="p64267944164645"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row16522014164645"><td class="cellrowborder" valign="top" width="20.76%" headers="mcps1.1.5.1.1 "><p id="p16994440164645"><a name="p16994440164645"></a><a name="p16994440164645"></a>X-Idp-Id</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.299999999999997%" headers="mcps1.1.5.1.2 "><p id="p34372423164645"><a name="p34372423164645"></a><a name="p34372423164645"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.48%" headers="mcps1.1.5.1.3 "><p id="p32702874164645"><a name="p32702874164645"></a><a name="p32702874164645"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.46%" headers="mcps1.1.5.1.4 "><p id="p45605165175031"><a name="p45605165175031"></a><a name="p45605165175031"></a>身份提供商的ID。</p>
    </td>
    </tr>
    <tr id="row27958398103142"><td class="cellrowborder" valign="top" width="20.76%" headers="mcps1.1.5.1.1 "><p id="p50037738103142"><a name="p50037738103142"></a><a name="p50037738103142"></a>Content-Type</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.299999999999997%" headers="mcps1.1.5.1.2 "><p id="p26525003103142"><a name="p26525003103142"></a><a name="p26525003103142"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.48%" headers="mcps1.1.5.1.3 "><p id="p1041673103142"><a name="p1041673103142"></a><a name="p1041673103142"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.46%" headers="mcps1.1.5.1.4 "><p id="p61308811103259"><a name="p61308811103259"></a><a name="p61308811103259"></a>客户端必须使用浏览器提交表单数据的方式向服务端传SAMLResponse参数，故该字段需取值如下：</p>
    <p id="p17266699103142"><a name="p17266699103142"></a><a name="p17266699103142"></a>application/x-www-form-urlencoded</p>
    </td>
    </tr>
    </tbody>
    </table>

-   Request Body参数说明

    <a name="table58447617102532"></a>
    <table><thead align="left"><tr id="row28600734102532"><th class="cellrowborder" valign="top" width="20.62%" id="mcps1.1.5.1.1"><p id="p34958131102532"><a name="p34958131102532"></a><a name="p34958131102532"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.27%" id="mcps1.1.5.1.2"><p id="p13036348102532"><a name="p13036348102532"></a><a name="p13036348102532"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.63%" id="mcps1.1.5.1.3"><p id="p49311266102532"><a name="p49311266102532"></a><a name="p49311266102532"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.480000000000004%" id="mcps1.1.5.1.4"><p id="p34789580102532"><a name="p34789580102532"></a><a name="p34789580102532"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row66492578102532"><td class="cellrowborder" valign="top" width="20.62%" headers="mcps1.1.5.1.1 "><p id="p17189774102532"><a name="p17189774102532"></a><a name="p17189774102532"></a>SAMLResponse</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.27%" headers="mcps1.1.5.1.2 "><p id="p50194421102532"><a name="p50194421102532"></a><a name="p50194421102532"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.63%" headers="mcps1.1.5.1.3 "><p id="p492243151519"><a name="p492243151519"></a><a name="p492243151519"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.480000000000004%" headers="mcps1.1.5.1.4 "><p id="p52716491103542"><a name="p52716491103542"></a><a name="p52716491103542"></a>在IdP认证成功后返回的响应体。</p>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >该接口只支持在命令行侧调用，需要客户端使用IdP initiated的联邦认证方式获取SAMLResponse，并采用浏览器提交表单数据的方式，获取unscoped token。  

-   请求样例

    ```
    curl -i -k -H 'Accept:application/json' -H 'x-Idp-Id:test_local_idp' -H 'Content-Type:application/x-www-form-urlencoded' -X POST -d 'SAMLResponse=PD94bWwgdmVyc2lvbj0iMS4wIiBl4WXZ1OGNmYmRzWk1ZeWlLKy96anpEbm1rT2FrVVBrUmlSWEpLYUt5NzJtUmtoRFBCNjgwVQpzalU3R2hKNHE4ZG48L3hlbmM6Q2lwaGVyVmFsdWU%2BPC94ZW5jOkNpcGhlckRhdGE%2BPC94ZW5jOkVuY3J5cHRlZERhdGE%2BPC9zYW1sMjpFbmNyeXB0ZWRBc3NlcnRpb24%2BPC9zYW1sMnA6UmVzcG9uc2U%2B' https://iam.example.com/v3.0/OS-FEDERATION/tokens
    ```


## 响应<a name="section5167254164730"></a>

-   Response Body参数说明

    <a name="table30197476165124"></a>
    <table><thead align="left"><tr id="row25190343165124"><th class="cellrowborder" valign="top" width="20.54%" id="mcps1.1.5.1.1"><p id="p63550324165124"><a name="p63550324165124"></a><a name="p63550324165124"></a>名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.39%" id="mcps1.1.5.1.2"><p id="p47302590165124"><a name="p47302590165124"></a><a name="p47302590165124"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.94%" id="mcps1.1.5.1.3"><p id="p6304564165124"><a name="p6304564165124"></a><a name="p6304564165124"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.13%" id="mcps1.1.5.1.4"><p id="p40907712165124"><a name="p40907712165124"></a><a name="p40907712165124"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row31669105165124"><td class="cellrowborder" valign="top" width="20.54%" headers="mcps1.1.5.1.1 "><p id="p27151923165124"><a name="p27151923165124"></a><a name="p27151923165124"></a>X-Subject-Token</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.39%" headers="mcps1.1.5.1.2 "><p id="p51822188165124"><a name="p51822188165124"></a><a name="p51822188165124"></a>header</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.94%" headers="mcps1.1.5.1.3 "><p id="p36847705165124"><a name="p36847705165124"></a><a name="p36847705165124"></a>string</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.13%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0026585112_p51812368"><a name="zh-cn_topic_0026585112_p51812368"></a><a name="zh-cn_topic_0026585112_p51812368"></a>签名后的unscoped token。</p>
    </td>
    </tr>
    <tr id="row15598896165124"><td class="cellrowborder" valign="top" width="20.54%" headers="mcps1.1.5.1.1 "><p id="p16586493165124"><a name="p16586493165124"></a><a name="p16586493165124"></a>token</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.39%" headers="mcps1.1.5.1.2 "><p id="p1328717165124"><a name="p1328717165124"></a><a name="p1328717165124"></a>body</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.94%" headers="mcps1.1.5.1.3 "><p id="p40517270165124"><a name="p40517270165124"></a><a name="p40517270165124"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.13%" headers="mcps1.1.5.1.4 "><p id="p60673407165124"><a name="p60673407165124"></a><a name="p60673407165124"></a>联邦认证的unscoped token，包含methods和用户信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例

    ```
    {
        "token": {
            "expires_at": "2018-03-13T03:00:01.168000Z",
            "methods": ["mapped"],
            "issued_at": "2018-03-12T03:00:01.168000Z",
            "user": {
                "OS-FEDERATION": {
                    "identity_provider": {
                        "id": "test_local_idp"
                    },
                    "protocol": {
                        "id": "saml"
                    },
                    "groups": [{
                        "name": "admin",
                        "id": "45a8c8f1894444e9a016af065e152b91"
                    }]
                },
                "domain": {
                    "name": "hansheng",
                    "id": "c0e20cc993a24ad4aa3251661ef37c87"
                },
                "name": "FederationUser",
                "id": "QNSzD0bycqUXE4hiRNfyFcWfoOs8z6gT"
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
<tbody><tr id="row27991504164730"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p52719384164730"><a name="p52719384164730"></a><a name="p52719384164730"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p42411696164730"><a name="p42411696164730"></a><a name="p42411696164730"></a>请求成功，返回token。</p>
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

