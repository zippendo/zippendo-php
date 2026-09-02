# UpdateOrderChannelRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**brand_id** | **string** | Brand this channel belongs to; null for organization-wide | [optional]
**name** | **string** | Display name for the channel. | [optional]
**enabled** | **bool** | Whether the channel is active. | [optional]
**credentials** | **array<string,mixed>** | Type-specific platform credentials. | [optional]
**settings** | [**\Zippendo\Sdk\Model\UpdateOrderChannelRequestSettings**](UpdateOrderChannelRequestSettings.md) |  | [optional]
**shipping_rule_ids** | **string[]** | IDs of shipping rules linked to this channel. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
