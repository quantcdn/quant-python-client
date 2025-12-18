# ListAISessions200ResponseInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | [optional] 
**title** | **str** |  | [optional] 
**model** | **str** |  | [optional] 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.list_ai_sessions200_response_inner import ListAISessions200ResponseInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListAISessions200ResponseInner from a JSON string
list_ai_sessions200_response_inner_instance = ListAISessions200ResponseInner.from_json(json)
# print the JSON string representation of the object
print(ListAISessions200ResponseInner.to_json())

# convert the object into a dict
list_ai_sessions200_response_inner_dict = list_ai_sessions200_response_inner_instance.to_dict()
# create an instance of ListAISessions200ResponseInner from a dict
list_ai_sessions200_response_inner_from_dict = ListAISessions200ResponseInner.from_dict(list_ai_sessions200_response_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


