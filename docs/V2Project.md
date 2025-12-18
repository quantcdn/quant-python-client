# V2Project


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **int** | Project ID | 
**uuid** | **str** | Project UUID | 
**name** | **str** | Project name | 
**machine_name** | **str** | Project machine name | 
**write_token** | **str** | Write token for API access | [optional] 

## Example

```python
from quantcdn.models.v2_project import V2Project

# TODO update the JSON string below
json = "{}"
# create an instance of V2Project from a JSON string
v2_project_instance = V2Project.from_json(json)
# print the JSON string representation of the object
print(V2Project.to_json())

# convert the object into a dict
v2_project_dict = v2_project_instance.to_dict()
# create an instance of V2Project from a dict
v2_project_from_dict = V2Project.from_dict(v2_project_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


