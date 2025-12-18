# V2StoreRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Store name | 

## Example

```python
from quantcdn.models.v2_store_request import V2StoreRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2StoreRequest from a JSON string
v2_store_request_instance = V2StoreRequest.from_json(json)
# print the JSON string representation of the object
print(V2StoreRequest.to_json())

# convert the object into a dict
v2_store_request_dict = v2_store_request_instance.to_dict()
# create an instance of V2StoreRequest from a dict
v2_store_request_from_dict = V2StoreRequest.from_dict(v2_store_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


