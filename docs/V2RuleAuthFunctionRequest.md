# V2RuleAuthFunctionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**domain** | **List[str]** | Exact hostnames the rule matches, or &#39;any&#39; (the default). Wildcards such as *.example.com are not supported. | 
**name** | **str** | Rule name | [optional] 
**uuid** | **str** | Rule UUID | [optional] 
**weight** | **int** | Rule order. Must be 0 or greater; lower weights are processed first. If omitted on create, the rule is placed last. | [optional] 
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
**asn** | **str** | ASN filter type (asn_is, asn_is_not, any). A PATCH that omits it keeps the current value. Invalid values return 422. | [optional] 
**asn_is** | **List[str]** | Allowed AS numbers. Positive integers up to 4294967295, stored as strings. A PATCH replaces the list. | [optional] 
**asn_is_not** | **List[str]** | Excluded AS numbers. Positive integers up to 4294967295, stored as strings. A PATCH replaces the list. | [optional] 
**ua** | **str** | User agent filter type (ua_is, ua_is_not, any). Invalid values return 422. | [optional] 
**ua_is** | **List[str]** | User agent strings to match. Each item has at most 255 characters. A PATCH replaces the list. | [optional] 
**ua_is_not** | **List[str]** | User agent strings to exclude. Each item has at most 255 characters. A PATCH replaces the list. | [optional] 
**traffic_source** | **str** | Traffic source filter type (traffic_source_is, traffic_source_is_not, any). Invalid values return 422. | [optional] 
**traffic_source_is** | **List[str]** | Traffic sources to match. A PATCH replaces the list. | [optional] 
**traffic_source_is_not** | **List[str]** | Traffic sources to exclude. A PATCH replaces the list. | [optional] 
**cookie_name** | **str** | Write name of only_with_cookie: the rule applies only when this cookie is present. Empty string clears it. | [optional] 
**fn_uuid** | **str** | UUID of a published function of type edge_auth in this project. A create, or a change of fn_uuid, that names any other function returns 422. | 

## Example

```python
from quantcdn.models.v2_rule_auth_function_request import V2RuleAuthFunctionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleAuthFunctionRequest from a JSON string
v2_rule_auth_function_request_instance = V2RuleAuthFunctionRequest.from_json(json)
# print the JSON string representation of the object
print(V2RuleAuthFunctionRequest.to_json())

# convert the object into a dict
v2_rule_auth_function_request_dict = v2_rule_auth_function_request_instance.to_dict()
# create an instance of V2RuleAuthFunctionRequest from a dict
v2_rule_auth_function_request_from_dict = V2RuleAuthFunctionRequest.from_dict(v2_rule_auth_function_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


