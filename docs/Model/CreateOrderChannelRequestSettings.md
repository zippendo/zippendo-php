# CreateOrderChannelRequestSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**use_webhooks** | **bool** | Use webhooks for real-time order sync. | [optional] [default to true]
**site_url** | **string** | WooCommerce store URL. | [optional]
**auto_fulfill** | **bool** | Push tracking back to the platform when a shipment is dispatched. Enabled by default (opt-out) — set to false to disable write-back; an unset value still syncs. | [optional]
**auto_sync** | **bool** | Periodically poll the channel for new orders. | [optional] [default to false]
**sync_interval_minutes** | **int** | Polling interval in minutes (5-1440). | [optional] [default to 15]
**auto_ship_on_create** | **bool** | Create a shipment automatically when an order arrives. | [optional] [default to false]
**default_carrier_id** | **string** | Default carrier ID for auto-shipping. | [optional]
**default_product_id** | **string** | Default carrier product ID for auto-shipping. | [optional]
**default_address_id** | **string** | Default sender address ID for auto-shipping. | [optional]
**shipping_method_mappings** | [**\Zippendo\Sdk\Model\CreateOrderChannelRequestSettingsShippingMethodMappingsInner[]**](CreateOrderChannelRequestSettingsShippingMethodMappingsInner.md) | Map imported shipping-method titles to shipping rules, for channels without checkout rate integration. | [optional]
**sync_only_unfulfilled** | **bool** | Only import orders that are not yet fulfilled. | [optional] [default to true]
**sync_orders_since** | **\DateTime** | Only sync orders placed at or after this timestamp. | [optional]
**service_point_count** | **int** | Number of service points to show at checkout (1-20). | [optional] [default to 6]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
