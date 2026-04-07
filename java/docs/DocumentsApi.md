# DocumentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**documentControllerUploadDocument**](DocumentsApi.md#documentControllerUploadDocument) | **POST** /documents | Uploading a new document |


<a id="documentControllerUploadDocument"></a>
# **documentControllerUploadDocument**
> String documentControllerUploadDocument(_file, monetized, fileHash, xClientEmail, derivedKey, password, isID, taskId)

Uploading a new document

### Example
```java
// Import classes:
import org.openapitools.client.ApiClient;
import org.openapitools.client.ApiException;
import org.openapitools.client.Configuration;
import org.openapitools.client.auth.*;
import org.openapitools.client.models.*;
import org.openapitools.client.api.DocumentsApi;

public class Example {
  public static void main(String[] args) {
    ApiClient defaultClient = Configuration.getDefaultApiClient();
    defaultClient.setBasePath("http://localhost");
    
    // Configure HTTP bearer authorization: bearer
    HttpBearerAuth bearer = (HttpBearerAuth) defaultClient.getAuthentication("bearer");
    bearer.setBearerToken("BEARER TOKEN");

    DocumentsApi apiInstance = new DocumentsApi(defaultClient);
    File _file = new File("/path/to/file"); // File | 
    Boolean monetized = true; // Boolean | Monetized documents will contribute to building the client's profile
    String fileHash = "fileHash_example"; // String | 
    String xClientEmail = "xClientEmail_example"; // String | user's email address (for enterprise use only, end-client should skip this header)
    String derivedKey = "derivedKey_example"; // String | (for end-client use only, enterprise should skip this property)
    String password = "password_example"; // String | user's decryption password (for end-client use only, enterprise should skip this property)
    Boolean isID = true; // Boolean | (for end-client use only, enterprise should skip this property)
    String taskId = "taskId_example"; // String | (for end-client use only, enterprise should skip this property)
    try {
      String result = apiInstance.documentControllerUploadDocument(_file, monetized, fileHash, xClientEmail, derivedKey, password, isID, taskId);
      System.out.println(result);
    } catch (ApiException e) {
      System.err.println("Exception when calling DocumentsApi#documentControllerUploadDocument");
      System.err.println("Status code: " + e.getCode());
      System.err.println("Reason: " + e.getResponseBody());
      System.err.println("Response headers: " + e.getResponseHeaders());
      e.printStackTrace();
    }
  }
}
```

### Parameters

| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **_file** | **File**|  | |
| **monetized** | **Boolean**| Monetized documents will contribute to building the client&#39;s profile | |
| **fileHash** | **String**|  | |
| **xClientEmail** | **String**| user&#39;s email address (for enterprise use only, end-client should skip this header) | [optional] |
| **derivedKey** | **String**| (for end-client use only, enterprise should skip this property) | [optional] |
| **password** | **String**| user&#39;s decryption password (for end-client use only, enterprise should skip this property) | [optional] |
| **isID** | **Boolean**| (for end-client use only, enterprise should skip this property) | [optional] |
| **taskId** | **String**| (for end-client use only, enterprise should skip this property) | [optional] |

### Return type

**String**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

 - **Content-Type**: multipart/form-data
 - **Accept**: application/json

### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | File upload successful. Document is processed asynchronously. |  -  |

