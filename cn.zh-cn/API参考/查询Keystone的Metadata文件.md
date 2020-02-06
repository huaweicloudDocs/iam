# 查询Keystone的Metadata文件<a name="zh-cn_topic_0057845577"></a>

## 功能介绍<a name="section5290716016471"></a>

该接口用于查询keystone的Metadata文件。

该接口可以使用全局区域的域名和其他区域的域名调用，全局区域的域名为iam.myhuaweicloud.com。

## URI<a name="section6523849916310"></a>

URI格式

GET /v3-ext/auth/OS-FEDERATION/SSO/metadata

## 请求<a name="section3867762216471"></a>

-   Request Header参数说明

    <a name="table4721442116350"></a>
    <table><thead align="left"><tr id="row4043595516350"><th class="cellrowborder" valign="top" width="17.478252174782526%" id="mcps1.1.5.1.1"><p id="p3628647916350"><a name="p3628647916350"></a><a name="p3628647916350"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.858214178582145%" id="mcps1.1.5.1.2"><p id="p5352366316350"><a name="p5352366316350"></a><a name="p5352366316350"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.23807619238076%" id="mcps1.1.5.1.3"><p id="p4044945616350"><a name="p4044945616350"></a><a name="p4044945616350"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="45.42545745425458%" id="mcps1.1.5.1.4"><p id="p5518050516350"><a name="p5518050516350"></a><a name="p5518050516350"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row4351522316350"><td class="cellrowborder" valign="top" width="17.478252174782526%" headers="mcps1.1.5.1.1 "><p id="p5408695016350"><a name="p5408695016350"></a><a name="p5408695016350"></a>unsigned</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.858214178582145%" headers="mcps1.1.5.1.2 "><p id="p1896680916350"><a name="p1896680916350"></a><a name="p1896680916350"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.23807619238076%" headers="mcps1.1.5.1.3 "><p id="p5991653216350"><a name="p5991653216350"></a><a name="p5991653216350"></a>Boolean</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.42545745425458%" headers="mcps1.1.5.1.4 "><p id="p2140092816350"><a name="p2140092816350"></a><a name="p2140092816350"></a>是否按SAML2.0规范，对元数据做签名，默认为<span class="parmvalue" id="parmvalue498614598404"><a name="parmvalue498614598404"></a><a name="parmvalue498614598404"></a>“false”</span>。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   请求样例

    ```
    GET /v3-ext/auth/OS-FEDERATION/SSO/metadata
    ```


## 响应<a name="section35305061164019"></a>

响应样例

```
<md:EntityDescriptor xmlns:md="urn:oasis:names:tc:SAML:2.0:metadata" ID="43ebac773925f6849b196a3c803baba5" entityID="https://www.example.com">
<ds:Signature xmlns:ds="http://www.w3.org/2000/09/xmldsig#">
<ds:SignedInfo>
<ds:CanonicalizationMethod Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#"/>
<ds:SignatureMethod Algorithm="http://www.w3.org/2000/09/xmldsig#rsa-sha1"/>
<ds:Reference URI="#43ebac773925f6849b196a3c803baba5">
<ds:Transforms>
<ds:Transform Algorithm="http://www.w3.org/2000/09/xmldsig#enveloped-signature"/>
<ds:Transform Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#"/>
</ds:Transforms>
<ds:DigestMethod Algorithm="http://www.w3.org/2000/09/xmldsig#sha1"/>
<ds:DigestValue>yuQJc6OI3xilt6X4cOEUBnVV2Vs=</ds:DigestValue>
</ds:Reference>
</ds:SignedInfo>
<ds:SignatureValue>...</ds:SignatureValue>
<ds:KeyInfo>
<ds:X509Data>
<ds:X509Certificate>...</ds:X509Certificate>
</ds:X509Data>
</ds:KeyInfo>
</ds:Signature>
<md:SPSSODescriptor AuthnRequestsSigned="true" WantAssertionsSigned="true" protocolSupportEnumeration="urn:oasis:names:tc:SAML:2.0:protocol">
<md:KeyDescriptor use="signing">
<ds:KeyInfo xmlns:ds="http://www.w3.org/2000/09/xmldsig#">
<ds:X509Data>
<ds:X509Certificate>...</ds:X509Certificate>
</ds:X509Data>
</ds:KeyInfo>
</md:KeyDescriptor>
<md:KeyDescriptor use="encryption">
<ds:KeyInfo xmlns:ds="http://www.w3.org/2000/09/xmldsig#">
<ds:X509Data>
<ds:X509Certificate>...</ds:X509Certificate>
</ds:X509Data>
</ds:KeyInfo>
</md:KeyDescriptor>
<md:NameIDFormat xmlns:md="urn:oasis:names:tc:SAML:2.0:metadata">
urn:oasis:names:tc:SAML:2.0:nameid-format:transient
</md:NameIDFormat>
<md:AssertionConsumerService xmlns:md="urn:oasis:names:tc:SAML:2.0:metadata" Binding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-POST" Location="https://www.example.com/v3-ext/auth/OS-FEDERATION/SSO/SAML2/POST" index="0" isDefault="true"/>
<md:AssertionConsumerService xmlns:md="urn:oasis:names:tc:SAML:2.0:metadata" Binding="urn:oasis:names:tc:SAML:2.0:bindings:PAOS" Location="https://www.example.com/v3-ext/auth/OS-FEDERATION/SSO/SAML2/ECP" index="1"/>
</md:SPSSODescriptor>
</md:EntityDescriptor>
```

## 状态码<a name="section1813979416471"></a>

<a name="table6003723016471"></a>
<table><thead align="left"><tr id="row4559823416471"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="p246947316471"><a name="p246947316471"></a><a name="p246947316471"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="p6580961616471"><a name="p6580961616471"></a><a name="p6580961616471"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2897870416471"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p6557370516471"><a name="p6557370516471"></a><a name="p6557370516471"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p986985816471"><a name="p986985816471"></a><a name="p986985816471"></a>请求成功。</p>
</td>
</tr>
<tr id="row2171985816471"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p1447804616471"><a name="p1447804616471"></a><a name="p1447804616471"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p3187110316471"><a name="p3187110316471"></a><a name="p3187110316471"></a>内部服务错误。</p>
</td>
</tr>
<tr id="row1840447916471"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="p1436785016471"><a name="p1436785016471"></a><a name="p1436785016471"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="p2294521416471"><a name="p2294521416471"></a><a name="p2294521416471"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

