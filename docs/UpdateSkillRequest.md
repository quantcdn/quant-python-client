# UpdateSkillRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**content** | **str** |  | [optional] 
**trigger_condition** | **str** |  | [optional] 
**tags** | **List[str]** |  | [optional] 
**required_tools** | **List[str]** |  | [optional] 
**source** | **object** |  | [optional] 
**files** | **object** |  | [optional] 
**disable_model_invocation** | **bool** |  | [optional] 
**allowed_tools** | **List[str]** |  | [optional] 
**namespace** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.update_skill_request import UpdateSkillRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateSkillRequest from a JSON string
update_skill_request_instance = UpdateSkillRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateSkillRequest.to_json())

# convert the object into a dict
update_skill_request_dict = update_skill_request_instance.to_dict()
# create an instance of UpdateSkillRequest from a dict
update_skill_request_from_dict = UpdateSkillRequest.from_dict(update_skill_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


