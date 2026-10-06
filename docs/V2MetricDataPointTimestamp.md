# V2MetricDataPointTimestamp

Timestamp for this data point (format depends on timestamp_format parameter)

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from quantcdn.models.v2_metric_data_point_timestamp import V2MetricDataPointTimestamp

# TODO update the JSON string below
json = "{}"
# create an instance of V2MetricDataPointTimestamp from a JSON string
v2_metric_data_point_timestamp_instance = V2MetricDataPointTimestamp.from_json(json)
# print the JSON string representation of the object
print(V2MetricDataPointTimestamp.to_json())

# convert the object into a dict
v2_metric_data_point_timestamp_dict = v2_metric_data_point_timestamp_instance.to_dict()
# create an instance of V2MetricDataPointTimestamp from a dict
v2_metric_data_point_timestamp_from_dict = V2MetricDataPointTimestamp.from_dict(v2_metric_data_point_timestamp_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


