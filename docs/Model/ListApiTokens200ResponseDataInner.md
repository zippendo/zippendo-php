# ListApiTokens200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique API token identifier |
**name** | **string** | Token name for identification |
**token_prefix** | **string** | First 12 chars of the token for identification |
**scopes** | **string[]** | Permission scopes granted by the token |
**last_used_at** | **string** | Timestamp the token was last used (ISO 8601), null if never used |
**expires_at** | **string** | Expiry timestamp (ISO 8601), null if it never expires |
**created_at** | **string** | Creation timestamp (ISO 8601) |
**created_by** | [**\Zippendo\Sdk\Model\ListApiTokens200ResponseDataInnerCreatedBy**](ListApiTokens200ResponseDataInnerCreatedBy.md) |  |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
