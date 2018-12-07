# 通过assume\_role方式获取用户token<a name="ZH-CN_TOPIC_0110485052"></a>

## 功能介绍<a name="s5888597838b0425a92e3419fb766c7f5"></a>

该接口用来获取委托用户的token，需要通过assume\_role的方式进行认证。例如：用户A委托用户B管理用户A中的某些资源，那么用户B可以通过assume\_role方式获取用户A的token。

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
    <td class="cellrowborder" valign="top" width="44.42%" headers="mcps1.1.5.1.4 "><p id="p7188184217297"><a name="p7188184217297"></a><a name="p7188184217297"></a>已认证的拥有Agent Operator权限的token。</p>
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
    <tbody><tr id="row108297317594"><td class="cellrowborder" valign="top" width="21.272127212721273%" headers="mcps1.1.5.1.1 "><p id="p283019305918"><a name="p283019305918"></a><a name="p283019305918"></a>methods</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.92169216921692%" headers="mcps1.1.5.1.2 "><p id="p148301735596"><a name="p148301735596"></a><a name="p148301735596"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.261726172617262%" headers="mcps1.1.5.1.3 "><p id="p178304311599"><a name="p178304311599"></a><a name="p178304311599"></a>String Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54445444544455%" headers="mcps1.1.5.1.4 "><p id="p683083165918"><a name="p683083165918"></a><a name="p683083165918"></a>该字段内容填为<span class="parmvalue" id="parmvalue4718752175915"><a name="parmvalue4718752175915"></a><a name="parmvalue4718752175915"></a>“assume_role”</span>。</p>
    </td>
    </tr>
    <tr id="row6830131594"><td class="cellrowborder" valign="top" width="21.272127212721273%" headers="mcps1.1.5.1.1 "><p id="p148301031596"><a name="p148301031596"></a><a name="p148301031596"></a>domain_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.92169216921692%" headers="mcps1.1.5.1.2 "><p id="p183015345918"><a name="p183015345918"></a><a name="p183015345918"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.261726172617262%" headers="mcps1.1.5.1.3 "><p id="p168307325915"><a name="p168307325915"></a><a name="p168307325915"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54445444544455%" headers="mcps1.1.5.1.4 "><p id="p18306325915"><a name="p18306325915"></a><a name="p18306325915"></a>指定租户名称。</p>
    </td>
    </tr>
    <tr id="row983018318592"><td class="cellrowborder" valign="top" width="21.272127212721273%" headers="mcps1.1.5.1.1 "><p id="p883010311590"><a name="p883010311590"></a><a name="p883010311590"></a>xrole_name</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.92169216921692%" headers="mcps1.1.5.1.2 "><p id="p1783014355918"><a name="p1783014355918"></a><a name="p1783014355918"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.261726172617262%" headers="mcps1.1.5.1.3 "><p id="p583020375917"><a name="p583020375917"></a><a name="p583020375917"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54445444544455%" headers="mcps1.1.5.1.4 "><p id="p19830834595"><a name="p19830834595"></a><a name="p19830834595"></a>委托名称。</p>
    </td>
    </tr>
    <tr id="row128341237593"><td class="cellrowborder" valign="top" width="21.272127212721273%" headers="mcps1.1.5.1.1 "><p id="p1983412318591"><a name="p1983412318591"></a><a name="p1983412318591"></a>roles</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.92169216921692%" headers="mcps1.1.5.1.2 "><p id="p1483443145911"><a name="p1483443145911"></a><a name="p1483443145911"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.261726172617262%" headers="mcps1.1.5.1.3 "><p id="p13834839594"><a name="p13834839594"></a><a name="p13834839594"></a>List Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54445444544455%" headers="mcps1.1.5.1.4 "><p id="p1883412375914"><a name="p1883412375914"></a><a name="p1883412375914"></a>权限信息。</p>
    </td>
    </tr>
    <tr id="row1283411395912"><td class="cellrowborder" valign="top" width="21.272127212721273%" headers="mcps1.1.5.1.1 "><p id="p5835133175915"><a name="p5835133175915"></a><a name="p5835133175915"></a>scope</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.92169216921692%" headers="mcps1.1.5.1.2 "><p id="p14835338590"><a name="p14835338590"></a><a name="p14835338590"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.261726172617262%" headers="mcps1.1.5.1.3 "><p id="p5835113195919"><a name="p5835113195919"></a><a name="p5835113195919"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.54445444544455%" headers="mcps1.1.5.1.4 "><p id="p183513385917"><a name="p183513385917"></a><a name="p183513385917"></a>token所属范围信息。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例：

    ```
    curl -i -k -H 'X-Auth-Token:$token' -H 'Content-Type:application/json;charset=utf8' -X POST -d '{"auth": {"identity":{"methods": ["assume_role"],"assume_role":{"domain_name":"exampledomain" ,"xrole_name":"exampleagency",}},"scope": {"domain":{"name": "exampledomain"}}}}' https://sample.domain.com/v3/auth/tokens
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
    <td class="cellrowborder" valign="top" width="44.879999999999995%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0026585112_p51812368"><a name="zh-cn_topic_0026585112_p51812368"></a><a name="zh-cn_topic_0026585112_p51812368"></a>签名后的token。</p>
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
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="a220a5e088be14830a1e9db57ad7e9d50"><a name="a220a5e088be14830a1e9db57ad7e9d50"></a><a name="a220a5e088be14830a1e9db57ad7e9d50"></a>示例：</p>
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
    <p id="p6447153513232"><a name="p6447153513232"></a><a name="p6447153513232"></a>password_expires_at：可选，密码过期时间（UTC时间），<span class="parmvalue" id="parmvalue9377181973011"><a name="parmvalue9377181973011"></a><a name="parmvalue9377181973011"></a>“null”</span>表示密码不过期。</p>
    </td>
    </tr>
    <tr id="rd33372d927214527ac870bb11715c536"><td class="cellrowborder" valign="top" width="21.26787321267873%" headers="mcps1.1.5.1.1 "><p id="a66272c967cb547c09f7a7316b4ae754c"><a name="a66272c967cb547c09f7a7316b4ae754c"></a><a name="a66272c967cb547c09f7a7316b4ae754c"></a>domain</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.728327167283272%" headers="mcps1.1.5.1.2 "><p id="a9183943cbe59479691b60e9c95a74a0d"><a name="a9183943cbe59479691b60e9c95a74a0d"></a><a name="a9183943cbe59479691b60e9c95a74a0d"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24827517248275%" headers="mcps1.1.5.1.3 "><p id="a06d0695f36184007ab70f95018c90a92"><a name="a06d0695f36184007ab70f95018c90a92"></a><a name="a06d0695f36184007ab70f95018c90a92"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="a72f97dddf8204ffb93f87e0d6ae2111f"><a name="a72f97dddf8204ffb93f87e0d6ae2111f"></a><a name="a72f97dddf8204ffb93f87e0d6ae2111f"></a>根据请求中的scope，判断是否返回该字段。</p>
    <p id="a4a60927497a74911bd2ab640524d9633"><a name="a4a60927497a74911bd2ab640524d9633"></a><a name="a4a60927497a74911bd2ab640524d9633"></a>示例：</p>
    <pre class="screen" id="s6426dc53b2a4457ea51cc7ea9e64f456"><a name="s6426dc53b2a4457ea51cc7ea9e64f456"></a><a name="s6426dc53b2a4457ea51cc7ea9e64f456"></a>"domain": { 
          "name" : "domainame",     
          "id" : "domainid"
    }</pre>
    <p id="a16cd99c4957d4834a871cfa10891897b"><a name="a16cd99c4957d4834a871cfa10891897b"></a><a name="a16cd99c4957d4834a871cfa10891897b"></a>domainname<em id="aa778606b54604456919e7183a40559f1"><a name="aa778606b54604456919e7183a40559f1"></a><a name="aa778606b54604456919e7183a40559f1"></a>：</em>企业账户名称。</p>
    <p id="abbaa49e0412d4820aa46f8ed83c8f296"><a name="abbaa49e0412d4820aa46f8ed83c8f296"></a><a name="abbaa49e0412d4820aa46f8ed83c8f296"></a>domainid<em id="a929ca2dc9f8d4dc488c64a5424f037ce"><a name="a929ca2dc9f8d4dc488c64a5424f037ce"></a><a name="a929ca2dc9f8d4dc488c64a5424f037ce"></a>：</em>企业账户的ID。</p>
    </td>
    </tr>
    <tr id="r3a914bf0c52c43e390883648cbe964ff"><td class="cellrowborder" valign="top" width="21.26787321267873%" headers="mcps1.1.5.1.1 "><p id="a0e6de929a1ea4db0b88e97acb4287d5e"><a name="a0e6de929a1ea4db0b88e97acb4287d5e"></a><a name="a0e6de929a1ea4db0b88e97acb4287d5e"></a>project</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.728327167283272%" headers="mcps1.1.5.1.2 "><p id="a346f8467c2e24793ab55c120fc37852f"><a name="a346f8467c2e24793ab55c120fc37852f"></a><a name="a346f8467c2e24793ab55c120fc37852f"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.24827517248275%" headers="mcps1.1.5.1.3 "><p id="af6953054960f4c59903b92961b10b426"><a name="af6953054960f4c59903b92961b10b426"></a><a name="af6953054960f4c59903b92961b10b426"></a>Json Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="a41001b564477400f98aef711e86f0197"><a name="a41001b564477400f98aef711e86f0197"></a><a name="a41001b564477400f98aef711e86f0197"></a>根据请求中的scope，判断是否返回该字段。</p>
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
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="a18bf24a442094153ab2a8f7391737d06"><a name="a18bf24a442094153ab2a8f7391737d06"></a><a name="a18bf24a442094153ab2a8f7391737d06"></a>角色列表。</p>
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
    <td class="cellrowborder" valign="top" width="44.755524447555246%" headers="mcps1.1.5.1.4 "><p id="p5760121404010"><a name="p5760121404010"></a><a name="p5760121404010"></a>被委托的用户信息。</p>
    <p id="p1855720205374"><a name="p1855720205374"></a><a name="p1855720205374"></a>示例：</p>
    <pre class="screen" id="screen13500076392"><a name="screen13500076392"></a><a name="screen13500076392"></a>"assumed_by": {
          "user": {
            "domain": {
              "name": "assumeddomainname",
              "id": "bfdd55e02a014894b5a2693f31539bba"
            },
            "name": "assumedusername",
            "id": "ff5ea657f1dd45c4b8f398cab9c145d1"
          }
        }</pre>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    Response Header中存储信息为：
    X-Subject-Token: MIIE9gYJKoZIhvcNAQcCoIIE5zCCBOMCAQExDTALBglghkgBZQMEAgEwggNEBgkqhkiG9w0BBwGgggM1BIIDMXsidG9rZW4iOnsibWV0aG9kcyI6WyJod19hc3N1bWVfcm9sZSJdLCJpc3N1ZWRfYXQiOiIyMDE3LTA1LTE4VDExOjQ0OjA1LjIzMjAwMFoiLCJleHBpcmVzX2F0IjoiMjAxNy0wNS0xOVQxMTo0NDowNS4yMzIwMDBaIiwidXNlciI6eyJpZCI6IjkzZTEyZWNkYWQ2ZjRhYmQ4NDk2ODc0MWRhZjVjNmEzIiwibmFtZSI6ImppeGlhbmcxL29wX3NlcnZpY2UiLCJkb21haW4iOnsiaWQiOiJjZTkyNWM0MmMyNTk0M2JlYmJhMTBlYTY0YWY5MzEwMiIsIm5hbWUiOiJqaXhpYW5nMSJ9fSwiZG9tYWluIjp7ImlkIjoiY2U5MjVjNDJjMjU5NDNiZWJiYTEwZWE2NGFmOTMxMDIiLCJuYW1lIjoiaml4aWFuZzEifSwicm9sZXMiOlt7ImlkIjoiYzExYzYxMzE5ZjA4NDA0ZWFmOTRmODAzMGI5ZDM3YmIiLCJuYW1lIjoic2VjdV9hZG1pbiJ9LHsiaWQiOiIwIiwibmFtZSI6Im9wX2xlZ2FjeSJ9LHsiaWQiOiIwIiwibmFtZSI6Im9wX3Jlc3RyaWN0ZWQifSx7ImlkIjoiMCIsIm5hbWUiOiJvcF9nYXRlZF90YXNzc2cxIn0seyJpZCI6IjAiLCJuYW1lIjoib3BfZ2F0ZWRfdGFzc3NnMiJ9LHsiaWQiOiIwIiwibmFtZSI6Im9wX2dhdGVkX3Rhc3NzZzQifSx7ImlkIjoiMCIsIm5hbWUiOiJvcF9nYXRlZF90YXNzc2c1In0seyJpZCI6IjAiLCJuYW1lIjoib3BfZ2F0ZWRfdGFzc3NnNiJ9XSwiYXNzdW1lZF9ieSI6eyJ1c2VyIjp7ImRvbWFpbiI6eyJuYW1lIjoib3Bfc2VydmljZSIsImlkIjoiYzFhNzhhODJkODFjNGExOWIwM2JmZTgyZDNhZGQ1ZTUifSwiaWQiOiJjZGViMTU4ZGRhODU0Y2MzYmFiNzdkODkyNmZmZWNmMyIsIm5hbWUiOiJyb2xlX191c2VyIn19fX0xggGFMIIBgQIBATBcMFcxCzAJBgNVBAYTAlVTMQ4wDAYDVQQIDAVVbnNldDEOMAwGA1UEBwwFVW5zZXQxDjAMBgNVBAoMBVVuc2V0MRgwFgYDVQQDDA93d3cuZXhhbXBsZS5jb20CAQEwCwYJYIZIAWUDBAIBMA0GCSqGSIb3DQEBAQUABIIBAB4IaWWzCwmqxH+ht4ZNWdvhwZ5NNAH1lcCeCjtEvKwu9jOAieeirCx6JjWcbN-uC0kRDHrAny3k-j02yAuGW0ndrzXDHQUC8PHzCdk3UPvJnwJdHp7drWIszPfDEM3ThwZTnq27gQY5V0MNFaoJKITtZhK2KcD7zD5GDFMRKF3pM5vy3naAd4dXCHCfoDsDxHt8XgrYjHEqlKmI-L2ScGBCuZAqQ0L4FwQYQ7W7QDW9ra1m9lo30KVdtWI0wb0vaUVx5OWcOPZVoQbJLyuZiX7b-u0c7lsQ34KegTHwgmWyUNJVfqxQPt8FFhoiXPSiFHVkhz++ioAd8ec-FeABbe8=
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
          "id": "93e12ecdad6f4abd84968741daf5c6a3",
          "name": "exampledomain/op_service",
          "password_expires_at":"2016-11-06T15:32:17.000000",
          "domain": {
            "id": "ce925c42c25943bebba10ea64af93102",
            "name": "exampledomain"
          }
        },
        "domain": {
          "id": "ce925c42c25943bebba10ea64af93102",
          "name": "exampledomain"
        },
        "roles": [
          {
            "id": "c11c61319f08404eaf94f8030b9d37bb",
            "name": "secu_admin"
          },
          {
            "id": "0",
            "name": "op_legacy"
          },
          {
            "id": "0",
            "name": "op_gated_tasssg1"
          },
          {
            "id": "0",
            "name": "op_gated_tasssg2"
          },
          {
            "id": "0",
            "name": "op_gated_tasssg4"
          },
          {
            "id": "0",
            "name": "op_gated_tasssg5"
          },
          {
            "id": "0",
            "name": "op_gated_tasssg6"
          }
        ],
        "assumed_by": {
          "user": {
            "domain": {
              "name": "examplename",
              "id": "c1a78a82d81c4a19b03bfe82d3add5e5"
            },
            "id": "cdeb158dda854cc3bab77d8926ffecf3",
            "name": "exampleusername"
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
<td class="cellrowborder" valign="top" width="49.97%" headers="mcps1.1.3.1.2 "><p id="a0261fc1955104ca3b1f0a46388724624"><a name="a0261fc1955104ca3b1f0a46388724624"></a><a name="a0261fc1955104ca3b1f0a46388724624"></a>鉴权失败。</p>
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

