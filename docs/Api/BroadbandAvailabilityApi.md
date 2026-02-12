# OpenAPI\Client\BroadbandAvailabilityApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**broadbandAvailabilityInputGet()**](BroadbandAvailabilityApi.md#broadbandAvailabilityInputGet) | **GET** /broadband/availability/{input} | Search for your phone number, access line ID or postcode and return a list of  available broadband products with the speeds available. |
| [**broadbandAvailabilityPost()**](BroadbandAvailabilityApi.md#broadbandAvailabilityPost) | **POST** /broadband/availability | Search with your exact BT address match and return a list of available broadband products with the speeds available |
| [**broadbandAvailabilityUprnInputGet()**](BroadbandAvailabilityApi.md#broadbandAvailabilityUprnInputGet) | **GET** /broadband/availability/uprn/{input} | Search with a UPRN and return a list of available broadband products with the speeds available. |


## `broadbandAvailabilityInputGet()`

```php
broadbandAvailabilityInputGet($input, $api_platform): \OpenAPI\Client\Model\BroadbandAvailabilityResults
```

Search for your phone number, access line ID or postcode and return a list of  available broadband products with the speeds available.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandAvailabilityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$input = 'input_example'; // string | Phone number, Access Line ID or postcode
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandAvailabilityInputGet($input, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandAvailabilityApi->broadbandAvailabilityInputGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **input** | **string**| Phone number, Access Line ID or postcode | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandAvailabilityResults**](../Model/BroadbandAvailabilityResults.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandAvailabilityPost()`

```php
broadbandAvailabilityPost($api_platform, $broadband_address): \OpenAPI\Client\Model\BroadbandAvailabilityResults
```

Search with your exact BT address match and return a list of available broadband products with the speeds available

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandAvailabilityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.
$broadband_address = new \OpenAPI\Client\Model\BroadbandAddress(); // \OpenAPI\Client\Model\BroadbandAddress | BroadbandAddress struct

try {
    $result = $apiInstance->broadbandAvailabilityPost($api_platform, $broadband_address);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandAvailabilityApi->broadbandAvailabilityPost: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |
| **broadband_address** | [**\OpenAPI\Client\Model\BroadbandAddress**](../Model/BroadbandAddress.md)| BroadbandAddress struct | [optional] |

### Return type

[**\OpenAPI\Client\Model\BroadbandAvailabilityResults**](../Model/BroadbandAvailabilityResults.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandAvailabilityUprnInputGet()`

```php
broadbandAvailabilityUprnInputGet($input, $api_platform): \OpenAPI\Client\Model\BroadbandAvailabilityResults
```

Search with a UPRN and return a list of available broadband products with the speeds available.

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandAvailabilityApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$input = 'input_example'; // string | UPRN
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandAvailabilityUprnInputGet($input, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandAvailabilityApi->broadbandAvailabilityUprnInputGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **input** | **string**| UPRN | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandAvailabilityResults**](../Model/BroadbandAvailabilityResults.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
