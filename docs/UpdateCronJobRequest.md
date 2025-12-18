# UpdateCronJobRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**description** | **str** |  | [optional] 
**schedule_expression** | **str** |  | [optional] 
**command** | **List[str]** |  | [optional] 
**target_container_name** | **str** |  | [optional] 
**is_enabled** | **bool** |  | [optional] 

## Example

```python
from quantcdn.models.update_cron_job_request import UpdateCronJobRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateCronJobRequest from a JSON string
update_cron_job_request_instance = UpdateCronJobRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateCronJobRequest.to_json())

# convert the object into a dict
update_cron_job_request_dict = update_cron_job_request_instance.to_dict()
# create an instance of UpdateCronJobRequest from a dict
update_cron_job_request_from_dict = UpdateCronJobRequest.from_dict(update_cron_job_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


