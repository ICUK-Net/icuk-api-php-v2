# OpenAPI\Client\BroadbandTroubleshootingApi



All URIs are relative to http://localhost, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**broadbandDlmResetPut()**](BroadbandTroubleshootingApi.md#broadbandDlmResetPut) | **PUT** /broadband/dlm/reset | Perform a DLM reset on a connection |
| [**broadbandDlmResetResultsUsernameGet()**](BroadbandTroubleshootingApi.md#broadbandDlmResetResultsUsernameGet) | **GET** /broadband/dlm/reset/results/{username} | Obtain results from the DLM reset tool. Returns the latest results, if no ID is specified |
| [**broadbandDlmResetResultsUsernameIdGet()**](BroadbandTroubleshootingApi.md#broadbandDlmResetResultsUsernameIdGet) | **GET** /broadband/dlm/reset/results/{username}/{id} | Obtain results from the DLM reset tool. Returns the latest results, if no ID is specified |
| [**broadbandInterleavingCurrentUsernameGet()**](BroadbandTroubleshootingApi.md#broadbandInterleavingCurrentUsernameGet) | **GET** /broadband/interleaving/current/{username} | Retrieves the current interleaving option. Only available for users with BT Wholesale products |
| [**broadbandInterleavingPut()**](BroadbandTroubleshootingApi.md#broadbandInterleavingPut) | **PUT** /broadband/interleaving | Updates the interleaving profile. Only available for users with BT Wholesale broadband products |
| [**broadbandPortFlexPut()**](BroadbandTroubleshootingApi.md#broadbandPortFlexPut) | **PUT** /broadband/port/flex | Perform a port flex on a connection |
| [**broadbandPortFlexResultsUsernameGet()**](BroadbandTroubleshootingApi.md#broadbandPortFlexResultsUsernameGet) | **GET** /broadband/port/flex/results/{username} | Obtain results from the port flex tool. Returns the latest results, if no ID is specified |
| [**broadbandPortFlexResultsUsernameIdGet()**](BroadbandTroubleshootingApi.md#broadbandPortFlexResultsUsernameIdGet) | **GET** /broadband/port/flex/results/{username}/{id} | Obtain results from the port flex tool. Returns the latest results, if no ID is specified |
| [**broadbandPortRebuildPut()**](BroadbandTroubleshootingApi.md#broadbandPortRebuildPut) | **PUT** /broadband/port/rebuild | Perform a port rebuild on a connection |
| [**broadbandPortRebuildResultsUsernameGet()**](BroadbandTroubleshootingApi.md#broadbandPortRebuildResultsUsernameGet) | **GET** /broadband/port/rebuild/results/{username} | Obtain results from the port rebuild tool. Returns the latest results, if no ID is specified |
| [**broadbandPortRebuildResultsUsernameIdGet()**](BroadbandTroubleshootingApi.md#broadbandPortRebuildResultsUsernameIdGet) | **GET** /broadband/port/rebuild/results/{username}/{id} | Obtain results from the port rebuild tool. Returns the latest results, if no ID is specified |
| [**broadbandPortResetPut()**](BroadbandTroubleshootingApi.md#broadbandPortResetPut) | **PUT** /broadband/port/reset | Perform a port reset on a connection |
| [**broadbandPortResetResultsUsernameGet()**](BroadbandTroubleshootingApi.md#broadbandPortResetResultsUsernameGet) | **GET** /broadband/port/reset/results/{username} | Obtain results from the port reset tool. Returns the latest results, if no ID is specified |
| [**broadbandPortResetResultsUsernameIdGet()**](BroadbandTroubleshootingApi.md#broadbandPortResetResultsUsernameIdGet) | **GET** /broadband/port/reset/results/{username}/{id} | Obtain results from the port reset tool. Returns the latest results, if no ID is specified |
| [**broadbandProfileCurrentUsernameGet()**](BroadbandTroubleshootingApi.md#broadbandProfileCurrentUsernameGet) | **GET** /broadband/profile/current/{username} | Gets the current SNR and interleaving profile. Only available for users with TalkTalk products |
| [**broadbandProfilePut()**](BroadbandTroubleshootingApi.md#broadbandProfilePut) | **PUT** /broadband/profile | Updates SNR and interleaving profile. Only available for users with TalkTalk products |
| [**broadbandSessionKillPut()**](BroadbandTroubleshootingApi.md#broadbandSessionKillPut) | **PUT** /broadband/session_kill | Perform a session kill on a connection |
| [**broadbandSessionKillResultsUsernameGet()**](BroadbandTroubleshootingApi.md#broadbandSessionKillResultsUsernameGet) | **GET** /broadband/session_kill/results/{username} | Obtain results from the session kill tool. Returns the latest results, if no ID is specified |
| [**broadbandSessionKillResultsUsernameIdGet()**](BroadbandTroubleshootingApi.md#broadbandSessionKillResultsUsernameIdGet) | **GET** /broadband/session_kill/results/{username}/{id} | Obtain results from the session kill tool. Returns the latest results, if no ID is specified |
| [**broadbandSnrLogsUsernameGet()**](BroadbandTroubleshootingApi.md#broadbandSnrLogsUsernameGet) | **GET** /broadband/snr/logs/{username} | Gets SNR logs for a user. Only available for users with BT Wholesale products |
| [**broadbandSnrUsernameGet()**](BroadbandTroubleshootingApi.md#broadbandSnrUsernameGet) | **GET** /broadband/snr/{username} | Reset the SNR of the user line. Only available for users with BT Wholesale products |
| [**broadbandStabilityCurrentUsernameGet()**](BroadbandTroubleshootingApi.md#broadbandStabilityCurrentUsernameGet) | **GET** /broadband/stability/current/{username} | Gets the current stability option of the line. The stability option will change once the order is complete |
| [**broadbandStabilityPut()**](BroadbandTroubleshootingApi.md#broadbandStabilityPut) | **PUT** /broadband/stability | Updates the stability of the line |


## `broadbandDlmResetPut()`

```php
broadbandDlmResetPut($api_platform, $broadband_self_service_request): \OpenAPI\Client\Model\BroadbandSelfServiceResponse
```

Perform a DLM reset on a connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.
$broadband_self_service_request = new \OpenAPI\Client\Model\BroadbandSelfServiceRequest(); // \OpenAPI\Client\Model\BroadbandSelfServiceRequest | A BroadbandSelfServiceRequest

try {
    $result = $apiInstance->broadbandDlmResetPut($api_platform, $broadband_self_service_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandDlmResetPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |
| **broadband_self_service_request** | [**\OpenAPI\Client\Model\BroadbandSelfServiceRequest**](../Model/BroadbandSelfServiceRequest.md)| A BroadbandSelfServiceRequest | [optional] |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResponse**](../Model/BroadbandSelfServiceResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandDlmResetResultsUsernameGet()`

```php
broadbandDlmResetResultsUsernameGet($username, $api_platform): \OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse
```

Obtain results from the DLM reset tool. Returns the latest results, if no ID is specified

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | Username in the format username@realm
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandDlmResetResultsUsernameGet($username, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandDlmResetResultsUsernameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| Username in the format username@realm | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse**](../Model/BroadbandSelfServiceResultsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandDlmResetResultsUsernameIdGet()`

```php
broadbandDlmResetResultsUsernameIdGet($username, $id, $api_platform): \OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse
```

Obtain results from the DLM reset tool. Returns the latest results, if no ID is specified

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | Username in the format username@realm
$id = 'id_example'; // string | Optional request identifier
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandDlmResetResultsUsernameIdGet($username, $id, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandDlmResetResultsUsernameIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| Username in the format username@realm | |
| **id** | **string**| Optional request identifier | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse**](../Model/BroadbandSelfServiceResultsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandInterleavingCurrentUsernameGet()`

```php
broadbandInterleavingCurrentUsernameGet($username, $api_platform): \OpenAPI\Client\Model\BroadbandInterleaving
```

Retrieves the current interleaving option. Only available for users with BT Wholesale products

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | The user name
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandInterleavingCurrentUsernameGet($username, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandInterleavingCurrentUsernameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| The user name | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandInterleaving**](../Model/BroadbandInterleaving.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandInterleavingPut()`

```php
broadbandInterleavingPut($api_platform, $broadband_interleaving)
```

Updates the interleaving profile. Only available for users with BT Wholesale broadband products

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.
$broadband_interleaving = new \OpenAPI\Client\Model\BroadbandInterleaving(); // \OpenAPI\Client\Model\BroadbandInterleaving | A BroadbandInterleaving structure

try {
    $apiInstance->broadbandInterleavingPut($api_platform, $broadband_interleaving);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandInterleavingPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |
| **broadband_interleaving** | [**\OpenAPI\Client\Model\BroadbandInterleaving**](../Model/BroadbandInterleaving.md)| A BroadbandInterleaving structure | [optional] |

### Return type

void (empty response body)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandPortFlexPut()`

```php
broadbandPortFlexPut($api_platform, $broadband_self_service_request): \OpenAPI\Client\Model\BroadbandSelfServiceResponse
```

Perform a port flex on a connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.
$broadband_self_service_request = new \OpenAPI\Client\Model\BroadbandSelfServiceRequest(); // \OpenAPI\Client\Model\BroadbandSelfServiceRequest | A BroadbandSelfServiceRequest

try {
    $result = $apiInstance->broadbandPortFlexPut($api_platform, $broadband_self_service_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandPortFlexPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |
| **broadband_self_service_request** | [**\OpenAPI\Client\Model\BroadbandSelfServiceRequest**](../Model/BroadbandSelfServiceRequest.md)| A BroadbandSelfServiceRequest | [optional] |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResponse**](../Model/BroadbandSelfServiceResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandPortFlexResultsUsernameGet()`

```php
broadbandPortFlexResultsUsernameGet($username, $api_platform): \OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse
```

Obtain results from the port flex tool. Returns the latest results, if no ID is specified

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | Username in the format username@realm
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandPortFlexResultsUsernameGet($username, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandPortFlexResultsUsernameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| Username in the format username@realm | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse**](../Model/BroadbandSelfServiceResultsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandPortFlexResultsUsernameIdGet()`

```php
broadbandPortFlexResultsUsernameIdGet($username, $id, $api_platform): \OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse
```

Obtain results from the port flex tool. Returns the latest results, if no ID is specified

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | Username in the format username@realm
$id = 'id_example'; // string | Optional request identifier
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandPortFlexResultsUsernameIdGet($username, $id, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandPortFlexResultsUsernameIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| Username in the format username@realm | |
| **id** | **string**| Optional request identifier | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse**](../Model/BroadbandSelfServiceResultsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandPortRebuildPut()`

```php
broadbandPortRebuildPut($api_platform, $broadband_self_service_request): \OpenAPI\Client\Model\BroadbandSelfServiceResponse
```

Perform a port rebuild on a connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.
$broadband_self_service_request = new \OpenAPI\Client\Model\BroadbandSelfServiceRequest(); // \OpenAPI\Client\Model\BroadbandSelfServiceRequest | A BroadbandSelfServiceRequest

try {
    $result = $apiInstance->broadbandPortRebuildPut($api_platform, $broadband_self_service_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandPortRebuildPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |
| **broadband_self_service_request** | [**\OpenAPI\Client\Model\BroadbandSelfServiceRequest**](../Model/BroadbandSelfServiceRequest.md)| A BroadbandSelfServiceRequest | [optional] |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResponse**](../Model/BroadbandSelfServiceResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandPortRebuildResultsUsernameGet()`

```php
broadbandPortRebuildResultsUsernameGet($username, $api_platform): \OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse
```

Obtain results from the port rebuild tool. Returns the latest results, if no ID is specified

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | Username in the format username@realm
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandPortRebuildResultsUsernameGet($username, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandPortRebuildResultsUsernameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| Username in the format username@realm | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse**](../Model/BroadbandSelfServiceResultsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandPortRebuildResultsUsernameIdGet()`

```php
broadbandPortRebuildResultsUsernameIdGet($username, $id, $api_platform): \OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse
```

Obtain results from the port rebuild tool. Returns the latest results, if no ID is specified

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | Username in the format username@realm
$id = 'id_example'; // string | Optional request identifier
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandPortRebuildResultsUsernameIdGet($username, $id, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandPortRebuildResultsUsernameIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| Username in the format username@realm | |
| **id** | **string**| Optional request identifier | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse**](../Model/BroadbandSelfServiceResultsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandPortResetPut()`

```php
broadbandPortResetPut($api_platform, $broadband_self_service_request): \OpenAPI\Client\Model\BroadbandSelfServiceResponse
```

Perform a port reset on a connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.
$broadband_self_service_request = new \OpenAPI\Client\Model\BroadbandSelfServiceRequest(); // \OpenAPI\Client\Model\BroadbandSelfServiceRequest | A BroadbandSelfServiceRequest

try {
    $result = $apiInstance->broadbandPortResetPut($api_platform, $broadband_self_service_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandPortResetPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |
| **broadband_self_service_request** | [**\OpenAPI\Client\Model\BroadbandSelfServiceRequest**](../Model/BroadbandSelfServiceRequest.md)| A BroadbandSelfServiceRequest | [optional] |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResponse**](../Model/BroadbandSelfServiceResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandPortResetResultsUsernameGet()`

```php
broadbandPortResetResultsUsernameGet($username, $api_platform): \OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse
```

Obtain results from the port reset tool. Returns the latest results, if no ID is specified

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | Username in the format username@realm
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandPortResetResultsUsernameGet($username, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandPortResetResultsUsernameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| Username in the format username@realm | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse**](../Model/BroadbandSelfServiceResultsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandPortResetResultsUsernameIdGet()`

```php
broadbandPortResetResultsUsernameIdGet($username, $id, $api_platform): \OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse
```

Obtain results from the port reset tool. Returns the latest results, if no ID is specified

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | Username in the format username@realm
$id = 'id_example'; // string | Optional request identifier
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandPortResetResultsUsernameIdGet($username, $id, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandPortResetResultsUsernameIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| Username in the format username@realm | |
| **id** | **string**| Optional request identifier | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse**](../Model/BroadbandSelfServiceResultsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandProfileCurrentUsernameGet()`

```php
broadbandProfileCurrentUsernameGet($username, $api_platform): \OpenAPI\Client\Model\BroadbandSnrProfile
```

Gets the current SNR and interleaving profile. Only available for users with TalkTalk products

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | The user name
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandProfileCurrentUsernameGet($username, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandProfileCurrentUsernameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| The user name | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSnrProfile**](../Model/BroadbandSnrProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandProfilePut()`

```php
broadbandProfilePut($api_platform, $broadband_snr_profile): \OpenAPI\Client\Model\BroadbandSnrProfile
```

Updates SNR and interleaving profile. Only available for users with TalkTalk products

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.
$broadband_snr_profile = new \OpenAPI\Client\Model\BroadbandSnrProfile(); // \OpenAPI\Client\Model\BroadbandSnrProfile | A BroadbandSnrProfile structure

try {
    $result = $apiInstance->broadbandProfilePut($api_platform, $broadband_snr_profile);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandProfilePut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |
| **broadband_snr_profile** | [**\OpenAPI\Client\Model\BroadbandSnrProfile**](../Model/BroadbandSnrProfile.md)| A BroadbandSnrProfile structure | [optional] |

### Return type

[**\OpenAPI\Client\Model\BroadbandSnrProfile**](../Model/BroadbandSnrProfile.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandSessionKillPut()`

```php
broadbandSessionKillPut($api_platform, $broadband_self_service_request): \OpenAPI\Client\Model\BroadbandSelfServiceResponse
```

Perform a session kill on a connection

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.
$broadband_self_service_request = new \OpenAPI\Client\Model\BroadbandSelfServiceRequest(); // \OpenAPI\Client\Model\BroadbandSelfServiceRequest | A BroadbandSelfServiceRequest

try {
    $result = $apiInstance->broadbandSessionKillPut($api_platform, $broadband_self_service_request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandSessionKillPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |
| **broadband_self_service_request** | [**\OpenAPI\Client\Model\BroadbandSelfServiceRequest**](../Model/BroadbandSelfServiceRequest.md)| A BroadbandSelfServiceRequest | [optional] |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResponse**](../Model/BroadbandSelfServiceResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandSessionKillResultsUsernameGet()`

```php
broadbandSessionKillResultsUsernameGet($username, $api_platform): \OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse
```

Obtain results from the session kill tool. Returns the latest results, if no ID is specified

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | Username in the format username@realm
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandSessionKillResultsUsernameGet($username, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandSessionKillResultsUsernameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| Username in the format username@realm | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse**](../Model/BroadbandSelfServiceResultsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandSessionKillResultsUsernameIdGet()`

```php
broadbandSessionKillResultsUsernameIdGet($username, $id, $api_platform): \OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse
```

Obtain results from the session kill tool. Returns the latest results, if no ID is specified

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | Username in the format username@realm
$id = 'id_example'; // string | Optional request identifier
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandSessionKillResultsUsernameIdGet($username, $id, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandSessionKillResultsUsernameIdGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| Username in the format username@realm | |
| **id** | **string**| Optional request identifier | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSelfServiceResultsResponse**](../Model/BroadbandSelfServiceResultsResponse.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandSnrLogsUsernameGet()`

```php
broadbandSnrLogsUsernameGet($username, $api_platform): \OpenAPI\Client\Model\BroadbandSnr[]
```

Gets SNR logs for a user. Only available for users with BT Wholesale products

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | The user name
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandSnrLogsUsernameGet($username, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandSnrLogsUsernameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| The user name | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSnr[]**](../Model/BroadbandSnr.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandSnrUsernameGet()`

```php
broadbandSnrUsernameGet($username, $api_platform): \OpenAPI\Client\Model\BroadbandSnr
```

Reset the SNR of the user line. Only available for users with BT Wholesale products

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | The user name
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandSnrUsernameGet($username, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandSnrUsernameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| The user name | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

[**\OpenAPI\Client\Model\BroadbandSnr**](../Model/BroadbandSnr.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandStabilityCurrentUsernameGet()`

```php
broadbandStabilityCurrentUsernameGet($username, $api_platform): string
```

Gets the current stability option of the line. The stability option will change once the order is complete

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$username = 'username_example'; // string | Name of the user
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.

try {
    $result = $apiInstance->broadbandStabilityCurrentUsernameGet($username, $api_platform);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandStabilityCurrentUsernameGet: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **username** | **string**| Name of the user | |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |

### Return type

**string**

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `broadbandStabilityPut()`

```php
broadbandStabilityPut($api_platform, $broadband_stability): \OpenAPI\Client\Model\BroadbandStabilityTermination
```

Updates the stability of the line

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: oauth2
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\BroadbandTroubleshootingApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$api_platform = 'api_platform_example'; // string | The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes.
$broadband_stability = new \OpenAPI\Client\Model\BroadbandStability(); // \OpenAPI\Client\Model\BroadbandStability | A BroadbandStability structure

try {
    $result = $apiInstance->broadbandStabilityPut($api_platform, $broadband_stability);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling BroadbandTroubleshootingApi->broadbandStabilityPut: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **api_platform** | **string**| The API provides access to two separate platforms: test and live. The test platform allows you to experiment with the API without incurring charges or affecting customer orders. The live platform allows you to make real world changes. | |
| **broadband_stability** | [**\OpenAPI\Client\Model\BroadbandStability**](../Model/BroadbandStability.md)| A BroadbandStability structure | [optional] |

### Return type

[**\OpenAPI\Client\Model\BroadbandStabilityTermination**](../Model/BroadbandStabilityTermination.md)

### Authorization

[oauth2](../../README.md#oauth2)

### HTTP request headers

- **Content-Type**: `application/json`, `text/json`, `application/*+json`
- **Accept**: `text/plain`, `application/json`, `text/json`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
