# ListShipments200ResponseDataInnerAddress

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique address identifier |
**name** | **string** | Name of the address |
**att_contact** | **string** | Attention contact person |
**address1** | **string** | Address line 1 |
**address2** | **string** | Address line 2 |
**zipcode** | **string** | Postal/ZIP code |
**city** | **string** | City |
**phone** | **string** | Phone number |
**country_code** | **string** | ISO country code |
**state** | **string** | State/Province |
**email** | **string** | Email address |
**customs** | **array<string,string>** | Customs identifiers keyed by type | [optional]
**address_types** | **string[]** | Address types (sender, pickup, return) |
**org_id** | **string** | Owning organization ID |
**brand_id** | **string** | Brand this record belongs to, or null when it is organization-wide |
**created_at** | **string** | Creation timestamp (ISO 8601) |
**updated_at** | **string** | Last update timestamp (ISO 8601) |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
