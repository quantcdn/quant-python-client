# V2KvTransactRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**idempotency_key** | **str** | A repeat of the same operations within 24 hours returns the first result with replayed true; other operations with the same key fail VALIDATION. Send it to make a lost-connection 503 retryable. | [optional] 
**operations** | [**List[V2KvTransactOperation]**](V2KvTransactOperation.md) | 1 to 25 operations on different keys. More than 25 is 400 LIMIT_EXCEEDED. | 

## Example

```python
from quantcdn.models.v2_kv_transact_request import V2KvTransactRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvTransactRequest from a JSON string
v2_kv_transact_request_instance = V2KvTransactRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvTransactRequest.to_json())

# convert the object into a dict
v2_kv_transact_request_dict = v2_kv_transact_request_instance.to_dict()
# create an instance of V2KvTransactRequest from a dict
v2_kv_transact_request_from_dict = V2KvTransactRequest.from_dict(v2_kv_transact_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


