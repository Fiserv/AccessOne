# **B.1 ENUMERATIONS**

This section specifies the detailed requirements for applying WS-Security Authentication using Username Tokens with a Username and Password Digest. The OASIS standard is being utilized with the profile of Web Services Security Username Token Profile Version 1.1.1.
The following request sample illustrates how the security information will be sent within SOAP Header. Note that the SOAP body will vary depending on the specifics of the data communicated by Lonestar pillars.

Request Message Sample
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd">
	<soap:Header>
		<wsa:Action>http://tempuri.org/HelloWorld</wsa:Action>
		<wsa:MessageID>urn:uuid:ebc4c587-52b8-4867-a47b-c0ddc750fc10</wsa:MessageID>
		<wsa:ReplyTo>
			<wsa:Address>http://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:Address>
		</wsa:ReplyTo>
		<wsa:To>http://localhost:60286/TestWS/Service.asmx</wsa:To>
		<wsse:Security soap:mustUnderstand="1">
			<wsu:Timestamp wsu:Id="Timestamp-55bec23e-030a-461b-9474-bc182879bb63">
				<wsu:Created>2014-11-27T04:49:32Z</wsu:Created>
				<wsu:Expires>2014-11-27T04:54:32Z</wsu:Expires>
			</wsu:Timestamp>
			<wsse:UsernameToken xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" wsu:Id="SecurityToken-95440d2c-3046-4aab-9ed3-d836966fb611">
				<wsse:Username>api_user</wsse:Username>
				<wsse:Password Type="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-username-token-profile-1.0#PasswordDigest">Z9DtKSZJ1N4hfi0blPNd6wNxIx4=</wsse:Password>
				<wsse:Nonce>P02bHRPDX85BAwsOeresGw==</wsse:Nonce>
				<wsu:Created>2014-11-27T04:49:32Z</wsu:Created>
			</wsse:UsernameToken>
		</wsse:Security>
	</soap:Header>
	<soap:Body>
		<!-- SOAP Body Data -->	
       </soap:Body>
</soap:Envelope>


The following namespaces are used: http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd and http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd which are represented below by the prefixes “wsu” and “wsse” respectively.
The entry-point to WS-Security is a SOAP Header element called <wsse:Security>. It contains the security-related data and information. Within <wsse:Security>, the following elements are required (Note that the order of the elements below is fixed for security purposes):
<wsu:Timestamp>: It is used to express the creation and expiration time of the message. To address replay attacks, the message timestamps are required:
-	<wsu:Created>: the creation time of the message.
-	<wsu:Expires>: the expiration time of the message.
<wsse:UsernameToken>: the Username, PasswordDigest and the security-related information to authenticate the identity will be provided within this element:
-	<wsse:Username>: the clear text username. 
-	<wsse:Password>: it holds the digested password which is constructed as follows:

PasswordDigest = Base64( SHA-1( nonce + created + password-token) )

That is, concatenate the nonce, creation timestamp, and the password-token, digest the combination using SHA-1 hash algorithm, then include the Base64 coding of that result as the password.

Note that depending on the specifics of the API, there would be a single username/password-token to consume the service or multiple usernames/password-tokens based on the AccessOne User Setup.

-	<wsse:Nonce>: a cryptographically random value. Each message must include a new nonce value to detect replay attacks.

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


