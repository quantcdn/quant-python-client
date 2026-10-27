# V2KvIndexRequest

An index definition. Definitions are immutable: to change one, drop the index and declare it again.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Unique in the store. | 
**collection** | **str** | A collection, or a pattern where * as one whole segment matches exactly one segment (customer:*:world). At most 512 UTF-8 bytes. | 
**fields** | **List[str]** | Top-level fields of a plaintext JSON object value (0-3). A unique index needs at least one. A field that a ledger on the collection marks as personal cannot be indexed (INDEX_FIELD_ENCRYPTED). | [optional] 
**sort_by** | **str** | Optional single sort field. | [optional] 
**unique** | **bool** | One key per value. Enables KV_indexes_lookup. Not allowed on a ledger collection (LEDGER_INDEX_KIND). | [optional] [default to False]
**count** | **bool** | Keeps a live count per value. Enables KV_indexes_count. Not allowed on a ledger collection (LEDGER_INDEX_KIND) or on items with a ttl (COUNT_WITH_TTL). | [optional] [default to False]

## Example

```python
from quantcdn.models.v2_kv_index_request import V2KvIndexRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvIndexRequest from a JSON string
v2_kv_index_request_instance = V2KvIndexRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvIndexRequest.to_json())

# convert the object into a dict
v2_kv_index_request_dict = v2_kv_index_request_instance.to_dict()
# create an instance of V2KvIndexRequest from a dict
v2_kv_index_request_from_dict = V2KvIndexRequest.from_dict(v2_kv_index_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


