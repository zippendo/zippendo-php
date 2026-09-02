# CreateOrderChannelWebhookSecret201Response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**secret** | **string** | The webhook signing secret. Returned only once — store it in your system; every push to the ingest URL must carry an HMAC-SHA256 hex signature of the raw body computed with it. |
**webhook_url** | **string** | The ingest URL your system pushes signed order events to. |
**created_at** | **\DateTime** | When this secret was issued (ISO 8601). |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
