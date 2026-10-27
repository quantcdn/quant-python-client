# KVItemsPurge202Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**status** | **str** |  | [optional] 
**deleted** | **int** |  | [optional] 
**scanned** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.kv_items_purge202_response import KVItemsPurge202Response

# TODO update the JSON string below
json = "{}"
# create an instance of KVItemsPurge202Response from a JSON string
kv_items_purge202_response_instance = KVItemsPurge202Response.from_json(json)
# print the JSON string representation of the object
print(KVItemsPurge202Response.to_json())

# convert the object into a dict
kv_items_purge202_response_dict = kv_items_purge202_response_instance.to_dict()
# create an instance of KVItemsPurge202Response from a dict
kv_items_purge202_response_from_dict = KVItemsPurge202Response.from_dict(kv_items_purge202_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


