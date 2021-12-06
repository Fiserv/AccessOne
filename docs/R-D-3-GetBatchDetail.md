# **R.D.3 GetBatchDetail*

|**Service Operation GetBatchDetail ()**|
| :-: |
|**Name**|GetBatchDetail|
|**Description**|Return transaction-details data of a selected batch number|
|**Pre-conditions**|+ **Parameters:** 

|**Name**|**Default**|**Require**|
| :-: | :-: | :-: |
|[BatchNumber](#P_BatchNumber)||True|
|[ReportDate](#P_ReportDate)|ToDay – 1||
|[MerchantNumber](#P_MerchantNumbet)||True|
|[PageSize](#P_PageSize)|100||
|[CurrentPageIndex](#P_CurrentPageSize)|0||

|||
| :- | :- |
|**Post-conditions**|Return  Batch Detail|
|**SOAP API**|
|**Message Exchange Pattern**|<p>**SAMPLE REQUEST:**</p><p></p><p>**See RESPONSE ATTACHED:** </p><p></p>|
|**REST API**|
|**Request URL**|/rest/GetBatchDetail|
|**Method**|POST|
|**Request Body Sample XML**|<p></p><p><BatchDetailFilter xmlns="http://api.lonestar.com/types"></p><p>`    `<MerchantNumber>02550630018</MerchantNumber></p><p>`    `<ReportDate>2019-10-13</ReportDate></p><p>`    `<CurrentPageIndex>1</CurrentPageIndex></p><p>`    `<PageSize>10</PageSize></p><p>`    `<BatchNumber>24421001</BatchNumber></p><p></BatchDetailFilter></p><p></p>|
|**Request Response Sample XML**||

