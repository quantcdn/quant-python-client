# V2ProjectRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Project name | [optional] 
**machine_name** | **str** | Project machine name | [optional] 
**region** | **str** | Project region | [optional] 
**allow_query_params** | **bool** | Allow query parameters | [optional] 
**disable_revisions** | **bool** | Disable revisions | [optional] 
**basic_auth_username** | **str** | Basic auth username | [optional] 
**basic_auth_password** | **str** | Basic auth password | [optional] 
**basic_auth_preview_only** | **bool** | Apply basic auth to preview domain only | [optional] [default to False]

## Example

```python
from quantcdn.models.v2_project_request import V2ProjectRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2ProjectRequest from a JSON string
v2_project_request_instance = V2ProjectRequest.from_json(json)
# print the JSON string representation of the object
print(V2ProjectRequest.to_json())

# convert the object into a dict
v2_project_request_dict = v2_project_request_instance.to_dict()
# create an instance of V2ProjectRequest from a dict
v2_project_request_from_dict = V2ProjectRequest.from_dict(v2_project_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


