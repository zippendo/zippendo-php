# CreateOrderChannelRequest

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Display name for the channel. |
**type** | **string** | Type of the order channel. Platform channels (Shopify, WooCommerce) are created via their connect flows. |
**brand_id** | **string** | Brand this channel belongs to; null for organization-wide | [optional]
**enabled** | **bool** | Whether the channel is active. | [optional] [default to true]
**role** | **string** | What Zippendo is used for on this channel. &#x60;orders_and_rates&#x60; (default) imports orders and serves checkout rates. &#x60;rates_only&#x60; serves checkout rates and service-point selection ONLY — orders are owned by an external system such as a WMS, nothing is imported, and no fulfilment or tracking is pushed back to the platform. | [optional] [default to 'orders_and_rates']
**settings** | [**\Zippendo\Sdk\Model\CreateOrderChannelRequestSettings**](CreateOrderChannelRequestSettings.md) |  | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
