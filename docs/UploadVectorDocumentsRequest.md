# UploadVectorDocumentsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**documents** | [**List[UploadVectorDocumentsRequestDocumentsInner]**](UploadVectorDocumentsRequestDocumentsInner.md) |  | 

## Example

```python
from quantcdn.models.upload_vector_documents_request import UploadVectorDocumentsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UploadVectorDocumentsRequest from a JSON string
upload_vector_documents_request_instance = UploadVectorDocumentsRequest.from_json(json)
# print the JSON string representation of the object
print(UploadVectorDocumentsRequest.to_json())

# convert the object into a dict
upload_vector_documents_request_dict = upload_vector_documents_request_instance.to_dict()
# create an instance of UploadVectorDocumentsRequest from a dict
upload_vector_documents_request_from_dict = UploadVectorDocumentsRequest.from_dict(upload_vector_documents_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


