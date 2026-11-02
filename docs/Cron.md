# Cron


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**schedule_expression** | **str** |  | [optional] 
**command** | **List[str]** |  | [optional] 
**target_container_name** | **str** |  | [optional] 
**is_enabled** | **bool** |  | [optional] 
**last_run** | [**CronLastRun**](CronLastRun.md) | The newest run of the job. Null when the job has never run. Sent by the cron list. | [optional] 
**consecutive_failures** | **int** | Failed runs (FAILED or FAILED_TO_START) from the newest run back to the first run that did not fail, counted over the latest 10 runs. 0 when the newest run did not fail. Sent by the cron list. | [optional] 

## Example

```python
from quantcdn.models.cron import Cron

# TODO update the JSON string below
json = "{}"
# create an instance of Cron from a JSON string
cron_instance = Cron.from_json(json)
# print the JSON string representation of the object
print(Cron.to_json())

# convert the object into a dict
cron_dict = cron_instance.to_dict()
# create an instance of Cron from a dict
cron_from_dict = Cron.from_dict(cron_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


