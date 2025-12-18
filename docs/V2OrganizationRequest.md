# V2OrganizationRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Organization name | 
**machine_name** | **str** | Organization machine name | 

## Example

```python
from quantcdn.models.v2_organization_request import V2OrganizationRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2OrganizationRequest from a JSON string
v2_organization_request_instance = V2OrganizationRequest.from_json(json)
# print the JSON string representation of the object
print(V2OrganizationRequest.to_json())

# convert the object into a dict
v2_organization_request_dict = v2_organization_request_instance.to_dict()
# create an instance of V2OrganizationRequest from a dict
v2_organization_request_from_dict = V2OrganizationRequest.from_dict(v2_organization_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


