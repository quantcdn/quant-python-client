# EnvironmentResponse

Environment response schema with runtime details

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**env_name** | **str** | Environment name | 
**status** | **str** | Environment status | [optional] 
**running_count** | **int** | Number of running tasks | [optional] 
**desired_count** | **int** | Desired number of tasks | [optional] 
**min_capacity** | **int** | Minimum capacity for autoscaling | [optional] 
**max_capacity** | **int** | Maximum capacity for autoscaling | [optional] 
**public_ip_address** | **str** | Public IP address for SSH access | [optional] 
**deployment_status** | **str** | Current deployment status. FAILED indicates the most recent deployment did not complete successfully. | [optional] 
**deployment_failure_type** | **str** | Type of deployment failure when deploymentStatus is FAILED (e.g., &#39;ECS_DEPLOYMENT_CIRCUIT_BREAKER&#39;, &#39;IMAGE_PULL_ERROR&#39;) | [optional] 
**deployment_failure_reason** | **str** | Human-readable explanation of why the deployment failed. Contains details such as wrong image architecture, missing image, or container startup errors. | [optional] 
**task_definition** | **object** | ECS task definition details | [optional] 
**service** | **object** | ECS service details | [optional] 
**load_balancer** | **object** | Load balancer configuration | [optional] 
**security_group** | **object** | Security group configuration | [optional] 
**subnet** | **object** | Subnet configuration | [optional] 
**vpc** | **object** | VPC configuration | [optional] 
**containers** | **List[object]** | Container configurations | [optional] 
**volumes** | [**List[Volume]**](Volume.md) | Persistent storage volumes | [optional] 
**cron** | [**List[Cron]**](Cron.md) | Scheduled cron jobs | [optional] 
**alb_routing** | **object** | ALB routing configuration | [optional] 
**created_at** | **datetime** | Creation timestamp | [optional] 
**updated_at** | **datetime** | Last update timestamp | [optional] 

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


