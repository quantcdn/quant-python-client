# V2MetricsMeta


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**period** | **str** | The period type for this data | 
**granularity** | **str** | The granularity of data points | 
**start_time** | **str** | Start time of the data range (ISO8601 or Unix timestamp based on timestamp_format parameter) | 
**end_time** | **str** | End time of the data range (ISO8601 or Unix timestamp based on timestamp_format parameter) | 
**metrics** | **List[str]** | List of metrics included in the response | 
**domain** | **str** | Domain filter applied (if any) | [optional] 

## Example

```python
from quantcdn.models.v2_metrics_meta import V2MetricsMeta

# TODO update the JSON string below
json = "{}"
# create an instance of V2MetricsMeta from a JSON string
v2_metrics_meta_instance = V2MetricsMeta.from_json(json)
# print the JSON string representation of the object
print(V2MetricsMeta.to_json())

# convert the object into a dict
v2_metrics_meta_dict = v2_metrics_meta_instance.to_dict()
# create an instance of V2MetricsMeta from a dict
v2_metrics_meta_from_dict = V2MetricsMeta.from_dict(v2_metrics_meta_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


