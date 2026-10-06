# DeleteVectorDocuments200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**message** | **str** |  | [optional] 
**collection_id** | **str** |  | [optional] 
**deleted_count** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.delete_vector_documents200_response import DeleteVectorDocuments200Response

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteVectorDocuments200Response from a JSON string
delete_vector_documents200_response_instance = DeleteVectorDocuments200Response.from_json(json)
# print the JSON string representation of the object
print(DeleteVectorDocuments200Response.to_json())

# convert the object into a dict
delete_vector_documents200_response_dict = delete_vector_documents200_response_instance.to_dict()
# create an instance of DeleteVectorDocuments200Response from a dict
delete_vector_documents200_response_from_dict = DeleteVectorDocuments200Response.from_dict(delete_vector_documents200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


