# CreateSlackInteractionRequestActionsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **str** |  | 
**label** | **str** |  | 
**style** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.create_slack_interaction_request_actions_inner import CreateSlackInteractionRequestActionsInner

# TODO update the JSON string below
json = "{}"
# create an instance of CreateSlackInteractionRequestActionsInner from a JSON string
create_slack_interaction_request_actions_inner_instance = CreateSlackInteractionRequestActionsInner.from_json(json)
# print the JSON string representation of the object
print(CreateSlackInteractionRequestActionsInner.to_json())

# convert the object into a dict
create_slack_interaction_request_actions_inner_dict = create_slack_interaction_request_actions_inner_instance.to_dict()
# create an instance of CreateSlackInteractionRequestActionsInner from a dict
create_slack_interaction_request_actions_inner_from_dict = CreateSlackInteractionRequestActionsInner.from_dict(create_slack_interaction_request_actions_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


