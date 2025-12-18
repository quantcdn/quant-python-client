# V1WafLogListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**draw** | **int** |  | 
**i_total_records** | **int** |  | 
**i_total_display_records** | **int** |  | 
**aa_data** | [**List[V1WafLogItem]**](V1WafLogItem.md) |  | 

## Example

```python
from quantcdn.models.v1_waf_log_list_response import V1WafLogListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V1WafLogListResponse from a JSON string
v1_waf_log_list_response_instance = V1WafLogListResponse.from_json(json)
# print the JSON string representation of the object
print(V1WafLogListResponse.to_json())

# convert the object into a dict
v1_waf_log_list_response_dict = v1_waf_log_list_response_instance.to_dict()
# create an instance of V1WafLogListResponse from a dict
v1_waf_log_list_response_from_dict = V1WafLogListResponse.from_dict(v1_waf_log_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


