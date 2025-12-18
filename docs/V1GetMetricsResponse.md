# V1GetMetricsResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | 
**data** | [**V1GetMetricsResponseData**](V1GetMetricsResponseData.md) |  | 

## Example

```python
from quantcdn.models.v1_get_metrics_response import V1GetMetricsResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1GetMetricsResponse from a JSON string
v1_get_metrics_response_instance = V1GetMetricsResponse.from_json(json)
# print the JSON string representation of the object
print(V1GetMetricsResponse.to_json())

# convert the object into a dict
v1_get_metrics_response_dict = v1_get_metrics_response_instance.to_dict()
# create an instance of V1GetMetricsResponse from a dict
v1_get_metrics_response_from_dict = V1GetMetricsResponse.from_dict(v1_get_metrics_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


