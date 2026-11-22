# V2RuleSchedule

Weekly windows and one-off ranges in local wall time for one IANA time zone. Start is inclusive, end is exclusive. A weekly window whose end is not later than its start crosses midnight. With no windows the rule always applies.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**timezone** | **str** | IANA time zone name, or UTC. Invalid values return 422. | 
**mode** | **str** | active_during: the rule applies only inside the windows. inactive_during: the rule applies only outside them. | 
**weekly** | [**List[V2RuleScheduleWeeklyInner]**](V2RuleScheduleWeeklyInner.md) | Weekly windows. Stored as an empty list when omitted. | [optional] 
**once** | [**List[V2RuleScheduleOnceInner]**](V2RuleScheduleOnceInner.md) | One-off ranges. Stored as an empty list when omitted. | [optional] 

## Example

```python
from quantcdn.models.v2_rule_schedule import V2RuleSchedule

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleSchedule from a JSON string
v2_rule_schedule_instance = V2RuleSchedule.from_json(json)
# print the JSON string representation of the object
print(V2RuleSchedule.to_json())

# convert the object into a dict
v2_rule_schedule_dict = v2_rule_schedule_instance.to_dict()
# create an instance of V2RuleSchedule from a dict
v2_rule_schedule_from_dict = V2RuleSchedule.from_dict(v2_rule_schedule_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


