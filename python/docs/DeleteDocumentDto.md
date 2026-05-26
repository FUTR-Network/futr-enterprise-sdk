# DeleteDocumentDto


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Document ID to delete | 
**delete_metadata** | **bool** | Whether to also delete metadata (true) or just soft-delete the file (false) | [optional] [default to False]

## Example

```python
from openapi_client.models.delete_document_dto import DeleteDocumentDto

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteDocumentDto from a JSON string
delete_document_dto_instance = DeleteDocumentDto.from_json(json)
# print the JSON string representation of the object
print(DeleteDocumentDto.to_json())

# convert the object into a dict
delete_document_dto_dict = delete_document_dto_instance.to_dict()
# create an instance of DeleteDocumentDto from a dict
delete_document_dto_from_dict = DeleteDocumentDto.from_dict(delete_document_dto_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


