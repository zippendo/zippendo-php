# ListOrgBrands200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**company_name** | **string** | Legal entity name printed on this brand&#39;s documents | [optional]
**vat_number** | **string** | VAT/tax ID for this brand&#39;s shipments and documents | [optional]
**customs** | **array<string,string>** | Customs identifiers keyed by type | [optional]
**address_line1** | **string** | Street address line 1 | [optional]
**address_line2** | **string** | Street address line 2 | [optional]
**city** | **string** | City | [optional]
**postal_code** | **string** | Postal code | [optional]
**country** | **string** | Country (ISO 3166-1 alpha-2) | [optional]
**primary_color** | **string** | Primary brand colour — document title and table headers | [optional]
**secondary_color** | **string** | Secondary brand colour — subtitle, section headings, totals accent | [optional]
**id** | **string** | Unique brand identifier |
**org_id** | **string** | Owning organization |
**name** | **string** | Brand display name |
**slug** | **string** | URL-safe identifier, unique within the organization |
**use_org_customs** | **bool** | Whether this brand ships under the organization&#39;s fiscal identity. True (the default) declares the organization&#39;s VAT number and customs identifiers and ignores the brand&#39;s own. False makes the brand&#39;s own values the sole source — nothing falls back to the organization, so an identifier the brand has not set is not declared at all. |
**logo_url** | **string** | Authenticated URL for the brand logo, or null when none is set |
**archived_at** | **string** | When the brand was archived; null when active |
**created_at** | **string** | Creation timestamp (ISO 8601) |
**updated_at** | **string** | Last update timestamp (ISO 8601) |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
