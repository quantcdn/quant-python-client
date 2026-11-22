# CiRunnerPoolConfigConnection


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider** | **str** |  | [optional] 
**installation_id** | **int** |  | [optional] 
**github_org** | **str** |  | [optional] 
**app_id** | **int** | The GitHub App that owns the installation. | [optional] 
**status** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.ci_runner_pool_config_connection import CiRunnerPoolConfigConnection

# TODO update the JSON string below
json = "{}"
# create an instance of CiRunnerPoolConfigConnection from a JSON string
ci_runner_pool_config_connection_instance = CiRunnerPoolConfigConnection.from_json(json)
# print the JSON string representation of the object
print(CiRunnerPoolConfigConnection.to_json())

# convert the object into a dict
ci_runner_pool_config_connection_dict = ci_runner_pool_config_connection_instance.to_dict()
# create an instance of CiRunnerPoolConfigConnection from a dict
ci_runner_pool_config_connection_from_dict = CiRunnerPoolConfigConnection.from_dict(ci_runner_pool_config_connection_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


