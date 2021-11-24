# **B.1 ENUMERATIONS**

### HierarchyFilterMode

||**Value**|**Description**|
| :- | :- | :- |
|**Common**|SubClient|<p>AO user created and managed by ISO client</p><p>Each sub client is responsible for managing a group of merchants – this is set up by ISO client</p>|
||Platform|Payment processing platform (Omaha, North, Memphis)|
||MasterSaleAgent|<p>AO user created and managed by ISO client</p><p>Each master sales agent in turn manages a group of sales agent assigned to them by ISO client</p>|
||CorporateName|Normalized corporate name|
||MerchantName|Normalized merchant name|
||MerchantNumber|Merchant Number|
|<p>**Omaha**</p><p></p>|Sys|System number. It defines the first level of processing and the second level of reporting after ISO-Client. Prins are assigned to Sys|
||SysPrin|Principal number, used as a level of reporting and processing in FDS. Agents are assigned to Prins|
||SysPrinAgent|Agent is a means of grouping merchants with the same Prin together for risk monitoring purposes. “Agent” is used by First Data to group retail merchants together in buckets like MOTO, e-Commerce, etc. |
||SalesAgent|Omaha sales agent|
||HeadquarterMerchantNumber|Merchant number of head merchant of a chain. A group of merchants owned by the same person or people is called chain. The head merchant of a chain is called headquarter merchant. |
|**North**|Bank|Bank number. (North) agents are assigned to banks|
||Agent|(North) Agent number. CORPs are assigned to agents|
||Corp|Corporate number. Grouping of merchants |
||NorthChain|A group of merchants owned by the same person or people, i.e. North’s counterpart to Omaha’s chain|
||NorthSalesAgent|North sales agent |
|**Memphis**|MasterChain|Master chain, used as a level of reporting for Memphis platform.  A group of merchants owned by the same person or people is called chain. Master chain is a group of (Memphis) chains. Chains are assigned to master chains |
||MemphisChain|Memphis’s counterpart to Omaha’s chain. |
||SalesmanNo|Memphis’ counterpart to North’s sales agent|
|**Others**|MccSic|<p>**MCC**: Merchant Category Code (4-digit), used for classifying a business by the type of goods/services it offers</p><p>**SIC**: Standard Industrial Organization code (4-digit), used for classifying industries </p><p>**MCC/SIC** </p>|
||FeeClass|Fee class of a card type|
||Misc1|Acquirer-defined merchant account miscellaneous information field 1|
||Misc2|Acquirer-defined merchant account miscellaneous information field 2|
||Last6MerchantNumber|Last 6 digits of a merchant number|

### Platform

|**Value**|**Description**|
| :- | :- |
||**All platform**|
|Omaha|Omaha processing platform |
|North|North (Cardnet) processing platform |
|Memphis|Memphis processing platform|

### ViewLevel

|**Value**|**Description**|
| :- | :- |
|Hierarchy|View Data by Hierarchy Entity|
|Merchant|View Data by Merchant|

### TransactionOperator

|**Value**|**Description**|
| :- | :- |
|EqualTo||
|Between||
|GreaterThan||
|LessThan||
|PlusMinus5|+/- 5$|


