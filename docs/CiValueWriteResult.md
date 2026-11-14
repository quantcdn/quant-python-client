# CiValueWriteResult


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**kind** | **str** |  | [optional] 
**scope** | **str** |  | [optional] 
**repo** | **str** |  | [optional] 
**branches** | **List[str]** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.ci_value_write_result import CiValueWriteResult

# TODO update the JSON string below
json = "{}"
# create an instance of CiValueWriteResult from a JSON string
ci_value_write_result_instance = CiValueWriteResult.from_json(json)
# print the JSON string representation of the object
print(CiValueWriteResult.to_json())

# convert the object into a dict
ci_value_write_result_dict = ci_value_write_result_instance.to_dict()
# create an instance of CiValueWriteResult from a dict
ci_value_write_result_from_dict = CiValueWriteResult.from_dict(ci_value_write_result_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


