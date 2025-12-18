# KVItemsCreate200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**success** | **bool** |  | [optional] 
**key** | **str** |  | [optional] 
**value** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.kv_items_create200_response import KVItemsCreate200Response

# TODO update the JSON string below
json = "{}"
# create an instance of KVItemsCreate200Response from a JSON string
kv_items_create200_response_instance = KVItemsCreate200Response.from_json(json)
# print the JSON string representation of the object
print(KVItemsCreate200Response.to_json())

# convert the object into a dict
kv_items_create200_response_dict = kv_items_create200_response_instance.to_dict()
# create an instance of KVItemsCreate200Response from a dict
kv_items_create200_response_from_dict = KVItemsCreate200Response.from_dict(kv_items_create200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


