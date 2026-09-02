# Zippendo\Sdk\OrderChannelsApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createOrderChannel()**](OrderChannelsApi.md#createOrderChannel) | **POST** /orgs/{orgId}/order-channels | Create order channel |
| [**createOrderChannelWebhookSecret()**](OrderChannelsApi.md#createOrderChannelWebhookSecret) | **POST** /orgs/{orgId}/order-channels/{channelId}/webhook-secret | Create or rotate webhook signing secret |
| [**deleteOrderChannel()**](OrderChannelsApi.md#deleteOrderChannel) | **DELETE** /orgs/{orgId}/order-channels/{channelId} | Delete order channel |
| [**getOrderChannel()**](OrderChannelsApi.md#getOrderChannel) | **GET** /orgs/{orgId}/order-channels/{channelId} | Get order channel |
| [**getOrderChannelWebhookStatus()**](OrderChannelsApi.md#getOrderChannelWebhookStatus) | **GET** /orgs/{orgId}/order-channels/{channelId}/webhooks | Get channel webhook status |
| [**listOrderChannels()**](OrderChannelsApi.md#listOrderChannels) | **GET** /orgs/{orgId}/order-channels | List order channels |
| [**revokeOrderChannelWebhookSecret()**](OrderChannelsApi.md#revokeOrderChannelWebhookSecret) | **DELETE** /orgs/{orgId}/order-channels/{channelId}/webhook-secret | Revoke webhook signing secret |
| [**updateOrderChannel()**](OrderChannelsApi.md#updateOrderChannel) | **PATCH** /orgs/{orgId}/order-channels/{channelId} | Update order channel |


## `createOrderChannel()`

```php
createOrderChannel($org_id, $create_order_channel_request): \Zippendo\Sdk\Model\ListOrderChannels200ResponseDataInner
```

Create order channel

Creates a new order channel for an organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrderChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$create_order_channel_request = new \Zippendo\Sdk\Model\CreateOrderChannelRequest(); // \Zippendo\Sdk\Model\CreateOrderChannelRequest

try {
    $result = $apiInstance->createOrderChannel($org_id, $create_order_channel_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderChannelsApi->createOrderChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **create_order_channel_request** | [**\Zippendo\Sdk\Model\CreateOrderChannelRequest**](../Model/CreateOrderChannelRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\ListOrderChannels200ResponseDataInner**](../Model/ListOrderChannels200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createOrderChannelWebhookSecret()`

```php
createOrderChannelWebhookSecret($org_id, $channel_id): \Zippendo\Sdk\Model\CreateOrderChannelWebhookSecret201Response
```

Create or rotate webhook signing secret

Generates (or rotates) the custom channel's webhook signing secret used to authenticate order pushes to the ingest URL. The secret is returned only once. Rotating invalidates the previous secret immediately.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrderChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = clz9k2f0a0000abcd0000zzzz; // string | Organization ID.
$channel_id = clz9k2f0a0001abcd1234efgh; // string | Order channel ID.

try {
    $result = $apiInstance->createOrderChannelWebhookSecret($org_id, $channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderChannelsApi->createOrderChannelWebhookSecret: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID. | |
| **channel_id** | **string**| Order channel ID. | |

### Return type

[**\Zippendo\Sdk\Model\CreateOrderChannelWebhookSecret201Response**](../Model/CreateOrderChannelWebhookSecret201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteOrderChannel()`

```php
deleteOrderChannel($org_id, $channel_id): \Zippendo\Sdk\Model\RevokeApiToken200Response
```

Delete order channel

Deletes an order channel and cascades deletion of its orders.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrderChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = clz9k2f0a0000abcd0000zzzz; // string | Organization ID.
$channel_id = clz9k2f0a0001abcd1234efgh; // string | Order channel ID.

try {
    $result = $apiInstance->deleteOrderChannel($org_id, $channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderChannelsApi->deleteOrderChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID. | |
| **channel_id** | **string**| Order channel ID. | |

### Return type

[**\Zippendo\Sdk\Model\RevokeApiToken200Response**](../Model/RevokeApiToken200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrderChannel()`

```php
getOrderChannel($org_id, $channel_id): \Zippendo\Sdk\Model\ListOrderChannels200ResponseDataInner
```

Get order channel

Returns a single order channel by ID, including its linked shipping rules.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrderChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = clz9k2f0a0000abcd0000zzzz; // string | Organization ID.
$channel_id = clz9k2f0a0001abcd1234efgh; // string | Order channel ID.

try {
    $result = $apiInstance->getOrderChannel($org_id, $channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderChannelsApi->getOrderChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID. | |
| **channel_id** | **string**| Order channel ID. | |

### Return type

[**\Zippendo\Sdk\Model\ListOrderChannels200ResponseDataInner**](../Model/ListOrderChannels200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrderChannelWebhookStatus()`

```php
getOrderChannelWebhookStatus($org_id, $channel_id): \Zippendo\Sdk\Model\GetOrderChannelWebhookStatus200Response
```

Get channel webhook status

Returns whether webhooks are enabled and lists the webhooks registered with the platform.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrderChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = clz9k2f0a0000abcd0000zzzz; // string | Organization ID.
$channel_id = clz9k2f0a0001abcd1234efgh; // string | Order channel ID.

try {
    $result = $apiInstance->getOrderChannelWebhookStatus($org_id, $channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderChannelsApi->getOrderChannelWebhookStatus: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID. | |
| **channel_id** | **string**| Order channel ID. | |

### Return type

[**\Zippendo\Sdk\Model\GetOrderChannelWebhookStatus200Response**](../Model/GetOrderChannelWebhookStatus200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listOrderChannels()`

```php
listOrderChannels($org_id, $page, $limit, $brand_id, $brand_scope, $type, $enabled, $search): \Zippendo\Sdk\Model\ListOrderChannels200Response
```

List order channels

Returns a paginated list of order channels for an organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrderChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$page = 1; // int | Page number (1-based)
$limit = 20; // int | Items per page (max 100)
$brand_id = brnd_8f3kd92ld0; // string | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
$brand_scope = own; // string | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
$type = shopify; // string | Filter by channel type.
$enabled = true; // string | Filter by enabled state.
$search = Anna's Shopify Store; // string | Search by channel name.

try {
    $result = $apiInstance->listOrderChannels($org_id, $page, $limit, $brand_id, $brand_scope, $type, $enabled, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderChannelsApi->listOrderChannels: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **page** | **int**| Page number (1-based) | [optional] [default to 1] |
| **limit** | **int**| Items per page (max 100) | [optional] [default to 20] |
| **brand_id** | **string**| Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **brand_scope** | **string**| How the brand context narrows this list: \&quot;own\&quot; returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \&quot;shared\&quot; returns only unassigned organization-wide rows, \&quot;both\&quot; (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \&quot;shared\&quot; returns no rows, since those records are never visible organization-wide from within a brand context. | [optional] |
| **type** | **string**| Filter by channel type. | [optional] |
| **enabled** | **string**| Filter by enabled state. | [optional] |
| **search** | **string**| Search by channel name. | [optional] |

### Return type

[**\Zippendo\Sdk\Model\ListOrderChannels200Response**](../Model/ListOrderChannels200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `revokeOrderChannelWebhookSecret()`

```php
revokeOrderChannelWebhookSecret($org_id, $channel_id): \Zippendo\Sdk\Model\RevokeOrderChannelWebhookSecret200Response
```

Revoke webhook signing secret

Revokes the custom channel's webhook signing secret. All subsequent pushes to the ingest URL are rejected until a new secret is generated.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrderChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = clz9k2f0a0000abcd0000zzzz; // string | Organization ID.
$channel_id = clz9k2f0a0001abcd1234efgh; // string | Order channel ID.

try {
    $result = $apiInstance->revokeOrderChannelWebhookSecret($org_id, $channel_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderChannelsApi->revokeOrderChannelWebhookSecret: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID. | |
| **channel_id** | **string**| Order channel ID. | |

### Return type

[**\Zippendo\Sdk\Model\RevokeOrderChannelWebhookSecret200Response**](../Model/RevokeOrderChannelWebhookSecret200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateOrderChannel()`

```php
updateOrderChannel($org_id, $channel_id, $update_order_channel_request): \Zippendo\Sdk\Model\ListOrderChannels200ResponseDataInner
```

Update order channel

Updates an order channel and its linked shipping rules.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrderChannelsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = clz9k2f0a0000abcd0000zzzz; // string | Organization ID.
$channel_id = clz9k2f0a0001abcd1234efgh; // string | Order channel ID.
$update_order_channel_request = new \Zippendo\Sdk\Model\UpdateOrderChannelRequest(); // \Zippendo\Sdk\Model\UpdateOrderChannelRequest

try {
    $result = $apiInstance->updateOrderChannel($org_id, $channel_id, $update_order_channel_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrderChannelsApi->updateOrderChannel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID. | |
| **channel_id** | **string**| Order channel ID. | |
| **update_order_channel_request** | [**\Zippendo\Sdk\Model\UpdateOrderChannelRequest**](../Model/UpdateOrderChannelRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\ListOrderChannels200ResponseDataInner**](../Model/ListOrderChannels200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
