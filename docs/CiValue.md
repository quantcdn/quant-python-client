# CiValue


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**kind** | **str** |  | [optional] 
**scope** | **str** |  | [optional] 
**repo** | **str** | Lower-case owner/name. Present when scope is repo. | [optional] 
**branches** | **List[str]** | The branch rule. Absent when the value applies to every branch. | [optional] 
**updated_at** | **datetime** |  | [optional] 
**updated_by** | **str** |  | [optional] 
**value** | **str** | Variables only. A secret value is never returned. | [optional] 

## Example

```python
from quantcdn.models.ci_value import CiValue

# TODO update the JSON string below
json = "{}"
# create an instance of CiValue from a JSON string
ci_value_instance = CiValue.from_json(json)
# print the JSON string representation of the object
print(CiValue.to_json())

# convert the object into a dict
ci_value_dict = ci_value_instance.to_dict()
# create an instance of CiValue from a dict
ci_value_from_dict = CiValue.from_dict(ci_value_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


