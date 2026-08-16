# Zippendo\Sdk\ShipmentsApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**batchSendShipments()**](ShipmentsApi.md#batchSendShipments) | **POST** /orgs/{orgId}/shipments/batch-send | Batch send shipments |
| [**batchSplitShipment()**](ShipmentsApi.md#batchSplitShipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/batch-split-shipment | Batch split shipment |
| [**createReturnShipment()**](ShipmentsApi.md#createReturnShipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/create-return | Create return shipment |
| [**createShipment()**](ShipmentsApi.md#createShipment) | **POST** /orgs/{orgId}/shipments | Create shipment |
| [**deleteShipment()**](ShipmentsApi.md#deleteShipment) | **DELETE** /orgs/{orgId}/shipments/{shipmentId} | Delete shipment |
| [**getShipment()**](ShipmentsApi.md#getShipment) | **GET** /orgs/{orgId}/shipments/{shipmentId} | Get shipment |
| [**getShipmentDocumentContent()**](ShipmentsApi.md#getShipmentDocumentContent) | **GET** /orgs/{orgId}/shipments/{shipmentId}/documents/{documentId}/content | Download shipment document |
| [**listShipments()**](ShipmentsApi.md#listShipments) | **GET** /orgs/{orgId}/shipments | List shipments |
| [**sendShipment()**](ShipmentsApi.md#sendShipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/send | Send shipment |
| [**splitShipment()**](ShipmentsApi.md#splitShipment) | **POST** /orgs/{orgId}/shipments/{shipmentId}/split-shipment | Split shipment |
| [**splitShipmentParcel()**](ShipmentsApi.md#splitShipmentParcel) | **POST** /orgs/{orgId}/shipments/{shipmentId}/split-parcel | Split parcels |
| [**trackShipment()**](ShipmentsApi.md#trackShipment) | **GET** /orgs/{orgId}/shipments/{shipmentId}/tracking | Get shipment tracking |
| [**updateShipment()**](ShipmentsApi.md#updateShipment) | **PATCH** /orgs/{orgId}/shipments/{shipmentId} | Update shipment |


## `batchSendShipments()`

```php
batchSendShipments($org_id, $batch_send_shipments_request): \Zippendo\Sdk\Model\BatchSendShipments200Response
```

Batch send shipments

Book multiple pending/error shipments with their carriers in one request. Each shipment is processed independently and reported in `results`; a failure on one shipment never aborts the others. Use it to send every shipment on an order at once.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$batch_send_shipments_request = new \Zippendo\Sdk\Model\BatchSendShipmentsRequest(); // \Zippendo\Sdk\Model\BatchSendShipmentsRequest

try {
    $result = $apiInstance->batchSendShipments($org_id, $batch_send_shipments_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->batchSendShipments: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **batch_send_shipments_request** | [**\Zippendo\Sdk\Model\BatchSendShipmentsRequest**](../Model/BatchSendShipmentsRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\BatchSendShipments200Response**](../Model/BatchSendShipments200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `batchSplitShipment()`

```php
batchSplitShipment($org_id, $shipment_id, $batch_split_shipment_request): \Zippendo\Sdk\Model\BatchSplitShipment201Response
```

Batch split shipment

Split a parcel into multiple new shipments with per-line quantities in a single atomic operation. Only draft or pending shipments can be split.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_1a2b3c4d; // string | Organization identifier.
$shipment_id = shp_4d9e7a2f; // string | Shipment identifier.
$batch_split_shipment_request = new \Zippendo\Sdk\Model\BatchSplitShipmentRequest(); // \Zippendo\Sdk\Model\BatchSplitShipmentRequest

try {
    $result = $apiInstance->batchSplitShipment($org_id, $shipment_id, $batch_split_shipment_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->batchSplitShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization identifier. | |
| **shipment_id** | **string**| Shipment identifier. | |
| **batch_split_shipment_request** | [**\Zippendo\Sdk\Model\BatchSplitShipmentRequest**](../Model/BatchSplitShipmentRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\BatchSplitShipment201Response**](../Model/BatchSplitShipment201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createReturnShipment()`

```php
createReturnShipment($org_id, $shipment_id): \Zippendo\Sdk\Model\CreateShipment201Response
```

Create return shipment

Create and auto-send a return shipment from a dispatched outbound shipment with swapped sender/receiver. Requires a configured return shipping rule.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_1a2b3c4d; // string | Organization identifier.
$shipment_id = shp_4d9e7a2f; // string | Shipment identifier.

try {
    $result = $apiInstance->createReturnShipment($org_id, $shipment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->createReturnShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization identifier. | |
| **shipment_id** | **string**| Shipment identifier. | |

### Return type

[**\Zippendo\Sdk\Model\CreateShipment201Response**](../Model/CreateShipment201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createShipment()`

```php
createShipment($org_id, $create_shipment_request): \Zippendo\Sdk\Model\CreateShipment201Response
```

Create shipment

Create a new shipment for an organization. When orderId is provided, parties and parcels are derived from the order.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$create_shipment_request = new \Zippendo\Sdk\Model\CreateShipmentRequest(); // \Zippendo\Sdk\Model\CreateShipmentRequest

try {
    $result = $apiInstance->createShipment($org_id, $create_shipment_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->createShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **create_shipment_request** | [**\Zippendo\Sdk\Model\CreateShipmentRequest**](../Model/CreateShipmentRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\CreateShipment201Response**](../Model/CreateShipment201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteShipment()`

```php
deleteShipment($org_id, $shipment_id): \Zippendo\Sdk\Model\RevokeApiToken200Response
```

Delete shipment

Delete a shipment. Only shipments in pending status can be deleted.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_1a2b3c4d; // string | Organization identifier.
$shipment_id = shp_4d9e7a2f; // string | Shipment identifier.

try {
    $result = $apiInstance->deleteShipment($org_id, $shipment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->deleteShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization identifier. | |
| **shipment_id** | **string**| Shipment identifier. | |

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

## `getShipment()`

```php
getShipment($org_id, $shipment_id): \Zippendo\Sdk\Model\CreateShipment201Response
```

Get shipment

Retrieve a single shipment by its ID, including parcels, parties, documents and activity.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_1a2b3c4d; // string | Organization identifier.
$shipment_id = shp_4d9e7a2f; // string | Shipment identifier.

try {
    $result = $apiInstance->getShipment($org_id, $shipment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->getShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization identifier. | |
| **shipment_id** | **string**| Shipment identifier. | |

### Return type

[**\Zippendo\Sdk\Model\CreateShipment201Response**](../Model/CreateShipment201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getShipmentDocumentContent()`

```php
getShipmentDocumentContent($org_id, $shipment_id, $document_id, $disposition, $filename)
```

Download shipment document

Streams a shipment document or label file from storage.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_1a2b3c4d; // string | Organization identifier.
$shipment_id = shp_4d9e7a2f; // string | Shipment identifier.
$document_id = doc_8f3a2b1c; // string | Document identifier.
$disposition = inline; // string | Render the document inline (default) or force a download.
$filename = label; // string | Suggested filename (without extension) for attachment downloads.

try {
    $apiInstance->getShipmentDocumentContent($org_id, $shipment_id, $document_id, $disposition, $filename);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->getShipmentDocumentContent: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization identifier. | |
| **shipment_id** | **string**| Shipment identifier. | |
| **document_id** | **string**| Document identifier. | |
| **disposition** | **string**| Render the document inline (default) or force a download. | [optional] [default to &#39;inline&#39;] |
| **filename** | **string**| Suggested filename (without extension) for attachment downloads. | [optional] |

### Return type

void (empty response body)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: Not defined

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listShipments()`

```php
listShipments($org_id, $page, $limit, $brand_id, $brand_scope): \Zippendo\Sdk\Model\ListShipments200Response
```

List shipments

List all shipments for an organization, paginated and ordered by newest first.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
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

try {
    $result = $apiInstance->listShipments($org_id, $page, $limit, $brand_id, $brand_scope);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->listShipments: ', $e->getMessage(), PHP_EOL;
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

### Return type

[**\Zippendo\Sdk\Model\ListShipments200Response**](../Model/ListShipments200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `sendShipment()`

```php
sendShipment($org_id, $shipment_id): \Zippendo\Sdk\Model\CreateShipment201Response
```

Send shipment

Book a pending or error shipment with the carrier, generating labels and tracking. Returns 422 with carrier errors if booking fails.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_1a2b3c4d; // string | Organization identifier.
$shipment_id = shp_4d9e7a2f; // string | Shipment identifier.

try {
    $result = $apiInstance->sendShipment($org_id, $shipment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->sendShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization identifier. | |
| **shipment_id** | **string**| Shipment identifier. | |

### Return type

[**\Zippendo\Sdk\Model\CreateShipment201Response**](../Model/CreateShipment201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `splitShipment()`

```php
splitShipment($org_id, $shipment_id, $split_shipment_request): \Zippendo\Sdk\Model\SplitShipment201Response
```

Split shipment

Move order lines from a parcel into a new shipment. Only draft or pending shipments can be split.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_1a2b3c4d; // string | Organization identifier.
$shipment_id = shp_4d9e7a2f; // string | Shipment identifier.
$split_shipment_request = new \Zippendo\Sdk\Model\SplitShipmentRequest(); // \Zippendo\Sdk\Model\SplitShipmentRequest

try {
    $result = $apiInstance->splitShipment($org_id, $shipment_id, $split_shipment_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->splitShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization identifier. | |
| **shipment_id** | **string**| Shipment identifier. | |
| **split_shipment_request** | [**\Zippendo\Sdk\Model\SplitShipmentRequest**](../Model/SplitShipmentRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\SplitShipment201Response**](../Model/SplitShipment201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `splitShipmentParcel()`

```php
splitShipmentParcel($org_id, $shipment_id, $split_shipment_parcel_request): \Zippendo\Sdk\Model\SplitShipmentParcel200Response
```

Split parcels

Redistribute order lines across parcels within a shipment, moving lines between parcels and creating new ones. Only draft, pending or error shipments can be modified.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_1a2b3c4d; // string | Organization identifier.
$shipment_id = shp_4d9e7a2f; // string | Shipment identifier.
$split_shipment_parcel_request = new \Zippendo\Sdk\Model\SplitShipmentParcelRequest(); // \Zippendo\Sdk\Model\SplitShipmentParcelRequest

try {
    $result = $apiInstance->splitShipmentParcel($org_id, $shipment_id, $split_shipment_parcel_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->splitShipmentParcel: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization identifier. | |
| **shipment_id** | **string**| Shipment identifier. | |
| **split_shipment_parcel_request** | [**\Zippendo\Sdk\Model\SplitShipmentParcelRequest**](../Model/SplitShipmentParcelRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\SplitShipmentParcel200Response**](../Model/SplitShipmentParcel200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `trackShipment()`

```php
trackShipment($org_id, $shipment_id): \Zippendo\Sdk\Model\TrackShipment200Response
```

Get shipment tracking

Retrieve the tracking timeline for a shipment, including current status and all carrier events.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_1a2b3c4d; // string | Organization identifier.
$shipment_id = shp_4d9e7a2f; // string | Shipment identifier.

try {
    $result = $apiInstance->trackShipment($org_id, $shipment_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->trackShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization identifier. | |
| **shipment_id** | **string**| Shipment identifier. | |

### Return type

[**\Zippendo\Sdk\Model\TrackShipment200Response**](../Model/TrackShipment200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateShipment()`

```php
updateShipment($org_id, $shipment_id, $update_shipment_request): \Zippendo\Sdk\Model\CreateShipment201Response
```

Update shipment

Update an existing shipment. Only draft, pending or error shipments can be updated; an applied shipping rule overrides carrier settings and sender party.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\ShipmentsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_1a2b3c4d; // string | Organization identifier.
$shipment_id = shp_4d9e7a2f; // string | Shipment identifier.
$update_shipment_request = new \Zippendo\Sdk\Model\UpdateShipmentRequest(); // \Zippendo\Sdk\Model\UpdateShipmentRequest

try {
    $result = $apiInstance->updateShipment($org_id, $shipment_id, $update_shipment_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling ShipmentsApi->updateShipment: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization identifier. | |
| **shipment_id** | **string**| Shipment identifier. | |
| **update_shipment_request** | [**\Zippendo\Sdk\Model\UpdateShipmentRequest**](../Model/UpdateShipmentRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\CreateShipment201Response**](../Model/CreateShipment201Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
