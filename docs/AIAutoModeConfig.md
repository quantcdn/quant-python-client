# AIAutoModeConfig


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | 
**orchestrator_model** | **str** | Empty when the setting was saved off without an orchestrator. | 
**group** | [**AIAutoModeConfigGroup**](AIAutoModeConfigGroup.md) |  | 
**watcher_interval_minutes** | **int** |  | 
**max_parallel_tasks** | **int** |  | [optional] 
**enforcement** | **str** |  | 
**autonomous_default** | **bool** |  | 
**updated_at** | **str** |  | 
**updated_by** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.ai_auto_mode_config import AIAutoModeConfig

# TODO update the JSON string below
json = "{}"
# create an instance of AIAutoModeConfig from a JSON string
ai_auto_mode_config_instance = AIAutoModeConfig.from_json(json)
# print the JSON string representation of the object
print(AIAutoModeConfig.to_json())

# convert the object into a dict
ai_auto_mode_config_dict = ai_auto_mode_config_instance.to_dict()
# create an instance of AIAutoModeConfig from a dict
ai_auto_mode_config_from_dict = AIAutoModeConfig.from_dict(ai_auto_mode_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


