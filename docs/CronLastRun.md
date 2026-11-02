# CronLastRun

Summary of the newest run of a cron job.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**run_id** | **str** |  | [optional] 
**status** | **str** | FAILED_TO_START: the task could not be launched, so the command never ran (for example, the job targets a container that no longer exists). | [optional] 
**created_at** | **datetime** |  | [optional] 
**exit_code** | **int** |  | [optional] 
**error_message** | **str** | Why the run failed, in plain text. Set when the status is FAILED_TO_START. | [optional] 

## Example

```python
from quantcdn.models.cron_last_run import CronLastRun

# TODO update the JSON string below
json = "{}"
# create an instance of CronLastRun from a JSON string
cron_last_run_instance = CronLastRun.from_json(json)
# print the JSON string representation of the object
print(CronLastRun.to_json())

# convert the object into a dict
cron_last_run_dict = cron_last_run_instance.to_dict()
# create an instance of CronLastRun from a dict
cron_last_run_from_dict = CronLastRun.from_dict(cron_last_run_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


