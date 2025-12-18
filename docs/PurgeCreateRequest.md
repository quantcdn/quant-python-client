# PurgeCreateRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cache_keys** | **List[str]** | Cache keys to purge | 
**urls** | **List[str]** | URLs to purge | [optional] 
**scope** | **str** | Purge scope (org or project) | [default to 'project']
**soft** | **bool** | Soft purge | [optional] [default to True]

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


