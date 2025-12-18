# CreateVectorCollection201ResponseCollection


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collection_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**embedding_model** | **str** |  | [optional] 
**dimensions** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.create_vector_collection201_response_collection import CreateVectorCollection201ResponseCollection

# TODO update the JSON string below
json = "{}"
# create an instance of CreateVectorCollection201ResponseCollection from a JSON string
create_vector_collection201_response_collection_instance = CreateVectorCollection201ResponseCollection.from_json(json)
# print the JSON string representation of the object
print(CreateVectorCollection201ResponseCollection.to_json())

# convert the object into a dict
create_vector_collection201_response_collection_dict = create_vector_collection201_response_collection_instance.to_dict()
# create an instance of CreateVectorCollection201ResponseCollection from a dict
create_vector_collection201_response_collection_from_dict = CreateVectorCollection201ResponseCollection.from_dict(create_vector_collection201_response_collection_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


