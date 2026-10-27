# V2SearchIndexSettings

Index settings. Named `algolia` for historical reasons; they are applied to whichever backend the project's platform_mode selects, including Typesense.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**facets** | **List[str]** | Fields offered as facets | [optional] 
**searchable_attributes** | **List[str]** | Fields a query matches against | [optional] 
**sortable_attributes** | **List[str]** | Fields results may be sorted by | [optional] 
**custom_ranking** | **List[str]** | Ranking rules, e.g. asc(title) | [optional] 
**synonyms** | **str** | Newline-separated synonym groups, each a comma-separated list of terms | [optional] 

## Example

```python
from quantcdn.models.v2_search_index_settings import V2SearchIndexSettings

# TODO update the JSON string below
json = "{}"
# create an instance of V2SearchIndexSettings from a JSON string
v2_search_index_settings_instance = V2SearchIndexSettings.from_json(json)
# print the JSON string representation of the object
print(V2SearchIndexSettings.to_json())

# convert the object into a dict
v2_search_index_settings_dict = v2_search_index_settings_instance.to_dict()
# create an instance of V2SearchIndexSettings from a dict
v2_search_index_settings_from_dict = V2SearchIndexSettings.from_dict(v2_search_index_settings_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


