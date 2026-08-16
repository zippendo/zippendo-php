# CreateOrgWebhookRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Human-readable webhook name |
**url** | **string** | Webhook endpoint URL |
**events** | **string[]** | Events to subscribe to |
**is_active** | **bool** | Whether the webhook is active | [optional] [default to true]
**brand_id** | **string** | Brand this record is assigned to; null (or omitted outside a brand session) keeps it organization-wide | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
