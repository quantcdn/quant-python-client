# AIAutoModeInputGroup


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**revision** | **int** | Revision from the last read. A stale value returns 409. | [optional] 
**roles** | [**AIAutoModeConfigGroupRoles**](AIAutoModeConfigGroupRoles.md) |  | 

## Example

```python
from quantcdn.models.ai_auto_mode_input_group import AIAutoModeInputGroup

# TODO update the JSON string below
json = "{}"
# create an instance of AIAutoModeInputGroup from a JSON string
ai_auto_mode_input_group_instance = AIAutoModeInputGroup.from_json(json)
# print the JSON string representation of the object
print(AIAutoModeInputGroup.to_json())

# convert the object into a dict
ai_auto_mode_input_group_dict = ai_auto_mode_input_group_instance.to_dict()
# create an instance of AIAutoModeInputGroup from a dict
ai_auto_mode_input_group_from_dict = AIAutoModeInputGroup.from_dict(ai_auto_mode_input_group_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


