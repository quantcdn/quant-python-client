# GetSkill200ResponseSkill


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**skill_id** | **str** |  | [optional] 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**content** | **str** |  | [optional] 
**trigger_condition** | **str** |  | [optional] 
**tags** | **List[str]** |  | [optional] 
**source** | **object** |  | [optional] 
**required_tools** | **List[str]** |  | [optional] 
**files** | **object** |  | [optional] 
**namespace** | **str** |  | [optional] 
**disable_model_invocation** | **bool** |  | [optional] 
**allowed_tools** | **List[str]** |  | [optional] 
**installed_at** | **datetime** |  | [optional] 
**updated_at** | **datetime** |  | [optional] 

## Example

```python
from quantcdn.models.get_skill200_response_skill import GetSkill200ResponseSkill

# TODO update the JSON string below
json = "{}"
# create an instance of GetSkill200ResponseSkill from a JSON string
get_skill200_response_skill_instance = GetSkill200ResponseSkill.from_json(json)
# print the JSON string representation of the object
print(GetSkill200ResponseSkill.to_json())

# convert the object into a dict
get_skill200_response_skill_dict = get_skill200_response_skill_instance.to_dict()
# create an instance of GetSkill200ResponseSkill from a dict
get_skill200_response_skill_from_dict = GetSkill200ResponseSkill.from_dict(get_skill200_response_skill_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


