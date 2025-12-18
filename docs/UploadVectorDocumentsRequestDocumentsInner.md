# UploadVectorDocumentsRequestDocumentsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**content** | **str** | Document text content | 
**metadata** | [**UploadVectorDocumentsRequestDocumentsInnerMetadata**](UploadVectorDocumentsRequestDocumentsInnerMetadata.md) |  | [optional] 

## Example

```python
from quantcdn.models.upload_vector_documents_request_documents_inner import UploadVectorDocumentsRequestDocumentsInner

# TODO update the JSON string below
json = "{}"
# create an instance of UploadVectorDocumentsRequestDocumentsInner from a JSON string
upload_vector_documents_request_documents_inner_instance = UploadVectorDocumentsRequestDocumentsInner.from_json(json)
# print the JSON string representation of the object
print(UploadVectorDocumentsRequestDocumentsInner.to_json())

# convert the object into a dict
upload_vector_documents_request_documents_inner_dict = upload_vector_documents_request_documents_inner_instance.to_dict()
# create an instance of UploadVectorDocumentsRequestDocumentsInner from a dict
upload_vector_documents_request_documents_inner_from_dict = UploadVectorDocumentsRequestDocumentsInner.from_dict(upload_vector_documents_request_documents_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


