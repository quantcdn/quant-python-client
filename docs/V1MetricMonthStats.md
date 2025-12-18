# V1MetricMonthStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**total** | **int** |  | 
**month_total** | **int** |  | 
**month_series** | **Dict[str, float]** |  | 
**month_average** | **float** |  | 

## Example

```python
from quantcdn.models.v1_metric_month_stats import V1MetricMonthStats

# TODO update the JSON string below
json = "{}"
# create an instance of V1MetricMonthStats from a JSON string
v1_metric_month_stats_instance = V1MetricMonthStats.from_json(json)
# print the JSON string representation of the object
print(V1MetricMonthStats.to_json())

# convert the object into a dict
v1_metric_month_stats_dict = v1_metric_month_stats_instance.to_dict()
# create an instance of V1MetricMonthStats from a dict
v1_metric_month_stats_from_dict = V1MetricMonthStats.from_dict(v1_metric_month_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


