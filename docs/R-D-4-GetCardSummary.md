# **R.D.4 GetCardSummary**

|**Service Operation GetCardSummary ()**|
| :-: |
|**Name**|GetCardSummary|
|**Description**|Return card summary data based on selected date range|
|**Pre-conditions**|+ **Parameters:** 

|**Name**|**Default**|
| :-: | :-: |
|[HierarchyFilterMode](#P_HierarchyFilterMode)|Platform|
|[HierarchyFilterValue](#P_HierarchyFilterValue)||
|[FromDate](#P_FromDate)|ToDay – 1|
|[ToDate](#P_ToDate)|ToDay – 1 |
|[PageSize](#P_PageSize)|100|
|[CurrentPageIndex](#P_CurrentPageSize)|0|
|[BatchNumber](#P_BatchNumber)||

||<p>** </p><p>+ **Contraints**:  </p><p>- [HierarchyFilterMode](#P_HierarchyFilterMode)** must be belong to group **[Ref**([II.3.1](#II_3_1))**]**</p><p>+ **Notes**: **[Ref([**III.5.1](#III_4_1))]**</p>|
| :- | :- |
|**Post-conditions**|Return  Card Summary|
|**SOAP API**|
|**Message Exchange Pattern**|<p>**SAMPLE REQUEST:**</p><p>**  </p><p>**See RESPONSE ATTACHED:** </p><p></p>|
|**REST API**|
|**Request URL**|/rest/GetCardSummary|
|**Method**|POST|
|**Request Body Sample XML**|<p></p><p><CardSummaryFilter xmlns="http://api.lonestar.com/types"></p><p>`    `<CurrentPageIndex>1</CurrentPageIndex></p><p>`    `<FromDate>2010-01-01T00:00:00</FromDate></p><p>`    `<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode></p><p>`    `<HierarchyFilterValue>02550630018</HierarchyFilterValue></p><p>`    `<PageSize>10</PageSize></p><p>`    `<ToDate>2019-10-23T00:00:00</ToDate></p><p>`    `<BatchNumber>24421001</BatchNumber></p><p></CardSummaryFilter></p><p></p>|
|**Request Response Sample XML**||


