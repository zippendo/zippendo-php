# UpdateOrgRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Organization name | [optional]
**slug** | **string** | Organization slug | [optional]
**description** | **string** | Organization description | [optional]
**currency** | **string** | Billing currency (ISO 4217 code) | [optional]
**vat_number** | **string** | Company VAT/tax ID for invoices | [optional]
**overage_enabled** | **bool** | Allow shipments beyond plan limit (overage charges apply) | [optional]
**billing_email** | **string** | Billing email for invoices | [optional]
**company_name** | **string** | Legal company name | [optional]
**address_line1** | **string** | Address line 1 | [optional]
**address_line2** | **string** | Address line 2 | [optional]
**city** | **string** | City | [optional]
**postal_code** | **string** | Postal code | [optional]
**country** | **string** | Country (ISO 3166-1 alpha-2 code) | [optional]
**customs** | **array<string,string>** | Organization-wide customs identifiers (EORI, IOSS, VOEC, etc.); null clears all | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
