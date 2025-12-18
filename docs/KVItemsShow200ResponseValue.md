# KVItemsShow200ResponseValue

Item value (decoded from JSON if applicable). Returns '[ENCRYPTED]' for secret items.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------

## Example

```python
from quantcdn.models.kv_items_show200_response_value import KVItemsShow200ResponseValue

# TODO update the JSON string below
json = "{}"
# create an instance of KVItemsShow200ResponseValue from a JSON string
kv_items_show200_response_value_instance = KVItemsShow200ResponseValue.from_json(json)
# print the JSON string representation of the object
print(KVItemsShow200ResponseValue.to_json())

# convert the object into a dict
kv_items_show200_response_value_dict = kv_items_show200_response_value_instance.to_dict()
# create an instance of KVItemsShow200ResponseValue from a dict
kv_items_show200_response_value_from_dict = KVItemsShow200ResponseValue.from_dict(kv_items_show200_response_value_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


