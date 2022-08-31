# **D.1 GetBatchSummaryByEntity**

exec spa\_64\_ms\_LoneStar\_GetBatchHistory @PlatformID=1,@SiteID=1000,@DDSClient=64,@UserID='Capital',@UserIDMode='Client',@HierarchyFilterMode=N'PLATFORM',@HierarchyFilterValue=N'',@DateFilterMode=3,@BeginDate='2018-09-01 00:00:00',@EndDate='2018-09-07 00:00:00',@SubClientDrilldown=N'',@ClientDrilldown=N'',@IsMerchantList=0,@IsPaging=1,@IsCountPageTotal=0,@PageNo=1,@PageSize=10,@stOrder='ENTITYNAME DESC',@stFilter=''

go

exec spa\_64\_ms\_LoneStar\_GetBatchHistory\_Total @PlatformID=1,@SiteID=1000,@DDSClient=64,@UserID='Capital',@UserIDMode='Client',@HierarchyFilterMode=N'PLATFORM',@HierarchyFilterValue=N'',@DateFilterMode=3,@BeginDate='2018-09-01 00:00:00',@EndDate='2018-09-07 00:00:00',@SubClientDrilldown=N'',@ClientDrilldown=N'',@IsMerchantList=0,@stFilter=''

go


|**Service Operation GetBatchSummaryByEntity()**|
| :-: |
|**Name**|GetBatchSummaryByEntity|
|**Description**|Return batch summary data of hierarchy entity choice(s) based on the selected date range |
|**Pre-conditions**|<p>+ **Parameters: [Ref([**III.3.1](#III_2_1))]**</p><p>+ **Contraints**:  </p><p>- [HierarchyFilterMode](#P_HierarchyFilterMode)** must be belong to group **[Ref**([II.3.1](#II_3_1))**]**</p><p>+ **Notes**: **[Ref([**III.5.1](#III_4_1))]**</p>|
|**Post-conditions**|Return  Batch Hierarchy Summary|
|**SOAP API**|
|**Message Exchange Pattern**|<p>**SAMPLE REQUEST:**</p><p>**  </p><p>**See RESPONSE ATTACHED:** </p><p></p>|
|**REST API**|
|**Request URL**|/rest/GetBatchSummaryByEntity|
|**Method**|POST|
|**Request Body Sample XML**|<p></p><p><GenericReportFilter xmlns="http://api.lonestar.com/types"></p><p>`    `<CurrentPageIndex>1</CurrentPageIndex></p><p>`    `<FromDate>2010-01-01T00:00:00</FromDate></p><p>`    `<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode></p><p>`    `<HierarchyFilterValue>512888888888051</HierarchyFilterValue></p><p>`    `<PageSize>10</PageSize></p><p>`    `<ToDate>2019-10-23T00:00:00</ToDate></p><p>`    `<ViewLevel>None</ViewLevel></p><p></GenericReportFilter></p><p></p>|
|**Request Response Sample XML**||

