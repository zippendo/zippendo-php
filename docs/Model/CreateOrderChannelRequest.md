# CreateOrderChannelRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Display name for the channel. |
**type** | **string** | Type of the order channel. Platform channels (Shopify, WooCommerce) are created via their connect flows. |
**brand_id** | **string** | Brand this channel belongs to; null for organization-wide | [optional]
**enabled** | **bool** | Whether the channel is active. | [optional] [default to true]
**settings** | [**\Zippendo\Sdk\Model\CreateOrderChannelRequestSettings**](CreateOrderChannelRequestSettings.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
