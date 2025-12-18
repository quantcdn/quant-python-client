# ContainerHealthCheck

Container health check configuration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**command** | **List[str]** | The command to run to determine if the container is healthy | [optional] 
**interval** | **int** | Time period (seconds) between health checks | [optional] [default to 30]
**timeout** | **int** | Time period (seconds) to wait for a health check to return | [optional] [default to 5]
**retries** | **int** | Number of times to retry a failed health check | [optional] [default to 3]
**start_period** | **int** | Grace period (seconds) to ignore unhealthy checks after container starts | [optional] 

## Example

```python
from quantcdn.models.container_health_check import ContainerHealthCheck

# TODO update the JSON string below
json = "{}"
# create an instance of ContainerHealthCheck from a JSON string
container_health_check_instance = ContainerHealthCheck.from_json(json)
# print the JSON string representation of the object
print(ContainerHealthCheck.to_json())

# convert the object into a dict
container_health_check_dict = container_health_check_instance.to_dict()
# create an instance of ContainerHealthCheck from a dict
container_health_check_from_dict = ContainerHealthCheck.from_dict(container_health_check_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


