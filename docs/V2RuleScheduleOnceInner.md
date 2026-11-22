# V2RuleScheduleOnceInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**start** | **str** | Local date and time, YYYY-MM-DDTHH:MM, no offset. | 
**end** | **str** | Local date and time after start, YYYY-MM-DDTHH:MM, no offset. | 

## Example

```python
from quantcdn.models.v2_rule_schedule_once_inner import V2RuleScheduleOnceInner

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleScheduleOnceInner from a JSON string
v2_rule_schedule_once_inner_instance = V2RuleScheduleOnceInner.from_json(json)
# print the JSON string representation of the object
print(V2RuleScheduleOnceInner.to_json())

# convert the object into a dict
v2_rule_schedule_once_inner_dict = v2_rule_schedule_once_inner_instance.to_dict()
# create an instance of V2RuleScheduleOnceInner from a dict
v2_rule_schedule_once_inner_from_dict = V2RuleScheduleOnceInner.from_dict(v2_rule_schedule_once_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


