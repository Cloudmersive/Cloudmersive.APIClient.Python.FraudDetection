# cloudmersive_fraud_detection_api_client.FraudDetectionApi

All URIs are relative to *https://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**document_detect_fraud**](FraudDetectionApi.md#document_detect_fraud) | **POST** /fraud-ai/detection/document | AI Fraud Detection for Documents
[**document_detect_fraud_advanced**](FraudDetectionApi.md#document_detect_fraud_advanced) | **POST** /fraud-ai/detection/document/advanced | Advanced AI Fraud Detection for Documents


# **document_detect_fraud**
> FraudDetectionResult document_detect_fraud(input_file=input_file)

AI Fraud Detection for Documents

Perform fraud detection and classification on input document and user context.  Input document formats supported include DOCX, PDF, PNG and JPG.

### Example
```python
from __future__ import print_function
import time
import cloudmersive_fraud_detection_api_client
from cloudmersive_fraud_detection_api_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Apikey
configuration = cloudmersive_fraud_detection_api_client.Configuration()
configuration.api_key['Apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Apikey'] = 'Bearer'

# create an instance of the API class
api_instance = cloudmersive_fraud_detection_api_client.FraudDetectionApi(cloudmersive_fraud_detection_api_client.ApiClient(configuration))
input_file = '/path/to/file.txt' # file | Input document, or photos of a document, to perform fraud detection on (optional)

try:
    # AI Fraud Detection for Documents
    api_response = api_instance.document_detect_fraud(input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FraudDetectionApi->document_detect_fraud: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **input_file** | **file**| Input document, or photos of a document, to perform fraud detection on | [optional] 

### Return type

[**FraudDetectionResult**](FraudDetectionResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **document_detect_fraud_advanced**
> AdvancedFraudDetectionResult document_detect_fraud_advanced(user_email_address=user_email_address, user_email_address_verified=user_email_address_verified, input_file=input_file)

Advanced AI Fraud Detection for Documents

Perform advanced fraud detection and classification on input document and user context.  Input document formats supported include DOCX, PDF, PNG and JPG.

### Example
```python
from __future__ import print_function
import time
import cloudmersive_fraud_detection_api_client
from cloudmersive_fraud_detection_api_client.rest import ApiException
from pprint import pprint

# Configure API key authorization: Apikey
configuration = cloudmersive_fraud_detection_api_client.Configuration()
configuration.api_key['Apikey'] = 'YOUR_API_KEY'
# Uncomment below to setup prefix (e.g. Bearer) for API key, if needed
# configuration.api_key_prefix['Apikey'] = 'Bearer'

# create an instance of the API class
api_instance = cloudmersive_fraud_detection_api_client.FraudDetectionApi(cloudmersive_fraud_detection_api_client.ApiClient(configuration))
user_email_address = 'user_email_address_example' # str | User email address for context (optional) (optional)
user_email_address_verified = true # bool | True if the user's email address was verified (optional) (optional)
input_file = '/path/to/file.txt' # file | Input document, or photos of a document, to perform fraud detection on (optional)

try:
    # Advanced AI Fraud Detection for Documents
    api_response = api_instance.document_detect_fraud_advanced(user_email_address=user_email_address, user_email_address_verified=user_email_address_verified, input_file=input_file)
    pprint(api_response)
except ApiException as e:
    print("Exception when calling FraudDetectionApi->document_detect_fraud_advanced: %s\n" % e)
```

### Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **user_email_address** | **str**| User email address for context (optional) | [optional] 
 **user_email_address_verified** | **bool**| True if the user&#39;s email address was verified (optional) | [optional] 
 **input_file** | **file**| Input document, or photos of a document, to perform fraud detection on | [optional] 

### Return type

[**AdvancedFraudDetectionResult**](AdvancedFraudDetectionResult.md)

### Authorization

[Apikey](../README.md#Apikey)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: text/plain, application/json, text/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

