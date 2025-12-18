# ContainerSecretsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | The environment variable name to be set in the container | 
**value_from** | **str** | The key of the secret in the environment&#39;s &#39;app-secrets&#39; store | 

## Example

```python
from quantcdn.models.container_secrets_inner import ContainerSecretsInner

# TODO update the JSON string below
json = "{}"
# create an instance of ContainerSecretsInner from a JSON string
container_secrets_inner_instance = ContainerSecretsInner.from_json(json)
# print the JSON string representation of the object
print(ContainerSecretsInner.to_json())

# convert the object into a dict
container_secrets_inner_dict = container_secrets_inner_instance.to_dict()
# create an instance of ContainerSecretsInner from a dict
container_secrets_inner_from_dict = ContainerSecretsInner.from_dict(container_secrets_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


