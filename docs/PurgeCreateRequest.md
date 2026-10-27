# PurgeCreateRequest

Send cache_keys, urls, or both. At least one of them must be non-empty.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cache_keys** | **List[str]** | Cache keys to purge. Optional when urls is set. | [optional] 
**urls** | **List[str]** | URL paths to purge, each starting with a slash (for example /contact). Use /* to purge the whole project. At most 100 per request; a single string is also accepted. The whole list is validated before any purge is sent. Optional when cache_keys is set. | [optional] 
**scope** | **str** | Purge scope for cache_keys (project or org). Not used for urls. | [optional] [default to 'project']
**soft** | **bool** | Soft purge: mark cached content stale instead of removing it. When omitted, the purge is soft (true). Send false for a hard purge. | [optional] [default to True]

## Example

```python
from quantcdn.models.purge_create_request import PurgeCreateRequest

# TODO update the JSON string below
json = "{}"
# create an instance of PurgeCreateRequest from a JSON string
purge_create_request_instance = PurgeCreateRequest.from_json(json)
# print the JSON string representation of the object
print(PurgeCreateRequest.to_json())

# convert the object into a dict
purge_create_request_dict = purge_create_request_instance.to_dict()
# create an instance of PurgeCreateRequest from a dict
purge_create_request_from_dict = PurgeCreateRequest.from_dict(purge_create_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


