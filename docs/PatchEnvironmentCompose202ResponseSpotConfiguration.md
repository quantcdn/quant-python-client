# PatchEnvironmentCompose202ResponseSpotConfiguration


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**strategy** | **str** |  | [optional] 
**tolerate_downtime** | **bool** |  | [optional] 

## Example

```python
from quantcdn.models.patch_environment_compose202_response_spot_configuration import PatchEnvironmentCompose202ResponseSpotConfiguration

# TODO update the JSON string below
json = "{}"
# create an instance of PatchEnvironmentCompose202ResponseSpotConfiguration from a JSON string
patch_environment_compose202_response_spot_configuration_instance = PatchEnvironmentCompose202ResponseSpotConfiguration.from_json(json)
# print the JSON string representation of the object
print(PatchEnvironmentCompose202ResponseSpotConfiguration.to_json())

# convert the object into a dict
patch_environment_compose202_response_spot_configuration_dict = patch_environment_compose202_response_spot_configuration_instance.to_dict()
# create an instance of PatchEnvironmentCompose202ResponseSpotConfiguration from a dict
patch_environment_compose202_response_spot_configuration_from_dict = PatchEnvironmentCompose202ResponseSpotConfiguration.from_dict(patch_environment_compose202_response_spot_configuration_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


