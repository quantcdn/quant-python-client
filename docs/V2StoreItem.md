# V2StoreItem


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | Item key | 
**value** | **str** | Item value (can be JSON string) | 

## Example

```python
from quantcdn.models.v2_store_item import V2StoreItem

# TODO update the JSON string below
json = "{}"
# create an instance of V2StoreItem from a JSON string
v2_store_item_instance = V2StoreItem.from_json(json)
# print the JSON string representation of the object
print(V2StoreItem.to_json())

# convert the object into a dict
v2_store_item_dict = v2_store_item_instance.to_dict()
# create an instance of V2StoreItem from a dict
v2_store_item_from_dict = V2StoreItem.from_dict(v2_store_item_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


