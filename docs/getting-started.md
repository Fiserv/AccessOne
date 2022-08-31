# Getting Started

## Welcome to the AccessOne API Suite

AccessOne APIs provide real-time access to our backend systems of record for inquiry and maintenance. These APIs are available for use by our wholesale and Full Service Processing ISO clients and are welcome to integrate these APIs within your own workflow and systems. APIs are available for merchant/equipment inquiry and maintenance.

<br>

## Support Information

Please contact your CSA for more information.

<br>

## Merchant Inquiry

Real-time inquiry APIs will retrieve merchant attribute information directly against the backend systems of record.  The APIs use a full REST/JSON implementation and all of the associated documentation is included directly in the API specifications.  An API is available to retrieve all merchant attributes.  There are also APIs to retrieve smaller subset of information (e.g. Location Chaining, Merchant Profile, Programs, Entitlements, Billing Attributes).

<br>

## Merchant Update

A real-time update API will allow for maintenance directly against the backend systems of record.  The API uses a full REST/JSON implementation and all of the associated documentation is included directly in the API specifications.  You can leverage this API in your workflow in order to keep your systems syncronized with the Fiserv processing platforms.

<br>

## Equipment Search

Real-time APIs provide access to our POS system of record for terminals, related accessories, and features.  Equipment Inquiry functions are supported.

<br>

## Equipment Update

Real-time APIs provide access to our POS system of record for terminals, related accessories, and features.  Equipment Add and Maintenance functions are fully supported.

<br>

## Request URL Structure

    [Base URL] [API Call]

<br>

## Request Parameters

    Base URL (UAT): https://uat-aoapi.youraccessone.com
    Base URL (PROD): coming soon
    API Call: The specific API call you want to make, e.g., /v1/api/auth/token

<br>

## Process

> - Currently in BETA testing.
>
> - For UAT access, contact your CSA and provide your IPs to be whitelisted along with your primary ID.
>
> - We will whitelist the IPs, create a username and provide the credentials to you and build test MIDs if necessary.
>
> - When you have completed testing in UAT, we will enable your profile in PROD.
>
> - You can create and manage your users and begin using AM APIs.
