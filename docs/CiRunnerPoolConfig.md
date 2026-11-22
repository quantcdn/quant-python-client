# CiRunnerPoolConfig

The config of a ci-runner-pool resource. connection and alerts are set by Quant: they are ignored on input and kept on update.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**tier** | **str** | Hard cap on concurrent jobs: small 2, medium 4, large 8. When the pool is full, jobs wait. | 
**architectures** | **List[str]** |  | [optional] [default to ["x64"]]
**network_mode** | **str** |  | [optional] [default to 'public']
**egress_allowlist** | **List[str]** | Domains allowed when networkMode is restricted. Wildcard only as a leading *. label. | [optional] 
**idle_timeout_minutes** | **int** |  | [optional] [default to 15]
**business_hours_warm** | [**CiRunnerPoolConfigBusinessHoursWarm**](CiRunnerPoolConfigBusinessHoursWarm.md) |  | [optional] 
**connection** | [**CiRunnerPoolConfigConnection**](CiRunnerPoolConfigConnection.md) |  | [optional] 
**cache_residency** | **str** | Where the pool&#39;s GitHub Actions build cache may live. au-only keeps cache data in Australia; if the pool&#39;s cache is unavailable, jobs run without a cache. allow-github lets jobs use GitHub&#39;s cache when the pool&#39;s cache is unavailable. When not set, a pool that accepts public repositories uses allow-github and every other pool uses au-only. A change applies to the next job each runner machine starts. | [optional] 
**alerts** | [**List[CiRunnerPoolConfigAlertsInner]**](CiRunnerPoolConfigAlertsInner.md) |  | [optional] [readonly] 

## Example

```python
from quantcdn.models.ci_runner_pool_config import CiRunnerPoolConfig

# TODO update the JSON string below
json = "{}"
# create an instance of CiRunnerPoolConfig from a JSON string
ci_runner_pool_config_instance = CiRunnerPoolConfig.from_json(json)
# print the JSON string representation of the object
print(CiRunnerPoolConfig.to_json())

# convert the object into a dict
ci_runner_pool_config_dict = ci_runner_pool_config_instance.to_dict()
# create an instance of CiRunnerPoolConfig from a dict
ci_runner_pool_config_from_dict = CiRunnerPoolConfig.from_dict(ci_runner_pool_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


