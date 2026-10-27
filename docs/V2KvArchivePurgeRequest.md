# V2KvArchivePurgeRequest

dryRun defaults to true. confirm must equal the store name, also for a dry run (else 400 CONFIRMATION_REQUIRED). requestedBy is set by Quant: a body that has the key requestedBy is 400 VALIDATION. An unknown field is 400 VALIDATION.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**dry_run** | **bool** | true: report only. false: start the purge. | [optional] [default to True]
**confirm** | **str** | The store name, exactly. | 
**reason** | **str** | Optional note kept with the purge and the receipt. No control characters. It is never echoed in an error message. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_archive_purge_request import V2KvArchivePurgeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvArchivePurgeRequest from a JSON string
v2_kv_archive_purge_request_instance = V2KvArchivePurgeRequest.from_json(json)
# print the JSON string representation of the object
print(V2KvArchivePurgeRequest.to_json())

# convert the object into a dict
v2_kv_archive_purge_request_dict = v2_kv_archive_purge_request_instance.to_dict()
# create an instance of V2KvArchivePurgeRequest from a dict
v2_kv_archive_purge_request_from_dict = V2KvArchivePurgeRequest.from_dict(v2_kv_archive_purge_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


