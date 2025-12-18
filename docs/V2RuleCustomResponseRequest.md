# V2RuleCustomResponseRequest


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
**custom_response_body** | **str** | Custom response body content | 
**custom_response_status_code** | **int** | HTTP status code for custom response | [optional] [default to 200]
**status_code** | **int** | Legacy field for status code (deprecated) | [optional] 
**body** | **str** | Legacy field for response body (deprecated) | [optional] 

## Example

```python
from quantcdn.models.v2_rule_custom_response_request import V2RuleCustomResponseRequest

# TODO update the JSON string below
json = "{}"
# create an instance of V2RuleCustomResponseRequest from a JSON string
v2_rule_custom_response_request_instance = V2RuleCustomResponseRequest.from_json(json)
# print the JSON string representation of the object
print(V2RuleCustomResponseRequest.to_json())

# convert the object into a dict
v2_rule_custom_response_request_dict = v2_rule_custom_response_request_instance.to_dict()
# create an instance of V2RuleCustomResponseRequest from a dict
v2_rule_custom_response_request_from_dict = V2RuleCustomResponseRequest.from_dict(v2_rule_custom_response_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


