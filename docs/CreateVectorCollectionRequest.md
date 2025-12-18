# CreateVectorCollectionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Collection name (used for reference) | 
**description** | **str** |  | [optional] 
**embedding_model** | **str** | Embedding model to use (default: amazon.titan-embed-text-v2:0) | [optional] 
**dimensions** | **int** | Embedding dimensions (default: 1024) | [optional] 

## Example

```python
from quantcdn.models.create_vector_collection_request import CreateVectorCollectionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateVectorCollectionRequest from a JSON string
create_vector_collection_request_instance = CreateVectorCollectionRequest.from_json(json)
# print the JSON string representation of the object
print(CreateVectorCollectionRequest.to_json())

# convert the object into a dict
create_vector_collection_request_dict = create_vector_collection_request_instance.to_dict()
# create an instance of CreateVectorCollectionRequest from a dict
create_vector_collection_request_from_dict = CreateVectorCollectionRequest.from_dict(create_vector_collection_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


