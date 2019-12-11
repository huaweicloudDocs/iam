# 查询Keystone API的3.0版本信息<a name="zh-cn_topic_0057845613"></a>

## 功能介绍<a name="s412c1f69bf89493b84b4b241cdbc9008"></a>

该接口用于获取Keystone API的3.0版本的信息。

该接口可以使用全局区域的域名和其他区域的域名调用，全局区域的域名为iam.myhuaweicloud.com。

## URI<a name="s06d21799b5ee48a4ae4757ef4e69b001"></a>

URI格式

GET /v3

## 请求<a name="sf38a0d89d61e455da87f7b6d64ae5205"></a>

请求样例

```
curl -i -k -X GET https://www.example.com/v3
```

## 响应<a name="sadb04a35c9184f34bb7d75b534f88786"></a>

-   响应参数说明

    <a name="zh-cn_topic_0035543752_table44962972"></a>
    <table><thead align="left"><tr id="zh-cn_topic_0035543752_row49143529"><th class="cellrowborder" valign="top" width="21.740000000000002%" id="mcps1.1.5.1.1"><p id="zh-cn_topic_0035543752_p21202951"><a name="zh-cn_topic_0035543752_p21202951"></a><a name="zh-cn_topic_0035543752_p21202951"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.63%" id="mcps1.1.5.1.2"><p id="p1700142751918"><a name="p1700142751918"></a><a name="p1700142751918"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="20.990000000000002%" id="mcps1.1.5.1.3"><p id="zh-cn_topic_0035543752_p39717481"><a name="zh-cn_topic_0035543752_p39717481"></a><a name="zh-cn_topic_0035543752_p39717481"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="34.64%" id="mcps1.1.5.1.4"><p id="zh-cn_topic_0035543752_p62999416"><a name="zh-cn_topic_0035543752_p62999416"></a><a name="zh-cn_topic_0035543752_p62999416"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="zh-cn_topic_0035543752_row2679067"><td class="cellrowborder" valign="top" width="21.740000000000002%" headers="mcps1.1.5.1.1 "><p id="aab1cc638a9a04361a245043d6ac69434"><a name="aab1cc638a9a04361a245043d6ac69434"></a><a name="aab1cc638a9a04361a245043d6ac69434"></a>version</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.63%" headers="mcps1.1.5.1.2 "><p id="p97001527171917"><a name="p97001527171917"></a><a name="p97001527171917"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="20.990000000000002%" headers="mcps1.1.5.1.3 "><p id="a2e9403dd87bf457bbe82812db9edf434"><a name="a2e9403dd87bf457bbe82812db9edf434"></a><a name="a2e9403dd87bf457bbe82812db9edf434"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="34.64%" headers="mcps1.1.5.1.4 "><p id="adda3be2c284f40228992db1aad71dcf9"><a name="adda3be2c284f40228992db1aad71dcf9"></a><a name="adda3be2c284f40228992db1aad71dcf9"></a>Keystone API的版本信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   version格式说明

    <a name="t6a822d2f816d42978a87fb9bbef76205"></a>
    <table><thead align="left"><tr id="r97d9ad0c317c452f8799bb5ab582ce92"><th class="cellrowborder" valign="top" width="21.947805219478052%" id="mcps1.1.5.1.1"><p id="aa2c0859a96fc41259e62450184740ed9"><a name="aa2c0859a96fc41259e62450184740ed9"></a><a name="aa2c0859a96fc41259e62450184740ed9"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="22.47775222477752%" id="mcps1.1.5.1.2"><p id="abcf3a01d1b5f455596b0c4516dab6421"><a name="abcf3a01d1b5f455596b0c4516dab6421"></a><a name="abcf3a01d1b5f455596b0c4516dab6421"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="21.137886211378863%" id="mcps1.1.5.1.3"><p id="ac11daac4b7d34cf6a84917519cb813c8"><a name="ac11daac4b7d34cf6a84917519cb813c8"></a><a name="ac11daac4b7d34cf6a84917519cb813c8"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="34.43655634436556%" id="mcps1.1.5.1.4"><p id="a8adf734076064f95bbaa01dc82bb4a2b"><a name="a8adf734076064f95bbaa01dc82bb4a2b"></a><a name="a8adf734076064f95bbaa01dc82bb4a2b"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="rea6a18e3f80e400cadb8b7984898e1e9"><td class="cellrowborder" valign="top" width="21.947805219478052%" headers="mcps1.1.5.1.1 "><p id="ad3d464bc21484966bfc0c9bc85e90874"><a name="ad3d464bc21484966bfc0c9bc85e90874"></a><a name="ad3d464bc21484966bfc0c9bc85e90874"></a>status</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.47775222477752%" headers="mcps1.1.5.1.2 "><p id="aa3373e1c45bf4e798ae5b423d1fb9768"><a name="aa3373e1c45bf4e798ae5b423d1fb9768"></a><a name="aa3373e1c45bf4e798ae5b423d1fb9768"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.137886211378863%" headers="mcps1.1.5.1.3 "><p id="a9bd260a7475d45ae856b6dbd50f19846"><a name="a9bd260a7475d45ae856b6dbd50f19846"></a><a name="a9bd260a7475d45ae856b6dbd50f19846"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="34.43655634436556%" headers="mcps1.1.5.1.4 "><p id="a050e1b3312254249b4e9bcbb24f4040e"><a name="a050e1b3312254249b4e9bcbb24f4040e"></a><a name="a050e1b3312254249b4e9bcbb24f4040e"></a>版本状态。</p>
    </td>
    </tr>
    <tr id="ra2fb2e24530b45209d824d0579ea5d3d"><td class="cellrowborder" valign="top" width="21.947805219478052%" headers="mcps1.1.5.1.1 "><p id="a2bdcc7582de045c4908485d963435436"><a name="a2bdcc7582de045c4908485d963435436"></a><a name="a2bdcc7582de045c4908485d963435436"></a>updated</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.47775222477752%" headers="mcps1.1.5.1.2 "><p id="a3313a0741f2e434bafdd8b22e13bd3a1"><a name="a3313a0741f2e434bafdd8b22e13bd3a1"></a><a name="a3313a0741f2e434bafdd8b22e13bd3a1"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.137886211378863%" headers="mcps1.1.5.1.3 "><p id="ace409facb32243d8ac9933f731ceb9c6"><a name="ace409facb32243d8ac9933f731ceb9c6"></a><a name="ace409facb32243d8ac9933f731ceb9c6"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="34.43655634436556%" headers="mcps1.1.5.1.4 "><p id="a698229ec7d4c4b1c88d81ed8b6acd4a3"><a name="a698229ec7d4c4b1c88d81ed8b6acd4a3"></a><a name="a698229ec7d4c4b1c88d81ed8b6acd4a3"></a>版本最后更新时间。</p>
    </td>
    </tr>
    <tr id="r53bd4f9cfb584d00854734ebe783093c"><td class="cellrowborder" valign="top" width="21.947805219478052%" headers="mcps1.1.5.1.1 "><p id="acfbcdab008954ce0995f8c476f962991"><a name="acfbcdab008954ce0995f8c476f962991"></a><a name="acfbcdab008954ce0995f8c476f962991"></a>media-types</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.47775222477752%" headers="mcps1.1.5.1.2 "><p id="aea4ed6b668464c7f83b279405b5923b0"><a name="aea4ed6b668464c7f83b279405b5923b0"></a><a name="aea4ed6b668464c7f83b279405b5923b0"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.137886211378863%" headers="mcps1.1.5.1.3 "><p id="addb0823c3fb24ff7bed6a1a7db8f6284"><a name="addb0823c3fb24ff7bed6a1a7db8f6284"></a><a name="addb0823c3fb24ff7bed6a1a7db8f6284"></a>Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="34.43655634436556%" headers="mcps1.1.5.1.4 "><p id="a3fc3cf9365ff4620b15038b747aecd20"><a name="a3fc3cf9365ff4620b15038b747aecd20"></a><a name="a3fc3cf9365ff4620b15038b747aecd20"></a>版本支持的消息格式。</p>
    </td>
    </tr>
    <tr id="r62a8026ae5c7476b9fba8e0df30dc6df"><td class="cellrowborder" valign="top" width="21.947805219478052%" headers="mcps1.1.5.1.1 "><p id="a09b07e17032b468d95057630a7621546"><a name="a09b07e17032b468d95057630a7621546"></a><a name="a09b07e17032b468d95057630a7621546"></a>id</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.47775222477752%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0035543752_p386591205643"><a name="zh-cn_topic_0035543752_p386591205643"></a><a name="zh-cn_topic_0035543752_p386591205643"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.137886211378863%" headers="mcps1.1.5.1.3 "><p id="a77699d14b9eb4893b164cd433f38afac"><a name="a77699d14b9eb4893b164cd433f38afac"></a><a name="a77699d14b9eb4893b164cd433f38afac"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="34.43655634436556%" headers="mcps1.1.5.1.4 "><p id="aa4c7add4b1254e80b2885140a5bd375c"><a name="aa4c7add4b1254e80b2885140a5bd375c"></a><a name="aa4c7add4b1254e80b2885140a5bd375c"></a>版本号，如v3.0。</p>
    </td>
    </tr>
    <tr id="rb39d64c1e7a845f59b98084fc32d29a7"><td class="cellrowborder" valign="top" width="21.947805219478052%" headers="mcps1.1.5.1.1 "><p id="abb45b631a9b54f1588da62006430d692"><a name="abb45b631a9b54f1588da62006430d692"></a><a name="abb45b631a9b54f1588da62006430d692"></a>links</p>
    </td>
    <td class="cellrowborder" valign="top" width="22.47775222477752%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0035543752_p372076171929"><a name="zh-cn_topic_0035543752_p372076171929"></a><a name="zh-cn_topic_0035543752_p372076171929"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="21.137886211378863%" headers="mcps1.1.5.1.3 "><p id="a5d5e0419bd5546e99543cb8faba19c67"><a name="a5d5e0419bd5546e99543cb8faba19c67"></a><a name="a5d5e0419bd5546e99543cb8faba19c67"></a>Array</p>
    </td>
    <td class="cellrowborder" valign="top" width="34.43655634436556%" headers="mcps1.1.5.1.4 "><p id="aea5df04267f447d3a49335e8bb570ade"><a name="aea5df04267f447d3a49335e8bb570ade"></a><a name="aea5df04267f447d3a49335e8bb570ade"></a>版本的资源链接。</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应样例（响应成功）

    ```
    {
        "version": {
            "status": "stable",
            "updated": "2016-04-04T00:00:00Z",
            "media-types": [
                {
                    "base": "application/json",
                    "type": "application/vnd.openstack.identity-v3+json"
                }
            ],
            "id": "v3.6",
            "links": [
                {
                    "href": "https://www.example.com/v3/",
                    "rel": "self"
                }
            ]
        }
    }
    ```


## 状态码<a name="sd26bdff9224841e48283adfdeeb0adba"></a>

<a name="zh-cn_topic_0035543752_table25927028"></a>
<table><thead align="left"><tr id="zh-cn_topic_0035543752_row10578662"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="zh-cn_topic_0035543752_p51565323"><a name="zh-cn_topic_0035543752_p51565323"></a><a name="zh-cn_topic_0035543752_p51565323"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="zh-cn_topic_0035543752_p16041657"><a name="zh-cn_topic_0035543752_p16041657"></a><a name="zh-cn_topic_0035543752_p16041657"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="zh-cn_topic_0035543752_row24305815"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0035543752_p22613965"><a name="zh-cn_topic_0035543752_p22613965"></a><a name="zh-cn_topic_0035543752_p22613965"></a>200</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0035543752_p19791876"><a name="zh-cn_topic_0035543752_p19791876"></a><a name="zh-cn_topic_0035543752_p19791876"></a>请求成功。</p>
</td>
</tr>
<tr id="zh-cn_topic_0035543752_row43909159"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="zh-cn_topic_0035543752_p66980994"><a name="zh-cn_topic_0035543752_p66980994"></a><a name="zh-cn_topic_0035543752_p66980994"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0035543752_p56751409"><a name="zh-cn_topic_0035543752_p56751409"></a><a name="zh-cn_topic_0035543752_p56751409"></a>请求错误。</p>
</td>
</tr>
<tr id="re523b3dbf728422f859f70773c174c00"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="a69d32f6ad2694b59b8a57e3712a06f1b"><a name="a69d32f6ad2694b59b8a57e3712a06f1b"></a><a name="a69d32f6ad2694b59b8a57e3712a06f1b"></a>404</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="a58bd559a77e240da82a8effff45ad230"><a name="a58bd559a77e240da82a8effff45ad230"></a><a name="a58bd559a77e240da82a8effff45ad230"></a>找不到资源。</p>
</td>
</tr>
<tr id="r545c1109f47e4a49a658e4a8ddfc3341"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="a1820de5ea0b043adb69e91c408f9e987"><a name="a1820de5ea0b043adb69e91c408f9e987"></a><a name="a1820de5ea0b043adb69e91c408f9e987"></a>503</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="a9e57dfbc46874219ac1dc154eb013fdf"><a name="a9e57dfbc46874219ac1dc154eb013fdf"></a><a name="a9e57dfbc46874219ac1dc154eb013fdf"></a>服务不可用。</p>
</td>
</tr>
</tbody>
</table>

