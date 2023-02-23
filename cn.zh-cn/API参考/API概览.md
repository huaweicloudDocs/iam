# API概览<a name="iam_01_0008"></a>

## Token管理<a name="section1161614265913"></a>

<a name="table13788185185910"></a>
<table><thead align="left"><tr id="row14788125114592"><th class="cellrowborder" valign="top" width="27.810000000000002%" id="mcps1.1.3.1.1"><p id="p678865110599"><a name="p678865110599"></a><a name="p678865110599"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="72.19%" id="mcps1.1.3.1.2"><p id="p1178835117597"><a name="p1178835117597"></a><a name="p1178835117597"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row0788195112595"><td class="cellrowborder" valign="top" width="27.810000000000002%" headers="mcps1.1.3.1.1 "><p id="p1078814511593"><a name="p1078814511593"></a><a name="p1078814511593"></a><a href="获取IAM用户Token（使用密码）.md">获取IAM用户Token（使用密码）</a></p>
</td>
<td class="cellrowborder" valign="top" width="72.19%" headers="mcps1.1.3.1.2 "><p id="p147881051185913"><a name="p147881051185913"></a><a name="p147881051185913"></a>该接口可以用于通过用户名/密码的方式进行认证来获取IAM用户Token。</p>
</td>
</tr>
<tr id="row1778875195913"><td class="cellrowborder" valign="top" width="27.810000000000002%" headers="mcps1.1.3.1.1 "><p id="p67884518590"><a name="p67884518590"></a><a name="p67884518590"></a><a href="获取IAM用户Token（使用密码+虚拟MFA）.md">获取IAM用户Token（使用密码+虚拟MFA）</a></p>
</td>
<td class="cellrowborder" valign="top" width="72.19%" headers="mcps1.1.3.1.2 "><p id="p6788751185917"><a name="p6788751185917"></a><a name="p6788751185917"></a>该接口可以用于在IAM用户开启了登录保护功能，并选择通过虚拟MFA验证时，通过用户名/密码+虚拟MFA的方式进行认证来获取IAM用户token。</p>
</td>
</tr>
<tr id="row1788165119592"><td class="cellrowborder" valign="top" width="27.810000000000002%" headers="mcps1.1.3.1.1 "><p id="p127881251125913"><a name="p127881251125913"></a><a name="p127881251125913"></a><a href="获取委托Token.md">获取委托Token</a></p>
</td>
<td class="cellrowborder" valign="top" width="72.19%" headers="mcps1.1.3.1.2 "><p id="p147887512590"><a name="p147887512590"></a><a name="p147887512590"></a>该接口可以用于获取委托方的token。</p>
</td>
</tr>
<tr id="row16764484017"><td class="cellrowborder" valign="top" width="27.810000000000002%" headers="mcps1.1.3.1.1 "><p id="p7764981903"><a name="p7764981903"></a><a name="p7764981903"></a><a href="校验Token的有效性.md">校验Token的有效性</a></p>
</td>
<td class="cellrowborder" valign="top" width="72.19%" headers="mcps1.1.3.1.2 "><p id="p9764081003"><a name="p9764081003"></a><a name="p9764081003"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>校验本帐号中IAM用户token的有效性，或IAM用户校验自己token的有效性</p>
</td>
</tr>
</tbody>
</table>

## 访问密钥管理<a name="section1964282105410"></a>

<a name="table469333016540"></a>
<table><thead align="left"><tr id="row6693123019542"><th class="cellrowborder" valign="top" width="27.900000000000002%" id="mcps1.1.3.1.1"><p id="p847757165919"><a name="p847757165919"></a><a name="p847757165919"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="72.1%" id="mcps1.1.3.1.2"><p id="p154775715913"><a name="p154775715913"></a><a name="p154775715913"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row969333045413"><td class="cellrowborder" valign="top" width="27.900000000000002%" headers="mcps1.1.3.1.1 "><p id="p1869353095418"><a name="p1869353095418"></a><a name="p1869353095418"></a><a href="通过委托获取临时访问密钥和securitytoken.md">通过委托获取临时访问密钥和securitytoken</a></p>
</td>
<td class="cellrowborder" valign="top" width="72.1%" headers="mcps1.1.3.1.2 "><p id="p569333055418"><a name="p569333055418"></a><a name="p569333055418"></a>该接口可以用于通过委托来获取临时访问密钥（临时AK/SK）和securitytoken。</p>
</td>
</tr>
<tr id="row10693230175414"><td class="cellrowborder" valign="top" width="27.900000000000002%" headers="mcps1.1.3.1.1 "><p id="p66935308548"><a name="p66935308548"></a><a name="p66935308548"></a><a href="通过token获取临时访问密钥和securitytoken.md">通过token获取临时访问密钥和securitytoken</a></p>
</td>
<td class="cellrowborder" valign="top" width="72.1%" headers="mcps1.1.3.1.2 "><p id="p126934309542"><a name="p126934309542"></a><a name="p126934309542"></a>该接口可以用于通过token来获取临时AK/SK和securitytoken。</p>
</td>
</tr>
<tr id="row11199134615918"><td class="cellrowborder" valign="top" width="27.900000000000002%" headers="mcps1.1.3.1.1 "><p id="p1419916465599"><a name="p1419916465599"></a><a name="p1419916465599"></a><a href="创建永久访问密钥.md">创建永久访问密钥</a></p>
</td>
<td class="cellrowborder" valign="top" width="72.1%" headers="mcps1.1.3.1.2 "><p id="p181993468598"><a name="p181993468598"></a><a name="p181993468598"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>给IAM用户创建永久访问密钥，或IAM用户给自己创建永久访问密钥。</p>
</td>
</tr>
<tr id="row152001546115911"><td class="cellrowborder" valign="top" width="27.900000000000002%" headers="mcps1.1.3.1.1 "><p id="p7200114665912"><a name="p7200114665912"></a><a name="p7200114665912"></a><a href="查询所有永久访问密钥.md">查询所有永久访问密钥</a></p>
</td>
<td class="cellrowborder" valign="top" width="72.1%" headers="mcps1.1.3.1.2 "><p id="p2200246125918"><a name="p2200246125918"></a><a name="p2200246125918"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询IAM用户的所有永久访问密钥，或IAM用户查询自己的所有永久访问密钥。</p>
</td>
</tr>
<tr id="row6383950105912"><td class="cellrowborder" valign="top" width="27.900000000000002%" headers="mcps1.1.3.1.1 "><p id="p93831150195911"><a name="p93831150195911"></a><a name="p93831150195911"></a><a href="查询指定永久访问密钥.md">查询指定永久访问密钥</a></p>
</td>
<td class="cellrowborder" valign="top" width="72.1%" headers="mcps1.1.3.1.2 "><p id="p1938395017592"><a name="p1938395017592"></a><a name="p1938395017592"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询IAM用户的指定永久访问密钥，或IAM用户查询自己的指定永久访问密钥。</p>
</td>
</tr>
<tr id="row1638335013599"><td class="cellrowborder" valign="top" width="27.900000000000002%" headers="mcps1.1.3.1.1 "><p id="p73835507591"><a name="p73835507591"></a><a name="p73835507591"></a><a href="修改指定永久访问密钥.md">修改指定永久访问密钥</a></p>
</td>
<td class="cellrowborder" valign="top" width="72.1%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482390_p016491313610"><a name="zh-cn_topic_0221482390_p016491313610"></a><a name="zh-cn_topic_0221482390_p016491313610"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改IAM用户的指定永久访问密钥，或IAM用户修改自己的指定永久访问密钥。</p>
</td>
</tr>
<tr id="row738315509598"><td class="cellrowborder" valign="top" width="27.900000000000002%" headers="mcps1.1.3.1.1 "><p id="p238310501592"><a name="p238310501592"></a><a name="p238310501592"></a><a href="删除指定永久访问密钥.md">删除指定永久访问密钥</a></p>
</td>
<td class="cellrowborder" valign="top" width="72.1%" headers="mcps1.1.3.1.2 "><p id="p1938315502598"><a name="p1938315502598"></a><a name="p1938315502598"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>删除IAM用户的指定永久访问密钥，或IAM用户删除自己的指定永久访问密钥。</p>
</td>
</tr>
</tbody>
</table>

## 区域管理<a name="section56242058939"></a>

<a name="table14780671944"></a>
<table><thead align="left"><tr id="row3780871743"><th class="cellrowborder" valign="top" width="28.249999999999996%" id="mcps1.1.3.1.1"><p id="p04252223416"><a name="p04252223416"></a><a name="p04252223416"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="71.75%" id="mcps1.1.3.1.2"><p id="p54251322140"><a name="p54251322140"></a><a name="p54251322140"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row18780479416"><td class="cellrowborder" valign="top" width="28.249999999999996%" headers="mcps1.1.3.1.1 "><p id="p17801471440"><a name="p17801471440"></a><a name="p17801471440"></a><a href="查询区域列表.md">查询区域列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.75%" headers="mcps1.1.3.1.2 "><p id="p18780276412"><a name="p18780276412"></a><a name="p18780276412"></a>该接口可以用于查询区域列表。</p>
</td>
</tr>
<tr id="row878020710410"><td class="cellrowborder" valign="top" width="28.249999999999996%" headers="mcps1.1.3.1.1 "><p id="p878010720415"><a name="p878010720415"></a><a name="p878010720415"></a><a href="查询区域详情.md">查询区域详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.75%" headers="mcps1.1.3.1.2 "><p id="p2078047748"><a name="p2078047748"></a><a name="p2078047748"></a>该接口可以用于查询区域详情。</p>
</td>
</tr>
</tbody>
</table>

## 项目管理<a name="section185885398519"></a>

<a name="table599452613515"></a>
<table><thead align="left"><tr id="row499420265519"><th class="cellrowborder" valign="top" width="28.51%" id="mcps1.1.3.1.1"><p id="p333918336516"><a name="p333918336516"></a><a name="p333918336516"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="71.49%" id="mcps1.1.3.1.2"><p id="p433910331151"><a name="p433910331151"></a><a name="p433910331151"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1699419261050"><td class="cellrowborder" valign="top" width="28.51%" headers="mcps1.1.3.1.1 "><p id="p169941526456"><a name="p169941526456"></a><a name="p169941526456"></a><a href="查询指定条件下的项目列表.md">查询指定条件下的项目列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.49%" headers="mcps1.1.3.1.2 "><p id="p119942261053"><a name="p119942261053"></a><a name="p119942261053"></a>该接口可以用于查询指定条件下的项目列表。</p>
</td>
</tr>
<tr id="row49942261953"><td class="cellrowborder" valign="top" width="28.51%" headers="mcps1.1.3.1.1 "><p id="p16994192614519"><a name="p16994192614519"></a><a name="p16994192614519"></a><a href="查询指定IAM用户的项目列表.md">查询指定IAM用户的项目列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.49%" headers="mcps1.1.3.1.2 "><p id="p189945261557"><a name="p189945261557"></a><a name="p189945261557"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询指定IAM用户的项目列表，或IAM用户查询自己的项目列表。</p>
</td>
</tr>
<tr id="row1599417261516"><td class="cellrowborder" valign="top" width="28.51%" headers="mcps1.1.3.1.1 "><p id="p5994026659"><a name="p5994026659"></a><a name="p5994026659"></a><a href="查询IAM用户可以访问的项目列表.md">查询IAM用户可以访问的项目列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.49%" headers="mcps1.1.3.1.2 "><p id="p19944261256"><a name="p19944261256"></a><a name="p19944261256"></a>该接口可以用于查询IAM用户可以访问的项目列表。</p>
</td>
</tr>
<tr id="row179941926551"><td class="cellrowborder" valign="top" width="28.51%" headers="mcps1.1.3.1.1 "><p id="p1999482613513"><a name="p1999482613513"></a><a name="p1999482613513"></a><a href="创建项目.md">创建项目</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.49%" headers="mcps1.1.3.1.2 "><p id="p2994192616511"><a name="p2994192616511"></a><a name="p2994192616511"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>创建项目。</p>
</td>
</tr>
<tr id="row29940261358"><td class="cellrowborder" valign="top" width="28.51%" headers="mcps1.1.3.1.1 "><p id="p1994112611513"><a name="p1994112611513"></a><a name="p1994112611513"></a><a href="修改项目信息.md">修改项目信息</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.49%" headers="mcps1.1.3.1.2 "><p id="p79941261650"><a name="p79941261650"></a><a name="p79941261650"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改指定项目信息。</p>
</td>
</tr>
<tr id="row299419267519"><td class="cellrowborder" valign="top" width="28.51%" headers="mcps1.1.3.1.1 "><p id="p1699414261058"><a name="p1699414261058"></a><a name="p1699414261058"></a><a href="查询项目详情.md">查询项目详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.49%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482461_p1844810247393"><a name="zh-cn_topic_0221482461_p1844810247393"></a><a name="zh-cn_topic_0221482461_p1844810247393"></a>该接口可以用于查询指定项目详情。</p>
</td>
</tr>
<tr id="row14994102619512"><td class="cellrowborder" valign="top" width="28.51%" headers="mcps1.1.3.1.1 "><p id="p18994122615514"><a name="p18994122615514"></a><a name="p18994122615514"></a><a href="设置项目状态.md">设置项目状态</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.49%" headers="mcps1.1.3.1.2 "><p id="p159940261758"><a name="p159940261758"></a><a name="p159940261758"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>设置指定项目状态。项目状态包括：正常、冻结。</p>
</td>
</tr>
<tr id="row526713466511"><td class="cellrowborder" valign="top" width="28.51%" headers="mcps1.1.3.1.1 "><p id="p182681546259"><a name="p182681546259"></a><a name="p182681546259"></a><a href="查询项目详情与状态.md">查询项目详情与状态</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.49%" headers="mcps1.1.3.1.2 "><p id="p9268194612512"><a name="p9268194612512"></a><a name="p9268194612512"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询指定项目详情与状态。</p>
</td>
</tr>
<tr id="row72682461516"><td class="cellrowborder" valign="top" width="28.51%" headers="mcps1.1.3.1.1 "><p id="p126816461358"><a name="p126816461358"></a><a name="p126816461358"></a><a href="查询项目配额.md">查询项目配额</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.49%" headers="mcps1.1.3.1.2 "><p id="p22681246155"><a name="p22681246155"></a><a name="p22681246155"></a>该接口可以用于查询指定项目配额。</p>
</td>
</tr>
</tbody>
</table>

## 帐号管理<a name="section8361103511113"></a>

<a name="table1742812406114"></a>
<table><thead align="left"><tr id="row1742916403119"><th class="cellrowborder" valign="top" width="28.77%" id="mcps1.1.3.1.1"><p id="p84297406119"><a name="p84297406119"></a><a name="p84297406119"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="71.23%" id="mcps1.1.3.1.2"><p id="p942914402110"><a name="p942914402110"></a><a name="p942914402110"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row6429184041118"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p164295408118"><a name="p164295408118"></a><a name="p164295408118"></a><a href="查询IAM用户可以访问的帐号详情.md">查询IAM用户可以访问的帐号详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p842954071117"><a name="p842954071117"></a><a name="p842954071117"></a>该接口可以用于查询IAM用户可以访问的帐号详情。</p>
</td>
</tr>
<tr id="row1429114061113"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p7429240121114"><a name="p7429240121114"></a><a name="p7429240121114"></a><a href="查询帐号密码强度策略.md">查询帐号密码强度策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p442984051118"><a name="p442984051118"></a><a name="p442984051118"></a>该接口可以用于查询帐号密码强度策略，查询结果包括密码强度策略的正则表达式及其描述。</p>
</td>
</tr>
<tr id="row8429114011116"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p10429134015110"><a name="p10429134015110"></a><a name="p10429134015110"></a><a href="按条件查询帐号密码强度策略.md">按条件查询帐号密码强度策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p34295401113"><a name="p34295401113"></a><a name="p34295401113"></a>该接口可以用于按条件查询帐号密码强度策略，查询结果包括密码强度策略的正则表达式及其描述。</p>
</td>
</tr>
<tr id="row3429114041115"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p11429114051110"><a name="p11429114051110"></a><a name="p11429114051110"></a><a href="查询帐号配额.md">查询帐号配额</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p242984015115"><a name="p242984015115"></a><a name="p242984015115"></a>该接口可以用于查询帐号配额。</p>
</td>
</tr>
</tbody>
</table>

## IAM用户管理<a name="section192470392139"></a>

<a name="table1379942951318"></a>
<table><thead align="left"><tr id="row19799162951317"><th class="cellrowborder" valign="top" width="28.77%" id="mcps1.1.3.1.1"><p id="p879912941314"><a name="p879912941314"></a><a name="p879912941314"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="71.23%" id="mcps1.1.3.1.2"><p id="p12799152910132"><a name="p12799152910132"></a><a name="p12799152910132"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row5799529161314"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p0799202911312"><a name="p0799202911312"></a><a name="p0799202911312"></a><a href="管理员查询IAM用户列表.md">管理员查询IAM用户列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p1779922931313"><a name="p1779922931313"></a><a name="p1779922931313"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询IAM用户列表。</p>
</td>
</tr>
<tr id="row37994291131"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p187992299131"><a name="p187992299131"></a><a name="p187992299131"></a><a href="查询IAM用户详情（推荐）.md">查询IAM用户详情（推荐）</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p107991329151312"><a name="p107991329151312"></a><a name="p107991329151312"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询IAM用户详情，或IAM用户查询自己的用户详情。（可以查询手机号、邮箱）</p>
</td>
</tr>
<tr id="row147997295137"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p12799229131312"><a name="p12799229131312"></a><a name="p12799229131312"></a><a href="查询IAM用户详情.md">查询IAM用户详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p179992951310"><a name="p179992951310"></a><a name="p179992951310"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询IAM用户详情，或IAM用户查询自己的用户详情。（不可以查询手机号、邮箱）</p>
</td>
</tr>
<tr id="row137991229141313"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p2799182913130"><a name="p2799182913130"></a><a name="p2799182913130"></a><a href="查询IAM用户所属用户组.md">查询IAM用户所属用户组</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p3799172913137"><a name="p3799172913137"></a><a name="p3799172913137"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询IAM用户所属用户组，或IAM用户查询自己所属用户组。</p>
</td>
</tr>
<tr id="row2799112912135"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p6799162911133"><a name="p6799162911133"></a><a name="p6799162911133"></a><a href="管理员查询用户组所包含的IAM用户.md">管理员查询用户组所包含的IAM用户</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p1379942961316"><a name="p1379942961316"></a><a name="p1379942961316"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询用户组中所包含的IAM用户。</p>
</td>
</tr>
<tr id="row47991029131313"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p979922918131"><a name="p979922918131"></a><a name="p979922918131"></a><a href="管理员创建IAM用户（推荐）.md">管理员创建IAM用户（推荐）</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482430_p15745145032515"><a name="zh-cn_topic_0221482430_p15745145032515"></a><a name="zh-cn_topic_0221482430_p15745145032515"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>创建IAM用户。</p>
</td>
</tr>
<tr id="row579992911135"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p18799629181312"><a name="p18799629181312"></a><a name="p18799629181312"></a><a href="管理员创建IAM用户.md">管理员创建IAM用户</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p12799429171318"><a name="p12799429171318"></a><a name="p12799429171318"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>创建IAM用户。</p>
</td>
</tr>
<tr id="row156241493156"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p136249911520"><a name="p136249911520"></a><a name="p136249911520"></a><a href="修改IAM用户密码.md">修改IAM用户密码</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p166246910159"><a name="p166246910159"></a><a name="p166246910159"></a>该接口可以用于IAM用户修改自己的密码。</p>
</td>
</tr>
<tr id="row362413911516"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p362413911153"><a name="p362413911153"></a><a name="p362413911153"></a><a href="修改IAM用户信息（推荐）.md">修改IAM用户信息（推荐）</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482381_p10973161413356"><a name="zh-cn_topic_0221482381_p10973161413356"></a><a name="zh-cn_topic_0221482381_p10973161413356"></a>该接口可以用于IAM用户修改自己的用户信息。</p>
</td>
</tr>
<tr id="row262479131518"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p1162418911159"><a name="p1162418911159"></a><a name="p1162418911159"></a><a href="管理员修改IAM用户信息（推荐）.md">管理员修改IAM用户信息（推荐）</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p76241896154"><a name="p76241896154"></a><a name="p76241896154"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改IAM用户信息 。</p>
</td>
</tr>
<tr id="row7624396156"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p262489121516"><a name="p262489121516"></a><a name="p262489121516"></a><a href="管理员修改IAM用户信息.md">管理员修改IAM用户信息</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0221482404_p104111103320"><a name="zh-cn_topic_0221482404_p104111103320"></a><a name="zh-cn_topic_0221482404_p104111103320"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改IAM用户信息。</p>
</td>
</tr>
<tr id="row1362559101517"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p26251911152"><a name="p26251911152"></a><a name="p26251911152"></a><a href="管理员删除IAM用户.md">管理员删除IAM用户</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p86256918158"><a name="p86256918158"></a><a name="p86256918158"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>删除指定IAM用户。</p>
</td>
</tr>
<tr id="row26257911154"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p5625095158"><a name="p5625095158"></a><a name="p5625095158"></a><a href="查询IAM用户的MFA绑定信息列表.md">查询IAM用户的MFA绑定信息列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p1185665293618"><a name="p1185665293618"></a><a name="p1185665293618"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询IAM用户的MFA绑定信息列表。</p>
</td>
</tr>
<tr id="row06252921510"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p462599141518"><a name="p462599141518"></a><a name="p462599141518"></a><a href="查询指定IAM用户的MFA绑定信息.md">查询指定IAM用户的MFA绑定信息</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p96251597153"><a name="p96251597153"></a><a name="p96251597153"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询指定IAM用户的MFA绑定信息，或IAM用户查询自己的MFA绑定信息。</p>
</td>
</tr>
<tr id="row1279310451617"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p1379316441615"><a name="p1379316441615"></a><a name="p1379316441615"></a><a href="查询IAM用户的登录保护状态信息列表.md">查询IAM用户的登录保护状态信息列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p87949451612"><a name="p87949451612"></a><a name="p87949451612"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询IAM用户的登录保护状态列表。</p>
</td>
</tr>
<tr id="row167941401613"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p117941143161"><a name="p117941143161"></a><a name="p117941143161"></a><a href="查询指定IAM用户的登录保护状态信息.md">查询指定IAM用户的登录保护状态信息</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p1079404121614"><a name="p1079404121614"></a><a name="p1079404121614"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询指定IAM用户的登录保护状态信息，或IAM用户查询自己的登录保护状态信息。</p>
</td>
</tr>
<tr id="row1828257162615"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p15829135714268"><a name="p15829135714268"></a><a name="p15829135714268"></a><a href="修改IAM用户的登录保护状态信息.md">修改IAM用户的登录保护状态信息</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p38291257142614"><a name="p38291257142614"></a><a name="p38291257142614"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改IAM用户的登录保护状态信息。</p>
</td>
</tr>
<tr id="row14829457172620"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p182911573269"><a name="p182911573269"></a><a name="p182911573269"></a><a href="绑定MFA设备.md">绑定MFA设备</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p1982915702617"><a name="p1982915702617"></a><a name="p1982915702617"></a>该接口可以用于IAM用户绑定MFA设备。</p>
</td>
</tr>
<tr id="row1382985710260"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p2829557132620"><a name="p2829557132620"></a><a name="p2829557132620"></a><a href="解绑MFA设备.md">解绑MFA设备</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p19829115722620"><a name="p19829115722620"></a><a name="p19829115722620"></a>该接口可以用于IAM用户解绑MFA设备。</p>
</td>
</tr>
<tr id="row12829145718261"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p15829175715262"><a name="p15829175715262"></a><a name="p15829175715262"></a><a href="创建MFA设备.md">创建MFA设备</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p13829185792610"><a name="p13829185792610"></a><a name="p13829185792610"></a>接口可以用于IAM用户创建MFA设备。</p>
</td>
</tr>
<tr id="row158297572269"><td class="cellrowborder" valign="top" width="28.77%" headers="mcps1.1.3.1.1 "><p id="p182914577261"><a name="p182914577261"></a><a name="p182914577261"></a><a href="删除MFA设备.md">删除MFA设备</a></p>
</td>
<td class="cellrowborder" valign="top" width="71.23%" headers="mcps1.1.3.1.2 "><p id="p98291577267"><a name="p98291577267"></a><a name="p98291577267"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>删除MFA设备。</p>
</td>
</tr>
</tbody>
</table>

## 用户组管理<a name="section563264711205"></a>

<a name="table13586820152119"></a>
<table><thead align="left"><tr id="row2586162012215"><th class="cellrowborder" valign="top" width="29.21%" id="mcps1.1.3.1.1"><p id="p758612062114"><a name="p758612062114"></a><a name="p758612062114"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="70.78999999999999%" id="mcps1.1.3.1.2"><p id="p558652019214"><a name="p558652019214"></a><a name="p558652019214"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row1258642017212"><td class="cellrowborder" valign="top" width="29.21%" headers="mcps1.1.3.1.1 "><p id="p6586920152114"><a name="p6586920152114"></a><a name="p6586920152114"></a><a href="查询用户组列表.md">查询用户组列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.78999999999999%" headers="mcps1.1.3.1.2 "><p id="p1458692032120"><a name="p1458692032120"></a><a name="p1458692032120"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询用户组列表。</p>
</td>
</tr>
<tr id="row145864203213"><td class="cellrowborder" valign="top" width="29.21%" headers="mcps1.1.3.1.1 "><p id="p10586920102116"><a name="p10586920102116"></a><a name="p10586920102116"></a><a href="查询用户组详情.md">查询用户组详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.78999999999999%" headers="mcps1.1.3.1.2 "><p id="p19586192019215"><a name="p19586192019215"></a><a name="p19586192019215"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询用户组详情。</p>
</td>
</tr>
<tr id="row45862203216"><td class="cellrowborder" valign="top" width="29.21%" headers="mcps1.1.3.1.1 "><p id="p958617205213"><a name="p958617205213"></a><a name="p958617205213"></a><a href="创建用户组.md">创建用户组</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.78999999999999%" headers="mcps1.1.3.1.2 "><p id="p558612022119"><a name="p558612022119"></a><a name="p558612022119"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>创建用户组。</p>
</td>
</tr>
<tr id="row1658682013216"><td class="cellrowborder" valign="top" width="29.21%" headers="mcps1.1.3.1.1 "><p id="p20586122017211"><a name="p20586122017211"></a><a name="p20586122017211"></a><a href="更新用户组.md">更新用户组</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.78999999999999%" headers="mcps1.1.3.1.2 "><p id="p13586920102119"><a name="p13586920102119"></a><a name="p13586920102119"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>更新用户组信息。</p>
</td>
</tr>
<tr id="row185861320142118"><td class="cellrowborder" valign="top" width="29.21%" headers="mcps1.1.3.1.1 "><p id="p18586152018214"><a name="p18586152018214"></a><a name="p18586152018214"></a><a href="删除用户组.md">删除用户组</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.78999999999999%" headers="mcps1.1.3.1.2 "><p id="p158617206217"><a name="p158617206217"></a><a name="p158617206217"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>删除用户组。</p>
</td>
</tr>
<tr id="row1658618201213"><td class="cellrowborder" valign="top" width="29.21%" headers="mcps1.1.3.1.1 "><p id="p358611201212"><a name="p358611201212"></a><a name="p358611201212"></a><a href="查询IAM用户是否在用户组中.md">查询IAM用户是否在用户组中</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.78999999999999%" headers="mcps1.1.3.1.2 "><p id="p115861820132110"><a name="p115861820132110"></a><a name="p115861820132110"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询IAM用户是否在用户组中。</p>
</td>
</tr>
<tr id="row3586192016216"><td class="cellrowborder" valign="top" width="29.21%" headers="mcps1.1.3.1.1 "><p id="p175861020112112"><a name="p175861020112112"></a><a name="p175861020112112"></a><a href="添加IAM用户到用户组.md">添加IAM用户到用户组</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.78999999999999%" headers="mcps1.1.3.1.2 "><p id="p858692022113"><a name="p858692022113"></a><a name="p858692022113"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>添加IAM用户到用户组。</p>
</td>
</tr>
<tr id="row1740605516223"><td class="cellrowborder" valign="top" width="29.21%" headers="mcps1.1.3.1.1 "><p id="p2406555162213"><a name="p2406555162213"></a><a name="p2406555162213"></a><a href="移除用户组中的IAM用户.md">移除用户组中的IAM用户</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.78999999999999%" headers="mcps1.1.3.1.2 "><p id="p10406145511224"><a name="p10406145511224"></a><a name="p10406145511224"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>移除用户组中的IAM用户。</p>
</td>
</tr>
</tbody>
</table>

## 权限管理<a name="section1823118592243"></a>

<a name="table716794916244"></a>
<table><thead align="left"><tr id="row131674499246"><th class="cellrowborder" valign="top" width="29.38%" id="mcps1.1.3.1.1"><p id="p1916764913243"><a name="p1916764913243"></a><a name="p1916764913243"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="70.62%" id="mcps1.1.3.1.2"><p id="p6167849142416"><a name="p6167849142416"></a><a name="p6167849142416"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row116794913246"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p15167134942411"><a name="p15167134942411"></a><a name="p15167134942411"></a><a href="查询权限列表.md">查询权限列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037529_p1181913213384"><a name="zh-cn_topic_0222037529_p1181913213384"></a><a name="zh-cn_topic_0222037529_p1181913213384"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询权限列表。</p>
</td>
</tr>
<tr id="row12167194942419"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p191671749132413"><a name="p191671749132413"></a><a name="p191671749132413"></a><a href="查询权限详情.md">查询权限详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="p1050234162710"><a name="p1050234162710"></a><a name="p1050234162710"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询权限详情。</p>
</td>
</tr>
<tr id="row1616794922416"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p12167184922413"><a name="p12167184922413"></a><a name="p12167184922413"></a><a href="查询全局服务中的用户组权限.md">查询全局服务中的用户组权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037499_p1348102711334"><a name="zh-cn_topic_0222037499_p1348102711334"></a><a name="zh-cn_topic_0222037499_p1348102711334"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询全局服务中的用户组权限。</p>
</td>
</tr>
<tr id="row716714497248"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p31671497247"><a name="p31671497247"></a><a name="p31671497247"></a><a href="查询项目服务中的用户组权限.md">查询项目服务中的用户组权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="p61558535274"><a name="p61558535274"></a><a name="p61558535274"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询项目服务中的用户组权限。</p>
</td>
</tr>
<tr id="row1316712497247"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p616794952412"><a name="p616794952412"></a><a name="p616794952412"></a><a href="为用户组授予全局服务权限.md">为用户组授予全局服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="p181671149152412"><a name="p181671149152412"></a><a name="p181671149152412"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>为用户组授予全局服务权限。</p>
</td>
</tr>
<tr id="row16167134972412"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p11168249102410"><a name="p11168249102410"></a><a name="p11168249102410"></a><a href="为用户组授予项目服务权限.md">为用户组授予项目服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="p18168144917248"><a name="p18168144917248"></a><a name="p18168144917248"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>为用户组授予项目服务权限。</p>
</td>
</tr>
<tr id="row21681749132420"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p19168164911244"><a name="p19168164911244"></a><a name="p19168164911244"></a><a href="查询用户组是否拥有全局服务权限.md">查询用户组是否拥有全局服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="p20168949122413"><a name="p20168949122413"></a><a name="p20168949122413"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询用户组是否拥有全局服务权限。</p>
</td>
</tr>
<tr id="row745971742510"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p1459101713257"><a name="p1459101713257"></a><a name="p1459101713257"></a><a href="查询用户组是否拥有项目服务权限.md">查询用户组是否拥有项目服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="p15459111718259"><a name="p15459111718259"></a><a name="p15459111718259"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询用户组是否拥有项目服务权限。</p>
</td>
</tr>
<tr id="row167431846195213"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p574314612523"><a name="p574314612523"></a><a name="p574314612523"></a><a href="查询用户组的所有项目权限列表.md">查询用户组的所有项目权限列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="p874310462525"><a name="p874310462525"></a><a name="p874310462525"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询用户组所有项目服务权限列表。</p>
</td>
</tr>
<tr id="row2743346165215"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p47431646125215"><a name="p47431646125215"></a><a name="p47431646125215"></a><a href="查询用户组是否拥有所有项目指定权限.md">查询用户组是否拥有所有项目指定权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="p17743194695214"><a name="p17743194695214"></a><a name="p17743194695214"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询用户组是否拥有所有项目指定权限。</p>
</td>
</tr>
<tr id="row6743164614529"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p474374610521"><a name="p474374610521"></a><a name="p474374610521"></a><a href="移除用户组的所有项目服务权限.md">移除用户组的所有项目服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="p1374316463528"><a name="p1374316463528"></a><a name="p1374316463528"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>移除用户组的所有项目服务权限。</p>
</td>
</tr>
<tr id="row13459171752518"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p114591717172519"><a name="p114591717172519"></a><a name="p114591717172519"></a><a href="移除用户组的全局服务权限.md">移除用户组的全局服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037475_p7301728173316"><a name="zh-cn_topic_0222037475_p7301728173316"></a><a name="zh-cn_topic_0222037475_p7301728173316"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>移除用户组的全局服务权限。</p>
</td>
</tr>
<tr id="row1545981712517"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p11459111719252"><a name="p11459111719252"></a><a name="p11459111719252"></a><a href="移除用户组的项目服务权限.md">移除用户组的项目服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037450_p41037287332"><a name="zh-cn_topic_0222037450_p41037287332"></a><a name="zh-cn_topic_0222037450_p41037287332"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>移除用户组的项目服务权限。</p>
</td>
</tr>
<tr id="row14459191712258"><td class="cellrowborder" valign="top" width="29.38%" headers="mcps1.1.3.1.1 "><p id="p445910174254"><a name="p445910174254"></a><a name="p445910174254"></a><a href="为用户组授予所有项目服务权限.md">为用户组授予所有项目服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.62%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224679530_p1752775218518"><a name="zh-cn_topic_0224679530_p1752775218518"></a><a name="zh-cn_topic_0224679530_p1752775218518"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>为用户组授予所有项目服务权限。</p>
</td>
</tr>
</tbody>
</table>

## 自定义策略管理<a name="section1018555582920"></a>

<a name="table19423114919298"></a>
<table><thead align="left"><tr id="row114241149112913"><th class="cellrowborder" valign="top" width="29.64%" id="mcps1.1.3.1.1"><p id="p942494916299"><a name="p942494916299"></a><a name="p942494916299"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="70.36%" id="mcps1.1.3.1.2"><p id="p1942484916298"><a name="p1942484916298"></a><a name="p1942484916298"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row842416492299"><td class="cellrowborder" valign="top" width="29.64%" headers="mcps1.1.3.1.1 "><p id="p4424174952917"><a name="p4424174952917"></a><a name="p4424174952917"></a><a href="查询自定义策略列表.md">查询自定义策略列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.36%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037472_p1345675524011"><a name="zh-cn_topic_0222037472_p1345675524011"></a><a name="zh-cn_topic_0222037472_p1345675524011"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询自定义策略列表。</p>
</td>
</tr>
<tr id="row7424104915299"><td class="cellrowborder" valign="top" width="29.64%" headers="mcps1.1.3.1.1 "><p id="p134242049122920"><a name="p134242049122920"></a><a name="p134242049122920"></a><a href="查询自定义策略详情.md">查询自定义策略详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.36%" headers="mcps1.1.3.1.2 "><p id="p10424949102916"><a name="p10424949102916"></a><a name="p10424949102916"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询自定义策略详情。</p>
</td>
</tr>
<tr id="row442419497292"><td class="cellrowborder" valign="top" width="29.64%" headers="mcps1.1.3.1.1 "><p id="p3424104932920"><a name="p3424104932920"></a><a name="p3424104932920"></a><a href="创建云服务自定义策略.md">创建云服务自定义策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.36%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037452_p124162508317"><a name="zh-cn_topic_0222037452_p124162508317"></a><a name="zh-cn_topic_0222037452_p124162508317"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>创建云服务自定义策略。</p>
</td>
</tr>
<tr id="row19424194919297"><td class="cellrowborder" valign="top" width="29.64%" headers="mcps1.1.3.1.1 "><p id="p742424912911"><a name="p742424912911"></a><a name="p742424912911"></a><a href="创建委托自定义策略.md">创建委托自定义策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.36%" headers="mcps1.1.3.1.2 "><p id="p5424124917296"><a name="p5424124917296"></a><a name="p5424124917296"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>创建委托自定义策略。</p>
</td>
</tr>
<tr id="row11424134922920"><td class="cellrowborder" valign="top" width="29.64%" headers="mcps1.1.3.1.1 "><p id="p15424204962917"><a name="p15424204962917"></a><a name="p15424204962917"></a><a href="修改云服务自定义策略.md">修改云服务自定义策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.36%" headers="mcps1.1.3.1.2 "><p id="p1442464972910"><a name="p1442464972910"></a><a name="p1442464972910"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改云服务自定义策略。</p>
</td>
</tr>
<tr id="row4424194915299"><td class="cellrowborder" valign="top" width="29.64%" headers="mcps1.1.3.1.1 "><p id="p842444952910"><a name="p842444952910"></a><a name="p842444952910"></a><a href="修改委托自定义策略.md">修改委托自定义策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.36%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037497_p11764131913410"><a name="zh-cn_topic_0222037497_p11764131913410"></a><a name="zh-cn_topic_0222037497_p11764131913410"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改委托自定义策略。</p>
</td>
</tr>
<tr id="row74241491294"><td class="cellrowborder" valign="top" width="29.64%" headers="mcps1.1.3.1.1 "><p id="p1642411499297"><a name="p1642411499297"></a><a name="p1642411499297"></a><a href="删除自定义策略.md">删除自定义策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.36%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222037462_p172541054104117"><a name="zh-cn_topic_0222037462_p172541054104117"></a><a name="zh-cn_topic_0222037462_p172541054104117"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>删除自定义策略。</p>
</td>
</tr>
</tbody>
</table>

## 委托管理<a name="section123052092482"></a>

<a name="table137158524471"></a>
<table><thead align="left"><tr id="row1271595254712"><th class="cellrowborder" valign="top" width="30.25%" id="mcps1.1.3.1.1"><p id="p117151652124717"><a name="p117151652124717"></a><a name="p117151652124717"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="69.75%" id="mcps1.1.3.1.2"><p id="p1171517521472"><a name="p1171517521472"></a><a name="p1171517521472"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row67156522476"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p4715115274713"><a name="p4715115274713"></a><a name="p4715115274713"></a><a href="查询指定条件下的委托列表.md">查询指定条件下的委托列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p187155527476"><a name="p187155527476"></a><a name="p187155527476"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询指定条件下的委托列表。</p>
</td>
</tr>
<tr id="row1271505215475"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p871575213470"><a name="p871575213470"></a><a name="p871575213470"></a><a href="查询委托详情.md">查询委托详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p17715145215474"><a name="p17715145215474"></a><a name="p17715145215474"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询委托详情。</p>
</td>
</tr>
<tr id="row971575211472"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p127151152174711"><a name="p127151152174711"></a><a name="p127151152174711"></a><a href="创建委托.md">创建委托</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p12715185254717"><a name="p12715185254717"></a><a name="p12715185254717"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>创建委托。</p>
</td>
</tr>
<tr id="row97151752194710"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p1571512527477"><a name="p1571512527477"></a><a name="p1571512527477"></a><a href="修改委托.md">修改委托</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222594389_p1735084816556"><a name="zh-cn_topic_0222594389_p1735084816556"></a><a name="zh-cn_topic_0222594389_p1735084816556"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改委托。</p>
</td>
</tr>
<tr id="row197151352144713"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p18715175204720"><a name="p18715175204720"></a><a name="p18715175204720"></a><a href="删除委托.md">删除委托</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p1471535214475"><a name="p1471535214475"></a><a name="p1471535214475"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>删除委托。</p>
</td>
</tr>
<tr id="row77154525479"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p7715175204710"><a name="p7715175204710"></a><a name="p7715175204710"></a><a href="查询全局服务中的委托权限.md">查询全局服务中的委托权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222594422_p1887534865516"><a name="zh-cn_topic_0222594422_p1887534865516"></a><a name="zh-cn_topic_0222594422_p1887534865516"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询全局服务中的委托权限。</p>
</td>
</tr>
<tr id="row1715165264710"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p1971555214472"><a name="p1971555214472"></a><a name="p1971555214472"></a><a href="查询项目服务中的委托权限.md">查询项目服务中的委托权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p17151552164711"><a name="p17151552164711"></a><a name="p17151552164711"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询项目服务中的委托权限。</p>
</td>
</tr>
<tr id="row12992458184713"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p16992135815477"><a name="p16992135815477"></a><a name="p16992135815477"></a><a href="为委托授予全局服务权限.md">为委托授予全局服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p29924581472"><a name="p29924581472"></a><a name="p29924581472"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>为委托授予全局服务权限。</p>
</td>
</tr>
<tr id="row13992258204714"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p13992155884715"><a name="p13992155884715"></a><a name="p13992155884715"></a><a href="为委托授予项目服务权限.md">为委托授予项目服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p399210581471"><a name="p399210581471"></a><a name="p399210581471"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>为委托授予项目服务权限。</p>
</td>
</tr>
<tr id="row499216583479"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p12993758124714"><a name="p12993758124714"></a><a name="p12993758124714"></a><a href="查询委托是否拥有全局服务权限.md">查询委托是否拥有全局服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0222594363_p9254184910551"><a name="zh-cn_topic_0222594363_p9254184910551"></a><a name="zh-cn_topic_0222594363_p9254184910551"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询委托是否拥有全局服务权限。</p>
</td>
</tr>
<tr id="row12993155812478"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p20993258114710"><a name="p20993258114710"></a><a name="p20993258114710"></a><a href="查询委托是否拥有项目服务权限.md">查询委托是否拥有项目服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p999325854713"><a name="p999325854713"></a><a name="p999325854713"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询委托是否拥有项目服务权限。</p>
</td>
</tr>
<tr id="row1799395874716"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p599318589471"><a name="p599318589471"></a><a name="p599318589471"></a><a href="移除委托的全局服务权限.md">移除委托的全局服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p19934582471"><a name="p19934582471"></a><a name="p19934582471"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>移除委托的全局服务权限。</p>
</td>
</tr>
<tr id="row12993125812479"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p129931958164719"><a name="p129931958164719"></a><a name="p129931958164719"></a><a href="移除委托的项目服务权限.md">移除委托的项目服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p199385874719"><a name="p199385874719"></a><a name="p199385874719"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>移除委托的项目服务权限。</p>
</td>
</tr>
<tr id="row1899325824714"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p099345844720"><a name="p099345844720"></a><a name="p099345844720"></a><a href="查询委托下的所有项目服务权限列表.md">查询委托下的所有项目服务权限列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p18683136612"><a name="p18683136612"></a><a name="p18683136612"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询委托所有项目服务权限列表。</p>
</td>
</tr>
<tr id="row1431517382501"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p73158380506"><a name="p73158380506"></a><a name="p73158380506"></a><a href="为委托授予所有项目服务权限.md">为委托授予所有项目服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p18315203865014"><a name="p18315203865014"></a><a name="p18315203865014"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>为委托授予所有项目服务权限。</p>
</td>
</tr>
<tr id="row3315153820501"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p4315638105010"><a name="p4315638105010"></a><a name="p4315638105010"></a><a href="检查委托下是否具有所有项目服务权限.md">检查委托下是否具有所有项目服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p9315738115018"><a name="p9315738115018"></a><a name="p9315738115018"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>检查委托是否具有所有项目服务权限。</p>
</td>
</tr>
<tr id="row20315163855020"><td class="cellrowborder" valign="top" width="30.25%" headers="mcps1.1.3.1.1 "><p id="p731563810502"><a name="p731563810502"></a><a name="p731563810502"></a><a href="移除委托下的所有项目服务权限.md">移除委托下的所有项目服务权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.75%" headers="mcps1.1.3.1.2 "><p id="p520765311178"><a name="p520765311178"></a><a name="p520765311178"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>移除委托的所有项目服务权限。</p>
</td>
</tr>
</tbody>
</table>

## 企业项目管理<a name="section9352415144919"></a>

<a name="table1128192784915"></a>
<table><thead align="left"><tr id="row7282172784920"><th class="cellrowborder" valign="top" width="29.92%" id="mcps1.1.3.1.1"><p id="p12500143512492"><a name="p12500143512492"></a><a name="p12500143512492"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="70.08%" id="mcps1.1.3.1.2"><p id="p85001350491"><a name="p85001350491"></a><a name="p85001350491"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row8282192764915"><td class="cellrowborder" valign="top" width="29.92%" headers="mcps1.1.3.1.1 "><p id="p11915915502"><a name="p11915915502"></a><a name="p11915915502"></a><a href="查询企业项目关联的用户组.md">查询企业项目关联的用户组</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.08%" headers="mcps1.1.3.1.2 "><p id="p6640266502"><a name="p6640266502"></a><a name="p6640266502"></a>该接口用于查询指定ID的企业项目所关联的用户组。</p>
</td>
</tr>
<tr id="row1628202716497"><td class="cellrowborder" valign="top" width="29.92%" headers="mcps1.1.3.1.1 "><p id="p4447202425018"><a name="p4447202425018"></a><a name="p4447202425018"></a><a href="查询企业项目关联用户组的权限.md">查询企业项目关联用户组的权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.08%" headers="mcps1.1.3.1.2 "><p id="p17446924155016"><a name="p17446924155016"></a><a name="p17446924155016"></a>该接口用于查询指定ID的企业项目所关联用户组的权限，适用于待查询的企业项目已关联了用户组。</p>
</td>
</tr>
<tr id="row770618564124"><td class="cellrowborder" valign="top" width="29.92%" headers="mcps1.1.3.1.1 "><p id="p1670785631213"><a name="p1670785631213"></a><a name="p1670785631213"></a><a href="基于用户组为企业项目授权.md">基于用户组为企业项目授权</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.08%" headers="mcps1.1.3.1.2 "><p id="p17426108131519"><a name="p17426108131519"></a><a name="p17426108131519"></a>该接口用于给指定ID的企业项目授权，建立企业项目、用户组和权限的绑定关系。</p>
</td>
</tr>
<tr id="row292920573491"><td class="cellrowborder" valign="top" width="29.92%" headers="mcps1.1.3.1.1 "><p id="p1149702813508"><a name="p1149702813508"></a><a name="p1149702813508"></a><a href="删除企业项目关联用户组的权限.md">删除企业项目关联用户组的权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.08%" headers="mcps1.1.3.1.2 "><p id="p7747356489"><a name="p7747356489"></a><a name="p7747356489"></a>该接口提供删除某个企业项目关联的用户组权限。</p>
</td>
</tr>
<tr id="row7929125744910"><td class="cellrowborder" valign="top" width="29.92%" headers="mcps1.1.3.1.1 "><p id="p39292579497"><a name="p39292579497"></a><a name="p39292579497"></a><a href="查询用户组关联的企业项目.md">查询用户组关联的企业项目</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.08%" headers="mcps1.1.3.1.2 "><p id="p1192945754913"><a name="p1192945754913"></a><a name="p1192945754913"></a>该接口可用于查询用户组所关联的企业项目。</p>
</td>
</tr>
<tr id="row44001833115013"><td class="cellrowborder" valign="top" width="29.92%" headers="mcps1.1.3.1.1 "><p id="p18400193325018"><a name="p18400193325018"></a><a name="p18400193325018"></a><a href="查询用户直接关联的企业项目.md">查询用户直接关联的企业项目</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.08%" headers="mcps1.1.3.1.2 "><p id="p440023315508"><a name="p440023315508"></a><a name="p440023315508"></a>该接口可用于查询用户所关联的企业项目。</p>
</td>
</tr>
<tr id="row45708163501"><td class="cellrowborder" valign="top" width="29.92%" headers="mcps1.1.3.1.1 "><p id="p14570141675018"><a name="p14570141675018"></a><a name="p14570141675018"></a><a href="查询企业项目直接关联用户.md">查询企业项目直接关联用户</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.08%" headers="mcps1.1.3.1.2 "><p id="p1357011614503"><a name="p1357011614503"></a><a name="p1357011614503"></a>该接口可用于查询企业项目直接关联用户。</p>
</td>
</tr>
<tr id="row557021610501"><td class="cellrowborder" valign="top" width="29.92%" headers="mcps1.1.3.1.1 "><p id="p757041616509"><a name="p757041616509"></a><a name="p757041616509"></a><a href="查询企业项目直接关联用户的权限.md">查询企业项目直接关联用户的权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.08%" headers="mcps1.1.3.1.2 "><p id="p357041615018"><a name="p357041615018"></a><a name="p357041615018"></a>该接口可用于查询企业项目直接关联用户的权限。</p>
</td>
</tr>
<tr id="row1957031619506"><td class="cellrowborder" valign="top" width="29.92%" headers="mcps1.1.3.1.1 "><p id="p1857014166508"><a name="p1857014166508"></a><a name="p1857014166508"></a><a href="基于用户为企业项目授权.md">基于用户为企业项目授权</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.08%" headers="mcps1.1.3.1.2 "><p id="p19570171695014"><a name="p19570171695014"></a><a name="p19570171695014"></a>该接口可用于基于用户为企业项目授权。</p>
</td>
</tr>
<tr id="row1557011615015"><td class="cellrowborder" valign="top" width="29.92%" headers="mcps1.1.3.1.1 "><p id="p3570151612505"><a name="p3570151612505"></a><a name="p3570151612505"></a><a href="删除企业项目直接关联用户的权限.md">删除企业项目直接关联用户的权限</a></p>
</td>
<td class="cellrowborder" valign="top" width="70.08%" headers="mcps1.1.3.1.2 "><p id="p10570121613508"><a name="p10570121613508"></a><a name="p10570121613508"></a>该接口可用于删除企业项目直接关联用户的权限，</p>
</td>
</tr>
</tbody>
</table>

## 安全设置<a name="section587194175313"></a>

<a name="table85817146537"></a>
<table><thead align="left"><tr id="row205911145539"><th class="cellrowborder" valign="top" width="30.599999999999998%" id="mcps1.1.3.1.1"><p id="p185941455311"><a name="p185941455311"></a><a name="p185941455311"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="69.39999999999999%" id="mcps1.1.3.1.2"><p id="p25951485312"><a name="p25951485312"></a><a name="p25951485312"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row115901418531"><td class="cellrowborder" valign="top" width="30.599999999999998%" headers="mcps1.1.3.1.1 "><p id="p2059201417537"><a name="p2059201417537"></a><a name="p2059201417537"></a><a href="修改帐号操作保护策略.md">修改帐号操作保护策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.39999999999999%" headers="mcps1.1.3.1.2 "><p id="p105901413531"><a name="p105901413531"></a><a name="p105901413531"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改帐号操作保护策略。</p>
</td>
</tr>
<tr id="row18595148534"><td class="cellrowborder" valign="top" width="30.599999999999998%" headers="mcps1.1.3.1.1 "><p id="p959614115316"><a name="p959614115316"></a><a name="p959614115316"></a><a href="查询帐号操作保护策略.md">查询帐号操作保护策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.39999999999999%" headers="mcps1.1.3.1.2 "><p id="p15991419537"><a name="p15991419537"></a><a name="p15991419537"></a>该接口可以用于查询帐号操作保护策略。</p>
</td>
</tr>
<tr id="row85913142531"><td class="cellrowborder" valign="top" width="30.599999999999998%" headers="mcps1.1.3.1.1 "><p id="p959714205316"><a name="p959714205316"></a><a name="p959714205316"></a><a href="修改帐号密码策略.md">修改帐号密码策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.39999999999999%" headers="mcps1.1.3.1.2 "><p id="p1346443901918"><a name="p1346443901918"></a><a name="p1346443901918"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改帐号密码策略。</p>
</td>
</tr>
<tr id="row1459814135315"><td class="cellrowborder" valign="top" width="30.599999999999998%" headers="mcps1.1.3.1.1 "><p id="p1959131411539"><a name="p1959131411539"></a><a name="p1959131411539"></a><a href="查询帐号密码策略.md">查询帐号密码策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.39999999999999%" headers="mcps1.1.3.1.2 "><p id="p1859314185317"><a name="p1859314185317"></a><a name="p1859314185317"></a>该接口可以用于查询帐号密码策略。</p>
</td>
</tr>
<tr id="row359131455317"><td class="cellrowborder" valign="top" width="30.599999999999998%" headers="mcps1.1.3.1.1 "><p id="p19591914175311"><a name="p19591914175311"></a><a name="p19591914175311"></a><a href="修改帐号登录策略.md">修改帐号登录策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.39999999999999%" headers="mcps1.1.3.1.2 "><p id="p85913142534"><a name="p85913142534"></a><a name="p85913142534"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改帐号登录策略。</p>
</td>
</tr>
<tr id="row13591514185311"><td class="cellrowborder" valign="top" width="30.599999999999998%" headers="mcps1.1.3.1.1 "><p id="p959101419533"><a name="p959101419533"></a><a name="p959101419533"></a><a href="查询帐号登录策略.md">查询帐号登录策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.39999999999999%" headers="mcps1.1.3.1.2 "><p id="p111711611102015"><a name="p111711611102015"></a><a name="p111711611102015"></a>该接口可以用于查询帐号登录策略。</p>
</td>
</tr>
<tr id="row1359114175317"><td class="cellrowborder" valign="top" width="30.599999999999998%" headers="mcps1.1.3.1.1 "><p id="p12598140536"><a name="p12598140536"></a><a name="p12598140536"></a><a href="修改帐号控制台访问策略.md">修改帐号控制台访问策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.39999999999999%" headers="mcps1.1.3.1.2 "><p id="p759131417533"><a name="p759131417533"></a><a name="p759131417533"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改帐号控制台访问策略。</p>
</td>
</tr>
<tr id="row179121414185416"><td class="cellrowborder" valign="top" width="30.599999999999998%" headers="mcps1.1.3.1.1 "><p id="p11912214155412"><a name="p11912214155412"></a><a name="p11912214155412"></a><a href="查询帐号控制台访问策略.md">查询帐号控制台访问策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.39999999999999%" headers="mcps1.1.3.1.2 "><p id="p1391220142548"><a name="p1391220142548"></a><a name="p1391220142548"></a>该接口可以用于查询帐号控制台访问控制策略。</p>
</td>
</tr>
<tr id="row15912191475412"><td class="cellrowborder" valign="top" width="30.599999999999998%" headers="mcps1.1.3.1.1 "><p id="p19120142540"><a name="p19120142540"></a><a name="p19120142540"></a><a href="修改帐号接口访问策略.md">修改帐号接口访问策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.39999999999999%" headers="mcps1.1.3.1.2 "><p id="p1791210148541"><a name="p1791210148541"></a><a name="p1791210148541"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>修改帐号接口访问策略。</p>
</td>
</tr>
<tr id="row1591281413547"><td class="cellrowborder" valign="top" width="30.599999999999998%" headers="mcps1.1.3.1.1 "><p id="p11912101412546"><a name="p11912101412546"></a><a name="p11912101412546"></a><a href="查询帐号接口访问策略.md">查询帐号接口访问策略</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.39999999999999%" headers="mcps1.1.3.1.2 "><p id="p267816554200"><a name="p267816554200"></a><a name="p267816554200"></a>该接口可以用于查询帐号接口访问控制策略。</p>
</td>
</tr>
</tbody>
</table>

## 联邦身份认证管理<a name="section4441165695718"></a>

<a name="table1518111612598"></a>
<table><thead align="left"><tr id="row151816166590"><th class="cellrowborder" valign="top" width="30.86%" id="mcps1.1.3.1.1"><p id="p2181141685910"><a name="p2181141685910"></a><a name="p2181141685910"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="69.14%" id="mcps1.1.3.1.2"><p id="p16181101615920"><a name="p16181101615920"></a><a name="p16181101615920"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row11181171695917"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p15181916145914"><a name="p15181916145914"></a><a name="p15181916145914"></a><a href="SP-initiated方式.md">通过联邦认证获取Token（SP initiated方式）</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p718117167595"><a name="p718117167595"></a><a name="p718117167595"></a>通过Openstack Client和ShibbolethECP Client获取联邦认证Token。</p>
</td>
</tr>
<tr id="row91811416165914"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p618116169590"><a name="p618116169590"></a><a name="p618116169590"></a><a href="IdP-initiated方式.md">通过联邦认证获取Token（IdP initiated方式）</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p131813166597"><a name="p131813166597"></a><a name="p131813166597"></a>以“Client4ShibbolethIdP”脚本为例，介绍IdP initiated方式获取联邦认证Token的方法。</p>
</td>
</tr>
<tr id="row41811116195916"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p1418117168597"><a name="p1418117168597"></a><a name="p1418117168597"></a><a href="查询身份提供商列表.md">查询身份提供商列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p3181181615919"><a name="p3181181615919"></a><a name="p3181181615919"></a>该接口可以用于查询身份提供商列表。</p>
</td>
</tr>
<tr id="row13181191615596"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p201811816115915"><a name="p201811816115915"></a><a name="p201811816115915"></a><a href="查询身份提供商详情.md">查询身份提供商详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p1618101625917"><a name="p1618101625917"></a><a name="p1618101625917"></a>该接口可以用于查询身份提供商详情。</p>
</td>
</tr>
<tr id="row718115161597"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p16181101611599"><a name="p16181101611599"></a><a name="p16181101611599"></a><a href="创建身份提供商.md">创建身份提供商</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p718151612593"><a name="p718151612593"></a><a name="p718151612593"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>注册身份提供商。</p>
</td>
</tr>
<tr id="row318110168598"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p17181121635911"><a name="p17181121635911"></a><a name="p17181121635911"></a><a href="修改SAML身份提供商配置.md">修改SAML身份提供商配置</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276697_p1884514611453"><a name="zh-cn_topic_0224276697_p1884514611453"></a><a name="zh-cn_topic_0224276697_p1884514611453"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>更新身份提供商。</p>
</td>
</tr>
<tr id="row13181201605912"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p318131665918"><a name="p318131665918"></a><a name="p318131665918"></a><a href="删除SAML身份提供商.md">删除SAML身份提供商</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p418191615599"><a name="p418191615599"></a><a name="p418191615599"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>删除身份提供商。</p>
</td>
</tr>
<tr id="row9124935392"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p20124143514920"><a name="p20124143514920"></a><a name="p20124143514920"></a><a href="查询映射列表.md">查询映射列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p1912414354912"><a name="p1912414354912"></a><a name="p1912414354912"></a>该接口可以用于查询映射列表。</p>
</td>
</tr>
<tr id="row012419351493"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p1812412351597"><a name="p1812412351597"></a><a name="p1812412351597"></a><a href="查询映射详情.md">查询映射详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p912413517916"><a name="p912413517916"></a><a name="p912413517916"></a>该接口可以用于查询映射详情。</p>
</td>
</tr>
<tr id="row151241435490"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p14124163520917"><a name="p14124163520917"></a><a name="p14124163520917"></a><a href="注册映射.md">注册映射</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p17125173513915"><a name="p17125173513915"></a><a name="p17125173513915"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>注册映射。</p>
</td>
</tr>
<tr id="row131257357913"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p1812516351097"><a name="p1812516351097"></a><a name="p1812516351097"></a><a href="更新映射.md">更新映射</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p21250350918"><a name="p21250350918"></a><a name="p21250350918"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>更新映射。</p>
</td>
</tr>
<tr id="row1795951841412"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p1995961891417"><a name="p1995961891417"></a><a name="p1995961891417"></a><a href="删除映射.md">删除映射</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p18469714113019"><a name="p18469714113019"></a><a name="p18469714113019"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>删除映射。</p>
</td>
</tr>
<tr id="row169591018111418"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p5959111818147"><a name="p5959111818147"></a><a name="p5959111818147"></a><a href="查询协议列表.md">查询协议列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p895991810140"><a name="p895991810140"></a><a name="p895991810140"></a>该接口可以用于查询协议列表。</p>
</td>
</tr>
<tr id="row095931816149"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p995981811416"><a name="p995981811416"></a><a name="p995981811416"></a><a href="查询协议详情.md">查询协议详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p1396071891413"><a name="p1396071891413"></a><a name="p1396071891413"></a>该接口可以用于查询协议详情。</p>
</td>
</tr>
<tr id="row109601818101410"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p19609186142"><a name="p19609186142"></a><a name="p19609186142"></a><a href="注册协议.md">注册协议</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p1960171820141"><a name="p1960171820141"></a><a name="p1960171820141"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>注册协议（将协议关联到某一身份提供商）。</p>
</td>
</tr>
<tr id="row10960201831416"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p9960818111412"><a name="p9960818111412"></a><a name="p9960818111412"></a><a href="更新协议.md">更新协议</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p69605187146"><a name="p69605187146"></a><a name="p69605187146"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>更新协议。</p>
</td>
</tr>
<tr id="row996071813146"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p79602185140"><a name="p79602185140"></a><a name="p79602185140"></a><a href="删除协议.md">删除协议</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276875_p10255153255111"><a name="zh-cn_topic_0224276875_p10255153255111"></a><a name="zh-cn_topic_0224276875_p10255153255111"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>删除协议。</p>
</td>
</tr>
<tr id="row9960141818147"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p139607188145"><a name="p139607188145"></a><a name="p139607188145"></a><a href="查询Metadata文件.md">查询Metadata文件</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p199601318181410"><a name="p199601318181410"></a><a name="p199601318181410"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>查询身份提供商导入到IAM中的Metadata文件。</p>
</td>
</tr>
<tr id="row1896031813142"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p29601318131418"><a name="p29601318131418"></a><a name="p29601318131418"></a><a href="查询Keystone的Metadata文件.md">查询Keystone的Metadata文件</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="zh-cn_topic_0224276972_p12917122355019"><a name="zh-cn_topic_0224276972_p12917122355019"></a><a name="zh-cn_topic_0224276972_p12917122355019"></a>该接口可以用于查询keystone的Metadata文件。</p>
</td>
</tr>
<tr id="row20691642121513"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p47094271512"><a name="p47094271512"></a><a name="p47094271512"></a><a href="导入Metadata文件.md">导入Metadata文件</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p5702425154"><a name="p5702425154"></a><a name="p5702425154"></a>该接口可以用于<a href="https://support.huaweicloud.com/usermanual-iam/iam_01_0001.html" target="_blank" rel="noopener noreferrer">管理员</a>导入Metadata文件。</p>
</td>
</tr>
<tr id="row147094212151"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p370174241517"><a name="p370174241517"></a><a name="p370174241517"></a><a href="获取联邦认证unscoped-token(IdP-initiated).md">获取联邦认证unscoped token(IdP initiated)</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p1970142171519"><a name="p1970142171519"></a><a name="p1970142171519"></a>该接口可以用于通过IdP initiated的联邦认证方式获取unscoped token。</p>
</td>
</tr>
<tr id="row117064217155"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p47054214157"><a name="p47054214157"></a><a name="p47054214157"></a><a href="获取联邦认证scoped-token.md">获取联邦认证scoped token</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p10701642151519"><a name="p10701642151519"></a><a name="p10701642151519"></a>该接口可以用于通过联邦认证方式获取scoped token。</p>
</td>
</tr>
<tr id="row107010426154"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p1970134271519"><a name="p1970134271519"></a><a name="p1970134271519"></a><a href="获取联邦认证token(OpenID-Connect-ID-token方式).md">获取联邦认证token(OpenID Connect ID token方式)</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p1770124213154"><a name="p1770124213154"></a><a name="p1770124213154"></a>该接口可以用于通过OpenID Connect ID token方式获取联邦认证token。</p>
</td>
</tr>
<tr id="row1770134241517"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p77010423152"><a name="p77010423152"></a><a name="p77010423152"></a><a href="获取联邦认证unscoped-token(OpenID-Connect-ID-token方式).md">获取联邦认证unscoped token(OpenID Connect ID token方式)</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p157019426153"><a name="p157019426153"></a><a name="p157019426153"></a>该接口可以用于通过OpenID Connect ID token方式获取联邦认证unscoped token。</p>
</td>
</tr>
<tr id="row1707151017179"><td class="cellrowborder" valign="top" width="30.86%" headers="mcps1.1.3.1.1 "><p id="p17707151091710"><a name="p17707151091710"></a><a name="p17707151091710"></a><a href="查询联邦用户可以访问的帐号列表.md">查询联邦用户可以访问的帐号列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="69.14%" headers="mcps1.1.3.1.2 "><p id="p167071110171718"><a name="p167071110171718"></a><a name="p167071110171718"></a>该接口用于查询联邦用户可以访问的帐号列表。</p>
</td>
</tr>
</tbody>
</table>

## 自定义身份代理<a name="section442112169209"></a>

<a name="table17276142617212"></a>
<table><thead align="left"><tr id="row22775262210"><th class="cellrowborder" valign="top" width="31.65%" id="mcps1.1.3.1.1"><p id="p227762632113"><a name="p227762632113"></a><a name="p227762632113"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="68.35%" id="mcps1.1.3.1.2"><p id="p202771326132110"><a name="p202771326132110"></a><a name="p202771326132110"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row5277132615214"><td class="cellrowborder" valign="top" width="31.65%" headers="mcps1.1.3.1.1 "><p id="p122771266213"><a name="p122771266213"></a><a name="p122771266213"></a><a href="获取自定义身份代理登录票据.md">获取自定义身份代理登录票据</a></p>
</td>
<td class="cellrowborder" valign="top" width="68.35%" headers="mcps1.1.3.1.2 "><p id="p027719266219"><a name="p027719266219"></a><a name="p027719266219"></a>该接口用于获取自定义身份代理登录票据logintoken。</p>
</td>
</tr>
</tbody>
</table>

## 版本信息管理<a name="section2282132062013"></a>

<a name="table534114101229"></a>
<table><thead align="left"><tr id="row12341310192218"><th class="cellrowborder" valign="top" width="32.17%" id="mcps1.1.3.1.1"><p id="p934216108228"><a name="p934216108228"></a><a name="p934216108228"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="67.83%" id="mcps1.1.3.1.2"><p id="p1834241052212"><a name="p1834241052212"></a><a name="p1834241052212"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row14342141022218"><td class="cellrowborder" valign="top" width="32.17%" headers="mcps1.1.3.1.1 "><p id="p134212107229"><a name="p134212107229"></a><a name="p134212107229"></a><a href="查询Keystone-API的版本信息.md">查询Keystone API的版本信息</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.83%" headers="mcps1.1.3.1.2 "><p id="p12342161082210"><a name="p12342161082210"></a><a name="p12342161082210"></a>该接口用于查询Keystone API的版本信息。</p>
</td>
</tr>
<tr id="row1434271042218"><td class="cellrowborder" valign="top" width="32.17%" headers="mcps1.1.3.1.1 "><p id="p123422010112212"><a name="p123422010112212"></a><a name="p123422010112212"></a><a href="查询Keystone-API的3-0版本信息.md">查询Keystone API的3.0版本信息</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.83%" headers="mcps1.1.3.1.2 "><p id="p53421810172210"><a name="p53421810172210"></a><a name="p53421810172210"></a>该接口用于查询Keystone API的3.0版本的信息。</p>
</td>
</tr>
</tbody>
</table>

## 服务和终端节点<a name="section2252823152013"></a>

<a name="table20277191218232"></a>
<table><thead align="left"><tr id="row527715123235"><th class="cellrowborder" valign="top" width="32.690000000000005%" id="mcps1.1.3.1.1"><p id="p17277141282317"><a name="p17277141282317"></a><a name="p17277141282317"></a>接口</p>
</th>
<th class="cellrowborder" valign="top" width="67.31%" id="mcps1.1.3.1.2"><p id="p152773123238"><a name="p152773123238"></a><a name="p152773123238"></a>说明</p>
</th>
</tr>
</thead>
<tbody><tr id="row2277101272318"><td class="cellrowborder" valign="top" width="32.690000000000005%" headers="mcps1.1.3.1.1 "><p id="p7277191282312"><a name="p7277191282312"></a><a name="p7277191282312"></a><a href="查询服务列表.md">查询服务列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.31%" headers="mcps1.1.3.1.2 "><p id="p14277141262310"><a name="p14277141262310"></a><a name="p14277141262310"></a>该接口可以用于查询服务列表。</p>
</td>
</tr>
<tr id="row927791218233"><td class="cellrowborder" valign="top" width="32.690000000000005%" headers="mcps1.1.3.1.1 "><p id="p12771612172313"><a name="p12771612172313"></a><a name="p12771612172313"></a><a href="查询服务详情.md">查询服务详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.31%" headers="mcps1.1.3.1.2 "><p id="p527741232312"><a name="p527741232312"></a><a name="p527741232312"></a>该接口可以用于查询服务详情。</p>
</td>
</tr>
<tr id="row3277111217234"><td class="cellrowborder" valign="top" width="32.690000000000005%" headers="mcps1.1.3.1.1 "><p id="p14277112152317"><a name="p14277112152317"></a><a name="p14277112152317"></a><a href="查询服务目录.md">查询服务目录</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.31%" headers="mcps1.1.3.1.2 "><p id="p1927719121237"><a name="p1927719121237"></a><a name="p1927719121237"></a>该接口可以用于查询请求头中X-Auth-Token对应的服务目录。</p>
</td>
</tr>
<tr id="row122771122239"><td class="cellrowborder" valign="top" width="32.690000000000005%" headers="mcps1.1.3.1.1 "><p id="p102771012132315"><a name="p102771012132315"></a><a name="p102771012132315"></a><a href="查询终端节点列表.md">查询终端节点列表</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.31%" headers="mcps1.1.3.1.2 "><p id="p12771812192315"><a name="p12771812192315"></a><a name="p12771812192315"></a>该接口可以用于查询终端节点列表。</p>
</td>
</tr>
<tr id="row72778129239"><td class="cellrowborder" valign="top" width="32.690000000000005%" headers="mcps1.1.3.1.1 "><p id="p827714122234"><a name="p827714122234"></a><a name="p827714122234"></a><a href="查询终端节点详情.md">查询终端节点详情</a></p>
</td>
<td class="cellrowborder" valign="top" width="67.31%" headers="mcps1.1.3.1.2 "><p id="p42774123236"><a name="p42774123236"></a><a name="p42774123236"></a>该接口可以用于查询终端节点详情。</p>
</td>
</tr>
</tbody>
</table>

