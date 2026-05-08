# \DocumentsAPI

All URIs are relative to *http://localhost*

Method | HTTP request | Description
------------- | ------------- | -------------
[**DocumentControllerUploadDocument**](DocumentsAPI.md#DocumentControllerUploadDocument) | **Post** /documents | Uploading a new document



## DocumentControllerUploadDocument

> string DocumentControllerUploadDocument(ctx).File(file).Monetized(monetized).FileHash(fileHash).XClientEmail(xClientEmail).DerivedKey(derivedKey).Password(password).IsID(isID).TaskId(taskId).Execute()

Uploading a new document

### Example

```go
package main

import (
	"context"
	"fmt"
	"os"
	openapiclient "github.com/GIT_USER_ID/GIT_REPO_ID"
)

func main() {
	file := os.NewFile(1234, "some_file") // *os.File | 
	monetized := true // bool | Monetized documents will contribute to building the client's profile
	fileHash := "fileHash_example" // string | SHA-256 hash of the file content for integrity verification (hex string)
	xClientEmail := "xClientEmail_example" // string | user's email address (for enterprise use only, end-client should skip this header) (optional)
	derivedKey := "derivedKey_example" // string | derived encryption key for the document               Users without a CMK or are **Enterprises** can skip this property.             For end-clients with a CMK, this should be provided to enable encryption at rest and decryption for agent queries.             For enterprise clients, this property should be skipped.              (optional)
	password := "password_example" // string | user's decryption password (for end-client use only, enterprise should skip this property) (optional)
	isID := true // bool | (for end-client use only, enterprise should skip this property) (optional)
	taskId := "taskId_example" // string | (for end-client use only, enterprise should skip this property) (optional)

	configuration := openapiclient.NewConfiguration()
	apiClient := openapiclient.NewAPIClient(configuration)
	resp, r, err := apiClient.DocumentsAPI.DocumentControllerUploadDocument(context.Background()).File(file).Monetized(monetized).FileHash(fileHash).XClientEmail(xClientEmail).DerivedKey(derivedKey).Password(password).IsID(isID).TaskId(taskId).Execute()
	if err != nil {
		fmt.Fprintf(os.Stderr, "Error when calling `DocumentsAPI.DocumentControllerUploadDocument``: %v\n", err)
		fmt.Fprintf(os.Stderr, "Full HTTP response: %v\n", r)
	}
	// response from `DocumentControllerUploadDocument`: string
	fmt.Fprintf(os.Stdout, "Response from `DocumentsAPI.DocumentControllerUploadDocument`: %v\n", resp)
}
```

### Path Parameters



### Other Parameters

Other parameters are passed through a pointer to a apiDocumentControllerUploadDocumentRequest struct via the builder pattern


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **file** | ***os.File** |  | 
 **monetized** | **bool** | Monetized documents will contribute to building the client&#39;s profile | 
 **fileHash** | **string** | SHA-256 hash of the file content for integrity verification (hex string) | 
 **xClientEmail** | **string** | user&#39;s email address (for enterprise use only, end-client should skip this header) | 
 **derivedKey** | **string** | derived encryption key for the document               Users without a CMK or are **Enterprises** can skip this property.             For end-clients with a CMK, this should be provided to enable encryption at rest and decryption for agent queries.             For enterprise clients, this property should be skipped.              | 
 **password** | **string** | user&#39;s decryption password (for end-client use only, enterprise should skip this property) | 
 **isID** | **bool** | (for end-client use only, enterprise should skip this property) | 
 **taskId** | **string** | (for end-client use only, enterprise should skip this property) | 

### Return type

**string**

### Authorization

[bearer](../README.md#bearer)

### HTTP request headers

- **Content-Type**: multipart/form-data
- **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints)
[[Back to Model list]](../README.md#documentation-for-models)
[[Back to README]](../README.md)

