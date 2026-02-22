# Swagger\Client\RedactApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**redactDocument**](RedactApi.md#redactDocument) | **POST** /dlp/redact/document | Redact User Data in Document
[**redactDocumentAdvanced**](RedactApi.md#redactDocumentAdvanced) | **POST** /dlp/redact/document/advanced | Redact User Data in Document (Advanced)
[**redactText**](RedactApi.md#redactText) | **POST** /dlp/redact/text | Redact User Data in Input Text
[**redactTextAdvanced**](RedactApi.md#redactTextAdvanced) | **POST** /dlp/redact/text/advanced | Redact User Data in Input Text (Advanced)


# **redactDocument**
> \Swagger\Client\Model\DlpDocumentRedactionResponse redactDocument($body)

Redact User Data in Document

Detects and redacts configurable types of user data in a document (PDF, DOCX, PNG, JPG) using Advanced AI. Rasterizes document pages, detects PII regions using a grid-overlay approach, blurs those regions, and returns a rasterized PDF.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\RedactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DlpDocumentRedactionRequest(); // \Swagger\Client\Model\DlpDocumentRedactionRequest | Input request

try {
    $result = $apiInstance->redactDocument($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedactApi->redactDocument: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DlpDocumentRedactionRequest**](../Model/DlpDocumentRedactionRequest.md)| Input request | [optional]

### Return type

[**\Swagger\Client\Model\DlpDocumentRedactionResponse**](../Model/DlpDocumentRedactionResponse.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **redactDocumentAdvanced**
> \Swagger\Client\Model\DlpAdvancedDocumentRedactionResponse redactDocumentAdvanced($body)

Redact User Data in Document (Advanced)

Detects and redacts 35 configurable types of user data including health-related PHI in a document (PDF, DOCX, PNG, JPG) using Advanced AI. Rasterizes document pages, detects PII regions using a row-overlay approach, redacts those regions, and returns a rasterized PDF.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\RedactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DlpAdvancedDocumentRedactionRequest(); // \Swagger\Client\Model\DlpAdvancedDocumentRedactionRequest | Input request

try {
    $result = $apiInstance->redactDocumentAdvanced($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedactApi->redactDocumentAdvanced: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DlpAdvancedDocumentRedactionRequest**](../Model/DlpAdvancedDocumentRedactionRequest.md)| Input request | [optional]

### Return type

[**\Swagger\Client\Model\DlpAdvancedDocumentRedactionResponse**](../Model/DlpAdvancedDocumentRedactionResponse.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **redactText**
> \Swagger\Client\Model\DlpRedactionResponse redactText($body)

Redact User Data in Input Text

Detects and redacts configurable types of user data in an input text string using Advanced AI. First detects PII, then redacts disallowed types by either deleting them or replacing them with asterisks.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\RedactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DlpRedactionRequest(); // \Swagger\Client\Model\DlpRedactionRequest | Input request

try {
    $result = $apiInstance->redactText($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedactApi->redactText: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DlpRedactionRequest**](../Model/DlpRedactionRequest.md)| Input request | [optional]

### Return type

[**\Swagger\Client\Model\DlpRedactionResponse**](../Model/DlpRedactionResponse.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

# **redactTextAdvanced**
> \Swagger\Client\Model\DlpAdvancedRedactionResponse redactTextAdvanced($body)

Redact User Data in Input Text (Advanced)

Detects and redacts 34 configurable types of user data including health-related PHI in an input text string using Advanced AI. First detects PII, then redacts disallowed types by either deleting them or replacing them with asterisks.

### Example
```php
<?php
require_once(__DIR__ . '/vendor/autoload.php');

// Configure API key authorization: Apikey
$config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKey('Apikey', 'YOUR_API_KEY');
// Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
// $config = Swagger\Client\Configuration::getDefaultConfiguration()->setApiKeyPrefix('Apikey', 'Bearer');

$apiInstance = new Swagger\Client\Api\RedactApi(
    // If you want use custom http client, pass your client which implements `GuzzleHttp\ClientInterface`.
    // This is optional, `GuzzleHttp\Client` will be used as default.
    new GuzzleHttp\Client(),
    $config
);
$body = new \Swagger\Client\Model\DlpAdvancedRedactionRequest(); // \Swagger\Client\Model\DlpAdvancedRedactionRequest | Input request

try {
    $result = $apiInstance->redactTextAdvanced($body);
    print_r($result);
} catch (Exception $e) {
    echo 'Exception when calling RedactApi->redactTextAdvanced: ', $e->getMessage(), PHP_EOL;
}
?>
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **body** | [**\Swagger\Client\Model\DlpAdvancedRedactionRequest**](../Model/DlpAdvancedRedactionRequest.md)| Input request | [optional]

### Return type

[**\Swagger\Client\Model\DlpAdvancedRedactionResponse**](../Model/DlpAdvancedRedactionResponse.md)

### Authorization

[Apikey](../../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: application/json, text/json, application/_*+json
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../../README.md#documentation-for-api-endpoints) [[Back to Model list]](../../README.md#documentation-for-models) [[Back to README]](../../README.md)

