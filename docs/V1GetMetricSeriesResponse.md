# V1GetMetricSeriesResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**data** | [**V1GetMetricSeriesResponseData**](V1GetMetricSeriesResponseData.md) |  | 

## Example

```python
from quantcdn.models.v1_get_metric_series_response import V1GetMetricSeriesResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1GetMetricSeriesResponse from a JSON string
v1_get_metric_series_response_instance = V1GetMetricSeriesResponse.from_json(json)
# print the JSON string representation of the object
print(V1GetMetricSeriesResponse.to_json())

# convert the object into a dict
v1_get_metric_series_response_dict = v1_get_metric_series_response_instance.to_dict()
# create an instance of V1GetMetricSeriesResponse from a dict
v1_get_metric_series_response_from_dict = V1GetMetricSeriesResponse.from_dict(v1_get_metric_series_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


