# Swagger\Client\DetectApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**detectDocument**](DetectApi.md#detectDocument) | **POST** /dlp/detect/document | Detect User Data in Document Image
[**detectDocumentAdvanced**](DetectApi.md#detectDocumentAdvanced) | **POST** /dlp/detect/document/advanced | Detect User Data in Document Image (Advanced)
[**detectText**](DetectApi.md#detectText) | **POST** /dlp/detect/text | Detect User Data in Input Text
[**detectTextAdvanced**](DetectApi.md#detectTextAdvanced) | **POST** /dlp/detect/text/advanced | Detect User Data in Input Text (Advanced)


# **detectDocument**
> \Swagger\Client\Model\DlpDetectionResponse detectDocument($body)

Detect User Data in Document Image

Detects configurable types of user data in a document image (PDF, DOCX, PNG, JPG) using Advanced AI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\DetectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DlpDocumentDetectionRequest(); // \Swagger\Client\Model\DlpDocumentDetectionRequest | Input request

try {
    $result = $apiInstance->detectDocument($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DetectApi->detectDocument: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DlpDocumentDetectionRequest**](../Model/DlpDocumentDetectionRequest.md)| Input request | [optional]

### Return type

[**\Swagger\Client\Model\DlpDetectionResponse**](../Model/DlpDetectionResponse.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **detectDocumentAdvanced**
> \Swagger\Client\Model\DlpAdvancedDetectionResponse detectDocumentAdvanced($body)

Detect User Data in Document Image (Advanced)

Detects 29 configurable types of user data including health-related PHI in a document image (PDF, DOCX, PNG, JPG) using Advanced AI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\DetectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DlpAdvancedDocumentDetectionRequest(); // \Swagger\Client\Model\DlpAdvancedDocumentDetectionRequest | Input request

try {
    $result = $apiInstance->detectDocumentAdvanced($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DetectApi->detectDocumentAdvanced: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DlpAdvancedDocumentDetectionRequest**](../Model/DlpAdvancedDocumentDetectionRequest.md)| Input request | [optional]

### Return type

[**\Swagger\Client\Model\DlpAdvancedDetectionResponse**](../Model/DlpAdvancedDetectionResponse.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **detectText**
> \Swagger\Client\Model\DlpDetectionResponse detectText($body)

Detect User Data in Input Text

Detects configurable types of user data in an input text string using Advanced AI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\DetectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DlpDetectionRequest(); // \Swagger\Client\Model\DlpDetectionRequest | Input request

try {
    $result = $apiInstance->detectText($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DetectApi->detectText: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DlpDetectionRequest**](../Model/DlpDetectionRequest.md)| Input request | [optional]

### Return type

[**\Swagger\Client\Model\DlpDetectionResponse**](../Model/DlpDetectionResponse.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **detectTextAdvanced**
> \Swagger\Client\Model\DlpAdvancedDetectionResponse detectTextAdvanced($body)

Detect User Data in Input Text (Advanced)

Detects 29 configurable types of user data including health-related PHI in an input text string using Advanced AI.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\DetectApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DlpAdvancedDetectionRequest(); // \Swagger\Client\Model\DlpAdvancedDetectionRequest | Input request

try {
    $result = $apiInstance->detectTextAdvanced($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling DetectApi->detectTextAdvanced: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DlpAdvancedDetectionRequest**](../Model/DlpAdvancedDetectionRequest.md)| Input request | [optional]

### Return type

[**\Swagger\Client\Model\DlpAdvancedDetectionResponse**](../Model/DlpAdvancedDetectionResponse.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

