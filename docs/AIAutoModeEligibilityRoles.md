# AIAutoModeEligibilityRoles


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**fast** | [**List[AIModelEligibility]**](AIModelEligibility.md) |  | 
**standard** | [**List[AIModelEligibility]**](AIModelEligibility.md) |  | 
**deep** | [**List[AIModelEligibility]**](AIModelEligibility.md) |  | 

## Example

```python
from quantcdn.models.ai_auto_mode_eligibility_roles import AIAutoModeEligibilityRoles

# TODO update the JSON string below
json = "{}"
# create an instance of AIAutoModeEligibilityRoles from a JSON string
ai_auto_mode_eligibility_roles_instance = AIAutoModeEligibilityRoles.from_json(json)
# print the JSON string representation of the object
print(AIAutoModeEligibilityRoles.to_json())

# convert the object into a dict
ai_auto_mode_eligibility_roles_dict = ai_auto_mode_eligibility_roles_instance.to_dict()
# create an instance of AIAutoModeEligibilityRoles from a dict
ai_auto_mode_eligibility_roles_from_dict = AIAutoModeEligibilityRoles.from_dict(ai_auto_mode_eligibility_roles_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


