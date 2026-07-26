# CreateShipment201ResponseLogsInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique log entry identifier. |
**direction** | **string** | Direction of the logged request. |
**request** | **mixed** | Captured request payload. |
**response** | **mixed** | Captured response payload. | [optional]
**status_code** | **float** | HTTP status code of the response. | [optional]
**error** | **string** | Error message if the request failed. | [optional]
**duration** | **float** | Request duration in milliseconds. | [optional]
**created_at** | **string** | Timestamp when the log entry was created. |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
