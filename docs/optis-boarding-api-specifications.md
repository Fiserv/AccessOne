

**“OMAHA BOARDING API SPECIFICATIONS”**

1





**1**

TABLE OF **CONTENTS**

[**1**](#br4)

[**Introduction.......................................................................................................................4**](#br4)

[1.1](#br4)

[1.2](#br5)

[Intended](#br4)[ ](#br4)[Audience](#br4)[ ](#br4)[and](#br4)[ ](#br4)[Reading](#br4)[ ](#br4)[Suggestions](#br4)[ ](#br4)[....................................................................................](#br4)[ ](#br4)[4](#br4)

[Project](#br5)[ ](#br5)[Scope](#br5)[ ](#br5)[....................................................................................................................................](#br5)[ ](#br5)[5](#br5)

[**2**](#br6)

[**3**](#br7)

[**Requirements.....................................................................................................................6**](#br6)

[2.1.1](#br6)[ ](#br6)[Test](#br6)[ ](#br6)[IP](#br6)[ ](#br6)[address](#br6)[ ](#br6)[&](#br6)[ ](#br6)[url..............................................................................................................................](#br6)[ ](#br6)[6](#br6)

[2.1.1](#br6)[ ](#br6)[Security](#br6)[ ](#br6)[................................................................................................................................................](#br6)[ ](#br6)[6](#br6)

[**Request**](#br7)[** ](#br7)[format**](#br7)[** ](#br7)[..................................................................................................................7**](#br7)

[3.1](#br8)

[SOAP](#br8)[ ](#br8)[Envelope](#br8)[ ](#br8)[.................................................................................................................................](#br8)[ ](#br8)[8](#br8)

[3.1.1](#br8)[ ](#br8)[Request](#br8)[ ](#br8)[Body........................................................................................................................................](#br8)[ ](#br8)[8](#br8)

[3.1.1](#br9)[ ](#br9)[MPA](#br9)[ ](#br9)[as](#br9)[ ](#br9)[xml](#br9)[ ](#br9)[file](#br9)[ ](#br9)[.....................................................................................................................................](#br9)[ ](#br9)[9](#br9)

[3.1.1](#br9)[ ](#br9)[Order](#br9)[ ](#br9)[of](#br9)[ ](#br9)[XML](#br9)[ ](#br9)[Tags................................................................................................................................](#br9)[ ](#br9)[9](#br9)

[3.1.1](#br10)[ ](#br10)[Unspecified](#br10)[ ](#br10)[MPA](#br10)[ ](#br10)[Fields.......................................................................................................................](#br10)[ ](#br10)[10](#br10)

[using](#br11)[ ](#br11)[master](#br11)[ ](#br11)[mapping](#br11)[ ](#br11)[document](#br11)[ ](#br11)[.....................................................................................................11](#br11)

[3.2](#br11)

[**4**](#br12)

[**5**](#br17)

[**ws-security**](#br12)[** ](#br12)[authentication**](#br12)[** ](#br12)[..............................................................................................12**](#br12)

[4.1.1](#br14)[ ](#br14)[Soap](#br14)[ ](#br14)[ui](#br14)[ ](#br14)[project](#br14)[ ](#br14)[....................................................................................................................................](#br14)[ ](#br14)[14](#br14)

[**Boarding**](#br17)[** ](#br17)[API**](#br17)[** ](#br17)[Methods**](#br17)[** ](#br17)[.....................................................................................................17**](#br17)

[5.1.1](#br17)[ ](#br17)[Submit](#br17)[ ](#br17)[MPA](#br17)[ ](#br17)[Method](#br17)[ ](#br17)[...........................................................................................................................17](#br17)

[5.2](#br20)

[Get](#br20)[ ](#br20)[Status](#br20)[ ](#br20)[By](#br20)[ ](#br20)[TimeSpan](#br20)[ ](#br20)[Method.....................................................................................................](#br20)[ ](#br20)[20](#br20)

[5.2.1](#br25)[ ](#br25)[Enable](#br25)[ ](#br25)[the](#br25)[ ](#br25)[ability](#br25)[ ](#br25)[to](#br25)[ ](#br25)[pull](#br25)[ ](#br25)[Cardnet](#br25)[ ](#br25)[TID](#br25)[ ](#br25)[and](#br25)[ ](#br25)[Cardnet](#br25)[ ](#br25)[Number](#br25)[ ](#br25)[.................................................................](#br25)[ ](#br25)[25](#br25)

[5.2.1](#br27)[ ](#br27)[Enable](#br27)[ ](#br27)[the](#br27)[ ](#br27)[ability](#br27)[ ](#br27)[to](#br27)[ ](#br27)[pull](#br27)[ ](#br27)[Nashville](#br27)[ ](#br27)[MID](#br27)[ ](#br27)[and](#br27)[ ](#br27)[Nashville](#br27)[ ](#br27)[TID](#br27)[ ](#br27)[....................................................................](#br27)[ ](#br27)[27](#br27)

[5.2.1](#br29)[ ](#br29)[Enable](#br29)[ ](#br29)[the](#br29)[ ](#br29)[ability](#br29)[ ](#br29)[to](#br29)[ ](#br29)[pull](#br29)[ ](#br29)[Omaha](#br29)[ ](#br29)[BE](#br29)[ ](#br29)[MID](#br29)[ ](#br29)[and](#br29)[ ](#br29)[Omaha](#br29)[ ](#br29)[Download](#br29)[ ](#br29)[ID......................................................](#br29)[ ](#br29)[29](#br29)

[5.2.1](#br34)[ ](#br34)[Enable](#br34)[ ](#br34)[the](#br34)[ ](#br34)[ability](#br34)[ ](#br34)[to](#br34)[ ](#br34)[pull](#br34)[ ](#br34)[Datawire](#br34)[ ](#br34)[DID](#br34)[ ](#br34)[................................................................................................](#br34)[ ](#br34)[34](#br34)

[5.2.1](#br35)[ ](#br35)[Enable](#br35)[ ](#br35)[the](#br35)[ ](#br35)[ability](#br35)[ ](#br35)[to](#br35)[ ](#br35)[back](#br35)[ ](#br35)[Clover](#br35)[ ](#br35)[ID](#br35)[ ](#br35)[.....................................................................................................](#br35)[ ](#br35)[35](#br35)

[5.2.1](#br36)[ ](#br36)[Enable](#br36)[ ](#br36)[the](#br36)[ ](#br36)[ability](#br36)[ ](#br36)[to](#br36)[ ](#br36)[pull](#br36)[ ](#br36)[Rapid](#br36)[ ](#br36)[Connect](#br36)[ ](#br36)[ID](#br36)[ ](#br36)[..........................................................................................](#br36)[ ](#br36)[36](#br36)

[5.2.1](#br37)[ ](#br37)[Enable](#br37)[ ](#br37)[the](#br37)[ ](#br37)[ability](#br37)[ ](#br37)[to](#br37)[ ](#br37)[pull](#br37)[ ](#br37)[Buypass](#br37)[ ](#br37)[MID](#br37)[ ](#br37)[and](#br37)[ ](#br37)[Buypass](#br37)[ ](#br37)[TID........................................................................37](#br37)

[5.2.1](#br39)[ ](#br39)[retrieve](#br39)[ ](#br39)[full](#br39)[ ](#br39)[mpa](#br39)[ ](#br39)[method.....................................................................................................................](#br39)[ ](#br39)[39](#br39)

[Retrieve](#br40)[ ](#br40)[mpa](#br40)[ ](#br40)[–](#br40)[ ](#br40)[testing](#br40)[ ](#br40)[support](#br40)[ ](#br40)[........................................................................................................](#br40)[ ](#br40)[40](#br40)

[5.3](#br40)

[5.4](#br41)

[MPA](#br41)[ ](#br41)[Status](#br41)[ ](#br41)[Reporting](#br41)[ ](#br41)[.....................................................................................................................](#br41)[ ](#br41)[41](#br41)

Omaha Boarding Specification.docx

Page 2 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





[5.5](#br46)

[Merchant](#br46)[ ](#br46)[Information](#br46)[ ](#br46)[XML](#br46)[ ](#br46)[Format](#br46)[ ](#br46)[.................................................................................................](#br46)[ ](#br46)[46](#br46)

[5.5.1](#br46)[ ](#br46)[sample](#br46)[ ](#br46)[xml..........................................................................................................................................](#br46)[ ](#br46)[46](#br46)

[Merchant](#br46)[ ](#br46)[Information](#br46)[ ](#br46)[Validation](#br46)[ ](#br46)[Handler........................................................................................](#br46)[ ](#br46)[46](#br46)

[Conditional](#br47)[ ](#br47)[Data](#br47)[ ](#br47)[Logic](#br47)[ ](#br47)[Validation....................................................................................................](#br47)[ ](#br47)[47](#br47)

[5.6](#br46)

[5.7](#br47)

[**6**](#br71)

[**High**](#br71)[** ](#br71)[Level**](#br71)[** ](#br71)[Test**](#br71)[** ](#br71)[Cases**](#br71)[** ](#br71)[......................................................................................................71**](#br71)

[6.1](#br71)

[Starting](#br71)[ ](#br71)[XML](#br71)[ ](#br71)[File](#br71)[ ](#br71)[..............................................................................................................................71](#br71)

[1.](#br71)[ ](#br71)[Successful](#br71)[ ](#br71)[Submission..............................................................................................................................71](#br71)

[2.](#br72)[ ](#br72)[Field](#br72)[ ](#br72)[Input](#br72)[ ](#br72)[Validation...............................................................................................................................](#br72)[ ](#br72)[72](#br72)

[3.](#br73)[ ](#br73)[Faulty](#br73)[ ](#br73)[Data](#br73)[ ](#br73)[Validation](#br73)[ ](#br73)[..............................................................................................................................73](#br73)

[4.](#br75)[ ](#br75)[Input](#br75)[ ](#br75)[Data](#br75)[ ](#br75)[Validity....................................................................................................................................75](#br75)

[5.](#br77)[ ](#br77)[Business](#br77)[ ](#br77)[Validation...................................................................................................................................77](#br77)

[6.](#br78)[ ](#br78)[Wholesale](#br78)[ ](#br78)[versus](#br78)[ ](#br78)[Retail](#br78)[ ](#br78)[...........................................................................................................................](#br78)[ ](#br78)[78](#br78)

[7.](#br79)[ ](#br79)[Multi-Location](#br79)[ ](#br79)[versus](#br79)[ ](#br79)[Single-Location](#br79)[ ](#br79)[.....................................................................................................](#br79)[ ](#br79)[79](#br79)

[8.](#br80)[ ](#br80)[MPA](#br80)[ ](#br80)[Fields](#br80)[ ](#br80)[Inter-Dependencies](#br80)[ ](#br80)[...............................................................................................................](#br80)[ ](#br80)[80](#br80)

[9.](#br81)[ ](#br81)[Conditional](#br81)[ ](#br81)[Data](#br81)[ ](#br81)[Validation](#br81)[ ](#br81)[.....................................................................................................................](#br81)[ ](#br81)[81](#br81)

[Common](#br82)[ ](#br82)[issues](#br82)[ ](#br82)[...............................................................................................................................](#br82)[ ](#br82)[82](#br82)

[6.2.1](#br82)[ ](#br82)[XML](#br82)[ ](#br82)[response](#br82)[ ](#br82)[.....................................................................................................................................](#br82)[ ](#br82)[82](#br82)

[6.2.1](#br83)[ ](#br83)[Generic](#br83)[ ](#br83)[Error](#br83)[ ](#br83)[Message](#br83)[ ](#br83)[........................................................................................................................](#br83)[ ](#br83)[83](#br83)

[6.2.1](#br83)[ ](#br83)[Specific](#br83)[ ](#br83)[Error](#br83)[ ](#br83)[Message](#br83)[ ](#br83)[........................................................................................................................](#br83)[ ](#br83)[83](#br83)

[Post](#br84)[ ](#br84)[MPA](#br84)[ ](#br84)[Submission](#br84)[ ](#br84)[Checks..........................................................................................................](#br84)[ ](#br84)[84](#br84)

[6.2](#br82)

[6.3](#br84)

[6.4](#br84)

[6.5](#br84)

[6.6](#br85)

[Front-End](#br84)[ ](#br84)[Data................................................................................................................................](#br84)[ ](#br84)[84](#br84)

[Stored](#br84)[ ](#br84)[Data](#br84)[ ](#br84)[.....................................................................................................................................](#br84)[ ](#br84)[84](#br84)

[Exported](#br85)[ ](#br85)[PDFs.................................................................................................................................](#br85)[ ](#br85)[85](#br85)

[**7**](#br85)

[**SOAP**](#br85)[** ](#br85)[Request**](#br85)[** ](#br85)[Guide**](#br85)[** ](#br85)[........................................................................................................85**](#br85)

[7.1](#br85)

[7.2](#br85)

[Prerequisite](#br85)[ ](#br85)[Checks](#br85)[ ](#br85)[.........................................................................................................................](#br85)[ ](#br85)[85](#br85)

[Configuring](#br85)[ ](#br85)[SOAP](#br85)[ ](#br85)[UI](#br85)[ ](#br85)[.......................................................................................................................](#br85)[ ](#br85)[85](#br85)

[7.3](#br86)

[7.4](#br87)

[7.5](#br92)

[Initiate](#br86)[ ](#br86)[SOAP](#br86)[ ](#br86)[Project](#br86)[ ](#br86)[Workspace](#br86)[ ](#br86)[........................................................................................................](#br86)[ ](#br86)[86](#br86)

[Set](#br87)[ ](#br87)[up](#br87)[ ](#br87)[Security](#br87)[ ](#br87)[and](#br87)[ ](#br87)[Authentication](#br87)[ ](#br87)[.....................................................................................................](#br87)[ ](#br87)[87](#br87)

[Start](#br92)[ ](#br92)[SOAP](#br92)[ ](#br92)[Request](#br92)[ ](#br92)[Submission](#br92)[ ](#br92)[.........................................................................................................](#br92)[ ](#br92)[92](#br92)

[8](#br92)

[Submitting](#br92)[ ](#br92)[SOAP](#br92)[ ](#br92)[Requests](#br92)[ ](#br92)[.............................................................................................................](#br92)[ ](#br92)[92](#br92)

[8.1](#br93)

[Web](#br93)[ ](#br93)[method](#br93)[ ](#br93)[SubmitMPA](#br93)[ ](#br93)[...................................................................................................................](#br93)[ ](#br93)[93](#br93)

Omaha Boarding Specification.docx

Page 3 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





[8.3](#br96)

[8.5](#br97)

[Web](#br96)[ ](#br96)[method](#br96)[ ](#br96)[RetrieveMPAXML](#br96)[ ](#br96)[..........................................................................................................](#br96)[ ](#br96)[96](#br96)

[Web](#br97)[ ](#br97)[method](#br97)[ ](#br97)[GetStatusByTimeSpan...................................................................................................](#br97)[ ](#br97)[97](#br97)

[11](#br99)

[12](#br99)

[Connectivity](#br99)[ ](#br99)[verification](#br99)[ ](#br99)[via](#br99)[ ](#br99)[an](#br99)[ ](#br99)[external](#br99)[ ](#br99)[tool....................................................................................](#br99)[ ](#br99)[99](#br99)

[SOAP](#br99)[ ](#br99)[Request](#br99)[ ](#br99)[Header.....................................................................................................................](#br99)[ ](#br99)[99](#br99)

[12.1](#br100)

[12.2](#br102)

[SOAP](#br100)[ ](#br100)[Header](#br100)[ ](#br100)[Structure](#br100)[ ](#br100)[....................................................................................................................](#br100)[ ](#br100)[100](#br100)

[SOAP](#br102)[ ](#br102)[Header](#br102)[ ](#br102)[Example......................................................................................................................](#br102)[ ](#br102)[102](#br102)

[13](#br102)

[12](#br105)

[SOAP](#br102)[ ](#br102)[Request](#br102)[ ](#br102)[Body](#br102)[ ](#br102)[......................................................................................................................](#br102)[ ](#br102)[102](#br102)

[13.1](#br102)

[13.2](#br103)

[SOAP](#br102)[ ](#br102)[Body](#br102)[ ](#br102)[Structure........................................................................................................................](#br102)[ ](#br102)[102](#br102)

[SOAP](#br103)[ ](#br103)[Body](#br103)[ ](#br103)[Example..........................................................................................................................103](#br103)

[Common](#br105)[ ](#br105)[issue](#br105)[ ](#br105)[#1:](#br105)[ ](#br105)[Generic](#br105)[ ](#br105)[Error](#br105)[ ](#br105)[....................................................................................................105](#br105)

[12.1.1](#br105)[ ](#br105)[Indicator](#br105)[ ](#br105)[...........................................................................................................................................105](#br105)

[12.1.1](#br105)[ ](#br105)[Cause................................................................................................................................................105](#br105)

[12.1.1](#br105)[ ](#br105)[Actions..............................................................................................................................................105](#br105)

[Common](#br105)[ ](#br105)[issue](#br105)[ ](#br105)[#2:](#br105)[ ](#br105)[Submission](#br105)[ ](#br105)[failure](#br105)[ ](#br105)[with](#br105)[ ](#br105)[specific](#br105)[ ](#br105)[errors](#br105)[ ](#br105)[..............................................................105](#br105)

[13.1.1](#br105)[ ](#br105)[Indicator............................................................................................................................................105](#br105)

[13.1.1](#br106)[ ](#br106)[Cause](#br106)[ ](#br106)[...............................................................................................................................................](#br106)[ ](#br106)[106](#br106)

[13.1.1](#br106)[ ](#br106)[Actions.............................................................................................................................................](#br106)[ ](#br106)[106](#br106)

[Common](#br106)[ ](#br106)[issue](#br106)[ ](#br106)[#3:](#br106)[ ](#br106)[Submission](#br106)[ ](#br106)[failure](#br106)[ ](#br106)[without](#br106)[ ](#br106)[specific](#br106)[ ](#br106)[errors](#br106)[ ](#br106)[........................................................](#br106)[ ](#br106)[106](#br106)

[14.1.1](#br106)[ ](#br106)[Indicator](#br106)[ ](#br106)[..........................................................................................................................................](#br106)[ ](#br106)[106](#br106)

[14.1.1](#br107)[ ](#br107)[Cause................................................................................................................................................107](#br107)

[14.1.1](#br107)[ ](#br107)[Actions..............................................................................................................................................107](#br107)

[13](#br105)

[14](#br106)

**1 Introduction**

**1.1 INTENDED AUDIENCE AND READING SUGGESTIONS**

This document is intended for developers, project managers, and QA testers. It is recommended

that the document be read in full in order to understand the functionality of each section and

how one relates to another.

Omaha Boarding Specification.docx

Page 4 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**1.2 PROJECT SCOPE**

This document describes the software functional requirements for the Boarding Omaha Inbound

API to submit the MPAs and retrieve the MPA Processing Statuses.

Omaha Boarding Specification.docx

Page 5 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**2 Requirements**

Boarding API Web Service provides two methods for the Client to submit the MPAs to Fiserv

retrieve the status updates after the MPAs have been successfully submitted. Below is the

architecture of the Boarding API Web Service that will be consumed by the Client System.

See attached documents “OmahaAPI\_XMLSchema\_V2.6.xsd” and “OmahaAPI\_V2.6.wsdl” for

technical implementation details.

**2.1.1 Test IP address & url**

Public IP: 63.241.224.44

URL: <https://lsuat-api.fdportfoliomanager.com/boarding/omaha>

**2.1.1 Security**

As per security purpose, TLS 1.0 is disabled and client should use TLS 1.2, The following code is

used for C# program where it should be set before making call to API.

**C#**

ServicePointManager.SecurityProtocol = SecurityProtocolType.Tls |

SecurityProtocolType.Tls11 | SecurityProtocolType.Tls12;

If you are using SoapUI for testing, below changes should be made to make it work.

The client will want to add the following parameter to their Soap UI

**PATH**: ..\Program Files\SmartBear\SoapUI-5.3.0\bin\SoapUI-5.3.0.vmoptions

Edit VMOptions.txt file in their Soap UI > '**-Dsoapui.https.protocols=TLSv1.2**'

Omaha Boarding Specification.docx

Page 6 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**3 Request format**

The vendor sends the merchant information to the boarding API in XML format. This chapter comprises

the following sections of the XML request message, with sample XML text:

·

·

·

SOAP Envelope

SOAP Header

SOAP Body

The merchant information should be sent to the boarding API in precise prescribed XML format. If the

merchant information does not conform to the prescribed format, then the boarding API returns a failure

response after validation of the information. The following points are to be noted:

·

Data elements are enclosed in a block of data and preceded by data element name. The

name of a start tag is enclosed in angular brackets <**Merchant\_No**>. An end tag includes a

slash (/) in front of the tag name </Merchant\_No>. Every start tag should have a matching

end tag, otherwise it will be rejected. A merchant number is represented as

<Merchant\_No>12345670001</Merchant\_No>.

·

There are no fixed set of tags. New tags are created when required. The new tags should

conform to the standard to ensure that that the tag names are not duplicated.

·

·

Tag names are case sensitive. <**Merchant\_No**> is not equivalent to <**merchant\_no**>.

XML data elements are of variable length. They do not require leading zeroes in numeric

fields and trailing spaces in alphanumeric fields to occupy a fixed number of positions.

·

White space is not permitted as part of the tag name. However space characters are allowed

in data content.

**Example of valid XML**

<MERCHANT\_NO>12345670001</MERCHANT\_NO>

Omaha Boarding Specification.docx

Page 7 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Example of invalid XML**

< MERCHANT\_NO >12345670001</ MERCHANT\_NO

·

All files that conform to the syntax of XML contain a set of parameters upfront, known as the

XML declaration, or prolog. This always appears at the beginning of the file. It includes

version information as well as an encoding declaration to describe how the characters in the

document are encoded. This parameter provides the version of XML that is being used and is

not to be confused with the SCP version. It describes the current level of XML, and is

controlled by the W3C.

·

**Example of invalid XML**

<?XML VERSION="1.0"?>

**3.1 SOAP ENVELOPE**

The required SOAP Envelope element is the root element of a SOAP message. This element defines the

XML document as a SOAP message.

**Sample SOAP Envelope Message**

**SOAP Envelope Message**

<con:soapui-project activeEnvironment="**Default**" name="**Boarding API UAT**"

resourceRoot="" soapui-version="**5.0.0**" abortOnError="**false**" runType="**SEQUENTIAL**"

xmlns:con="**http://eviware.com/soapui/config**">

**3.1.1 Request Body**

The request body message contains the details of merchant information in XML format.

**Sample SOAP Request Body Message**

Omaha Boarding Specification.docx

Page 8 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**SOAP Request Body Message**

Beginning at <MpaInfo>, the sample SOAP request body message is illustrated in the attached document.

Boarding-Omaha-API

27309 - FDC Spec -

-UAT 20151209-soap LoneStar SOAP APIs S

**3.1.1 MPA as xml file**

Submitting MPAs via Omaha Boarding API requires the submitted MPA data to be hosted within

an XML file with each XML tag corresponding to one MPA data field. Another way to look at this

is that the XML files are technically the MPAs themselves.

In the following example is a part of an XML MPA where details about equipments of the

corresponding merchant are captured:

<Equipment>

<EquipmentTemplate xsi:nil="true" xmlns:xsi="http://www.w3.org/2001/XMLSchema-

instance"></EquipmentTemplate>

<FrontEndFE>2</FrontEndFE>

<Model>AA1112</Model>

<PinPad xsi:nil="true" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"></PinPad>

<Printer xsi:nil="true" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"></Printer>

<CheckReader xsi:nil="true" xmlns:xsi="http://www.w3.org/2001/XMLSchema-

instance"></CheckReader>

<CloverOption xsi:nil="true" xmlns:xsi="http://www.w3.org/2001/XMLSchema-

instance"></CloverOption>

<EquipmentType>1</EquipmentType>

<SerialNumber>1000</SerialNumber>

<RoamEmvMobileReader xsi:nil="true" xmlns:xsi="http://www.w3.org/2001/XMLSchema-

instance"></RoamEmvMobileReader>

<BillingMethod>6</BillingMethod>

<TrainingIndicator xsi:nil="true" xmlns:xsi="http://www.w3.org/2001/XMLSchema-

instance"></TrainingIndicator>

<Quantity>1</Quantity>

<UnitPrice>9999.00</UnitPrice>

</Equipment>

i *It is advisable that the XML files are well formed for ease of (MPA) data management and*

*testing.*

**3.1.1 Order of XML Tags**

It is strictly mandatory that the order in which the XML tags are laid out match that of the

schema file of Omaha Boarding API.

Should there be any difference between those two; MPA submission via Omaha Boarding API

will not be possible. The action of submitting an incorrectly ordered MPA will always result in

what we would normally call the ‘schema’ error, as can be shown the example below (where

'Address1' is intentionally placed before 'LegalName'):

Omaha Boarding Specification.docx

Page 9 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">10/14/2015 04:34:40 AM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>The element 'CorporateInfo' has invalid child

element 'Address1'. List of possible elements expected:

'LegalName'.</ErrorDescription>

<LineNumber>14</LineNumber>

<ColumnNumber>4</ColumnNumber>

</MerchantError>

</Errors>

</SubmitMPAResult>

**3.1.1 Unspecified MPA Fields**

The total number of MPA data fields is huge, which is roughly 671 fields. But not all MPA fields

are required input fields. You can opt to leave the optional MPA input fields unspecified either

by completely removing the associated XML tags from the MPA XML file or adding a special

name space to them, as represented by the example below:

Option 1: Use namespace xsi:nil="true”

<Prin1FirstName>PABLO</Prin1FirstName>

<Prin1LastName>TEJADA</Prin1LastName>

<Prin1MiddleInitial>M</Prin1MiddleInitial>

<Prin1OwnershipPercent>100</Prin1OwnershipPercent>

<Prin1GuarantorCode>0</Prin1GuarantorCode>

<Prin1Title>1</Prin1Title>

<Prin1Address>1322 MORRIS</Prin1Address>

<Prin1City>BRONX</Prin1City>

<Prin1State>NY</Prin1State>

<Prin1First5Zip>10456</Prin1First5Zip>

<Prin1Last4Zip xsi:nil="true" />

<Prin1Phone>6468949236</Prin1Phone>

Option 2: Completely remove Prin1Last4Zip

<Prin1FirstName>PABLO</Prin1FirstName>

<Prin1LastName>TEJADA</Prin1LastName>

<Prin1MiddleInitial>M</Prin1MiddleInitial>

<Prin1OwnershipPercent>100</Prin1OwnershipPercent>

<Prin1GuarantorCode>0</Prin1GuarantorCode>

<Prin1Title>1</Prin1Title>

<Prin1Address>1322 MORRIS</Prin1Address>

<Prin1City>BRONX</Prin1City>

<Prin1State>NY</Prin1State>

<Prin1First5Zip>10456</Prin1First5Zip>

<Prin1Phone>6468949236</Prin1Phone>

Omaha Boarding Specification.docx

Page 10 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Option 3: Use namespace xsi:nil="true" xmlns:xsi="http://www.w3.org/2001/XMLSchema-

instance"

<Prin1FirstName>PABLO</Prin1FirstName>

<Prin1LastName>TEJADA</Prin1LastName>

<Prin1MiddleInitial>M</Prin1MiddleInitial>

<Prin1OwnershipPercent>100</Prin1OwnershipPercent>

<Prin1GuarantorCode>0</Prin1GuarantorCode>

<Prin1Title>1</Prin1Title>

<Prin1Address>1322 MORRIS</Prin1Address>

<Prin1City>BRONX</Prin1City>

<Prin1State>NY</Prin1State>

<Prin1First5Zip>10456</Prin1First5Zip>

<Prin1Last4Zip xsi:nil="true" xmlns:xsi="http://www.w3.org/2001/XMLSchema-

instance"></Prin1Last4Zip>

<Prin1Phone>6468949236</Prin1Phone>

All three options will produce the same result: Prin1Last4Zip is not specified.

**3.2 USING MASTER MAPPING DOCUMENT**

The master mapping document for Omaha API is very useful in that it contains a lot of

information that can be used to manipulate and control the input XMLs more effectively.

The most basic information you can obtain from the document includes:

·

·

·

·

XML Path: The parent XML tag representing MPA section

XML Field: The XML tag representing the MPA input field within the MPA section

Type: Input type of the MPA input field

Length/Range: Maximum allowed length of the MPA input field/Minimum value – Maximum value

of the MPA input field

·

·

Required: Is the MPA input field mandatory?

Enumeration Values: Selectable values in case the input type of the MPA input field is “Select List”

Omaha Boarding Specification.docx

Page 11 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Note: You must make sure the Omaha API master mapping is up-to-date with the Omaha

Boarding API tool.

**4 ws-security authentication**

This section specifies the detailed requirements for applying WS-Security Authentication using

Username Tokens with a Username and Password Digest. The OASIS standard is being utilized

with [the](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[profile](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[of](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Web](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Services](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Security](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Username](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Token](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Profile](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[Version](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[ ](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[1.1.1](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)[.](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html)

The following request sample illustrates how the security information will be sent within SOAP

Header. Note that the SOAP body will vary depending on the specifics of the data communicated

by Lonestar pillars.

Request Message Sample

<?xml version="1.0" encoding="utf-8"?>

<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing"

xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-

1.0.xsd" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-

utility-1.0.xsd">

<soap:Header>

<wsa:Action>http://tempuri.org/HelloWorld</wsa:Action>

<wsa:MessageID>urn:uuid:ebc4c587-52b8-4867-a47b-

c0ddc750fc10</wsa:MessageID>

<wsa:ReplyTo>

<wsa:Address>http://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous<

/wsa:Address>

</wsa:ReplyTo>

<wsa:To>http://localhost:60286/TestWS/Service.asmx</wsa:To>

<wsse:Security soap:mustUnderstand="1">

<wsu:Timestamp wsu:Id="Timestamp-55bec23e-030a-461b-9474-

bc182879bb63">

<wsu:Created>2014-11-27T04:49:32Z</wsu:Created>

<wsu:Expires>2014-11-27T04:54:32Z</wsu:Expires>

</wsu:Timestamp>

<wsse:UsernameToken xmlns:wsu="http://docs.oasis-

open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" wsu:Id="SecurityToken-

95440d2c-3046-4aab-9ed3-d836966fb611">

<wsse:Username>api\_user</wsse:Username>

Omaha Boarding Specification.docx

Page 12 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<wsse:Password Type="http://docs.oasis-

open.org/wss/2004/01/oasis-200401-wss-username-token-profile-

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

The following namespaces are used: **http://docs.oasis-open.org/wss/2004/01/oasis-200401-**

**wss-wssecurity-utility-1.0.xsd** and **http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-**

**wssecurity-secext-1.0.xsd** which are represented below by the prefixes “**wsu**” and “**wsse**”

respectively.

The entry-point to WS-Security is a SOAP Header element called <wsse:Security>. It contains the

security-related data and information. Within <wsse:Security>, the following elements are

required (Note that the order of the elements below is fixed for security purposes):

<wsu:Timestamp>: It is used to express the creation and expiration time of the message. To

address replay attacks, the message timestamps are required:

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

Omaha Boarding Specification.docx

Page 13 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Note that depending on the specifics of the API, there would be a single username/password-

token to consume the service or multiple usernames/password-tokens based on the Portfolio

Manager User Setup.

\-

\-

<wsse:Nonce>: a cryptographically random value. Each message must include a new nonce value

to detect replay attacks.

o

“Nonce”: is the clear text value that generated by sender. However, when it’s sent in

header of SOAP request, it must be encoded to a base64 string

<wsu:Created>: the creation time of the message.

**Sample code using Nonce and Create to compute the PasswordDigest:**

var nonce = "MTQ1Mjc4MzQzOTE0Mw=="; //nlapiEncrypt(date.getTime().toString(), 'base64');

// ex: "1453220513715" --> "MTQ1MzIyMDUxMzcxNQ=="

var nonceText = atob(nonce);

var created = "2016-01-14T10:15:19.143Z";//date.toISOString(); // ex: "2016-

01-19T16:21:53.715Z"

var pwToken = 'S7O0g2w7Q9';

var innerPass = nonceText + created + pwToken; // ex:

"MTQ1MzIyMDUxMzcxNQ==2016-01-19T16:21:53.715ZS7O0g2w7Q9"

var passwordDigest = CryptoJS.SHA1(innerPass).toString(CryptoJS.enc.Base64);

var **passwordDigestCorrect** = CryptoJS.SHA1(**nonceText** + created +

pwToken).toString(CryptoJS.enc.Base64);

Note: When computing the PasswordDigest, you need to use the clear text (non-encoded in

Base64)

**4.1.1 Soap ui project**

Follow the below instructions to import the sample project which will enable you to be able to

test your connection:

·

Import the sample project

o

PLACEHOLDER FOR SOAP UI TEMPLATE

·

·

·

Save the SOAP Project to your local computer

Open SoapUI 5.2.0

File>Import Project (Ctrl-l) to import the SOAP Project

Omaha Boarding Specification.docx

Page 14 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





·

You will see the project on the navigation panel on the left once the import is finished. Click the +

sign to display the web methods. There should be 3 as in the following image.

·

·

Expand SubmitMPA and double-click on Request1 to open its interface. Before sending a SOAP

request, make sure to apply the web service security configurations by right-clicking > Apply

outgoing WSS as in the following image

Make sure the URL points to [https://lsuat-](https://urldefense.proofpoint.com/v2/url?u=https-3A__lsuat-2Dapi.fdportfoliomanager.com_boarding_omaha_AsBoardingAPIService.svc&d=BQMFAw&c=ewHkv9vLloTwhsKn5d4bTdoqsmBfyfooQX5O7EQLv5TtBZ1CwcvjU063xndfqI8U&r=qOFmeH8jp_d2xkmDNk5tp2P1JYFaGjN1XetZ9DOsV9U&m=Kaq4OGl_ACgHo5zDqlMuQyaaWCb7LI5_04tXjkt0vZ4&s=ghWtxN462cQOmRLC11Xak8Su2hvUR30HYfLSq-SHYnI&e=)

[api.fdportfoliomanager.com/boarding/omaha/AsBoardingAPIService.svc](https://urldefense.proofpoint.com/v2/url?u=https-3A__lsuat-2Dapi.fdportfoliomanager.com_boarding_omaha_AsBoardingAPIService.svc&d=BQMFAw&c=ewHkv9vLloTwhsKn5d4bTdoqsmBfyfooQX5O7EQLv5TtBZ1CwcvjU063xndfqI8U&r=qOFmeH8jp_d2xkmDNk5tp2P1JYFaGjN1XetZ9DOsV9U&m=Kaq4OGl_ACgHo5zDqlMuQyaaWCb7LI5_04tXjkt0vZ4&s=ghWtxN462cQOmRLC11Xak8Su2hvUR30HYfLSq-SHYnI&e=)[ ](https://urldefense.proofpoint.com/v2/url?u=https-3A__lsuat-2Dapi.fdportfoliomanager.com_boarding_omaha_AsBoardingAPIService.svc&d=BQMFAw&c=ewHkv9vLloTwhsKn5d4bTdoqsmBfyfooQX5O7EQLv5TtBZ1CwcvjU063xndfqI8U&r=qOFmeH8jp_d2xkmDNk5tp2P1JYFaGjN1XetZ9DOsV9U&m=Kaq4OGl_ACgHo5zDqlMuQyaaWCb7LI5_04tXjkt0vZ4&s=ghWtxN462cQOmRLC11Xak8Su2hvUR30HYfLSq-SHYnI&e=)for Omaha WS in UAT

Omaha Boarding Specification.docx

Page 15 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





·

Click on the green arrow to send the request

·

·

Expand to display the web method RetrieveMPAXML. Repeat 5 and 6 to verify RetrieveMPAXML.

Note that MPA ID must be supplied, referenced from the result of step 6 above to make the

retrieval request valid.

Make sure the URL points to [https://lsuat-](https://urldefense.proofpoint.com/v2/url?u=https-3A__lsuat-2Dapi.fdportfoliomanager.com_boarding_omaha_AsBoardingAPIService.svc&d=BQMFAw&c=ewHkv9vLloTwhsKn5d4bTdoqsmBfyfooQX5O7EQLv5TtBZ1CwcvjU063xndfqI8U&r=qOFmeH8jp_d2xkmDNk5tp2P1JYFaGjN1XetZ9DOsV9U&m=Kaq4OGl_ACgHo5zDqlMuQyaaWCb7LI5_04tXjkt0vZ4&s=ghWtxN462cQOmRLC11Xak8Su2hvUR30HYfLSq-SHYnI&e=)

[api.fdportfoliomanager.com/boarding/omaha/AsBoardingAPIService.svc](https://urldefense.proofpoint.com/v2/url?u=https-3A__lsuat-2Dapi.fdportfoliomanager.com_boarding_omaha_AsBoardingAPIService.svc&d=BQMFAw&c=ewHkv9vLloTwhsKn5d4bTdoqsmBfyfooQX5O7EQLv5TtBZ1CwcvjU063xndfqI8U&r=qOFmeH8jp_d2xkmDNk5tp2P1JYFaGjN1XetZ9DOsV9U&m=Kaq4OGl_ACgHo5zDqlMuQyaaWCb7LI5_04tXjkt0vZ4&s=ghWtxN462cQOmRLC11Xak8Su2hvUR30HYfLSq-SHYnI&e=)[ ](https://urldefense.proofpoint.com/v2/url?u=https-3A__lsuat-2Dapi.fdportfoliomanager.com_boarding_omaha_AsBoardingAPIService.svc&d=BQMFAw&c=ewHkv9vLloTwhsKn5d4bTdoqsmBfyfooQX5O7EQLv5TtBZ1CwcvjU063xndfqI8U&r=qOFmeH8jp_d2xkmDNk5tp2P1JYFaGjN1XetZ9DOsV9U&m=Kaq4OGl_ACgHo5zDqlMuQyaaWCb7LI5_04tXjkt0vZ4&s=ghWtxN462cQOmRLC11Xak8Su2hvUR30HYfLSq-SHYnI&e=)for Omaha WS in UAT

·

Click on the green arrow to send the request

**Note:**

·

Rather than using this sample project, users can create an entirely new project from scratch by

entering the correct URL and configuring a WSS based on provided user account(s).

WSS must be re-applied every time before a request is sent to Omaha API WS.

·

Omaha Boarding Specification.docx

Page 16 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Note: It is recommended that if you are using a different interface than Soap UI to send the web

service calls that you work within Soap UI first to ensure that your submissions are making it to

FD successfully. Once you have this piece working, you can then port the information over to

the interface that you will be using.

**5 Boarding API Methods**

The Web Service Name is ASBoardingAPIService.

**5.1.1 Submit MPA Method**

This method allows the Client System to send MPA data to Boarding API. The following diagram

illustrates the business flow inside the method.

Omaha Boarding Specification.docx

Page 17 of 107

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

XMLContent String

simpleType

This xml has the merchant data from the Client

System. Details are in [MPA](#br46)[ ](#br46)[XML](#br46)[ ](#br46)[FORMAT](#br46)[ ](#br46)section.

Unique sequence generated by the Client System.

ExtRefID

String

simpleType

Note: The user credentials will be passed along with the request on the SOAP Header and are

identified in separate security document.

**Transmissions & Response**

When the Boarding API successfully receives and validates the XML content, it will respond with

a synchronous SUCCESS status. If the XML content is received and fails validation, the Boarding

API will respond with a FAILURE status and the detailed errors which explain the failure. The

response can report multiple errors as below.

If any failure in transmission occurs, e.g. the service is unavailable, undergoing maintenance, or

network connectivity problems occur, it is the Boarding API consumer’s responsibility to re-

transmit the message at a later time. It is recommended that a back off algorithm be used when

re-transmitting.

Success Message Response Sample XML

<SubmitMPAResponse>

Omaha Boarding Specification.docx

Page 18 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





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

<ErrorId>1</ErrorId>

<ErrorDescription></ErrorDescription>

<LineNumber/>

<ColumnNumber/>

</MerchantError>

</Errors>

</SubmitMPAResult>

</SubmitMPAResponse>

**Tag Name**

**ExternalRefId**

**Tag Description**

It will hold the external Ref Id received from

Client

**ASRefId**

It will hold the MPA ID generated from Fiserv

Boarding system in case of success. It will be

blank in case of failure

**Timestamp**

**Status**

The date time stamp of success or failure of

the submission.

If the MPA XML Content passes the

validation, it will be **SUCCESS**. Otherwise, it

will be **FAILURE**

**Errors**

It will hold the MerchantError tags – Only

applicable if the MPA XML Content fails

against the validation.

Omaha Boarding Specification.docx

Page 19 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**MerchantError**

It will contain multiple errors received while

XSD validation as well as error that relates to

MPA edits of boarding merchant.

**ErrorId** Holds the Error #.

**ErrorDescription** Holds the description of merchant error.

**LineNumber** Holds the Error Line #. It could be sent as

empty tag.

**ColumnNumber** Holds the Error Column #. It could be sent as

empty tag.

**5.2 GET STATUS BY TIMESPAN METHOD**

After the MPAs have been successfully submitted, this method allows the Client System to

retrieve the MPA status updates. It is recommended to invoke this service on a periodic basis as

a batch inquiry. The returned MPA status updates will correspond to the timestamps passed to

the method. The following diagram illustrates the business flow inside the method.

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

DateTime (MM/DD/YYYY

HH:MM:SS AM/PM)

simpleType

Value must be

within the last 168

Omaha Boarding Specification.docx

Page 20 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





hours from the

current time

ToTimeStamp

DateTime

(Format MM/DD/YYYY

HH:MM:SS AM/PM)

simpleType

Value must be

greater than

FromTimeStamp

Note: The user credentials will be passed along with the request on the SOAP Header and are

identified in separate security documentation.

**Transmissions & Response**

When the Boarding API successfully receives a valid request, based on the timestamp, it will

respond synchronously with a list of MPA status details. The result can contain multiple MPAs

with multiple status updates within specified time span. If there are no status updates within

specified time span, the result will be sent as blank tag.

If any failure in transmission occurs, e.g. the service is unavailable, undergoing maintenance, or

network connectivity problems occur, it is the Boarding API consumer’s responsibility to re-

transmit the message at a later time. It is recommended that a back off algorithm be used when

re-transmitting.

**No Record Found Response Sample XML**

<GetStatusByTimeSpanResponse xmlns="http://tempuri.org/">

<GetStatusByTimeSpanResult>

<MerchantApplicationStatus>

<ASRefId />

<FDMerchantNumber />

<Status>

<MerchantDetails>

<OmahaNumber />

<LocationNumber />

<DBAName />

<CardnetNumber />

<MerchantStatus>

<AppStatus>

<Code />

<Information>No record found against the specified timespan.</Information>

<Timestamp>12/12/2014 03:21:51 PM</Timestamp>

</AppStatus>

</MerchantStatus>

</MerchantDetails>

</Status>

<Errors />

<CreditOfficerComments />

</MerchantApplicationStatus>

Omaha Boarding Specification.docx

Page 21 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





</GetStatusByTimeSpanResult>

</GetStatusByTimeSpanResponse>

**MPA Status Details Response Sample XML**

<GetStatusByTimeSpanResponse xmlns="http://tempuri.org/">

<GetStatusByTimeSpanResult>

<MerchantApplicationStatus>

<ASRefId>1234</FDRefId>

<FDMerchantNumber>987838651881</FDMerchantNumber>

<Status>

<MerchantDetails>

<OmahaNumber />

<LocationNumber>1</LocationNumber>

<DBAName>SUPER BOWL TICKET</DBAName>

<CardnetNumber />

<MerchantStatus>

<AppStatus>

<Code>MpaKey</Code>

<Information>In Process</Information>

<Timestamp>10/14/2014 5:13:12 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MPA</Code>

<Information>In Process</Information>

<Timestamp>10/14/2014 5:13:13 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MpaKey</Code>

<Information>Submitted</Information>

<Timestamp>10/14/2014 5:14:09 PM</Timestamp>

</AppStatus>

</MerchantStatus>

</MerchantDetails>

</Status>

<Errors>

<AppError>

<ErrorId />

<ErrorDescription />

</AppError>

</Errors>

<CreditOfficerComments>

Omaha Boarding Specification.docx

Page 22 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<Comment>

<CreditOfficerId>SORR</CreditOfficerId>

<Message>Comment 1</Message>

<MessageDate>10/14/2014 5:40:57 PM</MessageDate>

</Comment>

<Comment>

<CreditOfficerId>SORR</CreditOfficerId>

<Message>Comment 2</Message>

<MessageDate>10/14/2014 5:40:57 PM</MessageDate>

</Comment>

</CreditOfficerComments>

</MerchantApplicationStatus>

<MerchantApplicationStatus>

<ASRefId>1235</FDRefId>

<FDMerchantNumber>987839375886</FDMerchantNumber>

<Status>

<MerchantDetails>

<OmahaNumber />

<LocationNumber>1</LocationNumber>

<DBAName>RBS COLLECTIONS INC</DBAName>

<CardnetNumber />

<MerchantStatus>

<AppStatus>

<Code>MpaKey</Code>

<Information>Submitted</Information>

<Timestamp>10/14/2014 5:15:19 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>ClientApproval</Code>

<Information>In Process</Information>

<Timestamp>10/14/2014 5:15:19 PM</Timestamp>

</AppStatus>

</MerchantStatus>

</MerchantDetails>

</Status>

<Errors>

<AppError>

<ErrorId />

<ErrorDescription />

</AppError>

Omaha Boarding Specification.docx

Page 23 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





</Errors>

<CreditOfficerComments>

<Comment>

<CreditOfficerId />

<Message />

<MessageDate />

</Comment>

</CreditOfficerComments>

</MerchantApplicationStatus>

</GetStatusByTimeSpanResult>

</GetStatusByTimeSpanResponse>

**Tag Name**

**ASRefID**

**Tag Description**

Cross Reference key returned during the

account setup, the MPA ID generated from

Fiserv Boarding system.

**FDMerchantNumber**

**Status**

Merchant number received from Fiserv.

Is the node which will consist of

**MerchantDetails**, which basically will hold the

detail of accounts for various locations. This

node will hold below fields:

**OmahaNumber**

Omaha Mid assigned by VAPP. (Only be

available after the account approved)

Outlet Number

The Do Business As name of the merchant.

This will contain various AppStatus (status)

consist of below:

**LocationNumber**

**DBAName**

**MerchantStatus**

**AppStatus**

**Code** Unique code defined for each status

attribute. Please refer to the status attributes

table in MPA STATUS REPORTING section.

**Information** This is used to report status values or

additional information for the status

attribute. This field’s value is populated

based on the value populated in the status

code. Please refer to the status attributes

table in MPA STATUS REPORTING section.

**TimeStamp** Timestamp of the status code.

Includes 2 elements, it will only be populated

in case Validation failure.

**Errors**

Omaha Boarding Specification.docx

Page 24 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**ErrorID** Error code will appear defined for Validation

Failure.

**ErrorDescription** Error description

**CreditOfficerComments** It will have the comments detail.

**Comment** This will have following fields:

**CreditOfficerId** Credit officer ID.

**Message** Credit message for the account.

**MessageDate** Date time for the message.

**5.2.1 Enable the ability to pull Cardnet TID and Cardnet Number**

**Pulled Values**

Key Cardnet values which should be pulled back as part of the change request include:

·

·

Cardnet Number

Cardnet TID

**Event**

**Code**

**EventType**

CardnetNumbe Cardnet

r

**Value**

**Example**

84950254988

4

**Example for Event Message**

Number

N/A

849502549884

537 -

EquipFECardne

t

CARDNETFE~Euip\_ID=11:TID=93214

4;

Cardnet TID

004GCF

537

EventType and Event Code can be used to identify which event to look into for the required

information, and to differentiate between an event that does not provide needed values and one

that does; as well as to avoid pulling duplicate records.

**XML changes**

The XML response returned by the web method GetStatusByTimeSpan must be updated to

incorporate Carnet Number and Cardnet TID.

·

CardnetNumber is specific to a merchant location and can only be pulled when available from VAPP. If

unavailable, the XML tag is still present but without any value in it. Cardnet Number is located under

DBA Name. Below is an example for a XML response with Cardnet Number available:

\1.

\2.

\3.

\4.

\5.

\6.

\7.

<MerchantApplicationStatus>

<FDRefId>987031715182470554846</FDRefId>

<FDMerchantNumber>987870276886</FDMerchantNumber>

<Status>

<MerchantDetails>

<OmahaNumber>517927120108121</OmahaNumber>

<LocationNumber>1</LocationNumber>

Omaha Boarding Specification.docx

Page 25 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\8.

\9.

\10.

\11.

\12.

\13.

\14.

<DBAName>SAMPLE</DBAName>

<CardnetNumber>849501488886</CardnetNumber>

<MerchantStatus>

</MerchantStatus>

</MerchantDetails>

</Status>

</MerchantApplicationStatus>

·

Cardnet TID is specific to equipments within a location. GetStatusByTimeSpan must be able to reflect

that in its XML response by assigning a sequential number to each equipment. Cardnet TID can only

be pulled when available from VAPP. If unavailable, the whole AppStatus will not be returned. Below

is the example of an XML response with Cardnet TID available:

\1.

\2.

\3.

\4.

<MerchantApplicationStatus>

<FDRefId>987031715182470554846</FDRefId>

<FDMerchantNumber>987870276886</FDMerchantNumber>

<Status>

\5.

\6.

\7.

\8.

<MerchantDetails>

<OmahaNumber>517927120108121</OmahaNumber>

<LocationNumber>1</LocationNumber>

<DBAName>SAMPLE</DBAName>

<CardnetNumber>849501488886</CardnetNumber>

<MerchantStatus>

\9.

\10.

\11.

\12.

\13.

\14.

\15.

\16.

\17.

\18.

\19.

\20.

\21.

\22.

\23.

\24.

\25.

\26.

\27.

\28.

\29.

<AppStatus>

<Code>VAPPBoarding</Code>

<Information>Boarded</Information>

<Timestamp>3/18/2015 12:25:31 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MPA</Code>

<Information>Boarded</Information>

<Timestamp>3/18/2015 12:26:02 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>EquipFECardnet</Code>

<Information>CARDNETFE~Euip\_ID=11:TID=932144;</Information>

<Timestamp>3/18/2015 12:28:36 PM</Timestamp>

</AppStatus>

</MerchantStatus>

</MerchantDetails>

</Status>

</MerchantApplicationStatus>

**Screenshot of pulled-back values on Front-End**

Omaha Boarding Specification.docx

Page 26 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**5.2.1 Enable the ability to pull Nashville MID and Nashville TID**

**Pulled Values**

Nashville values that are generated during Nashville equipment setup process include:

·

·

Nashville MID

Nashville TID

**Exampl Event**

**EventType**

**Value**

**e**

**Code**

**Example for Event Message**

160 -

EquipNashvill Nashville

e MID

475099

0

NASHVILLE~Euip\_ID=11:MID=4750990#TID=79723

95;

160

160 -

EquipNashvill Nashville

e TID

797239

5

NASHVILLE~Euip\_ID=11:MID=4750990#TID=79723

95;

160

EventType and Event Code can be used to differentiate between an event that does not provide

needed values and one that does, as well as to avoid pulling duplicate records.

**XML changes**

Omaha Boarding Specification.docx

Page 27 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





The XML response returned by the web method GetStatusByTimeSpan must be updated to

incorporate Nashville MID and Nashville TID.

·

Nashville MID and Nashville TID come in pairs and vary in accordance with the specific Nashville

equipment they are associated to within a location. A sequential number must be assigned to each

equipment to reflect that.

·

Nashville MID and Nashville TID can only be pulled when available from VAPP. If unavailable, the

whole AppStatus will not be returned. Below is the example of an XML response with Nashville

generated values available:

\1.

\2.

\3.

\4.

<MerchantApplicationStatus>

<FDRefId>987011415160070554856</FDRefId>

<FDMerchantNumber>987856833882</FDMerchantNumber>

<Status>

\5.

\6.

\7.

\8.

<MerchantDetails>

<OmahaNumber>518993730128303</OmahaNumber>

<LocationNumber>1</LocationNumber>

<DBAName>SAMPLE</DBAName>

<CardnetNumber />

\9.

\10.

\11.

\12.

\13.

\14.

\15.

\16.

\17.

\18.

\19.

\20.

\21.

\22.

\23.

\24.

\25.

\26.

\27.

\28.

\29.

<MerchantStatus>

<AppStatus>

<Code>VAPPBoarding</Code>

<Information>Boarded</Information>

<Timestamp>1/14/2015 4:01:57 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MPA</Code>

<Information>Boarded</Information>

<Timestamp>1/14/2015 4:08:50 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>EquipNashville</Code>

<Information>NASHVILLE~Euip\_ID=11:MID=511#TID=CL01;</Information>

<Timestamp>1/14/2015 4:14:50 PM</Timestamp>

</AppStatus>

</MerchantStatus>

</MerchantDetails>

</Status>

</MerchantApplicationStatus>

·

In the event there are multiple Nashville equipments, the returned XML should be formatted as

follows in terms of how to present generated Nashville data:

\1. <AppStatus>

Omaha Boarding Specification.docx

Page 28 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\2. <Code>EquipNashville</Code>

\3. <Information>NASHVILLE~Euip\_ID=11:MID=40#TID=;Euip\_ID=12:MID=7#TID=6;</Information>

\4. <Timestamp>10/27/2014 8:00:57 PM</Timestamp>

\5. </AppStatus>

**Screenshot of pulled-back values on Front-End**

**5.2.1 Enable the ability to pull Omaha BE MID and Omaha Download ID**

**Pulled Values**

Key Cardnet values which should be pulled back via GetStatusByTimeSpan are:

·

·

·

Omaha BE MID

Omaha Download ID

Application Name

**EventType**

**Value**

**Example**

**Event Code**

**Example for Event Message**

Omaha BE

MID

53638579019548

1

OmahaMID

N/A

536385790195481

Omaha Boarding Specification.docx

Page 29 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





201 -

OMAHAFE~Euip\_ID=11:DOWNLOADI

D

EquipFEOmah Omaha

a

Download ID 733707145

201

201

=733711261:APPLICATION=XEFB410;

OMAHAFE~Euip\_ID=11:DOWNLOADI

D

EquipFEOmah Application

a

Name

XEFB410

=733711261:APPLICATION=XEFB410;

EventType and Event Code can be used to differentiate between an event that does not provide

needed values and one that does; and also to avoid pulling duplicate records.

**XML changes**

The XML response returned by the web method GetStatusByTimeSpan must be updated to

incorporate important values for OmahaMID and EquipFEOmaha.

·

Each location within a merchant has its own unique Omaha BE MID. If unavailable, the XML tag

OmahaNumber is still present but without any value in it. Omaha BE MID is placed above Location

Number. Below is an example for a XML response with Omaha BE MID available:

\1. <GetStatusByTimeSpanResult>

\2.

\3.

\4.

\5.

\6.

\7.

\8.

\9.

\10.

<MerchantApplicationStatus>

<FDRefId>987011415160070554856</FDRefId>

<FDMerchantNumber>987856833882</FDMerchantNumber>

<Status>

<MerchantDetails>

<OmahaNumber>518993730128303</OmahaNumber>

<LocationNumber>1</LocationNumber>

<DBAName>LUCHAZIE GENERAL STORE</DBAName>

<CardnetNumber />

·

Each added equipment has its own Omaha Download ID. The XML response must be able to reflect

that information through the use of equipment sequential number. If not available the whole

AppStatus block would not be present in the XML response. In the following example, the Omaha

Download ID belongs to the second equipment of the first merchant location:

\1. <AppStatus>

\2. <Code>EquipFEOmaha</Code>

\3. <Information>OMAHAFE~Euip\_ID=12:DOWNLOADID=990102014:APPLICATION=XEFB410;</Infor

mation>

\4. <Timestamp>10/21/2014 2:19:28 PM</Timestamp>

\5. </AppStatus>

**Screenshot of pulled-back values on Front-End**

Omaha Boarding Specification.docx

Page 30 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Sample of response with double-locations:**

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

xmlns:xsd="http://www.w3.org/2001/XMLSchema">

<GetStatusByTimeSpanResponse xmlns="http://tempuri.org/">

<GetStatusByTimeSpanResult>

<GetStatusByTimeSpanResult>

<MerchantApplicationStatus>

<ASRefId>2999</ASRefId>

<FDMerchantNumber/>

<Status>

<MerchantDetails>

<OmahaNumber/>

<LocationNumber>1</LocationNumber>

<DBAName>API TEST APP AMEX #1 INC.</DBAName>

<MerchantStatus>

<AppStatus>

<Code>LocationBoarding</Code>

<Information>In Process</Information>

<Timestamp>11/30/2015 10:48:56 AM</Timestamp>

Omaha Boarding Specification.docx

Page 31 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





</AppStatus>

<AppStatus>

<Code>LocationEquipment</Code>

<Information>In Process</Information>

<Timestamp>11/30/2015 10:48:56 AM</Timestamp>

</AppStatus>

<AppStatus>

<Code>LocationNashville</Code>

<Information>In Process</Information>

<Timestamp>11/30/2015 10:48:56 AM</Timestamp>

</AppStatus>

<AppStatus>

<Code>BackEnd</Code>

<Information>In Process</Information>

<Timestamp>11/30/2015 10:48:56 AM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MPAKey</Code>

<Information>In Process</Information>

<Timestamp>11/30/2015 10:45:50 AM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MPA</Code>

<Information>In Process</Information>

<Timestamp>11/30/2015 10:45:50 AM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MpaKey</Code>

<Information>Submitted</Information>

<Timestamp>11/30/2015 10:46:04 AM</Timestamp>

</AppStatus>

<AppStatus>

<Code>ClientApproval</Code>

<Information>Direct Send</Information>

<Timestamp>11/30/2015 10:46:04 AM</Timestamp>

</AppStatus>

<AppStatus>

<Code>Transmission</Code>

<Information>In Process</Information>

<Timestamp>11/30/2015 10:48:07 AM</Timestamp>

Omaha Boarding Specification.docx

Page 32 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





</AppStatus>

<AppStatus>

<Code>Transmission</Code>

<Information>Success</Information>

<Timestamp>11/30/2015 10:48:56 AM</Timestamp>

</AppStatus>

<AppStatus>

<Code>Underwriting</Code>

<Information>In Process</Information>

<Timestamp>11/30/2015 10:48:56 AM</Timestamp>

</AppStatus>

</MerchantStatus>

<CardnetNumber/>

</MerchantDetails>

<MerchantDetails>

<OmahaNumber/>

<LocationNumber>2</LocationNumber>

<DBAName>API TEST APP AMEX #1 INC.</DBAName>

<MerchantStatus>

<AppStatus>

<Code>LocationBoarding</Code>

<Information>In Process</Information>

<Timestamp>11/30/2015 10:48:56 AM</Timestamp>

</AppStatus>

<AppStatus>

<Code>LocationEquipment</Code>

<Information>In Process</Information>

<Timestamp>11/30/2015 10:48:56 AM</Timestamp>

</AppStatus>

<AppStatus>

<Code>LocationNashville</Code>

<Information>In Process</Information>

<Timestamp>11/30/2015 10:48:56 AM</Timestamp>

</AppStatus>

<AppStatus>

<Code>BackEnd</Code>

<Information>In Process</Information>

<Timestamp>11/30/2015 10:48:56 AM</Timestamp>

</AppStatus>

</MerchantStatus>

Omaha Boarding Specification.docx

Page 33 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<CardnetNumber/>

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

**5.2.1 Enable the ability to pull Datawire DID**

**Pulled Values**

Datawire DID

**EventType**

**Value**

**Example**

**Event Code Example for Event Message**

566 -

EquipDatawir

e

53638579019548

1

Datawire~Euip\_ID=31:DID=

00041468421234602166;

Datawire DID

566

The correct message that contains the required value of Datawire DID can be identified via Event

Type and Event Code. However there are cases where the Event Message does not provide the

value, as in the example below:

566 - Datawire~Euip\_ID=11:DID=Not Applicable;Euip\_ID=12:DID=Not Applicable;

**XML Changes**

XML response returned by GetStatusByTimeSpan must be updated to accommodate the

requirement to include Datawire DID.

·

Datawire DID also varies by each equipment within a location. When Datawire DID is not available for

whatever reason (not applicable or not available yet), the whole block of AppStatus with EventType =

EquipDatawire should be excluded from the XML response

\1. <AppStatus>

\2. <Code>EquipDatawire</Code>

\3. <Information>Datawire~Euip\_ID=31:DID=00041468421234602166;</Information>

\4. <Timestamp>11/24/2015 11:57:49 AM</Timestamp>

\5. </AppStatus>

**Screenshot of pulled-back values on Front-End**

Omaha Boarding Specification.docx

Page 34 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**5.2.1 Enable the ability to back Clover ID**

**Pulled Values**

Clover ID is generated as a result of Clover equipment setup for merchant and is provided for

Fiserv by VAPP.

**Event**

**Code**

**EventType Value**

Clover

**Example**

**Example for Event Message**

568 -

EquipClover ID

V6PEZCJX9BC7T 568

Clover~Euip\_ID=11:CLOVERID=E7MJG5RBSCSD2;

The event to refer to for Clover ID can be identified with Event Type EquipClover and Event Code

\568.

**XML Changes**

·

XML response returned by GetStatusByTimeSpan must be updated to accommodate the requirement

to include Clover ID. When unavailable the whole AppStatus block must be excluded from

GetStatusByTimeSpan response.

\1. <AppStatus>

\2. <Code>EquipClover</Code>

Omaha Boarding Specification.docx

Page 35 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\3. <Information>Clover~Euip\_ID=11:CLOVERID=SZXKYQJFTKVJ0;</Information>

\4. <Timestamp>3/18/2015 3:53:38 PM</Timestamp>

\5. </AppStatus>

**Screenshot of pulled-back values on Front-End**

**5.2.1 Enable the ability to pull Rapid Connect ID**

**Pulled Values**

Clover ID is generated as a result of Clover equipment setup for merchant and is provided for

Fiserv by VAPP.

**Exampl Event**

**EventType**

**Value**

**e**

**Code**

**Example for Event Message**

601 -

EquipRapidConne Rapid

ct Connect ID

Rapidconnect~Euip\_ID=11:RAPIDID=400

01;

40001

601

The event to refer to for Rapid Connect ID can be identified with Event Type EquipRapidConnect

and Event Code 601.

**XML Changes**

·

XML response returned by GetStatusByTimeSpan must be updated to accommodate the requirement

to include Rapid Connect ID. When unavailable the whole AppStatus block must be excluded from

GetStatusByTimeSpan response.

Omaha Boarding Specification.docx

Page 36 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\1. <AppStatus>

\1. <Code>EquipRapidConnect</Code>

\2. <Information>601 - Rapidconnect~Euip\_ID=11:RAPIDID=40001;</Information>

\3. <Timestamp>3/18/2015 3:53:38 PM</Timestamp>

\4. </AppStatus>

**Screenshot of pulled-back values on Front-End**

**5.2.1 Enable the ability to pull Buypass MID and Buypass TID**

**Pulled Values**

·

·

Buypass MID

Buypass TID

**Event**

**Code**

**EventType**

**Value**

**Example**

**Example for Event Message**

EquipFEBuypas

s

EquipFEBuypas

s

KL2709928100

1

536 - BUYPASSFE~Euip\_ID=11:MID=

KL27099281001#TID=099281001;

536 - BUYPASSFE~Euip\_ID=11:MID=

KL27099281001#TID=099281001;

Buypass MID

Buypass TID

536

536

099281001

**XML changes**

Omaha Boarding Specification.docx

Page 37 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





·

·

Buypass MID varies per Omaha equipment. Like Buypass MID, Buypass TID also varies per Omaha

equipment.

If no information on the two values is available, the whole App Status block is not returned.

\1.

\2.

\3.

\4.

<MerchantApplicationStatus>

<FDRefId>987011415160070554856</FDRefId>

<FDMerchantNumber>987856833882</FDMerchantNumber>

<Status>

\5.

\6.

\7.

\8.

<MerchantDetails>

<OmahaNumber>518993730128303</OmahaNumber>

<LocationNumber>1</LocationNumber>

<DBAName>SAMPLE</DBAName>

<CardnetNumber />

\9.

\10.

\11.

\12.

\13.

\14.

\15.

\16.

\17.

\18.

\19.

\20.

\21.

\22.

\23.

\24.

\25.

\26.

\27.

\28.

\29.

<MerchantStatus>

<AppStatus>

<Code>VAPPBoarding</Code>

<Information>Boarded</Information>

<Timestamp>1/14/2015 4:01:57 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MPA</Code>

<Information>Boarded</Information>

<Timestamp>1/14/2015 4:08:50 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>EquipFEBuypass</Code>

<Information>536 - BUYPASSFE~Euip\_ID=11:MID#TID=09;</Information>

<Timestamp>1/14/2015 4:14:50 PM</Timestamp>

</AppStatus>

</MerchantStatus>

</MerchantDetails>

</Status>

</MerchantApplicationStatus>

**Screenshot**

Omaha Boarding Specification.docx

Page 38 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**5.2.1 retrieve full mpa method**

This web method allows Boarding API users to retrieve information of successfully submitted

MPAs. The information originates from the Boarding application database and is returned in the

same XML format used for MPA submission.

Omaha Boarding Specification.docx

Page 39 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





API ready to

receive the call?

API receives the call with

specified MPAID

RetrieveMpaXml

YES

MPAID is valid (MPA exists

and was submitted by the

retriever)

YES

NO

API sends Invalid MPAID

message

API send full MPA

data

NO

**5.3 RETRIEVE MPA – TESTING SUPPORT**

**Web Method Name:** RetrieveMpaXml

**Purpose:** Enables the ability for a MPA submissions values retrieved/pulled back in order to

perform field mapping. Note: UAT region is not available to be accessed by clients at this time.

This provides the ability to test the field mappings to ensure that the value mapped to the

correct field as expected.

**Input Parameters:**

Data

Type

Type

Category

Name

Description

Unique sequence generated for each

MPA submitted by AccessOne

Unique sequence generated by the

Client System.

mpaId

extRefID

String

String

simpleType

simpleType

**5.2.2.3 Request & Response**

Boarding API web service returns MPA data in its entirety for every valid request sent to the

RetrieveMpaXml web method. Each response is a snapshot of the corresponding MPA’s data from

the Boarding Application at the time the retrieval request is made.

Only one full MPA is returned per one call made to RetrieveMpaXml. Only the submitter is allowed

to retrieve the MPA they have submitted via Boarding API.

There are many reasons a retrieval request can fail, e.g. Boarding API web service is not available,

retrieval request supplies invalid parameters. In these cases Boarding API users are advised to

Omaha Boarding Specification.docx

Page 40 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





submit their retrieval request at a later time after all failure reasons have been identified and dealt

with.

**Failed Retrieval Response Sample (Non-existent MPA ID)**

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">

<RetrieveMpaXmlResponse xmlns="http://tempuri.org/">

<RetrieveMpaXmlResult>

<SubmitMPAResult xmlns="">

<Timestamp>12/10/2015 04:32:17 PM</Timestamp>

<Status>Invalid MPAID - 41000</Status>

</SubmitMPAResult>

</RetrieveMpaXmlResult>

</RetrieveMpaXmlResponse>

</s:Body>

</s:Envelope>

**Successful Retrieval Response Sample**

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">

<RetrieveMpaXmlResponse xmlns="http://tempuri.org/">

<RetrieveMpaXmlResult>

<ApplicationInformation xmlns="">

……………………………………………………………………………………………………

………………………………………………………………………………………………………………………………………………………

………………………………………………………………………………………………………….

</ApplicationInformation>

</RetrieveMpaXmlResult>

</RetrieveMpaXmlResponse>

</s:Body>

</s:Envelope>

**5.4 MPA STATUS REPORTING**

Below is the list of the status codes / status attributes with the possible values in the order of

their possible occurrence.

**Status Code/Status**

**Attribute**

**Description**

**Report**

**Level**

**Possible**

**Values/Information**

MPA

The overall MPA Status

MPA

In Process

Cancelled

Declined

Deleted

Omaha Boarding Specification.docx

Page 41 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Error

Boarded

MpaKey

MPA Key Status

MPA

MPA

Cancelled

In Process

Returned

Re-Submitted

Submitted

ClientApproval

MPA Client Approval

Status

In Process

Cancelled

Declined

Auto Approved

Approved with Changes

Approved

Direct Send

Locked for Decisioning

Returned

Merchant2Approval

MPA Merchant Owner 2

Approval Status

MPA

In Process

Approved

Approved with Changes

Cancelled by Merchant

Cancelled by Timeout

In Process

Expired

Omaha Boarding Specification.docx

Page 42 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Stopped On Action

Suspended

Merchant1Approval

MPA Merchant Owner 1

Approval Status

MPA

In Process

Approved

Approved with Changes

Cancelled by Merchant

Cancelled by Timeout

In Process

Expired

Stopped On Action

Suspended

MerchantChangeApproval MPA Merchant Change

Approval Status

MPA

No Approval Required

In Process

Declined

Approved

Transmission

VAPPBoarding

Transmission to VAPP

Status

MPA

MPA

In Process

Error

Success

MPA VAPP Boarding

Status

Boarded

In Process

Error

Underwriting

MPA Underwriting Status MPA

Risk Identified

Account Pending with

Credit

Omaha Boarding Specification.docx

Page 43 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Credit Approved

Credit Declined

In Process

Account Sent to Credit

Complete

BackEnd

Amex

Location Back End Setup

Status

Location

Location

In Process

Location Amex Setup

Status

Amex SE# Assigned

Account Sent to Amex

Complete

Merchant data sent to

RRS.

Pending Amex Setup

Complete

In Process

Success

TeleCheck

Location TeleCheck Setup Location

Status

LocationBoarding

LocationEquipment

Location Boarding Status Location

In Process

Pending Setup

Complete

In Process

In Process

Complete

In Process

Error

Location Equipment Front Location

End Setup Status

LocationNashville

LocationDatawire

Location Nashville Front

End Setup Status

Location

Location

Location Datawire Setup

Status

Complete

Omaha Boarding Specification.docx

Page 44 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





LocationFEOmaha

LocationFECardnet

LocationClover

Location Omaha Front

End Setup Status

Location

Location

Location

Location

In Process

Error

Complete

In Process

Error

Location Cardnet Front

End Setup Status

Complete

In Process

Error

Location Clover Setup

Status

Complete

In Process

Error

LocationRapidConnect

Location Rapid Connect

Setup Status

Complete

Since every status attribute has multiple status values, it will be reported multiple times based

on the status value updates. The status attributes which have the Report Level = “MPA” will be

reported on the first Location only, the others which have the Report Level = “Location” will be

reported on any Locations that have the status updates.

The status attributes table above contains all possible status attributes with status values.

However, reporting the status will totally depend on the MPA Type and the MPA data. The

following cases will explain how reporting status varies by MPA:

\-

Based on the MPA data, some of the status attributes may not be reported. For example, in an

MPA, if the Equipment Front End has not been set up for say Location #2, then Location #2 will

not have any of the Front End Statuses reported such as LocationEquipment, LocationNashville,

LocationDatawire, LocationFEOmaha, LocationFECardnet, LocationClover, LocationRapidConnect.

The status attributes which relate to Merchant Approval process such as Merchant2Approval,

Merchant1Approval, MerchantChangeApproval will not be reported for the MPAs submitted via

the API because all of them are Standard MPAs which do not require Merchant Approval. These

are identified for future use.

\-

Omaha Boarding Specification.docx

Page 45 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**5.5 MERCHANT INFORMATION XML FORMAT**

The details of Merchant Information in XML format/elements are described in the excel

spreadsheet “Master Mapping for Omaha API XML V3.2”. For more information on

implementation and XSD validation, please refer to the XSD document of

“OmahaAPI\_XMLSchema\_V2.6”.

**5.5.1 sample xml**

Omaha Retail

12092015.xml

Omaha Wholesale

12092015.xml

**5.6 MERCHANT INFORMATION VALIDATION HANDLER**

The validation handler will conduct two steps of validation against the Merchant Information

details. The following descriptions show how these steps function.

**Schema Validation**

This is the first step of validation to ensure the received XML content has well-formed structure

and valid enumerations that conform to the enumeration definition in the XML schema. If it

successfully passes the schema validation, the following steps will be conducted. Otherwise, the

error message will show specifically to every violation against the schema definition.

Error message received: Could not find schema information for the element

Correct schema

<ApplicationInformation>

<MpaInfo>

<MpaMerchantType>S</MpaMerchantType>

<ClientType>RETAIL</ClientType>

<SystemNumber>8740</SystemNumber>

<PrinNumber>9900</PrinNumber>

<Agent/>

<SalesID>0000</SalesID>

Incorrect schema

<tem:ApplicationInformation>

< tem:MpaInfo>

< tem:MpaMerchantType>S</MpaMerchantType>

< tem:ClientType>RETAIL</ClientType>

< tem:SystemNumber>8740</SystemNumber>

< tem:PrinNumber>9900</PrinNumber>

< tem:Agent/>

< tem:SalesID>0000</SalesID>

Omaha Boarding Specification.docx

Page 46 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**5.7 CONDITIONAL DATA LOGIC VALIDATION**

This step will ensure all the Merchant Information details conform to the MPA Capture edits.

The validation rules and error messages are defined in the following table.

Description of Validation Performed

**Error Message**

**General Validation**

The validation of conditionally mandatory fields,

value range, etc. Identified in the Master Mapping

for Omaha API XML spreadsheet.

Location NN: {Section Name} Errors!

When Agent is not specified for the Merchant

Information, the grid level cannot be Agent

State must be Puerto Rico when SYS selected in

Business Info/Ownership = 1572.

Invalid {Grid Name} Level.

Location NN: {Section Name} - State must

be Puerto Rico with SYS 1572.

State must be Virgin Islands when SYS selected in

Business Info/Ownership = 1396

Location NN: {Section Name} – State must

be Virgin Islands with SYS 1396

**MPA Info Validation**

NumberOfLocation and the added locations

conflict

Location NN: MPA Info - Locations field

does not reflect the number of locations

added.

**Signatures Validation**

Signature Date Signed fields are required when

MPA Type = Standard

Location NN: Signatures - Date Signed

fields are required

**Business Info Validation**

Cash advance Merchant are identified where the

MCC = 6010 or 6011

Location NN: Business Info - MCC = 6010

or 6011 is required for Assessment Code =

03 - Cash Advance Merchant.

Location NN: Business Info - Assessment

Code "03 - Cash Advance Merchant" must

be selected when MCC code is 6010 or

\6011.

Business Website Address, Technical Contact,

Location NN: Business Info - Business

Technical Phone & Technical Contact Email become Website Address is required for "YourPay

required fields if below equipments are present in

the submitted XML file:

Connect/ YOURPAY SP CONVERT"

Equipment selection.

ID

30

447

Equipment Type Description

Equip\_Code

400072

2

2

YourPay Connect

YourPay SP Convert 819320

Business Website Address, Technical Contact,

Location NN: Business Info - Technical

Technical Phone & Technical Contact Email become Contact is required for "YourPay Connect/

Omaha Boarding Specification.docx

Page 47 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





required fields if below equipments are present in YOURPAY SP CONVERT" Equipment

the submitted XML file:

selection.

ID

30

447

Equipment Type Description

Equip\_Code

400072

2

2

YourPay Connect

YourPay SP Convert 819320

Business Website Address, Technical Contact,

Location NN: Business Info - Technical

Technical Phone & Technical Contact Email become Phone is required for "YourPay Connect/

required fields if below equipments are present in

the submitted XML file:

YOURPAY SP CONVERT" Equipment

selection.

ID

30

447

Equipment Type Description

Equip\_Code

400072

2

2

YourPay Connect

YourPay SP Convert 819320

Business Website Address, Technical Contact,

Location NN: Business Info - Technical

Technical Phone & Technical Contact Email become Contact Email is required for "YourPay

required fields if below equipments are present in

the submitted XML file:

Connect/ YOURPAY SP CONVERT"

Equipment selection.

ID

30

447

Equipment Type Description

Equip\_Code

400072

2

2

YourPay Connect

YourPay SP Convert 819320

Business Email Address is required when

GGE4Indicator = YES and SIC = 5969)

Business Website Address is required when SIC =

5969

Location NN: Business Email Address is

required

Location NN: Business Info - Business

Website Address is required

Invalid Tax ID

Location NN: Business Info - Federal Tax Id

is invalid

If Business Type = "Sole Proprietorship" then

Federal Tax Id must be "SSN"

**Business Type:**

**1. Two existing business types have their**

**description changed:**

\+ Private Partnership (formerly Partnership)

\+ Private Limited Liability Company (formerly

Limited Liability Company)

Location NN: Federal Tax ID Type must be

SSN with Business Type of Sole Proprietor.

In case “Association/Estate/Trust” or

“International Organization” is selected

with AMEX Opt Blue specified.

"Location NN: Corporate Info - Business

Type - "Association/Estate/Trust" and

"International/Organization" are not

allowed for American Express."

**2. Two new business types are added:**

\+ Publicly Traded Partnership

\+ Publicly Traded Limited Liability Company

**Settlement Validation**

Invalid ABA Number

Location NN: Settlement - ABA Number

entered is not a valid ABA Number

**Processing Validation**

Omaha Boarding Specification.docx

Page 48 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**If GGE4 indicator – Y**

Location NN: Processing – Invalid {field

name} option.

If TransArmor Service Code is ‘00’ and encryption

type is ‘00’, token indicator must be spaces.

If TransArmor Service Code is ’03’ and encryption

type is ‘00’, token indicator must be ‘H’ or ‘M’

TransArmor Service Code 01 is not allowed for

GGe4 enabled merchants (gge4 ind =Y)

**If GGE4 indicator – N**

If TransArmor Service Code is ‘00’ and encryption

type is ‘00’, token indicator must be spaces.

If TransArmor Service Code is ‘01’ and encryption

type must be ‘01’ or ‘02’, token indicator must be

‘H’ or ‘M’ or ‘T’.

If TransArmor Service Code is ‘03’ and encryption

type is ‘00’, token indicator must be ‘H’ or ‘M’ or

‘T’.

In MPA entry for Retail, Wholesale, or FSP, If

Location NN: Processing - 01 - Encryption

Clover Equipment has been selected, the following and Tokenization TransArmor Service

TransArmor selections are required: Code is required for Clover Equipment.

\1. TransArmor Service Code must be selected = "01 Location NN: Processing - 01 - RSA/PKI

\- Encryption and Tokenization".

\2. Encryption Type must be selected = "01 -

RSA/PKI".

Encryption Type is required for Clover

Equipment.

Location NN: Processing - T - Token

Indicator is required for Clover Equipment.

\3. Token Indicator must be selected = "T - Token".

If Mobile pay is selected then the CAT Indicator for Visa Location NN: Processing - Visa CAT

Entitlement = “9 - Mobile Acceptance Solution”

Indicator must be “9 - Mobile Acceptance

Solution” when Mobile Pay is selected

If Mobile pay is selected then the CAT Indicator for Location NN: Processing - MC CAT

MasterCard Entitlement = “9 - Mobile Acceptance

Solution”

If Deposit Type = ETC and pin debit entitlement is

Indicator must be “9 - Mobile Acceptance

Solution” when Mobile Pay is selected

Location NN: ETC Type must be 7 or B for

PIN Debit entitlement.

selected then ETC Type has to be 7 or B

If the MPA is Bundle Option 0 and PIN Entitlements Location NN: Processing - ETC Type not

are enabled, then ETC\_Type must be ‘ETC Type 7’

or ‘ETC Type B’

valid for Pricing Option

If the MPA is Bundle Option 1, then ETC\_Type must

be ‘ETC Type 7’ or ‘ETC Type B’

Omaha Boarding Specification.docx

Page 49 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





If the MPA is Bundle Option 2, then ETC\_Type must

be ‘ETC Type 7’ or ‘ETC Type B’

If the MPA is Bundle Option 3 and PIN Entitlements

are enabled, then ETC\_Type must be ‘ETC Type 7’

or ‘ETC Type B’

If the MPA is Bundle Option 4, then ETC\_Type must

be ‘ETC Type 7’ or ‘ETC Type B’

GGE4 Effective Date must be today’s date or a future

date.

Location NN: Processing - The GGE4

Effective Date must be today’s date or a

future date.

Visa Aggregator constraint

Location NN: Processing - Selected Visa

Aggregator is not allowed for Location's

SIC Code.

Insightics Product Type Code = “1 – Standard Offering”

can only be selected if an MFC Grid has been selected

and contains the Fee = "MRCMAP01".

Location NN: “1 - Standard Offering”

Insightics Product Type Code can only be

selected when MFC Grid has been

selected and contains the Fee =

"MRCMAP01".

**Transaction Validation**

Annual MC Visa Sales Volume is required when MC Location NN: Transactions - Annual

is selected and Visa is selected in Bank Card

Entitlements

MC/VISA Credit Sales Volume is required

Annual American Express Credit Sales Volume is

required when American Express is selected

Location NN: Transactions - Annual

American Express Credit Sales Volume is

required

Annual Discover Credit Sales Volume must not be

specified when Discover is not selected

Location NN: Transactions - Annual

Discover Credit Sales Volume must not be

specified.

**Pricing Validation**

At least one of the following entitlements should

Location NN: Pricing – Invalid Bankcard

Entitlements options.

be selected

Visa Credit

Visa Debit

MC Credit

MC Debit

Pin Debit entitlement is allowed only for the

following SIC codes

3412 3438 3439 3506 3513 3538 3542 3555 3556

3565 3573 3578 3579 3583 3587 3618 3619

Location NN: Bundled Pricing Option -

Option 1, Option 2 and Option 4 are not

allowed for Location's SIC Code of {0}.

Omaha Boarding Specification.docx

Page 50 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





3624 3627 3631 3632 3634 3635 3639 3640 3646

3647 3650 3660 3674 3682 3689 3695 3699

3706 3707 3710 3720 3726 3730 3732 3746 3754

3761 3762 3770 3773 3777 3789 3792 3809

3811 4112 4225 4723 4789 5310 5399 5422 5511

5592 5631 5691 5722 5735 5937 5940 5942

5998 6011 7033 7230 7297 7299 7538 7692 7699

8041 8111 8220 8241 8651 8699 9752 1520

1750 3002 3003 3006 3027 3034 3040 3049 3065

3071 3077 3081 3117 3129 3133 3137 3151

3167 3174 3187 3197 3203 3213 3233 3252 3254

3256 3292 3302 3322 3333 3334 3342 3343

3354 3361 3368 3370 3396 3431 3436 3503 3504

3514 3515 3522 3544 3548 3550 3551 3557

3562 3575 3588 3597 3599 3609 3610 3617 3621

3636 3649 3655 3668 3702 3708 3715 3729

3731 3734 3735 3742 3751 3767 3771 3776 3787

3801 3808 4119 4215 5441 5571 5598 5699

5712 5713 5811 5813 5933 5963 5970 5978 5992

5995 6513 7211 7277 7296 7339 7512 7513

7519 7929 7933 8211 9751 0780 3004 3010 3011

3016 3017 3019 3028 3035 3039 3058 3061

3062 3079 3088 3090 3136 3144 3145 3146 3154

3175 3186 3190 3219 3222 3229 3260 3261

3294 3296 3306 3318 3324 3326 3331 3351 3366

3425 3429 3435 3511 3516 3520 3526 3530

3537 3553 3554 3585 3589 3600 3604 3608 3613

3622 3629 3633 3638 3641 3661 3670 3677

3688 3703 3709 3718 3719 3724 3733 3744 3765

3768 3774 3798 3800 3806 3814 4111 4214

5200 5499 5542 5599 5621 5714 5719 5931 5946

5972 6012 6051 6381 6532 7012 7273 7321

7995 7996 8042 8244 0742 1799 3000 3005 3009

3024 3043 3046 3050 3084 3096 3103 3106

3138 3159 3170 3196 3211 3223 3234 3236 3241

3245 3259 3285 3300 3321 3325 3332 3338

3353 3357 3362 3380 3381 3385 3394 3414 3433

3434 3437 3502 3508 3510 3521 3524 3525

3527 3533 3540 3549 3566 3567 3571 3572 3581

3584 3603 3607 3616 3628 3630 3644 3651

Location NN: PIN Debit entitlements are

not allowed for Location's SIC Code of {0}.

Omaha Boarding Specification.docx

Page 51 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





3652 3653 3664 3671 3672 3673 3681 3686 3692

3694 3700 3711 3712 3736 3757 3794 3803

3804 3810 4121 4722 4900 5211 5251 5551 5661

5697 5733 5812 5947 5949 5996 5997 7221

7261 7372 7531 7999 8031 8049 8062 8249 8398

8661 8911 3007 3012 3013 3021 3023 3030

3032 3036 3051 3053 3060 3064 3076 3078 3082

3087 3100 3118 3131 3148 3156 3176 3206

3212 3218 3220 3221 3231 3242 3284 3287 3293

3304 3313 3320 3328 3336 3337 3340 3346

3350 3360 3387 3405 3420 3423 3528 3535 3541

3543 3563 3568 3570 3574 3577 3582 3593

3595 3601 3605 3614 3642 3645 3659 3678 3690

3691 3696 3725 3739 3747 3750 3797 3802

3812 4011 4457 4511 4829 4899 5261 5300 5331

5462 5533 5681 5943 5950 5971 6211 6300

7032 7338 7342 7349 7395 7511 7629 7631 7641

7841 7932 7998 8011 9211 9222 9223 9331

1711 1771 3001 3018 3026 3037 3048 3054 3057

3059 3068 3099 3110 3238 3246 3262 3298

3307 3310 3312 3315 3319 3329 3345 3347 3355

3376 3389 3390 3393 3395 3421 3501 3507

3509 3517 3518 3531 3546 3558 3560 3564 3591

3592 3598 3612 3615 3623 3657 3663 3669 3679

3683 3697 3698 3701 3705 3722 3723 3727 3745

3748 3755 3756 3763 3764 3781 3790

3793 3805 4131 4411 4814 5311 5541 5561 5641

5651 5941 5973 5994 6050 6399 6534 7210

7216 7311 7399 7549 7622 7623 7922 7941 7991

7992 7994 7997 8044 8071 8099 9402 1740

3022 3029 3031 3038 3044 3047 3056 3067 3097

3112 3125 3165 3177 3180 3181 3184 3188

3191 3193 3215 3216 3226 3240 3247 3266 3267

3282 3286 3299 3301 3308 3327 3335 3339

3388 3391 3400 3409 3427 3430 3519 3523 3536

3539 3569 3580 3586 3596 3611 3625 3637

3656 3662 3665 3667 3675 3676 3685 3693 3714

3716 3717 3738 3740 3743 3752 3759 3772

3775 3778 3779 3782 3783 3788 3796 3799 3807

3813 4468 4582 4821 5309 5611 5698 5732

Omaha Boarding Specification.docx

Page 52 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





5814 5948 6010 6533 7011 7251 7276 7298 7392

7393 7394 7542 7911 8021 8043 8351 8641

8999 1761 3008 3014 3042 3045 3052 3083 3089

3094 3095 3102 3127 3130 3132 3135 3161

3164 3183 3185 3192 3204 3217 3235 3239 3243

3248 3263 3297 3303 3309 3311 3314 3344

3352 3359 3374 3386 3428 3432 3441 3505 3512

3529 3532 3534 3545 3547 3552 3559 3561

3576 3590 3594 3602 3606 3620 3626 3643 3648

3654 3658 3666 3680 3684 3687 3704 3713

3721 3728 3737 3741 3749 3753 3758 3760 3766

3769 3780 3784 3785 3786 3791 3795 4812

5231 5271 5411 5451 5521 5532 5655 5718 5734

5912 5921 5932 5935 5944 5945 5975 5976

5977 5983 5993 5999 6529 6530 7217 7278 7361

7523 7534 7535 7832 7993 8050 8299 8675

8931 9399 0763 1731 3015 3020 3025 3033 3041

3055 3063 3066 3075 3085 3086 3098 3111

3115 3126 3143 3171 3172 3178 3182 3200 3228

3251 3253 3280 3295 3305 3316 3317 3341 3348

3349 3364 3398

The following fee class values are valid for

MasterCard Credit entitlement

012 - Merit 3

049 - AUTO RENTAL

050 - TRVL LODGNG

001 - Merit 1

051 - TRVL CRUISE

015 - Supermarket

000 - Domestic

011 - SIP

017 - Domestic PT

031 - CONVPRCH

283 - PTROB5541

283 - PTROB5542

156 - UTILITIES

089 BPCR-REALEST

003 - Standard Credit

006 - Electronic Credit

Omaha Boarding Specification.docx

Page 53 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





The following fee class values are valid for

MasterCard Debit entitlement

083 - TRVL DEBIT

106 PSSD5541

075 DOMDEBIT

076 MERIT ID

077 SIPDEBIT

078 MERIT 3D

079 SUPRMK TD

080 MCPSS TRD

105 PCAFD5542

157 - UTILITIES

074 BPDB-REALEST

003 - Standard Debit

006 - Electronic Debit

The following fee class values are valid for Visa

Credit entitlement

007 - CPS RET CR

043 - CPS H&CR Card Present

034 - CPS PT Credit

055 - EIRF All Other

038 - CPS T & E Credit

015 - SPMKT CR

000 - Domestic A/O

099 - CPS Restaurant

011 - CPS MPHN

046 - CPS D/M

081 – CPSECBTE

076 – CPSECOMB

045 - CPS AUTOMATED FUEL DISP

100 - CPS RETAIL SRVC STATION

025 - CPS RET 2

044 - CPS H And CR CNP

012 – Charity

003 - Standard Credit

006 - Electronic Credit

009 - Recurring Bill payment (Only allowed for

SIC Code 4814 or 4899)

Omaha Boarding Specification.docx

Page 54 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





The following fee class values are valid for Visa

Debit entitlement

120 DOMA/ODB

132 CPS RESTAURANT

101 CPS RTDD

116 CPSPTDB

107 CPSCNPDB

103 SPMT DDB

114 HTCRCPRD

119 EIRFDB

111 CPSECBDB

127 CPSECTED

108 CPS AUTOMATED FUEL DISP

133 CPS SRVC STATION DEBIT

105 CPS RET 2

113 H And C CNP

003 - Standard Debit

006 - Electronic Debit

The following fee class values are valid for Discover

Credit entitlement

100 Recurring Payments-Rewards

102 Sprmkts/Warehse-Rewards

104 Emerging Markets-Rewards

106 Public Services-Rewards

108 Express Services-Rewards

110 Petroleum-Rewards

112 Retail-Rewards

114 Restaurants-Rewards

116 Hotel/Car Rental-Rewards

118 Passenger Trans-Rewards

120 Card Not Pres/ECom-Rewards

122 Key Entry-Rewards

125 Mid Submission Lvl-Rewards

127 Base Sub Lvl-Rewards

137 Utilities-Rewards

180 (PSL-Insurance Rewards)

The following fee class values are valid for Discover

Debit entitlement

Omaha Boarding Specification.docx

Page 55 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





101 PSL-Automatic Payments

103 PSL-Sprmkts/Warehse Clb

105 PSL-Emerging Markets

107 PSL-Public Services

109 PSL-Express Services

111 PSL-Petroleum

113 PSL-Retail

115 PSL-Restaurants

117 PSL-Hotel/Car Rental

119 PSL-Passenger Transport

121 Card Not Prsnt/E-Commerce

123 PSL-Key Entry

124 Commercial Electric

126 Mid Submission Level

128 Base Submission Level

138 Utilities

182 (PSL-Insurance Debit)

The following fields should be collected for MC credit

and debit

a. Card Type

b. Tiered Discount ID

c. Fee Class

d. Dues and Assessment

e. ERR%

f. Pricing grid ID

g. Interchange Fee Flag

h. Discount Rate

i. Mid Qual rate

j. Non Qual Rate

k. CAT Indicator

l. NABU Indicator

m. Acquirer Support Fee Indicator

n. Cross Border Fee Indicator

o. Processor Integrity fee

p. KiloByte Fee Indicator (Credit Only)

q. License Flat occurrence Indicator

(Credit Only)

Omaha Boarding Specification.docx

Page 56 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





r. CVC2 Fee Indicator (Credit Only)

s. Regulated\_ERR\_Flag (Debit Only)

t. Discount Method

u. Tiered Discount Grid Level

v. Pricing Grid Level

The following fields should be collected for Visa credit

and debit

a. Card Type

b. Tiered Discount ID

c. Fee Class

d. Dues and Assessment

e. ERR%

f. Pricing grid ID

g. Interchange Fee Flag

h. Discount Rate

i. Mid Qual rate

j. Non Qual Rate

k. CAT Indicator

l. Acquirer ISA Fee override

m. Acquirer Processor Fee

n. Zero floor limit fee

o. Misuse Auth fee

p. International Acquirer fee

q. Transaction Integrity fee

r. Fixed acquirer network fee (only available for

Visa Credit)

s. Kilo Byte Fee Indicator (only available for Visa

Credit)

t. Regulated\_ERR\_Flag (Debit Only)

u. Visa\_Business\_ID (applicable For Wholesale

ISO only)

v. Discount Method

w. Tiered Discount Grid Level

x. Pricing Grid Level

Omaha Boarding Specification.docx

Page 57 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





The following fields should be collected for Discover Full

Service credit and debit

a. Card Type

b. Tiered Discount ID

c. Fee Class

d. Dues and Assessment

e. ERR%

f. Pricing grid ID

g. Interchange Fee Flag

h. Discount Rate

i. Mid Qual rate

j. Non Qual Rate

k. Industry Indicator

l. International processing fee

m. International service fee

n. Data usage fee

o. Network Auth Fee Indicator (For Discover

credit only)

p. Regulated\_ERR\_Flag (Debit Only)

q. Discount Method

r. Tiered Discount Grid Level

s. Pricing Grid Level

For MCC = 4900 fee class “012 - Merit 3” is not

allowed for MasterCard Credit.

Location NN: Pricing – Invalid Fee Class for

selected Location’s SIC Code

For MCC = 4812 or 5960 or 6300 fee class “011 -

SIP” is not allowed for MasterCard Credit

For MCC = 4900 fee class “076 MERIT ID” is not

allowed for MasterCard Debit.

For MCC = 4812 fee class “077 SIPDEBIT” is not

allowed for MasterCard Debit.

For MCC = 4812 6513 fee class “078 MERIT 3D” is

not allowed for MasterCard Debit.

If MCC code entered by ISO ranges between 3351

to 3441 or 3501 to 3999. Discover Full Acquiring

will not be allowed.

Location NN: Pricing – Discover Full

Acquiring is not allowed for selected SIC

Code.

Omaha Boarding Specification.docx

Page 58 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Discount Method Should be equal to None when

Statement Bundled option Is not equal to None

Location NN: Discount Method must be

equal to None when Statement Bundled

option is not equal to None

If statement bundled option is not equal to none

you have to either have Bundled percent and rate

OR Regulated rate and percent AND Unregulated

rate and percent

If statement bundled option = “Bundled fees for PIN

Debit only” Pin debit entitlement is required.

w. Other item rate and other volume % are not

required will be set to 0

x. Online debit fee calc flag will be set to 0

If statement bundled option = “Bundled fees for PIN

and Signature Debit combined” Pin debit entitlements

and Signature Debit entitlements are required.

a. Other item rate and other volume %

are not required will be set to 0

b. Online debit fee calc flag will be set to 0

c. Pricing grid ID cannot be entered

d. Tiered Grid ID cannot be entered

e. Mid Qual rate should be 0

f. Non Qual rate should be set to 0

g. Interchange fee calc flag should be set

to 3 or 0 for Signature debit

h. Interchange fee calc flag should be set

to 0 for signature debit

i. Statement intcg print option should be

“Blank - Use Inter. Fee Prt Opt. in PCF”

If statement bundled option = “Bundled fees for

Signature Debit only” Signature Debit entitlements are

required.

Omaha Boarding Specification.docx

Page 59 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





a. Other item rate and other volume % are

not required will be set to 0

b. Online debit fee calc flag will be set to 0

c. Pricing grid ID cannot be entered

d. Tiered Grid ID cannot be entered

e. Mid Qual rate should be 0

f. Non Qual rate should be set to 0

g. Interchange fee calc flag should be set to 3

or 0 for Signature debit

h. Statement intcg print option should be

“Blank - Use Inter. Fee Prt Opt. in PCF”

If statement bundled option = “Bundled fees for PIN

Debit, Signature Debit and Credit combined” then

Signature debit, credit and pin debit entitlements are

required

a. Other item rate and other volume % are

not required will be set to 0

b. Online debit fee calc flag will be set to 0

c. Pricing grid ID cannot be entered

d. Tiered Grid ID cannot be entered

e. Mid Qual rate should be 0

f. Non Qual rate should be set to 0

g. Interchange fee calc flag should be set to 3

or 0 for Signature debit / credit

h. Interchange fee calc flag should be set to 0

for pin debit

i. Statement intcg print option should be

“Blank - Use Inter. Fee Prt Opt. in PCF”

If MPA Client Type = Retail, Prin number contains

'Tier 2' and Discount Method must be 'Daily'

Location NN: Pricing - Discount Method

must be Daily for Tier 2

**Other Entitlements Validation**

American Express entitlement cannot be selected

for estimated AMEX sales > 1MM.

Location NN: Other Entitlement -

American Express option can only be

selected under eligible Franchise if the

Annual American Express Sales Volume is

less than $1,000,000.

Omaha Boarding Specification.docx

Page 60 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





American Express is not allowed for "Puerto Rico." Location NN: American Express is not

or "Virgin Islands, U.S."

allowed for "Puerto Rico." or "Virgin

Islands, U.S."

If Existing Amex ESA is selected the following fields are

required

a. Card Type

b. SE #

If American Express is selected the following fields are

required

a. Discount Rate

b. Fee Class

c. Mid Qual

d. Non Qual

e. Tiered Grid ID

f. Pricing Grid ID

g. Enhanced reduced Recovery Percent

h. Interchange Fee Flag

i. Amex Volume

j. Other Volume Percent

k. Other Item Rate

l. Discount Method

m. Tiered Discount Grid Level

n. Pricing Grid Level

Amex Full service / American Express Entitlement

can be selected if SIC Code is one of the following

values

Location NN: Other Entitlement -

American Express option can only be

selected under eligible Franchise if the

0742, 0743, 0744, 0763, 0780, 1520, 1711, 1731, 1740, Annual American Express Sales Volume is

1750, 1761, 1771,

less than $1,000,000.

1799, 2741, 2791, 2842, 4119, 4121, 4131, 4214, 4215,

4225, 4457, 4468,

4582, 4722, 4789, 4812, 4821, 4900, 5013, 5021, 5039,

5044, 5045, 5046,

5047, 5051, 5065, 5072, 5074, 5085, 5099, 5111, 5122,

5131, 5137, 5139,

5169, 5192, 5193, 5198, 5200, 5211, 5231, 5251, 5261,

5271, 5309, 5310,

Omaha Boarding Specification.docx

Page 61 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





5311, 5331, 5399, 5411, 5422, 5441, 5451, 5462, 5499,

5511, 5521, 5531,

5532, 5533, 5541, 5542, 5551, 5561, 5571, 5592, 5598,

5599, 5621, 5631,

5641, 5651, 5655, 5661, 5681, 5691, 5697, 5698, 5699,

5712, 5713, 5714,

5715, 5718, 5719, 5722, 5732, 5733, 5734, 5735, 5811,

5812, 5813, 5814,

5912, 5921, 5931, 5932, 5933, 5935, 5937, 5940, 5941,

5942, 5943, 5944,

5945, 5946, 5947, 5948, 5949, 5950, 5964, 5965, 5968,

5969, 5970, 5971,

5972, 5973, 5975, 5976, 5977, 5978, 5983, 5992, 5993,

5994, 5995, 5996,

5997, 5998, 5999, 6300, 7011, 7032, 7033, 7210, 7211,

7216, 7217, 7221,

7230, 7251, 7261, 7276, 7277, 7278, 7296, 7298, 7299,

7311, 7333, 7338,

7339, 7342, 7349, 7361, 7372, 7375, 7379, 7392, 7393,

7394, 7395, 7399,

7523, 7531, 7534, 7535, 7538, 7542, 7549, 7622, 7623,

7629, 7631, 7641,

7692, 7699, 7829, 7832, 7841, 7911, 7922, 7929, 7932,

7933, 7941, 7991,

7992, 7993, 7994, 7996, 7997, 7998, 7999, 8011, 8021,

8031, 8041, 8043,

8049, 8050, 8062, 8071, 8099, 8111, 8211, 8220, 8241,

8244, 8249, 8299,

8351, 8398, 8641, 8661, 8675, 8699, 8734, 8911, 8931,

8999, 8042, 5199,

5094, 5611, 5300, 7321, 4816, 4899, 8651

New Amex Cap number is not allowed for MOTO or

internet merchants

Multiple outlet merchant should have a cap

number

Monthly flat fee is not allowed when a New Cap

number is selected for Amex ESA

Omaha Boarding Specification.docx

Page 62 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Add an edit to not allow special characters in the name

fields (DBA, Legal) etc. if Amex was selected the

allowable special characteristics, Amex supports are as

follows:

a. all US alphanumeric

b. ampersand

c. apostrophe

d. asterisk

e. back and forward slash

f. colon

g. comma

h. exclamation mark

i. hyphen

j. plus

k. pound or number sign

l. period

m. question mark

n. quote

o. underscore

Location NN: Other Entitlements -

Selected AMEX Fee Class is not allowed for

Location's SIC Code of XXXX

Restricted MCC for American Express…

• Digital Goods - Applications (Excludes Games) 5817

• Digital Goods - Games 5816

• Digital Goods - Large Digital Goods Merchant 5818

• Digital Goods - Media, Books, Movies, Music 5815

• Government - Licensed Casinos (Online Gambling)

7801

• Government - Licensed Horse/Dog Racing 7802

• Government - Owned Lotteries 7800

Wright Express entitlement can be selected only if Location NN: Other Entitlements – Wright

SIC code is one of the following values

5511, 5521, 5532, 5533, 5541, 5542, 7531, 7534,

7535, 7538, 7542, 7549, 7699, 8675

Express entitlement is not allowed for

selected SIC

If Wright express is selected the following fields are

required

a. Card Type

Omaha Boarding Specification.docx

Page 63 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Voyager entitlement can be selected only if SIC

code is one of the following values

5172, 5511, 5521, 5532, 5533, 5541, 5542, 7531,

7534, 7535, 7538, 7542, 7549, 7699, 8675

Voyager entitlement is not allowed for SYS = 1572

or 1396

Location NN: Other Entitlements - Voyager

entitlement is not allowed for selected SIC

Location NN: Other Entitlements –

Voyager entitlement is not allowed for

selected SYS.

If Voyager is selected the following field is required

a. Card Type

b. Discount Rate

c. Discount Method

TeleCheck entitlement is not allowed for ETC Type Location NN: Other Entitlements -

4

TeleCheck entitlement is not allowed for

ETC Type 4.

TeleCheck entitlement cannot be selected if SIC

Code is one of the following values

Location NN: TeleCheck (GGe4) is not

allowed for Location's SIC Code of {0}.

2791 4829 4816 5933 5960 5962 5963 5964 5965

5966 5967 5968 5969 6010

6011 6012 6050 6051 6211 6300 6381 6399 6529

6530 6531 6532 6533 6534

7273 7339 7392 7393 7399 7833 7941 7995 8931

8999 9223 9405 9700

If TeleCheck Entitlement is selected the TeleCheck N/A

compatible equipment should be selected

Please refer to the Equipment Spread sheet for

TeleCheck Compatible equipment. VARS are not

allowed when TeleCheck Entitlement is selected.

If TeleCheck entitlement is selected equipment is

mandatory.

TeleCheck Entitlement cannot be selected if the

ISO does not have an association code

The following fee class values are valid for Amex

Entitlement

N/A

N/A

001 - Retail

003 - Education

Omaha Boarding Specification.docx

Page 64 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





004 - Office based Healthcare

005 - Supermarket

006 – Mail Order Internet

007 - Restaurant

009 - Travel Transport

010 - Lodging

011 - Fast Food Restaurant

012 - Serv Wholesale All

013 - Independent Gas Station

018 - B2B

017 - Telecommunications

The following Fee class will be valid for American

Express Entitlement

N/A

500 - Retail Amount 1 (less than 75)

501 - Retail Amount 2 (75.01 – 1000)

502 - Retail Amount 3 (greater than 1000)

518 - HealthCare Amount 1(less than 150)

519 - HealthCare Amount 2 (150.01 to 2000)

520 - Healthcare Amount 3 (greater than

\2000)

524 - B2B /Wholesale Amount 1 (less than

\400)

525 - B2B/Wholesale Amount 2 (400.01-7500)

526 - B2B/Wholesale Amount 3 (greater than

\7500)

530 - Restaurant Amount 1 (less than 25)

531 - Restaurant Amount 2 (25.01 – 150)

532 - Restaurant Amount 3 (greater than 150)

536 - Bar/Caterer Amount 1(less than 25)

537 - Bar/Caterer Amount 2 (25.01 – 150)

538 - Bar/Caterer Amount 3(greater than 150)

542 - Svcs & Professional Svcs Amount 1 (less

than 400)

543 - Svcs & Professional Svcs Amount 2

(400.01 – 3000)

544 - Svcs & Professional Svcs Amount 3

(greater than 3000)

548 - Travel and Entertainment Amount 1 (less

than 100)

Omaha Boarding Specification.docx

Page 65 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





549 - Travel and Entertainment Amount 2

(100.01 – 1000)

550 - Travel and Entertainment Amount 3

(greater than 1000)

554 - Lodging Amount 1 (less than 100)

555 - Lodging Amount 2 (100.01 - 1000)

556 - Lodging Amount 3 (greater than 1000)

560 - Other Amount 1(less than 100)

561 - Other Amount 2(100.01 - 3000)

562 - Other Amount 3(greater than 3000)

569 - MO & Internet Amount 1 (less than 150)

570 - MO & Internet Amount 1 (150.01 - 3000)

571 - MO & Internet Amount 1 greater than

\3000)

If sys = 1572 and state = PR or sys = 1396 and state Location NN: Other Entitlements - Voyager

= VI then Voyager entitlement is not allowed

is not allowed for selected SYS

New Amex Cap number is not allowed for MOTO or Location NN: Other Entitlements - New

Internet merchants

Amex Cap number is not allowed for

MOTO or Internet merchants.

Both TeleCheck and TeleCheck GGe4 entitlement

cannot be selected.

Location NN: Other Entitlements - Both

GGe4 TeleCheck and TeleCheck

entitlement cannot be selected.

For American express entitlement

a. Fee class 500, 501 and 502 can be picked only for

the following MCC’s

Location NN: Other Entitlements – Invalid

Fee Class for selected Location’s SIC Code

5013, 5021, 5044, 5072, 5192, 5200, 5211, 5231,

5251, 5261, 5309, 5310, 5311, 5331, 5399, 5411,

5422, 5441, 5451, 5462, 5499, 5531, 5532, 5533,

5551, 5611, 5621, 5631, 5641, 5651, 5655, 5661,

5681, 5691, 5698, 5699, 5712, 5713, 5714, 5715,

5718, 5719, 5722, 5732, 5733, 5734, 5735, 5912,

5921, 5931, 5932, 5937, 5940, 5941, 5942, 5943,

5944, 5945, 5946, 5947, 5948, 5949, 5950, 5965,

5970, 5971, 5972, 5973, 5977, 5978, 5992, 5993,

5994, 5995, 5996, 5997, 5998, 5999, 7296, 7631,

7841

b. Fee Class 518, 519, 520 can be picked for the

following MCC’s

Omaha Boarding Specification.docx

Page 66 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





8011, 8021, 8031, 8041, 8042, 8043, 8049, 8050,

8062, 8071, 8099

c. Fee Class 524, 525, 526 can be picked for the

following MCC’s

0780, 1799, 2791, 4215, 5039, 5045, 5046, 5047,

5051, 5065, 5085, 5094, 5099, 5111, 5122, 5131,

5137, 5139, 5169, 5193, 5198, 5199, 6300, 7311,

7333, 7338, 7339, 7349, 7361, 7392, 7394, 7399,

7622, 7692, 7829, 7941, 8734, 8911, 8931, 8999

d. Fee class 530, 531, 532 can be selected for the

following mcc’s 5812, 5814

e. Fee class 536, 537, 538 can be selected for the

following mcc’s 5811, 5813

f. Fee class 542, 543, 544 can be selected for the

following mcc’s

0742, 0743, 0744, 0763, 1520, 1711, 1731,

1740, 1750, 1761, 1771, 2741, 2842, 4119,

4214, 4225, 4457, 4468, 4821, 4900, 5074,

5271, 5300, 5511, 5521, 5561, 5571, 5592,

5598, 5599, 5697, 5933, 5935, 5975, 5976,

5983, 7210, 7211, 7216, 7217, 7221, 7230,

7251, 7261, 7276, 7277, 7278, 7298, 7299,

7321, 7342, 7372, 7375, 7379, 7393, 7395,

7523, 7531, 7534, 7535, 7538, 7542, 7549,

7623, 7629, 7641, 7699, 7832, 7911, 7922,

7929, 7932, 7933, 7991, 7992, 7993, 7994,

7997, 7998, 8111, 8641, 8651, 8675, 8699

g. Fee class 548, 549, 550 can be selected for the

following mcc’s

4722, 7033, 7996, 7999

h. Fee class 554, 555, 556 can be selected for the

following mcc’s 7011

i. Fee class 560, 561, 562 can be selected for the

following mcc’s

4121, 4131, 4582, 4784, 4789, 4812, 4816, 4899,

5541, 5542, 7032, 8211, 8220, 8241, 8244, 8249,

8299, 8351, 8398, 8661, 9211, 9222, 9311, 9399

j. Fee class 569, 570, 571 can be selected for the

following mcc’s 5964, 5968, 5969

**Equipment and FE**

Omaha Boarding Specification.docx

Page 67 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





The validation of conditionally mandatory fields

identified in the Master Mapping for Omaha API

XML spreadsheet.

Location NN: Equipment and FE Errors!

The Bundle Options = 1, 2, and 4 are all options

which allow Pin Debit to be bundled. In all of these

cases, Clover Equipment should be restricted

Location NN: Equipment FE - Clover

Equipment is not allowed when Bundle

Pricing Options is equal to Option 1, 2 or

\4.

Clover can be selected if Business Type is Retail,

Restaurant or QSR

Location NN: Clover can only be selected

if Business Type is Retail, Restaurant or

QSR

If Clover is selected the following entitlements

cannot be selected

\1. TeleCheck

\2. TeleCheck (GGe4)

\3. EBT

Location NN: Equipment FE - Clover

Equipment cannot be selected when

Voyager [Wright Express,..] entitlement

has been selected.

\4. PayPal (Compass)

\5. Wright Express (WEX)

\6. Voyager

\7. Pin Debit

If sys = 1572 and state = PR and either Debit or EBT Location NN: Equipment FE – Nashville FE

entitlements are selected the merchant has to be

boarded to Nashville frontend

is required for selected SYS

If EBT Food stamp is selected the following fields are

required

a. Card Type

b. SE #

c. Interchange fee flag

If EBT Cash Benefit is selected the following fields is

required

a. Card Type

b. Interchange fee flag

If EBT third party is selected the following fields is

required

a. Car type

b. Interchange fee flag

Omaha Boarding Specification.docx

Page 68 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





If Debit is selected all 14 debit cards should be selected

and the following fields is required

a. Card Type

b. Online Debit fee calc flag

For the Debit (14 Card types ) and EBT (all 3) card types

The Interchange Fee flag can only have 2 values

a. Card Type

b. 0 - Do not pass IC Fees to Merchant

c. 1 - Pass Interchange Fee charges to

Merchant

For TeleCheck GGe4 entitlement we have to collect the

following

a. Card Type

b. Pay Check by phone

c. Internet check Acceptance

d. Remote Pay

If PayPal is selected the following fields are required

a. Card Type

If Mobile Pay is selected Pin Debit entitlement is

not allowed.

Location NN: Equipment - Equipment with

Mobile Pay Model is not allowed when

Bundle Pricing Options is equal to 0,1,2,3

and 4.

Shipping Info is required for Clover Equipment

Location NN: Equipment FE - Shipping Info

is required

Equipment selection is NOT allowed for ETC Type

\4.

Equipment validation:

Equipment selection is required with TeleCheck

entitlement.

Location NN: Equipment FE - Equipment

selection is NOT allowed for ETC Type 4.

Location NN: Equipment FE – Equipment

selection is required for TeleCheck

entitlement.

If ETC Type = 7, Omaha/Nashville/Cardnet/Buypass Location NN: Equipment FE – Only

FE is allowed.

If ETC Type 0, Nashville/Cardnet/Buypass FE is

allowed.

Omaha/Nashville/Cardnet/Buypass FE is

allowed for ETC Type 7.

Omaha Boarding Specification.docx

Page 69 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





If ETC Type = 4, Equipment selection is NOT

allowed.

If ETC Type = B, Omaha FE is allowed.

Location NN: Equipment FE - Only

Nashville/Cardnet/Buypass FE is allowed

for ETC Type 0.

Location NN: Equipment FE – Equipment

selection is not allowed for ETC Type 4.

Location NN: Equipment FE - Only Omaha

FE is allowed for ETC Type B.

Two existing pieces of equipment can no longer be

submitted with Nashville front end:

\+ VX510DC 12MEG Product Code: 160133

\+ VX570 FDPOS

Product Code: 160112

Equipment model (Fiserv FD55 Product Code:

\160129) cannot be submitted with a billing

method other than 1 - Client Deployed

"Outlet NN: Equipment and FE - 'Fiserv FD

55' cannot be selected with the Billing

Method 'Purchase'/'Lease 12

Months'/'Lease 24 Months'/'Lease 36

Months'/'Lease 48 Months'."

**Other Fees Validation**

The validation of conditionally mandatory fields

identified in the Master Mapping for Omaha API

XML spreadsheet.

Location NN: Other Fees Errors!

TeleCheck Gge4 Entitlement can be selected only

when GGe4 Indicator = Yes

Location NN: TeleCheck Gge4 Entitlement

can be selected only when GGe4 Indicator

= Yes

Do not allow TeleCheck GGe4 if SIC Code is in the

list

Location NN: TeleCheck (GGe4) is not

allowed for Location's SIC Code of {0}

'2791', '4829', '4816', '5933', '5960', '5962', '5963',

'5964', '5965', '5966', '5967', '5968', '5969', '6010',

'6011', '6012', '6050', '6051', '6211', '6300', '6381',

'6399', '6529', '6530', '6531', '6532', '6533', '6534',

'7273', '7339', '7392', '7393', '7399', '7833', '7941',

'7995', '8931', '8999', '9223', '9405', '9700'

Do not allow PayPal if SIC Code is in the list

Location NN: Other Fees - PayPal is not

'2791', '4829', '4816', '5933', '5960', '5962', '5963', allowed for Location's SIC Code of {0}.

'5964', '5965', '5966', '5967', '5968', '5969', '6010',

'6011', '6012', '6050', '6051', '6211', '6300', '6381',

'6399', '6529', '6530', '6531', '6532', '6533', '6534',

'7273', '7339', '7392', '7393', '7399', '7833', '7941',

'7995', '8931', '8999', '9223', '9405', '9700'

Omaha Boarding Specification.docx

Page 70 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**Client Expense Validation**

The validation of conditionally mandatory fields Location NN: Client Expense Errors!

identified in the Master Mapping for Omaha API

XML spreadsheet.

**Exceptions Validation**

The validation of conditionally mandatory fields

identified in the Master Mapping for Omaha API

XML spreadsheet.

Location NN: Exceptions Errors!

**6 High Level Test Cases**

**6.1 STARTING XML FILE**

Given the total number of XML fields, it is a lot more preferable to have a prepared XML file for

testing than to have to build a new XML file from scratch.

Based on Omaha API master mapping, various modifications can be made to this starting XML

file to suit different testing purposes.

**1.**

**Successful Submission**

**TEST CASE:**

Sucessful submission

**SUMMARY:**

The best case scenario flow starts with a successul submission of MPA via Boarding API. It is

also a pre-condition to further verfication of Omaha Boarding API.

You need to make sure that all data pieces of the to-be-submitted MPA are present in the

XML file and they being put together complies with the all the implemented business

validation and field validation rules.

**INPUT:**

XML of which MPA data pass all business validations and field validations

**OUTPUT:** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

Omaha Boarding Specification.docx

Page 71 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<ASRefId xmlns="http://tempuri.org/">5889</ASRefId>

<Timestamp xmlns="http://tempuri.org/">10/14/2015 11:45:46

AM</Timestamp>

<Status xmlns="http://tempuri.org/">SUCCESS</Status>

<Errors xmlns="http://tempuri.org/" />

</SubmitMPAResult>

**NOTES:**

**2.**

**Field Input Validation**

**TEST CASE:**

Failed submission due to failed validation of field input rule(s)

**SUMMARY:**

Each XML tag (MPA input field) has its own input rule, with regard to input type (text,

number, boolean), input legnth, and input range (min value, max value).

Example: For XML tag NumberOfLocation, you are only allowed to enter a number within the

range from 1 to 99.

**INPUT:**

XML containing a field specified with a value that violates the field’s input rule

which decides data type, length, or range

**OUTPUT:** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">10/14/2015 11:58:59

AM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

Omaha Boarding Specification.docx

Page 72 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ErrorDescription>The 'NumberOfLocation' element is invalid - The value

'100' is invalid according to its datatype 'Int' - The MaxInclusive constraint

failed.</ErrorDescription>

<LineNumber>11</LineNumber>

<ColumnNumber>26</ColumnNumber>

</MerchantError>

</Errors>

</SubmitMPAResult>

**NOTES:**

It is not necessary verify each and every XML tag so to save time there is another

shorter approach to this: verification of field input rules can be performed on the

Omaha Boarding API schema file instead of the Omaha Boarding API itself.

The reason this is possible is all the field input validation rules are implemented

only in Omaha Boarding API schema.

**3.**

**Faulty Data Validation**

**TEST CASE:**

Failed submission due to MPA containing faulty or non-existent data

**SUMMARY:**

For seletable MPA fields with values subject to changes like SYS or SYSPRIN (from here onward

regarded as **dynamic selectable fields**), Omaha Boarding Web has a way to limit user inputs

down to a number of currently available values. The result of that is user cannot enter values

not among the allowed selectable values.

Omaha Boarding Specification.docx

Page 73 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Omaha Boarding API uses a different way to prevent faulty data from entering through the API

tool. You are responsible for testing whether Omaha Boarding API is functioning correctly in

that regard.

MPA that contains faulty data, e.g. a non-existent SYS number

**INPUT:**

**OUTPUT:** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">10/14/2015 09:25:17 PM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>Outlet 01: MPA Info - The Prin Number is not

assigned.</ErrorDescription>

</MerchantError>

<MerchantError>

<ErrorId>2</ErrorId>

<ErrorDescription>Outlet 01: MPA Info - The Agent Number is not

assigned.</ErrorDescription>

</MerchantError>

Omaha Boarding Specification.docx

Page 74 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





</Errors>

</SubmitMPAResult>

**NOTES:**

One more advanced (and low-level) test case can be derived from this one is: Failed

submission due to specified SYS or specified PRIN does not belong to

WHOLESALE/RETAIL client.

Example: SYSPRIN 8740/3801 belongs to a WHOLESALE client. If you submit an XML

for RETAIL MPA with the following information:

<MpaInfo>

<MpaMerchantType>S</MpaMerchantType>

<ClientType>RETAIL</ClientType>

<SystemNumber>8740</SystemNumber>

<PrinNumber>3801</PrinNumber>

<Agent>0100</Agent>

<SalesID>1111</SalesID>

<ClientDbaName>API TEST APP AMEX #1 INC.</ClientDbaName>

<NumberOfLocation>1</NumberOfLocation>

<TemplateID xsi:nil="true" />

<TemplateVersion xsi:nil="true" />

</MpaInfo>

You will receive the following response from Omaha Boarding API:

<SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">10/14/2015 09:42:11 PM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>Outlet 01: MPA Info - The Prin Number is not

assigned.</ErrorDescription>

</MerchantError>

</Errors>

</SubmitMPAResult>

**4.**

**Input Data Validity**

Omaha Boarding Specification.docx

Page 75 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**TEST CASE:**

Failed submission due to MPA containing invalid data, i.e. not within the list of pre-defined

values

**SUMMARY:**

There are certain XML tags whose input values must fall into a pre-defined list. From here

onward these will be refered to as **“static selectable fields”.**

Example: XML tag BusinessType can only have one of the following values:

1

Sole Proprietorship

10

11

2

Publicly Traded Partnership

Publicly Traded Limited Liability Company

Private Partnership

3

Private Corp

4

Public Corp

5

Association/Estate/Trust

Tax Exempt Organization

Private Limited Liability Company

International/Organization

Government

6

7

8

9

**INPUT:**

MPA XML with at least one tag with specified value that lies outside the pre-

defined list of allowed values.

**OUTPUT:** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">10/14/2015 10:12:32

PM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

Omaha Boarding Specification.docx

Page 76 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ErrorDescription>The 'State' element is invalid - The value 'TT' is invalid

according to its datatype 'String' - The Enumeration constraint

failed.</ErrorDescription>

<LineNumber>20</LineNumber>

<ColumnNumber>14</ColumnNumber>

</MerchantError>

<MerchantError>

<ErrorId>2</ErrorId>

<ErrorDescription>The 'BusinessType' element is invalid - The value '0' is

invalid according to its datatype 'String' - The Enumeration constraint

failed.</ErrorDescription>

<LineNumber>28</LineNumber>

<ColumnNumber>20</ColumnNumber>

</MerchantError>

</Errors>

</SubmitMPAResult>

**NOTES:**

Changes have been, and might be made to the pre-defined lists of static

selectable values as required by future change requests.

**5.**

**Business Validation**

**TEST CASE:**

Failed submission due to information supplied within MPA does not comply with one or more

business validation rule

**SUMMARY:**

Many business validation rules are applied to the MPA submission process to preserve data

integrity, which will mean a successful VAPP transmission.

For instance, at present we have a busines rule that does not allow certain SIC codes to be

selected when AMEX Opt Blue is chosen.

**INPUT:**

MPA XML with at least one XML tag with data entered in such a way that at least

one business validation rule is violated.

**OUTPUT:** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

Omaha Boarding Specification.docx

Page 77 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">10/15/2015 01:36:45

AM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>Location 01: Other Entitlements - American Express option

can only be selected under eligible SIC Codes if the Annual American Express

Sales Volume is less than $1,000,000.</ErrorDescription>

</MerchantError>

</Errors>

</SubmitMPAResult>

**NOTES:**

The Omaha Boarding API SRS can be used as a reference for business rules

currently in place for Omaha Boarding.

Omaha Boarding API and Omaha Boarding Web should have the same set of

business validation rules

**6.**

**Wholesale versus Retail**

**TEST CASE:**

Failed submission due to information supplied not being compatible with chosen Client type

**SUMMARY:**

Omaha Wholesale Clients and Omaha Retail Clients have a lot of MPA data fields in common.

However there are some MPA fields which are exclusive to only one Client Type.

**INPUT:**

MPA XML with a specified MPA field that does not belong with the selected

Client type (specified via XML tag ClientType)

**OUTPUT:** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">10/15/2015 01:48:07

AM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

Omaha Boarding Specification.docx

Page 78 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>Outlet 01: Business Info - The Assessment Code cannot be

display for MPA RETAIL.</ErrorDescription>

</MerchantError>

</Errors>

</SubmitMPAResult>

**NOTES:**

None

**7.**

**Multi-Location versus Single-Location**

**TEST CASE:**

Submission of XML of merchant with more than one outlets

**SUMMARY:**

One single MPA can contain up to 99 outlets. It is important that all functionalities and

features offered by Omaha Boarding API still work as intended when more than one outlets

are included in submitted MPAs

**INPUT:**

MPA XML with more than one outlet

**OUTPUT:** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">10/15/2015 01:48:07

AM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>Outlet 01: Business Info - The Assessment Code cannot be

display for MPA RETAIL.</ErrorDescription>

</MerchantError>

</Errors>

</SubmitMPAResult>

Omaha Boarding Specification.docx

Page 79 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**NOTES:**

Please notice that each error descripition is preceded by Outlet NN in which NN

is the ordial number of the outlet corresponding to the error.

**8.**

**MPA Fields Inter-Dependencies**

**TEST CASE:**

Failed submisison due to incompatible MPA data

**SUMMARY:**

There are a number of input rules applied on MPA data fields to make sure VAPP tramission is

successful.

For Omaha Boarding Web, those rules are reflected by the JavaScript-coded Show/Hide

mechanism which makes certain fields available for inputting only when special conditions are

met, e.g. a checkbox is checked off.

Example: AMEX Volume is available only when AMEX Entitlement and AMEX is selected.

**INPUT:**

MPA XML with at least one XML tag incompatible with currently available selecions

**OUTPUT:** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">10/15/2015 02:53:03 AM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

Omaha Boarding Specification.docx

Page 80 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ErrorDescription>Location 01: Other Entitlements - Other Volume % is not

compatible with entered AmexOption</ErrorDescription>

</MerchantError>

</Errors>

</SubmitMPAResult>

**NOTES:**

None

**9.**

**Conditional Data Validation**

**TEST CASE:**

Failed submission due to incorrect MPA data combinations

**SUMMARY:**

The following is true for some static selectable fields:

Under certain circumstances, which values available to an XML tag can be determined by the

value selected for another XML tag. It is imperative that MPAs with incorrect combined data

must not be allowed to go through Omaha Boarding API.

Example: The equipment Fiserv FD 55 can only be deloyed by ISO, it cannot be purchased or

leased. So when that equipment is selected, billing method must be none other than ‘ISO

Deployed’.

**INPUT:**

MPA XML with wrong combination of input data

**OUTPUT:** <SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">10/15/2015 03:02:46

AM</Timestamp>

<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/">

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>Location 01: Other Entitlements - Other Volume % is not

compatible with entered AmexOption</ErrorDescription>

</MerchantError>

<MerchantError>

Omaha Boarding Specification.docx

Page 81 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<ErrorId>2</ErrorId>

<ErrorDescription>Outlet 01: Equipment and FE - 'Fiserv FD 55' cannot be

selected with the Billing Method 'Purchase'/'Lease 12 Months'/'Lease 24

Months'/'Lease 36 Months'/'Lease 48 Months'.</ErrorDescription>

</MerchantError>

</Errors>

</SubmitMPAResult>

**NOTES:**

None

**6.2 COMMON ISSUES**

**6.2.1 XML response**

After an XML file is submitted, Omaha Boarding API returns XML responses which are structured

as follows:

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

<ErrorId>1</ErrorId>

<ErrorDescription></ErrorDescription>

<LineNumber/>

<ColumnNumber/>

</MerchantError>

Omaha Boarding Specification.docx

Page 82 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





</Errors>

</SubmitMPAResult>

</SubmitMPAResponse>

ExternalRefId: It will hold the external Ref Id received from Client.

ASRefId: It will hold the MPA ID generated from Fiserv Boarding system in case of success. It will

be blank in case of failure.

Timestamp: The date time stamp of success or failure of the submission.

Status: if the MPA XML Content passes the validation, it will be SUCCESS. Otherwise, it will be

FAILURE.

Errors: It will hold the MerchantError tags – Only applicable if the MPA XML Content fails against

the validation.

MerchantError: It will contain multiple errors received while XSD validation as well as error that

relates to MPA edits of boarding merchant.

•

•

•

•

ErrorId: it will hold the Error #.

ErrorDescription: It will hold the description of merchant error.

LineNumber: it will hold the Error Line #. It could be sent as empty tag.

ColumnNumber: it will hold the Error Column #. It could be sent as empty tag.

**6.2.1 Generic Error Message**

There will be times when the XML response does not provide any useful information regarding

what results in submission failure.

Generic Failure Message Response Sample XML

<SubmitMPAResponse>

<SubmitMPAResult>

<ExternalRefId>234567890</ExternalRefId>

<ASRefId>234</ASRefId>

<Timestamp>2014-09-30 00:00:00.000</Timestamp>

<Status>FAILURE</Status>

</SubmitMPAResult>

</SubmitMPAResponse>

There are a lot of possible reasons to this highly undesirable scenario and the best action to take

is having a look at the API log file API\_Log.txt yourself or asking for assistance from involved

parties.

Note: API\_Log.txt contains more detailed information and might help a lot in identifying the

cause of the submission failure.

**6.2.1 Specific Error Message**

Omaha Boarding Specification.docx

Page 83 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





In scenarios where specific error messages are included in the XML response, just follow the

instructions, together with related documents to get the errors sorted. The error messages

should provide information as to what is determined to be invalid or not allowed.

**6.3 POST MPA SUBMISSION CHECKS**

Post-submission checks can only be performed after a successful submission.

Note: ASRefId is needed for these checks.

**6.4 FRONT-END DATA**

All MPAs submitted via Omaha Boarding API can be viewed or modified on Omaha Boarding

Web providing that:

·

·

·

MPAs of type API-STD are configured to be routed to Client Approval stage after submission

Approval Group settings are correct and already in place

Approver credential is needed to access AccessOne > One Stop > Client Approval Queue

**6.5 STORED DATA**

It is important to know that more than 90% of the Omaha XML tags have a corresponding

column under boarding database tables. These column names are identical to the XML tag

names. The retrieve MPA webservice call which is detailed in section 6.3 allows you to retrieve

the field values in order to perform field validations on each of the sections.

MPA Page

MPA Info

CORPORATE INFO

OWNERSHIP

SIGNATURE

DB Table(s)

Boarding\_MPAInformation

Boarding\_MPACorporateInformation

Boarding\_MPAOwnership

Boarding\_MPASignature

Boarding\_MPASignature\_Image

Boarding\_MPABusinessInformation

Boarding\_MPASiteInformation

Boarding\_MPAMOTOBBInternet

Boarding\_MPASettlement

Boarding\_MPAProcessing

Boarding\_MPATransaction

Boarding\_MPAPricing

BUSINESS INFO

SITE INFO

MOTO/NN/INTERNET

SETTLEMENT

PROCESSING

TRANSACTIONS

PRICING

Boarding\_MPAPricingDetail

Boarding\_MPAEntitlement

Boarding\_MPAOtherFees

Boarding\_MPAOtherFeesCards

Boarding\_MPAClientExpense

OTHER ENTITLEMENTS

OTHER FEES

CLIENT EXPENSE

Omaha Boarding Specification.docx

Page 84 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





EXCEPTIONS

EQUIPMENT AND FE

Boarding\_MPAExceptions

Boarding\_MPAEquipmentFE

Boarding\_MPAEquipmentFE\_Clover

Boarding\_MPAEquipmentFE\_FirstDeploy

**6.6 EXPORTED PDFS**

Data displayed on exported PDFs should be compared to the data specified in the submitted

XML tags to be certain of correctness, taking into consideration all alterations that have been

made to original submitted data.

Note: In order for this review to be completed, please work with your API product owner in

order for them to be pulled and provided to you from the test region.

**7 SOAP Request Guide**

**7.1 PREREQUISITE CHECKS**

The following conditions must be met before any connectivity verification can be carried out;

·

·

IP Whitelisting process has been completed.

Necessary user set-ups have been completed and the person submitting requests to Omaha SOAP

API has the correct credentials.

·

A working version of SOAP UI has been installed in advance.

**7.2 CONFIGURING SOAP UI**

Several important settings must be in place to secure a successful connection to the Omaha

Boarding SOAP API.

As per security purpose, TLS 1.0 is disabled and client should use TLS 1.2, The following

code is used for C# program where it should be set before making call to the Boarding API.

**C#**

ServicePointManager.SecurityProtocol = SecurityProtocolType.Tls |

SecurityProtocolType.Tls11 | SecurityProtocolType.Tls12;

If you are using SoapUI for testing, below changes should be made to make it work.

The client will want to add the following parameter to their Soap UI

**PATH**: ..\Program Files\SmartBear\SoapUI-5.3.0\bin\SoapUI-5.3.0.vmoptions

Edit VMOptions.txt file in their Soap UI > '**-Dsoapui.https.protocols=TLSv1.2**'

Omaha Boarding Specification.docx

Page 85 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**7.3 Initiate SOAP Project Workspace**

A new window will open prompting for entering Project Name and Initial WSDL;

Project Name: Enter a desired project name

Initial WSDL: [https://lsuat-](https://lsuat-api.fdportfoliomanager.com/boarding/omaha/AsBoardingAPIService.svc?wsdl)

[api.fdportfoliomanager.com/boarding/omaha/AsBoardingAPIService.svc?wsdl](https://lsuat-api.fdportfoliomanager.com/boarding/omaha/AsBoardingAPIService.svc?wsdl)

Click OK

·

·

In a few seconds or less the newly created SOAP project will be loaded with all the presentable

components of the Boarding API.

A successful load will be indicated by no error and the web service’s components being displayed on

the Navigator panel. An example is shown in the following screenshot:

Omaha Boarding Specification.docx

Page 86 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





It can also be seen from the above screenshot that the Omaha API web service is composed

of three separate web methods that will function together as a whole:

·

·

·

Submit MPA: used for submitting Omaha MPAs

Retrieve MPA: used for retrieving all MPA-oriented details of submitted Omaha MPAs

Get status by timespan: used for retrieving the states and statuses of submitted Omaha MPAs within

a limited time frame that span 168 hours

**7.4 Set up Security and Authentication**

Enable Project View by double-clicking on the SOAP project’s name or right-clicking the name

and then selecting Show Project View

Omaha Boarding Specification.docx

Page 87 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





A new window will appear where additional settings can be configured for the SOAP project.

As the communication with the Boarding API is done via SOAP calls, it is mandatory that all

the calls from SOAP client side contain a security header with sufficient and precise

information to guarantee a successful authentication with the Boarding API web service.

Omaha Boarding Specification.docx

Page 88 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Navigate to WS-Security Configurations tab to specify the credentials with which the SOAP

requests will be authenticated by. Note: Fiserv is responsible for providing the working

credentials.

·

Then select the tab Outgoing WS-Security Configurations. It should be the default sub-tab of the WS-

Security Configurations one.

·

Click on the

icon to create a new Outgoing WS-Security Configuration. Enter a name as desired

then click OK.

Omaha Boarding Specification.docx

Page 89 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Click on the

below to add a WSS entry for the new WSS configuration. The entry will home

the username and password provide by FD. In the opened pop-up Add WSS Entry, select entry

type Username and hit OK.

Omaha Boarding Specification.docx

Page 90 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Enter username and password as necessary and make sure:

·

·

·

Add Nonce field: checked off

Add Created field: checked off

Password Type: PasswordDigest Ext

Omaha Boarding Specification.docx

Page 91 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**7.5 Start SOAP Request Submission**

As the preparations are all completed now, it is time SOAP calls can be made to the Omaha

SOAP API to verify the connection, as well as the functionalities.

**8 SUBMITTING SOAP REQUESTS**

Omaha Boarding Specification.docx

Page 92 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**8.1 Web method SubmitMPA**

\1. Use the auto-generated SOAP request (Request 1) or right-click on SubmitMPA > Select

New Request

Double-click on Request 1 to modify the content as appropriate before sending it to Omaha

SOAP API.

Note: The added or updated content will go into the left panel of the SOAP request.

\2. Add security information to the SOAP request header for authentication purpose

·

Right-click on the SOAP request content and select Outgoing WSS > Apply [Name of the Outgoing WS-

Security Configuration]

Note: The outgoing WSS configuration must be applied every time before SOAP request is

sent to Boarding API.

Omaha Boarding Specification.docx

Page 93 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





\3. Add the merchant application to the SOAP request body for the obvious purpose of MPA

submission

·

Copy a valid merchant application in the form of XML and paste the whole content between these two

tags: <tem:xmlContent> and </tem:xmlContent>

\4. Hit the

icon to submit the SOAP request to Omaha API

·

·

The Omaha SOAP API web service will acknowledge the request by sending back a SOAP response

which will then show on the panel to the right of the request (Request 1 in the example).

The response will vary mainly depending on the supplied merchant application. However for most of

the time a successful submission will be indicated by these two most basic SOAP responses as follows:

Omaha Boarding Specification.docx

Page 94 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Note: This document does not discuss in details failed MPA submissions that are caused by the

provided data of the merchant application. The goal is to make sure the connection to Omaha Boarding

API is established successfully.

·

A successful submission

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

[<s:Body](http://www.w3.org/2001/XMLSchema-instance)[ ](http://www.w3.org/2001/XMLSchema-instance)[xmlns:xsi=](http://www.w3.org/2001/XMLSchema-instance)<http://www.w3.org/2001/XMLSchema-instance>

xmlns:xsd="http://www.w3.org/2001/XMLSchema">

<SubmitMPAResponse xmlns="http://tempuri.org/">

<SubmitMPAResult>

<ExternalRefId>?</ExternalRefId>

<ASRefId>3458</ASRefId>

<Timestamp>02/15/2016 01:50:20 PM</Timestamp>

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

<Timestamp>02/15/2016 02:10:08 PM</Timestamp>

<Status>FAILURE</Status>

<Errors>

<MerchantError>

<ErrorId>1</ErrorId>

<ErrorDescription>Location 01: MPA Info - The Agent Number is not

assigned.</ErrorDescription>

</MerchantError>

</Errors>

</SubmitMPAResult>

</SubmitMPAResponse>

</s:Body>

</s:Envelope>

**8.2**

**SOAP Request Format**

<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"

xmlns:tem="http://tempuri.org/">

<soapenv:Header>

<wsse:Security xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-

wssecurity-secext-1.0.xsd" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-

wssecurity-utility-1.0.xsd">

<wsse:UsernameToken wsu:Id="UsernameToken-699F92A9FFDD6BF4E714555674985404">

<wsse:Username>fdtstapi01</wsse:Username>

<wsse:Password Type="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-username-

token-profile-1.0#PasswordDigest">JCML1FkfdEIkIVbaid3ec7RvR+I=</wsse:Password>

Omaha Boarding Specification.docx

Page 95 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<wsse:Nonce EncodingType="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-soap-

message-security-1.0#Base64Binary">L2LlWQX92/Fqd+N4nQW4+Q==</wsse:Nonce>

<wsu:Created>2016-02-15T20:18:18.539Z</wsu:Created>

</wsse:UsernameToken>

</wsse:Security>

</soapenv:Header>

<soapenv:Body>

<tem:SubmitMPA>

<!--Optional:-->

<tem:xmlContent>

<ApplicationInformation>

<MpaInfo></MpaInfo>

<CorporateInfo></CorporateInfo>

<Ownership></Ownership>

<Signature></Signature>

<MpaOutletInfo>

<Outlet>

<BusinessInfo></BusinessInfo>

<SiteInfo></SiteInfo>

<MotoBBInet></MotoBBInet>

<Settlement></Settlement>

<Processing></Processing>

<Transaction></Transaction>

<Pricing></Pricing>

<Entitlement></Entitlement>

<EquipmentFE></EquipmentFE>

<OtherFees></OtherFees>

<ClientExpense xsi:nil="true" xmlns:xsi="http://www.w3.org/2001/XMLSchema-

instance"/>

<Exception xsi:nil="true" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>

</Outlet>

</MpaOutletInfo>

</ApplicationInformation>

</tem:xmlContent>

<!--Optional:-->

<tem:extRefID>?</tem:extRefID>

</tem:SubmitMPA>

</soapenv:Body>

</soapenv:Envelope>

**8.3 Web method RetrieveMPAXML**

Repeat 1 and 2 from 3.1.1.

Specify the MPA ID that was returned by Omaha Boarding API as a result of any successful

submission (See ASRefId in section 3.1.2)

MPA ID must be placed between the following two tags: <tem:mpaId> and </tem:mpaId>

An indicator to the acknowledgement of the web service for the SOAP request is also a

response form Omaha Boarding SOAP API web service. The response will contain all the

details of the corresponding submitted MPA, as in the example below: (application data

have been removed for simple presentation)

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

Omaha Boarding Specification.docx

Page 96 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

xmlns:xsd="http://www.w3.org/2001/XMLSchema">

<RetrieveMpaXmlResponse xmlns="http://tempuri.org/">

<RetrieveMpaXmlResult>

<ApplicationInformation xmlns=""></ApplicationInformation>

</RetrieveMpaXmlResult>

</RetrieveMpaXmlResponse>

</s:Body>

</s:Envelope>

**8.4**

**SOAP Request Format**

<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"

xmlns:tem="http://tempuri.org/">

<soapenv:Header>

<wsse:Security xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-

wss-wssecurity-secext-1.0.xsd" xmlns:wsu="http://docs.oasis-

open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">

<wsse:UsernameToken wsu:Id="UsernameToken-699F92A9FFDD6BF4E714555691132817">

<wsse:Username>fdtstapi01</wsse:Username>

<wsse:Password Type="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-

username-token-profile-

1.0#PasswordDigest">MnJboSZ4qzrkOef77DLM6Ey2CV4=</wsse:Password>

<wsse:Nonce EncodingType="http://docs.oasis-open.org/wss/2004/01/oasis-

200401-wss-soap-message-security-

1.0#Base64Binary">ZpcV0Lzok+0OSv8ZFl1v9A==</wsse:Nonce>

<wsu:Created>2016-02-15T20:45:13.281Z</wsu:Created>

</wsse:UsernameToken>

</wsse:Security>

</soapenv:Header>

<soapenv:Body>

<tem:RetrieveMpaXml>

<tem:mpaId>3458</tem:mpaId>

<!--Optional:-->

<tem:extRefID>?</tem:extRefID>

</tem:RetrieveMpaXml>

</soapenv:Body>

</soapenv:Envelope>

**8.5 Web method GetStatusByTimeSpan**

Repeat 1 and 2 from 3.1.1.

Enter values for the two xml elements as required. Omaha API will base on the supplied

values to return all the MPA status changes that happen in between the selected period.

·

·

<tem:fromTimeStamp>?</tem:fromTimeStamp>

<tem:toTimeStamp>?</tem:toTimeStamp>

Note:

·

·

For fromTimeStamp, the value must not be more than 168 hours earlier than the current date time.

The values passed to Omaha API must follow the exact format: YYYY-MM-DD HH:MM:SS [AM|PM]

Omaha Boarding Specification.docx

Page 97 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





Example: 2016-02-15 3:45:02 AM or 2016-02-15 9:44:02 PM

toTimeStamp must be later than fromTimeStamp

·

A successful call to Omaha API web service will be indicated by a successful response as

shown in the exmplae below:

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

<s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"

xmlns:xsd="http://www.w3.org/2001/XMLSchema">

<GetStatusByTimeSpanResponse xmlns="http://tempuri.org/">

<GetStatusByTimeSpanResult>

<GetStatusByTimeSpanResult>

<MerchantApplicationStatus>

<ASRefId>3456</ASRefId>

<FDMerchantNumber/>

<Status>

<MerchantDetails>

<OmahaNumber/>

<LocationNumber>1</LocationNumber>

<DBAName>NASHVILLE cardnet api test</DBAName>

<CardnetNumber/>

<MerchantStatus>

<AppStatus>

<Code>MPAKey</Code>

<Information>In Process</Information>

<Timestamp>2/15/2016 1:48:43 PM</Timestamp>

</AppStatus>

<AppStatus>

<Code>MPA</Code>

<Information>In Process</Information>

<Timestamp>2/15/2016 1:48:43 PM</Timestamp>

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

**8.6**

**SOAP Request Format**

<soapenv:Envelope xmlns:soapenv="http://schemas.xmlsoap.org/soap/envelope/"

xmlns:tem="http://tempuri.org/">

<soapenv:Header>

<wsse:Security xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-

wss-wssecurity-secext-1.0.xsd" xmlns:wsu="http://docs.oasis-

open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">

<wsse:UsernameToken wsu:Id="UsernameToken-699F92A9FFDD6BF4E7145557039343214">

<wsse:Username>fdtstapi01</wsse:Username>

Omaha Boarding Specification.docx

Page 98 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<wsse:Password Type="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-

username-token-profile-

1.0#PasswordDigest">UAIRC4MQSbdv0TpTYfxCEpUfxlg=</wsse:Password>

<wsse:Nonce EncodingType="http://docs.oasis-open.org/wss/2004/01/oasis-

200401-wss-soap-message-security-

1.0#Base64Binary">G2l16Lva2YMnIficPnOv/g==</wsse:Nonce>

<wsu:Created>2016-02-15T21:06:33.432Z</wsu:Created>

</wsse:UsernameToken>

</wsse:Security>

</soapenv:Header>

<soapenv:Body>

<tem:GetStatusByTimeSpan>

<!--Optional:-->

<tem:fromTimeStamp>2016-02-15 1:45:02 PM</tem:fromTimeStamp>

<!--Optional:-->

<tem:toTimeStamp>2016-02-15 1:49:02 PM</tem:toTimeStamp>

</tem:GetStatusByTimeSpan>

</soapenv:Body>

</soapenv:Envelope>

**11 CONNECTIVITY VERIFICATION VIA AN EXTERNAL TOOL**

As it is understood that web service calls actually are made from outside of the SOAP UI tool,

once the connectivity testing with the SOAP UI tool is completed, one can go ahead with

verifying the Omaha Boarding SOAP API using another internal tool other than the SOAP UI

one.

Fiserv must be informed of the result of connectivity tests with Omaha Boarding API using

the SOAP UI tool. This will help Fiserv stay up-to-date with the latest progress of partners and

will also expedite the troubleshooting/support process in case there is any technical difficulty

or issue involved.

This section provides additional information about how SOAP requests to Omaha Boarding

API should be constructed with an aim to assist with the generation of valid SOAP requests

from Fiserv partners.

Omaha Boarding SOAP API was designed to understand many different formats of SOAP

requests. However to be considered valid by the web service, SOAP requests must meet

defined minimum structural requirements to guarantee a successful integration with Omaha

Boarding SOAP API. More details are available in:

·

·

Section 1: SOAP request header

Section 2: SOAP request body

The link to Omaha Boarding SOAP API in UAT is:

<https://lsuat-api.fdportfoliomanager.com/boarding/omaha/AsBoardingAPIService.svc>

**12 SOAP REQUEST HEADER**

Omaha Boarding Specification.docx

Page 99 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**12.1 SOAP Header Structure**

The process to generate a valid SOAP can be in a general sense described as having the steps

below:

\1. Generate a random nonce value

\2. Get current local date time in UTC format

\3. Get username token (plain-text) from Fiserv

\4. Get password token (plain-text) from Fiserv

\5. Combine nonce value (plain-text) + created date (UTC) + password token (plain-text) to form a string.

Apply SHA-1 encryption on the string. The encryption result is then converted to base-64 string format

to obtain the password digest.

\6. Send to Omaha API

·

·

·

·

username token (plain-text)

password digest (encrypted)

nonce value (in base-64 string format)

created date time (UTC)

Header of SOAP requests to Omaha Boarding API is always required contains a <wsse:

UsernameToken> element of which XML Structure can be illustrated as:

<wsse:UsernameToken>

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

A new unique nonce value should be generated every single time a request is sent to

Omaha SOAP API for optimal security. Please be advised that this is only optional and

Omaha SOAP API does not require that or check whether the received nonce value is

unique or not.

Example:

Clear-text nonce = 1453220513715 → Encoded nonce = MTQ1MzIyMDUxMzcxNQ==

**<wsu:Created> Creation time of the SOAP request**

This element specifies the timestamp when the SOAP request is generated.

The value can be obtained by converting the current local date time to Coordinated

Universal Time (UTC).

Example: 2/16/2016 10:09 AM (EST) → 2016-02-16T16:09:54.790Z (UTC)

Omaha Boarding Specification.docx

Page 100 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**<wsse:Username> Plain text userid (API user)**

Userid is provided by Fiserv.

**<wsse:Password> Hashed value of password of wsse:Username**

This element has attribute Type which is used for specifying the password type being

provided. It should always be #PasswordDigest.

How the value for this element is generated can be described by the following pseudo-

code:

Password\_Digest = Base64 (SHA-1 (nonce + created + password))

The generated nonce (clear-text value, not the encrypted one sent in SOAP header),

creation timestamp, and the password (clear-text password) are concatenated into a

combination. The combination is digested using the SHA-1 hash algorithm. The digest

result is then encoded in Based64 encoding format and the final password digest value is

produced.

Example: The table below details how digest password can be computed.

**Field**

**Clear-text value**

**Operation**

**Sent value**

Password S7O0g2w7Q9

token

Concatenate Do not send

Nonce

Created

Nonce +

1453220513715

2016-01-14T10:15:19.143Z

14532205137152016-01-

Concatenate MTQ1MzIyMDUxMzcxNQ==

Concatenate 2016-01-14T10:15:19.143Z

SHA1 and

J93nsDIrtANaR39AVLRboICHhGM=

Created + 14T10:15:19.143ZS7O0g2w7Q9 then Base64

Password

A valid SOAP request header with the above values would appear as follows;

<soapenv:Header>

<wsse:Security xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-

wss-wssecurity-secext-1.0.xsd" xmlns:wsu="http://docs.oasis-

open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">

<wsse:UsernameToken>

<wsse:Username>omahaapitest</wsse:Username>

<wsse:Password Type="http://docs.oasis-open.org/wss/2004/01/oasis-200401-

wss-username-token-profile-

1.0#PasswordDigest">Dryu39kzetVb5mQO9JpKxShGH6k=</wsse:Password>

<wsse:Nonce EncodingType="http://docs.oasis-open.org/wss/2004/01/oasis-

200401-wss-soap-message-security-

1.0#Base64Binary">MTQ1MzIyMDUxMzcxNQ==</wsse:Nonce>

<wsu:Created>2016-01-14T10:15:19.143Z</wsu:Created>

</wsse:UsernameToken>

</wsse:Security>

</soapenv:Header>

Or as follows, without the attribute EncodingType of element wsse:Nonce;

Omaha Boarding Specification.docx

Page 101 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<soapenv:Header>

<wsse:Security xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-

wss-wssecurity-secext-1.0.xsd" xmlns:wsu="http://docs.oasis-

open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">

<wsse:UsernameToken>

<wsse:Username>omahaapitest</wsse:Username>

<wsse:Password Type="http://docs.oasis-open.org/wss/2004/01/oasis-200401-

wss-username-token-profile-

1.0#PasswordDigest">Dryu39kzetVb5mQO9JpKxShGH6k=</wsse:Password>

<wsse:Nonce>MTQ1MzIyMDUxMzcxNQ==</wsse:Nonce>

<wsu:Created>2016-01-14T10:15:19.143Z</wsu:Created>

</wsse:UsernameToken>

</wsse:Security>

</soapenv:Header>

Note: Compared to the SOAP header auto-generated by SOAP UI, an SOAP header can leave

out

the

attribute

**wsu:**

**Id**,

e.g.

wsu:

Id="UsernameToken-

699F92A9FFDD6BF4E7145557039343214" and still be fully understood by Omaha API.

**12.2 SOAP Header Example**

<soapenv:Header>

<wsse:Security xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-

wssecurity-secext-1.0.xsd" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-

200401-wss-wssecurity-utility-1.0.xsd">

<wsse:UsernameToken>

<wsse:Username>omahaapitest</wsse:Username>

<wsse:Password Type="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-

username-token-profile-

1.0#PasswordDigest">Dryu39kzetVb5mQO9JpKxShGH6k=</wsse:Password>

<wsse:Nonce>MTQ1MzIyMDUxMzcxNQ==</wsse:Nonce>

<wsu:Created>2016-01-14T10:15:19.143Z</wsu:Created>

</wsse:UsernameToken>

</wsse:Security>

</soapenv:Header>

**13 SOAP REQUEST BODY**

**13.1 SOAP Body Structure**

How the SOAP request body is constructed is based on which among the three currently

available web methods is called.

**13.1.1 Web method SubmitMPA**

·

·

The customized contents are highlighted.

Fiserv is responsible for providing the sample MPA XML contents.

<soapenv:Body>

Omaha Boarding Specification.docx

Page 102 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<tem:SubmitMPA>

<!--Optional:-->

<tem:xmlContent>

<!--MPA content to be entered here !-->

</tem:xmlContent>

<!--Optional:-->

<tem:extRefID>?</tem:extRefID>

</tem:SubmitMPA>

</soapenv:Body>

**13.1.1 Web method RetrieveMPAXML**

·

·

The customized contents are highlighted.

MPAID must be passed as an input parameter. It can be referenced from the output of a

successful submission to web method SubmitMPA as the ASRefId.

<soapenv:Body>

<tem:RetrieveMpaXml>

<tem:mpaId>3458</tem:mpaId>

<!--Optional:-->

<tem:extRefID>?</tem:extRefID>

</tem:RetrieveMpaXml>

</soapenv:Body>

**13.1.1 Web method GetStatusByTimeSpan**

·

·

Highlighted in yellows are customized inputs.

Unless the inputs are in correct format (YYYY-MM-DD HH:MM:SS [AM|PM])

<soapenv:Body>

<tem:GetStatusByTimeSpan>

<tem:fromTimeStamp>2016-02-15 1:45:02 PM</tem:fromTimeStamp>

<tem:toTimeStamp>2016-02-15 1:49:02 PM</tem:toTimeStamp>

</tem:GetStatusByTimeSpan>

</soapenv:Body>

**13.2 SOAP Body Example**

Please note the actual content of merchant application starting with

<ApplicationInformation> and ending with </ApplicationInformation> will be much longer

than the trimmed data in the content below.

Omaha Boarding Specification.docx

Page 103 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





**13.2.1 Web method SubmitMPA**

<soapenv:Body>

<tem:SubmitMPA>

<!--Optional:-->

<tem:xmlContent>

<ApplicationInformation>

<MpaInfo>

<MpaMerchantType>S</MpaMerchantType>

<ClientType>RETAIL</ClientType>

<SystemNumber>8740</SystemNumber>

<PrinNumber>9900</PrinNumber>

<Agent>0000</Agent>

<SalesID>0080</SalesID>

<ClientDbaName>NASHVILLE cardnet api test</ClientDbaName>

<NumberOfLocation>1</NumberOfLocation>

<TemplateID xsi:nil="true"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>

<TemplateVersion xsi:nil="true"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>

</MpaInfo>

<CorporateInfo>

</Outlet>

</MpaOutletInfo>

</ApplicationInformation>

</tem:xmlContent>

<!--Optional:-->

<tem:extRefID>?</tem:extRefID>

</tem:SubmitMPA>

</soapenv:Body>

**13.2.1 Web method RetrieveMPAXML**

<soapenv:Body>

<tem:RetrieveMpaXml>

<tem:mpaId>3458</tem:mpaId>

<tem:extRefID />

</tem:RetrieveMpaXml>

</soapenv:Body>

**13.2.1 Web method GetStatusByTimeSpan**

<soapenv:Body>

<tem:GetStatusByTimeSpan>

<tem:fromTimeStamp>2016-02-15 1:45:02 PM</tem:fromTimeStamp>

Omaha Boarding Specification.docx

Page 104 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<tem:toTimeStamp>2016-02-15 1:49:02 PM</tem:toTimeStamp>

</tem:GetStatusByTimeSpan>

</soapenv:Body>

**12 COMMON ISSUE #1: GENERIC ERROR**

**12.1.1**

**Indicator**

A response as seen below is returned by Omaha API after the submission of a request;

<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">

<s:Body>

<s:Fault>

<faultcode>s:Client</faultcode>

<faultstring xml:lang="en-US">Generic error

occurred.</faultstring>

</s:Fault>

</s:Body>

</s:Envelope>

**12.1.1**

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

sent. A large delay would cause Omaha API to consider the provided wsu:Created expired.

**12.1.1**

**Actions**

\1. Double-check username and password

\2. Log a request for issue investigation to Fiserv. The request must detail:

·

·

When the SOAP request was submitted

The submitting username

**13 COMMON ISSUE #2: SUBMISSION FAILURE WITH SPECIFIC**

**ERRORS**

**13.1.1**

**Indicator**

Omaha Boarding Specification.docx

Page 105 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





A response comparable to the one in the screenshot below is returned by Omaha API. More

details are available in Omaha Boarding API - Basic Verification Guide.

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

**13.1.1**

**Cause**

Omaha Boarding API was implemented with numerous validation rules to prevent false

MPA data from being entered into the Fiserv system.

**13.1.1**

**Actions**

If you are not aware of the existence of the validation rule or the error message(s) returned

are not informative enough, please contact Fiserv for further support.

The support request must provide the following information:

·

·

The username the MPA was submitted with

The XML content of the MPA

**14 COMMON ISSUE #3: SUBMISSION FAILURE WITHOUT**

**SPECIFIC ERRORS**

**14.1.1**

**Indicator**

A response comparable to the one in the screenshot below is returned by Omaha API. More

details are available in Omaha Boarding API - Basic Verification Guide.

<SubmitMPAResult xmlns:xsd="http://www.w3.org/2001/XMLSchema"

xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">

<ExternalRefId

xmlns="http://tempuri.org/">0000001</ExternalRefId>

<Timestamp xmlns="http://tempuri.org/">02/16/2016 05:19:12

PM</Timestamp>

Omaha Boarding Specification.docx

Page 106 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.





<Status xmlns="http://tempuri.org/">FAILURE</Status>

<Errors xmlns="http://tempuri.org/" />

</SubmitMPAResult>

**14.1.1**

**Cause**

As there should have been a clear error message indicating which validation rule was

violated that led to the submission failure, this is likely an unknown defect of Omaha

Boarding API.

**14.1.1**

**Actions**

Send a support request to Fiserv with information about:

·

·

The username the MPA was submitted with

The XML content of the MPA

Omaha Boarding Specification.docx

Page 107 of 107

This document contains confidential, proprietary information and may not be reproduced or copied without the express authorization of Fiserv.

