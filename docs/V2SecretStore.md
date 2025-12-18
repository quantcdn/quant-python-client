# V2SecretStore


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** | Secret store ID | 
**name** | **str** | Secret store name | 

## Example

```python
from quantcdn.models.v2_secret_store import V2SecretStore

# TODO update the JSON string below
json = "{}"
# create an instance of V2SecretStore from a JSON string
v2_secret_store_instance = V2SecretStore.from_json(json)
# print the JSON string representation of the object
print(V2SecretStore.to_json())

# convert the object into a dict
v2_secret_store_dict = v2_secret_store_instance.to_dict()
# create an instance of V2SecretStore from a dict
v2_secret_store_from_dict = V2SecretStore.from_dict(v2_secret_store_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


