# 支持IAM资源粒度授权的云服务<a name="iam_01_0610"></a>

如果您需要授予IAM用户特定资源的相应权限，可以[创建自定义策略](创建自定义策略.md)并选择特定资源，该IAM用户将仅拥有对应资源的使用权限。例如创建自定义策略时，选择资源类型并添加资源路径：OBS:\*:\*:bucket:TestBucket\*，即可授予IAM用户以TestBucket命名开头的桶相应权限。

下表为当前华为云支持资源级别授权的云服务及对应资源类型。

**表 1**  支持资源粒度授权的云服务及其资源类型

<a name="table194341254175413"></a>
<table><thead align="left"><tr id="row1443415465412"><th class="cellrowborder" valign="top" width="33.33666633336667%" id="mcps1.2.4.1.1"><p id="p0434175475418"><a name="p0434175475418"></a><a name="p0434175475418"></a>服务</p>
</th>
<th class="cellrowborder" valign="top" width="33.28667133286672%" id="mcps1.2.4.1.2"><p id="p443414544543"><a name="p443414544543"></a><a name="p443414544543"></a>资源类型</p>
</th>
<th class="cellrowborder" valign="top" width="33.37666233376663%" id="mcps1.2.4.1.3"><p id="p15434105435418"><a name="p15434105435418"></a><a name="p15434105435418"></a>资源名称</p>
</th>
</tr>
</thead>
<tbody><tr id="row13675121052913"><td class="cellrowborder" rowspan="2" valign="top" width="33.33666633336667%" headers="mcps1.2.4.1.1 "><p id="p13868271653"><a name="p13868271653"></a><a name="p13868271653"></a><a href="https://support.huaweicloud.com/usermanual-obs/obs_03_0154.html" target="_blank" rel="noopener noreferrer">对象存储服务（OBS）</a></p>
</td>
<td class="cellrowborder" valign="top" width="33.28667133286672%" headers="mcps1.2.4.1.2 "><p id="p841918397413"><a name="p841918397413"></a><a name="p841918397413"></a>bucket</p>
</td>
<td class="cellrowborder" valign="top" width="33.37666233376663%" headers="mcps1.2.4.1.3 "><p id="p17419539642"><a name="p17419539642"></a><a name="p17419539642"></a>桶</p>
</td>
</tr>
<tr id="row0675161032916"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p2868471356"><a name="p2868471356"></a><a name="p2868471356"></a>object</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p11868773510"><a name="p11868773510"></a><a name="p11868773510"></a>对象</p>
</td>
</tr>
<tr id="row1443410549545"><td class="cellrowborder" rowspan="8" valign="top" width="33.33666633336667%" headers="mcps1.2.4.1.1 "><p id="p186571542838"><a name="p186571542838"></a><a name="p186571542838"></a><a href="https://support.huaweicloud.com/usermanual-ief/ief_01_0066.html" target="_blank" rel="noopener noreferrer">智能边缘平台（IEF）</a></p>
</td>
<td class="cellrowborder" valign="top" width="33.28667133286672%" headers="mcps1.2.4.1.2 "><p id="p083217162017"><a name="p083217162017"></a><a name="p083217162017"></a>product</p>
</td>
<td class="cellrowborder" valign="top" width="33.37666233376663%" headers="mcps1.2.4.1.3 "><p id="p68321719208"><a name="p68321719208"></a><a name="p68321719208"></a>产品</p>
</td>
</tr>
<tr id="row11087417115"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p283171712019"><a name="p283171712019"></a><a name="p283171712019"></a>node</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1783151782020"><a name="p1783151782020"></a><a name="p1783151782020"></a>边缘节点</p>
</td>
</tr>
<tr id="row146576421230"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p198311702012"><a name="p198311702012"></a><a name="p198311702012"></a>group</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p683191717203"><a name="p683191717203"></a><a name="p683191717203"></a>边缘节点组</p>
</td>
</tr>
<tr id="row875410451739"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p168311177205"><a name="p168311177205"></a><a name="p168311177205"></a>deployment</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1483131792010"><a name="p1483131792010"></a><a name="p1483131792010"></a>应用部署</p>
</td>
</tr>
<tr id="row146793548311"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1283171782013"><a name="p1283171782013"></a><a name="p1283171782013"></a>batchjob</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p583161711209"><a name="p583161711209"></a><a name="p583161711209"></a>批量作业</p>
</td>
</tr>
<tr id="row45631521238"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1083917162017"><a name="p1083917162017"></a><a name="p1083917162017"></a>application</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p9831117162010"><a name="p9831117162010"></a><a name="p9831117162010"></a>应用模板</p>
</td>
</tr>
<tr id="row271612505312"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p6831517112015"><a name="p6831517112015"></a><a name="p6831517112015"></a>appVersion</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p10831617182018"><a name="p10831617182018"></a><a name="p10831617182018"></a>应用模板版本</p>
</td>
</tr>
<tr id="row642419488319"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1838174201"><a name="p1838174201"></a><a name="p1838174201"></a>IEFInstance</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p58311716202"><a name="p58311716202"></a><a name="p58311716202"></a>IEF实例</p>
</td>
</tr>
<tr id="row24345543544"><td class="cellrowborder" rowspan="6" valign="top" width="33.33666633336667%" headers="mcps1.2.4.1.1 "><p id="p19785647913"><a name="p19785647913"></a><a name="p19785647913"></a><a href="https://support.huaweicloud.com/usermanual-dli/dli_01_0417.html" target="_blank" rel="noopener noreferrer">数据湖探索（DLI）</a></p>
</td>
<td class="cellrowborder" valign="top" width="33.28667133286672%" headers="mcps1.2.4.1.2 "><p id="p8114155391910"><a name="p8114155391910"></a><a name="p8114155391910"></a>queue</p>
</td>
<td class="cellrowborder" valign="top" width="33.37666233376663%" headers="mcps1.2.4.1.3 "><p id="p101144535193"><a name="p101144535193"></a><a name="p101144535193"></a>队列</p>
</td>
</tr>
<tr id="row9638345817"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p14114135341913"><a name="p14114135341913"></a><a name="p14114135341913"></a>database</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p111149531199"><a name="p111149531199"></a><a name="p111149531199"></a>数据库</p>
</td>
</tr>
<tr id="row1247505118"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p7114195315196"><a name="p7114195315196"></a><a name="p7114195315196"></a>table</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p211555318198"><a name="p211555318198"></a><a name="p211555318198"></a>表</p>
</td>
</tr>
<tr id="row5785104718116"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p121151553191919"><a name="p121151553191919"></a><a name="p121151553191919"></a>column</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1011512538195"><a name="p1011512538195"></a><a name="p1011512538195"></a>列</p>
</td>
</tr>
<tr id="row141381325427"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p1611525313190"><a name="p1611525313190"></a><a name="p1611525313190"></a>datasourceauth</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p19115115317198"><a name="p19115115317198"></a><a name="p19115115317198"></a>安全认证信息</p>
</td>
</tr>
<tr id="row1170219335218"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p81153532196"><a name="p81153532196"></a><a name="p81153532196"></a>jobs</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p2115115331911"><a name="p2115115331911"></a><a name="p2115115331911"></a>作业</p>
</td>
</tr>
<tr id="row45161899517"><td class="cellrowborder" rowspan="2" valign="top" width="33.33666633336667%" headers="mcps1.2.4.1.1 "><p id="p1516179557"><a name="p1516179557"></a><a name="p1516179557"></a><a href="https://support.huaweicloud.com/usermanual-ges/ges_01_0074.html" target="_blank" rel="noopener noreferrer">图引擎服务（GES）</a></p>
</td>
<td class="cellrowborder" valign="top" width="33.28667133286672%" headers="mcps1.2.4.1.2 "><p id="p15161591257"><a name="p15161591257"></a><a name="p15161591257"></a>graphName</p>
</td>
<td class="cellrowborder" valign="top" width="33.37666233376663%" headers="mcps1.2.4.1.3 "><p id="p145161892516"><a name="p145161892516"></a><a name="p145161892516"></a>图名称</p>
</td>
</tr>
<tr id="row14471249950"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p044717491856"><a name="p044717491856"></a><a name="p044717491856"></a>backupName</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p844710491853"><a name="p844710491853"></a><a name="p844710491853"></a>备份名称</p>
</td>
</tr>
<tr id="row0668534616"><td class="cellrowborder" rowspan="2" valign="top" width="33.33666633336667%" headers="mcps1.2.4.1.1 "><p id="p146691031168"><a name="p146691031168"></a><a name="p146691031168"></a><a href="https://support.huaweicloud.com/usermanual-functiongraph/functiongraph_01_0215.html" target="_blank" rel="noopener noreferrer">函数工作流服务（FunctionGraph）</a></p>
</td>
<td class="cellrowborder" valign="top" width="33.28667133286672%" headers="mcps1.2.4.1.2 "><p id="p166694316619"><a name="p166694316619"></a><a name="p166694316619"></a>function</p>
</td>
<td class="cellrowborder" valign="top" width="33.37666233376663%" headers="mcps1.2.4.1.3 "><p id="p96691535617"><a name="p96691535617"></a><a name="p96691535617"></a>函数</p>
</td>
</tr>
<tr id="row1648517532610"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p19485153166"><a name="p19485153166"></a><a name="p19485153166"></a>trigger</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1048585317615"><a name="p1048585317615"></a><a name="p1048585317615"></a>触发器</p>
</td>
</tr>
<tr id="row1143013552068"><td class="cellrowborder" rowspan="2" valign="top" width="33.33666633336667%" headers="mcps1.2.4.1.1 "><p id="p15241232271"><a name="p15241232271"></a><a name="p15241232271"></a><a href="https://support.huaweicloud.com/usermanual-rabbitmq/CreatingCustomPolicy.html" target="_blank" rel="noopener noreferrer">分布式消息服务（DMS）</a></p>
</td>
<td class="cellrowborder" valign="top" width="33.28667133286672%" headers="mcps1.2.4.1.2 "><p id="p114301855265"><a name="p114301855265"></a><a name="p114301855265"></a>rabbitmq</p>
</td>
<td class="cellrowborder" valign="top" width="33.37666233376663%" headers="mcps1.2.4.1.3 "><p id="p843018550610"><a name="p843018550610"></a><a name="p843018550610"></a>RabbitMQ实例</p>
</td>
</tr>
<tr id="row14241532371"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p6241133210712"><a name="p6241133210712"></a><a name="p6241133210712"></a>kafka</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p1324118321076"><a name="p1324118321076"></a><a name="p1324118321076"></a>Kafka实例</p>
</td>
</tr>
<tr id="row52100348713"><td class="cellrowborder" valign="top" width="33.33666633336667%" headers="mcps1.2.4.1.1 "><p id="p1210133410712"><a name="p1210133410712"></a><a name="p1210133410712"></a>设备接入（IoTDA）</p>
</td>
<td class="cellrowborder" valign="top" width="33.28667133286672%" headers="mcps1.2.4.1.2 "><p id="p121016345720"><a name="p121016345720"></a><a name="p121016345720"></a>app</p>
</td>
<td class="cellrowborder" valign="top" width="33.37666233376663%" headers="mcps1.2.4.1.3 "><p id="p62101734376"><a name="p62101734376"></a><a name="p62101734376"></a>资源空间ID</p>
</td>
</tr>
<tr id="row179601171488"><td class="cellrowborder" valign="top" width="33.33666633336667%" headers="mcps1.2.4.1.1 "><p id="p096191717816"><a name="p096191717816"></a><a name="p096191717816"></a><a href="https://support.huaweicloud.com/usermanual-dew/dew_01_0161.html" target="_blank" rel="noopener noreferrer">数据加密服务（KMS）</a></p>
</td>
<td class="cellrowborder" valign="top" width="33.28667133286672%" headers="mcps1.2.4.1.2 "><p id="p179611917685"><a name="p179611917685"></a><a name="p179611917685"></a>KeyId</p>
</td>
<td class="cellrowborder" valign="top" width="33.37666233376663%" headers="mcps1.2.4.1.3 "><p id="p1896191715816"><a name="p1896191715816"></a><a name="p1896191715816"></a>密钥ID</p>
</td>
</tr>
<tr id="row106522571981"><td class="cellrowborder" rowspan="2" valign="top" width="33.33666633336667%" headers="mcps1.2.4.1.1 "><p id="p96528571815"><a name="p96528571815"></a><a name="p96528571815"></a>自动驾驶云服务（Octopus）</p>
</td>
<td class="cellrowborder" valign="top" width="33.28667133286672%" headers="mcps1.2.4.1.2 "><p id="p5652105710814"><a name="p5652105710814"></a><a name="p5652105710814"></a>dataset</p>
</td>
<td class="cellrowborder" valign="top" width="33.37666233376663%" headers="mcps1.2.4.1.3 "><p id="p16652125720817"><a name="p16652125720817"></a><a name="p16652125720817"></a>数据集</p>
</td>
</tr>
<tr id="row165205281594"><td class="cellrowborder" valign="top" headers="mcps1.2.4.1.1 "><p id="p552018283918"><a name="p552018283918"></a><a name="p552018283918"></a>replay</p>
</td>
<td class="cellrowborder" valign="top" headers="mcps1.2.4.1.2 "><p id="p95205281592"><a name="p95205281592"></a><a name="p95205281592"></a>视频回放</p>
</td>
</tr>
<tr id="row13376313919"><td class="cellrowborder" valign="top" width="33.33666633336667%" headers="mcps1.2.4.1.1 "><p id="p7677204114313"><a name="p7677204114313"></a><a name="p7677204114313"></a><a href="https://support.huaweicloud.com/mgtg-dws/dws_01_0148.html" target="_blank" rel="noopener noreferrer">数据仓库服务(DWS)</a></p>
</td>
<td class="cellrowborder" valign="top" width="33.28667133286672%" headers="mcps1.2.4.1.2 "><p id="p1433710317914"><a name="p1433710317914"></a><a name="p1433710317914"></a>cluster</p>
</td>
<td class="cellrowborder" valign="top" width="33.37666233376663%" headers="mcps1.2.4.1.3 "><p id="p133376311992"><a name="p133376311992"></a><a name="p133376311992"></a>集群</p>
</td>
</tr>
</tbody>
</table>

