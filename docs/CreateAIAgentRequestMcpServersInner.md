# CreateAIAgentRequestMcpServersInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**server** | **str** | The registered server name | 
**tools** | **List[str]** | Optional. Only these tools of the server. Omit for every tool the server allows; an empty array allows none. | [optional] 

## Example

```python
from quantcdn.models.create_ai_agent_request_mcp_servers_inner import CreateAIAgentRequestMcpServersInner

# TODO update the JSON string below
json = "{}"
# create an instance of CreateAIAgentRequestMcpServersInner from a JSON string
create_ai_agent_request_mcp_servers_inner_instance = CreateAIAgentRequestMcpServersInner.from_json(json)
# print the JSON string representation of the object
print(CreateAIAgentRequestMcpServersInner.to_json())

# convert the object into a dict
create_ai_agent_request_mcp_servers_inner_dict = create_ai_agent_request_mcp_servers_inner_instance.to_dict()
# create an instance of CreateAIAgentRequestMcpServersInner from a dict
create_ai_agent_request_mcp_servers_inner_from_dict = CreateAIAgentRequestMcpServersInner.from_dict(create_ai_agent_request_mcp_servers_inner_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


