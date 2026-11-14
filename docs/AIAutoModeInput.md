# AIAutoModeInput


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** |  | 
**orchestrator_model** | **str** | Required when enabled is true. May be left out when enabled is false. | [optional] 
**group** | [**AIAutoModeInputGroup**](AIAutoModeInputGroup.md) |  | 
**watcher_interval_minutes** | **int** |  | 
**max_parallel_tasks** | **int** |  | [optional] 
**enforcement** | **str** |  | 
**autonomous_default** | **bool** |  | 

## Example

```python
from quantcdn.models.ai_auto_mode_input import AIAutoModeInput

# TODO update the JSON string below
json = "{}"
# create an instance of AIAutoModeInput from a JSON string
ai_auto_mode_input_instance = AIAutoModeInput.from_json(json)
# print the JSON string representation of the object
print(AIAutoModeInput.to_json())

# convert the object into a dict
ai_auto_mode_input_dict = ai_auto_mode_input_instance.to_dict()
# create an instance of AIAutoModeInput from a dict
ai_auto_mode_input_from_dict = AIAutoModeInput.from_dict(ai_auto_mode_input_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


