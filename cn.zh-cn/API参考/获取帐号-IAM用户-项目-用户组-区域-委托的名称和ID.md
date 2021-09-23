# 获取帐号、IAM用户、项目、用户组、区域、委托的名称和ID<a name="iam_17_0002"></a>

## 获取帐号、IAM用户、项目名称和ID<a name="section13960118204914"></a>

-   **从控制台获取帐号名、帐号ID、用户名、用户ID、项目名称、项目ID**
    1.  在华为云首页右上角，点击“控制台”。
    2.  在右上角的用户名中选择“我的凭证“。

        **图 1**  进入我的凭证<a name="fig52163612527"></a>  
        ![](figures/进入我的凭证.png "进入我的凭证")

    3.  在“我的凭证”界面，API凭证页签中，查看帐号名、帐号ID、用户名、用户ID、项目名称、项目ID。

        **图 2**  查看帐号名、帐号ID、用户名、用户ID、项目名称、项目ID<a name="fig6764316135210"></a>  
        ![](figures/查看帐号名-帐号ID-用户名-用户ID-项目名称-项目ID.png "查看帐号名-帐号ID-用户名-用户ID-项目名称-项目ID")


-   **调用API获取项目ID**

    项目ID还可通过调用[查询指定条件下的项目信息](查询指定条件下的项目列表.md)API获取。

    获取项目ID的接口为“GET https://\{Endpoint\}/v3/projects/”，其中\{Endpoint\}为IAM的终端节点，可以从[地区和终端节点](https://developer.huaweicloud.com/endpoint?IAM)获取。接口的认证鉴权请参见[认证鉴权](认证鉴权.md)。

    响应示例如下，其中projects下的“id”即为项目ID。

    ```
    { 
        "projects": [ 
            { 
                "domain_id": "65382450e8f64ac0870cd180d...", 
                "is_domain": false, 
                "parent_id": "65382450e8f64ac0870cd180d1...", 
                "name": "cn-north-4", 
                "description": "", 
                "links": { 
                    "next": null, 
                    "previous": null, 
                    "self": "https://www.example.com/v3/projects/a4a5d4098fb4474fa22cd0..." 
                }, 
                "id": "a4a5d4098fb4474fa22cd05f897xxxx", 
                "enabled": true 
            } 
        ], 
        "links": { 
            "next": null, 
            "previous": null, 
            "self": "https://www.example.com/v3/projects" 
        } 
    }
    ```


## 获取用户组名称和ID<a name="section79181350155213"></a>

1.  登录华为云，进入IAM控制台，选择“用户组”页签。
2.  单击需要查询的用户组前的下拉框，即可查询用户组名称、用户组ID。

    **图 3**  查询用户组名称、用户组ID<a name="fig1264911578520"></a>  
    ![](figures/查询用户组名称-用户组ID.png "查询用户组名称-用户组ID")


## 获取区域ID<a name="section14125113011553"></a>

1.  登录华为云，进入IAM控制台，选择“项目”页签。
2.  “项目”列的内容即为所属区域对应的ID。

    **图 4**  查看区域ID<a name="fig971171316537"></a>  
    ![](figures/查看区域ID.png "查看区域ID")


## 获取委托名称和ID<a name="section468501394115"></a>

1.  登录华为云，进入IAM控制台，选择“委托”页签。
2.  鼠标移动到需要查询名称和ID的委托上，黑色框中出现的第一行为委托名称，第二行为委托ID。

    **图 5**  查看委托ID<a name="fig1386193419534"></a>  
    ![](figures/查看委托ID.png "查看委托ID")


