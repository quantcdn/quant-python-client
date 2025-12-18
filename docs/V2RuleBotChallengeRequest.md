# V2RuleBotChallengeRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **List[str]** | Domain patterns (default: any) | 
**name** | **str** | Rule name | [optional] 
**uuid** | **str** | Rule UUID | [optional] 
**weight** | **int** | Rule weight | [optional] [default to 0]
**disabled** | **bool** | Whether rule is disabled | [optional] [default to False]
**url** | **List[str]** | URL patterns | 
**country** | **str** | Country filter type (country_is, country_is_not, any) | [optional] 
**country_is** | **List[str]** | Allowed countries | [optional] 
**country_is_not** | **List[str]** | Excluded countries | [optional] 
**method** | **str** | Method filter type (method_is, method_is_not, any) | [optional] 
**method_is** | **List[str]** | Allowed HTTP methods | [optional] 
**method_is_not** | **List[str]** | Excluded HTTP methods | [optional] 
**ip** | **str** | IP filter type (ip_is, ip_is_not, any) | [optional] 
**ip_is** | **List[str]** | Allowed IP addresses | [optional] 
**ip_is_not** | **List[str]** | Excluded IP addresses | [optional] 
**robot_challenge_type** | **str** | Challenge type (invisible or checkbox) | 
**robot_challenge_verification_ttl** | **int** | Verification TTL in seconds | [optional] [default to 10800]
**robot_challenge_challenge_ttl** | **int** | Challenge TTL in seconds | [optional] [default to 30]

## Example

```python
from quantcdn.models.v2_rule_bot_challenge_request import V2RuleBotChallengeRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleBotChallengeRequest from a JSON string
v2_rule_bot_challenge_request_instance = V2RuleBotChallengeRequest.from_json(json)
# print the JSON string representation of the object
print(V2RuleBotChallengeRequest.to_json())

# convert the object into a dict
v2_rule_bot_challenge_request_dict = v2_rule_bot_challenge_request_instance.to_dict()
# create an instance of V2RuleBotChallengeRequest from a dict
v2_rule_bot_challenge_request_from_dict = V2RuleBotChallengeRequest.from_dict(v2_rule_bot_challenge_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


