# GetVectorCollection200ResponseCollection


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collection_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**document_count** | **int** |  | [optional] 
**embedding_model** | **str** |  | [optional] 
**dimensions** | **int** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.get_vector_collection200_response_collection import GetVectorCollection200ResponseCollection

# TODO update the JSON string below
json = "{}"
# create an instance of GetVectorCollection200ResponseCollection from a JSON string
get_vector_collection200_response_collection_instance = GetVectorCollection200ResponseCollection.from_json(json)
# print the JSON string representation of the object
print(GetVectorCollection200ResponseCollection.to_json())

# convert the object into a dict
get_vector_collection200_response_collection_dict = get_vector_collection200_response_collection_instance.to_dict()
# create an instance of GetVectorCollection200ResponseCollection from a dict
get_vector_collection200_response_collection_from_dict = GetVectorCollection200ResponseCollection.from_dict(get_vector_collection200_response_collection_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


