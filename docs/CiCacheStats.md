# CiCacheStats


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**days** | **int** |  | 
**hits** | **float** | Cache lookups that found an entry. | 
**misses** | **float** | Cache lookups that found no entry. | 
**saves** | **float** | Entries saved. | 
**bytes_in** | **float** | Bytes saved to the cache. | 
**bytes_out** | **float** | Bytes restored from the cache. | 
**hit_rate** | **float** | hits / (hits + misses); null when both are 0. | 

## Example

```python
from quantcdn.models.ci_cache_stats import CiCacheStats

# TODO update the JSON string below
json = "{}"
# create an instance of CiCacheStats from a JSON string
ci_cache_stats_instance = CiCacheStats.from_json(json)
# print the JSON string representation of the object
print(CiCacheStats.to_json())

# convert the object into a dict
ci_cache_stats_dict = ci_cache_stats_instance.to_dict()
# create an instance of CiCacheStats from a dict
ci_cache_stats_from_dict = CiCacheStats.from_dict(ci_cache_stats_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


