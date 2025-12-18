# UploadVectorDocuments200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**document_ids** | **List[str]** |  | [optional] 
**chunks_created** | **int** |  | [optional] 
**message** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.upload_vector_documents200_response import UploadVectorDocuments200Response

# TODO update the JSON string below
json = "{}"
# create an instance of UploadVectorDocuments200Response from a JSON string
upload_vector_documents200_response_instance = UploadVectorDocuments200Response.from_json(json)
# print the JSON string representation of the object
print(UploadVectorDocuments200Response.to_json())

# convert the object into a dict
upload_vector_documents200_response_dict = upload_vector_documents200_response_instance.to_dict()
# create an instance of UploadVectorDocuments200Response from a dict
upload_vector_documents200_response_from_dict = UploadVectorDocuments200Response.from_dict(upload_vector_documents200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


