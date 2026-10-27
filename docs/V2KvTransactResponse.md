# V2KvTransactResponse


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**conditional** | **bool** |  | 
**versions** | **Dict[str, str]** | The new version of each set and increment key. | 
**replayed** | **bool** | True when an earlier request with the same idempotencyKey applied the operations. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_transact_response import V2KvTransactResponse

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvTransactResponse from a JSON string
v2_kv_transact_response_instance = V2KvTransactResponse.from_json(json)
# print the JSON string representation of the object
print(V2KvTransactResponse.to_json())

# convert the object into a dict
v2_kv_transact_response_dict = v2_kv_transact_response_instance.to_dict()
# create an instance of V2KvTransactResponse from a dict
v2_kv_transact_response_from_dict = V2KvTransactResponse.from_dict(v2_kv_transact_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


