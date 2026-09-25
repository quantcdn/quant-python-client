# ImportSkillRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**source** | [**ImportSkillRequestSource**](ImportSkillRequestSource.md) |  | 
**name** | **str** |  | [optional] 
**description** | **str** |  | [optional] 
**tags** | **List[str]** |  | [optional] 
**trigger_condition** | **str** |  | [optional] 
**required_tools** | **List[str]** |  | [optional] 
**disable_model_invocation** | **bool** |  | [optional] 
**allowed_tools** | **List[str]** |  | [optional] 
**installed_by** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.import_skill_request import ImportSkillRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ImportSkillRequest from a JSON string
import_skill_request_instance = ImportSkillRequest.from_json(json)
# print the JSON string representation of the object
print(ImportSkillRequest.to_json())

# convert the object into a dict
import_skill_request_dict = import_skill_request_instance.to_dict()
# create an instance of ImportSkillRequest from a dict
import_skill_request_from_dict = ImportSkillRequest.from_dict(import_skill_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


