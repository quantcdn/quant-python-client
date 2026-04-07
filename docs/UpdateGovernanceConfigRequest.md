# UpdateGovernanceConfigRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**ai_enabled** | **bool** |  | 
**model_policy** | **str** |  | 
**model_list** | **List[str]** |  | [optional] 
**mandatory_guardrail_preset** | **str** |  | [optional] 
**mandatory_filter_policies** | **List[str]** |  | [optional] 
**spend_limits** | [**GetGovernanceConfig200ResponseSpendLimits**](GetGovernanceConfig200ResponseSpendLimits.md) |  | [optional] 
**version** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.update_governance_config_request import UpdateGovernanceConfigRequest

# TODO update the JSON string below
json = "{}"
# create an instance of UpdateGovernanceConfigRequest from a JSON string
update_governance_config_request_instance = UpdateGovernanceConfigRequest.from_json(json)
# print the JSON string representation of the object
print(UpdateGovernanceConfigRequest.to_json())

# convert the object into a dict
update_governance_config_request_dict = update_governance_config_request_instance.to_dict()
# create an instance of UpdateGovernanceConfigRequest from a dict
update_governance_config_request_from_dict = UpdateGovernanceConfigRequest.from_dict(update_governance_config_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


