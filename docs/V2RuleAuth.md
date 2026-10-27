# V2RuleAuth


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Rule name | [optional] 
**uuid** | **str** | Rule UUID | 
**rule_id** | **str** | Rule ID | [optional] 
**weight** | **int** | Rule order. Must be 0 or greater; lower weights are processed first. If omitted on create, the rule is placed last. | [optional] 
**url** | **List[str]** | URL patterns | [optional] 
**domain** | **List[str]** | Exact hostnames the rule matches, or &#39;any&#39;. Wildcards are not supported. | [optional] 
**disabled** | **bool** | Whether rule is disabled | [default to False]
**only_with_cookie** | **str** | Only apply with cookie | [optional] 
**method** | **str** | HTTP method | [optional] 
**method_is** | **List[str]** | Allowed HTTP methods | [optional] 
**method_is_not** | **List[str]** | Excluded HTTP methods | [optional] 
**ip** | **str** | IP address | [optional] 
**ip_is** | **List[str]** | Allowed IP addresses | [optional] 
**ip_is_not** | **List[str]** | Excluded IP addresses | [optional] 
**asn** | **str** | ASN condition type (asn_is, asn_is_not, any) | [optional] 
**asn_is** | **List[str]** | Allowed AS numbers | [optional] 
**asn_is_not** | **List[str]** | Excluded AS numbers | [optional] 
**ua** | **str** | User agent condition type (ua_is, ua_is_not, any) | [optional] 
**ua_is** | **List[str]** | User agent strings to match | [optional] 
**ua_is_not** | **List[str]** | User agent strings to exclude | [optional] 
**traffic_source** | **str** | Traffic source condition type (traffic_source_is, traffic_source_is_not, any) | [optional] 
**traffic_source_is** | **List[str]** | Traffic sources to match (cloud, vpn, tor-exit, abuser, crawler) | [optional] 
**traffic_source_is_not** | **List[str]** | Traffic sources to exclude (cloud, vpn, tor-exit, abuser, crawler) | [optional] 
**country** | **str** | Country code | [optional] 
**country_is** | **List[str]** | Allowed countries | [optional] 
**country_is_not** | **List[str]** | Excluded countries | [optional] 
**action** | **str** | Rule action | 
**action_config** | [**V2RuleAuthAction**](V2RuleAuthAction.md) |  | 

## Example

```python
from quantcdn.models.v2_rule_auth import V2RuleAuth

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleAuth from a JSON string
v2_rule_auth_instance = V2RuleAuth.from_json(json)
# print the JSON string representation of the object
print(V2RuleAuth.to_json())

# convert the object into a dict
v2_rule_auth_dict = v2_rule_auth_instance.to_dict()
# create an instance of V2RuleAuth from a dict
v2_rule_auth_from_dict = V2RuleAuth.from_dict(v2_rule_auth_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


