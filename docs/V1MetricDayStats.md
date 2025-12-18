# V1MetricDayStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** |  | 
**day_total** | **int** |  | 
**day_series** | **Dict[str, float]** |  | 
**day_average** | **float** |  | 

## Example

```python
from quantcdn.models.v1_metric_day_stats import V1MetricDayStats

# TODO update the JSON string below
json = "{}"
# create an instance of V1MetricDayStats from a JSON string
v1_metric_day_stats_instance = V1MetricDayStats.from_json(json)
# print the JSON string representation of the object
print(V1MetricDayStats.to_json())

# convert the object into a dict
v1_metric_day_stats_dict = v1_metric_day_stats_instance.to_dict()
# create an instance of V1MetricDayStats from a dict
v1_metric_day_stats_from_dict = V1MetricDayStats.from_dict(v1_metric_day_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


