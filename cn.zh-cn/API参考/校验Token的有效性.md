# 校验Token的有效性<a name="zh-cn_topic_0057845585"></a>

## 功能介绍<a name="s2f7665a32abf4492987e6dd3617bcb21"></a>

该接口用来校验Token的有效性，包括用户校验自己的Token有效性，以及管理员（具备Security Administrator权限的用户）校验本账号中其他用户的token有效性，管理员仅能校验本账号中用户的token有效性，不能校验其他账号中用户的token有效性。被校验的Token如果有效，则返回Token的详细信息。

该接口可以使用全局区域的域名和其他区域的域名调用，全局区域的域名为iam.myhuaweicloud.com。

## URI<a name="s1c0fd353ed38459c8baeab25cc3c62d2"></a>

URI格式

GET /v3/auth/tokens

## 请求<a name="s27bb6347561e424096c86cfc3d036e9e"></a>

-   Request Header参数说明

    <a name="t14a8c0fedd2149129bd965b2a4d51c90"></a>
    <table><thead align="left"><tr id="rc0444c4b152b43768b629e845d90495e"><th class="cellrowborder" valign="top" width="19.038096190380962%" id="mcps1.1.5.1.1"><p id="a293da93d33fc404ea05b069800a7eb13"><a name="a293da93d33fc404ea05b069800a7eb13"></a><a name="a293da93d33fc404ea05b069800a7eb13"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="17.578242175782425%" id="mcps1.1.5.1.2"><p id="ac06ad3b3b5174f3ebd57a1661506970a"><a name="ac06ad3b3b5174f3ebd57a1661506970a"></a><a name="ac06ad3b3b5174f3ebd57a1661506970a"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="16.75832416758324%" id="mcps1.1.5.1.3"><p id="a924a03bda76a46648797189b78bdd715"><a name="a924a03bda76a46648797189b78bdd715"></a><a name="a924a03bda76a46648797189b78bdd715"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="46.62533746625338%" id="mcps1.1.5.1.4"><p id="ab17a839c16b94f1e83ff3a3f8ef3b308"><a name="ab17a839c16b94f1e83ff3a3f8ef3b308"></a><a name="ab17a839c16b94f1e83ff3a3f8ef3b308"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="r6f5a057d2e2a48b6b1a71318684ba8b5"><td class="cellrowborder" valign="top" width="19.038096190380962%" headers="mcps1.1.5.1.1 "><p id="a927ddf565a2f45c0840a6e4ef3eab536"><a name="a927ddf565a2f45c0840a6e4ef3eab536"></a><a name="a927ddf565a2f45c0840a6e4ef3eab536"></a>X-Auth-Token</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.1.5.1.2 "><p id="a4edeb0b0c00144319701c1460d210ea8"><a name="a4edeb0b0c00144319701c1460d210ea8"></a><a name="a4edeb0b0c00144319701c1460d210ea8"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.75832416758324%" headers="mcps1.1.5.1.3 "><p id="a17c7fa87e9a54833a6064feb297b5e55"><a name="a17c7fa87e9a54833a6064feb297b5e55"></a><a name="a17c7fa87e9a54833a6064feb297b5e55"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.62533746625338%" headers="mcps1.1.5.1.4 "><a name="ul1963814299291"></a><a name="ul1963814299291"></a><ul id="ul1963814299291"><li>校验自己的Token有效性，使用自己的token即可，该token不需要具备特殊权限。</li><li>管理员校验本账号中其他用户的token有效性，需要具有Security Administrator权限的token。</li></ul>
    </td>
    </tr>
    <tr id="r4ebaddfb83fe4bffa462094cc2834cf2"><td class="cellrowborder" valign="top" width="19.038096190380962%" headers="mcps1.1.5.1.1 "><p id="ae9df07c230354205b9c3cb76f08eadb4"><a name="ae9df07c230354205b9c3cb76f08eadb4"></a><a name="ae9df07c230354205b9c3cb76f08eadb4"></a>X-Subject-Token</p>
    </td>
    <td class="cellrowborder" valign="top" width="17.578242175782425%" headers="mcps1.1.5.1.2 "><p id="a1100e03a09864240abecdff29c388bf8"><a name="a1100e03a09864240abecdff29c388bf8"></a><a name="a1100e03a09864240abecdff29c388bf8"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="16.75832416758324%" headers="mcps1.1.5.1.3 "><p id="a667fee7780224b0d9e78b40c59beaccf"><a name="a667fee7780224b0d9e78b40c59beaccf"></a><a name="a667fee7780224b0d9e78b40c59beaccf"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="46.62533746625338%" headers="mcps1.1.5.1.4 "><p id="p956292518331"><a name="p956292518331"></a><a name="p956292518331"></a>待校验的token。</p>
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

-   请求样例

    ```
    curl -i -k -H "X-Auth-Token:$token" -H "X-Subject-Token:$token" -X GET https://sample.domain.com/v3/auth/tokens?nocatalog=true
    ```


