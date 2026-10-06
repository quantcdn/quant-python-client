# ImportSkillCollectionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace** | **str** |  | 
**source** | [**ImportSkillCollectionRequestSource**](ImportSkillCollectionRequestSource.md) |  | 
**tags** | **List[str]** |  | [optional] 
**installed_by** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.import_skill_collection_request import ImportSkillCollectionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of ImportSkillCollectionRequest from a JSON string
import_skill_collection_request_instance = ImportSkillCollectionRequest.from_json(json)
# print the JSON string representation of the object
print(ImportSkillCollectionRequest.to_json())

# convert the object into a dict
import_skill_collection_request_dict = import_skill_collection_request_instance.to_dict()
# create an instance of ImportSkillCollectionRequest from a dict
import_skill_collection_request_from_dict = ImportSkillCollectionRequest.from_dict(import_skill_collection_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


