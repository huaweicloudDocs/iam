# 创建IAM用户<a name="iam_02_0001"></a>

如果您是[管理员](使用前必读.md#section209491111991)，在华为云购买了多种资源，例如弹性云服务器、云硬盘、裸金属服务器等，您需要将资源分配给企业中不同的员工或者应用程序使用，为了避免分享自己的账号密码，您可以使用IAM的用户管理功能，给员工或应用程序创建IAM用户。

默认情况下，**新创建的IAM用户没有任何权限**，管理员需要将其加入用户组，并给[用户组授权](创建用户组并授权.md)，用户组中的用户将获得用户组的权限。授权后，IAM用户就可以基于权限对云服务进行操作。

“admin”为华为云缺省提供的用户组，具有所有云服务资源的操作权限。将用户加入该用户组后，用户可以操作并使用所有云服务资源，包括但不仅限于创建用户组及用户、修改用户组权限、管理华为云资源等。

## 操作步骤<a name="section4493316"></a>

1.  登录华为云，在右上角单击“控制台”。

    ![](figures/zh-cn_image_0221110858.png)

2.  在控制台页面，鼠标移动至右上方的用户名，在下拉列表中选择“统一身份认证”。

    ![](figures/进入IAM.png)

3.  在统一身份认证服务，左侧导航窗格中，单击“用户”\>“创建用户”。
4.  在“创建用户”页面填写“用户信息”。如需一次创建多个用户，可以单击“添加用户”进行批量创建，每次最多可创建10个用户。

    **图 1**  配置用户信息<a name="fig4362111394210"></a>  
    ![](figures/配置用户信息.png "配置用户信息")

    **表 1**  用户信息

    <a name="table2085713152213"></a>
    <table><thead align="left"><tr id="row1585971132215"><th class="cellrowborder" valign="top" width="7.870000000000001%" id="mcps1.2.3.1.1"><p id="p49241120132516"><a name="p49241120132516"></a><a name="p49241120132516"></a>用户信息</p>
    </th>
    <th class="cellrowborder" valign="top" width="92.13%" id="mcps1.2.3.1.2"><p id="p1490342011259"><a name="p1490342011259"></a><a name="p1490342011259"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row148161516192520"><td class="cellrowborder" valign="top" width="7.870000000000001%" headers="mcps1.2.3.1.1 "><p id="p1185913111223"><a name="p1185913111223"></a><a name="p1185913111223"></a><span class="keyword" id="keyword5942172718229"><a name="keyword5942172718229"></a><a name="keyword5942172718229"></a>用户名</span></p>
    </td>
    <td class="cellrowborder" valign="top" width="92.13%" headers="mcps1.2.3.1.2 "><p id="p2085913117229"><a name="p2085913117229"></a><a name="p2085913117229"></a>必填。IAM用户登录华为云的用户名，此处以“James”和“Alice”为例。</p>
    </td>
    </tr>
    <tr id="row138598110225"><td class="cellrowborder" valign="top" width="7.870000000000001%" headers="mcps1.2.3.1.1 "><p id="p1185911132218"><a name="p1185911132218"></a><a name="p1185911132218"></a>邮箱</p>
    </td>
    <td class="cellrowborder" valign="top" width="92.13%" headers="mcps1.2.3.1.2 "><p id="p1085915132215"><a name="p1085915132215"></a><a name="p1085915132215"></a>“访问方式”选择“首次登录时设置”时必填，选择其他时选填。IAM用户绑定的邮箱，可作为子账户的登录凭证，也可由IAM用户自己绑定。</p>
    </td>
    </tr>
    <tr id="row58605162217"><td class="cellrowborder" valign="top" width="7.870000000000001%" headers="mcps1.2.3.1.1 "><p id="p178600116224"><a name="p178600116224"></a><a name="p178600116224"></a>手机号</p>
    </td>
    <td class="cellrowborder" valign="top" width="92.13%" headers="mcps1.2.3.1.2 "><p id="p386020114221"><a name="p386020114221"></a><a name="p386020114221"></a>选填。IAM用户绑定的手机号，可作为子账户的登录凭证，也可由IAM用户自己绑定。</p>
    </td>
    </tr>
    <tr id="row7386153642217"><td class="cellrowborder" valign="top" width="7.870000000000001%" headers="mcps1.2.3.1.1 "><p id="p63874367227"><a name="p63874367227"></a><a name="p63874367227"></a>描述</p>
    </td>
    <td class="cellrowborder" valign="top" width="92.13%" headers="mcps1.2.3.1.2 "><p id="p17387193652218"><a name="p17387193652218"></a><a name="p17387193652218"></a>选填。记录IAM用户相关信息。</p>
    </td>
    </tr>
    </tbody>
    </table>

5.  在“创建用户”页面选择“访问方式”，完成后单击“下一步”。

    **图 2**  配置访问方式<a name="fig5859185810416"></a>  
    ![](figures/配置访问方式.png "配置访问方式")

    **表 2**  访问方式

    <a name="table1777851811233"></a>
    <table><thead align="left"><tr id="row8779161802313"><th class="cellrowborder" valign="top" id="mcps1.2.5.1.1"><p id="p9262183452512"><a name="p9262183452512"></a><a name="p9262183452512"></a>访问方式</p>
    </th>
    <th class="cellrowborder" colspan="2" valign="top" id="mcps1.2.5.1.2"><p id="p11261134192512"><a name="p11261134192512"></a><a name="p11261134192512"></a>配置信息</p>
    </th>
    <th class="cellrowborder" valign="top" id="mcps1.2.5.1.3"><p id="p8233173420253"><a name="p8233173420253"></a><a name="p8233173420253"></a>说明</p>
    </th>
    </tr>
    </thead>
    <tbody><tr id="row10564326122520"><td class="cellrowborder" rowspan="5" valign="top" width="16.03839616038396%" headers="mcps1.2.5.1.1 "><p id="p1877941802314"><a name="p1877941802314"></a><a name="p1877941802314"></a>华为云管理控制台访问</p>
    <p id="p1877981832320"><a name="p1877981832320"></a><a name="p1877981832320"></a>&nbsp;&nbsp;</p>
    <p id="p96251705354"><a name="p96251705354"></a><a name="p96251705354"></a>&nbsp;&nbsp;</p>
    <p id="p131270377358"><a name="p131270377358"></a><a name="p131270377358"></a>&nbsp;&nbsp;</p>
    </td>
    <td class="cellrowborder" rowspan="3" valign="top" width="11.848815118488151%" headers="mcps1.2.5.1.2 "><p id="p1477916185230"><a name="p1477916185230"></a><a name="p1477916185230"></a>控制台登录密码设置方式</p>
    <p id="p8779151814236"><a name="p8779151814236"></a><a name="p8779151814236"></a>&nbsp;&nbsp;</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.248775122487752%" headers="mcps1.2.5.1.2 "><p id="p77791718142319"><a name="p77791718142319"></a><a name="p77791718142319"></a>首次登录时设置</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.86401359864014%" headers="mcps1.2.5.1.3 "><p id="p1181173162413"><a name="p1181173162413"></a><a name="p1181173162413"></a>如果您不是用户James的使用主体，建议您选择该方式，输入用户的邮箱和手机，用户James通过邮件中的一次性链接登录华为云，自行设置密码。</p>
    </td>
    </tr>
    <tr id="row10205744184711"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p620614449475"><a name="p620614449475"></a><a name="p620614449475"></a>自动生成</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p5206944124720"><a name="p5206944124720"></a><a name="p5206944124720"></a>仅在创建单个用户时适用，如果您本次创建2个及以上的用户，则不支持此方式。</p>
    </td>
    </tr>
    <tr id="row17779418132313"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p13779818132315"><a name="p13779818132315"></a><a name="p13779818132315"></a>自定义</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p1681219311246"><a name="p1681219311246"></a><a name="p1681219311246"></a>如果您是用户James的使用主体，建议您选择该方式，设置自己的登录密码。</p>
    </td>
    </tr>
    <tr id="row18624110123516"><td class="cellrowborder" rowspan="2" valign="top" headers="mcps1.2.5.1.1 "><p id="p156264012357"><a name="p156264012357"></a><a name="p156264012357"></a>登录保护</p>
    <p id="p1112723710353"><a name="p1112723710353"></a><a name="p1112723710353"></a>&nbsp;&nbsp;</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p1462615012356"><a name="p1462615012356"></a><a name="p1462615012356"></a>开启登录保护</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p16916235313"><a name="p16916235313"></a><a name="p16916235313"></a>开启登录保护后，IAM用户登录时，除了在登录页面输入用户名和密码外（第一次身份验证），还需要在登录验证页面输入验证码（第二次身份验证），该功能是一种安全实践，建议开启登录保护，多次身份认证可以提高账号安全性。</p>
    <p id="p1887784834514"><a name="p1887784834514"></a><a name="p1887784834514"></a>您可以选择通过手机、邮箱、虚拟MFA进行登录验证。</p>
    </td>
    </tr>
    <tr id="row5127153713351"><td class="cellrowborder" valign="top" headers="mcps1.2.5.1.1 "><p id="p11127113743516"><a name="p11127113743516"></a><a name="p11127113743516"></a>不开启</p>
    </td>
    <td class="cellrowborder" valign="top" headers="mcps1.2.5.1.2 "><p id="p1512763715358"><a name="p1512763715358"></a><a name="p1512763715358"></a>创建完成后，如需开启登录保护，请参见：<a href="敏感操作.md#zh-cn_topic_0176803437_section6465133820464">登录保护</a>。</p>
    </td>
    </tr>
    <tr id="row177991813236"><td class="cellrowborder" valign="top" width="16.03839616038396%" headers="mcps1.2.5.1.1 "><p id="p14779141832318"><a name="p14779141832318"></a><a name="p14779141832318"></a>编程访问</p>
    </td>
    <td class="cellrowborder" valign="top" width="11.848815118488151%" headers="mcps1.2.5.1.2 "><p id="p7779181822310"><a name="p7779181822310"></a><a name="p7779181822310"></a>--</p>
    </td>
    <td class="cellrowborder" valign="top" width="12.248775122487752%" headers="mcps1.2.5.1.2 "><p id="p15779121852314"><a name="p15779121852314"></a><a name="p15779121852314"></a>--</p>
    </td>
    <td class="cellrowborder" valign="top" width="59.86401359864014%" headers="mcps1.2.5.1.3 "><p id="p6812103102416"><a name="p6812103102416"></a><a name="p6812103102416"></a>创建用户完成后即可下载本次创建的所有用户的<a href="https://support.huaweicloud.com/usermanual-ca/ca_01_0003.html" target="_blank" rel="noopener noreferrer">访问密钥（AK/SK）</a>。一个用户最多拥有两个访问密钥。这些AK/SK可以对华为云进行编程调用，例如，通过API调用方式访问华为云时，您可能需要使用访问密钥。</p>
    </td>
    </tr>
    </tbody>
    </table>

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   用户可以使用此处设置的用户名、邮箱或手机号码任意一种方式登录华为云。  
    >-   当用户忘记密码时，可以通过此处绑定的邮箱或手机自行重置密码，如果用户没有绑定邮箱或手机号码，只能由管理员重置密码。  
    >-   用户登录系统时，输入用户名和初始密码后，将进入“首次登录修改密码”，需要创建一个新密码，该功能可以保证用户的密码是由使用者本人所设置，防止密码泄露。  

6.  单击“下一步”，将用户加入到用户组（可选）。

    -   将用户加入用户组，用户将具备用户组的权限，这一过程即给用户授权。
    -   如需创建新的用户组，可单击“创建用户组”，填写用户组名称和描述（可选），创建成功后即可将用户加入到新创建的用户组中。

    >![](public_sys-resources/icon-note.gif) **说明：**   
    >-   如果该用户是管理员，可以将用户加入默认用户组“admin”中。  
    >-   一个用户可以同时加入多个用户组。  

7.  单击“下一步”，IAM用户创建完成，用户列表中显示新创建的IAM用户。如果[表2 访问方式](#table1777851811233)勾选了“编程访问”，可在此页面下载访问密钥。

    ![](figures/用户创建成功.png)


