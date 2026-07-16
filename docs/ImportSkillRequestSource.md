# ImportSkillRequestSource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**url** | **str** |  | [optional] 
**repo** | **str** |  | [optional] 
**path** | **str** |  | [optional] 
**version** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.import_skill_request_source import ImportSkillRequestSource

# TODO update the JSON string below
json = "{}"
# create an instance of ImportSkillRequestSource from a JSON string
import_skill_request_source_instance = ImportSkillRequestSource.from_json(json)
# print the JSON string representation of the object
print(ImportSkillRequestSource.to_json())

# convert the object into a dict
import_skill_request_source_dict = import_skill_request_source_instance.to_dict()
# create an instance of ImportSkillRequestSource from a dict
import_skill_request_source_from_dict = ImportSkillRequestSource.from_dict(import_skill_request_source_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


