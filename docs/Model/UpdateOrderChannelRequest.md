# UpdateOrderChannelRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**brand_id** | **string** | Brand this channel belongs to; null for organization-wide | [optional]
**name** | **string** | Display name for the channel. | [optional]
**enabled** | **bool** | Whether the channel is active. | [optional]
**role** | **string** | What Zippendo is used for on this channel. &#x60;orders_and_rates&#x60; (default) imports orders and serves checkout rates. &#x60;rates_only&#x60; serves checkout rates and service-point selection ONLY — orders are owned by an external system such as a WMS, nothing is imported, and no fulfilment or tracking is pushed back to the platform. | [optional]
**credentials** | **array<string,mixed>** | Type-specific platform credentials. | [optional]
**settings** | [**\Zippendo\Sdk\Model\UpdateOrderChannelRequestSettings**](UpdateOrderChannelRequestSettings.md) |  | [optional]
**shipping_rule_ids** | **string[]** | IDs of shipping rules linked to this channel. | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
