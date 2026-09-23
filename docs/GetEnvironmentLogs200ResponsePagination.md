# GetEnvironmentLogs200ResponsePagination


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**limit** | **int** | Page size that was applied | [optional] 
**has_more** | **bool** | True when another page is available | [optional] 
**next_token** | **str** | Token for the next page. Present only when hasMore is true. | [optional] 
**total** | **int** | Total events in the time range. Present only when includeTotal&#x3D;true. | [optional] 
**total_pages** | **int** | ceil(total / limit). Present only when includeTotal&#x3D;true. | [optional] 

## Example

```python
from quantcdn.models.get_environment_logs200_response_pagination import GetEnvironmentLogs200ResponsePagination

# TODO update the JSON string below
json = "{}"
# create an instance of GetEnvironmentLogs200ResponsePagination from a JSON string
get_environment_logs200_response_pagination_instance = GetEnvironmentLogs200ResponsePagination.from_json(json)
# print the JSON string representation of the object
print(GetEnvironmentLogs200ResponsePagination.to_json())

# convert the object into a dict
get_environment_logs200_response_pagination_dict = get_environment_logs200_response_pagination_instance.to_dict()
# create an instance of GetEnvironmentLogs200ResponsePagination from a dict
get_environment_logs200_response_pagination_from_dict = GetEnvironmentLogs200ResponsePagination.from_dict(get_environment_logs200_response_pagination_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


