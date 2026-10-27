# V2KvBatchGetRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**keys** | **List[str]** | 1 to 100 keys. Duplicates are read once. More than 100 is 400 LIMIT_EXCEEDED. | 
**consistent** | **bool** | false for an eventually consistent read. | [optional] [default to True]

## Example

```python
from quantcdn.models.v2_kv_batch_get_request import V2KvBatchGetRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvBatchGetRequest from a JSON string
v2_kv_batch_get_request_instance = V2KvBatchGetRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvBatchGetRequest.to_json())

# convert the object into a dict
v2_kv_batch_get_request_dict = v2_kv_batch_get_request_instance.to_dict()
# create an instance of V2KvBatchGetRequest from a dict
v2_kv_batch_get_request_from_dict = V2KvBatchGetRequest.from_dict(v2_kv_batch_get_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


