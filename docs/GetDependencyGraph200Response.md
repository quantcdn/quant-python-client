# GetDependencyGraph200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**task_list_id** | **str** |  | [optional] 
**task_count** | **int** |  | [optional] 
**roots** | **List[str]** | Task IDs with no dependencies | [optional] 
**leaves** | **List[str]** | Task IDs with no dependents | [optional] 
**graph** | **object** | Adjacency list with task summaries, dependsOn, and dependents arrays | [optional] 

## Example

```python
from quantcdn.models.get_dependency_graph200_response import GetDependencyGraph200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetDependencyGraph200Response from a JSON string
get_dependency_graph200_response_instance = GetDependencyGraph200Response.from_json(json)
# print the JSON string representation of the object
print(GetDependencyGraph200Response.to_json())

# convert the object into a dict
get_dependency_graph200_response_dict = get_dependency_graph200_response_instance.to_dict()
# create an instance of GetDependencyGraph200Response from a dict
get_dependency_graph200_response_from_dict = GetDependencyGraph200Response.from_dict(get_dependency_graph200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


