# CreateFilterPolicyRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **str** |  | 
**description** | **str** |  | [optional] 
**enabled** | **bool** |  | [optional] 
**rules** | [**List[CreateFilterPolicyRequestRulesInner]**](CreateFilterPolicyRequestRulesInner.md) |  | 

## Example

```python
from quantcdn.models.create_filter_policy_request import CreateFilterPolicyRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateFilterPolicyRequest from a JSON string
create_filter_policy_request_instance = CreateFilterPolicyRequest.from_json(json)
# print the JSON string representation of the object
print(CreateFilterPolicyRequest.to_json())

# convert the object into a dict
create_filter_policy_request_dict = create_filter_policy_request_instance.to_dict()
# create an instance of CreateFilterPolicyRequest from a dict
create_filter_policy_request_from_dict = CreateFilterPolicyRequest.from_dict(create_filter_policy_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


