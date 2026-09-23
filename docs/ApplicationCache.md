# ApplicationCache

Managed Valkey cache configuration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cache_endpoint** | **str** | Cache cluster endpoint | [optional] 
**cache_identifier** | **str** | Cache cluster identifier | [optional] 
**data_storage_max_gb** | **int** | Maximum cache storage in GB | [optional] 

## Example

```python
from quantcdn.models.application_cache import ApplicationCache

# TODO update the JSON string below
json = "{}"
# create an instance of ApplicationCache from a JSON string
application_cache_instance = ApplicationCache.from_json(json)
# print the JSON string representation of the object
print(ApplicationCache.to_json())

# convert the object into a dict
application_cache_dict = application_cache_instance.to_dict()
# create an instance of ApplicationCache from a dict
application_cache_from_dict = ApplicationCache.from_dict(application_cache_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


