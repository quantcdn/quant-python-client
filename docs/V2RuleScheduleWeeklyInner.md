# V2RuleScheduleWeeklyInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**days** | **List[str]** |  | 
**start** | **str** | Local time HH:MM, 00:00 to 23:59. | 
**end** | **str** | Local time HH:MM, 00:00 to 24:00. | 

## Example

```python
from quantcdn.models.v2_rule_schedule_weekly_inner import V2RuleScheduleWeeklyInner

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleScheduleWeeklyInner from a JSON string
v2_rule_schedule_weekly_inner_instance = V2RuleScheduleWeeklyInner.from_json(json)
# print the JSON string representation of the object
print(V2RuleScheduleWeeklyInner.to_json())

# convert the object into a dict
v2_rule_schedule_weekly_inner_dict = v2_rule_schedule_weekly_inner_instance.to_dict()
# create an instance of V2RuleScheduleWeeklyInner from a dict
v2_rule_schedule_weekly_inner_from_dict = V2RuleScheduleWeeklyInner.from_dict(v2_rule_schedule_weekly_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


