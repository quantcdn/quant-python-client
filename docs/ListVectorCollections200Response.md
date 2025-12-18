# ListVectorCollections200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**collections** | [**List[ListVectorCollections200ResponseCollectionsInner]**](ListVectorCollections200ResponseCollectionsInner.md) |  | [optional] 
**count** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.list_vector_collections200_response import ListVectorCollections200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListVectorCollections200Response from a JSON string
list_vector_collections200_response_instance = ListVectorCollections200Response.from_json(json)
# print the JSON string representation of the object
print(ListVectorCollections200Response.to_json())

# convert the object into a dict
list_vector_collections200_response_dict = list_vector_collections200_response_instance.to_dict()
# create an instance of ListVectorCollections200Response from a dict
list_vector_collections200_response_from_dict = ListVectorCollections200Response.from_dict(list_vector_collections200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


