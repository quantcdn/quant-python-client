# V1MetricMinuteStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** |  | 
**minute_total** | **int** |  | 
**minute_series** | **Dict[str, float]** |  | 
**minute_average** | **float** |  | 

## Example

```python
from quantcdn.models.v1_metric_minute_stats import V1MetricMinuteStats

# TODO update the JSON string below
json = "{}"
# create an instance of V1MetricMinuteStats from a JSON string
v1_metric_minute_stats_instance = V1MetricMinuteStats.from_json(json)
# print the JSON string representation of the object
print(V1MetricMinuteStats.to_json())

# convert the object into a dict
v1_metric_minute_stats_dict = v1_metric_minute_stats_instance.to_dict()
# create an instance of V1MetricMinuteStats from a dict
v1_metric_minute_stats_from_dict = V1MetricMinuteStats.from_dict(v1_metric_minute_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


