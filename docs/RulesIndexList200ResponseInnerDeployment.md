# RulesIndexList200ResponseInnerDeployment

Present only on a rule that a deploy of `quant/edge-rules.json` wrote, or a copy of one. `namespace` is the file's top-level namespace and `id` is the rule's id in that file; a later deploy matches its rules to stored rules by this pair. A copy in another project (an environment or a clone) can keep the marker but has `managed` false.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**namespace** | **str** | The &#x60;namespace&#x60; of the edge-rules file that wrote the rule. | 
**id** | **str** | The &#x60;id&#x60; of the rule in that file. | 
**hash** | **str** | Hash of the rule as the deploy last wrote it, used to detect changes by other paths. | [optional] 

## Example

```python
from quantcdn.models.rules_index_list200_response_inner_deployment import RulesIndexList200ResponseInnerDeployment

# TODO update the JSON string below
json = "{}"
# create an instance of RulesIndexList200ResponseInnerDeployment from a JSON string
rules_index_list200_response_inner_deployment_instance = RulesIndexList200ResponseInnerDeployment.from_json(json)
# print the JSON string representation of the object
print(RulesIndexList200ResponseInnerDeployment.to_json())

# convert the object into a dict
rules_index_list200_response_inner_deployment_dict = rules_index_list200_response_inner_deployment_instance.to_dict()
# create an instance of RulesIndexList200ResponseInnerDeployment from a dict
rules_index_list200_response_inner_deployment_from_dict = RulesIndexList200ResponseInnerDeployment.from_dict(rules_index_list200_response_inner_deployment_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


