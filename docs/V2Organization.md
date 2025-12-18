# V2Organization


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Organization name | 
**machine_name** | **str** | Organization machine name | 
**type** | **str** | Organization type | [optional] 
**region** | **str** | Organization region | [optional] 
**subscription** | **str** | Subscription type | [optional] 
**created_at** | **datetime** | Creation timestamp | [optional] 
**updated_at** | **datetime** | Last update timestamp | [optional] 

## Example

```python
from quantcdn.models.v2_organization import V2Organization

# TODO update the JSON string below
json = "{}"
# create an instance of V2Organization from a JSON string
v2_organization_instance = V2Organization.from_json(json)
# print the JSON string representation of the object
print(V2Organization.to_json())

# convert the object into a dict
v2_organization_dict = v2_organization_instance.to_dict()
# create an instance of V2Organization from a dict
v2_organization_from_dict = V2Organization.from_dict(v2_organization_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


