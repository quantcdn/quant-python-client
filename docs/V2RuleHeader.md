# V2RuleHeader


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** | Rule name | [optional] 
**uuid** | **str** | Rule UUID | 
**rule_id** | **str** | Rule ID | [optional] 
**weight** | **int** | Rule weight | [optional] [default to 0]
**url** | **List[str]** | URL patterns | [optional] 
**domain** | **List[str]** | Domain patterns | [optional] 
**disabled** | **bool** | Whether rule is disabled | [default to False]
**only_with_cookie** | **str** | Only apply with cookie | [optional] 
**method** | **str** | HTTP method | [optional] 
**method_is** | **List[str]** | Allowed HTTP methods | [optional] 
**method_is_not** | **List[str]** | Excluded HTTP methods | [optional] 
**ip** | **str** | IP address | [optional] 
**ip_is** | **List[str]** | Allowed IP addresses | [optional] 
**ip_is_not** | **List[str]** | Excluded IP addresses | [optional] 
**country** | **str** | Country code | [optional] 
**country_is** | **List[str]** | Allowed countries | [optional] 
**country_is_not** | **List[str]** | Excluded countries | [optional] 
**action** | **str** | Rule action | 
**action_config** | [**V2RuleHeaderAction**](V2RuleHeaderAction.md) |  | 

## Example

```python
from quantcdn.models.v2_rule_header import V2RuleHeader

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleHeader from a JSON string
v2_rule_header_instance = V2RuleHeader.from_json(json)
# print the JSON string representation of the object
print(V2RuleHeader.to_json())

# convert the object into a dict
v2_rule_header_dict = v2_rule_header_instance.to_dict()
# create an instance of V2RuleHeader from a dict
v2_rule_header_from_dict = V2RuleHeader.from_dict(v2_rule_header_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


