# 获取联邦认证scoped token<a name="ZH-CN_TOPIC_0110485035"></a>

## 功能介绍<a name="section42419535165356"></a>

该接口用于通过联邦认证方式获取scoped token。

## URI<a name="section53764282165356"></a>

URI格式

POST /v3/auth/tokens

## 请求<a name="section27720749165356"></a>

-   Request Header参数说明

    <a name="table30788231165356"></a>
    <table><thead align="left"><tr id="row30649228165356"><th class="cellrowborder" valign="top" width="18.801880188018803%" id="mcps1.1.5.1.1"><p id="p66668440165356"><a name="p66668440165356"></a><a name="p66668440165356"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.921892189218923%" id="mcps1.1.5.1.2"><p id="p31434527165356"><a name="p31434527165356"></a><a name="p31434527165356"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.31183118311831%" id="mcps1.1.5.1.3"><p id="p63168779165356"><a name="p63168779165356"></a><a name="p63168779165356"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.96439643964396%" id="mcps1.1.5.1.4"><p id="p16397508165356"><a name="p16397508165356"></a><a name="p16397508165356"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row53129777165356"><td class="cellrowborder" valign="top" width="18.801880188018803%" headers="mcps1.1.5.1.1 "><p id="p8544699165356"><a name="p8544699165356"></a><a name="p8544699165356"></a>identity</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.921892189218923%" headers="mcps1.1.5.1.2 "><p id="p21032009165356"><a name="p21032009165356"></a><a name="p21032009165356"></a>Dict</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.31183118311831%" headers="mcps1.1.5.1.3 "><p id="p25871172165356"><a name="p25871172165356"></a><a name="p25871172165356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.96439643964396%" headers="mcps1.1.5.1.4 "><p id="p15190163165356"><a name="p15190163165356"></a><a name="p15190163165356"></a>鉴权信息（用户密码）。</p>
    </td>
    </tr>
    <tr id="row2493742165356"><td class="cellrowborder" valign="top" width="18.801880188018803%" headers="mcps1.1.5.1.1 "><p id="p666519165356"><a name="p666519165356"></a><a name="p666519165356"></a>scope</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.921892189218923%" headers="mcps1.1.5.1.2 "><p id="p53988040165356"><a name="p53988040165356"></a><a name="p53988040165356"></a>Dict</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.31183118311831%" headers="mcps1.1.5.1.3 "><p id="p10955114165356"><a name="p10955114165356"></a><a name="p10955114165356"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.96439643964396%" headers="mcps1.1.5.1.4 "><p id="p14949028165356"><a name="p14949028165356"></a><a name="p14949028165356"></a>Token所属范围信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   identity格式

    <a name="table27471026124712"></a>
    <table><thead align="left"><tr id="row19745112634711"><th class="cellrowborder" valign="top" width="18.828117188281173%" id="mcps1.1.5.1.1"><p id="p374315264471"><a name="p374315264471"></a><a name="p374315264471"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.938106189381063%" id="mcps1.1.5.1.2"><p id="p77441262478"><a name="p77441262478"></a><a name="p77441262478"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.098190180981902%" id="mcps1.1.5.1.3"><p id="p127441426154710"><a name="p127441426154710"></a><a name="p127441426154710"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.13558644135587%" id="mcps1.1.5.1.4"><p id="p1674414264474"><a name="p1674414264474"></a><a name="p1674414264474"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1274672684715"><td class="cellrowborder" valign="top" width="18.828117188281173%" headers="mcps1.1.5.1.1 "><p id="p174572624718"><a name="p174572624718"></a><a name="p174572624718"></a>methods</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.938106189381063%" headers="mcps1.1.5.1.2 "><p id="p0745152644712"><a name="p0745152644712"></a><a name="p0745152644712"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.098190180981902%" headers="mcps1.1.5.1.3 "><p id="p107451826104714"><a name="p107451826104714"></a><a name="p107451826104714"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.13558644135587%" headers="mcps1.1.5.1.4 "><p id="p874672694719"><a name="p874672694719"></a><a name="p874672694719"></a>token。</p>
    </td>
    </tr>
    <tr id="row9747162684713"><td class="cellrowborder" valign="top" width="18.828117188281173%" headers="mcps1.1.5.1.1 "><p id="p974632614716"><a name="p974632614716"></a><a name="p974632614716"></a>token</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.938106189381063%" headers="mcps1.1.5.1.2 "><p id="p18746102613478"><a name="p18746102613478"></a><a name="p18746102613478"></a>Dict</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.098190180981902%" headers="mcps1.1.5.1.3 "><p id="p137461226154713"><a name="p137461226154713"></a><a name="p137461226154713"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.13558644135587%" headers="mcps1.1.5.1.4 "><p id="p6747626184710"><a name="p6747626184710"></a><a name="p6747626184710"></a>联邦unscoped token。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   token格式

    <a name="table58557049165356"></a>
    <table><thead align="left"><tr id="row57181345165356"><th class="cellrowborder" valign="top" width="18.5%" id="mcps1.1.5.1.1"><p id="p1177374165356"><a name="p1177374165356"></a><a name="p1177374165356"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.15%" id="mcps1.1.5.1.2"><p id="p28258488165356"><a name="p28258488165356"></a><a name="p28258488165356"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.23%" id="mcps1.1.5.1.3"><p id="p7236182165356"><a name="p7236182165356"></a><a name="p7236182165356"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.12%" id="mcps1.1.5.1.4"><p id="p49259873165356"><a name="p49259873165356"></a><a name="p49259873165356"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row30626752165356"><td class="cellrowborder" valign="top" width="18.5%" headers="mcps1.1.5.1.1 "><p id="p64847836165356"><a name="p64847836165356"></a><a name="p64847836165356"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.15%" headers="mcps1.1.5.1.2 "><p id="p18183324165356"><a name="p18183324165356"></a><a name="p18183324165356"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.23%" headers="mcps1.1.5.1.3 "><p id="p63563112165356"><a name="p63563112165356"></a><a name="p63563112165356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.12%" headers="mcps1.1.5.1.4 "><p id="p48338473165356"><a name="p48338473165356"></a><a name="p48338473165356"></a>用于鉴权的联邦unscoped token ID。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   scope格式

    <a name="table885236173217"></a>
    <table><thead align="left"><tr id="row685112653213"><th class="cellrowborder" valign="top" width="18.51814818518148%" id="mcps1.1.5.1.1"><p id="p16851136173217"><a name="p16851136173217"></a><a name="p16851136173217"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.868113188681132%" id="mcps1.1.5.1.2"><p id="p10851176113213"><a name="p10851176113213"></a><a name="p10851176113213"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.528147185281473%" id="mcps1.1.5.1.3"><p id="p198511162322"><a name="p198511162322"></a><a name="p198511162322"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.085591440855914%" id="mcps1.1.5.1.4"><p id="p10851186113210"><a name="p10851186113210"></a><a name="p10851186113210"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1285117612323"><td class="cellrowborder" valign="top" width="18.51814818518148%" headers="mcps1.1.5.1.1 "><p id="p19851186123215"><a name="p19851186123215"></a><a name="p19851186123215"></a>project</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.1.5.1.2 "><p id="p17851196103215"><a name="p17851196103215"></a><a name="p17851196103215"></a>Dict</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.528147185281473%" headers="mcps1.1.5.1.3 "><p id="p78517663212"><a name="p78517663212"></a><a name="p78517663212"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.085591440855914%" headers="mcps1.1.5.1.4 "><p id="p198511263325"><a name="p198511263325"></a><a name="p198511263325"></a>项目，与domain二选一。</p>
    </td>
    </tr>
    <tr id="row1185218612327"><td class="cellrowborder" valign="top" width="18.51814818518148%" headers="mcps1.1.5.1.1 "><p id="p1785156133220"><a name="p1785156133220"></a><a name="p1785156133220"></a>domain</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.868113188681132%" headers="mcps1.1.5.1.2 "><p id="p9851562322"><a name="p9851562322"></a><a name="p9851562322"></a>Dict</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.528147185281473%" headers="mcps1.1.5.1.3 "><p id="p148514693210"><a name="p148514693210"></a><a name="p148514693210"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.085591440855914%" headers="mcps1.1.5.1.4 "><p id="p6852769329"><a name="p6852769329"></a><a name="p6852769329"></a>区域，与project二选一。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   project格式

    <a name="table185213613324"></a>
    <table><thead align="left"><tr id="row58523623213"><th class="cellrowborder" valign="top" width="18.64%" id="mcps1.1.5.1.1"><p id="p148524618329"><a name="p148524618329"></a><a name="p148524618329"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.96%" id="mcps1.1.5.1.2"><p id="p108529614329"><a name="p108529614329"></a><a name="p108529614329"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.04%" id="mcps1.1.5.1.3"><p id="p2085206143211"><a name="p2085206143211"></a><a name="p2085206143211"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.36%" id="mcps1.1.5.1.4"><p id="p085266183215"><a name="p085266183215"></a><a name="p085266183215"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row188527614325"><td class="cellrowborder" valign="top" width="18.64%" headers="mcps1.1.5.1.1 "><p id="p48521765325"><a name="p48521765325"></a><a name="p48521765325"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.1.5.1.2 "><p id="p1085206113220"><a name="p1085206113220"></a><a name="p1085206113220"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.1.5.1.3 "><p id="p1852136113217"><a name="p1852136113217"></a><a name="p1852136113217"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.36%" headers="mcps1.1.5.1.4 "><p id="p1085215673210"><a name="p1085215673210"></a><a name="p1085215673210"></a>项目名，与id二选一。</p>
    </td>
    </tr>
    <tr id="row178523693219"><td class="cellrowborder" valign="top" width="18.64%" headers="mcps1.1.5.1.1 "><p id="p13852156173216"><a name="p13852156173216"></a><a name="p13852156173216"></a>domain</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.1.5.1.2 "><p id="p11852566322"><a name="p11852566322"></a><a name="p11852566322"></a>Dict</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.1.5.1.3 "><p id="p1785214618321"><a name="p1785214618321"></a><a name="p1785214618321"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.36%" headers="mcps1.1.5.1.4 "><p id="p14852968329"><a name="p14852968329"></a><a name="p14852968329"></a>项目所属区域，使用name时必填。</p>
    </td>
    </tr>
    <tr id="row1185216653210"><td class="cellrowborder" valign="top" width="18.64%" headers="mcps1.1.5.1.1 "><p id="p2085256163212"><a name="p2085256163212"></a><a name="p2085256163212"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.1.5.1.2 "><p id="p16852869327"><a name="p16852869327"></a><a name="p16852869327"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.04%" headers="mcps1.1.5.1.3 "><p id="p185218614324"><a name="p185218614324"></a><a name="p185218614324"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.36%" headers="mcps1.1.5.1.4 "><p id="p20852106173210"><a name="p20852106173210"></a><a name="p20852106173210"></a>项目ID，与name二选一。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   domain格式

    <a name="table385317643214"></a>
    <table><thead align="left"><tr id="row185313613214"><th class="cellrowborder" valign="top" width="18.5%" id="mcps1.1.5.1.1"><p id="p9853106143216"><a name="p9853106143216"></a><a name="p9853106143216"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.96%" id="mcps1.1.5.1.2"><p id="p1485315673214"><a name="p1485315673214"></a><a name="p1485315673214"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.9%" id="mcps1.1.5.1.3"><p id="p985346193217"><a name="p985346193217"></a><a name="p985346193217"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.64%" id="mcps1.1.5.1.4"><p id="p1285317613325"><a name="p1285317613325"></a><a name="p1285317613325"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row1185313653210"><td class="cellrowborder" valign="top" width="18.5%" headers="mcps1.1.5.1.1 "><p id="p4853062327"><a name="p4853062327"></a><a name="p4853062327"></a>name</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.1.5.1.2 "><p id="p385346123219"><a name="p385346123219"></a><a name="p385346123219"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.9%" headers="mcps1.1.5.1.3 "><p id="p285317643214"><a name="p285317643214"></a><a name="p285317643214"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.64%" headers="mcps1.1.5.1.4 "><p id="p108532611328"><a name="p108532611328"></a><a name="p108532611328"></a>区域名称，与id二选一。</p>
    </td>
    </tr>
    <tr id="row185313663214"><td class="cellrowborder" valign="top" width="18.5%" headers="mcps1.1.5.1.1 "><p id="p48531966327"><a name="p48531966327"></a><a name="p48531966327"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.96%" headers="mcps1.1.5.1.2 "><p id="p108533612325"><a name="p108533612325"></a><a name="p108533612325"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.9%" headers="mcps1.1.5.1.3 "><p id="p185386183218"><a name="p185386183218"></a><a name="p185386183218"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.64%" headers="mcps1.1.5.1.4 "><p id="p168532067324"><a name="p168532067324"></a><a name="p168532067324"></a>区域id，与name二选一。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   请求样例

    ```
    POST /v3/auth/tokens
    {
    "auth": {
    "identity": {
    "methods": [
    "token"
    ],
    "token": {
    "id": "--federated-token-id--"
    }
    },
    "scope": {
    "domain": {
    "id": "e31ac82d778b4d128cb6fed37fd72cdb"
    }
    }
    }
    }
    ```


>![](public_sys-resources/icon-note.gif) **说明：**   
>不建议直接调用该接口，使用openstackclient获取token。  

## 响应<a name="section43835291165356"></a>

-   Response Body参数说明

    <a name="table60997658165356"></a>
    <table><thead align="left"><tr id="row28280121165356"><th class="cellrowborder" valign="top" width="18.44%" id="mcps1.1.5.1.1"><p id="p8988451165356"><a name="p8988451165356"></a><a name="p8988451165356"></a>参数名称</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.12%" id="mcps1.1.5.1.2"><p id="p56975950165356"><a name="p56975950165356"></a><a name="p56975950165356"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.919999999999998%" id="mcps1.1.5.1.3"><p id="p51649250165356"><a name="p51649250165356"></a><a name="p51649250165356"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="44.519999999999996%" id="mcps1.1.5.1.4"><p id="p22839685165356"><a name="p22839685165356"></a><a name="p22839685165356"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row38075234165356"><td class="cellrowborder" valign="top" width="18.44%" headers="mcps1.1.5.1.1 "><p id="p64195103165356"><a name="p64195103165356"></a><a name="p64195103165356"></a>methods</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.1.5.1.2 "><p id="p32420836165356"><a name="p32420836165356"></a><a name="p32420836165356"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.919999999999998%" headers="mcps1.1.5.1.3 "><p id="p8842074165356"><a name="p8842074165356"></a><a name="p8842074165356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.519999999999996%" headers="mcps1.1.5.1.4 "><p id="p45119400165356"><a name="p45119400165356"></a><a name="p45119400165356"></a>获取token时使用的鉴权方式。</p>
    </td>
    </tr>
    <tr id="row3421424165356"><td class="cellrowborder" valign="top" width="18.44%" headers="mcps1.1.5.1.1 "><p id="p8699959165356"><a name="p8699959165356"></a><a name="p8699959165356"></a>roles</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.1.5.1.2 "><p id="p33608041165356"><a name="p33608041165356"></a><a name="p33608041165356"></a>List</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.919999999999998%" headers="mcps1.1.5.1.3 "><p id="p37896816165356"><a name="p37896816165356"></a><a name="p37896816165356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.519999999999996%" headers="mcps1.1.5.1.4 "><p id="p49743284165356"><a name="p49743284165356"></a><a name="p49743284165356"></a>获取的token所代表的用户在项目或域中的角色信息。</p>
    </td>
    </tr>
    <tr id="row45036376165356"><td class="cellrowborder" valign="top" width="18.44%" headers="mcps1.1.5.1.1 "><p id="p24067841165356"><a name="p24067841165356"></a><a name="p24067841165356"></a>expires_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.1.5.1.2 "><p id="p3338139165356"><a name="p3338139165356"></a><a name="p3338139165356"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.919999999999998%" headers="mcps1.1.5.1.3 "><p id="p1953870165356"><a name="p1953870165356"></a><a name="p1953870165356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.519999999999996%" headers="mcps1.1.5.1.4 "><p id="p24045761165356"><a name="p24045761165356"></a><a name="p24045761165356"></a>token的失效时间。</p>
    </td>
    </tr>
    <tr id="row15085258165356"><td class="cellrowborder" valign="top" width="18.44%" headers="mcps1.1.5.1.1 "><p id="p13946368165356"><a name="p13946368165356"></a><a name="p13946368165356"></a>project</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.1.5.1.2 "><p id="p55914060165356"><a name="p55914060165356"></a><a name="p55914060165356"></a>Dict</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.919999999999998%" headers="mcps1.1.5.1.3 "><p id="p32744979165356"><a name="p32744979165356"></a><a name="p32744979165356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.519999999999996%" headers="mcps1.1.5.1.4 "><p id="p35097663165356"><a name="p35097663165356"></a><a name="p35097663165356"></a>token所属项目信息。</p>
    </td>
    </tr>
    <tr id="row47443519165356"><td class="cellrowborder" valign="top" width="18.44%" headers="mcps1.1.5.1.1 "><p id="p17719805165356"><a name="p17719805165356"></a><a name="p17719805165356"></a>catalog</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.1.5.1.2 "><p id="p26018067165356"><a name="p26018067165356"></a><a name="p26018067165356"></a>Dict</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.919999999999998%" headers="mcps1.1.5.1.3 "><p id="p27088682165356"><a name="p27088682165356"></a><a name="p27088682165356"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.519999999999996%" headers="mcps1.1.5.1.4 "><p id="p46699625165356"><a name="p46699625165356"></a><a name="p46699625165356"></a>服务及终端节点信息。</p>
    </td>
    </tr>
    <tr id="row17643448165356"><td class="cellrowborder" valign="top" width="18.44%" headers="mcps1.1.5.1.1 "><p id="p19833159165356"><a name="p19833159165356"></a><a name="p19833159165356"></a>extras</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.1.5.1.2 "><p id="p62982035165356"><a name="p62982035165356"></a><a name="p62982035165356"></a>Dict</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.919999999999998%" headers="mcps1.1.5.1.3 "><p id="p1271171165356"><a name="p1271171165356"></a><a name="p1271171165356"></a>否</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.519999999999996%" headers="mcps1.1.5.1.4 "><p id="p35855999165356"><a name="p35855999165356"></a><a name="p35855999165356"></a>token额外信息。</p>
    </td>
    </tr>
    <tr id="row54268542165356"><td class="cellrowborder" valign="top" width="18.44%" headers="mcps1.1.5.1.1 "><p id="p33675768165356"><a name="p33675768165356"></a><a name="p33675768165356"></a>user</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.1.5.1.2 "><p id="p43382707165356"><a name="p43382707165356"></a><a name="p43382707165356"></a>Dict</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.919999999999998%" headers="mcps1.1.5.1.3 "><p id="p24338391165356"><a name="p24338391165356"></a><a name="p24338391165356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.519999999999996%" headers="mcps1.1.5.1.4 "><p id="p25252618165356"><a name="p25252618165356"></a><a name="p25252618165356"></a>token所属用户信息。</p>
    </td>
    </tr>
    <tr id="row25946978165356"><td class="cellrowborder" valign="top" width="18.44%" headers="mcps1.1.5.1.1 "><p id="p21330482165356"><a name="p21330482165356"></a><a name="p21330482165356"></a>issued_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.12%" headers="mcps1.1.5.1.2 "><p id="p50047462165356"><a name="p50047462165356"></a><a name="p50047462165356"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.919999999999998%" headers="mcps1.1.5.1.3 "><p id="p27312615165356"><a name="p27312615165356"></a><a name="p27312615165356"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="44.519999999999996%" headers="mcps1.1.5.1.4 "><p id="p64838172165356"><a name="p64838172165356"></a><a name="p64838172165356"></a>token生成的时间。</p>
    </td>
    </tr>
    </tbody>
    </table>


-   响应样例

    ```
    X-Subject-Token: MIIFwAYJKoZIhvcNAQcCoIIFsTCCBa0CAQExDTALBglghkgBZQMEAgEwggQOBgkqhkiG9w0BBwGgggP-BIID+3sidG9rZW4iOnsibWV0aG9kcyI6WyJ0b2tlbiJdLCJpc3N1ZWRfYXQiOiIyMDE3LTA1LTIzVDA2OjU0OjEyLjUwODAwMFoiLCJleHBpcmVzX2F0IjoiMjAxNy0wNS0yNFQwNjo1NDoxMi41MDgwMDBaIiwidXNlciI6eyJpZCI6IlJNUVRndGpqU05HRGNLeTdvVW1JM0FaZzdHZ3NXRzBaIiwibmFtZSI6InN0b25laWRwMDEiLCJPUy1GRURFUkFUSU9OIjp7ImlkZW50aXR5X3Byb3ZpZGVyIjp7ImlkIjoic3RvbmVpZHAwMSJ9LCJwcm90b2NvbCI6eyJpZCI6InNhbWwifSwiZ3JvdXBzIjpbeyJpZCI6ImI0MDE4OWUyNmVhNDRmOTU5ODc3NjIxYjRiMjk4ZGI1In1dfSwiZG9tYWluIjp7ImlkIjoiZTMxYWM4MmQ3NzhiNGQxMjhjYjZmZWQzN2ZkNzJjZGIiLCJuYW1lIjoic3RvbmUiLCJ4ZG9tYWluX2lkIjoieGRvbWFpbmlkMDA2OTU4MTQ5MDM5NDQ1NzE0NDU5MzIzIiwieGRvbWFpbl90eXBlIjoiVFNJIn19LCJkb21haW4iOnsiaWQiOiJlMzFhYzgyZDc3OGI0ZDEyOGNiNmZlZDM3ZmQ3MmNkYiIsIm5hbWUiOiJzdG9uZSIsInhkb21haW5faWQiOiJ4ZG9tYWluaWQwMDY5NTgxNDkwMzk0NDU3MTQ0NTkzMjMiLCJ4ZG9tYWluX3R5cGUiOiJUU0kifSwicm9sZXMiOlt7ImlkIjoiZWFlODI2Njg0ZDc3NDYyNDgyZDgxNThjMGZjN2IxNjEiLCJuYW1lIjoidGVfYWRtaW4ifSx7ImlkIjoiMDA3YjczYjIyOWYxNGMzZDhlNzFmNWRjY2Y5NjY5YTYiLCJuYW1lIjoic2VjdV9hZG1pbiJ9LHsiaWQiOiI5M2JjNTc1M2UwZmM0ZjAxYTZmZDY5ZjQ1YTE1YzEyNiIsIm5hbWUiOiJ0ZV9hZ2VuY3kifSx7ImlkIjoiMCIsIm5hbWUiOiJvcF9nYXRlZF9zdG9uZSJ9LHsiaWQiOiIwIiwibmFtZSI6Im9wX2dhdGVkX3Rhc3NzZzEifSx7ImlkIjoiMCIsIm5hbWUiOiJvcF9nYXRlZF90YXNzc2cyIn0seyJpZCI6IjAiLCJuYW1lIjoib3BfZ2F0ZWRfdGFzc3NnNCJ9LHsiaWQiOiIwIiwibmFtZSI6Im9wX2dhdGVkX3Rhc3NzZzUifSx7ImlkIjoiMCIsIm5hbWUiOiJvcF9nYXRlZF90YXNzc2c2In1dLCJjYXRhbG9nIjpbXX19MYIBhTCCAYECAQEwXDBXMQswCQYDVQQGEwJVUzEOMAwGA1UECAwFVW5zZXQxDjAMBgNVBAcMBVVuc2V0MQ4wDAYDVQQKDAVVbnNldDEYMBYGA1UEAwwPd3d3LmV4YW1wbGUuY29tAgEBMAsGCWCGSAFlAwQCATANBgkqhkiG9w0BAQEFAASCAQBbiTxUJJ7OS-yk0XspQwu5f8labMMjpM8clbe3PrPZNQhBtJNqG1joUH9QIWXJkQ54VHu9B0yWzO8enbn2qQaHu6IVzs4tAl034k250CcYcBL241KJQtKDgJyu0Q1mnQXWCCcV9a5-3sQitvBYSINirYAh7UH-lUhO4q01nUp1O3UEOq6-xhLpCy63DP7LgrfE8tIvkRxfj62-NgVffaEgxSC7iCZMc84MQYxdYWPXTrJk110UUh86JyzXfOEov-sIWBGvC6g9FpPpUvTlpM+IK7yogFxmZwIshPLmDj5aqtaT6YxkMxMIY9G7kNCljTUn1QJhqbIEIM-5zl4f7m6w 
    {
        "token": {
            "domain": {
                "xdomain_type": "TSI",
                "id": "e31ac82d778b4d128cb6fed37fd72cdb",
                "xdomain_id": "xdomainid006958149039445714459323",
                "name": "exampledomain"
            },
            "methods": [
                "token"
            ],
            "roles": [
                {
                    "id": "eae826684d77462482d8158c0fc7b161",
                    "name": "te_admin"
                },
                {
                    "id": "007b73b229f14c3d8e71f5dccf9669a6",
                    "name": "secu_admin"
                },
                {
                    "id": "93bc5753e0fc4f01a6fd69f45a15c126",
                    "name": "te_agency"
                },
                {
                    "id": "0",
                    "name": "op_gated_stone"
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
            "expires_at": "2017-05-24T06:54:12.508000Z",
            "catalog": [
                {
                    "endpoints": [
                        {
                            "url": "https://sample.domain.com/v3",
                            "interface": "public",
                            "region": "*",
                            "region_id": "*",
                            "id": "f2a24165ecf14efeb5fcb2682ebc4cde"
                        }
                    ],
                    "type": "identity",
                    "id": "90ded4a66ee14ecea72266ee2fdc2b0a",
                    "name": "keystone"
                }
            ],
            "user": {
                "OS-FEDERATION": {
                    "identity_provider": {
                        "id": "stoneidp01"
                    },
                    "protocol": {
                        "id": "saml"
                    },
                    "groups": [
                        {
                            "id": "b40189e26ea44f959877621b4b298db5"
                        }
                    ]
                },
                "domain": {
                    "xdomain_type": "TSI",
                    "id": "e31ac82d778b4d128cb6fed37fd72cdb",
                    "xdomain_id": "xdomainid006958149039445714459323",
                    "name": "exampledomain"
                },
                "id": "RMQTgtjjSNGDcKy7oUmI3AZg7GgsWG0Z",
                "name": "exampleuser"
            },
            "issued_at": "2017-05-23T06:54:12.508000Z"
        }
    }
    ```


## 状态码<a name="section48834236165356"></a>

<a name="zh-cn_topic_0026585112_table34550710"></a>
<table><thead align="left"><tr id="zh-cn_topic_0026585112_row8352109"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0026585112_p5432205"><a name="zh-cn_topic_0026585112_p5432205"></a><a name="zh-cn_topic_0026585112_p5432205"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0026585112_p37355470"><a name="zh-cn_topic_0026585112_p37355470"></a><a name="zh-cn_topic_0026585112_p37355470"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0026585112_row5894231"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p7670737"><a name="zh-cn_topic_0026585112_p7670737"></a><a name="zh-cn_topic_0026585112_p7670737"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0026585112_p17349988"><a name="zh-cn_topic_0026585112_p17349988"></a><a name="zh-cn_topic_0026585112_p17349988"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0026585112_row21932166"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p31674992"><a name="zh-cn_topic_0026585112_p31674992"></a><a name="zh-cn_topic_0026585112_p31674992"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0026585112_p15537542"><a name="zh-cn_topic_0026585112_p15537542"></a><a name="zh-cn_topic_0026585112_p15537542"></a>请求错误。</p>
</td>
</tr>
<tr id="r22bf632ff3984ffbaa2734a029063cfb"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p947606916650"><a name="zh-cn_topic_0026585112_p947606916650"></a><a name="zh-cn_topic_0026585112_p947606916650"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="a3a62e2f9d6c84b4083dfb8b2ade8e14c"><a name="a3a62e2f9d6c84b4083dfb8b2ade8e14c"></a><a name="a3a62e2f9d6c84b4083dfb8b2ade8e14c"></a>认证失败。</p>
</td>
</tr>
<tr id="r41d0d854619349f898c16f7c61792083"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p762821816657"><a name="zh-cn_topic_0026585112_p762821816657"></a><a name="zh-cn_topic_0026585112_p762821816657"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="a0261fc1955104ca3b1f0a46388724624"><a name="a0261fc1955104ca3b1f0a46388724624"></a><a name="a0261fc1955104ca3b1f0a46388724624"></a>鉴权失败。</p>
</td>
</tr>
<tr id="rea66e1a745ee4e0882be6b9f5349ac4d"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p486971841676"><a name="zh-cn_topic_0026585112_p486971841676"></a><a name="zh-cn_topic_0026585112_p486971841676"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0026585112_p521578261676"><a name="zh-cn_topic_0026585112_p521578261676"></a><a name="zh-cn_topic_0026585112_p521578261676"></a>找不到资源。</p>
</td>
</tr>
<tr id="r230ba1b5ddec4cd0a41a5c37806e60f5"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="af8f4513c90d344e3b90952b53e3ee015"><a name="af8f4513c90d344e3b90952b53e3ee015"></a><a name="af8f4513c90d344e3b90952b53e3ee015"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="a19c27fd6b377464898ec6cae5778ec80"><a name="a19c27fd6b377464898ec6cae5778ec80"></a><a name="a19c27fd6b377464898ec6cae5778ec80"></a>内部服务错误。</p>
</td>
</tr>
<tr id="zh-cn_topic_0026585112_row6824316711"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0026585112_p61418816711"><a name="zh-cn_topic_0026585112_p61418816711"></a><a name="zh-cn_topic_0026585112_p61418816711"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="a4bc003bda05e465eb3a3f0f989888213"><a name="a4bc003bda05e465eb3a3f0f989888213"></a><a name="a4bc003bda05e465eb3a3f0f989888213"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

