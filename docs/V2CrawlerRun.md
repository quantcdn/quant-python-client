# V2CrawlerRun


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Run ID | 
**crawler_config_id** | **int** | Crawler config ID | 
**project_id** | **int** | Project ID | 
**last_status** | **str** | Run status | 
**task_id** | **str** | Task ID | 
**started_at** | **int** | Start time (Unix timestamp) | [optional] 
**completed_at** | **int** | Completion time (Unix timestamp) | [optional] 
**created_at** | **datetime** | Creation timestamp | [optional] 
**updated_at** | **datetime** | Last update timestamp | [optional] 

## Example

```python
from quantcdn.models.v2_crawler_run import V2CrawlerRun

# TODO update the JSON string below
json = "{}"
# create an instance of V2CrawlerRun from a JSON string
v2_crawler_run_instance = V2CrawlerRun.from_json(json)
# print the JSON string representation of the object
print(V2CrawlerRun.to_json())

# convert the object into a dict
v2_crawler_run_dict = v2_crawler_run_instance.to_dict()
# create an instance of V2CrawlerRun from a dict
v2_crawler_run_from_dict = V2CrawlerRun.from_dict(v2_crawler_run_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


