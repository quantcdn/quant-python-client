# V2MetricData


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**series** | [**List[V2MetricDataPoint]**](V2MetricDataPoint.md) | Time series data points | 
**period_total** | **float** | Total value for the period | 
**all_time_total** | **float** | All-time total value | 
**period_average** | **float** | Average value per time unit in the period | 

## Example

```python
from quantcdn.models.v2_metric_data import V2MetricData

# TODO update the JSON string below
json = "{}"
# create an instance of V2MetricData from a JSON string
v2_metric_data_instance = V2MetricData.from_json(json)
# print the JSON string representation of the object
print(V2MetricData.to_json())

# convert the object into a dict
v2_metric_data_dict = v2_metric_data_instance.to_dict()
# create an instance of V2MetricData from a dict
v2_metric_data_from_dict = V2MetricData.from_dict(v2_metric_data_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


