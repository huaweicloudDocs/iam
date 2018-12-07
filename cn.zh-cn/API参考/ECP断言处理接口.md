# ECP断言处理接口<a name="ZH-CN_TOPIC_0110485023"></a>

## 功能介绍<a name="section46562811165510"></a>

当IAM服务担任SAML2.0规范中的SP（Service Provider，即服务提供者）角色与IdP（Identity Provider，即身份提供者）进行单点登录时，该接口用于接收AuthnRequest请求返回的响应，即客户端代理发往SP的断言请求。

关于SAML2.0规范请参阅链接：[https://en.wikipedia.org/wiki/SAML\_2.0](https://en.wikipedia.org/wiki/SAML_2.0)

>![](public_sys-resources/icon-note.gif) **说明：**   
>不建议直接调用该接口，请使用openstackclient获取token。  

## URI<a name="section273229165510"></a>

URI格式

POST /v3-ext/auth/OS-FEDERATION/SSO/SAML2/ECP

