# 查询Keystone的Metadata文件<a name="iam_13_0503"></a>

## 功能介绍<a name="zh-cn_topic_0224276972_section19917132312500"></a>

该接口可以用于查询keystone的Metadata文件。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。IAM的Endpoint请参见：[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)。

## URI<a name="zh-cn_topic_0224276972_section13918162335012"></a>

GET /v3-ext/auth/OS-FEDERATION/SSO/metadata

## 请求参数<a name="zh-cn_topic_0224276972_section8918172311508"></a>

**表 1**  请求Header参数

<a name="zh-cn_topic_0224276972_HeaderParameter"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276972_row1991918233507"><th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.1"><p id="zh-cn_topic_0224276972_p19204231504"><a name="zh-cn_topic_0224276972_p19204231504"></a><a name="zh-cn_topic_0224276972_p19204231504"></a>参数</p>
</th>
<th class="cellrowborder" valign="top" width="20%" id="mcps1.2.5.1.2"><p id="zh-cn_topic_0224276972_p792116238508"><a name="zh-cn_topic_0224276972_p792116238508"></a><a name="zh-cn_topic_0224276972_p792116238508"></a>是否必选</p>
</th>
<th class="cellrowborder" valign="top" width="10%" id="mcps1.2.5.1.3"><p id="zh-cn_topic_0224276972_p18921202365015"><a name="zh-cn_topic_0224276972_p18921202365015"></a><a name="zh-cn_topic_0224276972_p18921202365015"></a>参数类型</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.2.5.1.4"><p id="zh-cn_topic_0224276972_p159226237506"><a name="zh-cn_topic_0224276972_p159226237506"></a><a name="zh-cn_topic_0224276972_p159226237506"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276972_row0919823205010"><td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.1 "><p id="zh-cn_topic_0224276972_p692222305015"><a name="zh-cn_topic_0224276972_p692222305015"></a><a name="zh-cn_topic_0224276972_p692222305015"></a>unsigned</p>
</td>
<td class="cellrowborder" valign="top" width="20%" headers="mcps1.2.5.1.2 "><p id="zh-cn_topic_0224276972_p10923112365015"><a name="zh-cn_topic_0224276972_p10923112365015"></a><a name="zh-cn_topic_0224276972_p10923112365015"></a>否</p>
</td>
<td class="cellrowborder" valign="top" width="10%" headers="mcps1.2.5.1.3 "><p id="zh-cn_topic_0224276972_p092312311507"><a name="zh-cn_topic_0224276972_p092312311507"></a><a name="zh-cn_topic_0224276972_p092312311507"></a>Boolean</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.2.5.1.4 "><p id="zh-cn_topic_0224276972_p4923823145016"><a name="zh-cn_topic_0224276972_p4923823145016"></a><a name="zh-cn_topic_0224276972_p4923823145016"></a>是否按SAML2.0规范对元数据做签名，默认为false。</p>
</td>
</tr>
</tbody>
</table>

## 响应参数<a name="zh-cn_topic_0224276972_section10924523115013"></a>

无

## 请求示例<a name="zh-cn_topic_0224276972_section592414239501"></a>

```
GET https://iam.myhuaweicloud.com/v3-ext/auth/OS-FEDERATION/SSO/metadata
```

## 响应示例<a name="zh-cn_topic_0224276972_section15925192319505"></a>

**状态码为 200 时:**

请求成功。

```
<?xml version="1.0" encoding="UTF-8"?>
<md:EntityDescriptor ID="Mc106d5b14b70a4945fa270d8b52d0ed" entityID="https://iam.myhuaweicloud.com" xmlns:md="urn:oasis:names:tc:SAML:2.0:metadata">
    <ds:Signature xmlns:ds="http://www.w3.org/2000/09/xmldsig#">
        <ds:SignedInfo>
            <ds:CanonicalizationMethod Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#"/>
            <ds:SignatureMethod Algorithm="http://www.w3.org/2001/04/xmldsig-more#rsa-sha256"/>
            <ds:Reference URI="#Mc106d5b14b70a4945fa270d8b52d0ed">
                <ds:Transforms>
                    <ds:Transform Algorithm="http://www.w3.org/2000/09/xmldsig#enveloped-signature"/>
                    <ds:Transform Algorithm="http://www.w3.org/2001/10/xml-exc-c14n#"/>
                </ds:Transforms>
                <ds:DigestMethod Algorithm="http://www.w3.org/2000/09/xmldsig#sha1"/>
                <ds:DigestValue>GmS+Nvta/AvNy4fE7dFID5D+P1U=</ds:DigestValue>
            </ds:Reference>
        </ds:SignedInfo>
        <ds:SignatureValue>ljRL...</ds:SignatureValue>
        <ds:KeyInfo>
            <ds:X509Data>
                <ds:X509Certificate>MIIC...</ds:X509Certificate>
            </ds:X509Data>
        </ds:KeyInfo>
    </ds:Signature>
    <md:SPSSODescriptor WantAssertionsSigned="true" protocolSupportEnumeration="urn:oasis:names:tc:SAML:2.0:protocol">
        <md:KeyDescriptor use="signing">
            <ds:KeyInfo xmlns:ds="http://www.w3.org/2000/09/xmldsig#">
                <ds:X509Data>
                    <ds:X509Certificate>MIIC...</ds:X509Certificate>
                </ds:X509Data>
            </ds:KeyInfo>
        </md:KeyDescriptor>
        <md:KeyDescriptor use="encryption">
            <ds:KeyInfo xmlns:ds="http://www.w3.org/2000/09/xmldsig#">
                <ds:X509Data>
                    <ds:X509Certificate>MIIC...</ds:X509Certificate>
                </ds:X509Data>
            </ds:KeyInfo>
        </md:KeyDescriptor>
        <md:NameIDFormat xmlns:md="urn:oasis:names:tc:SAML:2.0:metadata">urn:oasis:names:tc:SAML:2.0:nameid-format:transient</md:NameIDFormat>
        <md:AssertionConsumerService Binding="urn:oasis:names:tc:SAML:2.0:bindings:HTTP-POST" Location="https://iam.myhuaweicloud.com/v3-ext/auth/OS-FEDERATION/SSO/SAML2/POST" index="0" isDefault="true" xmlns:md="urn:oasis:names:tc:SAML:2.0:metadata"/>
        <md:AssertionConsumerService Binding="urn:oasis:names:tc:SAML:2.0:bindings:PAOS" Location="https://iam.myhuaweicloud.com/v3-ext/auth/OS-FEDERATION/SSO/SAML2/ECP" index="1" xmlns:md="urn:oasis:names:tc:SAML:2.0:metadata"/>
    </md:SPSSODescriptor>
</md:EntityDescriptor>
```

## 返回值<a name="zh-cn_topic_0224276972_section392752305013"></a>

<a name="zh-cn_topic_0224276972_table4328"></a>
<table><thead align="left"><tr id="zh-cn_topic_0224276972_row1892872317506"><th class="cellrowborder" valign="top" width="15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0224276972_p692942375014"><a name="zh-cn_topic_0224276972_p692942375014"></a><a name="zh-cn_topic_0224276972_p692942375014"></a>返回值</p>
</th>
<th class="cellrowborder" valign="top" width="85%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0224276972_p3930323195011"><a name="zh-cn_topic_0224276972_p3930323195011"></a><a name="zh-cn_topic_0224276972_p3930323195011"></a>描述</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0224276972_row2928523155017"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276972_p169306239501"><a name="zh-cn_topic_0224276972_p169306239501"></a><a name="zh-cn_topic_0224276972_p169306239501"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276972_p39309235505"><a name="zh-cn_topic_0224276972_p39309235505"></a><a name="zh-cn_topic_0224276972_p39309235505"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276972_row292812236507"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276972_p1593117237504"><a name="zh-cn_topic_0224276972_p1593117237504"></a><a name="zh-cn_topic_0224276972_p1593117237504"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276972_p1193142315020"><a name="zh-cn_topic_0224276972_p1193142315020"></a><a name="zh-cn_topic_0224276972_p1193142315020"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0224276972_row2928923195016"><td class="cellrowborder" valign="top" width="15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0224276972_p18932112315502"><a name="zh-cn_topic_0224276972_p18932112315502"></a><a name="zh-cn_topic_0224276972_p18932112315502"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="85%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276972_p593392345012"><a name="zh-cn_topic_0224276972_p593392345012"></a><a name="zh-cn_topic_0224276972_p593392345012"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

## 错误码<a name="zh-cn_topic_0224276972_section1393316230506"></a>

无

