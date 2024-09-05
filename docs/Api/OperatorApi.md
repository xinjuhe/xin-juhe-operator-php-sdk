# OpenAPI\Client\OperatorApi

All URIs are relative to https://api.juhe.xin, except if the operation defines another base path.

| Method | HTTP request | Description |
| ------------- | ------------- | ------------- |
| [**demoback()**](OperatorApi.md#demoback) | **POST** /sw/api/v1/code/demoback | 回到函数示例 |
| [**request()**](OperatorApi.md#request) | **POST** /sw/api/v1/code/request | 请求下发验证码接口 |
| [**verify()**](OperatorApi.md#verify) | **POST** /sw/api/v1/code/verify | 请求校验验证码接口 |


## `demoback()`

```php
demoback($data): string
```

回到函数示例

用户调用测试，业务系统无需调用

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: Authorization
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OperatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$data = new \OpenAPI\Client\Model\CallbackData(); // \OpenAPI\Client\Model\CallbackData | data

try {
    $result = $apiInstance->demoback($data);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OperatorApi->demoback: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **data** | [**\OpenAPI\Client\Model\CallbackData**](../Model/CallbackData.md)| data | |

### Return type

**string**

### Authorization

[Authorization](../../README.md#Authorization)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `request()`

```php
request($request): \OpenAPI\Client\Model\OutResponseOfCodeResponse
```

请求下发验证码接口

请求下发验证码接口

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: Authorization
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OperatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$request = new \OpenAPI\Client\Model\CodeRequest(); // \OpenAPI\Client\Model\CodeRequest | request

try {
    $result = $apiInstance->request($request);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OperatorApi->request: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **request** | [**\OpenAPI\Client\Model\CodeRequest**](../Model/CodeRequest.md)| request | |

### Return type

[**\OpenAPI\Client\Model\OutResponseOfCodeResponse**](../Model/OutResponseOfCodeResponse.md)

### Authorization

[Authorization](../../README.md#Authorization)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)

## `verify()`

```php
verify($verify): \OpenAPI\Client\Model\OutResponseOfCodeResponse
```

请求校验验证码接口

请求校验验证码接口

### Example

```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');


// Configure OAuth2 access token for authorization: Authorization
$config = OpenAPI\Client\Configuration::getDefaultConfiguration()->setAccessToken('YOUR_ACCESS_TOKEN');


$apiInstance = new OpenAPI\Client\Api\OperatorApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$verify = new \OpenAPI\Client\Model\CodeVerify(); // \OpenAPI\Client\Model\CodeVerify | verify

try {
    $result = $apiInstance->verify($verify);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling OperatorApi->verify: ', $e->getMessage(), PHP_EOL;
}
```

### Parameters

| Name | Type | Description  | Notes |
| ------------- | ------------- | ------------- | ------------- |
| **verify** | [**\OpenAPI\Client\Model\CodeVerify**](../Model/CodeVerify.md)| verify | |

### Return type

[**\OpenAPI\Client\Model\OutResponseOfCodeResponse**](../Model/OutResponseOfCodeResponse.md)

### Authorization

[Authorization](../../README.md#Authorization)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `*/*`

[[Back to top]](#) [[Back to API list]](../../README.md#endpoints)
[[Back to Model list]](../../README.md#models)
[[Back to README]](../../README.md)
