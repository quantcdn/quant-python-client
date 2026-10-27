# V2KvEntryDeleteResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | 
**status** | **str** |  | 
**message** | **str** |  | 
**conditional** | **bool** | Format 2 stores. True when the delete had if_version. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_entry_delete_response import V2KvEntryDeleteResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvEntryDeleteResponse from a JSON string
v2_kv_entry_delete_response_instance = V2KvEntryDeleteResponse.from_json(json)
# print the JSON string representation of the object
print(V2KvEntryDeleteResponse.to_json())

# convert the object into a dict
v2_kv_entry_delete_response_dict = v2_kv_entry_delete_response_instance.to_dict()
# create an instance of V2KvEntryDeleteResponse from a dict
v2_kv_entry_delete_response_from_dict = V2KvEntryDeleteResponse.from_dict(v2_kv_entry_delete_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


