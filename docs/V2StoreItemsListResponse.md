# V2StoreItemsListResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**data** | **List[str]** | List of item keys | [optional] 
**next_cursor** | **str** | Cursor for next page of results | [optional] 

## Example

```python
from quantcdn.models.v2_store_items_list_response import V2StoreItemsListResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V2StoreItemsListResponse from a JSON string
v2_store_items_list_response_instance = V2StoreItemsListResponse.from_json(json)
# print the JSON string representation of the object
print(V2StoreItemsListResponse.to_json())

# convert the object into a dict
v2_store_items_list_response_dict = v2_store_items_list_response_instance.to_dict()
# create an instance of V2StoreItemsListResponse from a dict
v2_store_items_list_response_from_dict = V2StoreItemsListResponse.from_dict(v2_store_items_list_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


