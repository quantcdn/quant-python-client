# V1SearchItemsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**hits** | [**List[V1SearchHit]**](V1SearchHit.md) |  | [optional] 
**nb_pages** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.v1_search_items_response import V1SearchItemsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1SearchItemsResponse from a JSON string
v1_search_items_response_instance = V1SearchItemsResponse.from_json(json)
# print the JSON string representation of the object
print(V1SearchItemsResponse.to_json())

# convert the object into a dict
v1_search_items_response_dict = v1_search_items_response_instance.to_dict()
# create an instance of V1SearchItemsResponse from a dict
v1_search_items_response_from_dict = V1SearchItemsResponse.from_dict(v1_search_items_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


