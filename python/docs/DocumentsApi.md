# openapi_client.DocumentsApi

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**document_controller_upload_document**](DocumentsApi.md#document_controller_upload_document) | **POST** /documents | Uploading a new document


# **document_controller_upload_document**
> str document_controller_upload_document(file, monetized, file_hash, x_client_email=x_client_email, derived_key=derived_key, password=password, is_id=is_id, task_id=task_id)

Uploading a new document

### Example

* Bearer (JWT) Authentication (bearer):

```python
import openapi_client
from openapi_client.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to http://localhost
# See configuration.py for a list of all supported configuration parameters.
configuration = openapi_client.Configuration(
    host = "http://localhost"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): bearer
configuration = openapi_client.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with openapi_client.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = openapi_client.DocumentsApi(api_client)
    file = None # bytes | 
    monetized = True # bool | Monetized documents will contribute to building the client's profile
    file_hash = 'file_hash_example' # str | SHA-256 hash of the file content for integrity verification (hex string)
    x_client_email = 'x_client_email_example' # str | user's email address (for enterprise use only, end-client should skip this header) (optional)
    derived_key = 'derived_key_example' # str | derived encryption key for the document               Users without a CMK or are **Enterprises** can skip this property.             For end-clients with a CMK, this should be provided to enable encryption at rest and decryption for agent queries.             For enterprise clients, this property should be skipped.              (optional)
    password = 'password_example' # str | user's decryption password (for end-client use only, enterprise should skip this property) (optional)
    is_id = True # bool | (for end-client use only, enterprise should skip this property) (optional)
    task_id = 'task_id_example' # str | (for end-client use only, enterprise should skip this property) (optional)

    try:
        # Uploading a new document
        api_response = api_instance.document_controller_upload_document(file, monetized, file_hash, x_client_email=x_client_email, derived_key=derived_key, password=password, is_id=is_id, task_id=task_id)
        print("The response of DocumentsApi->document_controller_upload_document:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling DocumentsApi->document_controller_upload_document: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | **bytes**|  | 
 **monetized** | **bool**| Monetized documents will contribute to building the client&#39;s profile | 
 **file_hash** | **str**| SHA-256 hash of the file content for integrity verification (hex string) | 
 **x_client_email** | **str**| user&#39;s email address (for enterprise use only, end-client should skip this header) | [optional] 
 **derived_key** | **str**| derived encryption key for the document               Users without a CMK or are **Enterprises** can skip this property.             For end-clients with a CMK, this should be provided to enable encryption at rest and decryption for agent queries.             For enterprise clients, this property should be skipped.              | [optional] 
 **password** | **str**| user&#39;s decryption password (for end-client use only, enterprise should skip this property) | [optional] 
 **is_id** | **bool**| (for end-client use only, enterprise should skip this property) | [optional] 
 **task_id** | **str**| (for end-client use only, enterprise should skip this property) | [optional] 

### Return type

**str**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** |          File upload accepted after validation and malware scan. Returns a document ID immediately; OCR,         storage, and downstream processing continue asynchronously. Use the returned ID with GET /documents/:id         to poll processing status and fetch extracted details.        |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

