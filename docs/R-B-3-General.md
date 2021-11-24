## GENERAL
1. ### HierarchyFilterMode Values Groups

|**1**|SubClient**,** Platform**,** MasterSaleAgent, CorporateName, MerchantName, MerchantNumber, Sys, SysPrin, SysPrinAgent, SalesAgent, HeadquarterMerchantNumber, Bank, Agent, Corp, NorthChain,  NorthSalesAgent, MasterChain, MemphisChain, SalesmanNo|
| :-: | :- |

### Parameters
1. HierarchyFilterMode

|**Name**|HierarchyFilterMode|
| :- | :- |
|**Type**|[HierarchyFilterMode](#_HierarchyFilterMode)|
|**Format**||
|**Description**|Filter mode selected by user|

1. HierarchyFilterValue

|**Name**|HierarchyFilterValue|
| :- | :- |
|**Type**|String|
|**Format**|Depend on [HierarchyFilterMode](#_HierarchyFilterMode) **[Ref**([II.1](#II_1))**]**|
|**Description**|Filter value entered/selected for the corresponding HierarchyFilterMode|

1. FromDate

|**Name**|FromDate|
| :- | :- |
|**Type**|DateTime|
|**Format**|<p>- <= ToDay</p><p>- <= [ToDate](#P_ToDate)</p>|
|**Description**|From date of date range picked by user|

1. ToDate

|**Name**|ToDate|
| :- | :- |
|**Type**|DateTime|
|**Format**|<p>- <= ToDay</p><p>- >= [FromDate](#P_FromDate)</p>|
|**Description**|To date of date range picked by user|

1. ViewLevel

|**Name**|ViewLevel|
| :- | :- |
|**Type**|[ViewLevel](#_ViewLevel)|
|**Format**||
|**Description**|The level at which data are being displayed|

1. PageSize

|**Name**|PageSize|
| :- | :- |
|**Type**|Int|
|**Format**|> 0|
|**Description**|Paging - Total number of data rows across all page numbers|

1. CurrentPageSize

|**Name**|CurrentPageSize|
| :- | :- |
|**Type**|Int|
|**Format**|>= 0|
|**Description**|Paging - The selected page number|

1. ReportDate

|**Name**|ReportDate|
| :- | :- |
|**Type**|DateTime|
|**Format**|<= ToDay|
|**Description**|The exactly selected date|

1. MerchantNumber

|**Name**|MerchantNumber|
| :- | :- |
|**Type**|String|
|**Format**|<p>- Only Numeric</p><p>- MaxLength = 16</p>|
|**Description**|The selected merchant number, only contain numeric and max length is 16|

1. BatchNumber

|**Name**|BatchNumber|
| :- | :- |
|**Type**|String|
|**Format**|<p>- Only Alphanumeric</p><p>- MaxLength = 20</p>|
|**Description**|The batch number of transaction|

1. TransactionId

|**Name**|TransactionId|
| :- | :- |
|**Type**|Guid|
|**Format**||
|**Description**|ID of a transaction|

1. AuthorizationNumber

|**Name**|AuthorizationNumber|
| :- | :- |
|**Type**|String|
|**Format**|<p>- Only Alphanumerics</p><p>- MaxLength = 16</p>|
|**Description**|The Authorization number of transaction|

1. First6CardNumber

|**Name**|First6CardNumber|
| :- | :- |
|**Type**|String|
|**Format**|<p>- Only numerics</p><p>- MinLength = 6</p><p>- MaxLength =6</p>|
|**Description**|The first 6 digits of card number|

1. Last4CardNumber

|**Name**|Last4CardNumber|
| :- | :- |
|**Type**|String|
|**Format**|<p>- Only numerics</p><p>- MinLength = 4</p><p>- MaxLength =4</p>|
|**Description**|The last 4 digits of card number|

1. TransactionOperator

|**Name**|TransactionOperator|
| :- | :- |
|**Type**|[TransactionOperator](#_TransactionOperator)|
|**Format**||
|**Description**|Operator for limit range of transaction amount|

1. TransactionAmountTo

|**Name**|TransactionAmountTo|
| :- | :- |
|**Type**|Decimal|
|**Format**||
|**Description**|The maximum transaction amount selected by user|

1. TransactionAmountFrom

|**Name**|TransactionAmountFrom|
| :- | :- |
|**Type**|Decimal|
|**Format**||
|**Description**|The minimum transaction amount selected by user|

1. VendorId

|**Name**|VendorId|
| :- | :- |
|**Type**|String|
|**Format**|<p>- All Characters Except</p><p>(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")</p><p>- MaxLength : 10</p>|
|**Description**|The vendor ID |

1. ProductCode

|**Name**|ProductCode|
| :- | :- |
|**Type**|String|
|**Format**|<p>- Only numerics</p><p>- MaxLength = 2</p>|
|**Description**||

1. CmsId

|**Name**|CmsId|
| :- | :- |
|**Type**|String|
|**Format**|<p>- Only numerics</p><p>- MaxLength = 7</p>|
|**Description**||

1. ServicesMerchantId

|**Name**|ServicesMerchantId|
| :- | :- |
|**Type**|String|
|**Format**|<p>- Only numerics</p><p>- MaxLength = 10</p>|
|**Description**||

1. EquipId

|**Name**|ServicesMerchantId|
| :- | :- |
|**Type**|String|
|**Format**|<p>- All Characters Except</p><p>(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")</p><p>- MaxLength : 8</p>|
|**Description**|ID of a  Equipment |

### Parameters Groups





|**Name**|**Default**|
| :-: | :-: |
|[HierarchyFilterMode](#P_HierarchyFilterMode)|Platform|
|[HierarchyFilterValue](#P_HierarchyFilterValue)||
|[FromDate](#P_FromDate)|ToDay – 1|
|[ToDate](#P_ToDate)|ToDay – 1|
|[ViewLevel](#P_ViewLevel)|Hierarchy|
|[PageSize](#P_PageSize)|100|
|[CurrentPageSize](#P_CurrentPageSize)|0|



|**Name**|**Default**|**Required**|
| :-: | :-: | :-: |
|[MerchantNumber](#P_MerchantNumber)||True|
|[FromDate](#P_FromDate)|ToDay – 1||
|[ToDate](#P_ToDate)|ToDay – 1||
|[PageSize](#P_PageSize)|100||
|[CurrentPageSize](#P_CurrentPageSize)|0||



|**Name**|**Default**|
| :-: | :-: |
|[HierarchyFilterMode](#P_HierarchyFilterMode)|Platform|
|[HierarchyFilterValue](#P_HierarchyFilterValue)||
|[PageSize](#P_PageSize)|100|
|[CurrentPageSize](#P_CurrentPageSize)|0|



|**Name**|**Default**|**Required**|
| :-: | :-: | :-: |
|[MerchantNumber](#P_MerchantNumber)||True|
|[PageSize](#P_PageSize)|100||
|[CurrentPageSize](#P_CurrentPageSize)|0||



|**Name**|**Required**|
| :-: | :-: |
|[MerchantNumber](#P_MerchantNumber)|True|



|**Name**|**Require**|
| :-: | :-: |
|[MerchantNumber](#P_MerchantNumbet)|True|
|[ProductCode](#P_ProductCode)|True|



|**Name**|**Require**|
| :-: | :-: |
|[MerchantNumber](#P_MerchantNumbet)|True|
|[EquipId](#P_EquipId)|True|

### Notes:


   - If [HierarchyFilterMode](#P_HierarchyFilterMode) = ‘MerchantNumber’ then result return despite value of [HierarchyFilterValue](#P_HierarchyFilterValue)





