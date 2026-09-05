# AttachOrgResourceRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**application** | **str** |  | 
**environment** | **str** |  | 
**env_var_prefix** | **str** | Namespaces every injected variable, so MEDIA yields MEDIA_S3_BUCKET | [optional] 

## Example

```python
from quantcdn.models.attach_org_resource_request import AttachOrgResourceRequest

# TODO update the JSON string below
json = "{}"
# create an instance of AttachOrgResourceRequest from a JSON string
attach_org_resource_request_instance = AttachOrgResourceRequest.from_json(json)
# print the JSON string representation of the object
print(AttachOrgResourceRequest.to_json())

# convert the object into a dict
attach_org_resource_request_dict = attach_org_resource_request_instance.to_dict()
# create an instance of AttachOrgResourceRequest from a dict
attach_org_resource_request_from_dict = AttachOrgResourceRequest.from_dict(attach_org_resource_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


