# V2StoreItemUpdateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **str** | Item value (can be JSON string) | 
**secret** | **bool** | Store as secret with KMS encryption. Note: Encryption status cannot be changed after initial creation - this value is preserved from the original item. | [optional] 

## Example

```python
from quantcdn.models.v2_store_item_update_request import V2StoreItemUpdateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2StoreItemUpdateRequest from a JSON string
v2_store_item_update_request_instance = V2StoreItemUpdateRequest.from_json(json)
# print the JSON string representation of the object
print(V2StoreItemUpdateRequest.to_json())

# convert the object into a dict
v2_store_item_update_request_dict = v2_store_item_update_request_instance.to_dict()
# create an instance of V2StoreItemUpdateRequest from a dict
v2_store_item_update_request_from_dict = V2StoreItemUpdateRequest.from_dict(v2_store_item_update_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


