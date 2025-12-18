# V1SearchHit

Generic search hit; fields vary by index

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**title** | **str** | The controller for managing Search integration. | [optional] 
**url** | **str** |  | [optional] 
**summary** | **str** |  | [optional] 
**content** | **str** |  | [optional] 
**image** | **str** |  | [optional] 
**object_id** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.v1_search_hit import V1SearchHit

# TODO update the JSON string below
json = "{}"
# create an instance of V1SearchHit from a JSON string
v1_search_hit_instance = V1SearchHit.from_json(json)
# print the JSON string representation of the object
print(V1SearchHit.to_json())

# convert the object into a dict
v1_search_hit_dict = v1_search_hit_instance.to_dict()
# create an instance of V1SearchHit from a dict
v1_search_hit_from_dict = V1SearchHit.from_dict(v1_search_hit_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


