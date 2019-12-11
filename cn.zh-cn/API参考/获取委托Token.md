# 获取委托Token<a name="zh-cn_topic_0064274720"></a>

## 功能介绍<a name="s5888597838b0425a92e3419fb766c7f5"></a>

该接口用来获取委托方的Token，例如：A账号与B账号创建了委托关系，A账号为委托方，B账号为被委托方，则B账号可以通过该接口获取委托Token。B账号仅能使用该Token管理A账号的委托资源，不能管理自己账号中的资源，如果B账号需要管理自己账号中的资源，需要通过[获取用户Token](获取用户Token.md)获取自己的Token。

该接口可以使用全局区域的域名和其他区域的域名调用，全局区域的域名为iam.myhuaweicloud.com。

>![](public_sys-resources/icon-note.gif) **说明：**   
>token的有效期为24小时，需要同一个token鉴权时，可以先缓存起来，避免频繁调用。  

## URI<a name="s46d3616bd4c54e55ba97a528518a5890"></a>

URI格式

POST /v3/auth/tokens

## 请求<a name="se7fe5cac0d544e119c49322cc1707eb6"></a>

-   Request Header参数说明

    <a name="t68c7bd10e66a4380a1e6cdc78ca95669"></a>
    <table><thead align="left"><tr id="r584496594a404ce18918a40e6e57c2ec"><th class="cellrowborder" valign="top" width="21.42%" id="mcps1.1.5.1.1"><p id="ac3a989cc5d3a405889eabb47dee84b04"><a name="ac3a989cc5d3a405889eabb47dee84b04"></a><a name="ac3a989cc5d3a405889eabb47dee84b04"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.939999999999998%" id="mcps1.1.5.1.2"><p id="a69a20ac00b86496aa8418517c542b0da"><a name="a69a20ac00b86496aa8418517c542b0da"></a><a name="a69a20ac00b86496aa8418517c542b0da"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.22%" id="mcps1.1.5.1.3"><p id="a92c23d4441054df0972e025aeb3a8d7f"><a name="a92c23d4441054df0972e025aeb3a8d7f"></a><a name="a92c23d4441054df0972e025aeb3a8d7f"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.42%" id="mcps1.1.5.1.4"><p id="abe6882c44cf4402d8ed7706b9278f33b"><a name="abe6882c44cf4402d8ed7706b9278f33b"></a><a name="abe6882c44cf4402d8ed7706b9278f33b"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r5d63069d6a8a426e8b25b94d1b4d302a"><td class="cellrowborder" valign="top" width="21.42%" headers="mcps1.1.5.1.1 "><p id="ad4fb6253385c46ab8720a0e13f573694"><a name="ad4fb6253385c46ab8720a0e13f573694"></a><a name="ad4fb6253385c46ab8720a0e13f573694"></a>Content-Type</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.1.5.1.2 "><p id="a6b33800bcb2a446695b1d33a2d751554"><a name="a6b33800bcb2a446695b1d33a2d751554"></a><a name="a6b33800bcb2a446695b1d33a2d751554"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.22%" headers="mcps1.1.5.1.3 "><p id="ab34a5e95b76b4b79a72da0734025f211"><a name="ab34a5e95b76b4b79a72da0734025f211"></a><a name="ab34a5e95b76b4b79a72da0734025f211"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.42%" headers="mcps1.1.5.1.4 "><p id="a716277ae541d4553bb10490f9c02593d"><a name="a716277ae541d4553bb10490f9c02593d"></a><a name="a716277ae541d4553bb10490f9c02593d"></a>该字段内容填为<span class="parmvalue" id="parmvalue123424712599"><a name="parmvalue123424712599"></a><a name="parmvalue123424712599"></a>“application/json;charset=utf8”</span>。</p>
    </td>
    </tr>
    <tr id="row3481201482919"><td class="cellrowborder" valign="top" width="21.42%" headers="mcps1.1.5.1.1 "><p id="p4121821192918"><a name="p4121821192918"></a><a name="p4121821192918"></a>X-Auth-Token</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.939999999999998%" headers="mcps1.1.5.1.2 "><p id="p104841714152913"><a name="p104841714152913"></a><a name="p104841714152913"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.22%" headers="mcps1.1.5.1.3 "><p id="p1484171415293"><a name="p1484171415293"></a><a name="p1484171415293"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.42%" headers="mcps1.1.5.1.4 "><p id="p7188184217297"><a name="p7188184217297"></a><a name="p7188184217297"></a>被委托方用户B具有Agent Operator权限的token，token获取方法请参见：<a href="获取用户Token.md">获取用户Token</a>。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   Request Body参数说明

    <a name="table178290313599"></a>
    <table><thead align="left"><tr id="row178294318597"><th class="cellrowborder" valign="top" width="21.272127212721273%" id="mcps1.1.5.1.1"><p id="p682963165915"><a name="p682963165915"></a><a name="p682963165915"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.92169216921692%" id="mcps1.1.5.1.2"><p id="p1482903105920"><a name="p1482903105920"></a><a name="p1482903105920"></a>是否为必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.261726172617262%" id="mcps1.1.5.1.3"><p id="p18829183145920"><a name="p18829183145920"></a><a name="p18829183145920"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.54445444544455%" id="mcps1.1.5.1.4"><p id="p982911375918"><a name="p982911375918"></a><a name="p982911375918"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row820912912437"><td class="cellrowborder" valign="top" width="21.272127212721273%" headers="mcps1.1.5.1.1 "><p id="p117271323403"><a name="p117271323403"></a><a name="p117271323403"></a>identity</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.92169216921692%" headers="mcps1.1.5.1.2 "><p id="p07279236010"><a name="p07279236010"></a><a name="p07279236010"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.261726172617262%" headers="mcps1.1.5.1.3 "><p id="p1072715231201"><a name="p1072715231201"></a><a name="p1072715231201"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54445444544455%" headers="mcps1.1.5.1.4 "><p id="p12733551037"><a name="p12733551037"></a><a name="p12733551037"></a>认证参数，包含：methods，assume_role。</p>
    <pre class="screen" id="screen4242448102819"><a name="screen4242448102819"></a><a name="screen4242448102819"></a>"identity": {
          "methods": ["assume_role"],
          "assume_role": {</pre>
    </td>
    </tr>
    <tr id="row118480418431"><td class="cellrowborder" valign="top" width="21.272127212721273%" headers="mcps1.1.5.1.1 "><p id="p81848145559"><a name="p81848145559"></a><a name="p81848145559"></a>methods</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.92169216921692%" headers="mcps1.1.5.1.2 "><p id="p19184101415559"><a name="p19184101415559"></a><a name="p19184101415559"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.261726172617262%" headers="mcps1.1.5.1.3 "><p id="p8184131410553"><a name="p8184131410553"></a><a name="p8184131410553"></a>String Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54445444544455%" headers="mcps1.1.5.1.4 "><p id="p101851414175513"><a name="p101851414175513"></a><a name="p101851414175513"></a>token的获取方式，该字段内容为<span class="parmvalue" id="parmvalue1718519140554"><a name="parmvalue1718519140554"></a><a name="parmvalue1718519140554"></a>“assume_role”</span>。</p>
    </td>
    </tr>
    <tr id="row2315147387"><td class="cellrowborder" valign="top" width="21.272127212721273%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0056596910_p4770553481"><a name="zh-cn_topic_0056596910_p4770553481"></a><a name="zh-cn_topic_0056596910_p4770553481"></a>domain_name或domain_id</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.92169216921692%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0056596910_p97709531782"><a name="zh-cn_topic_0056596910_p97709531782"></a><a name="zh-cn_topic_0056596910_p97709531782"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.261726172617262%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0056596910_p07709531487"><a name="zh-cn_topic_0056596910_p07709531487"></a><a name="zh-cn_topic_0056596910_p07709531487"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54445444544455%" headers="mcps1.1.5.1.4 "><p id="a7d17f5dc348644e4a0356f6229a75ad4"><a name="a7d17f5dc348644e4a0356f6229a75ad4"></a><a name="a7d17f5dc348644e4a0356f6229a75ad4"></a>委托方用户A的账号名称或者ID，domain_name和domain_id二选一。</p>
    </td>
    </tr>
    <tr id="row983018318592"><td class="cellrowborder" valign="top" width="21.272127212721273%" headers="mcps1.1.5.1.1 "><p id="p883010311590"><a name="p883010311590"></a><a name="p883010311590"></a>agency_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.92169216921692%" headers="mcps1.1.5.1.2 "><p id="p1783014355918"><a name="p1783014355918"></a><a name="p1783014355918"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.261726172617262%" headers="mcps1.1.5.1.3 "><p id="p583020375917"><a name="p583020375917"></a><a name="p583020375917"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54445444544455%" headers="mcps1.1.5.1.4 "><p id="p19830834595"><a name="p19830834595"></a><a name="p19830834595"></a>委托方用户A创建的委托的名称。</p>
    </td>
    </tr>
    <tr id="row1283411395912"><td class="cellrowborder" valign="top" width="21.272127212721273%" headers="mcps1.1.5.1.1 "><p id="p5835133175915"><a name="p5835133175915"></a><a name="p5835133175915"></a>scope</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.92169216921692%" headers="mcps1.1.5.1.2 "><p id="p14835338590"><a name="p14835338590"></a><a name="p14835338590"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.261726172617262%" headers="mcps1.1.5.1.3 "><p id="p5835113195919"><a name="p5835113195919"></a><a name="p5835113195919"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54445444544455%" headers="mcps1.1.5.1.4 "><p id="p154910141527"><a name="p154910141527"></a><a name="p154910141527"></a>token的使用范围，取值为project或domain，二选一即可。</p>
    <a name="ul13491314628"></a><a name="ul13491314628"></a><ul id="ul13491314628"><li>示例1：取值为project时，表示获取的token仅能访问指定project下的资源，project支持id和name，二选一即可。<pre class="screen" id="screen174911147216"><a name="screen174911147216"></a><a name="screen174911147216"></a>"scope": {
          "project": {
          "id": "0b95b78b67fa045b38104c12fb..."
          "name": "cn-north-1"
          }
        }</pre>
    <div class="note" id="note165016141527"><a name="note165016141527"></a><a name="note165016141527"></a><span class="notetitle"> 说明： </span><div class="notebody"><p id="p1463954416188"><a name="p1463954416188"></a><a name="p1463954416188"></a>使用区域的Endpoint（非全局域名）调用该接口时，推荐您将scope设置为project，该参数需要填入对应区域project的name或者id。</p>
    </div></div>
    </li><li>示例2：取值为domain时，表示获取的Token可以访问委托方账号中授权的所有资源，domain支持id和name，二选一即可。<pre class="screen" id="screen4501614421"><a name="screen4501614421"></a><a name="screen4501614421"></a>"scope": {
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
    <tr id="row138751029927"><td class="cellrowborder" valign="top" width="21.272127212721273%" headers="mcps1.1.5.1.1 "><p id="ab3f196e612a04b36898fca5391c8c71c"><a name="ab3f196e612a04b36898fca5391c8c71c"></a><a name="ab3f196e612a04b36898fca5391c8c71c"></a>nocatalog</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.92169216921692%" headers="mcps1.1.5.1.2 "><p id="ab701027c99914d0aa8bb847a8df6dd5e"><a name="ab701027c99914d0aa8bb847a8df6dd5e"></a><a name="ab701027c99914d0aa8bb847a8df6dd5e"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.261726172617262%" headers="mcps1.1.5.1.3 "><p id="a5fee45d14b11467e90c3ae4231a1c771"><a name="a5fee45d14b11467e90c3ae4231a1c771"></a><a name="a5fee45d14b11467e90c3ae4231a1c771"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54445444544455%" headers="mcps1.1.5.1.4 "><p id="a2c20ed7477cd4f059a3ea425cc7371d0"><a name="a2c20ed7477cd4f059a3ea425cc7371d0"></a><a name="a2c20ed7477cd4f059a3ea425cc7371d0"></a>如果设置该参数，返回的响应体中将不显示catalog信息。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    获取委托方账号名为“A-Company”，委托名称为“agencytest”的委托token。

    ```
    {
        "auth":{
            "identity":{
                "methods":[
                    "assume_role"
                ],
                "assume_role":{
                    "domain_name":"A-Company",
                    "agency_name":"agencytest"
                }
            },
            "scope":{
                "domain":{
                    "name":"A-Company"
                }
            }
        }
    }
    ```


## 响应<a name="s3a08e13bb5b34dc2ba4dcd84a0d51cf5"></a>

-   Response Header参数说明

    <a name="zh-cn_topic_0026585112_table44962972"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0026585112_row49143529"><th class="cellrowborder" valign="top" width="21.22%" id="mcps1.1.5.1.1"><p id="zh-cn_topic_0026585112_p21202951"><a name="zh-cn_topic_0026585112_p21202951"></a><a name="zh-cn_topic_0026585112_p21202951"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.78%" id="mcps1.1.5.1.2"><p id="p862619429218"><a name="p862619429218"></a><a name="p862619429218"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.119999999999997%" id="mcps1.1.5.1.3"><p id="zh-cn_topic_0026585112_p39717481"><a name="zh-cn_topic_0026585112_p39717481"></a><a name="zh-cn_topic_0026585112_p39717481"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.879999999999995%" id="mcps1.1.5.1.4"><p id="zh-cn_topic_0026585112_p62999416"><a name="zh-cn_topic_0026585112_p62999416"></a><a name="zh-cn_topic_0026585112_p62999416"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0026585112_row2679067"><td class="cellrowborder" valign="top" width="21.22%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0026585112_p15677883"><a name="zh-cn_topic_0026585112_p15677883"></a><a name="zh-cn_topic_0026585112_p15677883"></a>X-Subject-Token</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.78%" headers="mcps1.1.5.1.2 "><p id="p9626642329"><a name="p9626642329"></a><a name="p9626642329"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.119999999999997%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0026585112_p61948991"><a name="zh-cn_topic_0026585112_p61948991"></a><a name="zh-cn_topic_0026585112_p61948991"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.879999999999995%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0026585112_p51812368"><a name="zh-cn_topic_0026585112_p51812368"></a><a name="zh-cn_topic_0026585112_p51812368"></a>签名后的委托token。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   Token格式说明

    <a name="t9aa18688b0f44302a45f87a865a4f9d7"></a>
    <table><thead align="left"><tr id="r4495c7bbf2c14d50a55a4ac402e189ca"><th class="cellrowborder" valign="top" width="21.26787321267873%" id="mcps1.1.5.1.1"><p id="a604782cae932448db4a5fe6032c0703e"><a name="a604782cae932448db4a5fe6032c0703e"></a><a name="a604782cae932448db4a5fe6032c0703e"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.728327167283272%" id="mcps1.1.5.1.2"><p id="a6175c8a318d24e39837027e182baaed9"><a name="a6175c8a318d24e39837027e182baaed9"></a><a name="a6175c8a318d24e39837027e182baaed9"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.24827517248275%" id="mcps1.1.5.1.3"><p id="a8ed9dc140ab940ae83066efac4a62450"><a name="a8ed9dc140ab940ae83066efac4a62450"></a><a name="a8ed9dc140ab940ae83066efac4a62450"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.755524447555246%" id="mcps1.1.5.1.4"><p id="a7926893fadf64b0cba9adac5489deefd"><a name="a7926893fadf64b0cba9adac5489deefd"></a><a name="a7926893fadf64b0cba9adac5489deefd"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="rcc2f2253b42941d3976e9118b7899178"><td class="cellrowborder" valign="top" width="21.26787321267873%" headers="mcps1.1.5.1.1 "><p id="a07a6ef85698e438b842d000b6bcbb235"><a name="a07a6ef85698e438b842d000b6bcbb235"></a><a name="a07a6ef85698e438b842d000b6bcbb235"></a>methods</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.728327167283272%" headers="mcps1.1.5.1.2 "><p id="ab83556a39c894a0983c94c05bbe8a92d"><a name="ab83556a39c894a0983c94c05bbe8a92d"></a><a name="ab83556a39c894a0983c94c05bbe8a92d"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24827517248275%" headers="mcps1.1.5.1.3 "><p id="a558b3430e0444f97a88d96cdc036401e"><a name="a558b3430e0444f97a88d96cdc036401e"></a><a name="a558b3430e0444f97a88d96cdc036401e"></a>Json Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="a7b9d6f974d1e4d44890be49309a0382f"><a name="a7b9d6f974d1e4d44890be49309a0382f"></a><a name="a7b9d6f974d1e4d44890be49309a0382f"></a>获取token的方式。</p>
    </td>
    </tr>
    <tr id="r952955421b3345d29a03350797976bef"><td class="cellrowborder" valign="top" width="21.26787321267873%" headers="mcps1.1.5.1.1 "><p id="aec3770aaf9384235aed7d5a3e9b61d34"><a name="aec3770aaf9384235aed7d5a3e9b61d34"></a><a name="aec3770aaf9384235aed7d5a3e9b61d34"></a>expires_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.728327167283272%" headers="mcps1.1.5.1.2 "><p id="a2d5989348dcc4c34ab87e762205e3e25"><a name="a2d5989348dcc4c34ab87e762205e3e25"></a><a name="a2d5989348dcc4c34ab87e762205e3e25"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24827517248275%" headers="mcps1.1.5.1.3 "><p id="a06df05908d2046d6b318f3dbadcad5fa"><a name="a06df05908d2046d6b318f3dbadcad5fa"></a><a name="a06df05908d2046d6b318f3dbadcad5fa"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="af0c635100ad74b489f89c886e157e49b"><a name="af0c635100ad74b489f89c886e157e49b"></a><a name="af0c635100ad74b489f89c886e157e49b"></a>token到期时间。</p>
    </td>
    </tr>
    <tr id="r566af79660784b49a20126aeb8226599"><td class="cellrowborder" valign="top" width="21.26787321267873%" headers="mcps1.1.5.1.1 "><p id="a99ee5815381b446bab5b3b871f0cd77f"><a name="a99ee5815381b446bab5b3b871f0cd77f"></a><a name="a99ee5815381b446bab5b3b871f0cd77f"></a>issued_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.728327167283272%" headers="mcps1.1.5.1.2 "><p id="aa7051ea6df594043a3d18cfbdfb49dc8"><a name="aa7051ea6df594043a3d18cfbdfb49dc8"></a><a name="aa7051ea6df594043a3d18cfbdfb49dc8"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24827517248275%" headers="mcps1.1.5.1.3 "><p id="af1aa454ebf634d428c9498bb88dd9d45"><a name="af1aa454ebf634d428c9498bb88dd9d45"></a><a name="af1aa454ebf634d428c9498bb88dd9d45"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0026585112_p532161155713"><a name="zh-cn_topic_0026585112_p532161155713"></a><a name="zh-cn_topic_0026585112_p532161155713"></a>token产生时间。</p>
    </td>
    </tr>
    <tr id="r2bdea9cf4b4a40ea89733ee4ff3af64a"><td class="cellrowborder" valign="top" width="21.26787321267873%" headers="mcps1.1.5.1.1 "><p id="a313ab3f0623c4e57a9160a072e6a22c9"><a name="a313ab3f0623c4e57a9160a072e6a22c9"></a><a name="a313ab3f0623c4e57a9160a072e6a22c9"></a>user</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.728327167283272%" headers="mcps1.1.5.1.2 "><p id="a87695b24819042c8afa89bf8867ebdf5"><a name="a87695b24819042c8afa89bf8867ebdf5"></a><a name="a87695b24819042c8afa89bf8867ebdf5"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24827517248275%" headers="mcps1.1.5.1.3 "><p id="a27424032f78a40379dddacb5ab25166d"><a name="a27424032f78a40379dddacb5ab25166d"></a><a name="a27424032f78a40379dddacb5ab25166d"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="a220a5e088be14830a1e9db57ad7e9d50"><a name="a220a5e088be14830a1e9db57ad7e9d50"></a><a name="a220a5e088be14830a1e9db57ad7e9d50"></a>委托方用户A的详细信息，示例：</p>
    <pre class="screen" id="s94858990e5764505971cc869331632fc"><a name="s94858990e5764505971cc869331632fc"></a><a name="s94858990e5764505971cc869331632fc"></a>"user": { 
          "name": "<em id="ab903696341a94e65841ad3f0cc988047"><a name="ab903696341a94e65841ad3f0cc988047"></a><a name="ab903696341a94e65841ad3f0cc988047"></a>username</em>", 
          "id": "<em id="zh-cn_topic_0026585112_i433336816519"><a name="zh-cn_topic_0026585112_i433336816519"></a><a name="zh-cn_topic_0026585112_i433336816519"></a>userid</em>", 
          "password_expires_at":"2016-11-06T15:32:17.000000",
          "domain": { 
             "name": "<em id="zh-cn_topic_0026585112_i438354691645"><a name="zh-cn_topic_0026585112_i438354691645"></a><a name="zh-cn_topic_0026585112_i438354691645"></a>domainname</em>",
             "id": "<em id="zh-cn_topic_0026585112_i75268851664"><a name="zh-cn_topic_0026585112_i75268851664"></a><a name="zh-cn_topic_0026585112_i75268851664"></a>domainid</em>"
           } 
        }</pre>
    <a name="ul1414311427419"></a><a name="ul1414311427419"></a><ul id="ul1414311427419"><li>user.name：委托方租户名/委托名。</li><li>user.id：委托ID。</li><li>domain.name：用户所属的账户名称。</li><li>domain.id：用户所属的账户的ID。</li><li>password_expires_at：可选，密码过期时间（UTC时间），<span class="parmvalue" id="parmvalue9377181973011"><a name="parmvalue9377181973011"></a><a name="parmvalue9377181973011"></a>“null”</span>表示密码不过期。</li></ul>
    </td>
    </tr>
    <tr id="rd33372d927214527ac870bb11715c536"><td class="cellrowborder" valign="top" width="21.26787321267873%" headers="mcps1.1.5.1.1 "><p id="a66272c967cb547c09f7a7316b4ae754c"><a name="a66272c967cb547c09f7a7316b4ae754c"></a><a name="a66272c967cb547c09f7a7316b4ae754c"></a>domain</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.728327167283272%" headers="mcps1.1.5.1.2 "><p id="a9183943cbe59479691b60e9c95a74a0d"><a name="a9183943cbe59479691b60e9c95a74a0d"></a><a name="a9183943cbe59479691b60e9c95a74a0d"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24827517248275%" headers="mcps1.1.5.1.3 "><p id="a06d0695f36184007ab70f95018c90a92"><a name="a06d0695f36184007ab70f95018c90a92"></a><a name="a06d0695f36184007ab70f95018c90a92"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="p1963811012015"><a name="p1963811012015"></a><a name="p1963811012015"></a>如果请求体中scope参数设置为domain，则返回该字段。</p>
    <p id="a4a60927497a74911bd2ab640524d9633"><a name="a4a60927497a74911bd2ab640524d9633"></a><a name="a4a60927497a74911bd2ab640524d9633"></a>示例：</p>
    <pre class="screen" id="s6426dc53b2a4457ea51cc7ea9e64f456"><a name="s6426dc53b2a4457ea51cc7ea9e64f456"></a><a name="s6426dc53b2a4457ea51cc7ea9e64f456"></a>"domain": { 
          "name" : "<em id="i73871258304"><a name="i73871258304"></a><a name="i73871258304"></a>domainname</em>",     
          "id" : "<em id="i17061511305"><a name="i17061511305"></a><a name="i17061511305"></a>domainid</em>"
    }</pre>
    <a name="ul1274024713413"></a><a name="ul1274024713413"></a><ul id="ul1274024713413"><li>domain.name<em id="i144721032749"><a name="i144721032749"></a><a name="i144721032749"></a>：</em>委托方用户所属的账户名称。</li><li>domain.id<em id="a929ca2dc9f8d4dc488c64a5424f037ce"><a name="a929ca2dc9f8d4dc488c64a5424f037ce"></a><a name="a929ca2dc9f8d4dc488c64a5424f037ce"></a>：</em>委托方用户所属的账户ID。</li></ul>
    </td>
    </tr>
    <tr id="r3a914bf0c52c43e390883648cbe964ff"><td class="cellrowborder" valign="top" width="21.26787321267873%" headers="mcps1.1.5.1.1 "><p id="a0e6de929a1ea4db0b88e97acb4287d5e"><a name="a0e6de929a1ea4db0b88e97acb4287d5e"></a><a name="a0e6de929a1ea4db0b88e97acb4287d5e"></a>project</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.728327167283272%" headers="mcps1.1.5.1.2 "><p id="a346f8467c2e24793ab55c120fc37852f"><a name="a346f8467c2e24793ab55c120fc37852f"></a><a name="a346f8467c2e24793ab55c120fc37852f"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24827517248275%" headers="mcps1.1.5.1.3 "><p id="af6953054960f4c59903b92961b10b426"><a name="af6953054960f4c59903b92961b10b426"></a><a name="af6953054960f4c59903b92961b10b426"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="a41001b564477400f98aef711e86f0197"><a name="a41001b564477400f98aef711e86f0197"></a><a name="a41001b564477400f98aef711e86f0197"></a>如果请求体中scope参数设置为project，则返回该字段。</p>
    <p id="a2658c45981e64570b63c49c45cfdfac7"><a name="a2658c45981e64570b63c49c45cfdfac7"></a><a name="a2658c45981e64570b63c49c45cfdfac7"></a>示例：</p>
    <pre class="screen" id="s75cd01f2f3df45ada904958dc41f5307"><a name="s75cd01f2f3df45ada904958dc41f5307"></a><a name="s75cd01f2f3df45ada904958dc41f5307"></a>"project": { 
          "name": "<em id="af63ef597e10344ecaada944624eefa21"><a name="af63ef597e10344ecaada944624eefa21"></a><a name="af63ef597e10344ecaada944624eefa21"></a>projectname</em>", 
          "id": "<em id="zh-cn_topic_0026585112_i86520761696"><a name="zh-cn_topic_0026585112_i86520761696"></a><a name="zh-cn_topic_0026585112_i86520761696"></a>projectid</em>"
    }</pre>
    <a name="ul86769381572"></a><a name="ul86769381572"></a><ul id="ul86769381572"><li>project.name：project名称。</li><li>project.id：project的ID。</li></ul>
    </td>
    </tr>
    <tr id="row31009604113628"><td class="cellrowborder" valign="top" width="21.26787321267873%" headers="mcps1.1.5.1.1 "><p id="p22717013113628"><a name="p22717013113628"></a><a name="p22717013113628"></a>catalog</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.728327167283272%" headers="mcps1.1.5.1.2 "><p id="p54936595113628"><a name="p54936595113628"></a><a name="p54936595113628"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24827517248275%" headers="mcps1.1.5.1.3 "><p id="p46529556113628"><a name="p46529556113628"></a><a name="p46529556113628"></a>Json Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="p45368001113628"><a name="p45368001113628"></a><a name="p45368001113628"></a>endpoints相关信息。</p>
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
    <tr id="r57913d5a1da24c699a412dced6a7b573"><td class="cellrowborder" valign="top" width="21.26787321267873%" headers="mcps1.1.5.1.1 "><p id="a45bd202186b249bfa8fc87bbcbf05bb9"><a name="a45bd202186b249bfa8fc87bbcbf05bb9"></a><a name="a45bd202186b249bfa8fc87bbcbf05bb9"></a>roles</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.728327167283272%" headers="mcps1.1.5.1.2 "><p id="ae5cf82a55c21452aa028ff59e6973404"><a name="ae5cf82a55c21452aa028ff59e6973404"></a><a name="ae5cf82a55c21452aa028ff59e6973404"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24827517248275%" headers="mcps1.1.5.1.3 "><p id="aa1fb3d35fbda45208e6e58dbbbc00b01"><a name="aa1fb3d35fbda45208e6e58dbbbc00b01"></a><a name="aa1fb3d35fbda45208e6e58dbbbc00b01"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="a18bf24a442094153ab2a8f7391737d06"><a name="a18bf24a442094153ab2a8f7391737d06"></a><a name="a18bf24a442094153ab2a8f7391737d06"></a>Token的权限信息。</p>
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
    <tr id="row1930784083617"><td class="cellrowborder" valign="top" width="21.26787321267873%" headers="mcps1.1.5.1.1 "><p id="p3307174016361"><a name="p3307174016361"></a><a name="p3307174016361"></a>assumed_by</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.728327167283272%" headers="mcps1.1.5.1.2 "><p id="p93071640163616"><a name="p93071640163616"></a><a name="p93071640163616"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24827517248275%" headers="mcps1.1.5.1.3 "><p id="p16353154163614"><a name="p16353154163614"></a><a name="p16353154163614"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="p5760121404010"><a name="p5760121404010"></a><a name="p5760121404010"></a>被委托方用户B的详细信息。</p>
    <p id="p1855720205374"><a name="p1855720205374"></a><a name="p1855720205374"></a>示例：</p>
    <pre class="screen" id="screen171913204147"><a name="screen171913204147"></a><a name="screen171913204147"></a>"assumed_by": {
          "user": {
            "domain": {
              "name": "User B",
              "id": "bfdd55e02a014894b5a2693f31..."
            },
            "name": "assumedusername",
            "id": "ff5ea657f1dd45c4b8f398cab..."
          }
        }</pre>
    <a name="ul219615366138"></a><a name="ul219615366138"></a><ul id="ul219615366138"><li>domain.name：被委托方用户B所属的账户名称。</li><li>user.name：被委托方用户B的用户名称。</li></ul>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    样例中domain、user、role和assumed\_by的关系为：domain为委托方的华为云账号，账号是资源归属、资源使用计费的主体，对其所拥有的资源及云服务具有完全的访问权限，可以创建用户和用户组、分配用户权限等；user为实际创建委托的用户，user本身由账号在IAM中创建，是账号中的子用户，权限由账号分配。如果是账号本身创建的委托，则domain和user信息一致；role为获取的委托token具备的权限；assumed\_by为被委托方用户的详细信息。

    ```
    Response Header中存储信息为：
    X-Subject-Token:MIIDkgYJKoZIhvcNAQcCoIIDgzCCA38CAQExDTALBglghkgBZQMEAgEwgXXXXX...
    
    X-Frame-Options: SAMEORIGIN
    
    Response Body中存储信息为：
    {
      "token": {
        "methods": [
          "assume_role"
        ],
        "issued_at": "2017-05-18T11:44:05.232000Z",
        "expires_at": "2017-05-19T11:44:05.232000Z",
        "user": {
          "id": "93e12ecdad6f4abd84968741da...",
          "name": "A-Company/agencytest",
          "password_expires_at":"2016-11-06T15:32:17.000000",
          "domain": {
            "id": "ce925c42c25943bebba10ea64a...",
            "name": "A-Company"
          }
        },
        "domain": {
          "id": "ce925c42c25943bebba10ea64a...",
          "name": "A-Company"
        },
        "roles": [
          {
            "id": "c11c61319f08404eaf94f8030b9...",
            "name": "role1"
          },
          {
            "id": "d52dde35ijg62fex2ijhdc785sc3...",
            "name": "role2"
          },
          {
            "id": "d862dwd32dwhu854rdcs447ed1d7..."
            "name": "op_gated_tasssg6"
          }
        ],
        "assumed_by": {
          "user": {
            "domain": {
              "name": "B-Company",
              "id": "c1a78a82d81c4a19b03bfe82d3ad..."
            },
            "id": "cdeb158dda854cc3bab77d8926ff...",
            "name": "User B"
          }
        }
      }
    }
    ```


## 状态码<a name="sbfe93ca4c2b9427dbb2218a4e72da6a8"></a>

<a name="zh-cn_topic_0026585112_table34550710"></a>
<table><thead align="left"><tr id="zh-cn_topic_0026585112_row8352109"><th class="cellrowborder" valign="top" width="50.029999999999994%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0026585112_p5432205"><a name="zh-cn_topic_0026585112_p5432205"></a><a name="zh-cn_topic_0026585112_p5432205"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="49.97%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0026585112_p37355470"><a name="zh-cn_topic_0026585112_p37355470"></a><a name="zh-cn_topic_0026585112_p37355470"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0026585112_row5894231"><td class="cellrowborder" valign="top" width="50.029999999999994%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p7670737"><a name="zh-cn_topic_0026585112_p7670737"></a><a name="zh-cn_topic_0026585112_p7670737"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="49.97%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0026585112_p17349988"><a name="zh-cn_topic_0026585112_p17349988"></a><a name="zh-cn_topic_0026585112_p17349988"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0026585112_row21932166"><td class="cellrowborder" valign="top" width="50.029999999999994%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p31674992"><a name="zh-cn_topic_0026585112_p31674992"></a><a name="zh-cn_topic_0026585112_p31674992"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="49.97%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0026585112_p15537542"><a name="zh-cn_topic_0026585112_p15537542"></a><a name="zh-cn_topic_0026585112_p15537542"></a>请求错误。</p>
</td>
</tr>
<tr id="r22bf632ff3984ffbaa2734a029063cfb"><td class="cellrowborder" valign="top" width="50.029999999999994%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p947606916650"><a name="zh-cn_topic_0026585112_p947606916650"></a><a name="zh-cn_topic_0026585112_p947606916650"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="49.97%" headers="mcps1.1.3.1.2 "><p id="a3a62e2f9d6c84b4083dfb8b2ade8e14c"><a name="a3a62e2f9d6c84b4083dfb8b2ade8e14c"></a><a name="a3a62e2f9d6c84b4083dfb8b2ade8e14c"></a>认证失败。</p>
</td>
</tr>
<tr id="r41d0d854619349f898c16f7c61792083"><td class="cellrowborder" valign="top" width="50.029999999999994%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p762821816657"><a name="zh-cn_topic_0026585112_p762821816657"></a><a name="zh-cn_topic_0026585112_p762821816657"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="49.97%" headers="mcps1.1.3.1.2 "><p id="a0261fc1955104ca3b1f0a46388724624"><a name="a0261fc1955104ca3b1f0a46388724624"></a><a name="a0261fc1955104ca3b1f0a46388724624"></a>鉴权失败。（可能原因：被委托方用户缺少Agent Operator权限，请添加权限）</p>
</td>
</tr>
<tr id="rea66e1a745ee4e0882be6b9f5349ac4d"><td class="cellrowborder" valign="top" width="50.029999999999994%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p486971841676"><a name="zh-cn_topic_0026585112_p486971841676"></a><a name="zh-cn_topic_0026585112_p486971841676"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="49.97%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0026585112_p521578261676"><a name="zh-cn_topic_0026585112_p521578261676"></a><a name="zh-cn_topic_0026585112_p521578261676"></a>找不到资源。</p>
</td>
</tr>
<tr id="r230ba1b5ddec4cd0a41a5c37806e60f5"><td class="cellrowborder" valign="top" width="50.029999999999994%" headers="mcps1.1.3.1.1 "><p id="af8f4513c90d344e3b90952b53e3ee015"><a name="af8f4513c90d344e3b90952b53e3ee015"></a><a name="af8f4513c90d344e3b90952b53e3ee015"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="49.97%" headers="mcps1.1.3.1.2 "><p id="a19c27fd6b377464898ec6cae5778ec80"><a name="a19c27fd6b377464898ec6cae5778ec80"></a><a name="a19c27fd6b377464898ec6cae5778ec80"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0026585112_row6824316711"><td class="cellrowborder" valign="top" width="50.029999999999994%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p61418816711"><a name="zh-cn_topic_0026585112_p61418816711"></a><a name="zh-cn_topic_0026585112_p61418816711"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="49.97%" headers="mcps1.1.3.1.2 "><p id="a4bc003bda05e465eb3a3f0f989888213"><a name="a4bc003bda05e465eb3a3f0f989888213"></a><a name="a4bc003bda05e465eb3a3f0f989888213"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

