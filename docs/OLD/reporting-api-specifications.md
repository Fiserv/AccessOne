

AccessOne Reporting API Specifications

AccessOne Reporting API Specifications

Page **1** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Table of Contents

A. Revision History .....................................................................................................................................8

B. Requirements ........................................................................................................................................9

I.

ENUMERATIONS..............................................................................................................................11

\1. HierarchyFilterMode...................................................................................................................11

\2. Platform ......................................................................................................................................12

\3. ViewLevel ....................................................................................................................................12

\4. TransactionOperator...................................................................................................................12

II. VALIDATIONS: .................................................................................................................................13

\1. FORMAT OF HierarchyFilterValue...............................................................................................13

\2. DateTime Format ........................................................................................................................14

III. GENERAL .........................................................................................................................................14

\1. HierarchyFilterMode Values Groups...........................................................................................14

\2. Parameters..................................................................................................................................14

\3. Parameters Groups .....................................................................................................................18

\4. Notes:..........................................................................................................................................19

C. REST Guide...........................................................................................................................................20

\1. Initiate REST Project Workspace.................................................................................................20

\2. Setup Security and Authentication, Method and Media Type ...................................................21

AccessOne Reporting API Specifications

Page **2** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\3. Get Token....................................................................................... **Error! Bookmark not defined.**

\4. Input Rest Request Body.............................................................................................................29

SERVICE OPERATIONS .....................................................................................................................33

\1. GetBatchSummaryByEntity.........................................................................................................33

\2. GetBatchSummaryByMerchant ..................................................................................................35

\3. GetBatchDetail............................................................................................................................36

\4. GetCardSummary........................................................................................................................37

\5. GetPaymentSummaryByEntity ...................................................................................................39

\6. GetPaymentSummaryByMerchant.............................................................................................40

\7. GetPaymentDetail.......................................................................................................................41

\8. GetReturnSummaryByEntity.......................................................................................................42

\9. GetReturnSummaryByMerchant ................................................................................................43

\10. GetChargebacksSummary...........................................................................................................44

\11. GetChargebacksDetail.................................................................................................................45

\12. GetRetrievalsSummary ...............................................................................................................47

\13. GetRetrievalsDetail .....................................................................................................................48

\14. GetVoidsRejectsSummary...........................................................................................................49

\15. GetVoidsRejectsDetail.................................................................................................................50

\16. GetVoucher.................................................................................................................................51

\17. GetTransactions ..........................................................................................................................52

\18. GetAuthorizationLogSummary ...................................................................................................54

D.

AccessOne Reporting API Specifications

Page **3** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\19. GetAuthorizationLogDetail .........................................................................................................55

\20. GetAuthorizationLogBuyPassSummary ......................................................................................56

\21. GetAuthorizationLogBuyPassDetail ............................................................................................57

\22. GetAuthorizationLogGGe4Summary ..........................................................................................59

\23. GetAuthorizationLogGGe4Detail ................................................................................................60

\24. GetAuthorizationLogNashvilleSummary.....................................................................................61

\25. GetAuthorizationLogNashvilleDetail...........................................................................................62

\26. GetAuthorizationLogNorthSummary..........................................................................................63

\27. GetAuthorizationLogNorthDetail................................................................................................64

\28. GetAuthorizationLogOmahaSummary........................................................................................66

\29. GetAuthorizationLogOmahaDetail..............................................................................................67

\30. GetAuthorizationVendorSummary .............................................................................................68

\31. GetAuthorizationVendorDetail ...................................................................................................69

\32. GetMerchantList .........................................................................................................................71

\33. GetMerchantComments .............................................................................................................72

\34. GetOmahaMerchantProfile ........................................................................................................73

\35. GetOmahaMerchantCardType....................................................................................................74

\36. GetOmahaMerchantCardTypePinDebit......................................................................................75

\37. GetOmahaMerchantCardInfomationPrivateLabel......................................................................76

\38. GetOmahaMerchantMemos.......................................................................................................77

\39. GetNorthMerchantProfile...........................................................................................................78

AccessOne Reporting API Specifications

Page **4** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\40. GetNorthMechantEntitlements..................................................................................................79

\41. GetNorthMerchantPricingInformation.......................................................................................80

\42. GetNorthMerchantEntitlementFull ............................................................................................81

\43. GetNorthMerchantEntitlementDetail.........................................................................................82

\44. GetMemphisMerchantProfile.....................................................................................................83

\45. GetMemphisMerchantCardInformation.....................................................................................84

\46. GetMemphisMerchantCardServicesInformation........................................................................85

\47. GetMemphisMerchantDebitNetworks .......................................................................................86

\48. GetMemphisMerchantAttributes ...............................................................................................87

\49. GetMemphisMerchantEquipments ............................................................................................88

\50. GetMemphisMerchantBuypassInformation...............................................................................89

\51. GetMemphisMerchantCardInformationDetail ...........................................................................90

\52. GetMemphisMerchantEquipmentSpecificExtra .........................................................................91

\53. GetMemphisMerchantEquipmentAttribute...............................................................................92

\54. GetOmahaMerchantStatementList.............................................................................................93

\55. GetOmahaMerchantStatement..................................................................................................94

\56. GetNonQualifyingTransactionSummaryByEntity........................................................................95

\57. GetNonQualifyingTransactionByMerchant.................................................................................96

\58. GetGGe4MerchantEnrollment....................................................................................................98

\59. GetGGe4MerchantEnrollmentByMerchant..............................................................................100

\60. GetReturnsReportByEntity........................................................................................................102

AccessOne Reporting API Specifications

Page **5** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\61. GetReturnsReportByMerchant .................................................................................................104

\62. GetCustomerNotPresentByEntity.............................................................................................106

\63. GetCustomerNotPresentByMerchant.......................................................................................107

\64. GetHVMerchantsCustomerPresentByEntity.............................................................................109

\65. GetHVMerchantsCustomerPresentByMerchant ......................................................................111

\66. GetAllOtherMCCMerchantsCustomerPresentByEntity ............................................................112

\67. GetAllOtherMCCMerchantsCustomerPresentByMerchant......................................................114

\68. GetMerchantAdjustmentSummaryByEntity.............................................................................116

\69. GetMerchantAdjustmentSummaryByMerchant.......................................................................118

\70. GetMerchantAdjustmentDetail ................................................................................................119

\71. GetChatHistorySummaryByEntity.............................................................................................121

\72. GetChatHistoryByMerchant......................................................................................................123

\73. GetEMVIndicatorReportByEntity..............................................................................................124

\74. GetEMVIndicatorReportByMerchant........................................................................................125

\75. GetTaxReportDailySubmittedSummaryByEntity ......................................................................127

\76. GetTaxReportDailySubmittedSummaryByMerchant................................................................129

\77. GetTaxReportDailySubmittedDetailByEntity ............................................................................130

\78. GetTaxReportDailySubmittedDetailByMerchant......................................................................132

\79. GetTaxReportMonthlyInvalidSummaryByEntity.......................................................................134

\80. GetTaxReportMonthlyInvalidSummaryByMerchant ................................................................136

\81. GetTaxReportMonthlyInvalidDetailByEntity.............................................................................137

AccessOne Reporting API Specifications

Page **6** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\82. GetTaxReportMonthlyInvalidDetailByMerchant ......................................................................139

\83. GetTaxReportAdhoc..................................................................................................................140

\84. GetMonetaryRejectsByEntity....................................................................................................143

\85. GetMonetaryRejectsByMerchant .............................................................................................145

\86. GetRejectETCFrontEndEditExceptionsByEntity.........................................................................146

\87. GetRejectETCFrontEndEditExceptionsByMerchant..................................................................149

\88. GetTapeTransmittalRejectsByEntity .........................................................................................151

\89. GetTapeTransmittalRejectsByMerchant...................................................................................154

AccessOne Reporting API Specifications

Page **7** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Basic Service Information**

**Service Name**

**ReportService**

**Service**

**Version**

1.0

**Service**

This service is used to get report information from Access One

**Description**

<https://api.fdportfoliomanager.com/pm/ReportService.svc>

<https://api.fdportfoliomanager.com/pm/ReportService.svc/rest>

**Prod**

Revision History

**#**

**Date**

**Reason for Change**

V2.0

V3.0

07/31/2017

08/08/2018 [TL] **Added following reports to Reporting API:**

Section 56 to section 89:

\1. Non-Qualifying Transactions.

\2. Payeezy Gateway

\3. Returns

\4. Fixed Acquirer Network Fee Reports.

\5. Merchant Adjustment

\6. Chat History

\7. EMV Indicator Report

\8. Tax Report

\9. Monetary Rejects

V4.0

V4.1

10/25/2018 [TL] Updated sample XMLs, parameters of all APIs from section D.56

to D.87.

Removed API for “Monetary Rejects” report.

11/13/2018 [TL] Added following APIs into D.84 and D.85

·

·

GetMonetaryRejectsByEntity

GetMonetaryRejectsByMerchant

V4.2

V5.0

12/12/2018 [TL] Added following API:

·

58.1 - GetGGe4MerchantEnrollmentByMerchant

10/17/2019 **[TL] Added following sections:**

·

C – REST Guide

AccessOne Reporting API Specifications

Page **8** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**#**

**Date**

**Reason for Change**

Added Rest API sample request, Rest API sample response for

·

89 APIs.

01/20/2020 [**\[TL\]**](https://lsuat-api.fdportfoliomanager.com/)[** ](https://lsuat-api.fdportfoliomanager.com/)[Correct**](https://lsuat-api.fdportfoliomanager.com/)[** ](https://lsuat-api.fdportfoliomanager.com/)[the**](https://lsuat-api.fdportfoliomanager.com/)[** ](https://lsuat-api.fdportfoliomanager.com/)[Endpoint:**](https://lsuat-api.fdportfoliomanager.com/)

[**https://lsuat-api.fdportfoliomanager.com/**](https://lsuat-api.fdportfoliomanager.com/)

V5.1

Requirements

This section specifies the detailed requirements for applying WS-Security Authentication using

Username Tokens with a Username and Password Digest. The OASIS standard is being utilized with [the](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)

[profile](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[of](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Web](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Services](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Security](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Username](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Token](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Profile](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Version](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[1.1.1](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[.](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)

The following request sample illustrates how the security information will be sent within SOAP Header.

Note that the SOAP body will vary depending on the specifics of the data communicated by Lonestar

pillars.

Request Message Sample

<?xml version="1.0" encoding="utf-8"?>

<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsse="http://docs.oasis-

open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd" xmlns:wsu="http://docs.oasis-

open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">

<soap:Header>

<wsa:Action>http://tempuri.org/HelloWorld</wsa:Action>

<wsa:MessageID>urn:uuid:ebc4c587-52b8-4867-a47b-c0ddc750fc10</wsa:MessageID>

<wsa:ReplyTo>

<wsa:Address>http://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:Add

ress>

</wsa:ReplyTo>

<wsa:To>http://localhost:60286/TestWS/Service.asmx</wsa:To>

<wsse:Security soap:mustUnderstand="1">

<wsu:Timestamp wsu:Id="Timestamp-55bec23e-030a-461b-9474-

bc182879bb63">

<wsu:Created>2014-11-27T04:49:32Z</wsu:Created>

<wsu:Expires>2014-11-27T04:54:32Z</wsu:Expires>

</wsu:Timestamp>

<wsse:UsernameToken xmlns:wsu="http://docs.oasis-

open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" wsu:Id="SecurityToken-95440d2c-

3046-4aab-9ed3-d836966fb611">

<wsse:Username>api\_user</wsse:Username>

AccessOne Reporting API Specifications

Page **9** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<wsse:Password Type="http://docs.oasis-open.org/wss/2004/01/oasis-

200401-wss-username-token-profile-

1.0#PasswordDigest">Z9DtKSZJ1N4hfi0blPNd6wNxIx4=</wsse:Password>

<wsse:Nonce>P02bHRPDX85BAwsOeresGw==</wsse:Nonce>

<wsu:Created>2014-11-27T04:49:32Z</wsu:Created>

</wsse:UsernameToken>

</wsse:Security>

</soap:Header>

<soap:Body>

<!-- SOAP Body Data -->

</soap:Body>

</soap:Envelope>

The following namespaces are used: **http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-**

**wssecurity-utility-1.0.xsd** and **http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-**

**secext-1.0.xsd** which are represented below by the prefixes “**wsu**” and “**wsse**” respectively.

The entry-point to WS-Security is a SOAP Header element called <wsse:Security>. It contains the

security-related data and information. Within <wsse:Security>, the following elements are required

(Note that the order of the elements below is fixed for security purposes):

<wsu:Timestamp>: It is used to express the creation and expiration time of the message. To address

replay attacks, the message timestamps are required:

\-

\-

<wsu:Created>: the creation time of the message.

<wsu:Expires>: the expiration time of the message.

<wsse:UsernameToken>: the Username, PasswordDigest and the security-related information to

authenticate the identity will be provided within this element:

\-

\-

<wsse:Username>: the clear text username.

<wsse:Password>: it holds the digested password which is constructed as follows:

PasswordDigest = Base64( SHA-1( nonce + created + password-token) )

That is, concatenate the nonce, creation timestamp, and the password-token, digest the

combination using SHA-1 hash algorithm, then include the Base64 coding of that result as the

password.

Note that depending on the specifics of the API, there would be a single username/password-

token to consume the service or multiple usernames/password-tokens based on the AccessOne

User Setup.

AccessOne Reporting API Specifications

Page **10** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\-

\-

<wsse:Nonce>: a cryptographically random value. Each message must include a new nonce

value to detect replay attacks.

<wsu:Created>: the creation time of the message.

ENUMERATIONS

HierarchyFilterMode

**Value**

**Description**

AO user created and managed by ISO client

Each sub client is responsible for managing a group

of merchants – this is set up by ISO client

Payment processing platform (Omaha, North,

Memphis)

SubClient

Platform

AO user created and managed by ISO client

Each master sales agent in turn manages a group of

sales agent assigned to them by ISO client

Normalized corporate name

Normalized merchant name

Merchant Number

MasterSaleAgent

CorporateName

MerchantName

MerchantNumber

System number. It defines the first level of

processing and the second level of reporting after

ISO-Client. Prins are assigned to Sys

Principal number, used as a level of reporting and

processing in FDS. Agents are assigned to Prins

Agent is a means of grouping merchants with the

same Prin together for risk monitoring purposes.

“Agent” is used by First Data to group retail

merchants together in buckets like MOTO, e-

Commerce, etc.

Sys

SysPrin

SysPrinAgent

SalesAgent

Omaha sales agent

Merchant number of head merchant of a chain. A

group of merchants owned by the same person or

people is called chain. The head merchant of a

chain is called headquarter merchant.

Bank number. (North) agents are assigned to banks

(North) Agent number. CORPs are assigned to

agents

HeadquarterMerchantNumber

Bank

Agent

Corp

Corporate number. Grouping of merchants

A group of merchants owned by the same person or

people, i.e. North’s counterpart to Omaha’s chain

North sales agent

Master chain, used as a level of reporting for

Memphis platform. A group of merchants owned

NorthChain

NorthSalesAgent

MasterChain

AccessOne Reporting API Specifications

Page **11** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





by the same person or people is called chain.

Master chain is a group of (Memphis) chains. Chains

are assigned to master chains

MemphisChain

SalesmanNo

Memphis’s counterpart to Omaha’s chain.

Memphis’ counterpart to North’s sales agent

**MCC**: Merchant Category Code (4-digit), used for

classifying a business by the type of goods/services

it offers

MccSic

**SIC**: Standard Industrial Organization code (4-digit),

used for classifying industries

**MCC/SIC**

FeeClass

Misc1

Fee class of a card type

Acquirer-defined merchant account miscellaneous

information field 1

Acquirer-defined merchant account miscellaneous

information field 2

Misc2

Last6MerchantNumber

Last 6 digits of a merchant number

Platform

**Value**

**Description**

**All platform**

Omaha

North

Memphis

Omaha processing platform

North (Cardnet) processing platform

Memphis processing platform

ViewLevel

**Value**

**Description**

Hierarchy

Merchant

View Data by Hierarchy Entity

View Data by Merchant

TransactionOperator

**Value**

**Description**

EqualTo

Between

GreaterThan

LessThan

PlusMinus5

+/- 5$

AccessOne Reporting API Specifications

Page **12** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





VALIDATIONS:

\1. FORMAT OF HierarchyFilterValue

**Min**

**Max**

**Value of HierarchyFilterMode**

**Format of HierarchyFilterValue**

**Length Length**

All Characters Except

(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><,\")

**[Ref [**(](#br12)[I.2](#br12)[)](#br12)]**

10

SubClient

Platform

All Characters Except

(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")

All Characters Except (£)

All Characters Except (á)

Only Numerics

25

16

MasterSaleAgent

CorporateName

MerchantName

MerchantNumber

Sys

Only Numerics

SysPrin

XXXX/XXXX **(X is numberic)**

9

XXXX/XXXX/XXXX

**OR**

14

SysPrinAgent

XXXX/XXXX/XXXXXX **(X is numberic)**

All Characters Except

(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")

25

SalesAgent

HeadquarterMerchantNumber Only Numerics

16

12

12

12

12

25

Bank

Only Numerics

Agent

Only Numerics

Corp

Only Numerics

NorthChain

Only Numerics

All Characters Except

(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")

All Characters Except

(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")

All Characters Except

(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")

All Characters Except

(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")

YYY, YYYY, …

NorthSalesAgent

MasterChain

3

3

MemphisChain

SalesmanNo

25

MccSic

\-

\-

**YYY, YYYY is code.**

**Length of code <= 4**

XXX|YYYY

FeeClass

\-

**XXX is FeeClass Name**

**(**All Characters Except

(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")**)**

AccessOne Reporting API Specifications

Page **13** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\-

**YYYY is FeeClass Filter Value**

**(Length = 3 And Only**

**Numerics)**

All Characters Except

(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")

All Characters Except

(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")

Only Numerics

3

3

6

Misc1

Misc2

Last6MerchantNumber

6

**Note:** if **HierarchyFilterValue** is not required then system will return all records of **HierarchyFilterMode**

DateTime Format

ISO 8601 (YYYY-MM-DDThh:mm:ssTZD)

**Example**:

2014-07-16T19:20:30+07:00

2014-07-15T19:10:30

GENERAL

\1. HierarchyFilterMode Values Groups

SubClient**,** Platform**,** MasterSaleAgent, CorporateName, MerchantName,

MerchantNumber, Sys, SysPrin, SysPrinAgent, SalesAgent,

HeadquarterMerchantNumber, Bank, Agent, Corp, NorthChain,

NorthSalesAgent, MasterChain, MemphisChain, SalesmanNo

**1**

Parameters

1.1.HierarchyFilterMode

**Name**

**Type**

HierarchyFilterMode

[HierarchyFilterMode](#br11)

**Format**

**Description**

Filter mode selected by user

1.2.HierarchyFilterValue

**Name**

HierarchyFilterValue

**Type**

String

**Format**

**Description**

Depend on [HierarchyFilterMode](#br11)[ ](#br11)**[Ref[**(](#br13)[II.1](#br13)[)](#br13)]**

Filter value entered/selected for the

corresponding HierarchyFilterMode

1.3.FromDate

AccessOne Reporting API Specifications

Page **14** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Name**

**Type**

FromDate

DateTime

**Format**

\-

\-

<= ToDay

[<=](#br15)[ ](#br15)[ToDate](#br15)

**Description**

From date of date range picked by user

1.4.ToDate

**Name**

**Type**

ToDate

DateTime

**Format**

\-

\-

<= ToDay

[>=](#br14)[ ](#br14)[FromDate](#br14)

**Description**

To date of date range picked by user

1.5.ViewLevel

**Name**

ViewLevel

[ViewLevel](#br12)

**Type**

**Format**

**Description**

The level at which data are being displayed

1.6.PageSize

**Name**

PageSize

**Type**

Int

**Format**

\> 0

**Description**

Paging - Total number of data rows across all

page numbers

1.7.CurrentPageSize

**Name**

CurrentPageSize

**Type**

Int

**Format**

\>= 0

**Description**

Paging - The selected page number

1.8.ReportDate

**Name**

ReportDate

**Type**

DateTime

**Format**

<= ToDay

**Description**

The exactly selected date

1.9.MerchantNumber

**Name**

**Type**

MerchantNumber

String

**Format**

\-

Only Numeric

AccessOne Reporting API Specifications

Page **15** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\-

MaxLength = 16

**Description**

The selected merchant number, only contain

numeric and max length is 16

1.10.

BatchNumber

**Name**

**Type**

BatchNumber

String

**Format**

\-

\-

Only Alphanumeric

MaxLength = 20

**Description**

The batch number of transaction

1.11.

1.12.

TransactionId

**Name**

**Type**

TransactionId

Guid

**Format**

**Description**

ID of a transaction

AuthorizationNumber

**Name**

**Type**

AuthorizationNumber

String

**Format**

\-

\-

Only Alphanumerics

MaxLength = 16

**Description**

The Authorization number of transaction

1.13.

1.14.

1.15.

First6CardNumber

**Name**

**Type**

First6CardNumber

String

**Format**

\-

\-

\-

Only numerics

MinLength = 6

MaxLength =6

**Description**

The first 6 digits of card number

Last4CardNumber

**Name**

**Type**

Last4CardNumber

String

**Format**

\-

\-

\-

Only numerics

MinLength = 4

MaxLength =4

**Description**

The last 4 digits of card number

TransactionOperator

**Name**

TransactionOperator

AccessOne Reporting API Specifications

Page **16** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Type**

[TransactionOperator](#br12)

**Format**

**Description**

Operator for limit range of transaction amount

1.16.

1.17.

1.18.

TransactionAmountTo

**Name**

**Type**

TransactionAmountTo

Decimal

**Format**

**Description**

The maximum transaction amount selected by

user

TransactionAmountFrom

**Name**

**Type**

TransactionAmountFrom

Decimal

**Format**

**Description**

The minimum transaction amount selected by

user

VendorId

**Name**

**Type**

VendorId

String

**Format**

\-

All Characters Except

(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")

\-

MaxLength : 10

**Description**

The vendor ID

1.19.

1.20.

1.21.

ProductCode

**Name**

**Type**

ProductCode

String

**Format**

\-

\-

Only numerics

MaxLength = 2

**Description**

CmsId

**Name**

CmsId

String

\-

**Type**

**Format**

Only numerics

MaxLength = 7

\-

**Description**

ServicesMerchantId

**Name**

ServicesMerchantId

AccessOne Reporting API Specifications

Page **17** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Type**

String

**Format**

\-

\-

Only numerics

MaxLength = 10

**Description**

1.22.

EquipId

**Name**

**Type**

ServicesMerchantId

String

**Format**

\-

All Characters Except

(`~!@#$%^&\*()\_+=|[]{}:;'?/\\><.,-\")

MaxLength : 8

\-

**Description**

ID of a Equipment

Parameters Groups

3.1.

**Name**

**Default**

Platform

[HierarchyFilterMode](#br14)

[HierarchyFilterValue](#br14)

[FromDate](#br14)

[ToDate](#br15)

[ViewLevel](#br15)

[PageSize](#br15)

ToDay – 1

ToDay – 1

Hierarchy

100

[CurrentPageSize](#br15)

0

3.2.

**Name**

**Default**

**Required**

MerchantNumber

[FromDate](#br14)

[ToDate](#br15)

True

ToDay – 1

ToDay – 1

100

[PageSize](#br15)

[CurrentPageSize](#br15)

0

3.3.

**Name**

**Default**

[HierarchyFilterMode](#br14)

[HierarchyFilterValue](#br14)

[PageSize](#br15)

Platform

100

0

[CurrentPageSize](#br15)

AccessOne Reporting API Specifications

Page **18** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





3.4.

**Name**

**Default**

100

**Required**

MerchantNumber

[PageSize](#br15)

True

[CurrentPageSize](#br15)

0

3.5.

**Name**

**Name**

**Required**

MerchantNumber

True

3.6.

**Require**

True

True

[MerchantNumber](#br15)

[ProductCode](#br17)

3.7.

**Name**

**Require**

True

[MerchantNumber](#br15)

[EquipId](#br18)

True

Notes:

4.1.

\-

[If](#br14)[ ](#br14)[HierarchyFilterMode](#br14)[ ](#br14)= ‘MerchantNumber’ then result return despite value of

[HierarchyFilterValue](#br14)

AccessOne Reporting API Specifications

Page **19** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





REST Guide

This section provides the guidance to setup a Rest API request using SOAP UI.

\1. Initiate REST Project Workspace

There are three ways to open REST Project workspace:

·

Click on

icon on SoapUI Toolbar

·

·

Select File > New REST Project on SoapUI Toolbar

Hit Ctrl + Alt + N

A new window will prompt for entering URI.

Initial URI:

[**https://api.fdportfoliomanager.com/pm](https://api.fdportfoliomanager.com/)**/ReportService.svc/[APIName]**

**[APIName]** can be **API Name of the reporting**.

Click OK

·

In a few seconds or less the newly created REST project will be loaded with all the presentable

components of the North Boarding API.

AccessOne Reporting API Specifications

Page **20** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





·

A successful load will be indicated by no error and the web service’s components are displayed on the

Navigator panel. An example is shown in the following screenshot:

Setup Security and Authentication, Method and Media Type

In the initial new request window, setup following parameters with their corresponding values:

\- **Method**: POST

\- **Endpoint[**:](https://api.fdportfoliomanager.com/pm/ReportService.svc)[ ](https://api.fdportfoliomanager.com/pm/ReportService.svc)<https://api.fdportfoliomanager.com/pm/ReportService.svc>**

\- **Resource[**:](file://///dps2012/rest/GetGGe4MerchantEnrollment)[ ](file://///dps2012/rest/GetGGe4MerchantEnrollment)[/rest/APIName](file://///dps2012/rest/GetGGe4MerchantEnrollment)[,](file://///dps2012/rest/GetGGe4MerchantEnrollment)[ ](file://///dps2012/rest/GetGGe4MerchantEnrollment)[Fo](file://///dps2012/rest/GetGGe4MerchantEnrollment)**r example: [/rest/GetGGe4MerchantEnrollment](file://///dps2012/rest/GetGGe4MerchantEnrollment)

\*\*\*Note: Depending on which Reporting API, the APIName in the **Resource** link can be changed. Refer

to section [D](#br33)[ ](#br33)[–](#br33)[ ](#br33)[SERVICE](#br33)[ ](#br33)[OPERATIONS](#br33)[ ](#br33)to get the APIName.

For exampl[e,](file://///dps2012/rest/GetGGe4MerchantEnrollment)[ ](file://///dps2012/rest/GetGGe4MerchantEnrollment)[/rest/GetGGe4MerchantEnrollment](file://///dps2012/rest/GetGGe4MerchantEnrollment)[ ](file://///dps2012/rest/GetGGe4MerchantEnrollment)is used to get API for API

GetGGe4MerchantEnrollment. If the user wants to get API for GetPaymentDetail, the Resource link

should [be](file://///dps2012/rest/GetGGe4MerchantEnrollment)[ ](file://///dps2012/rest/GetGGe4MerchantEnrollment)[/rest/GetPaymentDetail](file://///dps2012/rest/GetGGe4MerchantEnrollment)[ ](file://///dps2012/rest/GetGGe4MerchantEnrollment).

\- **Parameters**: Blank

\- **Media Type**: application/xml

AccessOne Reporting API Specifications

Page **21** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





User and Token are always required for REST request.

Click on **Headers** tab and icon to add user and token parameters then input their value in **Value** column.

·

·

**user**: plain text, provided by Fiserv

**token**: encrypted API password based on SHA-256 standard.

AccessOne Reporting API Specifications

Page **22** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





At Headers tab, click on (**+**) button to add **user** and **token**.

**Add user to Header**:

AccessOne Reporting API Specifications

Page **23** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Input Value for Header user**. This Value is UserName which is used to access to AccessOne system.

AccessOne Reporting API Specifications

Page **24** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Add **token** to Header:

AccessOne Reporting API Specifications

Page **25** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Input Value for Header token**. Refer to step 3 – Generate Token below.

**Generate Token**

Get the **AccessOne API Password** (this is different from your AccessOne login password):

AccessOne Reporting API Specifications

Page **26** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





In Notepad++, go to Tools > SHA-256 > Generate:

Enter your API password which will generate the SHA-256 token:

AccessOne Reporting API Specifications

Page **27** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Copy this generated Token and input to the Value for Token Header at step 2.

AccessOne Reporting API Specifications

Page **28** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Input Rest Request Body

Input XML Request into the highlighted text box below.

AccessOne Reporting API Specifications

Page **29** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Each APIs in this document provides the Request Body Sample so that the user can copy them to paste

to the XML Request.

This is example to get report for GetGGe4MerchantEnrollment API, so in this text box, input the XML

Request fo[r](#br98)[ ](#br98)[GetGGe4MerchantEnrollment](#br98)[ ](#br98)API which was provided in section **E.55 –**

**GetGGe4MerchantEnrollment**.

AccessOne Reporting API Specifications

Page **30** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Then click

button to run the request.

AccessOne Reporting API Specifications

Page **31** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





The REST API Response will be shown in the right panel.

AccessOne Reporting API Specifications

Page **32** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





SERVICE OPERATIONS

\1. **GetBatchSummaryByEntity**

exec spa\_64\_ms\_LoneStar\_GetBatchHistory

@PlatformID=1,@SiteID=1000,@DDSClient=64,@UserID='Capital',@UserIDMode='Client',@HierarchyFil

terMode=N'PLATFORM',@HierarchyFilterValue=N'',@DateFilterMode=3,@BeginDate='2018-09-01

00:00:00',@EndDate='2018-09-07

00:00:00',@SubClientDrilldown=N'',@ClientDrilldown=N'',@IsMerchantList=0,@IsPaging=1,@IsCountPa

geTotal=0,@PageNo=1,@PageSize=10,@stOrder='ENTITYNAME DESC',@stFilter=''

go

exec spa\_64\_ms\_LoneStar\_GetBatchHistory\_Total

@PlatformID=1,@SiteID=1000,@DDSClient=64,@UserID='Capital',@UserIDMode='Client',@HierarchyFil

terMode=N'PLATFORM',@HierarchyFilterValue=N'',@DateFilterMode=3,@BeginDate='2018-09-01

00:00:00',@EndDate='2018-09-07

00:00:00',@SubClientDrilldown=N'',@ClientDrilldown=N'',@IsMerchantList=0,@stFilter=''

AccessOne Reporting API Specifications

Page **33** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





go

**Service Operation GetBatchSummaryByEntity()**

GetBatchSummaryByEntity

**Name**

Return batch summary data of hierarchy entity choice(s) based on the selected date

range

**Description**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

\+ **Contraints**:

**Pre-**

**conditions**

\-

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return Batch Hierarchy Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetBatchSummaryByEntityRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetBatchSummaryByEntityResponse.xml

**REST API**

**Request URL** /rest/GetBatchSummaryByEntity

**Method**

POST

**Request**

**Body Sample**

**XML**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

AccessOne Reporting API Specifications

Page **34** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<HierarchyFilterValue>512888888888051</HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-10-23T00:00:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetBatchSummaryByEntity\_RestResponse.xml

\2. GetBatchSummaryByMerchant

**Service Operation GetBatchSummaryByMerchant** ()

**Name**

GetBatchSummaryByMerchant

**Description**

Return batch summary data of the selected merchant number

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18)[**)\]**](#br18)**

**conditions**

**Post-**

Return Batch Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetBatchSummaryB

yMerchant\_SOAP\_Re

**Message**

**Exchange**

**Pattern**

**SAMPLE RESPONSE:**

GetBatchSummaryB

yMerchant\_SOAP\_Re

**REST API**

**Request URL** /rest/GetBatchSummaryByMerchant

**Method** POST

AccessOne Reporting API Specifications

Page **35** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Request**

**Body Sample**

**XML**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

<ToDate>2019-05-01T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetBatchSummaryByMerchant\_RestResponse.xml

\3. GetBatchDetail

**Service Operation GetBatchDetail** ()

**Name**

GetBatchDetail

**Description**

Return transaction-details data of a selected batch number

\+ **Parameters:**

**Name**

[BatchNumber](#br16)

[ReportDate](#br15)

[MerchantNumber](#br15)

[PageSize](#br15)

[CurrentPageIndex](#br15)

**Default**

**Require**

True

True

**Pre-**

**conditions**

ToDay – 1

100

0

Return Batch Detail

**Post-**

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

**Message**

**Exchange**

**Pattern**

GetBatchDetailRequest.xml

**See RESPONSE ATTACHED:**

AccessOne Reporting API Specifications

Page **36** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





GetBatchDetailResponse.xml

**REST API**

**Request URL** /rest/GetBatchDetail

**Method**

POST

**Request**

**Body Sample**

**XML**

<BatchDetailFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>02550630018</MerchantNumber>

<ReportDate>2019-10-13</ReportDate>

<CurrentPageIndex>1</CurrentPageIndex>

<PageSize>10</PageSize>

<BatchNumber>24421001</BatchNumber>

</BatchDetailFilter>

**Request**

**Response**

**Sample XML**

GetBatchDetail\_RestResponse.xml

\4. GetCardSummary

**Service Operation GetCardSummary ()**

**Name**

GetCardSummary

**Description**

Return card summary data based on selected date range

\+ **Parameters:**

**Name**

[HierarchyFilterMode](#br14)

**Default**

Platform

[HierarchyFilterValue](#br14)

[FromDate](#br14)

[ToDate](#br15)

**Pre-**

**conditions**

ToDay – 1

ToDay – 1

100

[PageSize](#br15)

[CurrentPageIndex](#br15)

[BatchNumber](#br16)

0

AccessOne Reporting API Specifications

Page **37** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\+ **Contraints**:

\-

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return Card Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetCardSummaryRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetCardSummaryResponse.xml

**REST API**

**Request URL** /rest/GetCardSummary

**Method**

POST

**Request**

**Body Sample**

**XML**

<CardSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue>02550630018</HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-10-23T00:00:00</ToDate>

<BatchNumber>24421001</BatchNumber>

</CardSummaryFilter>

**Request**

**Response**

**Sample XML**

GetCardSummary\_RestResponse.xml

AccessOne Reporting API Specifications

Page **38** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\5. GetPaymentSummaryByEntity

**Service Operation GetPaymentSummaryByEntity ()**

**Name**

GetPaymentSummaryByEntity

**Description**

Return payment data of the entity choices based on the selected date range

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

\+ **Contraints**:

**Pre-**

**conditions**

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return Deposit Hierarchy Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetPaymentSummaryByEntityRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetPaymentSummaryByEntityResponse.xml

**REST API**

**Request URL** /rest/GetPaymentSummaryByEntity

**Method**

POST

**Request**

**Body Sample**

**XML**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue>512888888888051</HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-10-23T00:00:00</ToDate>

<ViewLevel>None</ViewLevel>

AccessOne Reporting API Specifications

Page **39** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetPaymentSummaryByEntity\_RestResponse.xml

\6. GetPaymentSummaryByMerchant

**Service Operation GetPaymentSummaryByMerchant**()

**Name**

GetPaymentSummaryByMerchant

Return payment data of selected merchant number

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**Description**

**Pre-**

**conditions**

**Post-**

Return Deposit Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetPaymentSummaryByMerchantRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetPaymentSummaryByMerchantResponse.xml

**REST API**

**Request URL** /rest/GetPaymentSummaryByMerchant

**Method**

POST

**Request**

**Body Sample**

**XML**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

AccessOne Reporting API Specifications

Page **40** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

<ToDate>2019-10-23T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetPaymentSummaryByMerchant\_RestResponse.xml

\7. GetPaymentDetail

**Service Operation GetPaymentDetail()**

**Name**

GetPaymentDetail

**Description**

Return detailed payment data of the selected merchant number

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return Deposit Detail

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetPaymentDetailRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetPaymentDetailResponse.xml

**REST API**

**Request URL** /rest/GetPaymentDetail

AccessOne Reporting API Specifications

Page **41** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Method**

POST

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetPaymentDetail\_RestResponse.xml

\8. GetReturnSummaryByEntity

**Service Operation GetReturnSummaryByEntity ()**

**Name**

GetReturnSummaryByEntity

**Description**

Get summarized return data and sale data of the selected hierarchy entity choices

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

\+ **Contraints**:

**Pre-**

**conditions**

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return Return Hierarchy Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

**Message**

**Exchange**

**Pattern**

GetReturnSummaryByEntityRequest.xml

**See RESPONSE ATTACHED:**

AccessOne Reporting API Specifications

Page **42** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





GetReturnSummaryByEntityResponse.xml

**REST API**

**Request URL** /rest/GetReturnSummaryByEntity

**Method**

POST

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue>512888888888051</HierarchyFilterValue>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetReturnSummaryByEntity\_RestResponse.xml

\9. GetReturnSummaryByMerchant

**Service Operation GetReturnSummaryByMerchant ()**

**Name**

GetReturnSummaryByMerchant

Get detailed data of return transactions of the selected merchant number based on the

selected range

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return Return Summary

**conditions**

**SOAP API**

AccessOne Reporting API Specifications

Page **43** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**SAMPLE REQUEST:**

GetReturnSummaryByMerchantRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetReturnSummaryByMerchantResponse.xml

**REST API**

**Request URL** /rest/GetReturnSummaryByMerchant

**Method**

POST

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetReturnSummaryByMerchant\_RestRespone.xml

\10. GetChargebacksSummary

**Service Operation GetChargebacksSummary ()**

**Name**

GetChargebacksSummary

**Description**

Return chargeback data at summary level based on the selected date range

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**Pre-**

**conditions**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

AccessOne Reporting API Specifications

Page **44** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\+ **Notes**: **[Re[f(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return Chargeback Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetChargebacksSummaryRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetChargebacksSummaryResponse.xml

**REST API**

**Request URL** /rest/GetChargebacksSummary

**Method**

POST

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2008-01-01T00:00:00</FromDate>

<HierarchyFilterMode>SubClient</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetChargebacksSummary\_RestResponse.xml

\11. GetChargebacksDetail

**Service Operation GetChargebacksDetail()**

AccessOne Reporting API Specifications

Page **45** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Name**

GetChargebacksDetail

Return detailed data of chargeback transactions of a specific merchant number, based

on the selected date range

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return Chargeback Detail

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetChargebacksDetailRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetChargebacksDetailResponse.xml

**REST API**

**Request URL** /rest/GetChargebacksDetail

**Method**

POST

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetChargebacksDetail\_RestResponse.xml

AccessOne Reporting API Specifications

Page **46** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\12. GetRetrievalsSummary

**Service Operation GetRetrievalsSummary ()**

**Name**

GetRetrievalsSummary

**Description**

Return summarized retrieval data based on the selected date range

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18))]**

\+ **Contraints**:

**Pre-**

**conditions**

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return Retrievals Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

BatchSummaryRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

BatchSummaryResponse.xml

**REST API**

**Request URL** /rest/GetRetrievalsSummary

**Method**

POST

**Request**

**Body Sample**

**XML**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2008-01-01T00:00:00</FromDate>

<HierarchyFilterMode>SubClient</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-10-23T00:00:00</ToDate>

AccessOne Reporting API Specifications

Page **47** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetRetrievalsSummary\_RestResponse.xml

\13. GetRetrievalsDetail

**Service Operation GetRetrievalsDetail ()**

GetRetrievalsDetail

**Name**

Return detailed data of retrieval transactions of a specific merchant number, based on

the selected date range

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return Retrievals Detail

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetRetrievalsDetailRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetRetrievalsDetailResponse.xml

**REST API**

**Request URL** /rest/GetRetrievalsDetail

**Method** POST

AccessOne Reporting API Specifications

Page **48** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetRetrievalsDetail\_RestResponse.xml

\14. GetVoidsRejectsSummary

**Service Operation GetVoidsRejectsSummary()**

**Name**

GetVoidsRejectsSummary

**Description**

Return summarized data of voids/rejects transactions based on the selected date range

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

\+ **Contraints**:

**Pre-**

**conditions**

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return Voids Rejects Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetVoidsRejectsSummaryRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetVoidsRejectsSummaryResponse.xml

AccessOne Reporting API Specifications

Page **49** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**REST API**

**Request URL** /rest/GetVoidsRejectsSummary

**Method**

POST

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2008-01-01T00:00:00</FromDate>

<HierarchyFilterMode>SubClient</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetVoidsRejectsSummary\_RestResponse.xml

\15. GetVoidsRejectsDetail

**Service Operation GetVoidsRejectsDetail ()**

GetVoidsRejectsDetail

**Name**

Return detailed data of voids/rejects transactions of a specific merchant number, based

on the selected date range

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return Voids Rejects Detail

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

**Message**

**Exchange**

**Pattern**

GetVoidsRejectsDetailRequest.xml

AccessOne Reporting API Specifications

Page **50** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**See RESPONSE ATTACHED:**

GetVoidsRejectsDetailResponse.xml

**REST API**

**Request URL** /rest/GetVoidsRejectsDetail

**Method**

POST

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetVoidsRejectsDetail\_RestResponse.xml

\16. GetVoucher

**Service Operation GetVoucher ()**

**Name**

GetVoucher

**Description**

Return voucher details of the selected transaction

\+ **Parameters:**

**Name**

[MerchantNumber](#br15)

[ReportDate](#br15)

**Default**

**Require**

True

**Pre-**

**conditions**

ToDay - 1

[TransactionId](#br16)

True

**Post-**

Return Voucher

**conditions**

**SOAP API**

AccessOne Reporting API Specifications

Page **51** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**SAMPLE REQUEST:**

GetVoucherRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetVoucherResponse.xml

**REST API**

**Request URL** /rest/GetVoucher

**Method**

POST

<VoucherFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>512888888888051</MerchantNumber>

<ReportDate>2016-01-01T00:00:00</ReportDate>

<TransactionId>CE50BE3E-73B3-4132-98DB-C23D65E408D1</TransactionId>

</VoucherFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetVoucher\_RestResponse.xml

\17. GetTransactions

**Service Operation GetTransactions ()**

**Name**

GetTransactions

**Description**

Return a list of detailed transactions data based on the selected criteria

\+ **Parameters:**

Name

[HierarchyFilterMode](#br14)

[HierarchyFilterValue](#br14)

[FromDate](#br14)

**Default**

MerchantNumber

**Pre-**

**conditions**

ToDay – 1

ToDay – 1

[ToDate](#br15)

[AuthorizationNumber](#br16)

AccessOne Reporting API Specifications

Page **52** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





[First6CardNumber](#br16)

[Last4CardNumber](#br16)

[TransactionAmountFrom](#br17)

[TransactionAmountTo](#br17)

[TransactionOperator](#br16)

[PageSize](#br15)

100

0

[CurrentPageIndex](#br15)

\+ **Contraints**:

\-

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group (MasterSaleAgent,

CorporateName, MerchantName, MerchantNumber, Last6MerchantNumber,

Sys, SysPrin, SysPrinAgent, SalesAgent, HeadquarterMerchantNumber, Bank,

Agent, Corp, NorthChain, NorthSalesAgent, MasterChain, MemphisChain,

SalesmanNo)

**Post-**

Return Transaction List

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetTransactionsRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetTransactionsResponse.xml

**REST API**

**Request URL** /rest/GetTransactions

**Method**

POST

<TransactionSearchFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-01T00:00:00</FromDate>

<HierarchyFilterMode>Sys</HierarchyFilterMode>

**Request**

**Body Sample**

**XML**

AccessOne Reporting API Specifications

Page **53** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<HierarchyFilterValue>8740</HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-05-01T00:00:00</ToDate>

<AuthorizationNumber></AuthorizationNumber>

<First6CardNumber></First6CardNumber>

<Last4CardNumber></Last4CardNumber>

<TransactionAmountFrom>12</TransactionAmountFrom>

<TransactionAmountTo>0</TransactionAmountTo>

<TransactionOperator>GreaterThan</TransactionOperator>

</TransactionSearchFilter>

**Request**

**Response**

**Sample XML**

GetTransactions\_RestResponse.xml

\18. GetAuthorizationLogSummary

**Service Operation GetAuthorizationLogSummary ()**

**Name**

GetAuthorizationLogSummary

**Description**

Return summarized data of authorization transactions based on the selected criteria

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

\+ **Contraints**:

**Pre-**

**conditions**

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[Re[f(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return AuthorizationLog Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

**Message**

**Exchange**

**Pattern**

GetAuthorizationLogSummaryRequest.xml

**See RESPONSE ATTACHED:**

AccessOne Reporting API Specifications

Page **54** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





GetAuthorizationLogSummaryResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationLogSummary

**Method**

POST

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue>512888888888051</HierarchyFilterValue>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationLogSummary\_RestResponse.xml

\19. GetAuthorizationLogDetail

**Service Operation GetAuthorizationLogDetail ()**

**Name**

GetAuthorizationLogDetail

Return detailed data of authorization transactions for a specific merchant number,

based on the selected date range

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return AuthorizationLog Summary

**conditions**

**SOAP API**

AccessOne Reporting API Specifications

Page **55** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**SAMPLE REQUEST:**

GetAuthorizationLogDetailRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetAuthorizationLogDetailResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationLogDetail

**Method**

POST

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationLogDetail\_RestResponse.xml

\20. GetAuthorizationLogBuyPassSummary

**Service Operation GetAuthorizationLogBuyPassSummary ()**

**Name**

GetAuthorizationLogBuyPassSummary

Return summarized data of Buypass authorization transactions based on the selected

criteria

**Description**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**Pre-**

**conditions**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

AccessOne Reporting API Specifications

Page **56** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\+ **Notes**: **[Re[f(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return AuthorizationLogBuyPass Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetAuthorizationLogBuyPassSummaryRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetAuthorizationLogBuyPassSummaryResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationLogBuyPassSummary

**Method**

POST

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue>512888888888051</HierarchyFilterValue>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationLogBuyPassSummary\_RestResponse.xml

\21. GetAuthorizationLogBuyPassDetail

**Service Operation GetAuthorizationLogBuyPassDetail ()**

AccessOne Reporting API Specifications

Page **57** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Name**

GetAuthorizationLogBuyPassDetail

Return detailed data of Buypass authorization transactions for a specific merchant

number, based on the selected date range

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return Batch Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetAuthorizationLogBuyPassDetailRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetAuthorizationLogBuyPassDetailResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationLogBuyPassDetail

**Method**

POST

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationLogBuyPassDetail\_RestResponse.xml

AccessOne Reporting API Specifications

Page **58** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\22. GetAuthorizationLogGGe4Summary

**Service Operation GetAuthorizationLogGGe4Summary ()**

**Name**

GetAuthorizationLogGGe4Summary

Return summarized data of GGe4 authorization transactions based on the selected

criteria

**Description**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

\+ **Contraints**:

**Pre-**

**conditions**

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return AuthorizationLogGGe4 Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetAuthorizationLogGGe4SummaryRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetAuthorizationLogGGe4SummaryResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationLogGGe4Summary

**Method**

POST

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue>512888888888051</HierarchyFilterValue>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

AccessOne Reporting API Specifications

Page **59** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationLogGGe4Summary\_RestResponse.xml

\23. GetAuthorizationLogGGe4Detail

**Service Operation GetAuthorizationLogGGe4Detail ()**

**Name**

GetAuthorizationLogGGe4Detail

Return detailed data of GGe4 authorization transactions for a specific merchant

number, based on the selected date range

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return AuthorizationLogGGe4 Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetAuthorizationLogGGe4DetailRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetAuthorizationLogGGe4DetailResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationLogGGe4Detail

**Method** POST

AccessOne Reporting API Specifications

Page **60** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationLogGGe4Detail\_RestResponse.xml

\24. GetAuthorizationLogNashvilleSummary

**Service Operation GetAuthorizationLogNashvilleSummary()**

**Name**

GetAuthorizationLogNashvilleSummary

Return summarized data of Nashville authorization transactions based on the selected

criteria

**Description**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

\+ **Contraints**:

**Pre-**

**conditions**

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return AuthorizationLogNashville Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

**Message**

**Exchange**

**Pattern**

GetAuthorizationLogNashvilleSummaryRequest.xml

**See RESPONSE ATTACHED:**

AccessOne Reporting API Specifications

Page **61** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





GetAuthorizationLogNashvilleSummaryResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationLogNashvilleSummary

**Method**

POST

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue>512888888888051</HierarchyFilterValue>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationLogNashvilleSummary\_RestResponse.xml

\25. GetAuthorizationLogNashvilleDetail

**Service Operation GetAuthorizationLogNashvilleDetail ()**

**Name**

GetAuthorizationLogNashvilleDetail

Return detailed data of Nashville authorization transactions for a specific merchant

number, based on the selected date range

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return AuthorizationLogNashville Summary

**conditions**

**SOAP API**

AccessOne Reporting API Specifications

Page **62** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**SAMPLE REQUEST:**

GetAuthorizationLogNashvilleDetailRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetAuthorizationLogNashvilleDetailResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationLogNashvilleDetail

**Method**

POST

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-10-23T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationLogNashvilleDetail\_RestResponse.xml

\26. GetAuthorizationLogNorthSummary

**Service Operation GetAuthorizationLogNorthSummary ()**

**Name**

GetAuthorizationLogNorthSummary

Return summarized data of North authorization transactions based on the selected

criteria

**Description**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**Pre-**

**conditions**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

AccessOne Reporting API Specifications

Page **63** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return AuthorizationLogNorth Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetAuthorizationLogNorthSummaryRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetAuthorizationLogNorthSummaryResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationLogNorthSummary

**Method**

POST

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-01-01T00:00:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationLogNorthSummary\_RestResponse.xml

\27. GetAuthorizationLogNorthDetail

**Service Operation GetAuthorizationLogNorthDetail()**

AccessOne Reporting API Specifications

Page **64** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Name**

GetAuthorizationLogNorthDetail

Return detailed data of North authorization transactions for a specific merchant

number, based on the selected date range

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return AuthorizationLogNorth Details

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetAuthorizationLogNorthDetailRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetAuthorizationLogNorthDetailResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationLogNorthDetail

**Method**

POST

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-01-01T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationLogNorthDetail\_RestResponse.xml

AccessOne Reporting API Specifications

Page **65** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\28. GetAuthorizationLogOmahaSummary

**Service Operation GetAuthorizationLogOmahaSummary ()**

**Name**

GetAuthorizationLogOmahaSummary

Return summarized data of Omaha authorization transactions based on the selected

criteria

**Description**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

\+ **Contraints**:

**Pre-**

**conditions**

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return AuthorizationLogOmaha Summary

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetAuthorizationLogOmahaSummaryRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetAuthorizationLogOmahaSummaryResponse.xml

**REST API**

/rest/GetAuthorizationLogOmahaSummary

POST

**Request URL**

**Method**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-01-01T00:00:00</ToDate>

AccessOne Reporting API Specifications

Page **66** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationLogOmahaSummary\_RestResponse.xml

\29. GetAuthorizationLogOmahaDetail

**Service Operation GetAuthorizationLogOmahaDetail ()**

**Name**

GetAuthorizationLogOmahaDetail

Return detailed data of Omaha authorization transactions for a specific merchant

number, based on the selected date range

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return AuthorizationLogOmaha Details

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetAuthorizationLogOmahaDetailRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetAuthorizationLogOmahaDetailResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationLogOmahaDetail

**Method** POST

AccessOne Reporting API Specifications

Page **67** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-01-01T00:00:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationLogOmahaDetail\_RestResponse.xml

\30. GetAuthorizationVendorSummary

**Service Operation GetAuthorizationVendorSummary()**

**Name**

GetAuthorizationVendorSummary

Return summarized data of authorization transactions by vendors based on the selected

criteria

**Description**

\+ **Parameters:**

**Name**

[HierarchyFilterMode](#br14)

**Default**

Platform

[HierarchyFilterValue](#br14)

[FromDate](#br14)

[ToDate](#br15)

ToDay – 1

ToDay – 1

100

[PageSize](#br15)

**Pre-**

**conditions**

[CurrentPageIndex](#br15)

[VendorId](#br17)

0

**Blank**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return AuthorizationVendor Summary

**conditions**

**SOAP API**

AccessOne Reporting API Specifications

Page **68** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**SAMPLE REQUEST:**

GetAuthorizationVendorSummaryRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetAuthorizationVendorSummaryResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationVendorSummary

**Method**

POST

<VendorAuthorizationFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-01-01T00:00:00</ToDate>

<ViewLevel>None</ViewLevel>

<VendorId></VendorId>

</VendorAuthorizationFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationVendorSummary\_RestResponse.xml

\31. GetAuthorizationVendorDetail

**Service Operation GetAuthorizationVendorDetail ()**

**Name**

GetAuthorizationVendorDetail

Return detailed data of authorization transactions by vendors for a specific merchant

number, based on the selected date range

**Description**

AccessOne Reporting API Specifications

Page **69** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\+ **Parameters:**

**Name**

**Default**

ToDay – 1

**Require**

[MerchantNumber](#br15)

[FromDate](#br14)

[ToDate](#br15)

True

**Pre-**

**conditions**

ToDay – 1

100

[PageSize](#br15)

[CurrentPageIndex](#br15)

[VendorId](#br17)

0

**Blank**

Return AuthorizationVendor Detail

**Post-**

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetAuthorizationVendorDetailRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetAuthorizationVendorDetailResponse.xml

**REST API**

**Request URL** /rest/GetAuthorizationVendorDetail

**Method**

POST

<VendorAuthorizationDetailFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-01T00:00:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

<ToDate>2019-01-01T00:00:00</ToDate>

<VendorId></VendorId>

</VendorAuthorizationDetailFilter>

**Request**

**Response**

**Sample XML**

GetAuthorizationVendorDetail\_RestResponse.xml

AccessOne Reporting API Specifications

Page **70** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\32. GetMerchantList

**Service Operation GetMerchantList ()**

**Name**

GetMerchantList

Return a merchant list with detailed data for each merchant based on the selected

criteria

**Description**

\+ **Parameters: [[Ref(**](#br18)[**III.3.3](#br18))]**

\+ **Contraints**:

\-

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group (SubClient**,** Platform**,**

MasterSaleAgent, CorporateName, MerchantName, MerchantNumber, Sys,

SysPrin, SysPrinAgent, SalesAgent, HeadquarterMerchantNumber, Bank, Agent,

Corp, NorthChain, NorthSalesAgent, MasterChain, MemphisChain,

SalesmanNo, MccSic, FeeClass, Misc1, Misc2)

**Pre-**

**conditions**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

Return List Merchants

**Post-**

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetMerchantListRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetMerchantListResponse.xml

**REST API**

**Request URL** /rest/GetMerchantList

**Method** POST

AccessOne Reporting API Specifications

Page **71** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<HierarchyPagingFilter xmlns="http://api.lonestar.com/types">

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<CurrentPageIndex>1</CurrentPageIndex>

<PageSize>10</PageSize>

**Request**

**Body Sample**

**XML**

</HierarchyPagingFilter>

**Request**

**Response**

**Sample XML**

GetMerchantList\_RestResponse.xml

\33. GetMerchantComments

Service Operation **GetMerchantComments** ()

**Name**

GetMerchantComments

**Description**

Return the list of comment for specific merchant

**Pre-**

\+ **Parameters: [[Ref(**](#br19)[**III.3.4](#br19))]**

**conditions**

**Post-**

Return List Comment of merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetMerchantCommentsRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetMerchantCommentsResponse.xml

**REST API**

**Request URL** /rest/GetMerchantComments

**Method** POST

AccessOne Reporting API Specifications

Page **72** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Request**

**Body Sample**

**XML**

<MerchantInformationPagingFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>512888888888051</MerchantNumber>

<CurrentPageIndex>1</CurrentPageIndex>

<PageSize>10</PageSize>

</MerchantInformationPagingFilter>

**Request**

**Response**

**Sample XML**

GetMerchantComments\_RestResponse.xml

\34. GetOmahaMerchantProfile

**Service Operation GetOmahaMerchantProfile** ()

**Name**

GetOmahaMerchantProfile

**Description**

Return a full profile for specific Omaha merchant

**Pre-**

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**conditions**

**Post-**

Return Profile of Omaha Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetOmahaMerchantProfileRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetOmahaMerchantProfileResponse.xml

**REST API**

**Request URL** /rest/GetOmahaMerchantProfile

AccessOne Reporting API Specifications

Page **73** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Method**

POST

<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>512888888888051</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetOmahaMerchantProfile\_RestResponse.xml

\35. GetOmahaMerchantCardType

**Service Operation GetOmahaMerchantCardType()**

**Name**

GetOmahaMerchantCardType

**Description**

Return the card type list for specific Omaha merchant

**Pre-**

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**conditions**

**Post-**

Return the Card Type list of Omaha merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetOmahaMerchantCardTypeRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetOmahaMerchantCardTypeResponse.xml

**REST API**

**Request URL** /rest/GetOmahaMerchantCardType

**Method** POST

AccessOne Reporting API Specifications

Page **74** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>5348120280516883</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetOmahaMerchantCardType\_RestResponse.xml

\36. GetOmahaMerchantCardTypePinDebit

**Service Operation GetOmahaMerchantCardTypePinDebit()**

**Name**

GetOmahaMerchantCardTypePinDebit

**Description**

Return a list of Card Type PIN Debit for specific Omaha merchant

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**Pre-**

**conditions**

**Post-**

Return List CardType Pin Debit of Omaha Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetOmahaMerchantCardTypePinDebitRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetOmahaMerchantCardTypePinDebitResponse.xml

**REST API**

**Request URL** /rest/GetOmahaMerchantCardTypePinDebit

**Method** POST

AccessOne Reporting API Specifications

Page **75** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>5348120280516883</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetOmahaMerchantCardTypePinDebit\_RestResponse.xml

\37. GetOmahaMerchantCardInfomationPrivateLabel

**Service Operation GetOmahaMerchantCardInfomationPrivateLabel()**

**Name**

GetOmahaMerchantCardInfomationPrivateLabel

Return the detailed data of Private Label Card Type for specific Omaha merchant

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**Description**

**Pre-**

**conditions**

**Post-**

Return List Private Label Card Type of Omaha Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetOmahaMerchantCardInfomationPrivateLabelRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetOmahaMerchantCardInfomationPrivateLabelResponse.xml

**REST API**

**Request URL** /rest/GetOmahaMerchantCardInfomationPrivateLabel

**Method** POST

AccessOne Reporting API Specifications

Page **76** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>518564380305865</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetOmahaMerchantCardInfomationPrivateLabel\_RestResponse.xml

\38. GetOmahaMerchantMemos

**Service Operation GetOmahaMerchantMemos()**

**Name**

GetOmahaMerchantMemos

**Description**

Return Memos data for specific Omaha merchant

**Pre-**

\+ **Parameters: [[Ref(**](#br19)[**III.3.4](#br19))]**

**conditions**

**Post-**

Return List Memo of Omaha Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetOmahaMerchantMemosRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetOmahaMerchantMemosResponse.xml

**REST API**

**Request URL** /rest/GetOmahaMerchantMemos

**Method** POST

AccessOne Reporting API Specifications

Page **77** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationPagingFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>518564380158899</MerchantNumber>

<CurrentPageIndex>1</CurrentPageIndex>

**Request**

**Body Sample**

**XML**

<PageSize>10</PageSize>

</MerchantInformationPagingFilter>

**Request**

**Response**

**Sample XML**

GetOmahaMerchantMemos\_RestResponse.xml

\39. GetNorthMerchantProfile

**Service Operation GetNorthMerchantProfile ()**

**Name**

GetNorthMerchantProfile

**Description**

Return a full profile data for specific North merchant

**Pre-**

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**conditions**

**Post-**

Return profile of North Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetNorthMerchantProfileRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetNorthMerchantProfileResponse.xml

**REST API**

**Request URL** /rest/GetNorthMerchantProfile

**Method** POST

AccessOne Reporting API Specifications

Page **78** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>362310368885</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetNorthMerchantProfile\_RestResponse.xml

\40. GetNorthMechantEntitlements

**Service Operation GetNorthMechantEntitlements()**

**Name**

GetNorthMechantEntitlements

**Description**

Return entitlement data of the North merchant

**Pre-**

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**conditions**

**Post-**

Return List Entitlement of North merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetNorthMechantEntitlementsRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetNorthMechantEntitlementsResponse.xml

**REST API**

**Request URL** /rest/GetNorthMechantEntitlements

**Method** POST

AccessOne Reporting API Specifications

Page **79** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>362310368885</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetNorthMechantEntitlements\_RestResponse.xml

\41. GetNorthMerchantPricingInformation

**Service Operation GetNorthMerchantPricingInformation ()**

**Name**

GetNorthMerchantPricingInformation

**Description**

Return the pricing information (merchant fee) for specific North merchant

\+ **Parameters: [[Ref(**](#br19)[**III.3.4](#br19))]**

**Pre-**

**conditions**

**Post-**

Return List Pricing Info of North Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetNorthMerchantPricingInformationRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetNorthMerchantPricingInformationResponse.xml

**REST API**

**Request URL** /rest/GetNorthMerchantPricingInformation

**Method** POST

AccessOne Reporting API Specifications

Page **80** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>102212361996</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetNorthMerchantPricingInformation\_RestResponse.xml

\42. GetNorthMerchantEntitlementFull

**Service Operation GetNorthMerchantEntitlementFull()**

**Name**

GetNorthMerchantEntitlementFull

**Description**

Return full Entitlement data of specific product code for North merchant

\+ **Parameters: [[Ref(**](#br19)[**III.3.6](#br19))]**

**Pre-**

**conditions**

**Post-**

Return Entitlement Detail of North Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetNorthMerchantEntitlementFullRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetNorthMerchantEntitlementFullResponse.xml

**REST API**

**Request URL** /rest/GetNorthMerchantEntitlementFull

**Method** POST

AccessOne Reporting API Specifications

Page **81** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<NorthMerchantEntitlementDetailFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>102212361996</MerchantNumber>

<ProductCode>01</ProductCode>

**Request**

**Body Sample**

**XML**

</NorthMerchantEntitlementDetailFilter>

**Request**

**Response**

**Sample XML**

GetNorthMerchantEntitlementFull\_RestRespone.xml

\43. GetNorthMerchantEntitlementDetail

**Service Operation GetNorthMerchantEntitlementDetail**()

**Name**

GetNorthMerchantEntitlementDetail

**Description**

Return the detailed Entitlement data of specific product code for North merchant

\+ **Parameters: [[Ref(**](#br19)[**III.3.6](#br19))]**

**Pre-**

**conditions**

**Post-**

Return List Entitlement Sub Detail of North Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetNorthMerchantEntitlementDetailRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetNorthMerchantEntitlementDetailResponse.xml

**REST API**

**Request URL** /rest/GetNorthMerchantEntitlementDetail

**Method** POST

AccessOne Reporting API Specifications

Page **82** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Request**

**Body Sample**

**XML**

<NorthMerchantEntitlementDetailFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>362200216889</MerchantNumber>

<ProductCode>06</ProductCode>

</NorthMerchantEntitlementDetailFilter>

**Request**

**Response**

**Sample XML**

GetNorthMerchantEntitlementDetail\_RestResponse.xml

\44. GetMemphisMerchantProfile

**Service Operation GetMemphisMerchantProfile**()

**Name**

**GetMemphisMerchantProfile**

**Description**

Return a full profile for specific Memphis merchant

**Pre-**

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**conditions**

**Post-**

Return Profile of Memphis Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetMemphisMerchantProfileRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetMemphisMerchantProfileResponse.xml

**REST API**

**Request URL** /rest/GetMemphisMerchantProfile

**Method** POST

AccessOne Reporting API Specifications

Page **83** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>02550630018</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetMemphisMerchantProfile\_RestResponse.xml

\45. GetMemphisMerchantCardInformation

**Service Operation GetMemphisMerchantCardInformation**()

**Name**

GetMemphisMerchantCardInformation

Return data relating to card payment services accepted/rejected by the Memphis

merchant

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**conditions**

**Post-**

Return List Card Info of Memphis Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetMemphisMerchantCardInformationRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetMemphisMerchantCardInformationResponse.xml

**REST API**

**Request URL** /rest/GetMemphisMerchantCardInformation

**Method** POST

AccessOne Reporting API Specifications

Page **84** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>06283000001</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetMemphisMerchantCardInformation\_RestResponse.xml

\46. GetMemphisMerchantCardServicesInformation

**Service Operation GetMemphisMerchantCardServicesInformation**()

**Name**

GetMemphisMerchantCardServicesInformation

Return data relating to additional card payment services accepted/rejected by the

Memphis merchant

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**conditions**

**Post-**

Return List CardService of Memphis Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetMemphisMerchantCardServicesInformationRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetMemphisMerchantCardServicesInformationResponse.xml

**REST API**

**Request URL** /rest/GetMemphisMerchantCardServicesInformation

**Method** POST

AccessOne Reporting API Specifications

Page **85** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>04283036501</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetMemphisMerchantCardServicesInformation\_RestResponse.xml

\47. GetMemphisMerchantDebitNetworks

**Service Operation GetMemphisMerchantDebitNetworks** ()

**Name**

GetMemphisMerchantDebitNetworks

**Description**

Return data of debit networks that the Memphis merchant participates

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**Pre-**

**conditions**

**Post-**

Return List DebiteNetworks of Memphis Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetMemphisMerchantDebitNetworksRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetMemphisMerchantDebitNetworksResponse.xml

**REST API**

**Request URL** /rest/GetMemphisMerchantDebitNetworks

**Method** POST

AccessOne Reporting API Specifications

Page **86** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Request**

**Body Sample**

**XML**

<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>06283000001</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Response**

**Sample XML**

GetMemphisMerchantDebitNetworks\_RestResponse.xml

\48. GetMemphisMerchantAttributes

**Service Operation GetMemphisMerchantAttributes ()**

**Name**

GetMemphisMerchantAttributes

**Description**

Return detailed data of the attributes of the Memphis merchant

**Pre-**

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**conditions**

**Post-**

Return List Attribute of Memphis Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetMemphisMerchantAttributesRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetMemphisMerchantAttributesResponse.xml

**REST API**

**Request URL** /rest/GetMemphisMerchantAttributes

**Method** POST

AccessOne Reporting API Specifications

Page **87** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>06283000001</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetMemphisMerchantAttributes\_RestResponse.xml

\49. GetMemphisMerchantEquipments

**Service Operation GetMemphisMerchantEquipments ()**

**Name**

GetMemphisMerchantEquipments

**Description**

Return detailed data of the equipments currently **in** use by the Memphis merchant

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**Pre-**

**conditions**

**Post-**

Return List Equipment of Memphis Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetMemphisMerchantEquipmentsRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetMemphisMerchantEquipmentsResponse.xml

**REST API**

**Request URL** /rest/GetMemphisMerchantEquipments

**Method** POST

AccessOne Reporting API Specifications

Page **88** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>02550630018</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetMemphisMerchantEquipments\_RestResponse.xml

\50. GetMemphisMerchantBuypassInformation

**Service Operation GetMemphisMerchantBuypassInformation ()**

**Name**

GetMemphisMerchantBuypassInformation

**Description**

Return data of the Memphis merchant relating to Buypass merchant network

\+ **Parameters: [[Ref(**](#br19)[**III.3.5](#br19))]**

**Pre-**

**conditions**

**Post-**

Return List Buypass of Memphis Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetMemphisMerchantBuypassInformationRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetMemphisMerchantBuypassInformationResponse.xml

**REST API**

**Request URL** /rest/GetMemphisMerchantBuypassInformation

**Method** POST

AccessOne Reporting API Specifications

Page **89** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>06283000001</MerchantNumber>

</MerchantInformationFilter>

**Request**

**Body Sample**

**XML**

**Request**

**Response**

**Sample XML**

GetMemphisMerchantBuypassInformation\_RestResponse.xml

\51. GetMemphisMerchantCardInformationDetail

**Service Operation GetMemphisMerchantCardInformationDetail ()**

**Name**

GetMemphisMerchantCardInformationDetail

Return detailed data of all sub card payment services of the selected card payment

service accepted by the Memphis merchant

**Description**

\+ **Parameters:**

**Name**

[MerchantNumber](#br15)

[CmsId](#br17)

**Require**

True

True

**Pre-**

**conditions**

[ServicesMerchantId](#br17)

True

**Post-**

Return List CardInformation Detail of Memphis Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetMemphisMerchantCardInformationDetailRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetMemphisMerchantCardInformationDetailResponse.xml

**REST API**

**Request URL** /rest/GetMemphisMerchantCardInformationDetail

AccessOne Reporting API Specifications

Page **90** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Method**

POST

**Request**

**Body Sample**

<MemphisMerchantCardInformationDetailFilter

xmlns="http://api.lonestar.com/types">

<MerchantNumber>02550630018</MerchantNumber>

<CmsId>4926869</CmsId>

<ServicesMerchantId>122222</ServicesMerchantId>

</MemphisMerchantCardInformationDetailFilter>

**Request**

**Response**

**Sample**

GetMemphisMerchantCardInformationDetail\_RestResponse.xml

\52. GetMemphisMerchantEquipmentSpecificExtra

**Service Operation GetMemphisMerchantEquipmentSpecificExtra ()**

**Name**

GetMemphisMerchantEquipmentSpecificExtra

Return data relating to equipment specifics and equipment extras of the chosen

equipment ID

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br19)[**III.3.7](#br19))]**

**conditions**

**Post-**

Return EquipmentSpecificExtra of Memphis

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetMemphisMerchantEquipmentSpecificExtraRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetMemphisMerchantEquipmentSpecificExtraResponse.xml

**REST API**

AccessOne Reporting API Specifications

Page **91** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Request URL** /rest/ GetMemphisMerchantEquipmentSpecificExtra

**Method**

POST

**Request**

**Body Sample**

<MemphisMerchantEquipmentDetailFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>02550630018</MerchantNumber>

<EquipId>001LKZS</EquipId>

</MemphisMerchantEquipmentDetailFilter>

**Request**

**Response**

**Sample**

GetMemphisMerchantEquipmentSpecificExtra\_RestResponse.xml

\53. GetMemphisMerchantEquipmentAttribute

**Service Operation GetMemphisMerchantEquipmentAttribute ()**

**Name**

GetMemphisMerchantEquipmentAttribute

Return detailed data on the attributes of the chosen equipment id

\+ **Parameters: [[Ref(**](#br19)[**III.3.7](#br19))]**

**Description**

**Pre-**

**conditions**

**Post-**

Return List EquipmentAttribute of Memphis Merchant

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

GetMemphisMerchantEquipmentAttributeRequest.xml

**Message**

**Exchange**

**Pattern**

**See RESPONSE ATTACHED:**

GetMemphisMerchantEquipmentAttributeResponse.xml

**REST API**

AccessOne Reporting API Specifications

Page **92** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Request URL** /rest/ GetMemphisMerchantEquipmentAttribute

**Method**

POST

**Request**

**Body Sample**

<MemphisMerchantEquipmentDetailFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>02550630018</MerchantNumber>

<EquipId>001LKZS</EquipId>

</MemphisMerchantEquipmentDetailFilter>

**Request**

**Response**

**Sample**

GetMemphisMerchantEquipmentAttribute\_RestResponse.xml

\54. GetOmahaMerchantStatementList.

**Service Operation GetOmahaMerchantStatement ()**

**Name**

GetOmahaMerchantStatementList.

**Description**

Return available statements for a merchant

\+ **Parameters:**

**Pre-**

**conditions**

**Name**

**Require**

[MerchantNumber](#br15)

True

**Post-**

Returns list of StatementId values for available statements

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

**Message**

**Exchange**

**Pattern**

GetOmahaMerchan

tStatementList.xml

**REST API**

**Request URL** /rest/GetOmahaMerchantStatementList

AccessOne Reporting API Specifications

Page **93** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Method**

POST

**Request**

**Body Sample**

<MerchantInformationFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>02550630018</MerchantNumber>

</MerchantInformationFilter>

\55. GetOmahaMerchantStatement.

**Service Operation GetOmahaMerchantStatement ()**

**Name**

GetOmahaMerchantStatement.

**Description**

Return statement data for a merchant statement

\+ **Parameters:**

**Pre-**

**conditions**

**Name**

[MerchantNumber](#br15)

[StatementId](#br17)

**Require**

True

True

**Post-**

Returns the statement as a Base64 encoded PDF

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

**Message**

**Exchange**

**Pattern**

GetOmahaMerchan

tStatement.xml

**REST API**

**Request URL** /rest/GetOmahaMerchantStatement

**Method**

POST

**Request**

**Body Sample**

<MerchantStatementFilter xmlns="http://api.lonestar.com/types">

<MerchantNumber>02550630018</MerchantNumber>

<StatementId>1</StatementId>

</MerchantStatementFilter>

AccessOne Reporting API Specifications

Page **94** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





GetNonQualifyingTransactionSummaryByEntity

**Service Operation GetNonQualifyingTransactionSummaryByEntity ()**

**Name**

GetNonQualifyingTransactionSummaryByEntity.

**Description**

Return Non-qualifying transactions data of hierarchy entity choice(s) based on the

selected date range.

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**conditions**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return Non-qualifying transactions Hierarchy Summary.

**conditions**

·

·

·

NonQualifyingTransactions:

**Response**

**Data**

o

o

DowngradeCount

Entity

o

o

o

o

o

o

FeeCount

NetAmount

ReturnAmount

RowNumber

SaleAmount

TotalRows

o

o

TransactionCount

UpgradeCount

Total:

o

o

DowngradeCount

Entity

o

o

o

o

o

o

FeeCount

NetAmount

ReturnAmount

RowNumber

SaleAmount

TotalRows

o

TransactionCount

UpgradeCount

o

Paging:

o

CurrentPageIndex

PageSize

o

AccessOne Reporting API Specifications

Page **95** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetNonQualifyingTra

nsactionSummaryByEn

**SAMPLE RESPONSE:**

GetNonQualifyingTra

nsactionSummaryByEn

**REST API**

**Request URL** /rest/GetNonQualifyingTransactionSummaryByEntity

**Method**

POST

**Request**

**Body Sample**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2012-07-16T19:20:30</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>100</PageSize>

<ToDate>2018-07-16T19:20:30</ToDate>

<ViewLevel>Hierarchy</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample**

GetNonQualifyingTransactionSummaryByEntity\_RestResponse.xml

GetNonQualifyingTransactionByMerchant

**Service Operation GetNonQualifyingTransactionByMerchant ()**

**Name**

GetNonQualifyingTransactionByMerchant.

**Description**

Return Non-qualifying transactions data of the selected merchant number

AccessOne Reporting API Specifications

Page **96** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18)[**)\]**](#br18)**

**conditions**

**Post-**

Return Non-qualifying transactions data.

**conditions**

·

·

·

NonQualifyingTransactionsDetail:

**Response**

**Data**

o

o

o

o

AccountNumber

AuthorizationAmount

AuthorizationDate

AuthorizationNumber

FeeRate

o

o

o

o

o

FeeRateDescription

QualificationCode

QualificationDescription1

ReasonCode

o

o

ReasonCodeDescription

ReportDate

o

o

o

o

TotalRows

TransactionAmount

TransactionCode

TransactionDate

TransactionID

o

Total:

o

o

o

o

AccountNumber

AuthorizationAmount

AuthorizationDate

AuthorizationNumber

FeeRate

o

o

o

o

o

FeeRateDescription

QualificationCode

QualificationDescription1

ReasonCode

o

o

ReasonCodeDescription

ReportDate

o

o

o

o

TotalRows

TransactionAmount

TransactionCode

TransactionDate

TransactionID

o

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

AccessOne Reporting API Specifications

Page **97** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetNonQualifyingTra

nsactionByMerchant\_

**SAMPLE RESPONSE:**

GetNonQualifyingTra

nsactionByMerchant\_

**REST API**

**Request URL** /rest/GetNonQualifyingTransactionByMerchant

**Method**

POST

**Request**

**Body Sample**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2012-07-16T19:20:30</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>100</PageSize>

<ToDate>2018-07-16T19:20:30</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample**

GetNonQualifyingTransactionByMerchant\_RestResponse.xml

GetGGe4MerchantEnrollment

**Service Operation GetGGe4MerchantEnrollment()**

**Name**

GetGGe4MerchantEnrollment.

Return Payeezy Gateway Enrollment Activity report.

\+ **Parameters:**

**Description**

**Pre-**

**conditions**

**Name**

**Require/Default**

HierarchyFilterMode

AccessOne Reporting API Specifications

Page **98** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





HierarchyFilterValue

FromDate

ToDate

True

True

True

ViewLevel

ActivityMode

True

1:ALL;

1: ACCEPTED;

0: REJECTED;

2: CHANGED

WorkingMode

True

1:all,

1:worked,

0: not worked

CurrentPageIndex

PageSize

**Post-**

Return Payeezy Gateway Enrollment Activity report.

**conditions**

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetGGe4MerchantEn

rollment\_Request.xml

**SAMPLE RESPONSE:**

GetGGe4MerchantEn

rollment\_Response.xm

·

GGe4MerchantEnrollment:

**Response**

**Data**

o

EnrollmentStatus

LastMessage

MerchantNumber

ReportDate

o

o

o

o

o

o

RowNumber

TotalRows

Worked

·

Paging:

AccessOne Reporting API Specifications

Page **99** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**REST API**

**Request URL** /rest/ GetGGe4MerchantEnrollment

**Method**

POST

**Request**

**Body Sample**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2012-07-16T19:20:30</FromDate>

<HierarchyFilterMode>SubClient</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>100</PageSize>

<ToDate>2018-07-16T19:20:30</ToDate>

<ViewLevel>Hierarchy</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample**

GetGGe4MerchantEnrollment\_RestResponse.xml

GetGGe4MerchantEnrollmentByMerchant

**Service Operation GetGGe4MerchantEnrollmentByMerchant()**

**Name**

GetGGe4MerchantEnrollment.

**Description**

Return Payeezy Gateway Enrollment Activity report of the selected merchant number.

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

\+ **Parameters:**

**Name**

**Require/Default**

FromDate

MerchantNumber

ToDate

True

True

True

True

ActivityMode

1:ALL;

1: ACCEPTED;

AccessOne Reporting API Specifications

Page **100** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





0: REJECTED;

2: CHANGED

WorkingMode

True

1:all,

1:worked,

0: not worked

CurrentPageIndex

PageSize

**Post-**

Return Payeezy Gateway Enrollment Activity report of the selected merchant number.

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

**Message**

**Exchange**

**Pattern**

GetGGe4MerchantEn

rollmentByMerchant\_R

**SAMPLE RESPONSE:**

GetGGe4MerchantEn

rollmentByMerchant\_R

·

·

GGe4MerchantEnrollment:

**Response**

**Data**

o

o

o

o

EnrollmentStatus

LastMessage

MerchantNumber

ReportDate

o

o

RowNumber

TotalRows

o

Worked

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**REST API**

**Request URL** /rest/GetGGe4MerchantEnrollmentByMerchant

AccessOne Reporting API Specifications

Page **101** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Method**

POST

**Request**

**Body Sample**

<GGe4MerchantEnrollmentMerchantFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2012-07-16T19:20:30</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>100</PageSize>

<ToDate>2018-07-16T19:20:30</ToDate>

<ActivityMode>-1</ActivityMode>

<WorkingMode>-1</WorkingMode>

</GGe4MerchantEnrollmentMerchantFilter>

**Request**

**Response**

**Sample**

GetGGe4MerchantEnrollmentByMerchant\_RestResponse.xml

GetReturnsReportByEntity

**Service Operation GetReturnsReportByEntity ()**

**Name**

GetReturnsReportByEntity.

**Description**

Return the Returns report data of the entity choices based on the selected date range.

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**conditions**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return the Returns Hierarchy report.

**conditions**

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetReturnsReportBy

Entity\_Request.xml

AccessOne Reporting API Specifications

Page **102** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**SAMPLE RESPONSE:**

GetReturnsReportBy

Entity\_Response.xml

·

·

·

ReturnReport:

**Response**

**Data**

o

o

Entity

FullReturn

o

o

NetAmount

NoMatch

o

o

o

o

o

o

o

NonVerifiedReturnCount

PartialReturn

ReturnAmount

ReturnCount

RowNumber

SaleAmount

SaleCount

o

TotalRows

Total:

o

Entity

o

o

FullReturn

NetAmount

o

o

o

o

o

o

o

o

NoMatch

NonVerifiedReturnCount

PartialReturn

ReturnAmount

ReturnCount

RowNumber

SaleAmount

SaleCount

o

TotalRows

Paging

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**REST API**

**Request URL** /rest/GetReturnsReportByEntity

**Method** POST

AccessOne Reporting API Specifications

Page **103** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Request**

**Body Sample**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2012-07-16T19:20:30</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>100</PageSize>

<ToDate>2018-07-16T19:20:30</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample**

GetReturnsReportByEntity\_RestResponse.xml

GetReturnsReportByMerchant

**Service Operation GetReturnsReportByMerchant ()**

**Name**

GetReturnsReportByMerchant.

**Description**

Return Returns data of a selected merchant number.

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**Pre-**

**conditions**

**Post-**

Return Returns data of a selected merchant.

**conditions**

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetReturnsReportBy

Merchant\_Request.xm

**SAMPLE RESPONSE:**

GetReturnsReportBy

Merchant\_Response.x

AccessOne Reporting API Specifications

Page **104** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





·

·

·

MerchantReturnsReport:

**Response**

**Data**

o

o

o

o

AccountNumber

BatchNumber

CardDescription

CardType

o

o

o

Keyed

KeyedDescription

RecordId

o

o

o

o

ReportDate

ReturnMethod

TerminalNumber

TotalRows

o

o

o

TransactionAmount

TransactionDate

TransactionTime

Total:

o

o

o

o

AccountNumber

BatchNumber

CardDescription

CardType

o

o

o

Keyed

KeyedDescription

RecordId

o

o

o

o

ReportDate

ReturnMethod

TerminalNumber

TotalRows

o

o

o

TransactionAmount

TransactionDate

TransactionTime

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**REST API**

**Request URL** /rest/GetReturnsReportByMerchant

**Method**

POST

**Request**

**Body Sample**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2012-07-16T19:20:30</FromDate>

AccessOne Reporting API Specifications

Page **105** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>100</PageSize>

<ToDate>2018-07-16T19:20:30</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample**

GetReturnsReportByMerchant\_RestResponse.xml

GetCustomerNotPresentByEntity

**Service Operation GetCustomerNotPresentByEntity ()**

**Name**

GetCustomerNotPresentByEntity.

**Description**

Return Customer Not Present data of the entity choices based on the selected date

range.

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**conditions**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return Customer Not Present Report.

**conditions**

·

·

·

·

·

·

·

·

·

·

·

·

·

ReportDate

TaxPayerID

TaxPayerIDCount

MerchantNumber

MerchantName

SalesVolume

**Response**

**Data**

NPFFree

HashTaxPayerID

EncryptedTaxID

TotalRows

Sum\_TaxPayerIDCount

Sum\_SalesVolume

Sum\_NPFFee

AccessOne Reporting API Specifications

Page **106** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetCustomerNotPres

entByEntity\_Request.

**REST API**

**Request URL** /rest/GetCustomerNotPresentByEntity

**Method**

POST

**Request**

**Body Sample**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2012-07-16T19:20:30</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>100</PageSize>

<ToDate>2018-07-16T19:20:30</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample**

GetCustomerNotPresentByEntity\_RestResponse.xml

GetCustomerNotPresentByMerchant

**Service Operation GetCustomerNotPresentByMerchant ()**

**Name**

GetCustomerNotPresentByMerchant

**Description**

Return CustomerNot Present data of a selected merchant number.

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**Pre-**

**conditions**

**Post-**

Return CustomerNot Present data of a selected merchant number.

**conditions**

AccessOne Reporting API Specifications

Page **107** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





·

·

·

CustomerNotPresent:

**Response**

**Data**

o

o

o

o

EncryptedTaxID

HashTaxPayerID

MerchantName

MerchantNumber

NPFFee

o

o

o

o

o

ReportDate

RowNumber

SalesVolume

TaxPayerID

o

o

TaxPayerIDCount

TotalRows

Total:

o

o

o

o

EncryptedTaxID

HashTaxPayerID

MerchantName

MerchantNumber

NPFFee

o

o

o

o

o

ReportDate

RowNumber

SalesVolume

TaxPayerID

o

o

TaxPayerIDCount

TotalRows

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetCustomerNotPres

entByMerchant\_Requ

**SAMPLE RESPONSE:**

GetCustomerNotPres

entByMerchant\_Resp

AccessOne Reporting API Specifications

Page **108** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**REST API**

**Request URL** /rest/GetCustomerNotPresentByMerchant

**Method**

POST

**Request**

**Body Sample**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2012-07-16T19:20:30</FromDate>

<MerchantNumber>362200216889</MerchantNumber>

<PageSize>100</PageSize>

<ToDate>2018-07-16T19:20:30</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample**

GetCustomerNotPresentByMerchant\_RestResponse.xml

GetHVMerchantsCustomerPresentByEntity

**Service Operation GetHVMerchantsCustomerPresentByEntity ()**

**Name**

GetHVMerchantsCustomerPresentByEntity.

**Description**

Return high volume merchants customer present data of the entity choices based on

the selected date range.

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**conditions**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return high volume merchants customer present Hierarchy report.

**conditions**

·

HVMerchantsCustomerPresent:

**Response**

**Data**

o

o

o

o

EncryptedTaxID

HashTaxPayerID

MerchantName

MerchantNumber

AccessOne Reporting API Specifications

Page **109** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

o

o

o

o

o

NPFFee

ReportDate

RowNumber

SalesVolume

TaxPayerID

TaxPayerIDCount

TotalRows

·

Total:

o

o

o

o

EncryptedTaxID

HashTaxPayerID

MerchantName

MerchantNumber

NPFFee

o

o

o

o

o

ReportDate

RowNumber

SalesVolume

TaxPayerID

o

o

TaxPayerIDCount

TotalRows

·

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetHVMerchantsCust

omerPresentByEntity\_

**SAMPLE RESPONSE:**

GetHVMerchantsCust

omerPresentByEntity\_

**REST API**

**Request URL** /rest/GetHVMerchantsCustomerPresentByEntity

**Method** POST

AccessOne Reporting API Specifications

Page **110** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Request**

**Body Sample**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2012-07-16T19:20:30</FromDate>

<HierarchyFilterMode>Platform</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>100</PageSize>

<ToDate>2018-07-16T19:20:30</ToDate>

<ViewLevel>Hierarchy</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample**

GetHVMerchantsCustomerPresentByEntity\_RestResponse.xml

GetHVMerchantsCustomerPresentByMerchant

**Service Operation GetHVMerchantsCustomerPresentByMerchant ()**

**Name**

GetHVMerchantsCustomerPresentByMerchant.

**Description**

Return high volume merchants customer present data of selected merchant number.

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**Pre-**

**conditions**

**Post-**

Return high volume merchants customer present report.

**conditions**

·

HVMerchantsCustomerPresent:

**Response**

**Data**

o

o

o

o

o

o

o

o

o

o

o

EncryptedTaxID

HashTaxPayerID

MerchantName

MerchantNumber

NPFFee

ReportDate

RowNumber

SalesVolume

TaxPayerID

TaxPayerIDCount

TotalRows

·

·

Total

Paging:

AccessOne Reporting API Specifications

Page **111** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetHVMerchantsCust

omerPresentByMercha

**SAMPLE RESPONSE:**

GetHVMerchantsCust

omerPresentByMercha

**REST API**

**Request URL** /rest/GetHVMerchantsCustomerPresentByMerchant

**Method**

POST

**Request**

**Body Sample**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-31T11:20:00</FromDate>

<MerchantNumber>02550630018</MerchantNumber>

<PageSize>100</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample**

GetHVMerchantsCustomerPresentByMerchant\_RestResponse.xml

GetAllOtherMCCMerchantsCustomerPresentByEntity

**Service Operation GetAllOtherMCCMerchantsCustomerPresentByEntity ()**

**Name**

GetAllOtherMCCMerchantsCustomerPresentByEntity.

AccessOne Reporting API Specifications

Page **112** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Description**

Return all other MCC merchants customer present data of the entity choices based on

the selected date range.

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**conditions**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return all other MCC merchants customer present Hierarchy Summary.

**conditions**

·

·

·

AllOtherMCCMerchantsCustomerPresent:

**Response**

**Data**

o

o

o

o

EncryptedTaxID

HashTaxPayerID

MerchantName

MerchantNumber

NPFFee

o

o

o

o

o

ReportDate

RowNumber

SalesVolume

TaxPayerID

o

o

TaxPayerIDCount

TotalRows

Total:

o

o

o

o

EncryptedTaxID

HashTaxPayerID

MerchantName

MerchantNumber

NPFFee

o

o

o

o

o

ReportDate

RowNumber

SalesVolume

TaxPayerID

o

o

TaxPayerIDCount

TotalRows

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

AccessOne Reporting API Specifications

Page **113** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetAllOtherMCCMerc

hantsCustomerPresen

**SAMPLE RESPONSE:**

GetAllOtherMCCMerc

hantsCustomerPresen

**REST API**

**Request URL** /rest/GetAllOtherMCCMerchantsCustomerPresentByEntity

**Method**

POST

**Request**

**Body Sample**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2000-05-31T11:20:00</FromDate>

<HierarchyFilterMode>MerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue>02550630018</HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample**

GetAllOtherMCCMerchantsCustomerPresentByEntity\_RestResponse.xml

GetAllOtherMCCMerchantsCustomerPresentByMerchant

**Service Operation GetAllOtherMCCMerchantsCustomerPresentByMerchant ()**

**Name**

GetAllOtherMCCMerchantsCustomerPresentByMerchant.

**Description**

Return all other MCC merchants customer present data of selected merchant number.

AccessOne Reporting API Specifications

Page **114** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return all other MCC merchants customer present report.

**conditions**

·

·

·

AllOtherMCCMerchantsCustomerPresent:

**Response**

**Data**

o

o

o

o

EncryptedTaxID

HashTaxPayerID

MerchantName

MerchantNumber

NPFFee

o

o

o

o

o

ReportDate

RowNumber

SalesVolume

TaxPayerID

o

o

TaxPayerIDCount

TotalRows

Total:

o

o

o

o

EncryptedTaxID

HashTaxPayerID

MerchantName

MerchantNumber

NPFFee

o

o

o

o

o

ReportDate

RowNumber

SalesVolume

TaxPayerID

o

o

TaxPayerIDCount

TotalRows

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetAllOtherMCCMerc

hantsCustomerPresen

**SAMPLE RESPONSE:**

AccessOne Reporting API Specifications

Page **115** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





GetAllOtherMCCMerc

hantsCustomerPresen

**REST API**

**Request URL** /rest/GetAllOtherMCCMerchantsCustomerPresentByMerchant

**Method**

POST

**Request**

**Body Sample**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-31T11:20:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>1</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample**

GetAllOtherMCCMerchantsCustomerPresentByMerchant\_RestResponse.xml

GetMerchantAdjustmentSummaryByEntity

**Service Operation GetMerchantAdjustmentSummaryByEntity ()**

**Name**

GetMerchantAdjustmentSummaryByEntity.

**Description**

Return merchant adjustment data of the entity choices based on the selected date

range.

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**conditions**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return merchant adjustment Hierarchy Summary.

**conditions**

AccessOne Reporting API Specifications

Page **116** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetMerchantAdjustm

entSummaryByEntity\_

**SAMPLE RESPONSE:**

GetMerchantAdjustm

entSummaryByEntity\_

·

MerchantAdjustmentSummary:

**Response**

**Data**

o

o

o

o

o

o

o

Entity

ReturnsAmount

ReturnsCount

RowNumber

SalesAmount

SalesCount

TotalRows

·

·

Total

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**REST API**

**Request URL** /rest/GetMerchantAdjustmentSummaryByEntity

**Method**

POST

**Request**

**Body Sample**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>1999-05-31T11:20:00</FromDate>

<HierarchyFilterMode>Sys</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

AccessOne Reporting API Specifications

Page **117** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Request**

**Response**

**Sample**

GetMerchantAdjustmentSummaryByEntity\_RestResponse.xml

GetMerchantAdjustmentSummaryByMerchant

**Service Operation GetMerchantAdjustmentSummaryByMerchant ()**

**Name**

GetMerchantAdjustmentSummaryByMerchant.

Return merchant adjustment data of selected merchant number .

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**Description**

**Pre-**

**conditions**

**Post-**

Return merchant adjustment summary.

**conditions**

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetMerchantAdjustm

entSummaryByMercha

**SAMPLE RESPONSE:**

GetMerchantAdjustm

entSummaryByMercha

·

MerchantAdjustment:

**Response**

**Data**

o

BatchNumber

ReportDate

o

o

o

o

o

ReturnsAmount

ReturnsCount

SalesAmount

SalesCount

o

o

o

TotalRows

TransactionCode

TransactionDate

·

Total:

o

BatchNumber

AccessOne Reporting API Specifications

Page **118** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

o

o

ReportDate

ReturnsAmount

ReturnsCount

SalesAmount

SalesCount

o

o

o

o

TotalRows

TransactionCode

TransactionDate

·

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**REST API**

**Request URL** /rest/GetMerchantAdjustmentSummaryByMerchant

**Method**

POST

**Request**

**Body Sample**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>2</CurrentPageIndex>

<FromDate>2010-05-31T11:20:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>2</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample**

GetMerchantAdjustmentSummaryByMerchant\_RestResponse.xml

GetMerchantAdjustmentDetail

**Service Operation GetMerchantAdjustmentDetail ()**

**Name**

GetMerchantAdjustmentDetail.

**Description**

Return merchant adjustment details of selected merchant number .

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**Pre-**

**conditions**

**Name**

**Require/Default**

True

FromDate

AccessOne Reporting API Specifications

Page **119** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





ToDate

MerchantNumber

True

True

True

BatchNumber

CurrentPageIndex

PageSize

**Post-**

Return merchant adjustment details.

**conditions**

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetMerchantAdjustm

entDetail\_Request.xm

**SAMPLE RESPONSE:**

GetMerchantAdjustm

entDetail\_Response.x

·

·

·

MerchantAdjustmentDetail:

**Response**

**Data**

o

o

o

OriginalReferenceID

ReturnsAmount

ReturnsCount

o

o

SalesAmount

SalesCount

o

o

o

o

TotalRows

TransactionCode

TransactionCodeDescription

TransactionDate

Total:

o

o

o

OriginalReferenceID

ReturnsAmount

ReturnsCount

o

o

SalesAmount

SalesCount

o

o

o

TotalRows

TransactionCode

TransactionCodeDescription

TransactionDate

o

Paging:

AccessOne Reporting API Specifications

Page **120** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**REST API**

**Request URL** /rest/ GetMerchantAdjustmentDetail

**Method**

POST

<MerchantAdjustmentFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-31T11:20:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>2</PageSize>

**Request**

**Body Sample**

<ToDate>2019-08-31T11:20:00</ToDate>

<BatchNumber>061212MOADJ</BatchNumber>

</MerchantAdjustmentFilter>

**Request**

**Response**

**Sample**

GetMerchantAdjustmentDetail\_RestResponse.xml

GetChatHistorySummaryByEntity

**Service Operation GetChatHistorySummaryByEntity ()**

**Name**

GetChatHistorySummaryByEntity.

**Description**

Return Chat history data of the entity choices based on the selected date range.

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

**Pre-**

**conditions**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return Chat history Hierarchy Summary.

**conditions**

·

ChatSummary:

**Response**

**Data**

o

o

o

o

AverageChatTimeInSeconds

ChatAbandonedCount

ChatCount

ChatOpenedCount

AccessOne Reporting API Specifications

Page **121** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

ChatResolvedCount

Entity

o

o

o

RowNumber

TotalChatTimeInSeconds

TotalRows

·

Total:

o

o

o

AverageChatTimeInSeconds

ChatAbandonedCount

ChatCount

o

o

o

ChatOpenedCount

ChatResolvedCount

Entity

o

o

o

RowNumber

TotalChatTimeInSeconds

TotalRows

·

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**SAMPLE REQUEST:**

**Message**

**Exchange**

**Pattern**

GetChatHistorySumm

aryByEntity\_Request.

**SAMPLE RESPONSE:**

GetChatHistorySumm

aryByEntity\_Respons

**REST API**

**Request URL** /rest/GetChatHistorySummaryByEntity

**Method**

POST

**Request**

**Body Sample**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2000-05-31T11:20:00</FromDate>

<HierarchyFilterMode>Sys</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

AccessOne Reporting API Specifications

Page **122** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<PageSize>10</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample**

GetChatHistorySummaryByEntity\_RestResponse.xml

GetChatHistoryByMerchant

**Service Operation GetChatHistoryByMerchant()**

GetChatHistoryByMerchant.

Return chat history of a specific merchant.

**Name**

**Description**

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Post-**

Return chat history of a specific merchant.

**conditions**

**SOAP API**

**SAMPLE REQUEST:**

**Message**

**Exchange**

**Pattern**

GetChatHistoryByMe

rchant\_Request.xml

**REST API**

/rest/GetChatHistoryByMerchant

POST

**Request URL**

**Method**

**Request**

**Body Sample**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-31T11:20:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>5</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

AccessOne Reporting API Specifications

Page **123** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





</MerchantSummaryFilter>

**Request**

**Response**

**Sample**

GetChatHistoryByMerchant\_RestResponse.xml

GetEMVIndicatorReportByEntity

**Service Operation** GetEMVIndicatorReportByEntity()

**Name**

GetEMVIndicatorReportByEntity.

**Description**

Return EMV indicator data of the entity choices based on the selected date range.

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**Pre-**

**conditions**

**Name**

HierarchyFilterMode

**Require/Default**

HierarchyFilterValue

FromDate

ToDate

True

True

True

(Y,N)

EMVIndicator

CurrentPageIndex

PageSize

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return EMV indicator Hierarchy report.

**conditions**

·

·

EMVReport:

**Response**

**Data**

o

o

o

o

EMVIndicator

MerchantName

MerchantNumber

RowNumber

o

TotalRows

Paging:

o

CurrentPageIndex

AccessOne Reporting API Specifications

Page **124** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetEMVIndicatorRep

ortByEntity\_Request.

**SAMPLE REQUEST:**

GetEMVIndicatorRep

ortByEntity\_Response

**REST API**

**Request URL** /rest/GetEMVIndicatorReportByEntity

**Method**

POST

**Request**

**Body Sample**

<EMVReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-31T11:20:00</FromDate>

<HierarchyFilterMode>MerchantName</HierarchyFilterMode>

<HierarchyFilterValue>test</HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

<ViewLevel>None</ViewLevel>

<EMVIndicator>N</EMVIndicator>

</EMVReportFilter>

**Request**

**Response**

**Sample**

GetEMVIndicatorReportByEntity\_RestResponse.xml

GetEMVIndicatorReportByMerchant

**Service Operation** GetEMVIndicatorReportByMerchant ()

**Name**

GetEMVIndicatorReportByMerchant

AccessOne Reporting API Specifications

Page **125** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Description**

Return EMV indicator report of the merchant.

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**conditions**

**Name**

FromDate

**Require/Default**

True

ToDate

True

MerchantNumber

True

True (Y,N)

EMVIndicator

CurrentPageIndex

PageSize

**Post-**

Return EMV indicator report of the merchant.

**conditions**

·

EMVReportMerchart:

**Response**

**Data**

o

EMVIndicator

MerchantName

MerchantNumber

RowNumber

TotalRows

o

o

o

o

o

o

o

o

o

o

Total

EMVIndicator

MerchantName

MerchantNumber

RowNumber

TotalRows

·

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetEMVIndicatorRep

ortByMerchant\_Reque

**SAMPLE RESPONSE:**

AccessOne Reporting API Specifications

Page **126** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





GetEMVIndicatorRep

ortByMerchant\_Respo

**REST API**

**Request URL** /rest/GetEMVIndicatorReportByMerchant

**Method**

POST

**Request**

**Body Sample**

<EMVMerchantReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-31T11:20:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

<EMVIndicator>Y</EMVIndicator>

</EMVMerchantReportFilter>

**Request**

**Response**

**Sample**

GetEMVIndicatorReportByMerchant\_RestResponse.xml

GetTaxReportDailySubmittedSummaryByEntity

**Service Operation** GetTaxReportDailySubmittedSummaryByEntity()

**Name**

GetTaxReportDailySubmittedSummaryByEntity.

**Description**

Return daily submitted TIN matching summary data of hierarchy entity choice(s) based

on the selected date range.

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**conditions**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

**conditions**

Return daily submitted TIN matching summary data of hierarchy entity choice(s) based

on the selected date range.

AccessOne Reporting API Specifications

Page **127** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Response**

**Data**

·

·

·

TaxReportDailySubmittedSummary:

o

o

o

o

o

o

Entity

MatchedMerchantCount

NotMatchedMerchantCount

RowNumber

SubmittedMerchantCount

TotalRows

Total

o

Entity

o

o

o

MatchedMerchantCount

NotMatchedMerchantCount

RowNumber

o

o

SubmittedMerchantCount

TotalRows

Paging

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetTaxReportDailyS

ubmittedSummaryByE

**SAMPLE RESPONSE:**

GetTaxReportDailyS

ubmittedSummary By E

**REST API**

**Request URL** /rest/GetTaxReportDailySubmittedSummaryByEntity

**Method**

POST

**Request**

**Body Sample**

**XML**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>**1**</CurrentPageIndex>

<FromDate>**2000-05-31T11:20:00**</FromDate>

AccessOne Reporting API Specifications

Page **128** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<HierarchyFilterMode>**Platform**</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>**10**</PageSize>

<ToDate>**2019-10-20T11:20:00**</ToDate>

<ViewLevel>**None**</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetTaxReportDailySubmittedSummaryByEntity\_RestResponse.xml

GetTaxReportDailySubmittedSummaryByMerchant

**Service Operation** GetTaxReportDailySubmittedSummaryByMerchant ()

**Name**

GetTaxReportDailySubmittedSummaryByMerchant.

Return daily submitted TIN matching summary data of the selected merchant number.

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18)[**)\]**](#br18)**

**Description**

**Pre-**

**conditions**

**Post-**

Return daily submitted TIN matching summary data of the selected merchant number.

**conditions**

·

·

·

TaxReportDailySubmittedSummary:

**Response**

**Data**

o

o

o

o

Entity

MatchedMerchantCount

NotMatchedMerchantCount

RowNumber

o

o

SubmittedMerchantCount

TotalRows

Total:

o

Entity

o

o

o

MatchedMerchantCount

NotMatchedMerchantCount

RowNumber

o

o

SubmittedMerchantCount

TotalRows

Paging:

o

CurrentPageIndex

AccessOne Reporting API Specifications

Page **129** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetTaxReportDailyS

ubmittedSummaryByM

**SAMPLE REQUEST:**

GetTaxReportDailyS

ubmittedSummaryByM

**REST API**

**Request URL** /rest/GetTaxReportDailySubmittedSummaryByMerchant

**Method**

POST

**Request**

**Body Sample**

**XML**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2000-05-31T11:20:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

<PageSize>10</PageSize>

<ToDate>2019-10-20T11:20:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetTaxReportDailySubmittedSummaryByMerchant\_RestRespone.xml

GetTaxReportDailySubmittedDetailByEntity

**Service Operation** GetTaxReportDailySubmittedDetailByEntity ()

**Name**

GetTaxReportDailySubmittedDetailByEntity.

**Description**

Return daily submitted TIN matching summary data of hierarchy entity choice(s) based

on the selected date range.

AccessOne Reporting API Specifications

Page **130** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

\+ **Contraints**:

**Pre-**

**conditions**

\-

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\-

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

**conditions**

Return daily submitted TIN matching summary data of hierarchy entity choice(s) based

on the selected date range.

·

TaxReportDailySubmittedDetail:

**Response**

**Data**

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

City

Contact

CorporateName

Description

IRSName

Last4TIN

Matched

MerchantName

MerchantNumber

Phone

ReportDate

RowNumber

State

TIN

TotalRows

ValidationResponseCode

Zip

·

·

Total

Paging

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetTaxReportDailyS

ubmittedDetailByEntit

**SAMPLE RESPONSE:**

AccessOne Reporting API Specifications

Page **131** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





GetTaxReportDailyS

ubmittedDetailByEntit

**REST API**

**Request URL** /rest/GetTaxReportDailySubmittedDetailByEntity

**Method**

POST

**Request**

**Body Sample**

**XML**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2000-05-31T11:20:00</FromDate>

<HierarchyFilterMode>Platform</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-10-20T11:20:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetTaxReportDailySubmittedDetailByEntity\_RestRespone.xml

GetTaxReportDailySubmittedDetailByMerchant

**Service Operation** GetTaxReportDailySubmittedDetailByMerchant ()

**Name**

GetTaxReportDailySubmittedDetailByMerchant.

Return daily submitted TIN matching detail data of the selected merchant number.

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**Description**

**Pre-**

**conditions**

**Post-**

Return daily submitted TIN matching detail data of the selected merchant number.

**conditions**

·

TaxReportDailySubmittedDetail:

**Response**

**Data**

o

o

o

o

City

Contact

CorporateName

Description

AccessOne Reporting API Specifications

Page **132** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

o

o

o

o

o

o

o

o

o

o

o

IRSName

Last4TIN

Matched

MerchantName

MerchantNumber

Phone

ReportDate

RowNumber

State

TIN

TotalRows

ValidationResponseCode

Zip

·

·

Total

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetTaxReportDailyS

ubmittedDetailByMerc

**SAMPLE RESPONSE:**

GetTaxReportDailyS

ubmittedDetailByMerc

**REST API**

**Request URL** /rest/GetTaxReportDailySubmittedDetailByMerchant

**Method**

POST

**Request**

**Body Sample**

**XML**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2000-05-31T11:20:00</FromDate>

<MerchantNumber>512888888888051</MerchantNumber>

AccessOne Reporting API Specifications

Page **133** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<PageSize>10</PageSize>

<ToDate>2019-10-20T11:20:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetTaxReportDailySubmittedDetailByMerchant\_RestRespone.xml

GetTaxReportMonthlyInvalidSummaryByEntity

**Service Operation** GetTaxReportMonthlyInvalidSummaryByEntity ()

**Name**

GetTaxReportMonthlyInvalidSummaryByEntity.

**Description**

Return monthly invalid summary tax data of hierarchy entity choice(s) based on the

selected date range.

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**Pre-**

**conditions**

**Name**

HierarchyFilterMode

**Require/Default**

HierarchyFilterValue

FromDate

ToDate

True

True

True

YearMonth

CurrentPageIndex

PageSize

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return monthly invalid summary tax report.

**conditions**

·

TaxReportMonthlyInvalidSummary

**Response**

**Data**

o

o

o

o

o

Entity

MatchedMerchantCount

MerchantCount

NotMatchedMerchantCount

RowNumber

AccessOne Reporting API Specifications

Page **134** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

Total:

TotalRows

·

·

o

o

o

o

o

o

Entity

MatchedMerchantCount

MerchantCount

NotMatchedMerchantCount

RowNumber

TotalRows

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetTaxReportMonthl

yInvalidSummaryByEn

**SAMPLE RESPONSE:**

GetTaxReportMonthl

yInvalidSummaryByEn

**REST API**

**Request URL** /rest/GetTaxReportMonthlyInvalidSummaryByEntity

**Method**

POST

**Request**

**Body Sample**

**XML**

<GenericReportMonthlyFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<HierarchyFilterMode>HeadquarterMerchantNumber</HierarchyFilterMode>

<HierarchyFilterValue>512888888888051</HierarchyFilterValue>

<PageSize>10</PageSize>

<ViewLevel>None</ViewLevel>

<YearMonth>201009</YearMonth>

</GenericReportMonthlyFilter>

AccessOne Reporting API Specifications

Page **135** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Request**

**Response**

**Sample XML**

GetTaxReportMonthlyInvalidSummaryByEntity\_RestResponse.xml

GetTaxReportMonthlyInvalidSummaryByMerchant

**Service Operation** GetTaxReportMonthlyInvalidSummaryByMerchant()

**Name**

GetTaxReportMonthlyInvalidSummaryByMerchant.

**Description**

Return monthly invalid summary tax data of the selected merchant number.

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18)[**)\]**](#br18)**

**Pre-**

**conditions**

**Name**

**Require/Default**

FromDate

ToDate

MerchantNumber

True

True

True

TRue

YearMonth

CurrentPageIndex

PageSize

Return monthly invalid summary tax report.

**Post-**

**conditions**

**SOAP API**

**Sample Files SAMPLE REQUEST:**

GetTaxReportMonthl

yInvalidSummaryByMe

**SAMPLE RESPONSE:**

GetTaxReportMonthl

yInvalidSummaryByMe

**REST API**

**Request URL** /rest/GetTaxReportMonthlyInvalidSummaryByMerchant

AccessOne Reporting API Specifications

Page **136** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Method**

POST

**Request**

**Body Sample**

**XML**

<MerchantReportMonthlyFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<MerchantNumber>518564380203646</MerchantNumber>

<PageSize>1</PageSize>

<YearMonth>201009</YearMonth>

</MerchantReportMonthlyFilter>

**Request**

**Response**

**Sample XML**

GetTaxReportMonthlyInvalidSummaryByMerchant\_RestResponse.xml

GetTaxReportMonthlyInvalidDetailByEntity

**Service Operation** GetTaxReportMonthlyInvalidDetailByEntity()

**Name**

GetTaxReportMonthlyInvalidDetailByEntity.

**Description**

Return monthly invalid detail tax data of hierarchy entity choice(s) based on the

selected date range.

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**Pre-**

**conditions**

\+ **Contraints**:

\-

\-

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return monthly invalid hierarchy detail tax report.

**conditions**

·

TaxReportMonthlyInvalidDetail:

**Response**

**Data**

o

o

o

o

o

o

o

o

o

o

o

City

Contact

CorporateName

Description

IRSName

Last4TIN

Matched

MerchantName

MerchantNumber

Phone

ReportDate

AccessOne Reporting API Specifications

Page **137** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

o

o

o

o

o

RowNumber

State

TIN

TotalRows

ValidationDate

ValidationResponseCode

Zip

·

·

Total

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetTaxReportMonthl

yInvalidDetailByEntity

**SAMPLE RESPONSE:**

GetTaxReportMonthl

yInvalidDetailByEntity

**REST API**

**Request URL** /rest/GetTaxReportMonthlyInvalidDetailByEntity

**Method**

POST

**Request**

**Body Sample**

**XML**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-31T11:20:00</FromDate>

<HierarchyFilterMode>Platform</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-10-27T11:20:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

AccessOne Reporting API Specifications

Page **138** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Request**

**Response**

**Sample XML**

GetTaxReportMonthlyInvalidDetailByEntity\_RestResponse.xml

GetTaxReportMonthlyInvalidDetailByMerchant

**Service Operation** GetTaxReportMonthlyInvalidDetailByMerchant()

**Name**

GetTaxReportMonthlyInvalidDetailByMerchant.

Return monthly invalid detail tax data of the selected merchant number.

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**Description**

**Pre-**

**conditions**

**Post-**

Return monthly invalid detail tax data of the selected merchant number.

**conditions**

·

TaxReportMonthlyInvalidDetail:

**Response**

**Data**

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

City

Contact

CorporateName

Description

IRSName

Last4TIN

Matched

MerchantName

MerchantNumber

Phone

ReportDate

RowNumber

State

TIN

TotalRows

ValidationDate

ValidationResponseCode

Zip

·

·

Total

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

AccessOne Reporting API Specifications

Page **139** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetTaxReportMonthl

yInvalidDetailByMerch

**SAMPLE RESPONSE:**

GetTaxReportMonthl

yInvalidDetailByMerch

**REST API**

**Request URL** /rest/GetTaxReportMonthlyInvalidDetailByMerchant

**Method**

POST

**Request**

**Body Sample**

**XML**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-01-31T11:20:00</FromDate>

<MerchantNumber>02550630018</MerchantNumber>

<PageSize>10</PageSize>

<ToDate>2019-10-27T11:20:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetTaxReportMonthlyInvalidDetailByMerchant\_RestResponse.xml

GetTaxReportAdhoc

**Service Operation** GetTaxReportAdhoc()

GetTaxReportAdhoc

Return TIN Matching Ad-hoc report.

\+ **Parameters:**

**Name**

**Description**

**Pre-**

**conditions**

AccessOne Reporting API Specifications

Page **140** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Name**

HierarchyFilterMode

**Require/Default/Value**

HierarchyFilterValue

FromDate

ToDate

True

True

01,02,03,04

InvalidValidationCode

MatchAllFilters

OtherValidationCode

SelectedDate

05,88,66

ValidValidationCode

CurrentPageIndex

PageSize

00,06,07,08

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return TIN Matching Ad-hoc report.

**conditions**

·

TaxReportAdhoc:

**Response**

**Data**

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

AGENT

Chain

ChainID

City

ClientName

Contact

HeadquarterMerchantNumber

Last4TIN

LastReportDate

MasterChain

MasterSalesAgent

MatchedStatus

MerchantChain

MerchantName

MerchantNumber

NAgent

NBank

NBusiness

NCorp

NSalesAgent

AccessOne Reporting API Specifications

Page **141** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

o

o

o

o

o

o

o

o

o

o

o

PRIN

Phone

RowNumber

SYS

SalesAgent

SalesmanNo

State

TIN

TotalRows

ValidationDate

ValidationResponseCode

ValidationResponseCodeDesc

Zip

·

·

Total

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetTaxReportAdhoc

\_Request.xml

**SAMPLE RESPONSE:**

GetTaxReportAdhoc

\_Response.xml

**REST API**

**Request URL** /rest/GetTaxReportAdhoc

**Method**

POST

**Request**

**Body Sample**

**XML**

<TaxReportAdhocFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2019-10-01T11:20:00</FromDate>

AccessOne Reporting API Specifications

Page **142** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<HierarchyFilterMode>Platform</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-10-28T11:20:00</ToDate>

<ViewLevel>None</ViewLevel>

<InvalidValidationCode></InvalidValidationCode>

<MatchAllFilters>true</MatchAllFilters>

<OtherValidationCode></OtherValidationCode>

<SelectedDate></SelectedDate>

<ValidValidationCode></ValidValidationCode>

</TaxReportAdhocFilter>

**Request**

**Response**

**Sample XML**

GetTaxReportAdhoc\_RestResponse.xml

GetMonetaryRejectsByEntity

**Service Operation** GetMonetaryRejectsByEntity()

**Name**

GetMonetaryRejectsByEntity.

Return Monetary Rejects summary report.

**Description**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**Pre-**

**conditions**

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return Monetary Rejects summary report.

**conditions**

·

MonetaryRejectsDataSummary

**Response**

**Data**

o

o

o

o

o

o

o

o

Hierarchy

MerchantName

MerchantNumber

MonetaryRejectAmount

MonetaryRejectCount

Platform

RowNumber

TotalRows

·

Total

AccessOne Reporting API Specifications

Page **143** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

o

o

o

o

o

o

Hierarchy

MerchantName

MerchantNumber

MonetaryRejectAmount

MonetaryRejectCount

Platform

RowNumber

TotalRows

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetMonetaryRejects

ByEntity\_Request.xm

**SAMPLE RESPONSE:**

GetMonetaryRejects

ByEntity\_Response.x

**REST API**

**Request URL** /rest/GetMonetaryRejectsByEntity

**Method**

POST

**Request**

**Body Sample**

**XML**

<GenericReportFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-31T11:20:00</FromDate>

<HierarchyFilterMode>Platform</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

<ViewLevel>None</ViewLevel>

</GenericReportFilter>

**Request**

**Response**

**Sample XML**

GetMonetaryRejectsByEntity\_RestResponse.xml

AccessOne Reporting API Specifications

Page **144** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





GetMonetaryRejectsByMerchant

**Service Operation** GetMonetaryRejectsByMerchant()

**Name**

GetMonetaryRejectsByMerchant.

**Description**

Return Monetary Rejects report in detail.

**Pre-**

**conditions**

\+ **Parameters: [[Ref(**](#br18)[**III.3.2](#br18))]**

**Post-**

Return Monetary Rejects report in detail.

**conditions**

·

MonetaryRejectsDetail

**Response**

**Data**

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

o

AccountNumber

Action

ActionCode

AuthorizationNumber

CardDescription

CardType

EntryModeDescription

FileSource

Keyed

ReasonCode

ReasonCodeDescription

ReportDate

TotalRows

TransactionAmount

TransactionCode

TransactionDate

TransactionDescription

TransactionTime

·

Total

o

o

o

o

o

o

o

o

o

o

o

AccountNumber

Action

ActionCode

AuthorizationNumber

CardDescription

CardType

EntryModeDescription

FileSource

Keyed

ReasonCode

ReasonCodeDescription

AccessOne Reporting API Specifications

Page **145** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

o

o

o

o

o

ReportDate

TotalRows

TransactionAmount

TransactionCode

TransactionDate

TransactionDescription

TransactionTime

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetMonetaryRejects

ByMerchant\_Request

**SAMPLE RESPONSE:**

GetMonetaryRejects

ByMerchant\_Respons

**REST API**

**Request URL** /rest/GetMonetaryRejectsByMerchant

**Method**

POST

**Request**

**Body Sample**

**XML**

<MerchantSummaryFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-31T11:20:00</FromDate>

<MerchantNumber>518564380158899</MerchantNumber>

<PageSize>10</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

</MerchantSummaryFilter>

**Request**

**Response**

**Sample XML**

GetMonetaryRejectsByMerchant\_RestResponse.xml

GetRejectETCFrontEndEditExceptionsByEntity

**Service Operation** GetRejectETCFrontEndEditExceptionsByEntity()

AccessOne Reporting API Specifications

Page **146** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Name**

GetRejectETCFrontEndEditExceptionsByEntity.

**Description**

Return ETC Front End Edit Exceptions (CD-016) data of the entity choices based on the

selected date range.

**Pre-**

\+ **Parameters: [[Ref(**](#br18)[**III.3.1](#br18)[**)\]**](#br18)**

**conditions**

**Name**

HierarchyFilterMode

**Require/Default**

HierarchyFilterValue

FromDate

ToDate

True

True

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

<Empty> à All

DEBIT REVERSAL

DUPLICATE TRANSACTION

INVALID CARDHOLDER

ReasonFilterValue

INVALID DOLLAR AMOUNT

INVALID MERCHANT ID

NOT ON DESCRIPTION FILE

DUPLICATE TRANSACTION

OVERFLOW OF THE REV TABLE

NOT SET UP FOR CLOSE

OVERFLOW OF THE VOID TABLE

POSTED/RE-ENTERED TRANS

POSTED REVERSAL

RETURN INVALID/CASH ADV

REVERSAL – COMM ERROR

UNMATCHED-NO POSTING

UNMATCHED REVER/POSTED

VALID REVERSED TRANS

INVALID CARD TYPE

CurrentPageIndex

ViewLevel

PageSize

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

AccessOne Reporting API Specifications

Page **147** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Post-**

Return ETC Front End Edit Exceptions (CD-016) Hierarchy report.

**conditions**

·

ETCFrontEndEditExceptionsByEntity:

**Response**

**Data**

o

Entity

EntityName

o

o

o

RowNumber

TotalRows

o

o

TransactionAmount

TransactionCount

·

Total:

o

o

Entity

EntityName

o

o

RowNumber

TotalRows

o

TransactionAmount

TransactionCount

o

Paging:

o

·

·

CurrentPageIndex

PageSize

o

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetRejectETCFrontE

ndEditExceptionsByEn

**SAMPLE RESPONSE:**

GetRejectETCFrontE

ndEditExceptionsByEn

**REST API**

**Request URL** /rest/GetRejectETCFrontEndEditExceptionsByEntity

**Method**

POST

**Request**

**Body Sample**

**XML**

<MonetaryRejectsFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2000-05-31T11:20:00</FromDate>

AccessOne Reporting API Specifications

Page **148** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<HierarchyFilterMode>Platform</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

<ReasonFilterValue></ReasonFilterValue>

<ViewLevel>None</ViewLevel>

</MonetaryRejectsFilter>

**Request**

**Response**

**Sample XML**

GetRejectETCFrontEndEditExceptionsByEntity\_RestResponse.xml

GetRejectETCFrontEndEditExceptionsByMerchant

**Service Operation** GetRejectETCFrontEndEditExceptionsByMerchant()

**Name**

GetRejectETCFrontEndEditExceptionsByMerchant.

**Description**

Return ETC Front End Edit Exceptions (CD-016) data of selected merchant number .

\+ **Parameters:**

**Pre-**

**Name**

**Require/Default**

**conditions**

FromDate

ToDate

True

True

True

MerchantNumber

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

<Empty> à All

DEBIT REVERSAL

DUPLICATE TRANSACTION

INVALID CARDHOLDER

INVALID DOLLAR AMOUNT

INVALID MERCHANT ID

NOT ON DESCRIPTION FILE

DUPLICATE TRANSACTION

OVERFLOW OF THE REV TABLE

NOT SET UP FOR CLOSE

OVERFLOW OF THE VOID TABLE

POSTED/RE-ENTERED TRANS

POSTED REVERSAL

RETURN INVALID/CASH ADV

REVERSAL – COMM ERROR

UNMATCHED-NO POSTING

UNMATCHED REVER/POSTED

ReasonFilterValue

AccessOne Reporting API Specifications

Page **149** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





·

·

VALID REVERSED TRANS

INVALID CARD TYPE

CurrentPageIndex

PageSize

**Post-**

**conditions**

Return ETC Front End Edit Exceptions (CD-016) Hierarchy report.

ETCFrontEndEditExceptionsByMerchant:

·

·

·

**Response**

**Data**

o

o

o

o

o

o

o

o

AccountNumber

AuthorizationNumber

PartialCardNumber

ReasonCode

ReasonDescription

RecordID

ReportDate

TotalRows

TransactionAmount

TransactionDate

TransactionTime

o

o

o

Total:

o

o

o

o

o

o

o

o

AccountNumber

AuthorizationNumber

PartialCardNumber

ReasonCode

ReasonDescription

RecordID

ReportDate

TotalRows

TransactionAmount

TransactionDate

TransactionTime

o

o

o

Paging

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

AccessOne Reporting API Specifications

Page **150** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





GetRejectETCFrontE

ndEditExceptionsByMe

**SAMPLE RESPONSE:**

GetRejectETCFrontE

ndEditExceptionsByMe

**REST API**

**Request URL** /rest/GetRejectETCFrontEndEditExceptionsByMerchant

**Method**

POST

**Request**

**Body Sample**

**XML**

<MerchantMonetaryRejectsFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-31T11:20:00</FromDate>

<MerchantNumber>518564380158899</MerchantNumber>

<PageSize>10</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

<ReasonFilterValue></ReasonFilterValue>

</MerchantMonetaryRejectsFilter>

**Request**

**Response**

**Sample XML**

GetRejectETCFrontEndEditExceptionsByMerchant\_RestResponse.xml

GetTapeTransmittalRejectsByEntity

**Service Operation** GetTapeTransmittalRejectsByEntity()

**Name**

GetTapeTransmittalRejectsByEntity.

**Description**

Return Tape Transmittal Rejects (CD-1430) data of the entity choices based on the

selected date range,

\+ **Parameters:**

**Pre-**

**conditions**

**Name**

HierarchyFilterMode

HierarchyFilterValue

**Require/Default**

AccessOne Reporting API Specifications

Page **151** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





FromDate

ToDate

True

True

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

<Empty> à ALL

ReasonFilterValue

BNK HDR - INVALID DATELL

HDR/TRLR SYS/PRIN MISMATCH

INVALID COUNTRY CODE

INVALID DETAIL COUNT

INVALID NET AMOUNT

INVALID PRINCIPAL BANK

INVALID SYSTEM NUMBER

NO GOOD BATCHES THIS LETTER

NON NUMERIC DETAIL COUNT

NON NUMERIC NET AMOUNT

REJ TAPE IND=Y BATCH REJ

TOO MANY DUPLICATE BATCHES

TRAN TYPE INV/PURCH BIN

MISSING BANK TRAILER

BANK BATCH MISMATCH

CURRENCY CODE MISMATCH

DUPLICATE BATCH

DUP. BATCH - ON SAME TAPE

HDR/TRLR MERCH # MISMATCH

INVALID DETAIL COUNT

INVALID FORMAT FOR RETAIL

INVALID MERCHANT MEDIA

INVALID MERCHANT NUMBER

INVALID NET AMOUNT

MERCHANT NOT ON FILE

MISSING BATCH TRAILER REC

NON NUMERIC DETAIL COUNT

NON NUMERIC NET AMOUNT

AMOUNT TOO LARGE

CHD NOT ACCEPTD BY MRC

CURRENCY CODE MISMATCH

INVALID CARDHOLDER NUMBER

INVALID CHD ID METHOD

INVALID DEPT CODE

INVLD DEP TYPE W ADDEN

INVALID FOREIGN AMOUNT

INVALID MERCHANT

DESCRIPTION

INVALID RECORD CODE

·

AccessOne Reporting API Specifications

Page **152** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





·

·

·

·

·

·

·

·

·

·

·

INVALID TRAN AMOUNT

INVALID TRAN CODE

INVALID TRAN DATE

MISMATCHED CODES

MISSING ADDENDA RECORD

MISSING TERMS RECORD

NON NUMERIC TRAN ID

UNEXPECTED ADDENDA RECORD

NO REJECTED TRANSACTIONS

DUPLICATE TRAN

PTS EDIT PENDED

CurrentPageIndex

PageSize

\+ **Contraints**:

[HierarchyFilterMode](#br14)[ ](#br14)must be belong to group **[Ref[**(](#br14)[II.3.1](#br14)[)](#br14)]**

\+ **Notes**: **[[Ref(**](#br19)[**III.5.1](#br19)[**)\]**](#br19)**

**Post-**

Return Tape Transmittal Rejects (CD-1430) Hierarchy report.

**conditions**

·

·

·

·

·

·

·

·

·

·

·

·

·

Entity

**Response**

**Data**

EntityName

RowNumber

TotalRows

TransactionCount

TransactionAmount

Total:

Entity

EntityName

RowNumber

TotalRows

TransactionCount

TransactionAmount

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetTapeTransmittalR

ejectsByEntity\_Reque

AccessOne Reporting API Specifications

Page **153** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**SAMPLE RESPONSE:**

GetTapeTransmittalR

ejectsByEntity\_Respo

**REST API**

**Request URL** /rest/GetTapeTransmittalRejectsByEntity

**Method**

POST

**Request**

**Body Sample**

**XML**

<MonetaryRejectsFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-31T11:20:00</FromDate>

<HierarchyFilterMode>Platform</HierarchyFilterMode>

<HierarchyFilterValue></HierarchyFilterValue>

<PageSize>10</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

<ReasonFilterValue></ReasonFilterValue>

<ViewLevel>None</ViewLevel>

</MonetaryRejectsFilter>

**Request**

**Response**

**Sample XML**

GetTapeTransmittalRejectsByEntity\_RestResponse.xml

GetTapeTransmittalRejectsByMerchant

**Service Operation** GetTapeTransmittalRejectsByMerchant ()

**Name**

GetTapeTransmittalRejectsByMerchant.

**Description**

Return Tape Transmittal Rejects (CD-1430) data of selected merchant number.

\+ **Parameters:**

**Pre-**

**conditions**

**Name**

**Require/Default**

FromDate

ToDate

MerchantNumber

True

True

True

·

<Empty> à ALL

AccessOne Reporting API Specifications

Page **154** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





ReasonFilterValue

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

·

BNK HDR - INVALID DATELL

HDR/TRLR SYS/PRIN MISMATCH

INVALID COUNTRY CODE

INVALID DETAIL COUNT

INVALID NET AMOUNT

INVALID PRINCIPAL BANK

INVALID SYSTEM NUMBER

NO GOOD BATCHES THIS LETTER

NON NUMERIC DETAIL COUNT

NON NUMERIC NET AMOUNT

REJ TAPE IND=Y BATCH REJ

TOO MANY DUPLICATE BATCHES

TRAN TYPE INV/PURCH BIN

MISSING BANK TRAILER

BANK BATCH MISMATCH

CURRENCY CODE MISMATCH

DUPLICATE BATCH

DUP. BATCH - ON SAME TAPE

HDR/TRLR MERCH # MISMATCH

INVALID DETAIL COUNT

INVALID FORMAT FOR RETAIL

INVALID MERCHANT MEDIA

INVALID MERCHANT NUMBER

INVALID NET AMOUNT

MERCHANT NOT ON FILE

MISSING BATCH TRAILER REC

NON NUMERIC DETAIL COUNT

NON NUMERIC NET AMOUNT

AMOUNT TOO LARGE

CHD NOT ACCEPTD BY MRC

CURRENCY CODE MISMATCH

INVALID CARDHOLDER NUMBER

INVALID CHD ID METHOD

INVALID DEPT CODE

INVLD DEP TYPE W ADDEN

INVALID FOREIGN AMOUNT

INVALID MERCHANT

DESCRIPTION

INVALID RECORD CODE

INVALID TRAN AMOUNT

INVALID TRAN CODE

INVALID TRAN DATE

·

·

·

·

AccessOne Reporting API Specifications

Page **155** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





·

·

·

·

·

·

·

·

MISMATCHED CODES

MISSING ADDENDA RECORD

MISSING TERMS RECORD

NON NUMERIC TRAN ID

UNEXPECTED ADDENDA RECORD

NO REJECTED TRANSACTIONS

DUPLICATE TRAN

PTS EDIT PENDED

CurrentPageIndex

PageSize

**Post-**

Return Tape Transmittal Rejects (CD-1430) report.

**conditions**

· TapeTransmittalRejectsByMerchant:

**Response**

**Data**

o

o

AccountNumber

AuthorizationNumber

CardDescription

CardType

o

o

o

o

o

o

Keyed

KeyedDescription

PartialCardNumber

ReasonCode

o

o

ReasonDescription

RecordID

o

o

ReportDate

TotalRows

o

o

o

o

TransactionAmount

TransactionCode

TransactionDate

TransactionDescription

·

Total:

o

o

o

o

AccountNumber

AuthorizationNumber

CardDescription

CardType

o

o

o

o

Keyed

KeyedDescription

PartialCardNumber

ReasonCode

o

o

ReasonDescription

RecordID

o

o

ReportDate

TotalRows

o

TransactionAmount

AccessOne Reporting API Specifications

Page **156** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





o

o

TransactionCode

TransactionDate

o

TransactionDescription

·

Paging:

o

o

o

CurrentPageIndex

PageSize

NumberOfRecords

**SOAP API**

**Message**

**Exchange**

**Pattern**

**SAMPLE REQUEST:**

GetTapeTransmittalR

ejectsByMerchant\_Re

**SAMPLE RESPONSE:**

GetTapeTransmittalR

ejectsByMerchant\_Re

**REST API**

**Request URL** /rest/GetTapeTransmittalRejectsByMerchant

**Method**

POST

**Request**

**Body Sample**

**XML**

<MerchantMonetaryRejectsFilter xmlns="http://api.lonestar.com/types">

<CurrentPageIndex>1</CurrentPageIndex>

<FromDate>2010-05-31T11:20:00</FromDate>

<MerchantNumber>518564380158899</MerchantNumber>

<PageSize>10</PageSize>

<ToDate>2019-05-31T11:20:00</ToDate>

<ReasonFilterValue></ReasonFilterValue>

</MerchantMonetaryRejectsFilter>

**Request**

**Response**

**Sample XML**

GetTapeTransmittalRejectsByMerchant\_RestResponse.xml

AccessOne Reporting API Specifications

Page **157** of **157**

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.

