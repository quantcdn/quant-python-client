# ProjectsDelete503Response


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
from quantcdn.models.projects_delete503_response import ProjectsDelete503Response

# TODO update the JSON string below
json = "{}"
# create an instance of ProjectsDelete503Response from a JSON string
projects_delete503_response_instance = ProjectsDelete503Response.from_json(json)
# print the JSON string representation of the object
print(ProjectsDelete503Response.to_json())

# convert the object into a dict
projects_delete503_response_dict = projects_delete503_response_instance.to_dict()
# create an instance of ProjectsDelete503Response from a dict
projects_delete503_response_from_dict = ProjectsDelete503Response.from_dict(projects_delete503_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


