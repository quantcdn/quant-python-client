# SearchSlackWorkspaceUsers200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**results** | [**List[SearchSlackWorkspaceUsers200ResponseResultsInner]**](SearchSlackWorkspaceUsers200ResponseResultsInner.md) |  | [optional] 

## Example

```python
from quantcdn.models.search_slack_workspace_users200_response import SearchSlackWorkspaceUsers200Response

# TODO update the JSON string below
json = "{}"
# create an instance of SearchSlackWorkspaceUsers200Response from a JSON string
search_slack_workspace_users200_response_instance = SearchSlackWorkspaceUsers200Response.from_json(json)
# print the JSON string representation of the object
print(SearchSlackWorkspaceUsers200Response.to_json())

# convert the object into a dict
search_slack_workspace_users200_response_dict = search_slack_workspace_users200_response_instance.to_dict()
# create an instance of SearchSlackWorkspaceUsers200Response from a dict
search_slack_workspace_users200_response_from_dict = SearchSlackWorkspaceUsers200Response.from_dict(search_slack_workspace_users200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


