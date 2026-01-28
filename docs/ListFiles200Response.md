# ListFiles200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**files** | [**List[ListFiles200ResponseFilesInner]**](ListFiles200ResponseFilesInner.md) |  | [optional] 
**next_cursor** | **str** | Cursor for next page | [optional] 
**has_more** | **bool** | True if more results available | [optional] 

## Example

```python
from quantcdn.models.list_files200_response import ListFiles200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ListFiles200Response from a JSON string
list_files200_response_instance = ListFiles200Response.from_json(json)
# print the JSON string representation of the object
print(ListFiles200Response.to_json())

# convert the object into a dict
list_files200_response_dict = list_files200_response_instance.to_dict()
# create an instance of ListFiles200Response from a dict
list_files200_response_from_dict = ListFiles200Response.from_dict(list_files200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


