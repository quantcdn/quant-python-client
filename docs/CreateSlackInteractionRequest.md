# CreateSlackInteractionRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**channel** | **str** |  | 
**thread_ts** | **str** |  | [optional] 
**text** | **str** |  | 
**actions** | [**List[CreateSlackInteractionRequestActionsInner]**](CreateSlackInteractionRequestActionsInner.md) |  | 
**response_mode** | **str** |  | [optional] 
**expires_in_seconds** | **int** |  | [optional] [default to 3600]
**allowed_users** | **List[str]** |  | [optional] 
**metadata** | **object** | Opaque caller data, at most 4096 bytes of canonical JSON | [optional] 

## Example

```python
from quantcdn.models.create_slack_interaction_request import CreateSlackInteractionRequest

# TODO update the JSON string below
json = "{}"
# create an instance of CreateSlackInteractionRequest from a JSON string
create_slack_interaction_request_instance = CreateSlackInteractionRequest.from_json(json)
# print the JSON string representation of the object
print(CreateSlackInteractionRequest.to_json())

# convert the object into a dict
create_slack_interaction_request_dict = create_slack_interaction_request_instance.to_dict()
# create an instance of CreateSlackInteractionRequest from a dict
create_slack_interaction_request_from_dict = CreateSlackInteractionRequest.from_dict(create_slack_interaction_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


