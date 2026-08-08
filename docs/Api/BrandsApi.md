# Zippendo\Sdk\BrandsApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**archiveOrgBrand()**](BrandsApi.md#archiveOrgBrand) | **POST** /orgs/{orgId}/brands/{brandId}/archive | Archive brand |
| [**checkBrandSlug()**](BrandsApi.md#checkBrandSlug) | **GET** /orgs/{orgId}/brands/check-slug/{slug} | Check brand slug availability |
| [**createOrgBrand()**](BrandsApi.md#createOrgBrand) | **POST** /orgs/{orgId}/brands | Create brand |
| [**deleteBrandLogo()**](BrandsApi.md#deleteBrandLogo) | **DELETE** /orgs/{orgId}/brands/{brandId}/logo | Delete brand logo |
| [**getBrandLogo()**](BrandsApi.md#getBrandLogo) | **GET** /orgs/{orgId}/brands/{brandId}/logo | Get brand logo |
| [**getOrgBrand()**](BrandsApi.md#getOrgBrand) | **GET** /orgs/{orgId}/brands/{brandId} | Get brand |
| [**listOrgBrands()**](BrandsApi.md#listOrgBrands) | **GET** /orgs/{orgId}/brands | List brands |
| [**unarchiveOrgBrand()**](BrandsApi.md#unarchiveOrgBrand) | **POST** /orgs/{orgId}/brands/{brandId}/unarchive | Unarchive brand |
| [**updateOrgBrand()**](BrandsApi.md#updateOrgBrand) | **PATCH** /orgs/{orgId}/brands/{brandId} | Update brand |
| [**uploadBrandLogo()**](BrandsApi.md#uploadBrandLogo) | **POST** /orgs/{orgId}/brands/{brandId}/logo | Upload brand logo |


## `archiveOrgBrand()`

```php
archiveOrgBrand($org_id, $brand_id): \Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner
```

Archive brand

Archives a brand: it leaves the brand switcher and default listings, but its orders, shipments and settings are retained and remain visible in the organization-wide view.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\BrandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$brand_id = brnd_8f3kd92ld0; // string | Brand ID

try {
    $result = $apiInstance->archiveOrgBrand($org_id, $brand_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandsApi->archiveOrgBrand: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **brand_id** | **string**| Brand ID | |

### Return type

[**\Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner**](../Model/ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `checkBrandSlug()`

```php
checkBrandSlug($org_id, $slug): \Zippendo\Sdk\Model\CheckBrandSlug200Response
```

Check brand slug availability

Reports whether a brand slug is free within this organization. Brand slugs are unique per organization, so the same slug may exist in another organization. Archived brands still hold their slug.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\BrandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$slug = acme; // string | Brand slug to check

try {
    $result = $apiInstance->checkBrandSlug($org_id, $slug);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandsApi->checkBrandSlug: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **slug** | **string**| Brand slug to check | |

### Return type

[**\Zippendo\Sdk\Model\CheckBrandSlug200Response**](../Model/CheckBrandSlug200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `createOrgBrand()`

```php
createOrgBrand($org_id, $create_org_brand_request): \Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner
```

Create brand

Creates a brand (sub-account) in the organization. The slug is derived from the name when omitted. Requires a plan that includes brands.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\BrandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$create_org_brand_request = new \Zippendo\Sdk\Model\CreateOrgBrandRequest(); // \Zippendo\Sdk\Model\CreateOrgBrandRequest

try {
    $result = $apiInstance->createOrgBrand($org_id, $create_org_brand_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandsApi->createOrgBrand: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **create_org_brand_request** | [**\Zippendo\Sdk\Model\CreateOrgBrandRequest**](../Model/CreateOrgBrandRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner**](../Model/ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `deleteBrandLogo()`

```php
deleteBrandLogo($org_id, $brand_id): \Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner
```

Delete brand logo

Removes a brand's logo. Its documents fall back to the organization's logo. Requires the brands and customBranding entitlements.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\BrandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$brand_id = brnd_8f3kd92ld0; // string | Brand ID

try {
    $result = $apiInstance->deleteBrandLogo($org_id, $brand_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandsApi->deleteBrandLogo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **brand_id** | **string**| Brand ID | |

### Return type

[**\Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner**](../Model/ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getBrandLogo()`

```php
getBrandLogo($org_id, $brand_id): \SplFileObject
```

Get brand logo

Streams the brand's logo bytes. This is the URL returned as the brand's `logoUrl`.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\BrandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$brand_id = brnd_8f3kd92ld0; // string | Brand ID

try {
    $result = $apiInstance->getBrandLogo($org_id, $brand_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandsApi->getBrandLogo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **brand_id** | **string**| Brand ID | |

### Return type

**\SplFileObject**

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `image/png`, `image/jpeg`, `image/webp`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrgBrand()`

```php
getOrgBrand($org_id, $brand_id): \Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner
```

Get brand

Returns a single brand (sub-account) by id.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\BrandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$brand_id = brnd_8f3kd92ld0; // string | Brand ID

try {
    $result = $apiInstance->getOrgBrand($org_id, $brand_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandsApi->getOrgBrand: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **brand_id** | **string**| Brand ID | |

### Return type

[**\Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner**](../Model/ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `listOrgBrands()`

```php
listOrgBrands($org_id, $include_archived): \Zippendo\Sdk\Model\ListOrgBrands200Response
```

List brands

Returns the organization's brands (sub-accounts). Archived brands are excluded unless `includeArchived` is set.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\BrandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$include_archived = false; // string | Include archived brands in the response

try {
    $result = $apiInstance->listOrgBrands($org_id, $include_archived);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandsApi->listOrgBrands: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **include_archived** | **string**| Include archived brands in the response | [optional] |

### Return type

[**\Zippendo\Sdk\Model\ListOrgBrands200Response**](../Model/ListOrgBrands200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `unarchiveOrgBrand()`

```php
unarchiveOrgBrand($org_id, $brand_id): \Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner
```

Unarchive brand

Restores an archived brand so it appears in the brand switcher again.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\BrandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$brand_id = brnd_8f3kd92ld0; // string | Brand ID

try {
    $result = $apiInstance->unarchiveOrgBrand($org_id, $brand_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandsApi->unarchiveOrgBrand: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **brand_id** | **string**| Brand ID | |

### Return type

[**\Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner**](../Model/ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateOrgBrand()`

```php
updateOrgBrand($org_id, $brand_id, $update_org_brand_request): \Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner
```

Update brand

Updates a brand's name, slug, identity overrides (company name, VAT, customs, address) and document colours. Null clears an override so the organization's value applies again.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\BrandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$brand_id = brnd_8f3kd92ld0; // string | Brand ID
$update_org_brand_request = new \Zippendo\Sdk\Model\UpdateOrgBrandRequest(); // \Zippendo\Sdk\Model\UpdateOrgBrandRequest

try {
    $result = $apiInstance->updateOrgBrand($org_id, $brand_id, $update_org_brand_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandsApi->updateOrgBrand: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **brand_id** | **string**| Brand ID | |
| **update_org_brand_request** | [**\Zippendo\Sdk\Model\UpdateOrgBrandRequest**](../Model/UpdateOrgBrandRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner**](../Model/ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadBrandLogo()`

```php
uploadBrandLogo($org_id, $brand_id, $file): \Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner
```

Upload brand logo

Uploads a brand's logo as multipart/form-data. Accepts PNG, JPG or WEBP up to 5MB and 4096×4096px; the image is re-encoded and stored. Documents for this brand's shipments use it instead of the organization's logo. Requires the brands and customBranding entitlements.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\BrandsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$brand_id = brnd_8f3kd92ld0; // string | Brand ID
$file = '/path/to/file.txt'; // \SplFileObject | Image file (PNG, JPG, or WEBP)

try {
    $result = $apiInstance->uploadBrandLogo($org_id, $brand_id, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BrandsApi->uploadBrandLogo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **brand_id** | **string**| Brand ID | |
| **file** | **\SplFileObject****\SplFileObject**| Image file (PNG, JPG, or WEBP) | |

### Return type

[**\Zippendo\Sdk\Model\ListOrgBrands200ResponseDataInner**](../Model/ListOrgBrands200ResponseDataInner.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
