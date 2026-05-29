

# DeleteDocumentDto


## Properties

| Name | Type | Description | Notes |
|------------ | ------------- | ------------- | -------------|
|**id** | **String** | Document ID to delete |  |
|**target** | [**TargetEnum**](#TargetEnum) | What to delete: - &#39;file&#39; (default): delete only the stored file from disk - &#39;metadata&#39;: delete only the metadata (OCR results, markdown chunks) without touching the file - &#39;both&#39;: delete the file and all associated metadata |  [optional] |



## Enum: TargetEnum

| Name | Value |
|---- | -----|
| FILE | &quot;file&quot; |
| METADATA | &quot;metadata&quot; |
| BOTH | &quot;both&quot; |



