# Reporting

AccessOne Reporting APIs provide access to our system for reporting. These APIs are available for use by our Retail, Wholesale and Full Service Processing ISO clients and are welcome to integrate these APIs within your own workflow and systems.

## Request URL Structure

    [Base URL] [API Call]

## Request Parameters

    Base URL (PROD): https://api.fdportfoliomanager.com/pm/ReportService.svc/rest
    API Call: The specific API call you want to make

More information, specification document is available on firstdataclients.com by navigating to Acquiring & ISO Solutions > AccessOne > AccessOne API Spec Documents.

## Reporting API Calls:

### GetBatchSummaryByEntity

Return batch summary data of hierarchy entity choice(s) based on the selected date range 

### GetBatchSummaryByMerchant

Return batch summary data of the selected merchant number 

### GetBatchDetail

Return transaction-details data of a selected batch number

### GetCardSummary

Return card summary data based on selected date range

### GetPaymentSummaryByEntity

Return payment data of the entity choices based on the selected date range

### GetPaymentSummaryByMerchant

Return payment data of selected merchant number  

### GetPaymentDetail

Return detailed payment data of the selected merchant number

### GetReturnSummaryByEntity

Get summarized return data and sale data of the selected hierarchy entity choices 

### GetReturnSummaryByMerchant

Get detailed data of return transactions of the selected merchant number based on the selected range 

### GetChargebacksSummary

Return chargeback data at summary level based on the selected date range 

### GetChargebacksDetail

Return detailed data of chargeback transactions of a specific merchant number, based on the selected date range

### GetRetrievalsSummary

Return summarized retrieval data based on the selected date range

### GetRetrievalsDetail

Return detailed data of retrieval transactions of a specific merchant number, based on the selected date range

### GetVoidsRejectsSummary

Return summarized data of voids/rejects transactions based on the selected date range

### GetVoidsRejectsDetail

Return detailed data of voids/rejects transactions of a specific merchant number, based on the selected date range

### GetVoucher

Return voucher details of the selected transaction

### GetTransactions

Return a list of detailed transactions data based on the selected criteria

### GetAuthorizationLogSummary

Return summarized data of authorization transactions based on the selected criteria

### GetAuthorizationLogDetail

Return detailed data of authorization transactions for a specific merchant number, based on the selected date range

### GetAuthorizationLogBuyPassSummary

Return summarized data of Buypass authorization transactions based on the selected criteria

### GetAuthorizationLogBuyPassDetail

Return detailed data of Buypass authorization transactions for a specific merchant number, based on the selected date range

### GetAuthorizationLogGGeSummary

Return summarized data of GGe4 authorization transactions based on the selected criteria

### GetAuthorizationLogGGeDetail

Return detailed data of GGe4 authorization transactions for a specific merchant number, based on the selected date range

### GetAuthorizationLogNashvilleSummary

Return summarized data of Nashville authorization transactions based on the selected criteria

### GetAuthorizationLogNashvilleDetail

Return detailed data of Nashville authorization transactions for a specific merchant number, based on the selected date range

### GetAuthorizationLogNorthSummary

Return summarized data of North authorization transactions based on the selected criteria

### GetAuthorizationLogNorthDetail

Return detailed data of North authorization transactions for a specific merchant number, based on the selected date range

### GetAuthorizationLogOmahaSummary

Return summarized data of Omaha authorization transactions based on the selected criteria

### GetAuthorizationLogOmahaDetail

Return detailed data of Omaha authorization transactions for a specific merchant number, based on the selected date range

### GetAuthorizationVendorSummary

Return summarized data of authorization transactions by vendors based on the selected criteria

### GetAuthorizationVendorDetail

Return detailed data of authorization transactions by vendors for a specific merchant number, based on the selected date range

### GetMerchantList

Return a merchant list with detailed data for each merchant based on the selected criteria

### GetMerchantComments

Return the list of comment for specific merchant

### GetOmahaMerchantProfile

Return a full profile for specific Omaha merchant

### GetOmahaMerchantCardType

Return the card type list for specific Omaha merchant

### GetOmahaMerchantCardTypePinDebit

Return a list of Card Type PIN Debit for specific Omaha merchant

### GetOmahaMerchantCardInfomationPrivateLabel

Return the detailed data of Private Label Card Type for specific Omaha merchant

### GetOmahaMerchantMemos

Return Memos data for specific Omaha merchant

### GetNorthMerchantProfile

Return a full profile data for specific North merchant

### GetNorthMechantEntitlements

Return entitlement data of the North merchant

### GetNorthMerchantPricingInformation

Return the pricing information (merchant fee) for specific North merchant

### GetNorthMerchantEntitlementFull

Return full Entitlement data of specific product code for North merchant

### GetNorthMerchantEntitlementDetail

Return the detailed Entitlement data of specific product code for North merchant

### GetMemphisMerchantProfile

Return a full profile for specific Memphis merchant

### GetMemphisMerchantCardInformation

Return data relating to card payment services accepted/rejected by the Memphis merchant

### GetMemphisMerchantCardServicesInformation

Return data relating to additional card payment services accepted/rejected by the Memphis merchant

### GetMemphisMerchantDebitNetworks

Return data of debit networks that the Memphis merchant participates

### GetMemphisMerchantAttributes

Return detailed data of the attributes of the Memphis merchant

### GetMemphisMerchantEquipments

Return detailed data of the equipments currently in use by the Memphis merchant

### GetMemphisMerchantBuypassInformation

Return data of the Memphis merchant relating to Buypass merchant network

### GetMemphisMerchantCardInformationDetail

Return detailed data of all sub card payment services of the selected card payment service accepted by the Memphis merchant

### GetMemphisMerchantEquipmentSpecificExtra

Return data relating to equipment specifics and equipment extras of the chosen equipment ID

### GetMemphisMerchantEquipmentAttribute

Return detailed data on the attributes of the chosen equipment id

### GetOmahaMerchantStatementList

Return available statements for a merchant

### GetOmahaMerchantStatement

Return statement data for a merchant statement

### GetNonQualifyingTransactionSummaryByEntity

Return Non-qualifying transactions data of hierarchy entity choice(s) based on the selected date range.

### GetNonQualifyingTransactionByMerchant

Return Non-qualifying transactions data of the selected merchant number

### GetGGeMerchantEnrollment

Return Payeezy Gateway Enrollment Activity report.

### GetGGeMerchantEnrollmentByMerchant

Return Payeezy Gateway Enrollment Activity report of the selected merchant number.

### GetReturnsReportByEntity

Return the Returns report data of the entity choices based on the selected date range.

### GetReturnsReportByMerchant

Return Returns data of a selected merchant number.

### GetCustomerNotPresentByEntity

Return Customer Not Present data of the entity choices based on the selected date range.

### GetCustomerNotPresentByMerchant

Return CustomerNot Present data of a selected merchant number.

### GetHVMerchantsCustomerPresentByEntity

Return high volume merchants customer present data of the entity choices based on the selected date range.

### GetHVMerchantsCustomerPresentByMerchant

Return high volume merchants customer present data of selected merchant number.

### GetAllOtherMCCMerchantsCustomerPresentByEntity

Return all other MCC merchants customer present data of the entity choices based on the selected date range.

### GetAllOtherMCCMerchantsCustomerPresentByMerchant

Return all other MCC  merchants customer present data of selected merchant number.

### GetMerchantAdjustmentSummaryByEntity

Return merchant adjustment data of the entity choices based on the selected date range.

### GetMerchantAdjustmentSummaryByMerchant

Return merchant adjustment data of selected merchant number .

### GetMerchantAdjustmentDetail

Return merchant adjustment details of selected merchant number .

### GetChatHistorySummaryByEntity

Return Chat history data of the entity choices based on the selected date range.

### GetChatHistoryByMerchant

Return chat history of a specific merchant.

### GetEMVIndicatorReportByEntity

Return EMV indicator data of the entity choices based on the selected date range.

### GetEMVIndicatorReportByMerchant

Return EMV indicator report of the merchant.

### GetTaxReportDailySubmittedSummaryByEntity

Return daily submitted TIN matching summary data of hierarchy entity choice(s) based on the selected date range.

### GetTaxReportDailySubmittedSummaryByMerchant

Return daily submitted TIN matching summary data of the selected merchant number.

### GetTaxReportDailySubmittedDetailByEntity

Return daily submitted TIN matching summary data of hierarchy entity choice(s) based on the selected date range.

### GetTaxReportDailySubmittedDetailByMerchant

Return daily submitted TIN matching detail data of the selected merchant number.

### GetTaxReportMonthlyInvalidSummaryByEntity

Return monthly invalid summary tax data of hierarchy entity choice(s) based on the selected date range.

### GetTaxReportMonthlyInvalidSummaryByMerchant

Return monthly invalid summary tax data of the selected merchant number.

### GetTaxReportMonthlyInvalidDetailByEntity

Return monthly invalid detail tax data of hierarchy entity choice(s) based on the selected date range.

### GetTaxReportMonthlyInvalidDetailByMerchant

Return monthly invalid detail tax data of the selected merchant number.

### GetTaxReportAdhoc

Return TIN Matching Ad-hoc report.

### GetMonetaryRejectsByEntity

Return Monetary Rejects summary report.

### GetMonetaryRejectsByMerchant

Return Monetary Rejects report in detail.

### GetRejectETCFrontEndEditExceptionsByEntity

Return ETC Front End Edit Exceptions (CD-016) data of the entity choices based on the selected date range.

### GetRejectETCFrontEndEditExceptionsByMerchant

Return ETC Front End Edit Exceptions (CD-016) data of selected merchant number  .

### GetTapeTransmittalRejectsByEntity

Return Tape Transmittal Rejects (CD-1430) data of the entity choices based on the selected date range,

### GetTapeTransmittalRejectsByMerchant

Return Tape Transmittal Rejects (CD-1430) data of selected merchant number.

### GetNorthMerchantStatementList

Get Statement list for North Merchant

### GetNorthMerchantStatement

Get Statement for North Merchant
