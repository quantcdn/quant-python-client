# ImportSkillCollectionRequestSource


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**repo** | **str** |  | 
**path** | **str** |  | [optional] 
**version** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.import_skill_collection_request_source import ImportSkillCollectionRequestSource

# TODO update the JSON string below
json = "{}"
# create an instance of ImportSkillCollectionRequestSource from a JSON string
import_skill_collection_request_source_instance = ImportSkillCollectionRequestSource.from_json(json)
# print the JSON string representation of the object
print(ImportSkillCollectionRequestSource.to_json())

# convert the object into a dict
import_skill_collection_request_source_dict = import_skill_collection_request_source_instance.to_dict()
# create an instance of ImportSkillCollectionRequestSource from a dict
import_skill_collection_request_source_from_dict = ImportSkillCollectionRequestSource.from_dict(import_skill_collection_request_source_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


