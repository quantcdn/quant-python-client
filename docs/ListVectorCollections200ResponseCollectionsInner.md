# ListVectorCollections200ResponseCollectionsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collection_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**document_count** | **int** |  | [optional] 
**embedding_model** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.list_vector_collections200_response_collections_inner import ListVectorCollections200ResponseCollectionsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListVectorCollections200ResponseCollectionsInner from a JSON string
list_vector_collections200_response_collections_inner_instance = ListVectorCollections200ResponseCollectionsInner.from_json(json)
# print the JSON string representation of the object
print(ListVectorCollections200ResponseCollectionsInner.to_json())

# convert the object into a dict
list_vector_collections200_response_collections_inner_dict = list_vector_collections200_response_collections_inner_instance.to_dict()
# create an instance of ListVectorCollections200ResponseCollectionsInner from a dict
list_vector_collections200_response_collections_inner_from_dict = ListVectorCollections200ResponseCollectionsInner.from_dict(list_vector_collections200_response_collections_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


