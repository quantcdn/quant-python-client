# V2RuleBotChallengeAction


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**robot_challenge_type** | **str** | Challenge type (invisible or checkbox) | 
**robot_challenge_verification_ttl** | **int** | Verification TTL in seconds | [optional] [default to 10800]
**robot_challenge_challenge_ttl** | **int** | Challenge TTL in seconds | [optional] [default to 30]

## Example

```python
from quantcdn.models.v2_rule_bot_challenge_action import V2RuleBotChallengeAction

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleBotChallengeAction from a JSON string
v2_rule_bot_challenge_action_instance = V2RuleBotChallengeAction.from_json(json)
# print the JSON string representation of the object
print(V2RuleBotChallengeAction.to_json())

# convert the object into a dict
v2_rule_bot_challenge_action_dict = v2_rule_bot_challenge_action_instance.to_dict()
# create an instance of V2RuleBotChallengeAction from a dict
v2_rule_bot_challenge_action_from_dict = V2RuleBotChallengeAction.from_dict(v2_rule_bot_challenge_action_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


