# 获取临时AK/SK和securitytoken<a name="zh-cn_topic_0097949518"></a>

## 功能介绍<a name="s37f73fa9234e41d3aee73c75a47eabba"></a>

该接口通过用户或者委托token来获取临时AK/SK和securitytoken，临时AK/SK和securitytoken是系统颁发给用户的临时访问令牌，有效期为15分钟至24小时，过期后需要重新获取。临时AK/SK和securitytoken遵循权限最小化。使用临时AK/SK鉴权时，临时AK/SK和securitytoken必须同时使用，请求头中需要添加“x-security-token”字段，使用方法详情请参考：[API签名参考](https://support.huaweicloud.com/devg-apisign/api-sign-provide.html)。

该接口可以使用全局区域的域名和其他区域的域名调用，全局区域的域名为iam.myhuaweicloud.com。

## URI<a name="s6da80212b87341a6b73b416e9ceede6d"></a>

URI格式

POST /v3.0/OS-CREDENTIAL/securitytokens

## 请求消息<a name="s926b2080db4b47cc9d4dbc9ec412dcf1"></a>

-   Request Header参数说明
    -   通过委托token进行请求

        <a name="tcca7117b1c2545d986645420ee8f54a5"></a>
        <table><thead align="left"><tr id="r07376d92a1ee46a18f3360824eed2f9b"><th class="cellrowborder" valign="top" width="18.89%" id="mcps1.1.5.1.1"><p id="af118850a64de44e2b010fed5065e5707"><a name="af118850a64de44e2b010fed5065e5707"></a><a name="af118850a64de44e2b010fed5065e5707"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="19.99%" id="mcps1.1.5.1.2"><p id="zh-cn_topic_0056596910_p253072461917"><a name="zh-cn_topic_0056596910_p253072461917"></a><a name="zh-cn_topic_0056596910_p253072461917"></a>是否必选</p>
        </th>
        <th class="cellrowborder" valign="top" width="22.49%" id="mcps1.1.5.1.3"><p id="ab2fc6c7c0f5d4d7e903959655b885c0d"><a name="ab2fc6c7c0f5d4d7e903959655b885c0d"></a><a name="ab2fc6c7c0f5d4d7e903959655b885c0d"></a>类型</p>
        </th>
        <th class="cellrowborder" valign="top" width="38.629999999999995%" id="mcps1.1.5.1.4"><p id="zh-cn_topic_0056596910_p953052415195"><a name="zh-cn_topic_0056596910_p953052415195"></a><a name="zh-cn_topic_0056596910_p953052415195"></a>描述</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="r156b58bbc6044c8dacb4280d5d476f27"><td class="cellrowborder" valign="top" width="18.89%" headers="mcps1.1.5.1.1 "><p id="a70d12cc0284a4cea9ed5e4d1f8091d84"><a name="a70d12cc0284a4cea9ed5e4d1f8091d84"></a><a name="a70d12cc0284a4cea9ed5e4d1f8091d84"></a>Content-Type</p>
        </td>
        <td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.1.5.1.2 "><p id="a44eac6e555cc405c84239ee7423f313e"><a name="a44eac6e555cc405c84239ee7423f313e"></a><a name="a44eac6e555cc405c84239ee7423f313e"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.49%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0056596910_p125301245191"><a name="zh-cn_topic_0056596910_p125301245191"></a><a name="zh-cn_topic_0056596910_p125301245191"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="38.629999999999995%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0056596910_p185305242199"><a name="zh-cn_topic_0056596910_p185305242199"></a><a name="zh-cn_topic_0056596910_p185305242199"></a>该字段填为<span class="parmvalue" id="parmvalue3878171118187"><a name="parmvalue3878171118187"></a><a name="parmvalue3878171118187"></a>“application/json;charset=utf8”</span>。</p>
        </td>
        </tr>
        <tr id="row8272143315810"><td class="cellrowborder" valign="top" width="18.89%" headers="mcps1.1.5.1.1 "><p id="p783912371286"><a name="p783912371286"></a><a name="p783912371286"></a>X-Auth-Token</p>
        </td>
        <td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.1.5.1.2 "><p id="p168391237582"><a name="p168391237582"></a><a name="p168391237582"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.49%" headers="mcps1.1.5.1.3 "><p id="p08394371814"><a name="p08394371814"></a><a name="p08394371814"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="38.629999999999995%" headers="mcps1.1.5.1.4 "><p id="p1867119457257"><a name="p1867119457257"></a><a name="p1867119457257"></a>具有Agent Operator权限的token，token获取方法请参见：<a href="获取委托Token.md">获取委托Token</a>。</p>
        </td>
        </tr>
        </tbody>
        </table>

    -   通过用户token进行请求

        <a name="table117431052151715"></a>
        <table><thead align="left"><tr id="row10754152101713"><th class="cellrowborder" valign="top" width="18.891889188918892%" id="mcps1.1.5.1.1"><p id="p137571452151716"><a name="p137571452151716"></a><a name="p137571452151716"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="19.831983198319833%" id="mcps1.1.5.1.2"><p id="p8758205241713"><a name="p8758205241713"></a><a name="p8758205241713"></a>是否必选</p>
        </th>
        <th class="cellrowborder" valign="top" width="22.492249224922492%" id="mcps1.1.5.1.3"><p id="p4762165281715"><a name="p4762165281715"></a><a name="p4762165281715"></a>类型</p>
        </th>
        <th class="cellrowborder" valign="top" width="38.78387838783878%" id="mcps1.1.5.1.4"><p id="p3766175211720"><a name="p3766175211720"></a><a name="p3766175211720"></a>描述</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="row67691052141713"><td class="cellrowborder" valign="top" width="18.891889188918892%" headers="mcps1.1.5.1.1 "><p id="p14770165210171"><a name="p14770165210171"></a><a name="p14770165210171"></a>Content-Type</p>
        </td>
        <td class="cellrowborder" valign="top" width="19.831983198319833%" headers="mcps1.1.5.1.2 "><p id="p677385216175"><a name="p677385216175"></a><a name="p677385216175"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.492249224922492%" headers="mcps1.1.5.1.3 "><p id="p377610526177"><a name="p377610526177"></a><a name="p377610526177"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="38.78387838783878%" headers="mcps1.1.5.1.4 "><p id="p378095261710"><a name="p378095261710"></a><a name="p378095261710"></a>该字段填为<span class="parmvalue" id="parmvalue68351128101912"><a name="parmvalue68351128101912"></a><a name="parmvalue68351128101912"></a>“application/json;charset=utf8”</span>”。</p>
        </td>
        </tr>
        <tr id="row67811152191720"><td class="cellrowborder" valign="top" width="18.891889188918892%" headers="mcps1.1.5.1.1 "><p id="p7784195218170"><a name="p7784195218170"></a><a name="p7784195218170"></a>X-Auth-Token</p>
        </td>
        <td class="cellrowborder" valign="top" width="19.831983198319833%" headers="mcps1.1.5.1.2 "><p id="p147851152171713"><a name="p147851152171713"></a><a name="p147851152171713"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.492249224922492%" headers="mcps1.1.5.1.3 "><p id="p778845291718"><a name="p778845291718"></a><a name="p778845291718"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="38.78387838783878%" headers="mcps1.1.5.1.4 "><p id="p117911852141718"><a name="p117911852141718"></a><a name="p117911852141718"></a>普通token或者联邦token，该值与请求体中token二选一即可，如果都填写了，系统优先校验X-Auth-Token。</p>
        </td>
        </tr>
        </tbody>
        </table>


-   Request Body参数说明
    -   通过委托token进行请求

        <a name="t7f269af2050e4926afefd365e178465b"></a>
        <table><thead align="left"><tr id="rfa1f5a414e7649ccabd96455047cd3ec"><th class="cellrowborder" valign="top" width="18.81188118811881%" id="mcps1.1.5.1.1"><p id="a649ea58427784f7c8d86c5602b87104a"><a name="a649ea58427784f7c8d86c5602b87104a"></a><a name="a649ea58427784f7c8d86c5602b87104a"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="19.801980198019802%" id="mcps1.1.5.1.2"><p id="a52636b4d38214015a6e48784d5252467"><a name="a52636b4d38214015a6e48784d5252467"></a><a name="a52636b4d38214015a6e48784d5252467"></a>是否必选</p>
        </th>
        <th class="cellrowborder" valign="top" width="22.152215221522155%" id="mcps1.1.5.1.3"><p id="afd0e518a88e24a4e96c697a7be19cbc2"><a name="afd0e518a88e24a4e96c697a7be19cbc2"></a><a name="afd0e518a88e24a4e96c697a7be19cbc2"></a>类型</p>
        </th>
        <th class="cellrowborder" valign="top" width="39.23392339233923%" id="mcps1.1.5.1.4"><p id="ae12c862e63504aceac73f270bcbb9ef9"><a name="ae12c862e63504aceac73f270bcbb9ef9"></a><a name="ae12c862e63504aceac73f270bcbb9ef9"></a>描述</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="r5ba29f30d0294f649c0261f5ee268550"><td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.1 "><p id="ae5fb6c05f11245888a4a7a589ff026a7"><a name="ae5fb6c05f11245888a4a7a589ff026a7"></a><a name="ae5fb6c05f11245888a4a7a589ff026a7"></a>methods</p>
        </td>
        <td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.2 "><p id="ae26f131fe9d644aa83c2ad45d95fdb09"><a name="ae26f131fe9d644aa83c2ad45d95fdb09"></a><a name="ae26f131fe9d644aa83c2ad45d95fdb09"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.152215221522155%" headers="mcps1.1.5.1.3 "><p id="a58724c182f834f54a8f205ce939f82c9"><a name="a58724c182f834f54a8f205ce939f82c9"></a><a name="a58724c182f834f54a8f205ce939f82c9"></a>String Array</p>
        </td>
        <td class="cellrowborder" valign="top" width="39.23392339233923%" headers="mcps1.1.5.1.4 "><p id="a01ebfabb039940b98c89b3bdd2a6afd6"><a name="a01ebfabb039940b98c89b3bdd2a6afd6"></a><a name="a01ebfabb039940b98c89b3bdd2a6afd6"></a>该字段内容为<span class="parmvalue" id="parmvalue19922173518202"><a name="parmvalue19922173518202"></a><a name="parmvalue19922173518202"></a>“assume_role”</span>。</p>
        </td>
        </tr>
        <tr id="r0d2ff120207942b89f88af082b9117b0"><td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.1 "><p id="af4d55619f8a2469eaaf399b8834e518f"><a name="af4d55619f8a2469eaaf399b8834e518f"></a><a name="af4d55619f8a2469eaaf399b8834e518f"></a>agency_name</p>
        </td>
        <td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.2 "><p id="a5793c583ab0141fe972ccbf5facb7194"><a name="a5793c583ab0141fe972ccbf5facb7194"></a><a name="a5793c583ab0141fe972ccbf5facb7194"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.152215221522155%" headers="mcps1.1.5.1.3 "><p id="a3bdb8564f3174d0b993ece861ab5616f"><a name="a3bdb8564f3174d0b993ece861ab5616f"></a><a name="a3bdb8564f3174d0b993ece861ab5616f"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="39.23392339233923%" headers="mcps1.1.5.1.4 "><p id="a9ecdb84d5c71491b990a05b8ca924957"><a name="a9ecdb84d5c71491b990a05b8ca924957"></a><a name="a9ecdb84d5c71491b990a05b8ca924957"></a>委托名称。</p>
        </td>
        </tr>
        <tr id="r0c25bdcbbff040338d36adc023dd9f97"><td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0056596910_p4770553481"><a name="zh-cn_topic_0056596910_p4770553481"></a><a name="zh-cn_topic_0056596910_p4770553481"></a>domain_name或domain_id</p>
        </td>
        <td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0056596910_p97709531782"><a name="zh-cn_topic_0056596910_p97709531782"></a><a name="zh-cn_topic_0056596910_p97709531782"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.152215221522155%" headers="mcps1.1.5.1.3 "><p id="zh-cn_topic_0056596910_p07709531487"><a name="zh-cn_topic_0056596910_p07709531487"></a><a name="zh-cn_topic_0056596910_p07709531487"></a>String</p>
        </td>
        <td class="cellrowborder" valign="top" width="39.23392339233923%" headers="mcps1.1.5.1.4 "><p id="a7d17f5dc348644e4a0356f6229a75ad4"><a name="a7d17f5dc348644e4a0356f6229a75ad4"></a><a name="a7d17f5dc348644e4a0356f6229a75ad4"></a>委托方的账号名称或者ID，domain_name和domain_id二选一。</p>
        </td>
        </tr>
        <tr id="r97b524a758e644548a5bd34a3b932739"><td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.1 "><p id="a3ece2697bd6d4562bed05c8f4e7f1223"><a name="a3ece2697bd6d4562bed05c8f4e7f1223"></a><a name="a3ece2697bd6d4562bed05c8f4e7f1223"></a>duration-seconds</p>
        </td>
        <td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.2 "><p id="a2d5bebeac9e9467aa26ee50af3fd5add"><a name="a2d5bebeac9e9467aa26ee50af3fd5add"></a><a name="a2d5bebeac9e9467aa26ee50af3fd5add"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.152215221522155%" headers="mcps1.1.5.1.3 "><p id="af9d0db00c0434ce6a95dbfe36a10aeca"><a name="af9d0db00c0434ce6a95dbfe36a10aeca"></a><a name="af9d0db00c0434ce6a95dbfe36a10aeca"></a>Int</p>
        </td>
        <td class="cellrowborder" valign="top" width="39.23392339233923%" headers="mcps1.1.5.1.4 "><p id="af31246a849e544a3991f0e364ab07f69"><a name="af31246a849e544a3991f0e364ab07f69"></a><a name="af31246a849e544a3991f0e364ab07f69"></a>AK/SK和securitytoken的有效期，时间单位为秒。取值范围：15min ~ 24h ，默认为15min。</p>
        </td>
        </tr>
        <tr id="row156996551645"><td class="cellrowborder" valign="top" width="18.81188118811881%" headers="mcps1.1.5.1.1 "><p id="p10930532053"><a name="p10930532053"></a><a name="p10930532053"></a>session_user</p>
        </td>
        <td class="cellrowborder" valign="top" width="19.801980198019802%" headers="mcps1.1.5.1.2 "><p id="p20930132056"><a name="p20930132056"></a><a name="p20930132056"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.152215221522155%" headers="mcps1.1.5.1.3 "><p id="p139301231453"><a name="p139301231453"></a><a name="p139301231453"></a>Object</p>
        </td>
        <td class="cellrowborder" valign="top" width="39.23392339233923%" headers="mcps1.1.5.1.4 "><p id="p15930173557"><a name="p15930173557"></a><a name="p15930173557"></a>使用自定义代理方式获取时需要session_user，即企业用户名信息。用户名需满足如下规则：长度5~32，只能包含大写字母、小写字母、数字（0-9）、特殊字符（-_）且只能以字母开头。</p>
        <pre class="screen" id="screen189302036517"><a name="screen189302036517"></a><a name="screen189302036517"></a>"session_user": {
            "name": "user_name "
        }</pre>
        </td>
        </tr>
        </tbody>
        </table>

    -   通过用户token进行请求

        <a name="t0cc84c02310f4e9ead62efd457aee291"></a>
        <table><thead align="left"><tr id="r3dedc45671b342c18a7f17a5959c2c6d"><th class="cellrowborder" valign="top" width="18.89%" id="mcps1.1.5.1.1"><p id="a32881b797ceb4fd7bd9d1e95689a4b18"><a name="a32881b797ceb4fd7bd9d1e95689a4b18"></a><a name="a32881b797ceb4fd7bd9d1e95689a4b18"></a>参数</p>
        </th>
        <th class="cellrowborder" valign="top" width="19.99%" id="mcps1.1.5.1.2"><p id="ab36ba8846cb94d62b7f5d8b60b38ea6e"><a name="ab36ba8846cb94d62b7f5d8b60b38ea6e"></a><a name="ab36ba8846cb94d62b7f5d8b60b38ea6e"></a>是否必选</p>
        </th>
        <th class="cellrowborder" valign="top" width="22.43%" id="mcps1.1.5.1.3"><p id="zh-cn_topic_0056596910_p317413396472"><a name="zh-cn_topic_0056596910_p317413396472"></a><a name="zh-cn_topic_0056596910_p317413396472"></a>类型</p>
        </th>
        <th class="cellrowborder" valign="top" width="38.690000000000005%" id="mcps1.1.5.1.4"><p id="a47c280f6407e4eb9aa2aea4f0a17fe5f"><a name="a47c280f6407e4eb9aa2aea4f0a17fe5f"></a><a name="a47c280f6407e4eb9aa2aea4f0a17fe5f"></a>描述</p>
        </th>
        </tr>
        </thead>
        <tbody><tr id="r954d63fb5ea74e1ab584dcaf2647bbb6"><td class="cellrowborder" valign="top" width="18.89%" headers="mcps1.1.5.1.1 "><p id="a48ec5a0484d541f8bea4918148ba5196"><a name="a48ec5a0484d541f8bea4918148ba5196"></a><a name="a48ec5a0484d541f8bea4918148ba5196"></a>methods</p>
        </td>
        <td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.1.5.1.2 "><p id="a44e8a16c13df423fbc01aa468913ccb3"><a name="a44e8a16c13df423fbc01aa468913ccb3"></a><a name="a44e8a16c13df423fbc01aa468913ccb3"></a>是</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.43%" headers="mcps1.1.5.1.3 "><p id="a9555d192db1640e9bef878d59d74fbfe"><a name="a9555d192db1640e9bef878d59d74fbfe"></a><a name="a9555d192db1640e9bef878d59d74fbfe"></a>String Array</p>
        </td>
        <td class="cellrowborder" valign="top" width="38.690000000000005%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0056596910_p21894397479"><a name="zh-cn_topic_0056596910_p21894397479"></a><a name="zh-cn_topic_0056596910_p21894397479"></a>该字段内容为<span class="parmvalue" id="parmvalue1511115227211"><a name="parmvalue1511115227211"></a><a name="parmvalue1511115227211"></a>“token”</span>。</p>
        </td>
        </tr>
        <tr id="r0f9953c7a6d3424aa0970d2040e217e4"><td class="cellrowborder" valign="top" width="18.89%" headers="mcps1.1.5.1.1 "><p id="acaa2e64ab6fc49e68a46298439d441f9"><a name="acaa2e64ab6fc49e68a46298439d441f9"></a><a name="acaa2e64ab6fc49e68a46298439d441f9"></a>token</p>
        </td>
        <td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.1.5.1.2 "><p id="a71cb30778b8942ee9047b5f39d87ee65"><a name="a71cb30778b8942ee9047b5f39d87ee65"></a><a name="a71cb30778b8942ee9047b5f39d87ee65"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.43%" headers="mcps1.1.5.1.3 "><p id="aa8d2a2f59cdd48fba1e9314e917c8ac3"><a name="aa8d2a2f59cdd48fba1e9314e917c8ac3"></a><a name="aa8d2a2f59cdd48fba1e9314e917c8ac3"></a>Json Object</p>
        </td>
        <td class="cellrowborder" valign="top" width="38.690000000000005%" headers="mcps1.1.5.1.4 "><p id="ac870e4fca7234a2f94746dffa8f632b3"><a name="ac870e4fca7234a2f94746dffa8f632b3"></a><a name="ac870e4fca7234a2f94746dffa8f632b3"></a>普通token或者联邦token，该对象中的id与请求头部中的X-Auth-Token二选一，X-Auth-Token优先。</p>
        </td>
        </tr>
        <tr id="rb4e32f4fe494428f9ed9f658c259150f"><td class="cellrowborder" valign="top" width="18.89%" headers="mcps1.1.5.1.1 "><p id="zh-cn_topic_0056596910_p520553910477"><a name="zh-cn_topic_0056596910_p520553910477"></a><a name="zh-cn_topic_0056596910_p520553910477"></a>duration-seconds</p>
        </td>
        <td class="cellrowborder" valign="top" width="19.99%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0056596910_p720573919472"><a name="zh-cn_topic_0056596910_p720573919472"></a><a name="zh-cn_topic_0056596910_p720573919472"></a>否</p>
        </td>
        <td class="cellrowborder" valign="top" width="22.43%" headers="mcps1.1.5.1.3 "><p id="abbf4b1dc17a44f2b8babcc21c7a179d3"><a name="abbf4b1dc17a44f2b8babcc21c7a179d3"></a><a name="abbf4b1dc17a44f2b8babcc21c7a179d3"></a>Int</p>
        </td>
        <td class="cellrowborder" valign="top" width="38.690000000000005%" headers="mcps1.1.5.1.4 "><p id="aa2081311b8ac4113873c6dec1088c6ad"><a name="aa2081311b8ac4113873c6dec1088c6ad"></a><a name="aa2081311b8ac4113873c6dec1088c6ad"></a>AK/SK和securitytoken的有效期，时间单位为秒。取值范围：15min ~ 24h ，默认为15min。</p>
        </td>
        </tr>
        </tbody>
        </table>



-   请求示例
    -   通过委托token进行请求

        ```
        {
            "auth": {
                "identity": {
                    "methods": ["assume_role"],
                    "assume_role": {
                        "domain_id": "411edb4b634144f587ffc88f9bbd...",
                        "agency_name": "exampleagency",
                        "duration-seconds": 3600,
                        "session_user": {
                            "name": "user_name"
                        }
                    }
                }
            }
        }
        
        ```

    -   通过用户token进行请求

        ```
        {
            "auth": {
                "identity": {
                    "methods": [
                        "token"
                    ],
                    "token": {
                        "id": "MIIDkgYJKoZIhvcNAQcCoIIDgzCCA38CAQExDTALBglghkgBZQMEAgEwgXXXXX...",
                        "duration-seconds": 900
                    }
                }
            }
        }
        ```



## 响应<a name="s987a5f64dbf0425e90492e131d91dd6f"></a>

-   Response Body参数说明

    <a name="t71075bd9372146418f36f309206d546d"></a>
    <table><thead align="left"><tr id="rf7ba2ad3ea734fb189aae9eb6784fd91"><th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.1"><p id="ad370c33f356448bcb31af8e0a47fa4a7"><a name="ad370c33f356448bcb31af8e0a47fa4a7"></a><a name="ad370c33f356448bcb31af8e0a47fa4a7"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.2"><p id="a6b1db5c43430453cb2cfcfc6d048dfed"><a name="a6b1db5c43430453cb2cfcfc6d048dfed"></a><a name="a6b1db5c43430453cb2cfcfc6d048dfed"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.3"><p id="a7ad7e600531b40b3a8555205463593d3"><a name="a7ad7e600531b40b3a8555205463593d3"></a><a name="a7ad7e600531b40b3a8555205463593d3"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.4"><p id="ade5bee541a32463fa7012f60fcb3f63d"><a name="ade5bee541a32463fa7012f60fcb3f63d"></a><a name="ade5bee541a32463fa7012f60fcb3f63d"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="rf579990aecad486eac8bb7dfe74d6b74"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.1 "><p id="a278f9d3ee45e4fb8a3cc5936ff19051c"><a name="a278f9d3ee45e4fb8a3cc5936ff19051c"></a><a name="a278f9d3ee45e4fb8a3cc5936ff19051c"></a>credential</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.2 "><p id="aca41c717ac524f31a56378a2c8c4f51f"><a name="aca41c717ac524f31a56378a2c8c4f51f"></a><a name="aca41c717ac524f31a56378a2c8c4f51f"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><p id="ac04d3c547d714a10b2f62d91aa41f664"><a name="ac04d3c547d714a10b2f62d91aa41f664"></a><a name="ac04d3c547d714a10b2f62d91aa41f664"></a>Object</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.4 "><p id="a6411ff72d5ba4ea8ab677dc86ec0cced"><a name="a6411ff72d5ba4ea8ab677dc86ec0cced"></a><a name="a6411ff72d5ba4ea8ab677dc86ec0cced"></a>认证信息</p>
    </td>
    </tr>
    </tbody>
    </table>

-   credential内容说明

    <a name="t157a41ad55344766b92133f6d3f67e5a"></a>
    <table><thead align="left"><tr id="r9d3a37aba7ce462182a7cd0239930a7a"><th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.1"><p id="zh-cn_topic_0056596910_p320143315838"><a name="zh-cn_topic_0056596910_p320143315838"></a><a name="zh-cn_topic_0056596910_p320143315838"></a>参数</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.2"><p id="ac1c056f03f83468cb805ca9df721dbe0"><a name="ac1c056f03f83468cb805ca9df721dbe0"></a><a name="ac1c056f03f83468cb805ca9df721dbe0"></a>是否必选</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.3"><p id="zh-cn_topic_0056596910_p83862915838"><a name="zh-cn_topic_0056596910_p83862915838"></a><a name="zh-cn_topic_0056596910_p83862915838"></a>类型</p>
    </th>
    <th class="cellrowborder" valign="top" width="25%" id="mcps1.1.5.1.4"><p id="af0bf232ddbc7479499019d16557db9a0"><a name="af0bf232ddbc7479499019d16557db9a0"></a><a name="af0bf232ddbc7479499019d16557db9a0"></a>描述</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="rc7cc77854d024936aac9b583cfda4fe5"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.1 "><p id="a224f3f82590742e88e3374ce148016c1"><a name="a224f3f82590742e88e3374ce148016c1"></a><a name="a224f3f82590742e88e3374ce148016c1"></a>expires_at</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.2 "><p id="zh-cn_topic_0056596910_p980353615838"><a name="zh-cn_topic_0056596910_p980353615838"></a><a name="zh-cn_topic_0056596910_p980353615838"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><p id="af45ccde870e945cf85ab9f0d752a2280"><a name="af45ccde870e945cf85ab9f0d752a2280"></a><a name="af45ccde870e945cf85ab9f0d752a2280"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.4 "><p id="ae308362385a643649affe75a07309253"><a name="ae308362385a643649affe75a07309253"></a><a name="ae308362385a643649affe75a07309253"></a>过期时间</p>
    </td>
    </tr>
    <tr id="r64d452b576404dafa65dacd8447b5aaa"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.1 "><p id="ac3da1b0f861f418487ebd046cdb66b88"><a name="ac3da1b0f861f418487ebd046cdb66b88"></a><a name="ac3da1b0f861f418487ebd046cdb66b88"></a>access</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.2 "><p id="a5f47e16e7ea041e89d0d104441960b63"><a name="a5f47e16e7ea041e89d0d104441960b63"></a><a name="a5f47e16e7ea041e89d0d104441960b63"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><p id="a0bddf8bfa6144272b1e177b5309b0a52"><a name="a0bddf8bfa6144272b1e177b5309b0a52"></a><a name="a0bddf8bfa6144272b1e177b5309b0a52"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.4 "><p id="aa5f31f411bf14cbd95be31d808218af1"><a name="aa5f31f411bf14cbd95be31d808218af1"></a><a name="aa5f31f411bf14cbd95be31d808218af1"></a>AK</p>
    </td>
    </tr>
    <tr id="r5e51a148bd4e408ca0685564b5cab2e0"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.1 "><p id="a0e433ade2cf44aff83d3c39384ba7099"><a name="a0e433ade2cf44aff83d3c39384ba7099"></a><a name="a0e433ade2cf44aff83d3c39384ba7099"></a>secret</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.2 "><p id="acfbaff0b9ac74f40966e3cea0ed2a6d9"><a name="acfbaff0b9ac74f40966e3cea0ed2a6d9"></a><a name="acfbaff0b9ac74f40966e3cea0ed2a6d9"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><p id="a9b62f5a5264a45daa918b775d6a41364"><a name="a9b62f5a5264a45daa918b775d6a41364"></a><a name="a9b62f5a5264a45daa918b775d6a41364"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.4 "><p id="a3b6f57d267a247389755c61ec5eab3f7"><a name="a3b6f57d267a247389755c61ec5eab3f7"></a><a name="a3b6f57d267a247389755c61ec5eab3f7"></a>SK</p>
    </td>
    </tr>
    <tr id="r0e1615b25cf94e3f9d31da428fd6f183"><td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.1 "><p id="a03203c3fd4aa4562be555db0211fb280"><a name="a03203c3fd4aa4562be555db0211fb280"></a><a name="a03203c3fd4aa4562be555db0211fb280"></a>securitytoken</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.2 "><p id="a4677aaac4a2d4eaa811fd7fc4af15f4c"><a name="a4677aaac4a2d4eaa811fd7fc4af15f4c"></a><a name="a4677aaac4a2d4eaa811fd7fc4af15f4c"></a>是</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.3 "><p id="a0aba3b9c8a554f9785fbd81db65c487e"><a name="a0aba3b9c8a554f9785fbd81db65c487e"></a><a name="a0aba3b9c8a554f9785fbd81db65c487e"></a>String</p>
    </td>
    <td class="cellrowborder" valign="top" width="25%" headers="mcps1.1.5.1.4 "><p id="zh-cn_topic_0056596910_p299581715838"><a name="zh-cn_topic_0056596910_p299581715838"></a><a name="zh-cn_topic_0056596910_p299581715838"></a>用于后续换SK、 Token或loginToken使用</p>
    </td>
    </tr>
    </tbody>
    </table>

-   响应示例

    ```
    {
      "credential": {
        "access": "NQC51NFINJS1JXX...",
        "secret": "EY74MByPZ46kTRJL9ay5DskqXX...",
        "expires_at": "2017-04-17T07:55:18.575000Z",
        "securitytoken": "gAAAAABY9GbWUaGtoa9DPj7_dE4qUSnAXXX..."
      }
    }
    ```


## 状态码<a name="sf1bd0a17f1264315a1a57eb5a7071c36"></a>

<a name="t91b628302cf7421e82389201ba4efef3"></a>
<table><thead align="left"><tr id="re0457507a24943248c88a719663a909f"><th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.1"><p id="a15db1e723300498ba8617cc58814d6d6"><a name="a15db1e723300498ba8617cc58814d6d6"></a><a name="a15db1e723300498ba8617cc58814d6d6"></a>状态码</p>
</th>
<th class="cellrowborder" valign="top" width="50%" id="mcps1.1.3.1.2"><p id="a1a5e5610b8214de590cdd018dabefd62"><a name="a1a5e5610b8214de590cdd018dabefd62"></a><a name="a1a5e5610b8214de590cdd018dabefd62"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="ra1cb949214b145a785a6104d2b7c031c"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="ae777b0ccd79c4a7abd06adbe666cf58d"><a name="ae777b0ccd79c4a7abd06adbe666cf58d"></a><a name="ae777b0ccd79c4a7abd06adbe666cf58d"></a>201</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="a2bcab7f854f649bc8340f67c6af52f11"><a name="a2bcab7f854f649bc8340f67c6af52f11"></a><a name="a2bcab7f854f649bc8340f67c6af52f11"></a>请求成功</p>
</td>
</tr>
<tr id="r27baf852d3024d6083962a8e171779d7"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="a87b2b54aeca74bf0a937231e459e9f82"><a name="a87b2b54aeca74bf0a937231e459e9f82"></a><a name="a87b2b54aeca74bf0a937231e459e9f82"></a>400</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="a096326a738fe46e7ab08a31fcafc07bc"><a name="a096326a738fe46e7ab08a31fcafc07bc"></a><a name="a096326a738fe46e7ab08a31fcafc07bc"></a>请求失败</p>
</td>
</tr>
<tr id="r39eef0d38db74d6bbdc97157ff431207"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="a7d1f83e848ef4251a12c7dea6015c977"><a name="a7d1f83e848ef4251a12c7dea6015c977"></a><a name="a7d1f83e848ef4251a12c7dea6015c977"></a>401</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="ac0ff9b21c5e64620b8a4c45cd6f028fb"><a name="ac0ff9b21c5e64620b8a4c45cd6f028fb"></a><a name="ac0ff9b21c5e64620b8a4c45cd6f028fb"></a>认证失败</p>
</td>
</tr>
<tr id="r56e109619204490a8ac60a2823d869a3"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="ae2eefb749ba14306b62424ca672248dd"><a name="ae2eefb749ba14306b62424ca672248dd"></a><a name="ae2eefb749ba14306b62424ca672248dd"></a>403</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="a605e2f64e1da4fc1a570f243a8629758"><a name="a605e2f64e1da4fc1a570f243a8629758"></a><a name="a605e2f64e1da4fc1a570f243a8629758"></a>鉴权失败</p>
</td>
</tr>
<tr id="reb0e6b35be084cfc8ca80c6ff3187ae4"><td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.1 "><p id="a337aa80f74e34e5f80bd7dfb27912528"><a name="a337aa80f74e34e5f80bd7dfb27912528"></a><a name="a337aa80f74e34e5f80bd7dfb27912528"></a>500</p>
</td>
<td class="cellrowborder" valign="top" width="50%" headers="mcps1.1.3.1.2 "><p id="ae2f7f519962748728723158751d8697f"><a name="ae2f7f519962748728723158751d8697f"></a><a name="ae2f7f519962748728723158751d8697f"></a>系统异常</p>
</td>
</tr>
</tbody>
</table>

