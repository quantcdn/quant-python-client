# Command


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**run_id** | **str** |  | [optional] 
**run_type** | **str** |  | [optional] 
**command** | **str** |  | [optional] 
**status** | **str** |  | [optional] 
**start_time** | **str** |  | [optional] 
**end_time** | **str** |  | [optional] 
**exit_code** | **int** |  | [optional] 
**output** | **List[str]** |  | [optional] 
**schedule_name** | **str** |  | [optional] 
**target_container_name** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.command import Command

# TODO update the JSON string below
json = "{}"
# create an instance of Command from a JSON string
command_instance = Command.from_json(json)
# print the JSON string representation of the object
print(Command.to_json())

# convert the object into a dict
command_dict = command_instance.to_dict()
# create an instance of Command from a dict
command_from_dict = Command.from_dict(command_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


