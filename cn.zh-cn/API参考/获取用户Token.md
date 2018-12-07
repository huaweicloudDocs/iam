# 获取用户Token<a name="ZH-CN_TOPIC_0110485134"></a>

## 功能介绍<a name="s5888597838b0425a92e3419fb766c7f5"></a>

该接口用来获取用户自己的Token，可以通过用户名/密码的方式进行认证（开启了虚拟MFA方式的登录保护后，在通过用户名/密码的方式进行认证时需要加上验证码部分）。

>![](public_sys-resources/icon-note.gif) **说明：**   
>-   Token的有效期为24小时，需要使用一个Token鉴权时，可以先缓存起来，避免频繁调用。  
>-   该接口提供了锁定机制用于防止暴力破解，调用时，请确保用户名密码正确，输错一定次数（安全管理员可设置该规则）将被锁定。  

## URI<a name="s46d3616bd4c54e55ba97a528518a5890"></a>

URI格式

POST /v3/auth/tokens

## 请求<a name="se7fe5cac0d544e119c49322cc1707eb6"></a>

-   Request Header参数说明

    <a name="t68c7bd10e66a4380a1e6cdc78ca95669"></a>
    <table><thead align="left"><tr id="r584496594a404ce18918a40e6e57c2ec"><th class="cellrowborder" valign="top" width="17.818218178182182%" id="mcps1.1.5.1.1"><p id="ac3a989cc5d3a405889eabb47dee84b04"><a name="ac3a989cc5d3a405889eabb47dee84b04"></a><a name="ac3a989cc5d3a405889eabb47dee84b04"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.568243175682433%" id="mcps1.1.5.1.2"><p id="a69a20ac00b86496aa8418517c542b0da"><a name="a69a20ac00b86496aa8418517c542b0da"></a><a name="a69a20ac00b86496aa8418517c542b0da"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.108189181081894%" id="mcps1.1.5.1.3"><p id="a92c23d4441054df0972e025aeb3a8d7f"><a name="a92c23d4441054df0972e025aeb3a8d7f"></a><a name="a92c23d4441054df0972e025aeb3a8d7f"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.5053494650535%" id="mcps1.1.5.1.4"><p id="abe6882c44cf4402d8ed7706b9278f33b"><a name="abe6882c44cf4402d8ed7706b9278f33b"></a><a name="abe6882c44cf4402d8ed7706b9278f33b"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r5d63069d6a8a426e8b25b94d1b4d302a"><td class="cellrowborder" valign="top" width="17.818218178182182%" headers="mcps1.1.5.1.1 "><p id="ad4fb6253385c46ab8720a0e13f573694"><a name="ad4fb6253385c46ab8720a0e13f573694"></a><a name="ad4fb6253385c46ab8720a0e13f573694"></a>Content-Type</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.568243175682433%" headers="mcps1.1.5.1.2 "><p id="a6b33800bcb2a446695b1d33a2d751554"><a name="a6b33800bcb2a446695b1d33a2d751554"></a><a name="a6b33800bcb2a446695b1d33a2d751554"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.108189181081894%" headers="mcps1.1.5.1.3 "><p id="ab34a5e95b76b4b79a72da0734025f211"><a name="ab34a5e95b76b4b79a72da0734025f211"></a><a name="ab34a5e95b76b4b79a72da0734025f211"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.5053494650535%" headers="mcps1.1.5.1.4 "><p id="a716277ae541d4553bb10490f9c02593d"><a name="a716277ae541d4553bb10490f9c02593d"></a><a name="a716277ae541d4553bb10490f9c02593d"></a>该字段内容填为<span class="parmvalue" id="parmvalue17258191372713"><a name="parmvalue17258191372713"></a><a name="parmvalue17258191372713"></a>“application/json;charset=utf8”</span>。</p>
    </td>
    </tr>
    </tbody>
    </table>

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
    <td class="cellrowborder" valign="top" width="46.379999999999995%" headers="mcps1.1.5.1.4 "><p id="p12733551037"><a name="p12733551037"></a><a name="p12733551037"></a>包含：methods，password，totp。详情请参见<a href="#ZH-CN_TOPIC_0110485134__table178715913019">表1</a>。</p>
    </td>
    </tr>
    <tr id="row77278232020"><td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.1.5.1.1 "><p id="p124182557111"><a name="p124182557111"></a><a name="p124182557111"></a>scope</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.51%" headers="mcps1.1.5.1.2 "><p id="p144209551918"><a name="p144209551918"></a><a name="p144209551918"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.07%" headers="mcps1.1.5.1.3 "><p id="p144236557120"><a name="p144236557120"></a><a name="p144236557120"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.379999999999995%" headers="mcps1.1.5.1.4 "><p id="p144263552114"><a name="p144263552114"></a><a name="p144263552114"></a>token的作用范围。支持domain、project，但两者不能设置在同一层级上。</p>
    <p id="p13651522366"><a name="p13651522366"></a><a name="p13651522366"></a>示例1：</p>
    <p id="p1035625473615"><a name="p1035625473615"></a><a name="p1035625473615"></a>该示例表示本token仅能访问examplename企业账户下的资源。</p>
    <pre class="screen" id="screen134303554117"><a name="screen134303554117"></a><a name="screen134303554117"></a>"scope": {
          "domain": {
          "name": "examplename"
          }
        }</pre>
    <p id="p1244015551216"><a name="p1244015551216"></a><a name="p1244015551216"></a><span class="parmname" id="parmname1140754313274"><a name="parmname1140754313274"></a><a name="parmname1140754313274"></a>“name”</span>为企业账户名称，此处以<span class="parmvalue" id="parmvalue191641351182714"><a name="parmvalue191641351182714"></a><a name="parmvalue191641351182714"></a>“examplename”</span>为例。</p>
    <p id="p844165511115"><a name="p844165511115"></a><a name="p844165511115"></a>示例2：</p>
    <p id="p198977484378"><a name="p198977484378"></a><a name="p198977484378"></a>该示例表示本token仅能访问所属企业账户下的id为0215ef11e49d4743be23dd97a1561e91的project下的资源。</p>
    <pre class="screen" id="screen5443255511"><a name="screen5443255511"></a><a name="screen5443255511"></a>"scope": {
          "project": {
          "id": "0215ef11e49d4743be23dd97a1561e91"
          }
        }</pre>
    <p id="p64531155419"><a name="p64531155419"></a><a name="p64531155419"></a>示例3：</p>
    <p id="p412358203718"><a name="p412358203718"></a><a name="p412358203718"></a>该示例表示本token仅能访问examplename企业账户下名称为project_example的project下的资源。</p>
    <pre class="screen" id="screen045418552115"><a name="screen045418552115"></a><a name="screen045418552115"></a>    "scope": {
            "domain": {
                "name": "exampledomain",
                "project": {
                    "id": "0215ef11e49d4743be23dd97a1561e91"
                }
            }
        }</pre>
    </td>
    </tr>
    </tbody>
    </table>

    **表 1**  identity格式说明

    <a name="table178715913019"></a>
    <table><thead align="left"><tr id="row178259107"><th class="cellrowborder" valign="top" width="17.98%" id="mcps1.2.5.1.1"><p id="p2782592014"><a name="p2782592014"></a><a name="p2782592014"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.72%" id="mcps1.2.5.1.2"><p id="p107821391309"><a name="p107821391309"></a><a name="p107821391309"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.919999999999998%" id="mcps1.2.5.1.3"><p id="p1478220911014"><a name="p1478220911014"></a><a name="p1478220911014"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.379999999999995%" id="mcps1.2.5.1.4"><p id="p4782891400"><a name="p4782891400"></a><a name="p4782891400"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row19783694013"><td class="cellrowborder" valign="top" width="17.98%" headers="mcps1.2.5.1.1 "><p id="p2078229505"><a name="p2078229505"></a><a name="p2078229505"></a>methods</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.72%" headers="mcps1.2.5.1.2 "><p id="p97821091302"><a name="p97821091302"></a><a name="p97821091302"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.919999999999998%" headers="mcps1.2.5.1.3 "><p id="p13783692005"><a name="p13783692005"></a><a name="p13783692005"></a>String Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.379999999999995%" headers="mcps1.2.5.1.4 "><p id="p207831391104"><a name="p207831391104"></a><a name="p207831391104"></a>该字段内容为<span class="parmvalue" id="parmvalue0835327185719"><a name="parmvalue0835327185719"></a><a name="parmvalue0835327185719"></a>“password”</span>。如果开启了虚拟MFA方式的登录保护时，该字段内容为[“password”,"totp"]</p>
    </td>
    </tr>
    <tr id="row678413920012"><td class="cellrowborder" valign="top" width="17.98%" headers="mcps1.2.5.1.1 "><p id="p978317917017"><a name="p978317917017"></a><a name="p978317917017"></a>password</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.72%" headers="mcps1.2.5.1.2 "><p id="p14783391604"><a name="p14783391604"></a><a name="p14783391604"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.919999999999998%" headers="mcps1.2.5.1.3 "><p id="p878369601"><a name="p878369601"></a><a name="p878369601"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.379999999999995%" headers="mcps1.2.5.1.4 "><p id="p278314916018"><a name="p278314916018"></a><a name="p278314916018"></a>示例：</p>
    <pre class="screen" id="screen234320611429"><a name="screen234320611429"></a><a name="screen234320611429"></a>"password": {
    "user": {
    "name": "name",
    "password": "password",
    "domain": {
    "name": "name"
    }
    }
    }</pre>
    <p id="p778411910016"><a name="p778411910016"></a><a name="p778411910016"></a>domainname<em id="i077911411581"><a name="i077911411581"></a><a name="i077911411581"></a>：</em>用户所属的企业账户名称。</p>
    <p id="p9784991003"><a name="p9784991003"></a><a name="p9784991003"></a>username<em id="i16051475581"><a name="i16051475581"></a><a name="i16051475581"></a>：</em>用户名称。</p>
    <p id="p37841791809"><a name="p37841791809"></a><a name="p37841791809"></a>password<em id="i158181107583"><a name="i158181107583"></a><a name="i158181107583"></a>：</em>用户登录时的密码。</p>
    </td>
    </tr>
    <tr id="row44531471452"><td class="cellrowborder" valign="top" width="17.98%" headers="mcps1.2.5.1.1 "><p id="p44531471355"><a name="p44531471355"></a><a name="p44531471355"></a>totp</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.72%" headers="mcps1.2.5.1.2 "><p id="p1845367157"><a name="p1845367157"></a><a name="p1845367157"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.919999999999998%" headers="mcps1.2.5.1.3 "><p id="p1039618223512"><a name="p1039618223512"></a><a name="p1039618223512"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.379999999999995%" headers="mcps1.2.5.1.4 "><p id="p15453127359"><a name="p15453127359"></a><a name="p15453127359"></a>当开启了虚拟MFA方式的登录保护时，该参数必填。</p>
    <p id="p17544346257"><a name="p17544346257"></a><a name="p17544346257"></a>示例：</p>
    <pre class="screen" id="screen816391824220"><a name="screen816391824220"></a><a name="screen816391824220"></a>"totp": {
    "user": {
    "id": "b95b78b67fa045b38104c12fb2729cd0",
    "passcode": "012345"
    }
    }</pre>
    </td>
    </tr>
    </tbody>
    </table>

-   请求样例

    获取用户名为exampleuser，登录密码为Examplepassword123，所在domain名为exampledomain的token。

    ```
    {
      "auth": {
        "identity": {
          "methods": ["password"],
          "password": {
            "user": {
              "name": "exampleuser",
              "password": "Examplepassword123",
              "domain": {
                "name": "exampledomain"
              }
            }
          }
        },
        "scope": {
          "domain": {
            "name": "exampledomain"
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
    "methods": [
    "password","totp"
    ],
    "password": {
    "user": {
    "name": "name",
    "password": "password",
    "domain": {
    "name": "name"
    
    }
    }
    },
    "totp": {
    "user": {
    "id": "id",
    "passcode": "012345"
    }
    }
    },
    "scope": {
    "domain": {
    "name": "name"
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
          "name": "<em id="ab903696341a94e65841ad3f0cc988047"><a name="ab903696341a94e65841ad3f0cc988047"></a><a name="ab903696341a94e65841ad3f0cc988047"></a>username</em>", 
          "id": "<em id="zh-cn_topic_0026585112_i433336816519"><a name="zh-cn_topic_0026585112_i433336816519"></a><a name="zh-cn_topic_0026585112_i433336816519"></a>userid</em>", 
          "password_expires_at":"2016-11-06T15:32:17.000000",
          "domain": { 
             "name": "<em id="zh-cn_topic_0026585112_i438354691645"><a name="zh-cn_topic_0026585112_i438354691645"></a><a name="zh-cn_topic_0026585112_i438354691645"></a>domainname</em>",
             "id": "<em id="zh-cn_topic_0026585112_i75268851664"><a name="zh-cn_topic_0026585112_i75268851664"></a><a name="zh-cn_topic_0026585112_i75268851664"></a>domainid</em>"
           } 
        }</pre>
    <p id="a9ab4f8a193ab4c3ba18b867632f7ee69"><a name="a9ab4f8a193ab4c3ba18b867632f7ee69"></a><a name="a9ab4f8a193ab4c3ba18b867632f7ee69"></a>username：用户名称。</p>
    <p id="a3245b4ac92dc4cd1896ab1c512c69f28"><a name="a3245b4ac92dc4cd1896ab1c512c69f28"></a><a name="a3245b4ac92dc4cd1896ab1c512c69f28"></a>userid：用户ID。</p>
    <p id="a8fac11b7236847e4ac96ab14ef284ced"><a name="a8fac11b7236847e4ac96ab14ef284ced"></a><a name="a8fac11b7236847e4ac96ab14ef284ced"></a>domainname：用户所属的企业账户名称。</p>
    <p id="a0986260371f8424caed02efdd2582ac2"><a name="a0986260371f8424caed02efdd2582ac2"></a><a name="a0986260371f8424caed02efdd2582ac2"></a>domainid：用户所属的企业账户的ID。</p>
    <p id="p104501252195717"><a name="p104501252195717"></a><a name="p104501252195717"></a>password_expires_at：可选，密码过期时间（UTC时间），<span class="parmvalue" id="parmvalue1793374142317"><a name="parmvalue1793374142317"></a><a name="parmvalue1793374142317"></a>“null”</span>表示密码不过期。</p>
    </td>
    </tr>
    <tr id="rd33372d927214527ac870bb11715c536"><td class="cellrowborder" valign="top" width="22.06220622062206%" headers="mcps1.1.5.1.1 "><p id="a66272c967cb547c09f7a7316b4ae754c"><a name="a66272c967cb547c09f7a7316b4ae754c"></a><a name="a66272c967cb547c09f7a7316b4ae754c"></a>domain</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.01200120012001%" headers="mcps1.1.5.1.2 "><p id="a9183943cbe59479691b60e9c95a74a0d"><a name="a9183943cbe59479691b60e9c95a74a0d"></a><a name="a9183943cbe59479691b60e9c95a74a0d"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.711771177117715%" headers="mcps1.1.5.1.3 "><p id="a06d0695f36184007ab70f95018c90a92"><a name="a06d0695f36184007ab70f95018c90a92"></a><a name="a06d0695f36184007ab70f95018c90a92"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.21402140214022%" headers="mcps1.1.5.1.4 "><p id="a72f97dddf8204ffb93f87e0d6ae2111f"><a name="a72f97dddf8204ffb93f87e0d6ae2111f"></a><a name="a72f97dddf8204ffb93f87e0d6ae2111f"></a>根据请求中的scope，判断是否返回该字段。</p>
    <p id="a4a60927497a74911bd2ab640524d9633"><a name="a4a60927497a74911bd2ab640524d9633"></a><a name="a4a60927497a74911bd2ab640524d9633"></a>示例：</p>
    <pre class="screen" id="s6426dc53b2a4457ea51cc7ea9e64f456"><a name="s6426dc53b2a4457ea51cc7ea9e64f456"></a><a name="s6426dc53b2a4457ea51cc7ea9e64f456"></a>"domain": { 
          "name" : "<em id="i12041520132410"><a name="i12041520132410"></a><a name="i12041520132410"></a>domainame</em>",     
          "id" : "<em id="i1466122172413"><a name="i1466122172413"></a><a name="i1466122172413"></a>domainid</em>"}</pre>
    <p id="a16cd99c4957d4834a871cfa10891897b"><a name="a16cd99c4957d4834a871cfa10891897b"></a><a name="a16cd99c4957d4834a871cfa10891897b"></a>domainname<em id="aa778606b54604456919e7183a40559f1"><a name="aa778606b54604456919e7183a40559f1"></a><a name="aa778606b54604456919e7183a40559f1"></a>：</em>企业账户名称。</p>
    <p id="abbaa49e0412d4820aa46f8ed83c8f296"><a name="abbaa49e0412d4820aa46f8ed83c8f296"></a><a name="abbaa49e0412d4820aa46f8ed83c8f296"></a>domainid<em id="a929ca2dc9f8d4dc488c64a5424f037ce"><a name="a929ca2dc9f8d4dc488c64a5424f037ce"></a><a name="a929ca2dc9f8d4dc488c64a5424f037ce"></a>：</em>企业账户的ID。</p>
    </td>
    </tr>
    <tr id="r3a914bf0c52c43e390883648cbe964ff"><td class="cellrowborder" valign="top" width="22.06220622062206%" headers="mcps1.1.5.1.1 "><p id="a0e6de929a1ea4db0b88e97acb4287d5e"><a name="a0e6de929a1ea4db0b88e97acb4287d5e"></a><a name="a0e6de929a1ea4db0b88e97acb4287d5e"></a>project</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.01200120012001%" headers="mcps1.1.5.1.2 "><p id="a346f8467c2e24793ab55c120fc37852f"><a name="a346f8467c2e24793ab55c120fc37852f"></a><a name="a346f8467c2e24793ab55c120fc37852f"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.711771177117715%" headers="mcps1.1.5.1.3 "><p id="af6953054960f4c59903b92961b10b426"><a name="af6953054960f4c59903b92961b10b426"></a><a name="af6953054960f4c59903b92961b10b426"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.21402140214022%" headers="mcps1.1.5.1.4 "><p id="a41001b564477400f98aef711e86f0197"><a name="a41001b564477400f98aef711e86f0197"></a><a name="a41001b564477400f98aef711e86f0197"></a>根据请求中的scope，判断是否返回该字段。</p>
    <p id="a2658c45981e64570b63c49c45cfdfac7"><a name="a2658c45981e64570b63c49c45cfdfac7"></a><a name="a2658c45981e64570b63c49c45cfdfac7"></a>示例：</p>
    <pre class="screen" id="s75cd01f2f3df45ada904958dc41f5307"><a name="s75cd01f2f3df45ada904958dc41f5307"></a><a name="s75cd01f2f3df45ada904958dc41f5307"></a>"project": { 
          "name": "<em id="af63ef597e10344ecaada944624eefa21"><a name="af63ef597e10344ecaada944624eefa21"></a><a name="af63ef597e10344ecaada944624eefa21"></a>projectname</em>", 
          "id": "<em id="zh-cn_topic_0026585112_i86520761696"><a name="zh-cn_topic_0026585112_i86520761696"></a><a name="zh-cn_topic_0026585112_i86520761696"></a>projectid</em>", 
          "domain": { 
             "name": "<em id="ae7bc36a90d54412ba16df0b9c7be1214"><a name="ae7bc36a90d54412ba16df0b9c7be1214"></a><a name="ae7bc36a90d54412ba16df0b9c7be1214"></a>domainname</em>",
             "id": "<em id="ad861b7bb0b754849984a9e1ccc72003d"><a name="ad861b7bb0b754849984a9e1ccc72003d"></a><a name="ad861b7bb0b754849984a9e1ccc72003d"></a>domainid</em>"
           } 
       }</pre>
    <p id="aa22635b7681745fcaf880dd1ff0a00d3"><a name="aa22635b7681745fcaf880dd1ff0a00d3"></a><a name="aa22635b7681745fcaf880dd1ff0a00d3"></a>projectname：project名称。</p>
    <p id="a4e39e6c9ab974c2eaee7fb73a9aad692"><a name="a4e39e6c9ab974c2eaee7fb73a9aad692"></a><a name="a4e39e6c9ab974c2eaee7fb73a9aad692"></a>projectid：project的ID。</p>
    <p id="zh-cn_topic_0026585112_p288050616314"><a name="zh-cn_topic_0026585112_p288050616314"></a><a name="zh-cn_topic_0026585112_p288050616314"></a>domainname：poject所属的企业账户名称。</p>
    <p id="afc6bc78b6643448eadc6c9e4c3c5887f"><a name="afc6bc78b6643448eadc6c9e4c3c5887f"></a><a name="afc6bc78b6643448eadc6c9e4c3c5887f"></a>domainid：project所属的企业账户的ID。</p>
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
        "id": "1331e5cff2a74d76b03da1225910e31d",
        "name": "iam",
        "endpoints": [{
            "url": "<em id="i17055930114035"><a name="i17055930114035"></a><a name="i17055930114035"></a>www.example.com</em>/v3",
            "region": "*",
            "region_id": "*",
            "interface": "public",
            "id": "089d4a381d574308a703122d3ae738e9"
        }]
    }]</pre>
    </td>
    </tr>
    <tr id="r57913d5a1da24c699a412dced6a7b573"><td class="cellrowborder" valign="top" width="22.06220622062206%" headers="mcps1.1.5.1.1 "><p id="a45bd202186b249bfa8fc87bbcbf05bb9"><a name="a45bd202186b249bfa8fc87bbcbf05bb9"></a><a name="a45bd202186b249bfa8fc87bbcbf05bb9"></a>roles</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.01200120012001%" headers="mcps1.1.5.1.2 "><p id="ae5cf82a55c21452aa028ff59e6973404"><a name="ae5cf82a55c21452aa028ff59e6973404"></a><a name="ae5cf82a55c21452aa028ff59e6973404"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.711771177117715%" headers="mcps1.1.5.1.3 "><p id="aa1fb3d35fbda45208e6e58dbbbc00b01"><a name="aa1fb3d35fbda45208e6e58dbbbc00b01"></a><a name="aa1fb3d35fbda45208e6e58dbbbc00b01"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="40.21402140214022%" headers="mcps1.1.5.1.4 "><p id="a18bf24a442094153ab2a8f7391737d06"><a name="a18bf24a442094153ab2a8f7391737d06"></a><a name="a18bf24a442094153ab2a8f7391737d06"></a>角色列表。</p>
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
          "id" : "ee4dfb6e5540447cb3741905149d9b6e",
          "name" : "exampleuser",
          "password_expires_at":"2016-11-06T15:32:17.000000",
        },
        "domain" : {
           "name" : "exampledomain",
           "id" : "default"
        },
        "catalog": [{
            "type": "identity",
            "id": "1331e5cff2a74d76b03da1225910e31d",
            "name": "iam",
            "endpoints": [{
                "url": "www.example.com/v3",
                "region": "*",
                "region_id": "*",
               "interface": "public",
                 "id": "089d4a381d574308a703122d3ae738e9"
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

