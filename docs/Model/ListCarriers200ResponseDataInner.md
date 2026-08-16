# ListCarriers200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique carrier identifier |
**name** | **string** | Carrier display name |
**carrier_slug** | **string** | Carrier slug identifier |
**config** | [**array<string,\Zippendo\Sdk\Model\ListCarriers200ResponseDataInnerConfigValue>**](ListCarriers200ResponseDataInnerConfigValue.md) | Carrier configuration (required and optional fields) |
**org_id** | **string** | Owning organization ID |
**brand_id** | **string** | Brand this record belongs to, or null when it is organization-wide |
**created_at** | **string** | Creation timestamp (ISO 8601) |
**updated_at** | **string** | Last update timestamp (ISO 8601) |
**logo** | **string** | Carrier logo URL | [optional]
**brand_color** | **string** | Carrier brand color (hex) | [optional]
**deprecated** | **bool** | Whether this carrier integration is deprecated (still works, but discouraged) | [optional]
**deprecation_message** | **string** | Guidance shown alongside the deprecated tag (e.g. what to migrate to) | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
