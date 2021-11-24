### Setup Security and Authentication, Method and Media Type 

In the initial new request window, setup following parameters with their corresponding values:

` `- **Method**: POST

` `- **Endpoint**: <https://api.fdportfoliomanager.com/pm/ReportService.svc>

` `- **Resource**: [/rest/APIName](\\dps2012\rest\GetGGe4MerchantEnrollment), For example: [/rest/GetGGe4MerchantEnrollment](\\dps2012\rest\GetGGe4MerchantEnrollment)  

\*\*\*Note: Depending on which Reporting API, the APIName in the **Resource** link can be changed. Refer to section [D – SERVICE OPERATIONS](#_SERVICE_OPERATIONS) to get the APIName.

For example, [/rest/GetGGe4MerchantEnrollment](\\dps2012\rest\GetGGe4MerchantEnrollment)  is used to get API for API GetGGe4MerchantEnrollment. If the user wants to get API for GetPaymentDetail, the Resource link should be [/rest/GetPaymentDetail](\\dps2012\rest\GetGGe4MerchantEnrollment) . 

` `- **Parameters**: Blank

` `- **Media Type**: application/xml




User and Token are always required for REST request.

Click on **Headers** tab and  icon to add user and token parameters then input their value in **Value** column.

- **user**: plain text, provided by Fiserv
- **token**: encrypted API password based on SHA-256 standard.













At Headers tab, click on (**+**) button to add **user** and **token**.


**Add user to Header**:

**Input Value for Header user**. This Value is UserName which is used to access to AccessOne system.


Add **token** to Header:


**Input Value for Header token**. Refer to step 3 – Generate Token below.

