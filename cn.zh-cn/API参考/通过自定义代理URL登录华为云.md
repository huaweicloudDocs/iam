# 通过自定义代理URL登录华为云<a name="iam_14_1102"></a>

## 功能介绍<a name="section3516738171214"></a>

该接口用于获取自定义代理登录的URL，使用该URL企业用户可以免密访问华为云控制台。

该接口可以使用全局区域的域名和其他区域的域名调用，全局区域的域名为auth.huaweicloud.com。

## URI<a name="section1051843811219"></a>

URI格式

GET /authui/federation/login?idp\_login\_url=\{enterprise\_system\_loginURL\}&service=\{console\_service\_url\}&logintoken=\{logintoken\}

-   参数说明

    <a name="table105201138141210"></a>
    <table><thead align="left"><tr id="row95631538111214"><th class="cellrowborder" valign="top" width="19.19191919191919%" id="mcps1.1.5.1.1"><p id="p1056383811122"><a name="p1056383811122"></a><a name="p1056383811122"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="18.18181818181818%" id="mcps1.1.5.1.2"><p id="p17563163851215"><a name="p17563163851215"></a><a name="p17563163851215"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="19.19191919191919%" id="mcps1.1.5.1.3"><p id="p18563838171213"><a name="p18563838171213"></a><a name="p18563838171213"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="43.43434343434344%" id="mcps1.1.5.1.4"><p id="p1856393831211"><a name="p1856393831211"></a><a name="p1856393831211"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row11563103831211"><td class="cellrowborder" valign="top" width="19.19191919191919%" headers="mcps1.1.5.1.1 "><p id="p185631384122"><a name="p185631384122"></a><a name="p185631384122"></a>idp_login_url</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.18181818181818%" headers="mcps1.1.5.1.2 "><p id="p1556343818122"><a name="p1556343818122"></a><a name="p1556343818122"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.19191919191919%" headers="mcps1.1.5.1.3 "><p id="p14563193814123"><a name="p14563193814123"></a><a name="p14563193814123"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.43434343434344%" headers="mcps1.1.5.1.4 "><p id="p1456303810125"><a name="p1456303810125"></a><a name="p1456303810125"></a>企业系统登录地址。</p>
    </td>
    </tr>
    <tr id="row15631038151213"><td class="cellrowborder" valign="top" width="19.19191919191919%" headers="mcps1.1.5.1.1 "><p id="p95632385127"><a name="p95632385127"></a><a name="p95632385127"></a>service</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.18181818181818%" headers="mcps1.1.5.1.2 "><p id="p1056315385127"><a name="p1056315385127"></a><a name="p1056315385127"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.19191919191919%" headers="mcps1.1.5.1.3 "><p id="p195631538151216"><a name="p195631538151216"></a><a name="p195631538151216"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.43434343434344%" headers="mcps1.1.5.1.4 "><p id="p155631838171217"><a name="p155631838171217"></a><a name="p155631838171217"></a>需要访问的华为云服务地址。</p>
    </td>
    </tr>
    <tr id="row356333851212"><td class="cellrowborder" valign="top" width="19.19191919191919%" headers="mcps1.1.5.1.1 "><p id="p1756318382127"><a name="p1756318382127"></a><a name="p1756318382127"></a>logintoken</p>
    </td>
    <td class="cellrowborder" valign="top" width="18.18181818181818%" headers="mcps1.1.5.1.2 "><p id="p956373881219"><a name="p956373881219"></a><a name="p956373881219"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="19.19191919191919%" headers="mcps1.1.5.1.3 "><p id="p19563193881213"><a name="p19563193881213"></a><a name="p19563193881213"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="43.43434343434344%" headers="mcps1.1.5.1.4 "><p id="p8563738181214"><a name="p8563738181214"></a><a name="p8563738181214"></a>自定义代理登录票据。</p>
    </td>
    </tr>
    </tbody>
    </table>


## 请求<a name="section12529838101211"></a>

-   请求样例

    通过浏览器访问如下地址：

    ```
    https://iam.example.com/authui/federation/login?idp_login_url=https%3A%2F%2Fexample.com&service=https%3a%2f%2fconsole.huaweicloud.com%2fapm%2f%3fregion%3dcn-north-4%23%2fapm%2fatps%2ftopology&logintoken=******
    ```


## 响应<a name="section1253173816124"></a>

-   logintoken认证成功，跳转到华为云控制台。
-   logintoken认证失败，跳转到企业系统登录界面。

