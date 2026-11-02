# RulesIndexList200ResponseInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**position** | **int** | 0-based index in the stored order. | [optional] 
**managed** | **bool** | True when a template deploy owns the rule in this project. | [optional] 

## Example

```python
from quantcdn.models.rules_index_list200_response_inner import RulesIndexList200ResponseInner

# TODO update the JSON string below
json = "{}"
# create an instance of RulesIndexList200ResponseInner from a JSON string
rules_index_list200_response_inner_instance = RulesIndexList200ResponseInner.from_json(json)
# print the JSON string representation of the object
print(RulesIndexList200ResponseInner.to_json())

# convert the object into a dict
rules_index_list200_response_inner_dict = rules_index_list200_response_inner_instance.to_dict()
# create an instance of RulesIndexList200ResponseInner from a dict
rules_index_list200_response_inner_from_dict = RulesIndexList200ResponseInner.from_dict(rules_index_list200_response_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


