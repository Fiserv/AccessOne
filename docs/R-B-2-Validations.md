## VALIDATIONS:
1. ### FORMAT OF HierarchyFilterValue

||**Value of HierarchyFilterMode**|**Format of HierarchyFilterValue**|**Min Length**|**Max Length**|
| :-: | :-: | :-: | :-: | :-: |
|**Common**|SubClient|All Characters Except (`~!@#$%^&\*()\_+=|[]{}:;'?/\\><,\")||10|
||Platform|**[Ref** ([I.2](#I_2))**]**|||
||MasterSaleAgent|<p>All Characters Except</p><p>(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")</p>||25|
||CorporateName|All Characters Except (£)|||
||MerchantName|All Characters Except (á)|||
||MerchantNumber|Only Numerics||16|
|**Omaha**|Sys|Only Numerics|||
||SysPrin|XXXX/XXXX **(X is numberic)**||9|
||SysPrinAgent|<p>XXXX/XXXX/XXXX</p><p>**OR**</p><p>XXXX/XXXX/XXXXXX **(X is numberic)**</p>||14|
||SalesAgent|<p>All Characters Except</p><p>(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")</p>||25|
||HeadquarterMerchantNumber|Only Numerics||16|
|**North**|Bank|Only Numerics||12|
||Agent|Only Numerics||12|
||Corp|Only Numerics||12|
||NorthChain|Only Numerics||12|
||NorthSalesAgent|<p>All Characters Except</p><p>(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")</p>||25|
|**Memphis**|MasterChain|<p>All Characters Except</p><p>(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")</p>||3|
||MemphisChain|<p>All Characters Except</p><p>(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")</p>||3|
||SalesmanNo|<p>All Characters Except</p><p>(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")</p>||25|
|**Others**|MccSic|<p>YYY, YYYY, … </p><p></p><p>- **YYY, YYYY is code.**</p><p>- **Length of code <= 4**</p>|||
||FeeClass|<p>XXX|YYYY </p><p></p><p>- **XXX is FeeClass Name**</p><p>` `**(**All Characters Except</p><p>(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")**)** </p><p>- **YYYY is FeeClass Filter Value (Length =  3 And Only Numerics)**</p>|||
||Misc1|<p>All Characters Except</p><p>(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")</p>||3|
||Misc2|<p>All Characters Except</p><p>(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")</p>||3|
||Last6MerchantNumber|Only Numerics|6|6|

**Note:**  if **HierarchyFilterValue** is not required then** system will return all records of **HierarchyFilterMode** 
### DateTime Format
ISO 8601** (YYYY-MM-DDThh:mm:ssTZD)

**Example**:

2014-07-16T19:20:30+07:00

2014-07-15T19:10:30

