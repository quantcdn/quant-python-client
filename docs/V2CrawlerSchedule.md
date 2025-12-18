# V2CrawlerSchedule


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Schedule ID | 
**name** | **str** | Schedule name | [optional] 
**crawler_config_id** | **int** | Crawler config ID | 
**crawler_uuid** | **str** | Crawler UUID | [optional] 
**project_id** | **int** | Project ID | 
**crawler_last_run_id** | **int** | Last run ID | 
**schedule_cron_string** | **str** | Cron schedule string | 
**created_at** | **datetime** | Creation timestamp | [optional] 
**updated_at** | **datetime** | Last update timestamp | [optional] 

## Example

```python
from quantcdn.models.v2_crawler_schedule import V2CrawlerSchedule

# TODO update the JSON string below
json = "{}"
# create an instance of V2CrawlerSchedule from a JSON string
v2_crawler_schedule_instance = V2CrawlerSchedule.from_json(json)
# print the JSON string representation of the object
print(V2CrawlerSchedule.to_json())

# convert the object into a dict
v2_crawler_schedule_dict = v2_crawler_schedule_instance.to_dict()
# create an instance of V2CrawlerSchedule from a dict
v2_crawler_schedule_from_dict = V2CrawlerSchedule.from_dict(v2_crawler_schedule_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


