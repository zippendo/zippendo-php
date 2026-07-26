# Zippendo\Sdk\OrgsApi



All URIs are relative to https://api.zippendo.com, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**deleteOrgLogo()**](OrgsApi.md#deleteOrgLogo) | **DELETE** /orgs/{orgId}/branding/logo | Delete org logo |
| [**getOrg()**](OrgsApi.md#getOrg) | **GET** /orgs/{id} | Get org |
| [**getOrgBranding()**](OrgsApi.md#getOrgBranding) | **GET** /orgs/{orgId}/branding | Get org branding |
| [**getOrgLogo()**](OrgsApi.md#getOrgLogo) | **GET** /orgs/{orgId}/branding/logo | Download org logo |
| [**updateOrg()**](OrgsApi.md#updateOrg) | **PUT** /orgs/{id} | Update org |
| [**updateOrgBranding()**](OrgsApi.md#updateOrgBranding) | **PUT** /orgs/{orgId}/branding | Update org branding |
| [**uploadOrgLogo()**](OrgsApi.md#uploadOrgLogo) | **POST** /orgs/{orgId}/branding/logo | Upload org logo |


## `deleteOrgLogo()`

```php
deleteOrgLogo($org_id): \Zippendo\Sdk\Model\GetOrgBranding200Response
```

Delete org logo

Removes the org logo. Requires the customBranding entitlement.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrgsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID

try {
    $result = $apiInstance->deleteOrgLogo($org_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrgsApi->deleteOrgLogo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |

### Return type

[**\Zippendo\Sdk\Model\GetOrgBranding200Response**](../Model/GetOrgBranding200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrg()`

```php
getOrg($id): \Zippendo\Sdk\Model\GetOrg200Response
```

Get org

Returns a specific organization by ID, including its member count.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrgsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = clz9x8a7b0001; // string | Resource ID

try {
    $result = $apiInstance->getOrg($id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrgsApi->getOrg: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Resource ID | |

### Return type

[**\Zippendo\Sdk\Model\GetOrg200Response**](../Model/GetOrg200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrgBranding()`

```php
getOrgBranding($org_id): \Zippendo\Sdk\Model\GetOrgBranding200Response
```

Get org branding

Returns the org's brand colors and an authenticated URL to download the logo.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrgsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID

try {
    $result = $apiInstance->getOrgBranding($org_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrgsApi->getOrgBranding: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |

### Return type

[**\Zippendo\Sdk\Model\GetOrgBranding200Response**](../Model/GetOrgBranding200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `getOrgLogo()`

```php
getOrgLogo($org_id): \SplFileObject
```

Download org logo

Returns the org logo image bytes with the stored content type.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrgsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID

try {
    $result = $apiInstance->getOrgLogo($org_id);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrgsApi->getOrgLogo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |

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

## `updateOrg()`

```php
updateOrg($id, $update_org_request): \Zippendo\Sdk\Model\UpdateOrg200Response
```

Update org

Updates an existing organization's profile, billing, and customs settings.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrgsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$id = clz9x8a7b0001; // string | Resource ID
$update_org_request = new \Zippendo\Sdk\Model\UpdateOrgRequest(); // \Zippendo\Sdk\Model\UpdateOrgRequest

try {
    $result = $apiInstance->updateOrg($id, $update_org_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrgsApi->updateOrg: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **id** | **string**| Resource ID | |
| **update_org_request** | [**\Zippendo\Sdk\Model\UpdateOrgRequest**](../Model/UpdateOrgRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\UpdateOrg200Response**](../Model/UpdateOrg200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `updateOrgBranding()`

```php
updateOrgBranding($org_id, $update_org_branding_request): \Zippendo\Sdk\Model\GetOrgBranding200Response
```

Update org branding

Sets the org brand colors. Requires the customBranding entitlement.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrgsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$update_org_branding_request = new \Zippendo\Sdk\Model\UpdateOrgBrandingRequest(); // \Zippendo\Sdk\Model\UpdateOrgBrandingRequest

try {
    $result = $apiInstance->updateOrgBranding($org_id, $update_org_branding_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrgsApi->updateOrgBranding: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **update_org_branding_request** | [**\Zippendo\Sdk\Model\UpdateOrgBrandingRequest**](../Model/UpdateOrgBrandingRequest.md)|  | |

### Return type

[**\Zippendo\Sdk\Model\GetOrgBranding200Response**](../Model/GetOrgBranding200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `uploadOrgLogo()`

```php
uploadOrgLogo($org_id, $file): \Zippendo\Sdk\Model\GetOrgBranding200Response
```

Upload org logo

Uploads the org logo as multipart/form-data. Accepts PNG, JPG, or WEBP up to 5MB and 4096×4096px; the image is re-encoded and stored. Requires the customBranding entitlement.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure Bearer (JWT) authorization: bearerAuth
$config = Zippendo\Sdk\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new Zippendo\Sdk\Api\OrgsApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$org_id = org_8f3kd92ld0; // string | Organization ID
$file = '/path/to/file.txt'; // \SplFileObject | Image file (PNG, JPG, or WEBP)

try {
    $result = $apiInstance->uploadOrgLogo($org_id, $file);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OrgsApi->uploadOrgLogo: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **org_id** | **string**| Organization ID | |
| **file** | **\SplFileObject****\SplFileObject**| Image file (PNG, JPG, or WEBP) | |

### Return type

[**\Zippendo\Sdk\Model\GetOrgBranding200Response**](../Model/GetOrgBranding200Response.md)

### Authorization

[bearerAuth](../../README.md#bearerAuth)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
