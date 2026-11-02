# CronRun


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**run_id** | **str** |  | [optional] 
**run_type** | **str** |  | [optional] 
**command** | **str** |  | [optional] 
**status** | **str** | FAILED_TO_START: the task could not be launched, so the command never ran (for example, the job targets a container that no longer exists). | [optional] 
**error_message** | **str** | Why the run failed, in plain text. Set when the status is FAILED_TO_START. | [optional] 
**start_time** | **datetime** |  | [optional] 
**end_time** | **datetime** |  | [optional] 
**exit_code** | **int** |  | [optional] 
**output** | **List[str]** |  | [optional] 
**schedule_name** | **str** |  | [optional] 
**target_container_name** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.cron_run import CronRun

# TODO update the JSON string below
json = "{}"
# create an instance of CronRun from a JSON string
cron_run_instance = CronRun.from_json(json)
# print the JSON string representation of the object
print(CronRun.to_json())

# convert the object into a dict
cron_run_dict = cron_run_instance.to_dict()
# create an instance of CronRun from a dict
cron_run_from_dict = CronRun.from_dict(cron_run_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


