# ListOrderChannels200ResponseDataInnerSettings

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**use_webhooks** | **bool** | Use webhooks for real-time order sync. | [default to true]
**webhook_id** | **string** | External webhook identifier for management. | [optional]
**webhook_ids** | **int[]** | Registered WooCommerce webhook ids. | [optional]
**webhook_secret_created_at** | **\DateTime** | When the custom channel&#39;s webhook signing secret was issued. A non-secret signal so clients can show that a secret exists; the secret itself is never returned after creation. | [optional]
**site_url** | **string** | WooCommerce store URL. | [optional]
**auto_fulfill** | **bool** | Push tracking back to the platform when a shipment is dispatched. Enabled by default (opt-out) — set to false to disable write-back; an unset value still syncs. | [optional]
**checkout_token_created_at** | **\DateTime** | When the checkout token was issued (internal; never exposed in API responses). | [optional]
**auto_sync** | **bool** | Periodically poll the channel for new orders. | [default to false]
**sync_interval_minutes** | **int** | Polling interval in minutes (5-1440). | [default to 15]
**auto_ship_on_create** | **bool** | Create a shipment automatically when an order arrives. | [default to false]
**default_carrier_id** | **string** | Default carrier ID for auto-shipping. | [optional]
**default_product_id** | **string** | Default carrier product ID for auto-shipping. | [optional]
**default_address_id** | **string** | Default sender address ID for auto-shipping. | [optional]
**shipping_method_mappings** | [**\Zippendo\Sdk\Model\ListOrderChannels200ResponseDataInnerSettingsShippingMethodMappingsInner[]**](ListOrderChannels200ResponseDataInnerSettingsShippingMethodMappingsInner.md) | Map imported shipping-method titles to shipping rules, for channels without checkout rate integration. | [optional]
**sync_only_unfulfilled** | **bool** | Only import orders that are not yet fulfilled. | [default to true]
**sync_orders_since** | **\DateTime** | Only sync orders placed at or after this timestamp. | [optional]
**service_point_count** | **int** | Number of service points to show at checkout (1-20). | [default to 6]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
