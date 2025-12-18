# V2CrawlerScheduleRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Schedule name | 
**schedule_cron_string** | **str** | Cron schedule string | 

## Example

```python
from quantcdn.models.v2_crawler_schedule_request import V2CrawlerScheduleRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2CrawlerScheduleRequest from a JSON string
v2_crawler_schedule_request_instance = V2CrawlerScheduleRequest.from_json(json)
# print the JSON string representation of the object
print(V2CrawlerScheduleRequest.to_json())

# convert the object into a dict
v2_crawler_schedule_request_dict = v2_crawler_schedule_request_instance.to_dict()
# create an instance of V2CrawlerScheduleRequest from a dict
v2_crawler_schedule_request_from_dict = V2CrawlerScheduleRequest.from_dict(v2_crawler_schedule_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


