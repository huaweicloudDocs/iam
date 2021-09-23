# 对IAM用户的权限进行安全审计<a name="iam_20_0004"></a>

## 场景描述<a name="section648293905613"></a>

企业级用户通常需要对公有云上IAM用户的权限定期进行安全审计，以确定IAM用户的权限未超出规定的范围。例如：除帐号和审计员用户以外的所有IAM用户都不应该具有任何IAM的管理权限。此安全审计往往是系统定期自动检查，所以需要使用API来完成。

本章节指导用户如何使用API调用的方式对IAM用户的权限进行安全审计，您可进一步通过编程手段完成定期安全审计工作。

## 前提条件<a name="section4209170135714"></a>

审计员对IAM用户的权限进行安全审计时，需要拥有IAM ReadOnlyAccess（推荐）或Security Administrator权限。

## 总体思路<a name="section14318192517579"></a>

对IAM用户的权限进行安全审计，步骤如下：

1.  查询用户组列表；
2.  查询全局服务中的用户组权限；
3.  查询项目服务中的用户组权限；
4.  确定需要审计的权限，查询用户组中的IAM用户，进行安全审计。

涉及的接口如下：

-   [查询用户组列表](查询用户组列表.md)
-   [查询全局服务中的用户组权限](查询全局服务中的用户组权限.md)
-   [查询项目服务中的用户组权限](查询项目服务中的用户组权限.md)
-   [管理员查询用户组所包含的IAM用户](管理员查询用户组所包含的IAM用户.md)

## 步骤1：查询用户组列表<a name="section242218592194"></a>

URI：GET /v3/groups

API文档详情请参见：[查询用户组列表](查询用户组列表.md)

API Explorer在线调试请参见：[查询用户组列表](https://apiexplorer.developer.huaweicloud.com/apiexplorer/debug?product=IAM&api=KeystoneListGroups)

-   请求示例

    ```
    GET https://iam.myhuaweicloud.com/v3/groups
    ```

-   响应示例

    ```
    {
         "groups":[
             {
                 "create_time":1536293929624,
                 "description":"IAMDescription",
                 "domain_id":"d78cbac186b744899480f25bd022....",
                 "id":"5b050baea9db472c88cbae67e8d6....",
                 "links":{
                     "self":"https://iam.huaweicloud.com/v3/groups/5b050baea9db472c88cbae67e8d6...."
                 },
                 "name":"IAMGroupA"
             },
             {
                 "create_time":1578107542861,
                 "description":"IAMDescription",
                 "domain_id":"d78cbac186b744899480f25bd022....",
                 "id":"07609e7eb200250a3f7dc003cb7a....",
                 "links":{
                     "self":"https://iam.huaweicloud.com/v3/groups/07609e7eb200250a3f7dc003cb7a...."
                 },
                 "name":"IAMGroupB"
             }
         ],
         "links":{
             "self":"https://iam.huaweicloud.com/v3/groups"
         }
     }
    ```


## 步骤2：查询全局服务中的用户组权限<a name="section20134155012243"></a>

URI：GET /v3/domains/\{domain\_id\}/groups/\{group\_id\}/roles

API文档详情请参见：[查询全局服务中的用户组权限](查询全局服务中的用户组权限.md)

API Explorer在线调试请参见：[查询全局服务中的用户组权限](https://apiexplorer.developer.huaweicloud.com/apiexplorer/debug?product=IAM&api=KeystoneListPermissionsForGroupOnDomain)

-   请求示例

    ```
    GET https://iam.myhuaweicloud.com/v3/domains/{domain_id}/groups/{group_id}/roles
    ```

-   响应示例

    ```
    {
         "links":{
             "self":"https://iam.myhuaweicloud.com/v3/domains/d78cbac186b744899480f25bd022f468/groups/077d71374b8025173f61c003ea0a11ac/roles"
         },
         "roles":[
             {
                 "catalog":"CDN",
                 "description":"Allow Query Domains",
                 "description_cn":"查询域名信息",
                 "display_name":"CDN Domain Viewer",
                 "flag":"fine_grained",
                 "id":"db4259cce0ce47c9903dfdc195eb....",
                 "links":{
                     "self":"https://iam.myhuaweicloud.com/v3/roles/db4259cce0ce47c9903dfdc195eb...."
                 },
                 "name":"system_all_11",
                 "policy":{
                     "Statement":[
                         {
                             "Action":[
                                 "cdn:configuration:queryDomains",
                                 "cdn:configuration:queryOriginServerInfo",
                                 "cdn:configuration:queryOriginConfInfo",
                                 "cdn:configuration:queryHttpsConf",
                                 "cdn:configuration:queryCacheRule",
                                 "cdn:configuration:queryReferConf",
                                 "cdn:configuration:queryChargeMode",
                                 "cdn:configuration:queryCacheHistoryTask",
                                 "cdn:configuration:queryIpAcl",
                                 "cdn:configuration:queryResponseHeaderList"
                             ],
                             "Effect":"Allow"
                         }
                     ],
                     "Version":"1.1"
                 },
                 "type":"AX"
             }
         ]
     }
    ```


## 步骤3：查询项目服务中的用户组权限<a name="section36672196293"></a>

URI：GET /v3/projects/\{project\_id\}/groups/\{group\_id\}/roles

API文档详情请参见：[查询项目服务中的用户组权限](查询项目服务中的用户组权限.md)

API Explorer在线调试请参见：[查询项目服务中的用户组权限](https://apiexplorer.developer.huaweicloud.com/apiexplorer/debug?product=IAM&api=KeystoneListPermissionsForGroupOnDomain)

-   请求示例

    ```
    GET https://iam.myhuaweicloud.com/v3/projects/{project_id}/groups/{group_id}/roles
    ```


-   响应示例

    ```
    {
         "links":{
             "self":"https://iam.myhuaweicloud.com/v3/projects/065a7c66da0010992ff7c0031e5a..../groups/077d71374b8025173f61c003ea0a..../roles"
         },
         "roles":[
             {
                 "catalog":"AOM",
                 "description":"AOM read only",
                 "description_cn":"应用运维管理服务只读权限",
                 "display_name":"AOM Viewer",
                 "flag":"fine_grained",
                 "id":"75cfe22af2b3498d82b655fbb39d....",
                 "links":{
                     "self":"https://iam.myhuaweicloud.com/v3/roles/75cfe22af2b3498d82b655fbb39d...."
                 },
                 "name":"system_all_30",
                 "policy":{
                     "Statement":[
                         {
                             "Action":[
                                 "aom:*:list",
                                 "aom:*:get",
                                 "apm:*:list",
                                 "apm:*:get"
                             ],
                             "Effect":"Allow"
                         }
                     ],
                     "Version":"1.1"
                 },
                 "type":"XA"
             }
         ]
     }
    ```


## 步骤4：确定需要审计的权限，查询用户组中的IAM用户，进行安全审计<a name="section458061471214"></a>

URI：GET /v3/groups/\{group\_id\}/users

API文档详情请参见：[管理员查询用户组所包含的IAM用户](管理员查询用户组所包含的IAM用户.md)

API Explorer在线调试请参见：[管理员查询用户组所包含的IAM用户](https://apiexplorer.developer.huaweicloud.com/apiexplorer/debug?product=IAM&api=KeystoneListUsersForGroupByAdmin)

-   请求示例

    ```
    GET https://iam.myhuaweicloud.com/v3/groups/{group_id}/users
    ```

-   响应示例

    ```
    {
         "links":{
             "self":"https://iam.huaweicloud.com/v3/groups/07609e7eb200250a3f7dc003cb7a..../users"
         },
         "users":[
             {
                 "description":"--",
                 "domain_id":"d78cbac186b744899480f25bd022....",
                 "enabled":true,
                 "id":"07609fb9358010e21f7bc003751c....",
                 "last_project_id":"065a7c66da0010992ff7c0031e5a....",
                 "links":{
                     "self":"https://iam.huaweicloud.com/v3/users/07609fb9358010e21f7bc003751c...."
                 },
                 "name":"IAMUserA",
                 "pwd_status":true
             },
             {
                 "description":"",
                 "domain_id":"d78cbac186b744899480f25bd022....",
                 "enabled":true,
                 "id":"076837351e80251c1f0fc003afe4....",
                 "last_project_id":"065a7c66da0010992ff7c0031e5a....",
                 "links":{
                     "self":"https://iam.huaweicloud.com/v3/users/076837351e80251c1f0fc003afe4...."
                 },
                 "name":"IAMUserB",
                 "pwd_status":true
             }
         ]
     }
    ```


