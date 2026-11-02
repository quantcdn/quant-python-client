# ProjectsDelete409Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**error** | **bool** |  | [optional] 
**message** | **str** |  | [optional] 
**code** | **str** |  | [optional] 
**retryable** | **bool** |  | [optional] 
**stores** | **List[str]** |  | [optional] 

## Example

```python
from quantcdn.models.projects_delete409_response import ProjectsDelete409Response

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectsDelete409Response from a JSON string
projects_delete409_response_instance = ProjectsDelete409Response.from_json(json)
# print the JSON string representation of the object
print(ProjectsDelete409Response.to_json())

# convert the object into a dict
projects_delete409_response_dict = projects_delete409_response_instance.to_dict()
# create an instance of ProjectsDelete409Response from a dict
projects_delete409_response_from_dict = ProjectsDelete409Response.from_dict(projects_delete409_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


