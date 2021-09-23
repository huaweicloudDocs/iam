# 使用token方式创建云服务登录地址<a name="iam_08_1003"></a>

该章节提供使用token方式创建登录华为云云服务的联邦代理登录地址的示例代码。

## Java示例代码<a name="section1836313731719"></a>

以下示例说明了如何使用java编程的方式创建云服务登录地址FederationProxyUrl，该示例基于[华为云 Java 软件开发工具包（Java SDK）](https://github.com/huaweicloud/huaweicloud-sdk-java-v3/blob/master/README_CN.md)开发。

```
import java.net.URLEncoder;
import java.util.Collections;
import com.huaweicloud.sdk.core.auth.GlobalCredentials;
import com.huaweicloud.sdk.core.http.HttpConfig;
import com.huaweicloud.sdk.core.exception.*;
import com.huaweicloud.sdk.iam.v3.IamClient;
import com.huaweicloud.sdk.iam.v3.model.*;

//使用全局域名获取自定义代理登录票据
String endpoint = "https://iam.myhuaweicloud.com";

//配置客户端属性
HttpConfig config = HttpConfig.getDefaultHttpConfig()
		.withIgnoreSSLVerification(true)
		.withProxyHost("proxy.huawei.com")
		.withProxyPort(8080);

// 使用IAM userB的domainID/ak/sk,初始化指定IAM客户端 {Service}Client,用户B的创建方式见“创建IAM用户”章节
IamClient iamClient = IamClient.newBuilder().withCredential(new GlobalCredentials()
		.withDomainId(domainId)
		.withAk(ak)
		.withSk(sk))
		.withEndpoint(endpoint)
		.withHttpConfig(config)
		.build();

/*CreateTemporaryAccessKeyByToken
调用通过token获取临时访问密钥和securitytoken接口获取具有临时身份的访问密钥和securitytoken。
访问秘钥和securitytoken的默认有效期为900秒，即15分钟，取值范围为15分钟-24小时，这里设置有效期为3600秒，即一小时。
注意： 下一步获取自定义代理登录票据logintoken时，如果您设置了有效期，则有效期不能大于这里获取的securitytoken的剩余有效时间。
*/
TokenAuthIdentity tokenAuthIdentity = new TokenAuthIdentity().withMethods(Collections.singletonList(TokenAuthIdentity.MethodsEnum.fromValue("token"))).withToken(new IdentityToken().withDurationSeconds(3600));
CreateTemporaryAccessKeyByTokenRequestBody createTemporaryAccessKeyByTokenRequestBody = new CreateTemporaryAccessKeyByTokenRequestBody().withAuth(new TokenAuth().withIdentity(tokenAuthIdentity));
CreateTemporaryAccessKeyByTokenResponse createTemporaryAccessKeyByTokenResponse = iamClient.createTemporaryAccessKeyByToken(new CreateTemporaryAccessKeyByTokenRequest().withBody(createTemporaryAccessKeyByTokenRequestBody));
Credential credential = createTemporaryAccessKeyByTokenResponse.getCredential();

/*CreateLoginToken
获取自定义代理登录票据logintoken。
logintoken是系统颁发给自定义代理用户的登录票据，承载用户的身份、session等信息。
调用自定义代理URL登录云服务控制台时，可以使用本接口获取的logintoken进行认证。
自定义代理登录票据logintoken的有效期默认为600秒，即10分钟，取值范围为10分钟-12小时，这里设置为1800秒，即半小时。
注意：自定义代理登录票据logintoken的有效期不能大于上一步获取的securitytoken的剩余有效时间。
*/
CreateLoginTokenRequestBody createLoginTokenRequestBody = new CreateLoginTokenRequestBody().
		withAuth(new LoginTokenAuth().withSecuritytoken(new LoginTokenSecurityToken().
				withAccess(credential.getAccess()).
				withId(credential.getSecuritytoken()).
				withSecret(credential.getSecret()).withDurationSeconds(1800)));
CreateLoginTokenResponse createLoginTokenResponse = iamClient.createLoginToken(new CreateLoginTokenRequest().withBody(createLoginTokenRequestBody));
String loginToken = createLoginTokenResponse.getXSubjectLoginToken();

//获取自定义代理登录票据URL
String authURL = "https://auth.huaweicloud.com/authui/federation/login";
//企业管理系统登录地址
String enterpriseSystemLoginURL = "https://example.com/";
//需要访问的华为云服务地址
String targetConsoleURL = "https://console.huaweicloud.com/iam/?region=cn-north-4";

//创建云服务登录地址FederationProxyUrl，作为Location返回给浏览器。
String FederationProxyUrl = authURL + "?idp_login_url=" +
		URLEncoder.encode(enterpriseSystemLoginURL, "UTF-8") +
		"&service=" + URLEncoder.encode(targetConsoleURL, "UTF-8") +
		"&logintoken=" +URLEncoder.encode(loginToken, "UTF-8");
```

## Python示例代码<a name="section8721916181819"></a>

以下示例说明了如何使用Python编程的方式创建云服务登录地址FederationProxyUrl，该示例基于[华为云开发者 Python 软件开发工具包 （Python SDK）](https://github.com/huaweicloud/huaweicloud-sdk-python-v3/blob/master/README_CN.md)开发。

```
from huaweicloudsdkcore.auth.credentials import GlobalCredentials
from huaweicloudsdkcore.http.http_config import HttpConfig
from huaweicloudsdkiam.v3 import *

import urllib

# 使用全局域名获取自定义代理登录票据
endpoint = "https://iam.myhuaweicloud.com"

# 配置客户端属性
config = HttpConfig.get_default_config()
config.ignore_ssl_verification = True
config.proxy_protocol = "https"
config.proxy_host = "proxy.huawei.com"
config.proxy_port = 8080
credentials = GlobalCredentials(ak, sk, domain_id)

# 使用IAM userB的domainID/ak/sk,初始化指定IAM客户端 {Service}Client,用户B的创建方式见“创建IAM用户”章节
client = IamClient().new_builder(IamClient) \
	.with_http_config(config) \
	.with_credentials(credentials) \
	.with_endpoint(endpoint) \
	.build()

# CreateTemporaryAccessKeyByToken
# 调用通过token获取临时访问密钥和securitytoken接口获取具有临时身份的访问密钥和securityToken
# 访问秘钥和securitytoken的默认有效期为900秒，即15分钟，取值范围为15分钟-24小时，这里设置有效期为3600秒，即一小时。
# 注意： 下一步获取自定义代理登录票据logintoken时，如果您设置了有效期，则有效期不能大于这里获取的securitytoken的剩余有效时间。
identity_methods = ["token"]
identity_token = IdentityToken(duration_seconds=3600)
body = CreateTemporaryAccessKeyByTokenRequestBody(
	TokenAuth(TokenAuthIdentity(methods=identity_methods, token=identity_token)))
request = CreateTemporaryAccessKeyByTokenRequest(body)
create_temporary_access_key_by_token_response = client.create_temporary_access_key_by_token(request)
credential = create_temporary_access_key_by_token_response.credential

# CreateLoginToken
# 获取自定义代理登录票据logintoken。
# logintoken是系统颁发给自定义代理用户的登录票据，承载用户的身份、session等信息。
# 调用自定义代理URL登录云服务控制台时，可以使用本接口获取的logintoken进行认证。
# 自定义代理登录票据logintoken的有效期默认为600秒，即10分钟，取值范围为10分钟-12小时，这里设置为1800秒，即半小时。
# 注意：自定义代理登录票据logintoken的有效期不能大于上一步获取的securitytoken的剩余有效时间。
login_token_security_token = LoginTokenSecurityToken(access=credential.access, secret=credential.secret,
							id=credential.securitytoken, duration_seconds=1800)
body = CreateLoginTokenRequestBody(LoginTokenAuth(login_token_security_token))
request = CreateLoginTokenRequest(body)
create_login_token_response = client.create_login_token(request)
login_token = create_login_token_response.x_subject_login_token


#自定义代理登录地址
auth_URL = "https://auth.huaweicloud.com/authui/federation/login"
#企业管理系统登录地址
enterprise_system_login_URL = "https://example.com/"
#需要访问的华为云服务地址
target_console_URL = "https://console.huaweicloud.com/iam/?region=cn-north-4"

# 创建云服务登录地址FederationProxyUrl，作为Location返回给浏览器。
FederationProxyUrl = auth_URL + "?idp_login_url=" + urllib.parse.quote(
	enterprise_system_login_URL) + "&service=" + urllib.parse.quote(
	target_console_URL) + "&logintoken=" + urllib.parse.quote(login_token)
print(FederationProxyUrl)

```

