# ListOrgWebhookDeliveries200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Delivery log ID |
**webhook_id** | **string** | ID of the webhook this delivery belongs to |
**event** | **string** | Event type that was delivered |
**payload** | **mixed** | JSON payload that was sent |
**status_code** | **float** | HTTP status code returned by the endpoint |
**response** | **string** | Response body returned by the endpoint |
**duration** | **float** | Request duration in milliseconds |
**success** | **bool** | Whether the delivery succeeded |
**attempt** | **float** | Delivery attempt number |
**error** | **string** | Error message if the delivery failed |
**created_at** | **string** | Delivery timestamp (ISO 8601) |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
