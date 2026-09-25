# KVDelete409Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 
**hint** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.kv_delete409_response import KVDelete409Response

# TODO update the JSON string below
json = "{}"
# create an instance of KVDelete409Response from a JSON string
kv_delete409_response_instance = KVDelete409Response.from_json(json)
# print the JSON string representation of the object
print(KVDelete409Response.to_json())

# convert the object into a dict
kv_delete409_response_dict = kv_delete409_response_instance.to_dict()
# create an instance of KVDelete409Response from a dict
kv_delete409_response_from_dict = KVDelete409Response.from_dict(kv_delete409_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


