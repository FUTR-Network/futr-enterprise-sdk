# DocumentsApi

All URIs are relative to *http://localhost*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**documentControllerUploadDocument**](DocumentsApi.md#documentcontrolleruploaddocument) | **POST** /documents | Uploading a new document |



## documentControllerUploadDocument

> string documentControllerUploadDocument(file, monetized, fileHash, xClientEmail, derivedKey, password, isID, taskId)

Uploading a new document

### Example

```ts
import {
  Configuration,
  DocumentsApi,
} from '';
import type { DocumentControllerUploadDocumentRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // Configure HTTP bearer authorization: bearer
    accessToken: "YOUR BEARER TOKEN",
  });
  const api = new DocumentsApi(config);

  const body = {
    // Blob
    file: BINARY_DATA_HERE,
    // boolean | Monetized documents will contribute to building the client\\\'s profile
    monetized: true,
    // string
    fileHash: fileHash_example,
    // string | user\'s email address (for enterprise use only, end-client should skip this header) (optional)
    xClientEmail: xClientEmail_example,
    // string | (for end-client use only, enterprise should skip this property) (optional)
    derivedKey: derivedKey_example,
    // string | user\\\'s decryption password (for end-client use only, enterprise should skip this property) (optional)
    password: password_example,
    // boolean | (for end-client use only, enterprise should skip this property) (optional)
    isID: true,
    // string | (for end-client use only, enterprise should skip this property) (optional)
    taskId: taskId_example,
  } satisfies DocumentControllerUploadDocumentRequest;

  try {
    const data = await api.documentControllerUploadDocument(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **file** | `Blob` |  | [Defaults to `undefined`] |
| **monetized** | `boolean` | Monetized documents will contribute to building the client\\\&#39;s profile | [Defaults to `undefined`] |
| **fileHash** | `string` |  | [Defaults to `undefined`] |
| **xClientEmail** | `string` | user\&#39;s email address (for enterprise use only, end-client should skip this header) | [Optional] [Defaults to `undefined`] |
| **derivedKey** | `string` | (for end-client use only, enterprise should skip this property) | [Optional] [Defaults to `undefined`] |
| **password** | `string` | user\\\&#39;s decryption password (for end-client use only, enterprise should skip this property) | [Optional] [Defaults to `undefined`] |
| **isID** | `boolean` | (for end-client use only, enterprise should skip this property) | [Optional] [Defaults to `undefined`] |
| **taskId** | `string` | (for end-client use only, enterprise should skip this property) | [Optional] [Defaults to `undefined`] |

### Return type

**string**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

- **Content-Type**: `multipart/form-data`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | File upload successful. Document is processed asynchronously. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

