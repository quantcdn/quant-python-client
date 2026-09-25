# CreateSkillRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**description** | **str** |  | [optional] 
**content** | **str** |  | 
**trigger_condition** | **str** |  | 
**tags** | **List[str]** |  | [optional] 
**required_tools** | **List[str]** |  | [optional] 
**namespace** | **str** |  | [optional] 
**files** | **object** |  | [optional] 
**disable_model_invocation** | **bool** |  | [optional] 
**allowed_tools** | **List[str]** |  | [optional] 
**installed_by** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.create_skill_request import CreateSkillRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateSkillRequest from a JSON string
create_skill_request_instance = CreateSkillRequest.from_json(json)
# print the JSON string representation of the object
print(CreateSkillRequest.to_json())

# convert the object into a dict
create_skill_request_dict = create_skill_request_instance.to_dict()
# create an instance of CreateSkillRequest from a dict
create_skill_request_from_dict = CreateSkillRequest.from_dict(create_skill_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


