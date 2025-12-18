# CreateCronJobRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**description** | **str** |  | [optional] 
**schedule_expression** | **str** |  | 
**command** | **List[str]** |  | 
**target_container_name** | **str** |  | [optional] 
**is_enabled** | **bool** |  | [optional] [default to True]

## Example

```python
from quantcdn.models.create_cron_job_request import CreateCronJobRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateCronJobRequest from a JSON string
create_cron_job_request_instance = CreateCronJobRequest.from_json(json)
# print the JSON string representation of the object
print(CreateCronJobRequest.to_json())

# convert the object into a dict
create_cron_job_request_dict = create_cron_job_request_instance.to_dict()
# create an instance of CreateCronJobRequest from a dict
create_cron_job_request_from_dict = CreateCronJobRequest.from_dict(create_cron_job_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


