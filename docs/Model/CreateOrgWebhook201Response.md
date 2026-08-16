# CreateOrgWebhook201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Webhook ID |
**name** | **string** | Human-readable webhook name |
**url** | **string** | Webhook endpoint URL |
**secret** | **string** | Signing secret used to verify webhook payloads |
**events** | **string[]** | Events the webhook is subscribed to |
**is_active** | **bool** | Whether the webhook is active |
**brand_id** | **string** | Brand this record belongs to, or null when it is organization-wide |
**created_at** | **string** | Creation timestamp (ISO 8601) |
**updated_at** | **string** | Last update timestamp (ISO 8601) |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
