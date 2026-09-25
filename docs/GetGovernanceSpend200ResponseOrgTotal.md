# GetGovernanceSpend200ResponseOrgTotal


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**spend_cents** | **int** | Total org spend in US cents | [optional] 
**request_count** | **int** |  | [optional] 

## Example

```python
from quantcdn.models.get_governance_spend200_response_org_total import GetGovernanceSpend200ResponseOrgTotal

# TODO update the JSON string below
json = "{}"
# create an instance of GetGovernanceSpend200ResponseOrgTotal from a JSON string
get_governance_spend200_response_org_total_instance = GetGovernanceSpend200ResponseOrgTotal.from_json(json)
# print the JSON string representation of the object
print(GetGovernanceSpend200ResponseOrgTotal.to_json())

# convert the object into a dict
get_governance_spend200_response_org_total_dict = get_governance_spend200_response_org_total_instance.to_dict()
# create an instance of GetGovernanceSpend200ResponseOrgTotal from a dict
get_governance_spend200_response_org_total_from_dict = GetGovernanceSpend200ResponseOrgTotal.from_dict(get_governance_spend200_response_org_total_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


