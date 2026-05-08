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
    // string | SHA-256 hash of the file content for integrity verification (hex string)
    fileHash: fileHash_example,
    // string | user\'s email address (for enterprise use only, end-client should skip this header) (optional)
    xClientEmail: xClientEmail_example,
    // string | derived encryption key for the document               Users without a CMK or are **Enterprises** can skip this property.             For end-clients with a CMK, this should be provided to enable encryption at rest and decryption for agent queries.             For enterprise clients, this property should be skipped.              (optional)
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
| **fileHash** | `string` | SHA-256 hash of the file content for integrity verification (hex string) | [Defaults to `undefined`] |
| **xClientEmail** | `string` | user\&#39;s email address (for enterprise use only, end-client should skip this header) | [Optional] [Defaults to `undefined`] |
| **derivedKey** | `string` | derived encryption key for the document               Users without a CMK or are **Enterprises** can skip this property.             For end-clients with a CMK, this should be provided to enable encryption at rest and decryption for agent queries.             For enterprise clients, this property should be skipped.              | [Optional] [Defaults to `undefined`] |
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
| **201** |          File upload accepted after validation and malware scan. Returns a document ID immediately; OCR,         storage, and downstream processing continue asynchronously. Use the returned ID with GET /documents/:id         to poll processing status and fetch extracted details.        |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

