# KVLinkToProjectRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**project_id** | **int** | Target project ID to link to | 

## Example

```python
from quantcdn.models.kv_link_to_project_request import KVLinkToProjectRequest

# TODO update the JSON string below
json = "{}"
# create an instance of KVLinkToProjectRequest from a JSON string
kv_link_to_project_request_instance = KVLinkToProjectRequest.from_json(json)
# print the JSON string representation of the object
print(KVLinkToProjectRequest.to_json())

# convert the object into a dict
kv_link_to_project_request_dict = kv_link_to_project_request_instance.to_dict()
# create an instance of KVLinkToProjectRequest from a dict
kv_link_to_project_request_from_dict = KVLinkToProjectRequest.from_dict(kv_link_to_project_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


