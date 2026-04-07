# EnvironmentResponse

Environment response schema with runtime details

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**env_name** | **str** | Environment name | 
**status** | **str** | Environment status | [optional] [readonly] 
**running_count** | **int** | Number of running tasks | [optional] [readonly] 
**desired_count** | **int** | Desired number of tasks | [optional] [readonly] 
**min_capacity** | **int** | Minimum capacity for autoscaling | [optional] 
**max_capacity** | **int** | Maximum capacity for autoscaling | [optional] 
**public_ip_address** | **str** | Public IP address for SSH access | [optional] [readonly] 
**deployment_status** | **str** | Current deployment status | [optional] [readonly] 
**deployment_failure_type** | **str** | Type of deployment failure | [optional] [readonly] 
**deployment_failure_reason** | **str** | Reason for deployment failure | [optional] [readonly] 
**task_definition** | **object** | ECS task definition details | [optional] [readonly] 
**service** | **object** | ECS service details | [optional] [readonly] 
**load_balancer** | **object** | Load balancer configuration | [optional] [readonly] 
**security_group** | **object** | Security group configuration | [optional] [readonly] 
**subnet** | **object** | Subnet configuration | [optional] [readonly] 
**vpc** | **object** | VPC configuration | [optional] [readonly] 
**container_names** | **List[str]** | Container name list | [optional] [readonly] 
**volumes** | [**List[Volume]**](Volume.md) | Persistent storage volumes | [optional] [readonly] 
**cron** | [**List[Cron]**](Cron.md) | Scheduled cron jobs | [optional] [readonly] 
**alb_routing** | **object** | ALB routing configuration | [optional] [readonly] 
**created_at** | **datetime** | Creation timestamp | [optional] [readonly] 
**updated_at** | **datetime** | Last update timestamp | [optional] [readonly] 

## Example

```python
from quantcdn.models.environment_response import EnvironmentResponse

# TODO update the JSON string below
json = "{}"
# create an instance of EnvironmentResponse from a JSON string
environment_response_instance = EnvironmentResponse.from_json(json)
# print the JSON string representation of the object
print(EnvironmentResponse.to_json())

# convert the object into a dict
environment_response_dict = environment_response_instance.to_dict()
# create an instance of EnvironmentResponse from a dict
environment_response_from_dict = EnvironmentResponse.from_dict(environment_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


