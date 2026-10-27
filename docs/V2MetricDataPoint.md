# V2MetricDataPoint


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timestamp** | [**V2MetricDataPointTimestamp**](V2MetricDataPointTimestamp.md) |  | 
**value** | **float** | Metric value at this timestamp | 

## Example

```python
from quantcdn.models.v2_metric_data_point import V2MetricDataPoint

# TODO update the JSON string below
json = "{}"
# create an instance of V2MetricDataPoint from a JSON string
v2_metric_data_point_instance = V2MetricDataPoint.from_json(json)
# print the JSON string representation of the object
print(V2MetricDataPoint.to_json())

# convert the object into a dict
v2_metric_data_point_dict = v2_metric_data_point_instance.to_dict()
# create an instance of V2MetricDataPoint from a dict
v2_metric_data_point_from_dict = V2MetricDataPoint.from_dict(v2_metric_data_point_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


