# DecideToolProposalRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**decision** | **str** |  | 
**reason** | **str** |  | [optional] 
**scope** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.decide_tool_proposal_request import DecideToolProposalRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DecideToolProposalRequest from a JSON string
decide_tool_proposal_request_instance = DecideToolProposalRequest.from_json(json)
# print the JSON string representation of the object
print(DecideToolProposalRequest.to_json())

# convert the object into a dict
decide_tool_proposal_request_dict = decide_tool_proposal_request_instance.to_dict()
# create an instance of DecideToolProposalRequest from a dict
decide_tool_proposal_request_from_dict = DecideToolProposalRequest.from_dict(decide_tool_proposal_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


