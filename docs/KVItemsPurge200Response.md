# KVItemsPurge200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**deleted** | **int** |  | [optional] 
**scanned** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.kv_items_purge200_response import KVItemsPurge200Response

# TODO update the JSON string below
json = "{}"
# create an instance of KVItemsPurge200Response from a JSON string
kv_items_purge200_response_instance = KVItemsPurge200Response.from_json(json)
# print the JSON string representation of the object
print(KVItemsPurge200Response.to_json())

# convert the object into a dict
kv_items_purge200_response_dict = kv_items_purge200_response_instance.to_dict()
# create an instance of KVItemsPurge200Response from a dict
kv_items_purge200_response_from_dict = KVItemsPurge200Response.from_dict(kv_items_purge200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


