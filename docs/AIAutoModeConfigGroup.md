# AIAutoModeConfigGroup


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**revision** | **int** |  | 
**roles** | [**AIAutoModeConfigGroupRoles**](AIAutoModeConfigGroupRoles.md) |  | 

## Example

```python
from quantcdn.models.ai_auto_mode_config_group import AIAutoModeConfigGroup

# TODO update the JSON string below
json = "{}"
# create an instance of AIAutoModeConfigGroup from a JSON string
ai_auto_mode_config_group_instance = AIAutoModeConfigGroup.from_json(json)
# print the JSON string representation of the object
print(AIAutoModeConfigGroup.to_json())

# convert the object into a dict
ai_auto_mode_config_group_dict = ai_auto_mode_config_group_instance.to_dict()
# create an instance of AIAutoModeConfigGroup from a dict
ai_auto_mode_config_group_from_dict = AIAutoModeConfigGroup.from_dict(ai_auto_mode_config_group_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


