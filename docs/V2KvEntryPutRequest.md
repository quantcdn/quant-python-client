# V2KvEntryPutRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**value** | **object** | Any JSON value. An empty object {} is stored as {}. | 
**secret** | **bool** | Encrypt the value with KMS. Lists show [ENCRYPTED]. Not in a collection with an index on the value (INDEX_FIELD_ENCRYPTED). | [optional] [default to False]
**ttl** | **int** | Seconds until the key expires (60 to 31,536,000). A write without ttl removes any expiry. | [optional] 
**if_absent** | **bool** | Format 2 only. Write only if the key is missing or expired (201). Not with ifVersion. | [optional] 
**if_version** | **str** | Format 2 only. Write only if the current version is this one. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_entry_put_request import V2KvEntryPutRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvEntryPutRequest from a JSON string
v2_kv_entry_put_request_instance = V2KvEntryPutRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvEntryPutRequest.to_json())

# convert the object into a dict
v2_kv_entry_put_request_dict = v2_kv_entry_put_request_instance.to_dict()
# create an instance of V2KvEntryPutRequest from a dict
v2_kv_entry_put_request_from_dict = V2KvEntryPutRequest.from_dict(v2_kv_entry_put_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


