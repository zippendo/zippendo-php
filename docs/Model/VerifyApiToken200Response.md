# VerifyApiToken200Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**valid** | **bool** | Whether the token is valid |
**token_id** | **string** | Token identifier | [optional]
**user_id** | **string** | User identifier the token belongs to | [optional]
**org_id** | **string** | Organization identifier the token belongs to | [optional]
**scopes** | **string[]** | Permission scopes granted by the token | [optional]
**expires_at** | **string** | Expiry timestamp (ISO 8601), null if it never expires | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
