# V2KvEntryPutResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**key** | **str** |  | 
**value** | **object** | The stored JSON value. | [optional] 
**status** | **str** |  | 
**message** | **str** |  | 
**created_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 
**expires_at** | **int** | Epoch seconds. Absent without ttl. | [optional] 
**version** | **str** | Format 2 stores only. The new version. | [optional] 
**conditional** | **bool** | Format 2 stores. True when the write had ifAbsent or ifVersion. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_entry_put_response import V2KvEntryPutResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvEntryPutResponse from a JSON string
v2_kv_entry_put_response_instance = V2KvEntryPutResponse.from_json(json)
# print the JSON string representation of the object
print(V2KvEntryPutResponse.to_json())

# convert the object into a dict
v2_kv_entry_put_response_dict = v2_kv_entry_put_response_instance.to_dict()
# create an instance of V2KvEntryPutResponse from a dict
v2_kv_entry_put_response_from_dict = V2KvEntryPutResponse.from_dict(v2_kv_entry_put_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


