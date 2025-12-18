# ContainerOriginProtectionConfig

Extended origin protection configuration with IP allow list support

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**enabled** | **bool** | Whether origin protection is enabled. Defaults to true if this config object is provided. | [optional] [default to True]
**ip_allow** | **List[str]** | List of IP addresses or CIDR ranges that can bypass origin protection for direct access (e.g., VPN IPs) | [optional] 

## Example

```python
from quantcdn.models.container_origin_protection_config import ContainerOriginProtectionConfig

# TODO update the JSON string below
json = "{}"
# create an instance of ContainerOriginProtectionConfig from a JSON string
container_origin_protection_config_instance = ContainerOriginProtectionConfig.from_json(json)
# print the JSON string representation of the object
print(ContainerOriginProtectionConfig.to_json())

# convert the object into a dict
container_origin_protection_config_dict = container_origin_protection_config_instance.to_dict()
# create an instance of ContainerOriginProtectionConfig from a dict
container_origin_protection_config_from_dict = ContainerOriginProtectionConfig.from_dict(container_origin_protection_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


