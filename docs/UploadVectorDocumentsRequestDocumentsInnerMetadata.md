# UploadVectorDocumentsRequestDocumentsInnerMetadata


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** |  | [optional] 
**source_url** | **str** |  | [optional] 
**section** | **str** |  | [optional] 
**tags** | **List[str]** |  | [optional] 

## Example

```python
from quantcdn.models.upload_vector_documents_request_documents_inner_metadata import UploadVectorDocumentsRequestDocumentsInnerMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of UploadVectorDocumentsRequestDocumentsInnerMetadata from a JSON string
upload_vector_documents_request_documents_inner_metadata_instance = UploadVectorDocumentsRequestDocumentsInnerMetadata.from_json(json)
# print the JSON string representation of the object
print(UploadVectorDocumentsRequestDocumentsInnerMetadata.to_json())

# convert the object into a dict
upload_vector_documents_request_documents_inner_metadata_dict = upload_vector_documents_request_documents_inner_metadata_instance.to_dict()
# create an instance of UploadVectorDocumentsRequestDocumentsInnerMetadata from a dict
upload_vector_documents_request_documents_inner_metadata_from_dict = UploadVectorDocumentsRequestDocumentsInnerMetadata.from_dict(upload_vector_documents_request_documents_inner_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


