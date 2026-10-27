# V2SearchConfig

How the project builds and serves its search index. A PATCH merges one section at a time, so sending only `extractors` leaves `algolia` untouched; within a section a list replaces wholesale.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**extractors** | [**V2SearchExtractors**](V2SearchExtractors.md) |  | [optional] 
**algolia** | [**V2SearchIndexSettings**](V2SearchIndexSettings.md) |  | [optional] 

## Example

```python
from quantcdn.models.v2_search_config import V2SearchConfig

# TODO update the JSON string below
json = "{}"
# create an instance of V2SearchConfig from a JSON string
v2_search_config_instance = V2SearchConfig.from_json(json)
# print the JSON string representation of the object
print(V2SearchConfig.to_json())

# convert the object into a dict
v2_search_config_dict = v2_search_config_instance.to_dict()
# create an instance of V2SearchConfig from a dict
v2_search_config_from_dict = V2SearchConfig.from_dict(v2_search_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


