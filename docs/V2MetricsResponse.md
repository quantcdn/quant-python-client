# V2MetricsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**meta** | [**V2MetricsMeta**](V2MetricsMeta.md) |  | 
**data** | [**Dict[str, V2MetricData]**](V2MetricData.md) | Metrics data keyed by metric name | 

## Example

```python
from quantcdn.models.v2_metrics_response import V2MetricsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V2MetricsResponse from a JSON string
v2_metrics_response_instance = V2MetricsResponse.from_json(json)
# print the JSON string representation of the object
print(V2MetricsResponse.to_json())

# convert the object into a dict
v2_metrics_response_dict = v2_metrics_response_instance.to_dict()
# create an instance of V2MetricsResponse from a dict
v2_metrics_response_from_dict = V2MetricsResponse.from_dict(v2_metrics_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


