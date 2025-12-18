# KVItemsShow200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | [optional] 
**value** | [**KVItemsShow200ResponseValue**](KVItemsShow200ResponseValue.md) |  | [optional] 

## Example

```python
from quantcdn.models.kv_items_show200_response import KVItemsShow200Response

# TODO update the JSON string below
json = "{}"
# create an instance of KVItemsShow200Response from a JSON string
kv_items_show200_response_instance = KVItemsShow200Response.from_json(json)
# print the JSON string representation of the object
print(KVItemsShow200Response.to_json())

# convert the object into a dict
kv_items_show200_response_dict = kv_items_show200_response_instance.to_dict()
# create an instance of KVItemsShow200Response from a dict
kv_items_show200_response_from_dict = KVItemsShow200Response.from_dict(kv_items_show200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


