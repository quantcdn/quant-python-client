# AIModelEligibility


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**model_id** | **str** |  | 
**resolved_id** | **str** |  | 
**eligible** | **bool** |  | 
**reason** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.ai_model_eligibility import AIModelEligibility

# TODO update the JSON string below
json = "{}"
# create an instance of AIModelEligibility from a JSON string
ai_model_eligibility_instance = AIModelEligibility.from_json(json)
# print the JSON string representation of the object
print(AIModelEligibility.to_json())

# convert the object into a dict
ai_model_eligibility_dict = ai_model_eligibility_instance.to_dict()
# create an instance of AIModelEligibility from a dict
ai_model_eligibility_from_dict = AIModelEligibility.from_dict(ai_model_eligibility_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


