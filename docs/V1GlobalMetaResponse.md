# V1GlobalMetaResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**global_meta** | [**V1GlobalMetaResponseGlobalMeta**](V1GlobalMetaResponseGlobalMeta.md) |  | [optional] 
**total_records** | **int** |  | [optional] 
**total_pages** | **int** |  | [optional] 
**page** | **int** |  | [optional] 
**page_size** | **int** |  | [optional] 
**refine_search** | **bool** |  | [optional] 

## Example

```python
from quantcdn.models.v1_global_meta_response import V1GlobalMetaResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1GlobalMetaResponse from a JSON string
v1_global_meta_response_instance = V1GlobalMetaResponse.from_json(json)
# print the JSON string representation of the object
print(V1GlobalMetaResponse.to_json())

# convert the object into a dict
v1_global_meta_response_dict = v1_global_meta_response_instance.to_dict()
# create an instance of V1GlobalMetaResponse from a dict
v1_global_meta_response_from_dict = V1GlobalMetaResponse.from_dict(v1_global_meta_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


