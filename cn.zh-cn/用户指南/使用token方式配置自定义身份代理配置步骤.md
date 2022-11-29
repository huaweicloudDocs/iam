# 使用token方式配置自定义身份代理配置步骤<a name="iam_08_1005"></a>

如果您的企业IdP不支持SAML、OIDC协议，可以使用自定义身份代理，通过编写代码获得华为云登录链接，使企业用户通过企业IdP验证身份后，即可登录华为云。

>![](public_sys-resources/icon-note.gif) **说明：** 
>自定义身份代理适用于不支持SAML、OIDC的企业IdP，如果您使用了支持SAML、OIDC的IdP（身份提供商），推荐您通过配置[联邦身份认证](联邦身份认证配置概述.md)实现用户使用企业管理系统帐号单点登录华为云。

## 前提条件<a name="section2089016116416"></a>

-   企业已有企业管理系统。
-   企业管理员在华为云上注册了可用的帐号（帐号名以DomainA为例）。

## 操作步骤<a name="section929104317167"></a>

1.  在DomainA中创建IAM用户（用户名以UserB为例），具体方法请参见：[创建IAM用户](创建IAM用户.md)。
2.  （可选）将用户UserB加入用户组中（用户组名以GroupC为例），并为用户组授予必要的权限，具体方法请参见：[创建用户组并授权](创建用户组并授权.md)
3.  <a name="zh-cn_topic_0185387373_li5651420111115"></a>将UserB的[访问密钥](https://support.huaweicloud.com/usermanual-ca/ca_01_0003.html)或用户名和密码（推荐使用访问密钥）配置到企业IdP的配置文件中，以便获取用户认证token。为了保障您的帐号安全，密码和访问密钥建议加密存储。
4.  企业管理员登录企业管理系统后，访问自定义代理，从用户列表中选择需要登录华为云的企业用户，具体操作请参见企业管理系统帮助文档。此处以企业管理员选择[2](#zh-cn_topic_0185387373_li5651420111115)中配置的用户UserB为例。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >自定义代理的用户列表是在华为云帐号下的IAM用户列表，将IAM用户的[访问密钥](https://support.huaweicloud.com/usermanual-ca/ca_01_0003.html)或用户名和密码（推荐使用访问密钥）配置到企业IdP的配置文件中，即可将这些用户按需赋予不同企业用户。

5.  企业IdP自定义代理携带IAM用户UserB的token调用API（POST /v3.0/OS-CREDENTIAL/securitytokens），获取临时访问密钥和securityToken，调用方法请参见：[通过token获取临时访问密钥和securitytoken](https://support.huaweicloud.com/zh-cn/api-iam/iam_04_0002.html)。
6.  企业IdP自定义代理携带获取到的临时访问密钥和securitytoken通过全局域名（iam.myhuaweicloud.com）调用API（POST /v3.0/OS-AUTH/securitytoken/logintokens）获取登录票据loginToken。登录票据位于Response Header中的X-Subject-LoginToken。获取方式请参见：[获取自定义代理登录票据](https://support.huaweicloud.com/api-iam/iam_14_1101.html)。

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >-   调用API（POST /v3.0/OS-AUTH/securitytoken/logintokens）获取登录票据loginToken时，需要使用全局域名：iam.myhuaweicloud.com。
    >-   logintoken是系统颁发给自定义代理用户的登录票据，承载用户的身份、session等信息，默认有效期为10分钟。
    >-   调用API（POST /v3.0/OS-AUTH/securitytoken/logintokens）时可以设置logintoken的有效时间，有效时间设置范围为10分钟\~12小时。如果传入的值大于临时安全凭证securitytoken剩余的过期时间，则使用临时安全凭证securitytoken剩余的过期时间。

7.  企业IdP自定义代理根据如下规范创建云服务代理登录地址，并作为Location返回给浏览器：

    ```
    https://auth.huaweicloud.com/authui/federation/login?idp_login_url={enterprise_system_loginURL}&service={console_service_region_url}&logintoken={logintoken}
    ```

    **示例：**

    ```
    https://auth.huaweicloud.com/authui/federation/login?idp_login_url=https%3A%2F%2Fexample.com&service=https%3a%2f%2fconsole.huaweicloud.com%2fapm%2f%3fregion%3dcn-north-4%23%2fapm%2fatps%2ftopology&logintoken=******
    ```

    **表 1**  参数说明

    <a name="table105201138141210"></a>
    <table><thead align="left"><tr id="row95631538111214"><th class="cellrowborder" valign="top" width="23.46%" id="mcps1.2.3.1.1"><p id="p1056383811122"><a name="p1056383811122"></a><a name="p1056383811122"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="76.53999999999999%" id="mcps1.2.3.1.2"><p id="p1856393831211"><a name="p1856393831211"></a><a name="p1856393831211"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row11563103831211"><td class="cellrowborder" valign="top" width="23.46%" headers="mcps1.2.3.1.1 "><p id="p185631384122"><a name="p185631384122"></a><a name="p185631384122"></a>idp_login_url</p>
    </td>
    <td class="cellrowborder" valign="top" width="76.53999999999999%" headers="mcps1.2.3.1.2 "><p id="p1456303810125"><a name="p1456303810125"></a><a name="p1456303810125"></a>企业管理系统登录地址。</p>
    </td>
    </tr>
    <tr id="row15631038151213"><td class="cellrowborder" valign="top" width="23.46%" headers="mcps1.2.3.1.1 "><p id="p95632385127"><a name="p95632385127"></a><a name="p95632385127"></a>service</p>
    </td>
    <td class="cellrowborder" valign="top" width="76.53999999999999%" headers="mcps1.2.3.1.2 "><p id="p155631838171217"><a name="p155631838171217"></a><a name="p155631838171217"></a>需要访问的华为云服务地址。</p>
    </td>
    </tr>
    <tr id="row356333851212"><td class="cellrowborder" valign="top" width="23.46%" headers="mcps1.2.3.1.1 "><p id="p1756318382127"><a name="p1756318382127"></a><a name="p1756318382127"></a>logintoken</p>
    </td>
    <td class="cellrowborder" valign="top" width="76.53999999999999%" headers="mcps1.2.3.1.2 "><p id="p8563738181214"><a name="p8563738181214"></a><a name="p8563738181214"></a>自定义代理登录票据。</p>
    </td>
    </tr>
    </tbody>
    </table>

    您可以参考以下Demo示例创建云服务登录地址：[使用token方式创建云服务登录地址](使用token方式创建云服务登录地址.md)

    >![](public_sys-resources/icon-note.gif) **说明：** 
    >云服务代理登录地址中包含从IAM获得的登录票据loginToken，loginToken用于对访问的用户进行身份验证。云服务代理登录地址中每个参数的值都需要经过UrlEncode编码。

8.  华为云认证登录票据loginToken成功后，浏览器自动重定向到需要访问的华为云服务地址，即云服务代理登录地址中**service**设定的地址，企业用户成功访问华为云的控制台。

    loginToken认证失败，则重定向到**idp\_login\_url**设定的地址。


