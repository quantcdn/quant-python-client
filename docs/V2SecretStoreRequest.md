# V2SecretStoreRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Secret store name | 

## Example

```python
from quantcdn.models.v2_secret_store_request import V2SecretStoreRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2SecretStoreRequest from a JSON string
v2_secret_store_request_instance = V2SecretStoreRequest.from_json(json)
# print the JSON string representation of the object
print(V2SecretStoreRequest.to_json())

# convert the object into a dict
v2_secret_store_request_dict = v2_secret_store_request_instance.to_dict()
# create an instance of V2SecretStoreRequest from a dict
v2_secret_store_request_from_dict = V2SecretStoreRequest.from_dict(v2_secret_store_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


