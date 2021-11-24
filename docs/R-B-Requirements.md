# **B - Requirements**

This section specifies the detailed requirements for applying WS-Security Authentication using Username Tokens with a Username and Password Digest. The OASIS standard is being utilized with [the profile of Web Services Security Username Token Profile Version 1.1.1](http://docs.oasis-open.org/wss-m/wss/v1.1.1/os/wss-UsernameTokenProfile-v1.1.1-os.html).

The following request sample illustrates how the security information will be sent within SOAP Header. Note that the SOAP body will vary depending on the specifics of the data communicated by Lonestar pillars.

|Request Message Sample|
| :-: |
|<p><?xml version="1.0" encoding="utf-8"?></p><p><soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:wsa="http://schemas.xmlsoap.org/ws/2004/08/addressing" xmlns:wsse="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd" xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd"></p><p>`	`<soap:Header></p><p>`		`<wsa:Action>http://tempuri.org/HelloWorld</wsa:Action></p><p>`		`<wsa:MessageID>urn:uuid:ebc4c587-52b8-4867-a47b-c0ddc750fc10</wsa:MessageID></p><p>`		`<wsa:ReplyTo></p><p>`			`<wsa:Address>http://schemas.xmlsoap.org/ws/2004/08/addressing/role/anonymous</wsa:Address></p><p>`		`</wsa:ReplyTo></p><p>`		`<wsa:To>http://localhost:60286/TestWS/Service.asmx</wsa:To></p><p>`		`<wsse:Security soap:mustUnderstand="1"></p><p>`			`<wsu:Timestamp wsu:Id="Timestamp-55bec23e-030a-461b-9474-bc182879bb63"></p><p>`				`<wsu:Created>2014-11-27T04:49:32Z</wsu:Created></p><p>`				`<wsu:Expires>2014-11-27T04:54:32Z</wsu:Expires></p><p>`			`</wsu:Timestamp></p><p>`			`<wsse:UsernameToken xmlns:wsu="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd" wsu:Id="SecurityToken-95440d2c-3046-4aab-9ed3-d836966fb611"></p><p>`				`<wsse:Username>api\_user</wsse:Username></p><p>`				`<wsse:Password Type="http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-username-token-profile-1.0#PasswordDigest">Z9DtKSZJ1N4hfi0blPNd6wNxIx4=</wsse:Password></p><p>`				`<wsse:Nonce>P02bHRPDX85BAwsOeresGw==</wsse:Nonce></p><p>`				`<wsu:Created>2014-11-27T04:49:32Z</wsu:Created></p><p>`			`</wsse:UsernameToken></p><p>`		`</wsse:Security></p><p>`	`</soap:Header></p><p>`	`<soap:Body></p><p>`		`<!-- SOAP Body Data -->	</p><p>`       `</soap:Body></p><p></soap:Envelope></p><p></p>|

The following namespaces are used: **http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-utility-1.0.xsd** and **http://docs.oasis-open.org/wss/2004/01/oasis-200401-wss-wssecurity-secext-1.0.xsd** which are represented below by the prefixes “**wsu**” and “**wsse**” respectively.

The entry-point to WS-Security is a SOAP Header element called <wsse:Security>. It contains the security-related data and information. Within <wsse:Security>, the following elements are required (Note that the order of the elements below is fixed for security purposes):

<wsu:Timestamp>: It is used to express the creation and expiration time of the message. To address replay attacks, the message timestamps are required:

- <wsu:Created>: the creation time of the message.
- <wsu:Expires>: the expiration time of the message.

<wsse:UsernameToken>: the Username, PasswordDigest and the security-related information to authenticate the identity will be provided within this element:

- <wsse:Username>: the clear text username. 
- <wsse:Password>: it holds the digested password which is constructed as follows:

PasswordDigest = Base64( SHA-1( nonce + created + password-token) )

That is, concatenate the nonce, creation timestamp, and the password-token, digest the combination using SHA-1 hash algorithm, then include the Base64 coding of that result as the password.

Note that depending on the specifics of the API, there would be a single username/password-token to consume the service or multiple usernames/password-tokens based on the AccessOne User Setup.

- <wsse:Nonce>: a cryptographically random value. Each message must include a new nonce value to detect replay attacks.

