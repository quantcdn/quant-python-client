# AIAutoModeEligibility


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**orchestrator** | [**AIModelEligibility**](AIModelEligibility.md) |  | 
**roles** | [**AIAutoModeEligibilityRoles**](AIAutoModeEligibilityRoles.md) |  | 
**usable** | **bool** |  | 

## Example

```python
from quantcdn.models.ai_auto_mode_eligibility import AIAutoModeEligibility

# TODO update the JSON string below
json = "{}"
# create an instance of AIAutoModeEligibility from a JSON string
ai_auto_mode_eligibility_instance = AIAutoModeEligibility.from_json(json)
# print the JSON string representation of the object
print(AIAutoModeEligibility.to_json())

# convert the object into a dict
ai_auto_mode_eligibility_dict = ai_auto_mode_eligibility_instance.to_dict()
# create an instance of AIAutoModeEligibility from a dict
ai_auto_mode_eligibility_from_dict = AIAutoModeEligibility.from_dict(ai_auto_mode_eligibility_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


