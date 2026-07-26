# GetOrg200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique organization identifier |
**name** | **string** | Organization name |
**slug** | **string** | Organization URL slug (unique identifier) |
**description** | **string** | Organization description |
**currency** | **string** | Billing currency (ISO 4217 code) | [default to 'DKK']
**vat_number** | **string** | Company VAT/tax ID for invoices | [optional]
**billing_email** | **string** | Billing email for invoices | [optional]
**company_name** | **string** | Legal company name | [optional]
**address_line1** | **string** | Address line 1 | [optional]
**address_line2** | **string** | Address line 2 | [optional]
**city** | **string** | City | [optional]
**postal_code** | **string** | Postal code | [optional]
**country** | **string** | Country (ISO 3166-1 alpha-2 code) | [optional]
**customs** | **array<string,string>** | Customs identifiers keyed by type | [optional]
**created_at** | **string** | Creation timestamp (ISO 8601) |
**updated_at** | **string** | Last update timestamp (ISO 8601) |
**_count** | [**\Zippendo\Sdk\Model\GetOrg200ResponseCount**](GetOrg200ResponseCount.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
