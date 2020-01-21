# 获取用户Token<a name="zh-cn_topic_0057845583"></a>

## 功能介绍<a name="s5888597838b0425a92e3419fb766c7f5"></a>

该接口通过用户名/密码的方式进行认证，用来获取用户自身的Token，可以获取Token的用户包括账号本身以及账号下的用户。Token是系统颁发给用户的访问令牌，承载用户的身份、权限等信息。调用IAM以及其他云服务的接口时，可以使用本接口获取的token进行鉴权。

该接口可以使用全局区域的Endpoint和其他区域的Endpoint调用。如果使用全局区域的Endpoint调用，该token可以在所有区域使用。如果使用区域的Endpoint调用，该token仅在该区域生效，不能跨区域使用。IAM的Endpoint请参见：[终端节点](使用前必读.md#section1661773463712)。

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   Token的有效期为24小时，需要使用一个Token鉴权时，可以先缓存起来，避免频繁调用。  
>-   获取用户Token示例，请参见：[如何通过Postman获取用户Token](https://support.huaweicloud.com/iam_faq/iam_01_034.html)。  
>-   如果需要获取具有Security Administrator权限的Token，请参见：[IAM 常见问题](https://support.huaweicloud.com/iam_faq/iam_01_0608.html)。  

## URI<a name="s46d3616bd4c54e55ba97a528518a5890"></a>

URI格式

POST /v3/auth/tokens

## 请求<a name="se7fe5cac0d544e119c49322cc1707eb6"></a>

-   Request Header参数说明

    <a name="t68c7bd10e66a4380a1e6cdc78ca95669"></a>
    <table><thead align="left"><tr id="r584496594a404ce18918a40e6e57c2ec"><th class="cellrowborder" valign="top" width="18.95810418958104%" id="mcps1.1.5.1.1"><p id="ac3a989cc5d3a405889eabb47dee84b04"><a name="ac3a989cc5d3a405889eabb47dee84b04"></a><a name="ac3a989cc5d3a405889eabb47dee84b04"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.42835716428357%" id="mcps1.1.5.1.2"><p id="a69a20ac00b86496aa8418517c542b0da"><a name="a69a20ac00b86496aa8418517c542b0da"></a><a name="a69a20ac00b86496aa8418517c542b0da"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.108189181081894%" id="mcps1.1.5.1.3"><p id="a92c23d4441054df0972e025aeb3a8d7f"><a name="a92c23d4441054df0972e025aeb3a8d7f"></a><a name="a92c23d4441054df0972e025aeb3a8d7f"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.5053494650535%" id="mcps1.1.5.1.4"><p id="abe6882c44cf4402d8ed7706b9278f33b"><a name="abe6882c44cf4402d8ed7706b9278f33b"></a><a name="abe6882c44cf4402d8ed7706b9278f33b"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r5d63069d6a8a426e8b25b94d1b4d302a"><td class="cellrowborder" valign="top" width="18.95810418958104%" headers="mcps1.1.5.1.1 "><p id="ad4fb6253385c46ab8720a0e13f573694"><a name="ad4fb6253385c46ab8720a0e13f573694"></a><a name="ad4fb6253385c46ab8720a0e13f573694"></a>Content-Type</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.42835716428357%" headers="mcps1.1.5.1.2 "><p id="a6b33800bcb2a446695b1d33a2d751554"><a name="a6b33800bcb2a446695b1d33a2d751554"></a><a name="a6b33800bcb2a446695b1d33a2d751554"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.108189181081894%" headers="mcps1.1.5.1.3 "><p id="ab34a5e95b76b4b79a72da0734025f211"><a name="ab34a5e95b76b4b79a72da0734025f211"></a><a name="ab34a5e95b76b4b79a72da0734025f211"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.5053494650535%" headers="mcps1.1.5.1.4 "><p id="a716277ae541d4553bb10490f9c02593d"><a name="a716277ae541d4553bb10490f9c02593d"></a><a name="a716277ae541d4553bb10490f9c02593d"></a>该字段内容填为<span class="parmvalue" id="parmvalue17258191372713"><a name="parmvalue17258191372713"></a><a name="parmvalue17258191372713"></a>“application/json;charset=utf8”</span>。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   查询参数说明

    <a name="tb63966ba606d4ce4b360f40a653abff8"></a>
    <table><thead align="left"><tr id="re1669fb2a3c9480bb3a00c0dd34cfc26"><th class="cellrowborder" valign="top" width="18.891889188918892%" id="mcps1.1.5.1.1"><p id="ad1f8f00641de4d56931fab6c023ee27c"><a name="ad1f8f00641de4d56931fab6c023ee27c"></a><a name="ad1f8f00641de4d56931fab6c023ee27c"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.64176417641764%" id="mcps1.1.5.1.2"><p id="a7a0e922d4ac64a23a8ee0149912e026c"><a name="a7a0e922d4ac64a23a8ee0149912e026c"></a><a name="a7a0e922d4ac64a23a8ee0149912e026c"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.581758175817583%" id="mcps1.1.5.1.3"><p id="a3fca62cae08b4adcaba323f7f3ad866e"><a name="a3fca62cae08b4adcaba323f7f3ad866e"></a><a name="a3fca62cae08b4adcaba323f7f3ad866e"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="45.88458845884588%" id="mcps1.1.5.1.4"><p id="a0cfd690722644009b8bc0cb94a5a9327"><a name="a0cfd690722644009b8bc0cb94a5a9327"></a><a name="a0cfd690722644009b8bc0cb94a5a9327"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="rd8377b31aedb40a6ac2c78ec645295bb"><td class="cellrowborder" valign="top" width="18.891889188918892%" headers="mcps1.1.5.1.1 "><p id="ab3f196e612a04b36898fca5391c8c71c"><a name="ab3f196e612a04b36898fca5391c8c71c"></a><a name="ab3f196e612a04b36898fca5391c8c71c"></a>nocatalog</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.64176417641764%" headers="mcps1.1.5.1.2 "><p id="ab701027c99914d0aa8bb847a8df6dd5e"><a name="ab701027c99914d0aa8bb847a8df6dd5e"></a><a name="ab701027c99914d0aa8bb847a8df6dd5e"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.581758175817583%" headers="mcps1.1.5.1.3 "><p id="a5fee45d14b11467e90c3ae4231a1c771"><a name="a5fee45d14b11467e90c3ae4231a1c771"></a><a name="a5fee45d14b11467e90c3ae4231a1c771"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="45.88458845884588%" headers="mcps1.1.5.1.4 "><p id="a2c20ed7477cd4f059a3ea425cc7371d0"><a name="a2c20ed7477cd4f059a3ea425cc7371d0"></a><a name="a2c20ed7477cd4f059a3ea425cc7371d0"></a>如果设置该参数，返回的响应体中将不显示catalog信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

    本接口功能为获取Token，因此调用该接口时，请求头中不用填写“X-Auth-Token”字段，只添加“Content-Type“即可，添加消息头后的请求如下所示。

    ```
    POST https://iam.cn-north-1.myhuaweicloud.com/v3/auth/tokens?nocatalog=true
    ```

-   Request Body参数说明

    <a name="table1472672314012"></a>
    <table><thead align="left"><tr id="row372613231901"><th class="cellrowborder" valign="top" width="18.04%" id="mcps1.1.5.1.1"><p id="p127271523609"><a name="p127271523609"></a><a name="p127271523609"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.51%" id="mcps1.1.5.1.2"><p id="p10727523607"><a name="p10727523607"></a><a name="p10727523607"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.07%" id="mcps1.1.5.1.3"><p id="p672717232020"><a name="p672717232020"></a><a name="p672717232020"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.379999999999995%" id="mcps1.1.5.1.4"><p id="p4727142310020"><a name="p4727142310020"></a><a name="p4727142310020"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row117274231708"><td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.1.5.1.1 "><p id="p117271323403"><a name="p117271323403"></a><a name="p117271323403"></a>identity</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.51%" headers="mcps1.1.5.1.2 "><p id="p07279236010"><a name="p07279236010"></a><a name="p07279236010"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.07%" headers="mcps1.1.5.1.3 "><p id="p1072715231201"><a name="p1072715231201"></a><a name="p1072715231201"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.379999999999995%" headers="mcps1.1.5.1.4 "><p id="p12733551037"><a name="p12733551037"></a><a name="p12733551037"></a>认证参数，包含：methods，password。</p>
    <pre class="screen" id="screen4242448102819"><a name="screen4242448102819"></a><a name="screen4242448102819"></a>"identity": {
          "methods": ["password"],
          "password": {</pre>
    </td>
    </tr>
    <tr id="row14766951175411"><td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.1.5.1.1 "><p id="p81848145559"><a name="p81848145559"></a><a name="p81848145559"></a>methods</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.51%" headers="mcps1.1.5.1.2 "><p id="p19184101415559"><a name="p19184101415559"></a><a name="p19184101415559"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.07%" headers="mcps1.1.5.1.3 "><p id="p8184131410553"><a name="p8184131410553"></a><a name="p8184131410553"></a>String Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.379999999999995%" headers="mcps1.1.5.1.4 "><p id="p101851414175513"><a name="p101851414175513"></a><a name="p101851414175513"></a>认证方法，该字段内容为<span class="parmvalue" id="parmvalue1718519140554"><a name="parmvalue1718519140554"></a><a name="parmvalue1718519140554"></a>“password”</span>。如果用户开启了虚拟MFA设备的登录保护功能时，该字段内容为[“password”,"totp"]</p>
    </td>
    </tr>
    <tr id="row102161954175410"><td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.1.5.1.1 "><p id="p31853141551"><a name="p31853141551"></a><a name="p31853141551"></a>password</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.51%" headers="mcps1.1.5.1.2 "><p id="p41851214175516"><a name="p41851214175516"></a><a name="p41851214175516"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.07%" headers="mcps1.1.5.1.3 "><p id="p6185514205514"><a name="p6185514205514"></a><a name="p6185514205514"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.379999999999995%" headers="mcps1.1.5.1.4 "><p id="p171859142556"><a name="p171859142556"></a><a name="p171859142556"></a>认证信息，示例：</p>
    <pre class="screen" id="screen19185191413550"><a name="screen19185191413550"></a><a name="screen19185191413550"></a>"password": {
            "user": {
              "name": "<em id="i15909184182615"><a name="i15909184182615"></a><a name="i15909184182615"></a>James</em>",
              "password": "<em id="i461013131265"><a name="i461013131265"></a><a name="i461013131265"></a>**********</em>",
              "domain": {
                "name": "<em id="i828662272616"><a name="i828662272616"></a><a name="i828662272616"></a>A-Company</em>"</pre>
    <a name="ul2147135719418"></a><a name="ul2147135719418"></a><ul id="ul2147135719418"><li>user.name<em id="i1818514149552"><a name="i1818514149552"></a><a name="i1818514149552"></a>：</em>用户名称，根据获取token的主体填写。</li><li>password<em id="i41861514195510"><a name="i41861514195510"></a><a name="i41861514195510"></a>：</em>用户的登录密码。</li><li>domain.name<em id="i2185171455519"><a name="i2185171455519"></a><a name="i2185171455519"></a>：</em>用户所属的账号名称。如果是账号获取token，账号的user.name和domain.name相同，此处填写user.name即可。否则此处填写用户所属的账号名称。</li></ul>
    <div class="note" id="note397091844418"><a name="note397091844418"></a><a name="note397091844418"></a><span class="notetitle"> 说明： </span><div class="notebody"><a name="ul434294114414"></a><a name="ul434294114414"></a><ul id="ul434294114414"><li>user.name和domain.name可以在界面控制台“我的凭证”中查看，具体获取方法请参见：<a href="获取IAM用户-项目-用户组的名称和ID.md">获取IAM用户、项目、用户组的名称和ID</a>。</li><li>如果是第三方系统用户，直接使用联邦认证的用户名和密码获取token，系统会提示密码错误。需要在华为云的登录页面，通过“忘记密码”功能，在华为云中设置登录密码，并在password中输入新设置的密码。</li><li>该接口提供了锁定机制用于防止暴力破解，调用时，请确保用户名密码正确，输错一定次数（管理员可设置该规则）将被锁定。</li></ul>
    </div></div>
    </td>
    </tr>
    <tr id="row1135014915519"><td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.1.5.1.1 "><p id="p618618143556"><a name="p618618143556"></a><a name="p618618143556"></a>totp</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.51%" headers="mcps1.1.5.1.2 "><p id="p1818641419559"><a name="p1818641419559"></a><a name="p1818641419559"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.07%" headers="mcps1.1.5.1.3 "><p id="p618651417559"><a name="p618651417559"></a><a name="p618651417559"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.379999999999995%" headers="mcps1.1.5.1.4 "><p id="p4186114115512"><a name="p4186114115512"></a><a name="p4186114115512"></a>认证信息，仅在您开启了虚拟MFA方式的登录保护功能时，该参数需要填写。</p>
    <p id="p10186414155519"><a name="p10186414155519"></a><a name="p10186414155519"></a>示例：</p>
    <pre class="screen" id="screen01571135184615"><a name="screen01571135184615"></a><a name="screen01571135184615"></a>"totp": {
            "user": {
              "id": "b95b78b67fa045b38104c12fb...",
              "passcode": "******"</pre>
    <a name="ul85041943518"></a><a name="ul85041943518"></a><ul id="ul85041943518"><li>user.id：用户ID，获取方法请参见<a href="获取IAM用户-项目-用户组的名称和ID.md">获取IAM用户、项目、用户组的名称和ID</a>。</li><li>passcode：虚拟MFA验证码，在MFA应用程序中获取动态验证码。</li></ul>
    </td>
    </tr>
    <tr id="row77278232020"><td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.1.5.1.1 "><p id="p124182557111"><a name="p124182557111"></a><a name="p124182557111"></a>scope</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.51%" headers="mcps1.1.5.1.2 "><p id="p144209551918"><a name="p144209551918"></a><a name="p144209551918"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.07%" headers="mcps1.1.5.1.3 "><p id="p144236557120"><a name="p144236557120"></a><a name="p144236557120"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.379999999999995%" headers="mcps1.1.5.1.4 "><p id="p8397345145417"><a name="p8397345145417"></a><a name="p8397345145417"></a>token的使用范围，取值为project或domain，二选一即可。</p>
    <a name="ul32091543195912"></a><a name="ul32091543195912"></a><ul id="ul32091543195912"><li>示例1：取值为project时，表示获取的token仅能访问指定project下的资源，project支持id和name，二选一即可。<pre class="screen" id="screen842664845912"><a name="screen842664845912"></a><a name="screen842664845912"></a>"scope": {
          "project": {
          "id": "0b95b78b67fa045b38104c12fb..."
          "name": "cn-north-1_"
          }
        }</pre>
    <div class="note" id="note1426185318212"><a name="note1426185318212"></a><a name="note1426185318212"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1463954416188"><a name="p1463954416188"></a><a name="p1463954416188"></a>使用区域的Endpoint（非全局域名）调用该接口时，推荐您将scope设置为project，该参数需要填入对应区域project的name或者id。</p>
    </div></div>
    </li><li>示例2：取值为domain时，表示获取的Token可以跨区域使用，domain支持id和name，二选一即可。<pre class="screen" id="screen59171740125811"><a name="screen59171740125811"></a><a name="screen59171740125811"></a>"scope": {
          "domain": {
          "id": "6b8eb224c76842e3ac2..."
          "name": "A-Company"
          }
        }</pre>
    <div class="note" id="note5433164615164"><a name="note5433164615164"></a><a name="note5433164615164"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p993392661712"><a name="p993392661712"></a><a name="p993392661712"></a>使用全局区域的Endpoint调用该接口时，推荐您将scope设置为domain，该token可以跨区域使用，如果将scope设置为project，该token仅能在指定的project中使用，不能跨区域使用。</p>
    </div></div>
    </li></ul>
    </td>
    </tr>
    </tbody>
    </table>

-   请求样例

    获取用户名为James，登录密码为“\*\*\*\*\*\*\*\*\*\*”，所属账号名为A-Company，作用范围为整个账号的token。

    ```
    {
      "auth": {
        "identity": {
          "methods": ["password"],
          "password": {
            "user": {
              "name": "James",
              "password": "**********",
              "domain": {
                "name": "A-Company"
              }
            }
          }
        },
        "scope": {
          "domain": {
            "name": "A-Company"
          }
        }
      }
    }
    ```

    获取用户名为James，登录密码为“\*\*\*\*\*\*\*\*\*\*”，所属账号名为A-Company，作用范围为指定project的token。

    ```
    {
      "auth": {
        "identity": {
          "methods": ["password"],
          "password": {
            "user": {
              "name": "James",
              "password": "**********",
              "domain": {
                "name": "A-Company"
              }
            }
          }
        },
        "scope": {
          "project": {
            "name": "cn-north-1"
          }
        }
      }
    }
    ```

    开启虚拟MFA方式登录保护时获取token的请求样例。

    ```
    {
    	"auth": {
    		"identity": {
    			"methods": ["password", "totp"],
    			"password": {
    				"user": {
    					"name": "James",
    					"password": "********",
    					"domain": {
    						"name": "A-Company"
    					}
    				}
    			},
    			"totp" : {
    				"user": {
    					"id": "dfsafdfsaf....",
    					"passcode": "******"
    				}
    			}
    		},
    		"scope": {
    			"domain": {
    				"name": "A-Company"
    			}
    		}
    	}
    }
    ```


## 响应<a name="s3a08e13bb5b34dc2ba4dcd84a0d51cf5"></a>

-   Response Header参数说明

    <a name="zh-cn_topic_0026585112_table44962972"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0026585112_row49143529"><th class="cellrowborder" valign="top" width="22%" id="mcps1.1.5.1.1"><p id="zh-cn_topic_0026585112_p21202951"><a name="zh-cn_topic_0026585112_p21202951"></a><a name="zh-cn_topic_0026585112_p21202951"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.759999999999998%" id="mcps1.1.5.1.2"><p id="p1354817920213"><a name="p1354817920213"></a><a name="p1354817920213"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.060000000000002%" id="mcps1.1.5.1.3"><p id="zh-cn_topic_0026585112_p39717481"><a name="zh-cn_topic_0026585112_p39717481"></a><a name="zh-cn_topic_0026585112_p39717481"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="40.18%" id="mcps1.1.5.1.4"><p id="zh-cn_topic_0026585112_p62999416"><a name="zh-cn_topic_0026585112_p62999416"></a><a name="zh-cn_topic_0026585112_p62999416"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0026585112_row2679067"><td class="cellrowborder" valign="top" width="22%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0026585112_p15677883"><a name="zh-cn_topic_0026585112_p15677883"></a><a name="zh-cn_topic_0026585112_p15677883"></a>X-Subject-Token</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.759999999999998%" headers="mcps1.1.5.1.2 "><p id="p954817912217"><a name="p954817912217"></a><a name="p954817912217"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.060000000000002%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0026585112_p61948991"><a name="zh-cn_topic_0026585112_p61948991"></a><a name="zh-cn_topic_0026585112_p61948991"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.18%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0026585112_p51812368"><a name="zh-cn_topic_0026585112_p51812368"></a><a name="zh-cn_topic_0026585112_p51812368"></a>签名后的token。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   Token格式说明

    <a name="t9aa18688b0f44302a45f87a865a4f9d7"></a>
    <table><thead align="left"><tr id="r4495c7bbf2c14d50a55a4ac402e189ca"><th class="cellrowborder" valign="top" width="22.06220622062206%" id="mcps1.1.5.1.1"><p id="a604782cae932448db4a5fe6032c0703e"><a name="a604782cae932448db4a5fe6032c0703e"></a><a name="a604782cae932448db4a5fe6032c0703e"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.01200120012001%" id="mcps1.1.5.1.2"><p id="a6175c8a318d24e39837027e182baaed9"><a name="a6175c8a318d24e39837027e182baaed9"></a><a name="a6175c8a318d24e39837027e182baaed9"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.711771177117715%" id="mcps1.1.5.1.3"><p id="a8ed9dc140ab940ae83066efac4a62450"><a name="a8ed9dc140ab940ae83066efac4a62450"></a><a name="a8ed9dc140ab940ae83066efac4a62450"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="40.21402140214022%" id="mcps1.1.5.1.4"><p id="a7926893fadf64b0cba9adac5489deefd"><a name="a7926893fadf64b0cba9adac5489deefd"></a><a name="a7926893fadf64b0cba9adac5489deefd"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="rcc2f2253b42941d3976e9118b7899178"><td class="cellrowborder" valign="top" width="22.06220622062206%" headers="mcps1.1.5.1.1 "><p id="a07a6ef85698e438b842d000b6bcbb235"><a name="a07a6ef85698e438b842d000b6bcbb235"></a><a name="a07a6ef85698e438b842d000b6bcbb235"></a>methods</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.01200120012001%" headers="mcps1.1.5.1.2 "><p id="ab83556a39c894a0983c94c05bbe8a92d"><a name="ab83556a39c894a0983c94c05bbe8a92d"></a><a name="ab83556a39c894a0983c94c05bbe8a92d"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.711771177117715%" headers="mcps1.1.5.1.3 "><p id="a558b3430e0444f97a88d96cdc036401e"><a name="a558b3430e0444f97a88d96cdc036401e"></a><a name="a558b3430e0444f97a88d96cdc036401e"></a>Json Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.21402140214022%" headers="mcps1.1.5.1.4 "><p id="a7b9d6f974d1e4d44890be49309a0382f"><a name="a7b9d6f974d1e4d44890be49309a0382f"></a><a name="a7b9d6f974d1e4d44890be49309a0382f"></a>获取token的方式。</p>
    </td>
    </tr>
    <tr id="r952955421b3345d29a03350797976bef"><td class="cellrowborder" valign="top" width="22.06220622062206%" headers="mcps1.1.5.1.1 "><p id="aec3770aaf9384235aed7d5a3e9b61d34"><a name="aec3770aaf9384235aed7d5a3e9b61d34"></a><a name="aec3770aaf9384235aed7d5a3e9b61d34"></a>expires_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.01200120012001%" headers="mcps1.1.5.1.2 "><p id="a2d5989348dcc4c34ab87e762205e3e25"><a name="a2d5989348dcc4c34ab87e762205e3e25"></a><a name="a2d5989348dcc4c34ab87e762205e3e25"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.711771177117715%" headers="mcps1.1.5.1.3 "><p id="a06df05908d2046d6b318f3dbadcad5fa"><a name="a06df05908d2046d6b318f3dbadcad5fa"></a><a name="a06df05908d2046d6b318f3dbadcad5fa"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.21402140214022%" headers="mcps1.1.5.1.4 "><p id="af0c635100ad74b489f89c886e157e49b"><a name="af0c635100ad74b489f89c886e157e49b"></a><a name="af0c635100ad74b489f89c886e157e49b"></a>token到期时间。</p>
    </td>
    </tr>
    <tr id="r566af79660784b49a20126aeb8226599"><td class="cellrowborder" valign="top" width="22.06220622062206%" headers="mcps1.1.5.1.1 "><p id="a99ee5815381b446bab5b3b871f0cd77f"><a name="a99ee5815381b446bab5b3b871f0cd77f"></a><a name="a99ee5815381b446bab5b3b871f0cd77f"></a>issued_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.01200120012001%" headers="mcps1.1.5.1.2 "><p id="aa7051ea6df594043a3d18cfbdfb49dc8"><a name="aa7051ea6df594043a3d18cfbdfb49dc8"></a><a name="aa7051ea6df594043a3d18cfbdfb49dc8"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.711771177117715%" headers="mcps1.1.5.1.3 "><p id="af1aa454ebf634d428c9498bb88dd9d45"><a name="af1aa454ebf634d428c9498bb88dd9d45"></a><a name="af1aa454ebf634d428c9498bb88dd9d45"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.21402140214022%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0026585112_p532161155713"><a name="zh-cn_topic_0026585112_p532161155713"></a><a name="zh-cn_topic_0026585112_p532161155713"></a>token产生时间。</p>
    </td>
    </tr>
    <tr id="r2bdea9cf4b4a40ea89733ee4ff3af64a"><td class="cellrowborder" valign="top" width="22.06220622062206%" headers="mcps1.1.5.1.1 "><p id="a313ab3f0623c4e57a9160a072e6a22c9"><a name="a313ab3f0623c4e57a9160a072e6a22c9"></a><a name="a313ab3f0623c4e57a9160a072e6a22c9"></a>user</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.01200120012001%" headers="mcps1.1.5.1.2 "><p id="a87695b24819042c8afa89bf8867ebdf5"><a name="a87695b24819042c8afa89bf8867ebdf5"></a><a name="a87695b24819042c8afa89bf8867ebdf5"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.711771177117715%" headers="mcps1.1.5.1.3 "><p id="a27424032f78a40379dddacb5ab25166d"><a name="a27424032f78a40379dddacb5ab25166d"></a><a name="a27424032f78a40379dddacb5ab25166d"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.21402140214022%" headers="mcps1.1.5.1.4 "><p id="a220a5e088be14830a1e9db57ad7e9d50"><a name="a220a5e088be14830a1e9db57ad7e9d50"></a><a name="a220a5e088be14830a1e9db57ad7e9d50"></a>示例：</p>
    <pre class="screen" id="s94858990e5764505971cc869331632fc"><a name="s94858990e5764505971cc869331632fc"></a><a name="s94858990e5764505971cc869331632fc"></a>"user": { 
          "name": "James", 
          "id": "b95b78b67fa045b38104...", 
          "password_expires_at":"2016-11-06T15:32:17.000000",
          "domain": { 
             "name": "A-Company",
             "id": "fdec73ffea524aa1b373e40..."
           } 
        }</pre>
    <a name="ul10538192315141"></a><a name="ul10538192315141"></a><ul id="ul10538192315141"><li>user.name：用户名称。</li><li>user.id：用户ID。</li><li>domain.name：用户所属的账号名称。</li><li>domain.id：用户所属的账户的ID。</li><li>password_expires_at：密码过期时间（UTC时间），<span class="parmvalue" id="parmvalue1793374142317"><a name="parmvalue1793374142317"></a><a name="parmvalue1793374142317"></a>“null”</span>表示密码不过期。</li></ul>
    </td>
    </tr>
    <tr id="rd33372d927214527ac870bb11715c536"><td class="cellrowborder" valign="top" width="22.06220622062206%" headers="mcps1.1.5.1.1 "><p id="a66272c967cb547c09f7a7316b4ae754c"><a name="a66272c967cb547c09f7a7316b4ae754c"></a><a name="a66272c967cb547c09f7a7316b4ae754c"></a>domain</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.01200120012001%" headers="mcps1.1.5.1.2 "><p id="a9183943cbe59479691b60e9c95a74a0d"><a name="a9183943cbe59479691b60e9c95a74a0d"></a><a name="a9183943cbe59479691b60e9c95a74a0d"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.711771177117715%" headers="mcps1.1.5.1.3 "><p id="a06d0695f36184007ab70f95018c90a92"><a name="a06d0695f36184007ab70f95018c90a92"></a><a name="a06d0695f36184007ab70f95018c90a92"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.21402140214022%" headers="mcps1.1.5.1.4 "><p id="a72f97dddf8204ffb93f87e0d6ae2111f"><a name="a72f97dddf8204ffb93f87e0d6ae2111f"></a><a name="a72f97dddf8204ffb93f87e0d6ae2111f"></a>如果请求体中scope参数设置为domain，则返回该字段。</p>
    <p id="a4a60927497a74911bd2ab640524d9633"><a name="a4a60927497a74911bd2ab640524d9633"></a><a name="a4a60927497a74911bd2ab640524d9633"></a>示例：</p>
    <pre class="screen" id="s6426dc53b2a4457ea51cc7ea9e64f456"><a name="s6426dc53b2a4457ea51cc7ea9e64f456"></a><a name="s6426dc53b2a4457ea51cc7ea9e64f456"></a>"domain": { 
          "name" : "A-Company"     
          "id" : "fdec73ffea524aa1b373e40..."</pre>
    <a name="ul4940103212141"></a><a name="ul4940103212141"></a><ul id="ul4940103212141"><li>domain.name<em id="aa778606b54604456919e7183a40559f1"><a name="aa778606b54604456919e7183a40559f1"></a><a name="aa778606b54604456919e7183a40559f1"></a>：</em>用户所属的账户名称。</li><li>domain.id<em id="a929ca2dc9f8d4dc488c64a5424f037ce"><a name="a929ca2dc9f8d4dc488c64a5424f037ce"></a><a name="a929ca2dc9f8d4dc488c64a5424f037ce"></a>：</em>用户所属的账户的ID。</li></ul>
    </td>
    </tr>
    <tr id="r3a914bf0c52c43e390883648cbe964ff"><td class="cellrowborder" valign="top" width="22.06220622062206%" headers="mcps1.1.5.1.1 "><p id="a0e6de929a1ea4db0b88e97acb4287d5e"><a name="a0e6de929a1ea4db0b88e97acb4287d5e"></a><a name="a0e6de929a1ea4db0b88e97acb4287d5e"></a>project</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.01200120012001%" headers="mcps1.1.5.1.2 "><p id="a346f8467c2e24793ab55c120fc37852f"><a name="a346f8467c2e24793ab55c120fc37852f"></a><a name="a346f8467c2e24793ab55c120fc37852f"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.711771177117715%" headers="mcps1.1.5.1.3 "><p id="af6953054960f4c59903b92961b10b426"><a name="af6953054960f4c59903b92961b10b426"></a><a name="af6953054960f4c59903b92961b10b426"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.21402140214022%" headers="mcps1.1.5.1.4 "><p id="a41001b564477400f98aef711e86f0197"><a name="a41001b564477400f98aef711e86f0197"></a><a name="a41001b564477400f98aef711e86f0197"></a>如果请求体中scope参数设置为project，则返回该字段。</p>
    <p id="a2658c45981e64570b63c49c45cfdfac7"><a name="a2658c45981e64570b63c49c45cfdfac7"></a><a name="a2658c45981e64570b63c49c45cfdfac7"></a>示例：</p>
    <pre class="screen" id="s75cd01f2f3df45ada904958dc41f5307"><a name="s75cd01f2f3df45ada904958dc41f5307"></a><a name="s75cd01f2f3df45ada904958dc41f5307"></a>"project": { 
          "name": "Project A", 
          "id": "34c77f3eaf84c00aaf54...", 
          "domain": { 
             "name": "A-Company",
             "id": "fdec73ffea524aa1b373e40..."
           } 
       }</pre>
    <a name="ul198562416149"></a><a name="ul198562416149"></a><ul id="ul198562416149"><li>project.name：project名称。</li><li>project.id：project的ID。</li><li>domain.name：project所属的账户名称。</li><li>domain.id：project所属的账户的ID。</li></ul>
    </td>
    </tr>
    <tr id="row31009604113628"><td class="cellrowborder" valign="top" width="22.06220622062206%" headers="mcps1.1.5.1.1 "><p id="p22717013113628"><a name="p22717013113628"></a><a name="p22717013113628"></a>catalog</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.01200120012001%" headers="mcps1.1.5.1.2 "><p id="p54936595113628"><a name="p54936595113628"></a><a name="p54936595113628"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.711771177117715%" headers="mcps1.1.5.1.3 "><p id="p46529556113628"><a name="p46529556113628"></a><a name="p46529556113628"></a>Json Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.21402140214022%" headers="mcps1.1.5.1.4 "><p id="p45368001113628"><a name="p45368001113628"></a><a name="p45368001113628"></a>endpoints相关信息。</p>
    <p id="p50787600113939"><a name="p50787600113939"></a><a name="p50787600113939"></a>示例：</p>
    <pre class="screen" id="screen17568328113914"><a name="screen17568328113914"></a><a name="screen17568328113914"></a>"catalog": [{
        "type": "identity",
        "id": "1331e5cff2a74d76b03da122591...",
        "name": "iam",
        "endpoints": [{
            "url": "<em id="i17055930114035"><a name="i17055930114035"></a><a name="i17055930114035"></a>www.example.com</em>/v3",
            "region": "*",
            "region_id": "*",
            "interface": "public",
            "id": "089d4a381d574308a703122d3ae7..."
        }]
    }]</pre>
    <a name="ul243124664420"></a><a name="ul243124664420"></a><ul id="ul243124664420"><li>type：该接口所属的服务。</li><li>id：服务的id。</li><li>name：服务的名称。</li><li>endpoints：终端节点。</li><li>url：调用该接口的url。</li><li>region：服务的所属区域。</li><li>region_id：服务的所属区域id。</li><li>interface：接口状态，public表示为公开。</li><li>id：接口的id。</li></ul>
    </td>
    </tr>
    <tr id="r57913d5a1da24c699a412dced6a7b573"><td class="cellrowborder" valign="top" width="22.06220622062206%" headers="mcps1.1.5.1.1 "><p id="a45bd202186b249bfa8fc87bbcbf05bb9"><a name="a45bd202186b249bfa8fc87bbcbf05bb9"></a><a name="a45bd202186b249bfa8fc87bbcbf05bb9"></a>roles</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.01200120012001%" headers="mcps1.1.5.1.2 "><p id="ae5cf82a55c21452aa028ff59e6973404"><a name="ae5cf82a55c21452aa028ff59e6973404"></a><a name="ae5cf82a55c21452aa028ff59e6973404"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.711771177117715%" headers="mcps1.1.5.1.3 "><p id="aa1fb3d35fbda45208e6e58dbbbc00b01"><a name="aa1fb3d35fbda45208e6e58dbbbc00b01"></a><a name="aa1fb3d35fbda45208e6e58dbbbc00b01"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.21402140214022%" headers="mcps1.1.5.1.4 "><p id="a18bf24a442094153ab2a8f7391737d06"><a name="a18bf24a442094153ab2a8f7391737d06"></a><a name="a18bf24a442094153ab2a8f7391737d06"></a>Token的权限信息。</p>
    <p id="ace14d3d704ae4d41abdcfc9ae99def0f"><a name="ace14d3d704ae4d41abdcfc9ae99def0f"></a><a name="ace14d3d704ae4d41abdcfc9ae99def0f"></a>示例：</p>
    <pre class="screen" id="s71b72ebcaad84e58881c80352e028dff"><a name="s71b72ebcaad84e58881c80352e028dff"></a><a name="s71b72ebcaad84e58881c80352e028dff"></a>"roles" : [{ 
         "name" : "role1", 
         "id" : "roleid1" 
         }, { 
         "name" : "role2", 
         "id" : "roleid2" 
         } 
       ] </pre>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例

    样例中domain、user和role的关系为：domain为华为云账号，账号是资源归属、资源使用计费的主体，对其所拥有的资源及云服务具有完全的访问权限，可以创建用户和用户组、分配用户权限等。user为账号在IAM中创建的用户，是账号中的子用户，权限由账号分配。如果是账号本身获取token，则domain和user信息一致。role为获取的token具备的权限。

    ```
    Response Header中存储信息为：
    X-Subject-Token:MIIDkgYJKoZIhvcNAQcCoIIDgzCCA38CAQExDTALBglghkgBZQMEAgEwgXXXXX...
    
    Response Body中存储信息为： 
    {
      "token" : {
        "methods" : ["password"],
        "expires_at" : "2015-11-09T01:42:57.527363Z",
        "issued_at" : "2015-11-09T00:42:57.527404Z",
        "user" : {
          "domain" : {
          "id" : "default",
          "name" : "exampledomain"
          },
          "id" : "ee4dfb6e5540447cb37419051XXX..",
          "name" : "exampleuser",
          "password_expires_at":"2016-11-06T15:32:17.000000",
        },
        "domain" : {
           "name" : "exampledomain",
           "id" : "default"
        },
        "catalog": [{
            "type": "identity",
            "id": "1331e5cff2a74d76b03da12259XXXX...",
            "name": "iam",
            "endpoints": [{
                "url": "www.example.com/v3",
                "region": "*",
                "region_id": "*",
               "interface": "public",
                 "id": "089d4a381d574308a703122d3aXXXX..."
           }]
        }], 
        "roles" : [{
           "name" : "role1",
           "id" : "roleid1"
           }, {
           "name" : "role2",
           "id" : "roleid2"
           }
      ]
      }
    }
    ```


## 状态码<a name="sbfe93ca4c2b9427dbb2218a4e72da6a8"></a>

<a name="zh-cn_topic_0026585112_table34550710"></a>
<table><thead align="left"><tr id="zh-cn_topic_0026585112_row8352109"><th class="cellrowborder" valign="top" width="48.15%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0026585112_p5432205"><a name="zh-cn_topic_0026585112_p5432205"></a><a name="zh-cn_topic_0026585112_p5432205"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="51.849999999999994%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0026585112_p37355470"><a name="zh-cn_topic_0026585112_p37355470"></a><a name="zh-cn_topic_0026585112_p37355470"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0026585112_row5894231"><td class="cellrowborder" valign="top" width="48.15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p7670737"><a name="zh-cn_topic_0026585112_p7670737"></a><a name="zh-cn_topic_0026585112_p7670737"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="51.849999999999994%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0026585112_p17349988"><a name="zh-cn_topic_0026585112_p17349988"></a><a name="zh-cn_topic_0026585112_p17349988"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0026585112_row21932166"><td class="cellrowborder" valign="top" width="48.15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p31674992"><a name="zh-cn_topic_0026585112_p31674992"></a><a name="zh-cn_topic_0026585112_p31674992"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="51.849999999999994%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0026585112_p15537542"><a name="zh-cn_topic_0026585112_p15537542"></a><a name="zh-cn_topic_0026585112_p15537542"></a>请求错误。</p>
</td>
</tr>
<tr id="r22bf632ff3984ffbaa2734a029063cfb"><td class="cellrowborder" valign="top" width="48.15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p947606916650"><a name="zh-cn_topic_0026585112_p947606916650"></a><a name="zh-cn_topic_0026585112_p947606916650"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="51.849999999999994%" headers="mcps1.1.3.1.2 "><p id="a3a62e2f9d6c84b4083dfb8b2ade8e14c"><a name="a3a62e2f9d6c84b4083dfb8b2ade8e14c"></a><a name="a3a62e2f9d6c84b4083dfb8b2ade8e14c"></a>认证失败。</p>
</td>
</tr>
<tr id="r41d0d854619349f898c16f7c61792083"><td class="cellrowborder" valign="top" width="48.15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p762821816657"><a name="zh-cn_topic_0026585112_p762821816657"></a><a name="zh-cn_topic_0026585112_p762821816657"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="51.849999999999994%" headers="mcps1.1.3.1.2 "><p id="a0261fc1955104ca3b1f0a46388724624"><a name="a0261fc1955104ca3b1f0a46388724624"></a><a name="a0261fc1955104ca3b1f0a46388724624"></a>鉴权失败。</p>
</td>
</tr>
<tr id="rea66e1a745ee4e0882be6b9f5349ac4d"><td class="cellrowborder" valign="top" width="48.15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p486971841676"><a name="zh-cn_topic_0026585112_p486971841676"></a><a name="zh-cn_topic_0026585112_p486971841676"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="51.849999999999994%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0026585112_p521578261676"><a name="zh-cn_topic_0026585112_p521578261676"></a><a name="zh-cn_topic_0026585112_p521578261676"></a>找不到资源。</p>
</td>
</tr>
<tr id="r230ba1b5ddec4cd0a41a5c37806e60f5"><td class="cellrowborder" valign="top" width="48.15%" headers="mcps1.1.3.1.1 "><p id="af8f4513c90d344e3b90952b53e3ee015"><a name="af8f4513c90d344e3b90952b53e3ee015"></a><a name="af8f4513c90d344e3b90952b53e3ee015"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="51.849999999999994%" headers="mcps1.1.3.1.2 "><p id="a19c27fd6b377464898ec6cae5778ec80"><a name="a19c27fd6b377464898ec6cae5778ec80"></a><a name="a19c27fd6b377464898ec6cae5778ec80"></a>内部服务错误。可能是格式错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0026585112_row6824316711"><td class="cellrowborder" valign="top" width="48.15%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p61418816711"><a name="zh-cn_topic_0026585112_p61418816711"></a><a name="zh-cn_topic_0026585112_p61418816711"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="51.849999999999994%" headers="mcps1.1.3.1.2 "><p id="a4bc003bda05e465eb3a3f0f989888213"><a name="a4bc003bda05e465eb3a3f0f989888213"></a><a name="a4bc003bda05e465eb3a3f0f989888213"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

