# Zippendo\Sdk\OrdersApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**createOrder()**](OrdersApi.md#createOrder) | **POST** /orgs/{orgId}/orders | Create order |
| [**deleteOrder()**](OrdersApi.md#deleteOrder) | **DELETE** /orgs/{orgId}/orders/{orderId} | Delete order |
| [**getOrder()**](OrdersApi.md#getOrder) | **GET** /orgs/{orgId}/orders/{orderId} | Get order |
| [**listOrders()**](OrdersApi.md#listOrders) | **GET** /orgs/{orgId}/orders | List orders |
| [**updateOrder()**](OrdersApi.md#updateOrder) | **PATCH** /orgs/{orgId}/orders/{orderId} | Update order |


## `createOrder()`

```php
createOrder($org_id, $create_order_request): \Zippendo\Sdk\Model\CreateOrder201Response
```

Create order

Creates a new order under an existing order channel for the organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$create_order_request = new \Zippendo\Sdk\Model\CreateOrderRequest(); // \Zippendo\Sdk\Model\CreateOrderRequest

try {
    $result = $apiInstance->createOrder($org_id, $create_order_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->createOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **create_order_request** | [**\Zippendo\Sdk\Model\CreateOrderRequest**](../Model/CreateOrderRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\CreateOrder201Response**](../Model/CreateOrder201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteOrder()`

```php
deleteOrder($org_id, $order_id): \Zippendo\Sdk\Model\RevokeApiToken200Response
```

Delete order

Deletes an order. Fails if the order has associated shipments.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = clz9k2f0a0000abcd0000zzzz; // string | Organization ID.
$order_id = clz9k2f0a0003abcd9012mnop; // string | Order ID.

try {
    $result = $apiInstance->deleteOrder($org_id, $order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->deleteOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID. | |
| **order_id** | **string**| Order ID. | |

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

## `getOrder()`

```php
getOrder($org_id, $order_id): \Zippendo\Sdk\Model\GetOrder200Response
```

Get order

Returns a single order with its channel, shipping rule, shipments, and documents.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = clz9k2f0a0000abcd0000zzzz; // string | Organization ID.
$order_id = clz9k2f0a0003abcd9012mnop; // string | Order ID.

try {
    $result = $apiInstance->getOrder($org_id, $order_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->getOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID. | |
| **order_id** | **string**| Order ID. | |

### Return type

[**\Zippendo\Sdk\Model\GetOrder200Response**](../Model/GetOrder200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listOrders()`

```php
listOrders($org_id, $page, $limit, $brand_id, $status, $order_channel_id, $search): \Zippendo\Sdk\Model\ListOrders200Response
```

List orders

Returns a paginated list of orders for an organization, filterable by status, channel, and search term.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$page = 1; // int | Page number (1-based)
$limit = 20; // int | Items per page (max 100)
$brand_id = brnd_8f3kd92ld0; // string | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
$status = processing; // string | Order fulfilment status derived from its shipments.
$order_channel_id = clz9k2f0a0001abcd1234efgh; // string | Filter by order channel ID.
$search = Anna; // string | Search by order number or customer name/email.

try {
    $result = $apiInstance->listOrders($org_id, $page, $limit, $brand_id, $status, $order_channel_id, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->listOrders: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **page** | **int**| Page number (1-based) | [optional] [default to 1] |
| **limit** | **int**| Items per page (max 100) | [optional] [default to 20] |
| **brand_id** | **string**| Filter by brand. Pass a brand ID, or \&quot;none\&quot; for records not assigned to any brand. | [optional] |
| **status** | **string**| Order fulfilment status derived from its shipments. | [optional] |
| **order_channel_id** | **string**| Filter by order channel ID. | [optional] |
| **search** | **string**| Search by order number or customer name/email. | [optional] |

### Return type

[**\Zippendo\Sdk\Model\ListOrders200Response**](../Model/ListOrders200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateOrder()`

```php
updateOrder($org_id, $order_id, $update_order_request): \Zippendo\Sdk\Model\CreateOrder201Response
```

Update order

Updates an order that is not yet fulfilled or cancelled.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrdersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = clz9k2f0a0000abcd0000zzzz; // string | Organization ID.
$order_id = clz9k2f0a0003abcd9012mnop; // string | Order ID.
$update_order_request = new \Zippendo\Sdk\Model\UpdateOrderRequest(); // \Zippendo\Sdk\Model\UpdateOrderRequest

try {
    $result = $apiInstance->updateOrder($org_id, $order_id, $update_order_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrdersApi->updateOrder: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID. | |
| **order_id** | **string**| Order ID. | |
| **update_order_request** | [**\Zippendo\Sdk\Model\UpdateOrderRequest**](../Model/UpdateOrderRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\CreateOrder201Response**](../Model/CreateOrder201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
