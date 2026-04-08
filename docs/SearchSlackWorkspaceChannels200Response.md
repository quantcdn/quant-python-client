# SearchSlackWorkspaceChannels200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**results** | [**List[SearchSlackWorkspaceChannels200ResponseResultsInner]**](SearchSlackWorkspaceChannels200ResponseResultsInner.md) |  | [optional] 

## Example

```python
from quantcdn.models.search_slack_workspace_channels200_response import SearchSlackWorkspaceChannels200Response

# TODO update the JSON string below
json = "{}"
# create an instance of SearchSlackWorkspaceChannels200Response from a JSON string
search_slack_workspace_channels200_response_instance = SearchSlackWorkspaceChannels200Response.from_json(json)
# print the JSON string representation of the object
print(SearchSlackWorkspaceChannels200Response.to_json())

# convert the object into a dict
search_slack_workspace_channels200_response_dict = search_slack_workspace_channels200_response_instance.to_dict()
# create an instance of SearchSlackWorkspaceChannels200Response from a dict
search_slack_workspace_channels200_response_from_dict = SearchSlackWorkspaceChannels200Response.from_dict(search_slack_workspace_channels200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


