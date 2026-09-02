# GetOrderChannelWebhookStatus200ResponseWebhooksInner

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **float** | Platform webhook ID. |
**topic** | **string** | Webhook event topic. |
**address** | **string** | Registered callback address. |
**created_at** | **string** | Webhook creation timestamp. |
**delivery_url** | **string** | WooCommerce delivery URL (same as &#x60;address&#x60;; present for WooCommerce channels). | [optional]
**status** | **string** | WooCommerce webhook status. A value other than &#x60;active&#x60; means WooCommerce disabled the webhook (e.g. after repeated delivery failures). | [optional]

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)
