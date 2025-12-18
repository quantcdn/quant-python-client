# V2StoreItemRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** | Item key | 
**value** | **str** | Item value (can be JSON string) | 
**secret** | **bool** | Store as secret with KMS encryption. Secrets cannot be retrieved via GET operations (returns [ENCRYPTED]). Ideal for API keys, passwords, and credentials. | [optional] [default to False]

## Example

```python
from quantcdn.models.v2_store_item_request import V2StoreItemRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2StoreItemRequest from a JSON string
v2_store_item_request_instance = V2StoreItemRequest.from_json(json)
# print the JSON string representation of the object
print(V2StoreItemRequest.to_json())

# convert the object into a dict
v2_store_item_request_dict = v2_store_item_request_instance.to_dict()
# create an instance of V2StoreItemRequest from a dict
v2_store_item_request_from_dict = V2StoreItemRequest.from_dict(v2_store_item_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


