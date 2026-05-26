# DeleteDocumentDto

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**Id** | **string** | Document ID to delete | 
**DeleteMetadata** | Pointer to **bool** | Whether to also delete metadata (true) or just soft-delete the file (false) | [optional] [default to false]

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


### GetDeleteMetadata

`func (o *DeleteDocumentDto) GetDeleteMetadata() bool`

GetDeleteMetadata returns the DeleteMetadata field if non-nil, zero value otherwise.

### GetDeleteMetadataOk

`func (o *DeleteDocumentDto) GetDeleteMetadataOk() (*bool, bool)`

GetDeleteMetadataOk returns a tuple with the DeleteMetadata field if it's non-nil, zero value otherwise
and a boolean to check if the value has been set.

### SetDeleteMetadata

`func (o *DeleteDocumentDto) SetDeleteMetadata(v bool)`

SetDeleteMetadata sets DeleteMetadata field to given value.

### HasDeleteMetadata

`func (o *DeleteDocumentDto) HasDeleteMetadata() bool`

HasDeleteMetadata returns a boolean if a field has been set.


[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


