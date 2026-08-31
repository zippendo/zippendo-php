# Zippendo\Sdk\CarriersApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**connectCarrier()**](CarriersApi.md#connectCarrier) | **POST** /orgs/{orgId}/carriers | Connect carrier |
| [**disconnectCarrier()**](CarriersApi.md#disconnectCarrier) | **DELETE** /orgs/{orgId}/carriers/{carrierId} | Disconnect carrier |
| [**getCarrier()**](CarriersApi.md#getCarrier) | **GET** /orgs/{orgId}/carriers/{carrierId} | Get carrier |
| [**listCarrierProductServicePoints()**](CarriersApi.md#listCarrierProductServicePoints) | **POST** /orgs/{orgId}/carriers/{carrierId}/products/{productId}/service-points | List product service points |
| [**listCarrierProducts()**](CarriersApi.md#listCarrierProducts) | **GET** /orgs/{orgId}/carriers/{carrierId}/products | List carrier products |
| [**listCarriers()**](CarriersApi.md#listCarriers) | **GET** /orgs/{orgId}/carriers | List carriers |
| [**updateCarrier()**](CarriersApi.md#updateCarrier) | **PUT** /orgs/{orgId}/carriers/{carrierId} | Update carrier |


## `connectCarrier()`

```php
connectCarrier($org_id, $connect_carrier_request): \Zippendo\Sdk\Model\ListCarriers200ResponseDataInner
```

Connect carrier

Connects a new carrier to the organization with its configuration.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\CarriersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$connect_carrier_request = new \Zippendo\Sdk\Model\ConnectCarrierRequest(); // \Zippendo\Sdk\Model\ConnectCarrierRequest

try {
    $result = $apiInstance->connectCarrier($org_id, $connect_carrier_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CarriersApi->connectCarrier: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **connect_carrier_request** | [**\Zippendo\Sdk\Model\ConnectCarrierRequest**](../Model/ConnectCarrierRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\ListCarriers200ResponseDataInner**](../Model/ListCarriers200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `disconnectCarrier()`

```php
disconnectCarrier($org_id, $carrier_id): string
```

Disconnect carrier

Disconnects a carrier from the organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\CarriersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$carrier_id = carr_01HZX9K2QF; // string | Carrier ID

try {
    $result = $apiInstance->disconnectCarrier($org_id, $carrier_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CarriersApi->disconnectCarrier: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **carrier_id** | **string**| Carrier ID | |

### Return type

**string**

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getCarrier()`

```php
getCarrier($org_id, $carrier_id): \Zippendo\Sdk\Model\ListCarriers200ResponseDataInner
```

Get carrier

Returns a single connected carrier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\CarriersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$carrier_id = carr_01HZX9K2QF; // string | Carrier ID

try {
    $result = $apiInstance->getCarrier($org_id, $carrier_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CarriersApi->getCarrier: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **carrier_id** | **string**| Carrier ID | |

### Return type

[**\Zippendo\Sdk\Model\ListCarriers200ResponseDataInner**](../Model/ListCarriers200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCarrierProductServicePoints()`

```php
listCarrierProductServicePoints($org_id, $carrier_id, $product_id, $list_carrier_product_service_points_request): \Zippendo\Sdk\Model\ListCarrierProductServicePoints200ResponseInner[]
```

List product service points

Returns pickup service points near a location for a specific carrier product.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\CarriersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$carrier_id = carr_01HZX9K2QF; // string | Carrier ID
$product_id = PNL13; // string | Carrier product ID
$list_carrier_product_service_points_request = new \Zippendo\Sdk\Model\ListCarrierProductServicePointsRequest(); // \Zippendo\Sdk\Model\ListCarrierProductServicePointsRequest

try {
    $result = $apiInstance->listCarrierProductServicePoints($org_id, $carrier_id, $product_id, $list_carrier_product_service_points_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CarriersApi->listCarrierProductServicePoints: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **carrier_id** | **string**| Carrier ID | |
| **product_id** | **string**| Carrier product ID | |
| **list_carrier_product_service_points_request** | [**\Zippendo\Sdk\Model\ListCarrierProductServicePointsRequest**](../Model/ListCarrierProductServicePointsRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\ListCarrierProductServicePoints200ResponseInner[]**](../Model/ListCarrierProductServicePoints200ResponseInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCarrierProducts()`

```php
listCarrierProducts($org_id, $carrier_id): \Zippendo\Sdk\Model\ListCarrierProducts200ResponseInner[]
```

List carrier products

Returns the shipping products available for a connected carrier.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\CarriersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$carrier_id = carr_01HZX9K2QF; // string | Carrier ID

try {
    $result = $apiInstance->listCarrierProducts($org_id, $carrier_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CarriersApi->listCarrierProducts: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **carrier_id** | **string**| Carrier ID | |

### Return type

[**\Zippendo\Sdk\Model\ListCarrierProducts200ResponseInner[]**](../Model/ListCarrierProducts200ResponseInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listCarriers()`

```php
listCarriers($org_id, $page, $limit, $brand_id, $brand_scope, $carrier_slug, $search): \Zippendo\Sdk\Model\ListCarriers200Response
```

List carriers

Returns a paginated list of carriers connected to the organization.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\CarriersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$page = 1; // int | Page number (1-based)
$limit = 20; // int | Items per page (max 100)
$brand_id = brnd_8f3kd92ld0; // string | Filter by brand. Pass a brand ID, or \"none\" for records not assigned to any brand.
$brand_scope = own; // string | How the brand context narrows this list: \"own\" returns only rows assigned to the current brand (requires a brand session, a brand-bound token, or the X-Zippendo-Brand header), \"shared\" returns only unassigned organization-wide rows, \"both\" (default) returns both. The X-Zippendo-Brand-Scope header supplies a default when the parameter is omitted. For strictly brand-owned records (orders, shipments), a brand-scoped request combined with \"shared\" returns no rows, since those records are never visible organization-wide from within a brand context.
$carrier_slug = gls; // string | Filter by carrier slug.
$search = PostNord; // string | Search by carrier name.

try {
    $result = $apiInstance->listCarriers($org_id, $page, $limit, $brand_id, $brand_scope, $carrier_slug, $search);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CarriersApi->listCarriers: ', $e->getMessage(), PHP_EOL;
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
| **carrier_slug** | **string**| Filter by carrier slug. | [optional] |
| **search** | **string**| Search by carrier name. | [optional] |

### Return type

[**\Zippendo\Sdk\Model\ListCarriers200Response**](../Model/ListCarriers200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateCarrier()`

```php
updateCarrier($org_id, $carrier_id, $update_carrier_request): \Zippendo\Sdk\Model\ListCarriers200ResponseDataInner
```

Update carrier

Updates a connected carrier's configuration or name.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\CarriersApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_01HZX9K2QF; // string | Organization ID
$carrier_id = carr_01HZX9K2QF; // string | Carrier ID
$update_carrier_request = new \Zippendo\Sdk\Model\UpdateCarrierRequest(); // \Zippendo\Sdk\Model\UpdateCarrierRequest

try {
    $result = $apiInstance->updateCarrier($org_id, $carrier_id, $update_carrier_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling CarriersApi->updateCarrier: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **carrier_id** | **string**| Carrier ID | |
| **update_carrier_request** | [**\Zippendo\Sdk\Model\UpdateCarrierRequest**](../Model/UpdateCarrierRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\ListCarriers200ResponseDataInner**](../Model/ListCarriers200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
