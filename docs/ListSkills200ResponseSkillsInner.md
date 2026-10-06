# ListSkills200ResponseSkillsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**skill_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**tags** | **List[str]** |  | [optional] 
**source** | **object** |  | [optional] 
**trigger_condition** | **str** |  | [optional] 
**namespace** | **str** |  | [optional] 
**installed_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.list_skills200_response_skills_inner import ListSkills200ResponseSkillsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ListSkills200ResponseSkillsInner from a JSON string
list_skills200_response_skills_inner_instance = ListSkills200ResponseSkillsInner.from_json(json)
# print the JSON string representation of the object
print(ListSkills200ResponseSkillsInner.to_json())

# convert the object into a dict
list_skills200_response_skills_inner_dict = list_skills200_response_skills_inner_instance.to_dict()
# create an instance of ListSkills200ResponseSkillsInner from a dict
list_skills200_response_skills_inner_from_dict = ListSkills200ResponseSkillsInner.from_dict(list_skills200_response_skills_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


