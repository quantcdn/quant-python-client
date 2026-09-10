# ImportSkillCollection201Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace** | **str** |  | [optional] 
**imported** | **int** |  | [optional] 
**failed** | **int** |  | [optional] 
**skills** | **List[object]** |  | [optional] 
**errors** | **List[object]** |  | [optional] 

## Example

```python
from quantcdn.models.import_skill_collection201_response import ImportSkillCollection201Response

# TODO update the JSON string below
json = "{}"
# create an instance of ImportSkillCollection201Response from a JSON string
import_skill_collection201_response_instance = ImportSkillCollection201Response.from_json(json)
# print the JSON string representation of the object
print(ImportSkillCollection201Response.to_json())

# convert the object into a dict
import_skill_collection201_response_dict = import_skill_collection201_response_instance.to_dict()
# create an instance of ImportSkillCollection201Response from a dict
import_skill_collection201_response_from_dict = ImportSkillCollection201Response.from_dict(import_skill_collection201_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


