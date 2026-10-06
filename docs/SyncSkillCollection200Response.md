# SyncSkillCollection200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace** | **str** |  | [optional] 
**synced** | **int** |  | [optional] 
**created** | **int** |  | [optional] 
**failed** | **int** |  | [optional] 
**removed_from_source** | **List[str]** |  | [optional] 
**skills** | **List[object]** |  | [optional] 

## Example

```python
from quantcdn.models.sync_skill_collection200_response import SyncSkillCollection200Response

# TODO update the JSON string below
json = "{}"
# create an instance of SyncSkillCollection200Response from a JSON string
sync_skill_collection200_response_instance = SyncSkillCollection200Response.from_json(json)
# print the JSON string representation of the object
print(SyncSkillCollection200Response.to_json())

# convert the object into a dict
sync_skill_collection200_response_dict = sync_skill_collection200_response_instance.to_dict()
# create an instance of SyncSkillCollection200Response from a dict
sync_skill_collection200_response_from_dict = SyncSkillCollection200Response.from_dict(sync_skill_collection200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


