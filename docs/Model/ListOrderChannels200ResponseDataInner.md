# ListOrderChannels200ResponseDataInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique order channel ID. |
**name** | **string** | Display name of the channel. |
**type** | **string** | Type of the order channel (sales platform). |
**enabled** | **bool** | Whether the channel is active. |
**role** | **string** | What Zippendo is used for on this channel. &#x60;orders_and_rates&#x60; (default) imports orders and serves checkout rates. &#x60;rates_only&#x60; serves checkout rates and service-point selection ONLY — orders are owned by an external system such as a WMS, nothing is imported, and no fulfilment or tracking is pushed back to the platform. |
**brand_id** | **string** | Brand this channel belongs to, or null for organization-wide. Orders synced from this channel inherit it, and so do the shipments and documents made from them. |
**has_credentials** | **bool** | Whether credentials are configured (values are never exposed). |
**settings** | [**\Zippendo\Sdk\Model\ListOrderChannels200ResponseDataInnerSettings**](ListOrderChannels200ResponseDataInnerSettings.md) |  |
**webhooks_enabled** | **bool** | Whether real-time webhooks are enabled. | [optional]
**last_sync_at** | **\DateTime** | Timestamp of the last successful sync. | [optional]
**last_sync_error** | **string** | Error message from the last failed sync. | [optional]
**shipping_rule_ids** | **string[]** | IDs of shipping rules linked to this channel. | [optional]
**org_id** | **string** | Owning organization ID. |
**created_at** | **string** | Creation timestamp (ISO 8601). |
**updated_at** | **string** | Last update timestamp (ISO 8601). |

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
