# DeleteDocumentDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Document ID to delete | 
**Target** | Pointer to **string** | What to delete: - &#39;file&#39; (default): delete only the stored file from disk - &#39;metadata&#39;: delete only the metadata (OCR results, markdown chunks) without touching the file - &#39;both&#39;: delete the file and all associated metadata | [optional] [default to "file"]

## Methods

### NewDeleteDocumentDto

`func NewDeleteDocumentDto(id string, ) *DeleteDocumentDto`

NewDeleteDocumentDto instantiates a new DeleteDocumentDto object
This constructor will assign default values to properties that have it defined,
and makes sure properties required by API are set, but the set of arguments
will change when the set of required properties is changed

### NewDeleteDocumentDtoWithDefaults

`func NewDeleteDocumentDtoWithDefaults() *DeleteDocumentDto`

NewDeleteDocumentDtoWithDefaults instantiates a new DeleteDocumentDto object
This constructor will only assign default values to properties that have it defined,
but it doesn't guarantee that properties required by API are set

### GetId

`func (o *DeleteDocumentDto) GetId() string`

GetId returns the Id field if non-nil, zero value otherwise.

### GetIdOk

`func (o *DeleteDocumentDto) GetIdOk() (*string, bool)`

GetIdOk returns a tuple with the Id field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetId

`func (o *DeleteDocumentDto) SetId(v string)`

SetId sets Id field to given value.


### GetTarget

`func (o *DeleteDocumentDto) GetTarget() string`

GetTarget returns the Target field if non-nil, zero value otherwise.

### GetTargetOk

`func (o *DeleteDocumentDto) GetTargetOk() (*string, bool)`

GetTargetOk returns a tuple with the Target field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetTarget

`func (o *DeleteDocumentDto) SetTarget(v string)`

SetTarget sets Target field to given value.

### HasTarget

`func (o *DeleteDocumentDto) HasTarget() bool`

HasTarget returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


