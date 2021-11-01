

**NORTH BOARDING API SPECIFICATIONS**

1





**1 Table of Contents**

[**1**](#br2)

[**2**](#br4)

[**Table**](#br2)[** ](#br2)[of**](#br2)[** ](#br2)[Contents**](#br2)[** ](#br2)[...............................................................................................................2**](#br2)

[**Introduction.......................................................................................................................4**](#br4)

[2.1.](#br4)[ ](#br4)[Intended](#br4)[ ](#br4)[Audience](#br4)[ ](#br4)[............................................................................................................................](#br4)[ ](#br4)[4](#br4)

[2.2.](#br4)[ ](#br4)[Project](#br4)[ ](#br4)[Scope](#br4)[ ](#br4)[....................................................................................................................................](#br4)[ ](#br4)[4](#br4)

[**3.**](#br5)

[**Technical**](#br5)[** ](#br5)[Specifications.....................................................................................................5**](#br5)

[3.1.](#br5)[ ](#br5)[Boarding](#br5)[ ](#br5)[API](#br5)[ ](#br5)[Methods.......................................................................................................................](#br5)[ ](#br5)[5](#br5)

[3.1.1.](#br5)[ ](#br5)[SubmitMPA](#br5)[ ](#br5)[..........................................................................................................................................](#br5)[ ](#br5)[5](#br5)

[3.1.2.](#br7)[ ](#br7)[GetStatusByTimeSpan](#br7)[ ](#br7)[.........................................................................................................................](#br7)[ ](#br7)[7](#br7)

[3.2.](#br10)[ ](#br10)[XML](#br10)[ ](#br10)[Format](#br10)[ ](#br10)[....................................................................................................................................](#br10)[ ](#br10)[10](#br10)

[3.3.](#br11)[ ](#br11)[Validation](#br11)[ ](#br11)[Handler............................................................................................................................11](#br11)

[3.4.](#br21)[ ](#br21)[MPA](#br21)[ ](#br21)[Status](#br21)[ ](#br21)[Report](#br21)[ ](#br21)[..........................................................................................................................](#br21)[ ](#br21)[21](#br21)

[3.5.](#br23)[ ](#br23)[Boarding](#br23)[ ](#br23)[Process.............................................................................................................................](#br23)[ ](#br23)[23](#br23)

[**4.**](#br24)

[**SOAP**](#br24)[** ](#br24)[Security**](#br24)[** ](#br24)[Guide**](#br24)[** ](#br24)[........................................................................................................24**](#br24)

[4.1.](#br24)[ ](#br24)[Connectivity](#br24)[ ](#br24)[Verification](#br24)[ ](#br24)[via](#br24)[ ](#br24)[SOAP](#br24)[ ](#br24)[UI](#br24)[ ](#br24)[..................................................................................................](#br24)[ ](#br24)[24](#br24)

[4.1.1.](#br24)[ ](#br24)[Prerequisite](#br24)[ ](#br24)[Checks](#br24)[ ](#br24)[............................................................................................................................](#br24)[ ](#br24)[24](#br24)

[4.1.2.](#br24)[ ](#br24)[Configure](#br24)[ ](#br24)[SOAP](#br24)[ ](#br24)[UI](#br24)[ ](#br24)[.............................................................................................................................](#br24)[ ](#br24)[24](#br24)

[4.1.3.](#br31)[ ](#br31)[Submit](#br31)[ ](#br31)[SOAP](#br31)[ ](#br31)[Requests........................................................................................................................31](#br31)

[4.2.](#br34)[ ](#br34)[Connectivity](#br34)[ ](#br34)[Verification](#br34)[ ](#br34)[via](#br34)[ ](#br34)[Other](#br34)[ ](#br34)[Platforms](#br34)[ ](#br34)[..................................................................................](#br34)[ ](#br34)[34](#br34)

[4.2.1.](#br35)[ ](#br35)[SOAP](#br35)[ ](#br35)[Request](#br35)[ ](#br35)[Header........................................................................................................................](#br35)[ ](#br35)[35](#br35)

[4.2.2.](#br37)[ ](#br37)[SOAP](#br37)[ ](#br37)[Request](#br37)[ ](#br37)[Body............................................................................................................................37](#br37)

[4.3.](#br38)[ ](#br38)[Common](#br38)[ ](#br38)[Connectivity](#br38)[ ](#br38)[Issues...........................................................................................................](#br38)[ ](#br38)[38](#br38)

[4.3.1.](#br38)[ ](#br38)[Common](#br38)[ ](#br38)[issue](#br38)[ ](#br38)[#1:](#br38)[ ](#br38)[Generic](#br38)[ ](#br38)[Error.........................................................................................................](#br38)[ ](#br38)[38](#br38)

[4.3.2.](#br39)[ ](#br39)[Common](#br39)[ ](#br39)[issue](#br39)[ ](#br39)[#2:](#br39)[ ](#br39)[Submission](#br39)[ ](#br39)[failure](#br39)[ ](#br39)[................................................................................................](#br39)[ ](#br39)[39](#br39)

[4.3.3.](#br39)[ ](#br39)[Common](#br39)[ ](#br39)[issue](#br39)[ ](#br39)[#3:](#br39)[ ](#br39)[Submission](#br39)[ ](#br39)[failure](#br39)[ ](#br39)[without](#br39)[ ](#br39)[specific](#br39)[ ](#br39)[errors..............................................................](#br39)[ ](#br39)[39](#br39)

[**5**](#br40)

[**Basic**](#br40)[** ](#br40)[Verification**](#br40)[** ](#br40)[Guides**](#br40)[** ](#br40)[.................................................................................................40**](#br40)

[6.1.](#br41)[ ](#br41)[Preparations](#br41)[ ](#br41)[....................................................................................................................................](#br41)[ ](#br41)[41](#br41)

[6.1.1.](#br41)[ ](#br41)[Permission](#br41)[ ](#br41)[Settings](#br41)[ ](#br41)[............................................................................................................................](#br41)[ ](#br41)[41](#br41)

[6.1.2.](#br41)[ ](#br41)[MPA](#br41)[ ](#br41)[as](#br41)[ ](#br41)[XML](#br41)[ ](#br41)[File.................................................................................................................................](#br41)[ ](#br41)[41](#br41)

[6.1.3.](#br42)[ ](#br42)[XML](#br42)[ ](#br42)[Elements](#br42)[ ](#br42)[Ordering......................................................................................................................](#br42)[ ](#br42)[42](#br42)

North Boarding API Specifications.docxSpecifications

Page 2 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





[6.1.4.](#br43)[ ](#br43)[Unspecified](#br43)[ ](#br43)[MPA](#br43)[ ](#br43)[Fields](#br43)[ ](#br43)[......................................................................................................................](#br43)[ ](#br43)[43](#br43)

[6.1.5.](#br44)[ ](#br44)[Using](#br44)[ ](#br44)[Master](#br44)[ ](#br44)[Mapping........................................................................................................................](#br44)[ ](#br44)[44](#br44)

[6.1.6.](#br44)[ ](#br44)[Starting](#br44)[ ](#br44)[XML](#br44)[ ](#br44)[File................................................................................................................................](#br44)[ ](#br44)[44](#br44)

[6.2.](#br44)[ ](#br44)[Merchant](#br44)[ ](#br44)[Application](#br44)[ ](#br44)[Submission](#br44)[ ](#br44)[...................................................................................................](#br44)[ ](#br44)[44](#br44)

[6.2.1.](#br44)[ ](#br44)[High-level](#br44)[ ](#br44)[Test](#br44)[ ](#br44)[Cases..........................................................................................................................](#br44)[ ](#br44)[44](#br44)

[6.2.3.](#br52)[ ](#br52)[Common](#br52)[ ](#br52)[Issues](#br52)[ ](#br52)[..................................................................................................................................](#br52)[ ](#br52)[52](#br52)

[6.3.](#br54)[ ](#br54)[Post-Merchant](#br54)[ ](#br54)[Submission..............................................................................................................](#br54)[ ](#br54)[54](#br54)

[6.3.1.](#br54)[ ](#br54)[Front-End](#br54)[ ](#br54)[Data...................................................................................................................................](#br54)[ ](#br54)[54](#br54)

[6.3.2.](#br54)[ ](#br54)[Exported](#br54)[ ](#br54)[PDFs....................................................................................................................................](#br54)[ ](#br54)[54](#br54)

[6.4.](#br54)[ ](#br54)[MPA](#br54)[ ](#br54)[Status](#br54)[ ](#br54)[Tracking](#br54)[ ](#br54)[.......................................................................................................................](#br54)[ ](#br54)[54](#br54)

[**7.**](#br59)

[**Frequently**](#br59)[** ](#br59)[Asked**](#br59)[** ](#br59)[Questions**](#br59)[** ](#br59)[............................................................................................59**](#br59)

North Boarding API Specifications.docxSpecifications

Page 3 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**2 Introduction**

**2.1. INTENDED AUDIENCE**

This document is intended for developers, project managers, and QA testers. It is

recommended that the document be read in full in order to understand the functionality of

each section and how one relates to another.

This document is primarily intended for software developers with sufficient technical

background. Non-technical readers are encouraged to read the document as it might greatly

support them in the verification process of North FACS API.

It is suggested the document be read in its entirety for a full-fledged understanding of how

North Boarding FACS API receives and answers to SOAP web service calls.

Due to the sensitivity of the information included in this document, under no circumstances

must this document be disclosed to any parties that are not directly involved in the testing or

using North FACS API.

**2.2. PROJECT SCOPE**

This project was initiated for the purpose of creating North FACS Inbound API – a Web

Service which will allow First Data to programmatically submit standard MPAs and retrieve

the submitted MPAs’ Processing Statuses.

This document covers the use of the API and describe the business logic on how to

successfully submit the MPAs and retrieve the statuses.

North Boarding API Specifications.docxSpecifications

Page 4 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**3. Technical Specifications**

Boarding API Web Service provides two methods for the Client to submit the MPAs to Fiserv

database and retrieve the status updates after the MPAs have been successfully submitted.

Below is the architecture of the Boarding API Web Service that will be consumed by the Client

System.

See attached documents “North FACSAPI\_XMLSchema\_V1.0.xsd” and “North

FACSAPI\_V1.0.wsdl” for technical implementation details.

The business requirements are identified in the following sections.

**3.1. BOARDING API METHODS**

The Web Service Name is NorthASBoardingAPIService.

**3.1.1.SubmitMPA**

This method allows the Client System to send MPA data to Boarding API. The following

diagram illustrates the business flow inside the method.

North Boarding API Specifications.docxSpecifications

Page 5 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Validation Handler

Schema Validation

FD Calls SubmitMPA

Method

API ready to

receive the call?

API receives MPA’s XML

YES

Content

Conditional Data Logic Validation

Store the received XML

message and error detail to

Boarding\_APIErrorLog

The XML Content

passes all

validation?

API sends FAILURE with detailed

error message.

NO

YES

API sends SUCCESS return

message

Store the XML message to

the Boarding\_APILog

Store the MPA data to MPA

tables

Details of the method are as follows:

Web Method Name: SubmitMPA.

Input Parameters:

**Name**

**Data Type Type Category Description**

XMLContent

String

simpleType

This xml has the merchant data from the Client System. Details are in

[MPA](#br10)[ ](#br10)[XML](#br10)[ ](#br10)[FORMAT](#br10)[ ](#br10)section.

ExtRefID

String

simpleType

simpleType

Unique sequence generated by the Client System.

NorthChannel String

Channel indicator. Can be FACS or FDS

Note that the user credentials will be passed along with the request on the SOAP Header and

are identified in [Section](#br24)[ ](#br24)[5](#br24)[ ](#br24)[SOAP](#br24)[ ](#br24)[Security](#br24)[ ](#br24)[Guide](#br24)

**Transmissions & Response**

When the Boarding API successfully receives and validates the XML content, it will respond

with a synchronous SUCCESS status. If the XML content is received and fails validation, the

Boarding API will respond with a FAILURE status and the detailed errors which explain the

failure. The response can report multiple errors as below.

If any failure in transmission occurs, e.g. the service is unavailable, undergoing maintenance,

or network connectivity problems occur, it is the Boarding API consumer’s responsibility to

re-transmit the message at a later time. It is recommended that a back off algorithm be used

when re-transmitting.

Success Message Response Sample XML

<SubmitMPAResponse>

<SubmitMPAResult>

North Boarding API Specifications.docxSpecifications

Page 6 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ExternalRefId>123456789</ExternalRefId>

<ASRefId>123</ASRefId>

<Timestamp>2014-09-30 00:00:00.000</Timestamp>

<Status>SUCCESS</Status>

</SubmitMPAResult>

</SubmitMPAResponse>

Failure Message Response Sample XML

<SubmitMPAResponse>

<SubmitMPAResult>

<ExternalRefId>234567890</ExternalRefId>

<ASRefId>234</ASRefId>

<Timestamp>2014-09-30 00:00:00.000</Timestamp>

<Status>FAILURE</Status>

<Errors>

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription></ErrorDescription>

<LineNumber/>

<ColumnNumber/>

</MerchantError>

</Errors>

</SubmitMPAResult>

</SubmitMPAResponse>

**ExternalRefId**: It will hold the external Ref Id received from Client.

**ASRefId**: It will hold the MPA ID generated from Fiserv Boarding system in case of success.

It will be blank in case of failure.

**Timestamp**: The date time stamp of success or failure of the submission.

**Status**: if the MPA XML Content passes the validation, it will be **SUCCESS**. Otherwise, it will

be **FAILURE.**

**Errors**: It will hold the MerchantError tags – Only applicable if the MPA XML Content fails

against the validation.

**MerchantError**: It will contain multiple errors received while XSD validation as well as

error that relates to MPA edits of boarding merchant.

·

·

·

·

**ErrorId** : it will hold the Error #.

**ErrorDescription**: It will hold the description of merchant error.

**LineNumber:** it will hold the Error Line #. It could be sent as empty tag.

**ColumnNumber :** it will hold the Error Column #. It could be sent as empty tag.

**3.1.2.GetStatusByTimeSpan**

After the MPAs have been successfully submitted, this method allows the Client System to

retrieve the MPA status updates. It is recommended to invoke this service on a periodic basis

as a batch inquiry. The returned MPA status updates will correspond to the timestamps

passed to the method.The following diagram illustrates the business flow inside the method.

North Boarding API Specifications.docxSpecifications

Page 7 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





FD Calls

GetStatusbyTimeSpan

Method

API ready to

receive the call?

API receives the call with

specified Time Span

YES

FromTimeStamp within the

**last 72 hours** from the

current time?

YES

NO

Status Updates

within specified

Time Span?

API sends NO RECORD FOUND

return message

NO

YES

API sends MPA Status

Update Details Response

Details of the method are as follows:

Web Method Name: GetStatusByTimeSpan.

Input Parameters:

**Name**

**Data Type**

**Type Category**

**Description**

FromTimeStamp

DateTime (In UTC format –

ISO 8601)

simpleType

Value must be

within the last 72

hours from the

current time

ToTimeStamp

DateTime (In UTC format –

ISO 8601)

simpleType

Value must be

greater than

FromTimeStamp

Note that the user credentials will be passed along with the request on the SOAP Header and

are identified in a separate security documentation.

**Transmissions & Response**

When the Boarding API successfully receives a valid request, based on the timestamp, it will

respond synchronously with a list of MPA status details. The result can contain multiple MPAs

with multiple status updates within specified time span. If there are no status updates within

specified time span, the result will be sent as blank tag.

If any failure in transmission occurs, e.g. the service is unavailable, undergoing maintenance,

or network connectivity problems occur, it is the Boarding API consumer’s responsibility to

re-transmit the message at a later time. It is recommended that a back off algorithm be used

when re-transmitting.

**No Record Found Response Sample XML**

<GetStatusByTimeSpanResponse xmlns="http://tempuri.org/">

<GetStatusByTimeSpanResult>

North Boarding API Specifications.docxSpecifications

Page 8 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantApplicationStatus>

<ASRefId />

<FDMerchantNumber />

<Status>

<MerchantDetails>

<North FACSNumber />

<LocationNumber />

<DBAName />

<CardnetNumber />

<MerchantStatus>

<AppStatus>

<Code />

<Information>No record found against the specified

timespan.</Information>

<Timestamp>12/12/2014 03:21:51 PM</Timestamp>

</AppStatus>

</MerchantStatus>

</MerchantDetails>

</Status>

<Errors />

<CreditOfficerComments />

</MerchantApplicationStatus>

</GetStatusByTimeSpanResult>

</GetStatusByTimeSpanResponse>

**MPA Status Details Response Sample XML**

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

xmlns:xsd="http://www.w3.org/2001/XMLSchema">

<GetStatusByTimeSpanResponse xmlns="http://tempuri.org/">

<GetStatusByTimeSpanResult>

<GetStatusByTimeSpanResult>

<MerchantApplicationStatus>

<ASRefId>3495</ASRefId>

<FDMerchantNumber/>

<Status>

<MerchantDetails>

<NorthNumber/>

<CloverID/>

<LocationNumber>1</LocationNumber>

<DBAName>MMIS FDTST 0217 TT</DBAName>

<CardnetNumber/>

<MerchantStatus>

<AppStatus>

<Code>MPAKey</Code>

<Information>In Process</Information>

<Timestamp>2/18/2016 4:33:38 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MPA</Code>

<Information>In Process</Information>

<Timestamp>2/18/2016 4:33:38 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MpaKey</Code>

<Information>Submitted</Information>

<Timestamp>2/18/2016 4:33:40 PM</Timestamp>

</AppStatus>

North Boarding API Specifications.docxSpecifications

Page 9 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<AppStatus>

<Code>ClientApproval</Code>

<Information>Direct Send</Information>

<Timestamp>2/18/2016 4:33:40 PM</Timestamp>

</AppStatus>

</MerchantStatus>

<EquipmentDetails/>

</MerchantDetails>

</Status>

<Errors/>

<CreditOfficerComments/>

</MerchantApplicationStatus>

</GetStatusByTimeSpanResult>

</GetStatusByTimeSpanResult>

</GetStatusByTimeSpanResponse>

</s:Body>

</s:Envelope>

**ASRefID**: Cross Reference key returned during the account setup, the MPA ID generated

from Fiserv Boarding system.

**FDMerchantNumber**: Merchant number received from First Data.

**Status**: Is the node which will consist of **MerchantDetails**, which basically will hold the

Detail of accounts for various locations. This node will hold below fields:

**NorthNumber**: North FACS Mid assigned by VAPP. (Only be available after the account

approved)

**LocationNumber** : Outlet Number

**DBAName**: The Do Business As name of the merchant.

**MerchantStatus:** Which will contain various AppStatus (status)

**AppStatus**: Consists of below:

**-**

**Code**: Unique code defined for each status attribute. Please refer status attributes

table [in](#br21)[ ](#br21)[MPA](#br21)[ ](#br21)[STATUS](#br21)[ ](#br21)[REPORTING](#br21)[ ](#br21)section.

**-**

**Information**: This is used to report status values or additional information for the

status attribute. This field’s value is populated based on the value populated in the

status code. Please refer status attributes table [in](#br21)[ ](#br21)[MPA](#br21)[ ](#br21)[STATUS](#br21)[ ](#br21)[REPORTING](#br21)[ ](#br21)section.

**TimeStamp**: Timestamp of the status code.

**-**

**Errors**: Includes 2 elements, it will only be populated in the case of Validation failure.

\-

\-

**ErrorID**: Error code will appear defined for Validation Failure.

**ErrorDescription** : Error description

**CreditOfficerComments**: It will have the comments detail.

**Comment:** This will have following fields:

\-

\-

\-

CreditOfficerId: Credit officer ID.

Message: Credit message for the account.

MessageDate: Date time for the message.

**3.2. XML FORMAT**

The details of meerchant Information in XML format/elements are described in the excel

spreadsheet “Master Mapping for North FACS API XML V1.0”. For more information on

North Boarding API Specifications.docxSpecifications

Page 10 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





implementation and XSD validation, please refer to the XSD document of “North

FACSAPI\_XMLSchema\_V1.0”.

**3.3. VALIDATION HANDLER**

The validation handler will conduct two steps of validation against the merchant

information details . The following descriptions show how these steps function.

**Schema Validation**

This is the first step of validation to ensure the received XML content has well-formed

structure and valid enumerations that conform to the enumeration definition in the XML

schema. If it successfully passes the schema validation, the following steps will be conducted.

Otherwise, the error message will show specifically to every violation against the schema

definition.

**Conditional Data Logic Validation**

This step will ensure all the Merchant Information details conform to the MPA Capture edits.

The validation rules and error messages are defined in the following table.

**Description of Validation Performed**

**GENERAL VALIDATION**

**Error Message**

The validation of conditionally mandatory

fields, value range, ect. identified in the

Master Mapping for North FACS API XML

spreadsheet.

Location NN: {Section Name} Errors!

**MPA INFO VALIDATION**

The validation of conditionally mandatory

fields identified in the Master Mapping for

North FACS API XML spreadsheet.

MPA Info Errors!

Number of Locations value and the number of MPA Info - Locations field does not reflect

added locations do not match

the number of locations added.

**SIGNATURES VALIDATION**

The validation of conditionally mandatory

fields identified in the Master Mapping for

North FACS API XML spreadsheet.

SignaturesErrors!

Date Signed must be specified for Client MPA

Signatures 1 if Merchant Type = S - Standard

If in Ownership, Owner 2 is specified and

Merchant Type = S - Standard Date Signed

must be specified for Client MPA Signatures 2

If in Ownership Prin1GuarantorCode = 1 and

Client MPA Signatures 1 - Date Signed is

required.

Client MPA Signatures 2 - Date Signed is

required.

Personal Guarantee 1 - Title of Signer is

Merchant Type = S - Standard, Title of Signer is required.

required for Personal Guarantee 1

North Boarding API Specifications.docxSpecifications

Page 11 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





If in Ownership Prin1GuarantorCode = 1 and

Personal Guarantee 1 - Name of Signer is

Merchant Type = S - Standard, Name of Signer required.

is required for Personal Guarantee 1

If in Ownership Prin1GuarantorCode = 1 and

Merchant Type = S - Standard, Date Signed is

required for Personal Guarantee 1

Personal Guarantee 1 - Date Signed is

required.

If in Ownership Prin1GuarantorCode = 1 and

Personal Guarantee 2 - Title of Signer is

Merchant Type = S - Standard, Title of Signer is required.

required for Personal Guarantee 2

If in Ownership Prin1GuarantorCode = 1 and

Merchant Type = S - Standard, Name of Signer required.

is required for Personal Guarantee 2

Personal Guarantee 2 - Name of Signer is

If in Ownership Prin1GuarantorCode = 1 and

Merchant Type = S - Standard, Date Signed is

required for Personal Guarantee 2

Personal Guarantee 2 - Date Signed is

required.

If Merchant Type = S and Telecheck

TeleCheck ACH Authorization - Name of

Signer is required.

entitlement is selected, Name of Signer mut

be specified for Telecheck ACH Authorization

If Merchant Type = S and Telecheck

entitlement is selected, Name of Signer mut

be specified for Telecheck ACH Authorization

TeleCheck ACH Authorization - Name of

Signer is required.

**BUSINESS INFO VALIDATION**

The validation of conditionally mandatory

fields identified in the Master Mapping for

North FACS API XML spreadsheet.

Industry Type must be MOTO/Internet or

Retail if GGe4 Entitlement is selected in

Entitlements page

Business Info Errors!

Industry Type must be MOTO/Internet or

Retail for Payeezy entitlement selection.

Industry Type must be MOTO/Internet if one

of the following values is selected for Pricing

Type in Pricing page:

The Industry Type must be MOTO/Internet

when Pricing Type is 003 - MO/TO or 004 -

MO/TO (NO AVS) or 103 - DC MOTO or 104 -

DC MOTO (NO AVS).

·

·

·

·

003 - MO/TO

004 - MO/TO (NO AVS)

103 - DC MOTO

104 - DC MOTO (NO AVS)

In Corporate Info page SPARK Exclusion

Indicator must be "Financial Institution" if

SIC/MCC code is 6010 - Member Financial

Institutions or 6011 - Member Financial

Institutions - Automated Cash

Foreign Entity Flag = "Financial Institution"

must be selected when MCC code is 6010 or

\6011.

North Boarding API Specifications.docxSpecifications

Page 12 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





If SPARK Exclusion Indicator in Corporate Info

is "Financial Institution" SIC/MCC code must

be 6010 - Member Financial Institutions -

Manual Cash or 6011 - Member Financial

Institutions - Automated Cash

MCC = 6010 or 6011 is required for Foreign

Entity Flag = "Financial Institution".

Fax Type must be ‘MAIL’ or ‘MAIL AND EIDS’ if The Fax Type must be MAIL, MAIL AND EIDS

Location Fax in Business Info page is not

entered

when Process Mode is EDC and Location Fax

is not entered.

If Location Fax in Business Info page is

entered, Fax Type must be among the

following values:

Business Info - The Fax Type must be

CM/ALERT ONLY, FAX, PC TO PC, EIDS ONLY,

MAIL AND EIDS, AUTOFAX AND EIDS when

Process Mode is EDC and Location Fax is

entered.

·

·

·

·

·

·

CM/ALERT ONLY,

FAX,

PC TO PC,

EIDS ONLY,

MAIL AND EIDS,

AUTOFAX AND EIDS

Please refer to 31494 - Master Mapping for

North FACS API XML for a list of valid web

extensions

Invalid Website extension.

**CORPORARATE INFO VALIDATION**

The validation of conditionally mandatory

fields identified in the Master Mapping for

North FACS API XML spreadsheet.

Corporate Info Errors!

Please refer to 31494 - Master Mapping for

North FACS API XML for the list of allowed

compatible combinations of country and state

Country is invalid with State selection.

**ENTITLEMENTS VALIDATION**

The validation of conditionally mandatory

fields identified in the Master Mapping for

North FACS API XML spreadsheet.

Entitlements Errors!

Please refer 31494 - Master Mapping for North The American Express is not allowed for

FACS API XML to for the list of SIC codes Location's SIC code of [SICcode].

compatible with AMEX DIRECT

GGe4 entitltment is required if any of the

following GGe4 equipments has been added

for the MPA:

GGe4 Entitlement is required for GGe4

Equipment selection.

**ModelCo EquipmentNa EquipmentDescri**

**de**

**me**

North Boarding API Specifications.docxSpecifications

Page 13 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





60402 GEH4ST

60403 EGHS4M

60404 GRT4TP

GGE4 - HOSTED PMT (RTL/MOTO)

GGE4 - HOSTED PMT (ECOMM)

GGE4 - REALTIME PMT MGR

(RTL/MOTO)

60405 GAPISV

60406 GS4WBS

GGE4 - WEB SVC API (ECOMM)

GGE4 - WEB SVC API (RTL/MOTO)

If Front end Network (in Processing page) is not

BuyPass Fees is not allowed when Front End

BUYPASS, BuyPass Fees entitlement is not allowed Network is not Buypass.

If MCC/SIC in Business Info is 4722 - Travel

Agencies and Tour Operators, IATA Number is

required

The IATA Number field is required.

EBT entitlement is not allowed if there has been

any equipment of COMPASS network added for

the MPA

EBT entitlement is not allowed for Compass

FE.

Voyager entitlement is not allowed if there

has been any equipment of any of the

following processing network added for the

MPA:

Voyager entitlement is not allowed for

Cardnet FE or Compass FE or FDR FE or

Nashville FE.

·

·

·

·

COMPASS

CARDNET

FDR

NASHVILLE

Wright Express Full Acquiring entitlement is

not allowed if there has been any equipment

of any of the following processing network

added for the MPA:

Wright Express Full Acquiring entitlement is

not allowed for Cardnet FE or Compass FE or

FDR FE or Nashville FE.

·

·

·

·

COMPASS

CARDNET

FDR

NASHVILLE

Wright Express Pass Through entitlement is

not allowed if there has been any equipment

of any of the following processing network

added for the MPA:

Wright Express Pass Through entitlement is

not allowed for Cardnet FE or Compass FE or

FDR FE or Nashville FE.

·

·

·

·

COMPASS

CARDNET

FDR

NASHVILLE

North Boarding API Specifications.docxSpecifications

Page 14 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**PRICING VALIDATION**

The validation of conditionally mandatory

Pricing Errors!

fields identified in the Master Mapping for

North FACS API XML spreadsheet.

Please refer to 31494 - Master Mapping for

The American Express is not allowed for

North FACS API XML for SICs not allowed with Location's SIC code of [SICcode].

Amex Opt Blue

UnBundled PIN Debit is not allowed if Industry UnBundled PIN Debit is not allowed for

Type = L - Lodging

Lodging Industry Type.

Bundled PIN Debit is not allowed if Industry

Type = L - Lodging

Bundled PIN Debit is not allowed for Lodging

Industry Type.

Please refer to 31494 - Master Mapping for

North FACS API XML for invalid combinations

of Pricing Type and SIC

The selection of Pricing Type is not allowed

for Location's SIC Code of [SICcode].

If AMEX DIRECT is selected for Entitlements,

AMEX Opt Blue is not allowed and vice versa

If Annual Amex Credit Sales Volume >=

1,000,000 or Country (in Business Info) is not

USA. American Express is not allowed

At least one of the following entitlements

must be selected:

Both American Express and AMEX Direct

cannot be selected.

American Express can only be selected if the

Annual Amex Credit Sales Volume is less than

$1,000,000 or Country is USA.

One of the following entitlements: PIN Debit,

Pin/Non-PIN Debit, EBT, Voyager, Wright

Express Full Acquiring, Wright Express Pass

Through is required.

·

·

·

·

·

·

PIN Debit

Pin/Non-PIN Debit

EBT

Voyager

Wright Express Full Acquiring

Wright Express Pass Through

If Front-End Network is COMPASS, Unbundled Unbundled PIN Debit must not be specified

PIN Debit is not allowed for Compass FE.

**OWNERSHIP VALIDATION**

The validation of conditionally mandatory Ownership Errors!

fields identified in the Master Mapping for

North FACS API XML spreadsheet.

Please refer to 31494 - Master Mapping for

North FACS API XML for the list of allowed

compatible combinations of country and state

If for Owner 1, location = H or Location = A,

Personal Guarantee for Owner 1 must be Yes

If for Owner 2, location = H or Location = A,

Personal Guarantee for Owner 2 must be Yes

Country is invalid with State selection.

The Owner 1 Personal Guarantee must be

Yes when Location is Apartment or Home.

The Owner 2 Personal Guarantee must be

Yes when Location is Apartment or Home.

North Boarding API Specifications.docxSpecifications

Page 15 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





If Merchant Type = C (C2A), E-mail Address is

required for Owner 1

If Merchant Type = C (C2A), E-mail Address is

required for Owner 2

Owner 1 - The Email Address field is required.

Owner 2 - The Email Address field is required.

**EQUIPMENT AND FE VALIDATION**

The validation of conditionally mandatory Equipment and FE Errors!

fields identified in the Master Mapping for

North FACS API XML spreadsheet.

There must be at least one equipment added

The Front End Network of all equipments

specified must match the Front End Network

in Processing page

Equipment selection is required.

The Equipment selection is incomplatible with

selected Front End Network.

It is required that one of the following

At

least

one

equipment

with

conditions be met if in Entitlements page, EBT Model/Peripheral Feature of Integrated

entitlement is selected:

PinPad = Yes or PinPad Peripheral selection

should be setup for EBT entitlement selection.

·

·

·

At least one equipment has intergrated

pin pad

At least one equipment has pinpad

peripheral

At least one equipment has a peripheral

which has an integrated pin pad

It is required that one of the following

conditions be met if in Pricing page, Bundled

PIN/Non-PIN Debit is selected:

At

least

one

equipment

with

Model/Peripheral Feature of Integrated

PinPad = Yes or PinPad Peripheral selection

should be setup for Bundled PIN/Non-PIN

entitlement selection.

·

·

·

At least one equipment has intergrated

pin pad (pin pad is a model feature)

At least one equipment has pinpad

peripheral

At least one equipment has a peripheral

which has an integrated pin pad

It is required that one of the following

conditions be met if in Pricing Page,

UnBundled PIN Debit is selected and there is

no equipment with EMV feature

At

least

one

equipment

with

Model/Peripheral Feature of Integrated

PinPad = Yes or PinPad Peripheral selection

should be setup for Unbundled PIN Debit

entitlement selection.

·

·

·

At least one equipment has intergrated

pin pad (pin pad is a model feature)

At least one equipment has pinpad

peripheral

At least one equipment has a peripheral

which has an integrated pin pad

North Boarding API Specifications.docxSpecifications

Page 16 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





If Payeezy Entitlement is selected in

The Compass/Payeezy Equipment is required

Entitlments page at least one of the following for Payeezy entitlement selection.

equipment must be added for the MPA:

·

·

·

·

·

·

ModelCode

EquipmentName

EquipmentDescription

60402

GEH4ST

GGE4 - HOSTED PMT (RTL/MOTO)

60403 EGHS4M

GGE4 - HOSTED PMT (ECOMM)

60404 GRT4TP

GGE4 - REALTIME PMT MGR (RTL/MOTO)

60405 GAPISV

GGE4 - WEB SVC API (ECOMM)

60406 GS4WBS

GGE4 - WEB SVC API (RTL/MOTO)

Only one of the following four GGE4

equipment models is allowed at the same

time:

Only one of the following models is allowed:

GGE4 - HOSTED PMT (RTL/MOTO) , GGE4 -

HOSTED PMT (ECOMM), GGE4 - REALTIME

PMT MGR (RTL/MOTO),GGE4 - WEB SVC API

(ECOMM), GGE4 - WEB SVC API (RTL/MOTO).

·

·

·

·

·

·

ModelCode

EquipmentName

EquipmentDescription

60402

GEH4ST

GGE4 - HOSTED PMT (RTL/MOTO)

60403 EGHS4M

GGE4 - HOSTED PMT (ECOMM)

60404 GRT4TP

GGE4 - REALTIME PMT MGR (RTL/MOTO)

60405 GAPISV

GGE4 - WEB SVC API (ECOMM)

60406 GS4WBS

GGE4 - WEB SVC API (RTL/MOTO)

Please refer to 31494 - Master Mapping for

North FACS API XML for a complete list of EB-

compatible equipments

Invalid FrontEnd/EBT Combination

At

least

one

equipment

with

It is required that one of the following

conditions be met if in Pricing Page Bundled

PIN/Non-PIN Debit is selected and Combined

Transaction Fee/Combined Discount Fee is

specified for PIN/Non-PIN Debit:

Model/Peripheral Feature of Integrated

PinPad = Yes or PinPad Peripheral selection

should be setup for Bundled PIN/Non-PIN

entitlement selection.

·

At least one equipment has intergrated

pin pad (pin pad is a model feature)

North Boarding API Specifications.docxSpecifications

Page 17 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





·

·

·

At least one equipment has pinpad

peripheral

At least one equipment has a peripheral

which has an integrated pin pad

At least one equipment has EMV as a

model feature

If TransArmor Token Registration & Encryption Equipment and FE - At least one equipment

is specified, there must be at least one with Model Feature of TransArmor Security

equipment with Model Feature of TransArmor Level = “01 – TOKENIZATION & ENCRYTPION”

Security Level = “01 – TOKENIZATION &

ENCRYTPION”

should be setup for "TransArmor Token

Registration & Encryption" Fee.

If TransArmor Token is specified, there must

Equipment and FE - At least one equipment

be at least one equipment with Model Feature with Model Feature of TransArmor Security

of TransArmor Security Level = "03 –

TOKENIZATION ONLY"

Token Only = "03 – TOKENIZATION ONLY"

should be setup for "TransArmor Token" Fee.

**OTHER FEES VALIDATION**

The validation of conditionally mandatory

fields identified in the Master Mapping for

North FACS API XML spreadsheet.

Other Fees Errors!

Billed Monthly Fee of type Regulatory Product The Regulatory Product is not allowed to

is not allowed if MCC/SIC code is 6010 or 6011 specify with Location's SIC Code of 6010 and

\6011.

If there is any Nashville equipment with

TransArmor Security Level feature (value)

configured as 01 – TOKENIZATION &

ENCRYTPION, TransArmor Token Registration

& Encryption fee is required

TransArmor Token Registration & Encryption

Fee is required with TransArmor Security

Level = “01 – TOKENIZATION &

ENCRYTPION”.

If there is any Nashville equipment with a

value different from 01 – TOKENIZATION &

ENCRYTPION selected for its feature

TransArmor Token Registration & Encryption

Fee must NOT be specified with TransArmor

Security Level <> “01 – TOKENIZATION &

TransArmor Security Level, TransArmor Token ENCRYTPION”.

Registration & Encryption fee must not be

specified

If TransArmor Security Level-Token Only value TransArmor Token Registration & Encryption

is set to 03 and there is at least one

equipment with Front-End network =

CARDNET

Fee is required with "TransArmor Security

Level-Token Only" = "03 - TOKENIZATION

ONLY".

North Boarding API Specifications.docxSpecifications

Page 18 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





If TransArmor Security Level-Token Only value "{0}" Fee must NOT be specified with

is not 03 - TOKENIZATION ONLY and there is at "TransArmor Security Level-Token Only" <>

least one equipment with Front-End Network "03 - TOKENIZATION ONLY".

= CARDNET, TransArmor Token Registration &

Encryption Fee is not allowed to specify

Only one of the following is allowed to be

specified at a time:

Both Visa/MC/Disc Chargeback and Retrieval

Fee and Retrieval Fee values are NOT

allowed.

·

Visa/MC/Disc Chargeback and Retrieval

Fee

·

Retrieval Fee

Only one of the following is allowed to be

specified at a time:

Both Visa/MC/Disc Chargeback and Retrieval

Fee and Chargeback Fee values are NOT

allowed.

·

Visa/MC/Disc Chargeback and Retrieval

Fee

·

Chargeback Fee

Only one of the following is allowed to be

specified at a time:

Both TransArmor Min Monthly Fee and

TransArmor Monthly Fee values are NOT

allowed.

·

TransArmor Min Monthly Fee

TransArmor Monthly Fee

·

If Front-End Network is COMPASS or FDR,

TransArmor Token Registration & Encryption

must not be specified

TransArmor Token Registration & Encryption

must not be specified for Compass FE or FDR

FE.

**PROCESSING VALIDATION**

The validation of conditionally mandatory

fields identified in the Master Mapping for

North FACS API XML spreadsheet.

Frequency Indicator must be either D - Daily

or M - Monthly

Processing Errors!

Frequency Indicator should be Daily or

Monthly for North FACS.

If GGe4 (Payeezy) entitlement is selected

Front-End Network must be COMPASS

Front End Network must be Compass for

Payeezy entitlement selection.

**SALES VALDIATION**

The validation of conditionally mandatory

fields identified in the Master Mapping for

North FACS API XML spreadsheet.

Sale Errors!

If American Express is selected Amex Credit

Sales Volume must be specified

If American Express is selected Location

Average Amex Ticket must be specified

If American Express is selected Amex Credit

Sales Volume must be specified

Location Amex Credit Sales Volume is

required if American Express selected.

Location Average Amex Ticket is required if

American Express selected.

Combined Amex Credit Sales Volume is

required if American Express selected.

North Boarding API Specifications.docxSpecifications

Page 19 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





If in Pricing, Discover Credit and Discover

Debit are selected Annual Discover Credit

Sales Volume must be specified

The Annual Discover Credit Sales Volume

field is required.

If selected MCC/SIC code = 5814 Location

Location Average MC/VISA/Discover Ticket

Average MC/VISA/Discover Ticket must not be must NOT be greater than $25 for SIC/MCC

greater than $25

of 5814.

If selected MCC/SIC code = 5814 Location

Location Average Amex Ticket (Total Annual

Sales Volume (Cash+Credit+Debit+Check) )

must not be greater than $25

Location Average Amex Ticket must NOT be

greater than $25 for SIC/MCC of 5814.

**SITE INFO VALIDATION**

The validation of conditionally mandatory

fields identified in the Master Mapping for

North FACS API XML spreadsheet.

Site Info Errors!

Please refer to 31494 - Master Mapping for

North FACS API XML for the list of allowed

compatible combinations of country and state

If the number of locations of the MPA is

greater than 1, Statement Type of the first

location must be ‘G’

Country is invalid with State selection.

Statement Type must be Summary FDMS

Summary for the first location.

If the number of locations of the MPA is 1,

statement Recap must have one of the

following values:

Statement Recap must be Mail To Outlet or

Mail To Corporate No Recap or No Statement

for MPA which contains only one location.

·

·

·

07 - Mail To Outlet

02 - Mail To Corporate No Recap

01 - No Statement

If Statement Recap = 07 - No Statement,

Delivery Option must be O - Online

If Statement Recap = 07 - No Statement,

Delivery Option must be O - Online and vice

versa

The Delivery Option must be Online when

Statement Recap is No Statement.

The Statement Recap must be No Statement

when Delivery Option is Online and vice

versa.

If Statement Recap is 01 - Mail To Outlet or 02 Delivery Option must be Print and Mail when

\- Mail to Corporate No Recap, Delivery Option Statement Recap is Mail To Outlet or Mail To

must be P - Print and Mail

Corporate No Recap.

Delivery Option must be O - Online if

Statement Recap is 09 - Mail To Corporate

With Recap

Delivery Option cannot be Online for the first

location and Statement Recap is Mail To

Corporate With Recap.

North Boarding API Specifications.docxSpecifications

Page 20 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**3.4. MPA STATUS REPORT**

Below is the list of the status codes and status attributes with the possible values in the

order of their possible occurrence.

**Status Code/Status**

**Attribute**

**Description**

**Report**

**Level**

**Possible**

**Values/Informati**

**on**

The following event types reflect merchant Boarding progress.

MPA

The overall MPA Status

MPA

In Process

Cancelled

Declined

Deleted

Error

Boarded

MpaKey

MPA Key Status

MPA

MPA

Cancelled

In Process

Returned

ReSubmitted

Submitted

In Process

Cancelled

Declined

ClientApproval

MPA Client Approval Status

Auto Approved

Approved with

Changes

Approved

Direct Send

Locked for

Decisioning

Returned

In Process

Approved

Approved with

Changes

Merchant2Approval

MPA Merchant Owner 2 Approval

Status

MPA

Cancelled by

Merchant

Cancelled by

Timeout

In Process

Expired

North Boarding API Specifications.docxSpecifications

Page 21 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Stopped On

Action

Suspended

In Process

Approved

Approved with

Changes

Merchant1Approval

MPA Merchant Owner 1 Approval

Status

MPA

Cancelled by

Merchant

Cancelled by

Timeout

In Process

Expired

Stopped On

Action

Suspended

No Approval

Required

In Process

Declined

MerchantChangeAppro MPA Merchant Change Approval

MPA

val

Status

Approved

In Process

Error

Success

Boarded

Transmission

Transmission to VAPP Status

MPA UAL Boarding Status

MPA

MPA

FDBoarding

In Process

Error

Locationunderwriting

Location-based MPA Underwriting Location Risk Identified

Status

Account Pending

with Credit

Credit Approved

Credit Declined

In Process

Account Sent to

Credit

BackEnd

Location Back End Setup Status

MPA Equipment Status

Location Complete

In Process

Location Complete

In Process

LocationEquipment

Pending Setup

North Boarding API Specifications.docxSpecifications

Page 22 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





The following additional data from UAL (with the exception of NorthNumber) become

available only when the merchant has been successfully boarded.

TID

Cardnet/Nashville/Datwawire/Buy Equipme Each TID is

pass

TID

nt

specific to the

equipment with

front-end Cardnet

it is assigned to.

EQUIPDESC

DID

Description of equipment

Datawire ID

Equipme

nt

Equipme Datawire ID varies

nt

per the

equipment to

which it is

assigned

DOWNLOADID

Nashville/Buypass Download ID

Equipme Distinguish with

nt

other Download

ID by selected

front-end

RCGROUPID

RapidConnect ID

North BE MID

Equipme

nt

Location

NorthNumber

Since every status attribute has multiple status values, it will be reported multiple times

based on the status value updates. The status attributes which have the Report Level = “MPA”

will be reported on the first Location only, the others which have the Report Level =

“Location” will be reported on any Locations that have the status updates.

The status attributes table above contains all possible status attributes with status values.

However, reporting the status will totally depend on the MPA Type and the MPA data. The

following cases will explain how reporting status varies by MPA:

\-

Based on the MPA data, some of the status attributes may not be reported. For example, in an

MPA, if the Equipment Front End has not been set up for say Location #2, then Location #2 will not

have any of the Front End Statuses reported such as LocationEquipment.

\-

The status attributes which relate to Merchant Approval process such as Merchant2Approval,

Merchant1Approval, MerchantChangeApproval will not be reported for the MPAs submitted via

the API because all of them are Standard MPAs which do not require Merchant Approval. These

are identified for future use.

**3.5. BOARDING PROCESS**

Once the MPAs have been successfully submitted through Boarding API, they will be

processed as standard MPAs in Boarding system. These MPAs are regarded as complete in

North Boarding API Specifications.docxSpecifications

Page 23 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





keying under the user account whose credentials have been passed along with the MPA XML

Content. They will be then transmitted to UAL after being approved in the Client Approval

process.

During keying, Client Approval, Transmission and UAL Boarding processes, it is the Fiserv

Boarding system’s responsibility to track and update the MPA status.

For managing and reporting purposes, these MPAs will be permanently set with the MPA

Type of “API” to distinguish them from the Standard MPAs created from the UI. This will not

allowed the users to change the MPA Type. The users, however, are still able to edit other

MPA data where applicable.

**4. SOAP Security Guide**

This section aims at providing an insight into the important preparation procedures that must

be seen through to facilitate a successful integration with the API specifically designed for

North Boarding FACS.

This sectionis primarily intended for software developers with sufficient technical

background. Non-technical readers are encouraged to read the document as it might greatly

support them in the verification process of North FACS API.

It is suggested the document be read in its entirety for a full-fledged understanding of how

North Boarding FACS API receives and answers to web service calls.

**4.1. CONNECTIVITY VERIFICATION VIA SOAP UI**

It is of high importance that before any attempt to connect to or to utilize North FACS SOAP

API is made, North FACS SOAP API has been verified to be up and running as required.

Refer to this section for detailed information as to how to interact with North FACS SOAP API

using a tool – SOAP 5.2.0. The document particularly addresses version 5.2.0. Details

mentioned in this section may not be the same as or applied in the same way for other

versions of SOAP UI.

**4.1.1.Prerequisite Checks**

The following conditions must be met before any connectivity verification can be carried out;

·

·

IP Whitelisting process has been completed.

Necessary user set-ups have been completed and the person submitting requests to North FACS

SOAP API has the correct credentials.

·

A working version of SOAP UI has been installed in advance.

**4.1.2.Configure SOAP UI**

North Boarding API Specifications.docxSpecifications

Page 24 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Several important settings must be in place to secure a successful connection to the North

FACS Boarding SOAP API.

**4.1.2.1.**

**Initiate SOAP Project Workspace**

Hit Ctrl + N and a new window will open prompting for entering Project Name and Initial

WSDL;

Project Name: Enter a desired project name

Initial WSDL: [https://lsuat-](https://lsuat-api.fdportfoliomanager.com/boarding/north/NorthAsBoardingAPIService.svc?wsdl)

[api.fdportfoliomanager.com/boarding/north/NorthAsBoardingAPIService.svc?wsdl](https://lsuat-api.fdportfoliomanager.com/boarding/north/NorthAsBoardingAPIService.svc?wsdl)

Click OK

·

·

In a few seconds or less the newly created SOAP project will be loaded with all the presentable

components of the North Boarding FACS API.

A successful load will be indicated by no error and the web service’s components being displayed on

the Navigator panel. An example is shown in the following screenshot:

North Boarding API Specifications.docxSpecifications

Page 25 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





It can be seen from the above screenshot that the North FACS API web service is composed

of two separate web methods that will function together as a whole:

·

·

SubmitMPA is used for submitting North FACS MPAs

GetStatusByTimeSpan is used for retrieving the states and statuses of submitted North FACS MPAs

within a limited time window that spans 72 hours.

**4.1.2.2.**

**Set up Security and Authentication**

Enable Project View by double-clicking on the SOAP project’s name or right-clicking the name

and then selecting Show Project View

A new window will appear where additional settings can be configured for the SOAP project.

As the communication with North Boarding FACS API is done via SOAP calls, it is mandatory

that all the calls from SOAP client side contain a security header with sufficient and precise

information to guarantee a successful authentication with the Boarding API web service.

North Boarding API Specifications.docxSpecifications

Page 26 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Navigate to WS-Security Configurations tab to specify the credentials with which the SOAP

requests will be authenticated by. Note: First Data is responsible for providing the working

credentials.

·

Then select the tab Outgoing WS-Security Configurations. It should be the default sub-tab of the WS-

Security Configurations one.

·

Click on the

icon to create a new Outgoing WS-Security Configuration. Enter a name as desired

then click OK.

North Boarding API Specifications.docxSpecifications

Page 27 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Click on the

below to add a WSS entry for the new WSS configuration. The entry will home

the username and password provide by FD. In the opened pop-up Add WSS Entry, select entry

type Username and hit OK.

North Boarding API Specifications.docxSpecifications

Page 28 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Enter username and password as necessary and make sure that:

·

·

·

Add Nonce field: checked off

Add Created field: checked off

Password Type: PasswordDigest Ext

North Boarding API Specifications.docxSpecifications

Page 29 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**4.1.2.3.**

**Start SOAP Request Submission**

As the preparations are all completed now, it is time SOAP calls can be made to the North

FACS API to verify the connection, as well as the functionalities it offers.

31494 - North FACS

API Sample Project - V

Note that the WS security header will still need to be customized with the provided API

username and password.

North Boarding API Specifications.docxSpecifications

Page 30 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**4.1.2.4.**

**SOAP Project Template**

As an alternative to setting up a new SOAP project from scratch, one can opt to import the

pre-configured SOAP project below:

**4.1.3.Submit SOAP Requests**

**4.1.3.1.**

**SubmitMPA**

Use the auto-generated SOAP request (Request 1) or right-click on SubmitMPA > Select New

Request

Double-click on Request 1 to modify the content as appropriate before sending it to North

FACS SOAP API.

Note: The added or updated content will go into the left panel of the SOAP request.

Add security information to the SOAP request header for authentication purpose

Right-click on the SOAP request content and select Outgoing WSS > Apply [Name of the

Outgoing WS-Security Configuration]

Note: The outgoing WSS configuration must be applied every time before SOAP request is sent

to North Boarding FACS API. Failing to do this will most likely cause the Omaha API to respond

with a Generic Error message.

North Boarding API Specifications.docxSpecifications

Page 31 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Add the merchant application to the SOAP request body for the obvious purpose of MPA

submission

·

·

Copy a valid merchant application in the form of XML and paste the whole content between these two

tags: <tem:xmlContent> and </tem:xmlContent>

Change the value of element <tem:northChannel> to “FACS”

Hit the

icon to submit the SOAP request to North FACS API

·

·

The North Boarding FACS SOAP API web service will acknowledge the request by sending back a SOAP

response which will then show on the panel to the right of the request (Request 1 in the example).

The response will vary mainly depending on the supplied merchant application. However for most of

the time a successful submission will be indicated by these two most basic SOAP responses as follows:

North Boarding API Specifications.docxSpecifications

Page 32 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





·

·

Note: This document does not discuss in details failed MPA submissions that are caused by the

provided data of the merchant application. The goal is to make sure the connection to North Boarding

FACS API is established successfully.

A successful submission is characterized by the response below:

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

xmlns:xsd="http://www.w3.org/2001/XMLSchema">

<SubmitMPAResponse xmlns="http://tempuri.org/">

<SubmitMPAResult>

<ExternalRefId>?</ExternalRefId>

<ASRefId>3482</ASRefId>

<Timestamp>02/17/2016 01:40:31 PM</Timestamp>

<Status>SUCCESS</Status>

<Errors/>

</SubmitMPAResult>

</SubmitMPAResponse>

</s:Body>

</s:Envelope>

·

An unsuccessful submission caused by the merchant application data

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

xmlns:xsd="http://www.w3.org/2001/XMLSchema">

<SubmitMPAResponse xmlns="http://tempuri.org/">

<SubmitMPAResult>

<ExternalRefId>?</ExternalRefId>

<Timestamp>02/17/2016 01:43:14 PM</Timestamp>

<Status>FAILURE</Status>

<Errors>

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>MPA Info - The Bank is not

assigned.</ErrorDescription>

</MerchantError>

<MerchantError>

<ErrorId>2</ErrorId>

<ErrorDescription>MPA Info - The Agent is not

assigned.</ErrorDescription>

</MerchantError>

</Errors>

</SubmitMPAResult>

</SubmitMPAResponse>

</s:Body>

</s:Envelope>

**4.1.3.2.**

**GetStatusByTimeSpan**

Enter values for the two xml elements as required. North FACS API will base on the supplied

values to return all the MPA status changes that happen in between the selected period.

·

<tem:fromTimeStamp>?</tem:fromTimeStamp>

North Boarding API Specifications.docxSpecifications

Page 33 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





·

<tem:toTimeStamp>?</tem:toTimeStamp>

Note:

·

·

For fromTimeStamp, the value must not be more than 72 hours earlier than the current date time.

The values passed to North FACS API must be in UTC format (ISO 8601). For an example: 2016-02-15

10:13:16.887 AM (CST) → 2016-02-26T16:13:16.887Z

·

toTimeStamp must be later than fromTimeStamp

A successful call to North FACS API web service will be indicated by a successful response as

shown in the example below:

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

xmlns:xsd="http://www.w3.org/2001/XMLSchema">

<GetStatusByTimeSpanResponse xmlns="http://tempuri.org/">

<GetStatusByTimeSpanResult>

<GetStatusByTimeSpanResult>

<MerchantApplicationStatus>

<ASRefId>3483</ASRefId>

<FDMerchantNumber/>

<Status>

<MerchantDetails>

<NorthNumber/>

<CloverID/>

<LocationNumber>1</LocationNumber>

<DBAName>MMIS FDTST 0217 TT</DBAName>

<CardnetNumber/>

<MerchantStatus>

<AppStatus>

<Code>Transmission</Code>

<Information>In Process</Information>

<Timestamp>2/17/2016 1:45:03 PM</Timestamp>

</AppStatus>

</MerchantStatus>

<EquipmentDetails/>

</MerchantDetails>

</Status>

<Errors/>

<CreditOfficerComments/>

</MerchantApplicationStatus>

</GetStatusByTimeSpanResult>

</GetStatusByTimeSpanResult>

</GetStatusByTimeSpanResponse>

</s:Body>

</s:Envelope>

**4.2. CONNECTIVITY VERIFICATION VIA OTHER PLATFORMS**

As it is understood that web service calls actually are made from outside of the SOAP UI tool,

once the connectivity testing with the SOAP UI tool is completed, one can go ahead with

verifying the North Boarding API using another internal platform other than the SOAP UI one.

North Boarding API Specifications.docxSpecifications

Page 34 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





First Data must be informed of the result of connectivity tests with North Boarding API using

the SOAP UI tool. This will help First Data stay up-to-date with the latest progress of partners

and will also expedite the troubleshooting/support process in case there is any technical

difficulty or issue involved.

This section provides additional information about how SOAP requests to North Boarding API

should be constructed with an aim to assist with the generation of valid SOAP requests from

First Data partners.

North Boarding SOAP API was designed to understand many different formats of SOAP

requests. However to be considered valid by the web service, SOAP requests must meet

defined minimum structural requirements to guarantee a successful integration with North

Boarding FACS SOAP API. More details are available in:

·

·

[SOAP](#br35)[ ](#br35)[Request](#br35)[ ](#br35)[Header](#br35)

[SOAP](#br37)[ ](#br37)[Request](#br37)[ ](#br37)[Body](#br37)

The link to North Boarding API in UAT is:

<https://lsuat-api.fdportfoliomanager.com/boarding/north/NorthAsBoardingAPIService.svc>

**4.2.1.SOAP Request Header**

Note: A SOAP header can leave out the attribute **wsu: Id**, e.g. wsu: Id="UsernameToken-

699F92A9FFDD6BF4E7145557039343214" and still be fully understood by North FACS

API.

The process to generate a valid SOAP can be in a general sense described as having the steps

below:

\1. Generate a random nonce value

\2. Get current local date time in UTC format

\3. Get username token (plain-text) from First Data

\4. Get password token (plain-text) from First Data

\5. Combine nonce value (plain-text) + created date (UTC) + password token (plain-text) to form a string.

Apply SHA-1 encryption on the string. The encryption result is then converted to base-64 string format

to obtain the password digest.

\6. Send to North FACS API

·

·

·

·

username token (plain-text)

password digest (encrypted)

nonce value (in base-64 string format)

created date time (UTC)

Header of SOAP requests to North Boarding FACS API is always required contains a <wsse:

UsernameToken> element of which XML Structure can be illustrated as:

<wsse:UsernameToken>

North Boarding API Specifications.docxSpecifications

Page 35 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<wsse:Username>...</wsse:Username>

<wsse:Password Type="..."> ... </wsse:Password>

<wsse:Nonce EncodingType=" ... "> ... </wsse:Nonce>

<wsu:Created> ... </wsu:Created>

</wsse:UsernameToken>

The four mandatory XML elements (with highlighted values) that must be specified within

the <wsse: UsernameToken> element in the SOAP header request are:

**<wsse:Nonce> Encrypted value of a random nonce**

This element has an optional attribute EncodingType which can be used for specifying the

encoding type of the nonce. If the attribute isn’t specified then the default Base64Binary

encoding is used.

A new unique nonce value should be generated every single time a request is sent to North

FACS SOAP API for optimal security. Please be advised that this is only optional and North

FACS SOAP API does not require that or check whether the received nonce value is unique or

not.

Example:

Clear-text nonce = 1458232109983 → Encoded nonce = MTQ1ODIzMjEwOTk4Mw==

**<wsu:Created> Creation time of the SOAP request**

This element specifies the timestamp when the SOAP request is generated.

The value can be obtained by converting the current local date time to Coordinated Universal

Time (UTC).

Example: 3/17/2016 11:28 AM (EST) → 2016-03-17T16:28:29.983Z (UTC)

**<wsse:Username> Plain text userid (API user)**

Userid is provided by First Data.

**<wsse:Password> Hashed value of password of wsse:Username**

This element has attribute Type which is used for specifying the password type being

provided. It should always be #PasswordDigest.

How the value for this element is generated can be described by the following pseudo-code:

Password\_Digest = Base64 (SHA-1 (nonce + created + password))

The generated nonce (clear-text value), creation timestamp, and the password (clear-text

password) are concatenated into a combination. The combination is digested using the SHA-

1 hash algorithm. The digest result is then encoded in Based64 encoding format and the final

password digest value is produced.

The steps below demonstrate how the elements within SOAP request header is generated:

\1. Generate random nonce: 1458232109983

\2. Get Base64 of nonce: 1458232109983 → MTQ1ODIzMjEwOTk4Mw==

\3. Get current date time and convert to UTC: 3/17/2016 11:28 AM (EST) → 2016-03-

17T16:28:29.983Z (UTC)

\4. Receive password: 123456

\5. Create inner password: 14582321099832016-03-17T16:28:29.983Z123456

\6. Apply SHA1 to inner password: 14582321099832016-03-17T16:28:29.983Z123456 →

3b781af3b3cdffc4286348490b4f42c50f6df221

North Boarding API Specifications.docxSpecifications

Page 36 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\7. Get Base64 of the SHA1 digest password: 3b781af3b3cdffc4286348490b4f42c50f6df221 →

O3ga87PN/8QoY0hJC09CxQ9t8iE=

A valid SOAP request header with the above values would appear as follows;

<soapenv:Header>

<wsse:Security xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-

wssecurity-secext-1.0.xsd" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-

200401-wss-wssecurity-utility-1.0.xsd">

<wsse:UsernameToken>

<wsse:Username>apitest</wsse:Username>

<wsse:Password Type="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-

username-token-profile-1.0#PasswordDigest">

O3ga87PN/8QoY0hJC09CxQ9t8iE=</wsse:Password>

<wsse:Nonce EncodingType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-

wss-soap-message-security-1.0#Base64Binary">MTQ1ODIzMjEwOTk4Mw==</wsse:Nonce>

<wsu:Created>2016-03-17T16:28:29.983Z</wsu:Created>

</wsse:UsernameToken>

</wsse:Security>

</soapenv:Header>

Or as follows, without the attribute EncodingType of element wsse:Nonce;

<soapenv:Header>

<wsse:Security xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-

wssecurity-secext-1.0.xsd" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-

200401-wss-wssecurity-utility-1.0.xsd">

<wsse:UsernameToken>

<wsse:Username>apitest</wsse:Username>

<wsse:Password Type="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-

username-token-profile-1.0#PasswordDigest">

O3ga87PN/8QoY0hJC09CxQ9t8iE=</wsse:Password>

<wsse:Nonce>MTQ1ODIzMjEwOTk4Mw==</wsse:Nonce>

<wsu:Created>2016-03-17T16:28:29.983Z</wsu:Created>

</wsse:UsernameToken>

</wsse:Security>

</soapenv:Header>

**4.2.2.SOAP Request Body**

How the SOAP request body is constructed is based on which among the two currently

available web methods is called

**4.2.2.1.**

**SubmitMPA**

The customizable contents are highlighted.

<soapenv:Body>

<tem:SubmitMPA>

<!--Optional:-->

<tem:xmlContent>

e

<!--You may enter ANY elements at this point-->

gero

</tem:xmlContent>

North Boarding API Specifications.docxSpecifications

Page 37 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<!--Optional:-->

<tem:extRefID>?</tem:extRefID>

<!--Optional:-->

<tem:northChannel>?</tem:northChannel>

</tem:SubmitMPA>

</soapenv:Body>

**4.2.2.2.**

**GetStatusByTimeSpan**

<soapenv:Body>

<tem:GetStatusByTimeSpan>

<tem:fromTimeStamp>2016-02-24T11:00:00Z</tem:fromTimeStamp>

<tem:toTimeStamp>2016-02-24T19:00:00Z</tem:toTimeStamp>

</tem:GetStatusByTimeSpan>

</soapenv:Body>

**4.3. COMMON CONNECTIVITY ISSUES**

**4.3.1.Common issue #1: Generic Error**

**4.3.1.1.**

**Indicator**

A response as seen below is returned by North FACS API after the submission of a request;

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

<s:Body>

<s:Fault>

<faultcode>s:Client</faultcode>

<faultstring xml:lang="en-US">Generic error

occurred.</faultstring>

</s:Fault>

</s:Body>

</s:Envelope>

**4.3.1.2.**

**Cause**

There are many possible causes to this particular type of error, among which the most

common ones are:

·

If it is a request to the web method GetStatusByTimeSpan, the provided dates are not in correct

format.

·

·

Either username token or password token in the request header is not correct.

The element wsu:Created has expired. It must be re-generated at the time before the request is

sent. A large delay would cause North FACS API to consider the provided wsu:Created expired.

North Boarding API Specifications.docxSpecifications

Page 38 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**4.3.1.3.**

**Actions**

\1. Double-check username and password

\2. Log a request for issue investigation to First Data. The request must detail:

·

·

When the SOAP request was submitted

The submitting username

**4.3.2.Common issue #2: Submission failure**

**4.3.2.1.**

**Indicator**

A response comparable to the one in the screenshot below is returned by North FACS API.

More details are available in North FACS Boarding API - Basic Verification Guide.

<SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId

xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">02/16/2016 05:16:05

PM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>MPA Info - Locations field does not

reflect the number of locations added.</ErrorDescription>

</MerchantError>

</Errors>

</SubmitMPAResult>

**4.3.2.2.**

**Cause**

North Boarding API was implemented with numerous validation rules to prevent false MPA

data from being entered into the First Data system.

**4.3.2.3.**

**Actions**

If you are not aware of the existence of the validation rule or the error message(s) returned

are not informative enough, please contact First Data for further support.

The support request must provide the following information:

·

·

The username the MPA was submitted with

The XML content of the MPA

**4.3.3.Common issue #3: Submission failure without specific errors**

North Boarding API Specifications.docxSpecifications

Page 39 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**4.3.3.1.**

**Indicator**

A response comparable to the one in the screenshot below is returned by North FACS API.

More details are available i[n](#br40)[ ](#br40)[North](#br40)[ ](#br40)[FACS](#br40)[ ](#br40)[Boarding](#br40)[ ](#br40)[API](#br40)[ ](#br40)[-](#br40)[ ](#br40)[Basic](#br40)[ ](#br40)[Verification](#br40)[ ](#br40)[Guide.](#br40)

<SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId

xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">02/16/2016 05:19:12

PM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/" />

</SubmitMPAResult>

**4.3.3.2.**

**Cause**

As there should have been a clear error message indicating which validation rule was

violated that led to the submission failure, this is likely an unknown defect of North

Boarding FACS API.

**4.3.3.3.**

**Actions**

Send a support request to First Data with information about:

·

·

The username the MPA was submitted with

The XML content of the MPA

**5 Basic Verification Guides**

This will provide new users of North Boarding FACS API with a basic guide to verifying

general functions offered by North Boarding FACS API

·

·

MPA Submission via Boarding API

MPA Status Tracking for MPAs submitted via Boarding API

This document might also serve as an easy to read source of reference for readers who wish

to gain an overview of North Boarding FACS API.

*Note: Section 3.1 of this document is the high to mid – level test cases which should be utilized*

*during the verification process of North Boarding FACS API.*

This manual is composed of 4 parts.

**Part 1**

**Part 2**

**Part 3**

**Part 4**

An introduction to the document

Preparations prior to submission

MPA submission via North Boarding FACS API and required testing

Checks needed to be performed after MPA submission

North Boarding API Specifications.docxSpecifications

Page 40 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Part 5**

MPA status tracking via North Boarding FACS API

**6.1. PREPARATIONS**

The following prerequisites should be met before the action of submitting MPAs via North

Boarding FACS API takes place.

**6.1.1.Permission Settings**

Make sure that you are using a credential that has been granted sufficient permissions to use

North Boarding FACS API.

Make sure that your credential which consists of a username and a North FACS API password

is correctly supplied.

*Note: Both above conditions must be met. Otherwise, submitting MPA via North Boarding FACS*

*API is not allowed.*

**6.1.2.MPA as XML File**

Submitting MPAs via North Boarding FACS API requires the submitted MPA data to be

hosted within an XML file with each XML element corresponding to one MPA data field.

Another way to look at this is that the XML files are technically the MPAs themselves.

In the following example is a part of an XML MPA where details about equipments of the

corresponding merchant are captured:

<EquipmentFE>

<Equipments>

<Equipment>

<FrontEndFE>NASHVILLE</FrontEndFE>

<EquipmentType>CLOVER</EquipmentType>

<Model>74722</Model>

<Quantity>1</Quantity>

<BillingMethod>P</BillingMethod>

<UnitPrice>9999</UnitPrice>

<ModelFeatures>

</ModelFeatures>

<Peripherals>

<Peripheral>

<Name>OPTION</Name>

<Value>74563</Value>

<PeripheralFeatures>

<PeripheralFeature>

<Domain>TERM\_ATTR</Domain>

<Name>EMV</Name>

<Value>Y</Value>

</PeripheralFeature>

North Boarding API Specifications.docxSpecifications

Page 41 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





</PeripheralFeatures>

</Peripheral>

<Peripheral>

<Name>SOFT</Name>

<Value>65823</Value>

<PeripheralFeatures>

</PeripheralFeatures>

</Peripheral>

</Peripherals>

</Equipment>

</Equipments>

</EquipmentFE>

i *It is advisable that the XML files are well formed for ease of (MPA) data management and*

*testing.*

**6.1.3.XML Elements Ordering**

It is mandatory that XML elements are laid out in an order that matches with one in schema

file of North Boarding FACS API.

Should there be any difference between that order and the predefined one by the schema,

MPA submission via North Boarding FACS API will not be permitted. The action of submitting

an incorrectly ordered MPA will always result in what we would normally call the ‘schema’

error, of which an example is displayed below. Please also note that failing to include a

mandatory element or including one invalid element will also cause the validation performed

against the North FACS schema to fail and produce issues of similar natures, but with various

error messages depending on the input elements in each case.

<SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">02/18/2016 11:58:50 AM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>The element 'OtherFees' has invalid child element

'AuthAmericanExpressFee'. List of possible elements expected:

'AVSMCVisaDiscoverAmexVoice, AuthMCVisaDiscoverAmexVoiceFee, AVSFee,

AuthMCVisaDiscoverAmexVoiceFeeIssuerReferral, ProductFDMobilePayMonthlyFee,

ProductFDMobilePaySetupFee, ProductMCGEPServiceFee, ProductVisaGEPServiceFee,

ProductCloverAndTransArmorServicesFeeMonthyPerStation,

North Boarding API Specifications.docxSpecifications

Page 42 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





ProductCloverAndTransArmorServicesFeeQuantity, ProductInsighticsSolution,

ProductPERKASolution'.</ErrorDescription>

<LineNumber>459</LineNumber>

<ColumnNumber>6</ColumnNumber>

</MerchantError>

</Errors>

</SubmitMPAResult>

**6.1.4.Unspecified MPA Fields**

The total number of MPA data elements that are passed to the North API is roughly 476 fields.

But not all MPA elements are required to be present at the time of submissions. You can opt

to leave the optional MPA input fields unspecified either by completely removing the

associated XML tags from the MPA XML file or adding a special null namespace to them, as

illustrated by the example below:

<Prin1FirstName>JON</Prin1FirstName>

<Prin1LastName>CONSUMER</Prin1LastName>

<Prin1MiddleInitial>M</Prin1MiddleInitial>

<Prin1OwnershipPercent>100</Prin1OwnershipPercent>

<Prin1GuarantorCode>0</Prin1GuarantorCode>

<Prin1Title>1</Prin1Title>

<Prin1Address>1322 MORRIS</Prin1Address>

<Prin1City>BRONX</Prin1City>

<Prin1State>NY</Prin1State>

<Prin1First5Zip>10456</Prin1First5Zip>

<Prin1Phone>6468949236</Prin1Phone>

<Prin1FirstName>JON</Prin1FirstName>

<Prin1LastName>CONSUMER</Prin1LastName>

<Prin1MiddleInitial>M</Prin1MiddleInitial>

<Prin1OwnershipPercent>100</Prin1OwnershipPercent>

<Prin1GuarantorCode>0</Prin1GuarantorCode>

<Prin1Title>1</Prin1Title>

<Prin1Address>999 ELM STREET</Prin1Address>

<Prin1City>BRONX</Prin1City>

<Prin1State>NY</Prin1State>

<Prin1First5Zip>10456</Prin1First5Zip>

<Prin1Last4Zip

xsi:nil="true"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-

instance"></Prin1Last4Zip>

<Prin1Phone>6468949236</Prin1Phone>

All three options will produce the same result: Prin1Last4Zip is not specified.

North Boarding API Specifications.docxSpecifications

Page 43 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**6.1.5.Using Master Mapping**

The master mapping document for North FACS API is very useful in that it contains a lot of

information that can be used to customize and control the input XMLs more effectively.

The most basic information you can obtain from the document includes:

·

·

·

·

XML Path: The parent XML element representing MPA section

XML Field: The XML element representing the MPA input field within the MPA section

Type: Input type of the MPA input field

Length/Range: Maximum allowed length of the MPA input field/Minimum value – Maximum value

of the MPA input field

·

·

Required: Indicator of whether the field is a mandatory input

Enumeration Values: Selectable values in case the input type of the MPA input field is “Select List”

**6.1.6.Starting XML File**

Given the total number of XML elements, it is a lot more preferable to have a prepared XML

file for testing than to have to build a new XML file from scratch.

Based on North FACS API master mapping, various modifications can be made to this starting

XML file to address different testing purposes.

**6.2. MERCHANT APPLICATION SUBMISSION**

Once all the preparation steps are completed, North Boarding FACS API should be ready for

verification.

**6.2.1.High-level Test Cases**

**6.2.1.1.**

**Successful Submission**

North Boarding API Specifications.docxSpecifications

Page 44 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**TEST CASE**

Successful submission

**SUMMARY**

The best working flow starts with a successul submission of MPA via Boarding API. It is also a

pre-condition to further verfication of North Boarding FACS API.

You need to make sure that all data pieces of the to-be-submitted MPA are present in the XML

file and they being put together complies with the all the implemented business validation and

field validation rules.

**INPUT**

XML with MPA data pass all business validations and field validations

**OUTPUT** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<ASRefId xmlns="http://tempuri.org/">3489</ASRefId>

<Timestamp xmlns="http://tempuri.org/">02/18/2016 02:28:09

PM</Timestamp>

<Status xmlns="http://tempuri.org/">SUCCESS</Status>

<Errors xmlns="http://tempuri.org/" />

</SubmitMPAResult>

**6.2.1.2.**

**Field-Level Validation**

**TEST CASE**

Failed submission due to failed validation of field input rule(s)

**SUMMARY**

Each XML element (MPA input field) has its own input rule, with regards to input type (text,

number, boolean), input legnth, and input range (min value, max value).

North Boarding API Specifications.docxSpecifications

Page 45 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Example: For XML elements Prin1FirstName and Prin1LastName you are not allowed to enter

values whose length is less than 2 characters.

**INPUT**

XML containing a field specified with a value that violates the field’s input rule

which decides data type, length, or range, e.g. put in ‘J’ for both Prin1FirstName

and Prin1LastName

**OUTPUT** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">02/18/2016 02:31:35

PM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>The 'Prin1FirstName' element is invalid - The value 'J' is

invalid according to its datatype 'String' - The actual length is less than the

MinLength value.</ErrorDescription>

<LineNumber>41</LineNumber>

<ColumnNumber>22</ColumnNumber>

</MerchantError>

<MerchantError>

<ErrorId>2</ErrorId>

<ErrorDescription>The 'Prin1LastName' element is invalid - The value 'J' is

invalid according to its datatype 'String' - The actual length is less than the

MinLength value.</ErrorDescription>

<LineNumber>42</LineNumber>

<ColumnNumber>21</ColumnNumber>

</MerchantError>

</Errors>

</SubmitMPAResult>

**NOTES**

It is not necessary to verify each and every XML element, so to save time there is

a shorter approach to this: Verification of field input rules can be performed on

North Boarding API Specifications.docxSpecifications

Page 46 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





the North Boarding FACS API schema file instead of the North Boarding FACS API

itself.

This approach is possible because all the field-level input validation rules are

implemented only in North Boarding FACS API schema.

**6.2.2.3.**

**Faulty Data Validation**

**TEST CASE**

Failed submission due to MPA containing faulty or non-existent data

**SUMMARY**

For seletable MPA fields with values subject to changes like BANK/AGENT (from here onward

regarded as **dynamic selectable fields**), North Boarding FACS Web has a way to limit user inputs

down to a number of currently available values. The result of that is user cannot enter values

not among the allowed selectable values.

North Boarding FACS API uses a different way to prevent faulty data from entering through the

API tool.

**INPUT**

MPA that contains faulty data, e.g. a non-existent SYS number

**OUTPUT** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">02/18/2016 02:40:27

PM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>MPA Info - The Bank is not assigned.</ErrorDescription>

</MerchantError>

<MerchantError>

<ErrorId>2</ErrorId>

<ErrorDescription>MPA Info - The Agent is not assigned.</ErrorDescription>

</MerchantError>

</Errors>

North Boarding API Specifications.docxSpecifications

Page 47 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





</SubmitMPAResult>

**6.2.2.4.**

**Input Data Validation**

**TEST CASE**

Failed submission due to MPA containing invalid data, i.e. not within the list of pre-defined

values

**SUMMARY**

There are certain XML tags whose input values must fall into a pre-defined list. From here

onward these will be refered to as **“static selectable fields”.**

Example: XML tag BusinessType can only have one of the following values:

C

L

CAR RENTAL

LODGING

M

O

P

SUPERMARKET

MOTO/Internet

PETROLEUM

QSR

Q

R

S

RETAIL

RESTAURANT

An error message that contains the phrase “The Enumeration constraint failed” is expected.

**INPUT**

MPA XML with at least one tag with specified value that lies outside the allowed

list of values.

**OUTPUT** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">02/18/2016 02:53:14

PM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

North Boarding API Specifications.docxSpecifications

Page 48 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ErrorId>1</ErrorId>

<ErrorDescription>The 'IndustryType' element is invalid - The value 'W' is

invalid according to its datatype 'String' - The Enumeration constraint

failed.</ErrorDescription>

<LineNumber>111</LineNumber>

<ColumnNumber>22</ColumnNumber>

</MerchantError>

</Errors>

</SubmitMPAResult>

**NOTES**

Changes have been, and might be made to the pre-defined lists of static selectable

values as required by future change requests.

**6.2.2.5.**

**Business Vlidation**

**TEST CASE**

Failed submission due to information supplied within MPA does not comply with one or more

business validation rule

**SUMMARY**

Many business validation rules are applied to the MPA submission process to preserve data

integrity, which will mean a successful VAPP transmission.

**INPUT**

MPA XML with at least one XML tag with data entered in such a way that at least

one business validation rule is violated.

**OUTPUT** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">02/18/2016 03:04:55

PM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

North Boarding API Specifications.docxSpecifications

Page 49 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ErrorId>1</ErrorId>

<ErrorDescription>Location 01: Equipment and FE - Invalid FrontEnd/EBT

Combination</ErrorDescription>

</MerchantError>

</Errors>

</SubmitMPAResult>

**NOTES**

The North Boarding FACS API SRS and the North FACS Master BRS Rules

spreadsheet can be used as a reference for business rules currently in place for

North Boarding FACS.

**6.2.2.6.**

**Multi-Location versus Single-Location**

**TEST CASE**

Submission of XML of merchant with more than one outlets

**SUMMARY**

One single MPA can contain up to 99 outlets. It is important that all functionalities and features

offered by North Boarding FACS API still work as intended when more than one outlets are

included in submitted MPAs

**INPUT**

MPA XML with more than one outlet

**OUTPUT** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">02/18/2016 03:04:55

PM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>Location 01: Equipment and FE - Invalid FrontEnd/EBT

Combination</ErrorDescription>

<ErrorId>2</ErrorId>

North Boarding API Specifications.docxSpecifications

Page 50 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ErrorDescription>Location 02: Equipment and FE - Invalid FrontEnd/EBT

Combination</ErrorDescription>

</MerchantError>

</Errors>

</SubmitMPAResult>

**NOTES**

Please notice that each error descripition is preceded by Location NN in which NN

is the ordial number of the outlet corresponding to the error.

**6.2.2.7.**

**Field Interdependencies**

**TEST CASE**

Failed submisison due to incompatible MPA data

**SUMMARY**

There are a number of input rules applied on MPA data fields to make sure VAPP tramission is

successful.

For North Boarding FACS Web, those rules are reflected by the JavaScript-coded Show/Hide

mechanism which makes certain fields available for inputting only when special conditions are

met, e.g. a checkbox is checked off.

Example: AMEX SE Number is available only when AMEX Direct

**INPUT**

MPA XML with at least one XML element incompatible with currently available

selecions

North Boarding API Specifications.docxSpecifications

Page 51 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**OUTPUT** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">10/15/2015 02:53:03

AM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>Location 01: Other Entitlements – SE Number is not

compatible with entered AMEX Direct</ErrorDescription>

</MerchantError>

</Errors>

</SubmitMPAResult>

**6.2.3.Common Issues**

**6.2.3.1.**

**XML response**

After a merchant application is submitted, North Boarding FACS API will return an XML

response which is are structured as follows:

Success Message Response Sample XML

<SubmitMPAResponse>

<SubmitMPAResult>

<ExternalRefId>123456789</ExternalRefId>

<ASRefId>123</ASRefId>

<Timestamp>2014-09-30 00:00:00.000</Timestamp>

<Status>SUCCESS</Status>

</SubmitMPAResult>

</SubmitMPAResponse>

Failure Message Response Sample XML

<SubmitMPAResponse>

<SubmitMPAResult>

<ExternalRefId>234567890</ExternalRefId>

<ASRefId>234</ASRefId>

<Timestamp>2014-09-30 00:00:00.000</Timestamp>

<Status>FAILURE</Status>

<Errors>

<MerchantError>

North Boarding API Specifications.docxSpecifications

Page 52 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ErrorId>1</ErrorId>

<ErrorDescription></ErrorDescription>

<LineNumber/>

<ColumnNumber/>

</MerchantError>

</Errors>

</SubmitMPAResult>

</SubmitMPAResponse>

ExternalRefId: The external Ref Id received from Client.

ASRefId: The MPA ID generated from Fiserv Boarding system in case of success. It will be

blank in case of failure.

Timestamp: The date time stamp of success or failure of the submission.

Status: The MPA XML Content passes the validation, it will be SUCCESS. Otherwise, it will be

FAILURE.

Errors: MerchantError tags – Only applicable if the MPA XML Content fails against the

validation.

MerchantError: Multiple errors received while XSD validation as well as error that relates to

MPA edits of boarding merchant.

•

•

•

•

ErrorId: The error #.

ErrorDescription: The description of merchant error.

LineNumber: The Error Line #. It could be sent as empty tag.

ColumnNumber: The Error Column #. It could be sent as empty tag.

**6.2.3.2.**

**Generic Error Message**

There will be times when the XML response does not provide any useful information

regarding what results in submission failure.

Generic Failure Message Response Sample XML

<SubmitMPAResponse>

<SubmitMPAResult>

<ExternalRefId>234567890</ExternalRefId>

<ASRefId>234</ASRefId>

<Timestamp>2014-09-30 00:00:00.000</Timestamp>

<Status>FAILURE</Status>

</SubmitMPAResult>

</SubmitMPAResponse>

There are a lot of possible reasons to this highly undesirable scenario and the best action to

take is having a look at the API log file API\_Log.txt yourself or asking for assistance from

involved parties.

Note: API\_Log.txt contains more detailed information and might help a lot in identifying the

cause of the submission failure.

North Boarding API Specifications.docxSpecifications

Page 53 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**6.2.3.3.**

**Specific Error Message**

In scenarios where specific error messages are included in the XML response, just follow the

instructions, together with related sections to get the errors sorted.

**6.3. POST-MERCHANT SUBMISSION**

Post-submission testing with a specifcal merchant application can only be performed after a

successful submission.

Note: ASRefId is needed.

**6.3.1.Front-End Data**

All MPAs submitted via North Boarding FACS API can be viewed or modified on North

Boarding FACS Web providing that:

·

·

·

MPAs of type API-STD are configured to be routed to Client Approval stage after submission

Approval Group settings are correct and already in place

Approver credential is needed to access AccessOne > One Stop > Client Approval Queue

**6.3.2.Exported PDFs**

Data displayed on exported PDFs should be compared to the data specified in the submitted

XML elements to be certain of correctness, taking into consideration all alterations that have

been made to original submitted data.

**6.4. MPA STATUS TRACKING**

To retrieve the current status of successfully submitted MPAs, you need to provide two pieces

of information, which are:

**Name**

**Data Type**

**Type Category**

**Description**

FromTimeStamp

DateTime in UTC (ISO 8601) simpleType

format

Value must be

within the last 72

hours from the

current time

ToTimeStamp

DateTime in UTC (ISO 8601) simpleType

format

Value must be

greater

than

FromTimeStamp

Note: Any request with the FromTimeStamp more than 72 hours away from the current time

will not be considered a valid request and thus, will receive no information about MPA status.

Each status change event of a submitted MPA is associated with a timestamp. In another word

if a status change event is more than 72 hours old compared to the current date time, it is will

not be retrievable.

North Boarding API Specifications.docxSpecifications

Page 54 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**6.4.1. Successful Status Retrieval**

Example

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

<s:Body

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

xmlns:xsd="http://www.w3.org/2001/XMLSchema">

<GetStatusByTimeSpanResponse xmlns="http://tempuri.org/">

<GetStatusByTimeSpanResult>

<GetStatusByTimeSpanResult>

<MerchantApplicationStatus>

<ASRefId>3489</ASRefId>

<FDMerchantNumber/>

<Status>

<MerchantDetails>

<NorthNumber/>

<CloverID/>

<LocationNumber>1</LocationNumber>

<DBAName>MMIS FDTST 0217 TT</DBAName>

<CardnetNumber/>

<MerchantStatus>

<AppStatus>

<Code>MPAKey</Code>

<Information>In Process</Information>

<Timestamp>2/18/2016 2:28:06 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MPA</Code>

<Information>In Process</Information>

<Timestamp>2/18/2016 2:28:06 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MpaKey</Code>

<Information>Submitted</Information>

<Timestamp>2/18/2016 2:28:08 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>ClientApproval</Code>

<Information>Direct Send</Information>

<Timestamp>2/18/2016 2:28:08 PM</Timestamp>

</AppStatus>

<AppStatus>

North Boarding API Specifications.docxSpecifications

Page 55 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<Code>Transmission</Code>

<Information>In Process</Information>

<Timestamp>2/18/2016 2:30:03 PM</Timestamp>

</AppStatus>

</MerchantStatus>

<EquipmentDetails/>

</MerchantDetails>

</Status>

<Errors/>

<CreditOfficerComments/>

</MerchantApplicationStatus>

<MerchantApplicationStatus>

<ASRefId>3490</ASRefId>

<FDMerchantNumber/>

<Status>

<MerchantDetails>

<NorthNumber/>

<CloverID/>

<LocationNumber>1</LocationNumber>

<DBAName>MMIS FDTST 0217 TT</DBAName>

<CardnetNumber/>

<MerchantStatus>

<AppStatus>

<Code>MPAKey</Code>

<Information>In Process</Information>

<Timestamp>2/18/2016 2:40:07 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MPA</Code>

<Information>In Process</Information>

<Timestamp>2/18/2016 2:40:07 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MpaKey</Code>

<Information>Submitted</Information>

<Timestamp>2/18/2016 2:40:09 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>ClientApproval</Code>

<Information>Direct Send</Information>

North Boarding API Specifications.docxSpecifications

Page 56 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<Timestamp>2/18/2016 2:40:09 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>Transmission</Code>

<Information>In Process</Information>

<Timestamp>2/18/2016 2:42:02 PM</Timestamp>

</AppStatus>

</MerchantStatus>

<EquipmentDetails/>

</MerchantDetails>

</Status>

<Errors/>

<CreditOfficerComments/>

</MerchantApplicationStatus>

<MerchantApplicationStatus>

<ASRefId>3491</ASRefId>

<FDMerchantNumber/>

<Status>

<MerchantDetails>

<NorthNumber/>

<CloverID/>

<LocationNumber>1</LocationNumber>

<DBAName>MMIS FDTST 0217 TT</DBAName>

<CardnetNumber/>

<MerchantStatus>

<AppStatus>

<Code>MPAKey</Code>

<Information>In Process</Information>

<Timestamp>2/18/2016 2:48:04 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MPA</Code>

<Information>In Process</Information>

<Timestamp>2/18/2016 2:48:04 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MpaKey</Code>

<Information>Submitted</Information>

<Timestamp>2/18/2016 2:48:08 PM</Timestamp>

</AppStatus>

North Boarding API Specifications.docxSpecifications

Page 57 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<AppStatus>

<Code>ClientApproval</Code>

<Information>Direct Send</Information>

<Timestamp>2/18/2016 2:48:08 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>Transmission</Code>

<Information>In Process</Information>

<Timestamp>2/18/2016 2:51:02 PM</Timestamp>

</AppStatus>

</MerchantStatus>

<EquipmentDetails/>

</MerchantDetails>

</Status>

<Errors/>

<CreditOfficerComments/>

</MerchantApplicationStatus>

</GetStatusByTimeSpanResult>

</GetStatusByTimeSpanResult>

</GetStatusByTimeSpanResponse>

</s:Body>

</s:Envelope>

**6.4.2. Failed Status Retrieval**

Example

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

<s:Body

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

xmlns:xsd="http://www.w3.org/2001/XMLSchema">

<GetStatusByTimeSpanResponse xmlns="http://tempuri.org/">

<GetStatusByTimeSpanResult>

<GetStatusByTimeSpanResult>

<MerchantApplicationStatus>

<ASRefId/>

<FDMerchantNumber/>

<Status>

<MerchantDetails>

<OmahaNumber/>

<LocationNumber/>

<DBAName/>

<CardnetNumber/>

North Boarding API Specifications.docxSpecifications

Page 58 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<MerchantStatus>

<AppStatus>

<Code/>

<Information>No record found against the specified timespan.</Information>

<Timestamp>02/18/2016 15:58:50 PM</Timestamp>

</AppStatus>

</MerchantStatus>

</MerchantDetails>

</Status>

<Errors/>

<CreditOfficerComments/>

</MerchantApplicationStatus>

</GetStatusByTimeSpanResult>

</GetStatusByTimeSpanResult>

</GetStatusByTimeSpanResponse>

</s:Body>

</s:Envelope>

**7. Frequently Asked Questions**

North Boarding API Specifications.docxSpecifications

Page 59 of 59

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.

