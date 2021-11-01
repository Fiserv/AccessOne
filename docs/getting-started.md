# Getting Started

## Welcome to the AccessOne API Suite!

Fiserv's Full Service Processing ISO clients are welcome to integrate these APIs within your own workflow and systems.  APIs are available for merchant boarding, reporting, inquiry, and maintenance.
 

## North Merchant Boarding

North backend platform boarding via AccessOne API currently uses a SOAP/XML implementation.  For more information please refer to [North Boarding](?path=docs/north-boarding-api-specifications.md)


## Optis Merchant Boarding

Optis (formally Omaha) backend platform boarding via AccessOne API currently uses a SOAP/XML implementation.  For more information please refer to [Optis Boarding](?path=docs/optis-boarding-api-specifications.md)


## Merchant Reporting

Various reporting APIs are available to retrieve authorization/settlement/funding related information using a REST/XML implmentation.  For more information please refer to [reporting-api-specifications](?path=docs/reporting-api-specifications.md)


## Merchant Inquiry
Real-time inquiry APIs will retrieve merchant attribute information directly against the backend systems of record.  The APIs use a full REST/JSON implementation and all of the associated documentation is included directly in the API specifications (including a full data dictionary).  An API is available to retrieve all merchant attributes.  There are also APIs to retrieve smaller subset of information (e.g. Location Chaining, Merchant Profile, Programs, Entitlements, Billing Attributes).

## Merchant Update
A real-time update API will allow for maintenance directly against the backend systems of record.  The API use a full REST/JSON implementation and all of the associated documentation is included directly in the API specifications (including a full data dictionary).  You can leverage this API in your workflow in order to keep your systems syncronized with the Fiserv processing platforms.
