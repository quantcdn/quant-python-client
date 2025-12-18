# quantcdn.AIAgentsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**chat_with_ai_agent**](AIAgentsApi.md#chat_with_ai_agent) | **POST** /api/v3/organizations/{organisation}/ai/agents/{agentId}/chat | Chat with AI Agent
[**create_ai_agent**](AIAgentsApi.md#create_ai_agent) | **POST** /api/v3/organizations/{organisation}/ai/agents | Create AI Agent
[**delete_ai_agent**](AIAgentsApi.md#delete_ai_agent) | **DELETE** /api/v3/organizations/{organisation}/ai/agents/{agentId} | Delete Agent
[**get_ai_agent**](AIAgentsApi.md#get_ai_agent) | **GET** /api/v3/organizations/{organisation}/ai/agents/{agentId} | Get Agent Details
[**list_ai_agents**](AIAgentsApi.md#list_ai_agents) | **GET** /api/v3/organizations/{organisation}/ai/agents | List AI Agents
[**update_ai_agent**](AIAgentsApi.md#update_ai_agent) | **PUT** /api/v3/organizations/{organisation}/ai/agents/{agentId} | Update Agent


# **chat_with_ai_agent**
> ChatWithAIAgent200Response chat_with_ai_agent(organisation, agent_id, chat_with_ai_agent_request)

Chat with AI Agent

Initiates a chat session with a specific AI agent. The agent's configuration (system prompt, temperature, model, allowed tools) is automatically applied.
     *
     * **Key Features:**
     * - **Session Management**: Automatic session creation and state tracking
     * - **Multi-turn Conversations**: Full conversation history maintained server-side
     * - Agent's system prompt is prepended to conversation
     * - Only agent's allowed tools are available
     * - All tools are auto-executed (no client confirmation)
     * - Temperature and model from agent config
     *
     * **Session Support:**
     * - Omit `sessionId` to create a new session automatically
     * - Include `sessionId` to continue an existing conversation
     * - Sessions expire after 60 minutes of inactivity
     * - Use `/sessions/{sessionId}` to retrieve full conversation history

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.chat_with_ai_agent200_response import ChatWithAIAgent200Response
from quantcdn.models.chat_with_ai_agent_request import ChatWithAIAgentRequest
from quantcdn.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://dashboard.quantcdn.io
# See configuration.py for a list of all supported configuration parameters.
configuration = quantcdn.Configuration(
    host = "https://dashboard.quantcdn.io"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): BearerAuth
configuration = quantcdn.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with quantcdn.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = quantcdn.AIAgentsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    agent_id = 'agent_id_example' # str | The agent ID
    chat_with_ai_agent_request = quantcdn.ChatWithAIAgentRequest() # ChatWithAIAgentRequest | 

    try:
        # Chat with AI Agent
        api_response = api_instance.chat_with_ai_agent(organisation, agent_id, chat_with_ai_agent_request)
        print("The response of AIAgentsApi->chat_with_ai_agent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAgentsApi->chat_with_ai_agent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **agent_id** | **str**| The agent ID | 
 **chat_with_ai_agent_request** | [**ChatWithAIAgentRequest**](ChatWithAIAgentRequest.md)|  | 

### Return type

[**ChatWithAIAgent200Response**](ChatWithAIAgent200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Agent response generated successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**404** | Agent not found |  -  |
**500** | Failed to chat with agent |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_ai_agent**
> CreateAIAgent201Response create_ai_agent(organisation, create_ai_agent_request)

Create AI Agent

Creates a new AI agent with specific configuration, system prompt, and tool permissions.
     *
     * **Agent Configuration:**
     * - **System Prompt**: Instructions that guide the agent's behavior
     * - **Model**: Which foundation model to use (e.g., 'amazon.nova-pro-v1:0')
     * - **Temperature**: Creativity level (0-1)
     * - **Allowed Tools**: Which tools the agent can auto-execute
     * - **Allowed Collections**: Vector DB collections for RAG
     * - **Group**: Optional categorization (e.g., 'development', 'compliance')
     *
     * **Auto-Execution:**
     * All tools are automatically executed when an agent requests them (no client confirmation needed).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_ai_agent201_response import CreateAIAgent201Response
from quantcdn.models.create_ai_agent_request import CreateAIAgentRequest
from quantcdn.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://dashboard.quantcdn.io
# See configuration.py for a list of all supported configuration parameters.
configuration = quantcdn.Configuration(
    host = "https://dashboard.quantcdn.io"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): BearerAuth
configuration = quantcdn.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with quantcdn.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = quantcdn.AIAgentsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    create_ai_agent_request = quantcdn.CreateAIAgentRequest() # CreateAIAgentRequest | 

    try:
        # Create AI Agent
        api_response = api_instance.create_ai_agent(organisation, create_ai_agent_request)
        print("The response of AIAgentsApi->create_ai_agent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAgentsApi->create_ai_agent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **create_ai_agent_request** | [**CreateAIAgentRequest**](CreateAIAgentRequest.md)|  | 

### Return type

[**CreateAIAgent201Response**](CreateAIAgent201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Agent created successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**500** | Failed to create agent |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_ai_agent**
> DeleteAIAgent200Response delete_ai_agent(organisation, agent_id)

Delete Agent

Permanently deletes an AI agent. This action cannot be undone.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.delete_ai_agent200_response import DeleteAIAgent200Response
from quantcdn.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://dashboard.quantcdn.io
# See configuration.py for a list of all supported configuration parameters.
configuration = quantcdn.Configuration(
    host = "https://dashboard.quantcdn.io"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): BearerAuth
configuration = quantcdn.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with quantcdn.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = quantcdn.AIAgentsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    agent_id = 'agent_id_example' # str | The agent ID

    try:
        # Delete Agent
        api_response = api_instance.delete_ai_agent(organisation, agent_id)
        print("The response of AIAgentsApi->delete_ai_agent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAgentsApi->delete_ai_agent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **agent_id** | **str**| The agent ID | 

### Return type

[**DeleteAIAgent200Response**](DeleteAIAgent200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Agent deleted successfully |  -  |
**403** | Access denied |  -  |
**404** | Agent not found |  -  |
**500** | Failed to delete agent |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_ai_agent**
> GetAIAgent200Response get_ai_agent(organisation, agent_id)

Get Agent Details

Retrieves detailed configuration for a specific AI agent.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_ai_agent200_response import GetAIAgent200Response
from quantcdn.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://dashboard.quantcdn.io
# See configuration.py for a list of all supported configuration parameters.
configuration = quantcdn.Configuration(
    host = "https://dashboard.quantcdn.io"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): BearerAuth
configuration = quantcdn.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with quantcdn.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = quantcdn.AIAgentsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    agent_id = 'agent_id_example' # str | The agent ID

    try:
        # Get Agent Details
        api_response = api_instance.get_ai_agent(organisation, agent_id)
        print("The response of AIAgentsApi->get_ai_agent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAgentsApi->get_ai_agent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **agent_id** | **str**| The agent ID | 

### Return type

[**GetAIAgent200Response**](GetAIAgent200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Agent details retrieved successfully |  -  |
**403** | Access denied |  -  |
**404** | Agent not found |  -  |
**500** | Failed to retrieve agent |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_ai_agents**
> ListAIAgents200Response list_ai_agents(organisation, group=group)

List AI Agents

Lists all AI agents for an organization. Agents are pre-configured AI assistants with specific system prompts, model settings, and tool permissions.
     *
     * **Features:**
     * - Filter by group (e.g., 'development', 'compliance')
     * - Organization-scoped
     * - Returns agent configurations without execution history

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_ai_agents200_response import ListAIAgents200Response
from quantcdn.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://dashboard.quantcdn.io
# See configuration.py for a list of all supported configuration parameters.
configuration = quantcdn.Configuration(
    host = "https://dashboard.quantcdn.io"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): BearerAuth
configuration = quantcdn.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with quantcdn.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = quantcdn.AIAgentsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    group = 'group_example' # str | Optional group filter (e.g., 'development', 'compliance') (optional)

    try:
        # List AI Agents
        api_response = api_instance.list_ai_agents(organisation, group=group)
        print("The response of AIAgentsApi->list_ai_agents:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAgentsApi->list_ai_agents: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **group** | **str**| Optional group filter (e.g., &#39;development&#39;, &#39;compliance&#39;) | [optional] 

### Return type

[**ListAIAgents200Response**](ListAIAgents200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of agents retrieved successfully |  -  |
**403** | Access denied |  -  |
**500** | Failed to retrieve agents |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_ai_agent**
> UpdateAIAgent200Response update_ai_agent(organisation, agent_id, update_ai_agent_request)

Update Agent

Updates an existing AI agent configuration. All fields except agentId, organizationId, createdAt, and createdBy can be updated.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.update_ai_agent200_response import UpdateAIAgent200Response
from quantcdn.models.update_ai_agent_request import UpdateAIAgentRequest
from quantcdn.rest import ApiException
from pprint import pprint

# Defining the host is optional and defaults to https://dashboard.quantcdn.io
# See configuration.py for a list of all supported configuration parameters.
configuration = quantcdn.Configuration(
    host = "https://dashboard.quantcdn.io"
)

# The client must configure the authentication and authorization parameters
# in accordance with the API server security policy.
# Examples for each auth method are provided below, use the example that
# satisfies your auth use case.

# Configure Bearer authorization (JWT): BearerAuth
configuration = quantcdn.Configuration(
    access_token = os.environ["BEARER_TOKEN"]
)

# Enter a context with an instance of the API client
with quantcdn.ApiClient(configuration) as api_client:
    # Create an instance of the API class
    api_instance = quantcdn.AIAgentsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    agent_id = 'agent_id_example' # str | The agent ID
    update_ai_agent_request = quantcdn.UpdateAIAgentRequest() # UpdateAIAgentRequest | 

    try:
        # Update Agent
        api_response = api_instance.update_ai_agent(organisation, agent_id, update_ai_agent_request)
        print("The response of AIAgentsApi->update_ai_agent:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAgentsApi->update_ai_agent: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **agent_id** | **str**| The agent ID | 
 **update_ai_agent_request** | [**UpdateAIAgentRequest**](UpdateAIAgentRequest.md)|  | 

### Return type

[**UpdateAIAgent200Response**](UpdateAIAgent200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Agent updated successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**404** | Agent not found |  -  |
**500** | Failed to update agent |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

