# GetGovernanceConfig200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**org_id** | **str** |  | [optional] 
**ai_enabled** | **bool** |  | [optional] 
**model_policy** | **str** |  | [optional] 
**model_list** | **List[str]** |  | [optional] 
**mandatory_guardrail_preset** | **str** |  | [optional] 
**mandatory_filter_policies** | **List[str]** |  | [optional] 
**spend_limits** | [**GetGovernanceConfig200ResponseSpendLimits**](GetGovernanceConfig200ResponseSpendLimits.md) |  | [optional] 
**version** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.get_governance_config200_response import GetGovernanceConfig200Response

# TODO update the JSON string below
json = "{}"
# create an instance of GetGovernanceConfig200Response from a JSON string
get_governance_config200_response_instance = GetGovernanceConfig200Response.from_json(json)
# print the JSON string representation of the object
print(GetGovernanceConfig200Response.to_json())

# convert the object into a dict
get_governance_config200_response_dict = get_governance_config200_response_instance.to_dict()
# create an instance of GetGovernanceConfig200Response from a dict
get_governance_config200_response_from_dict = GetGovernanceConfig200Response.from_dict(get_governance_config200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


