# quantcdn.AIToolsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_ai_orchestration_status**](AIToolsApi.md#get_ai_orchestration_status) | **GET** /api/v3/organizations/{organisation}/ai/tools/orchestrations/{orchestrationId} | Get Tool Orchestration Status (Async Tool Polling)
[**get_ai_tool_execution_status**](AIToolsApi.md#get_ai_tool_execution_status) | **GET** /api/v3/organizations/{organisation}/ai/tools/executions/{executionId} | Get async tool execution status and result
[**list_ai_tool_executions**](AIToolsApi.md#list_ai_tool_executions) | **GET** /api/v3/organizations/{organisation}/ai/tools/executions | List tool executions for monitoring and debugging
[**list_ai_tool_names**](AIToolsApi.md#list_ai_tool_names) | **GET** /api/v3/organizations/{organisation}/ai/tools/names | List tool names only (lightweight response)
[**list_ai_tools**](AIToolsApi.md#list_ai_tools) | **GET** /api/v3/organizations/{organisation}/ai/tools | List available built-in tools for function calling
[**list_mcp_servers**](AIToolsApi.md#list_mcp_servers) | **GET** /api/v3/organizations/{organisation}/ai/mcp-servers | List MCP servers with gateway URLs


# **get_ai_orchestration_status**
> GetAIOrchestrationStatus200Response get_ai_orchestration_status(organisation, orchestration_id)

Get Tool Orchestration Status (Async Tool Polling)

Retrieves the status and synthesized result of a multi-tool async execution orchestration.
     *
     * **Note:** This endpoint is for async tool execution polling (`/tools/orchestrations`).
     * For durable batch processing orchestrations, see `GET /orchestrations` endpoints.
     *
     * **Orchestration Pattern:**
     * When the AI requests multiple async tools simultaneously, an orchestration is created
     * to track all tool executions and synthesize their results into a single coherent response.
     *
     * **Flow:**
     * 1. AI requests multiple async tools (e.g., image generation + web search)
     * 2. Chat API creates orchestration and returns orchestrationId
     * 3. Tool Orchestrator Lambda polls all async tools
     * 4. When all tools complete, Orchestrator synthesizes results using AI
     * 5. Client polls this endpoint and receives final synthesized response
     *
     * **Status Values:**
     * - pending: Orchestration created, tools not yet started
     * - polling: Orchestrator is actively polling async tools
     * - synthesizing: All tools complete, AI is synthesizing response
     * - complete: Orchestration finished, synthesizedResponse available
     * - failed: Orchestration failed, error available
     *
     * **Polling Recommendations:**
     * - Poll every 2 seconds
     * - Maximum poll time: 10 minutes
     * - Orchestrator handles tool polling internally
     *
     * **Benefits over individual polling:**
     * - Single poll endpoint for multiple async tools
     * - AI synthesizes all results into coherent response
     * - Answers the original user question, not just tool summaries

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_ai_orchestration_status200_response import GetAIOrchestrationStatus200Response
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
    api_instance = quantcdn.AIToolsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    orchestration_id = 'orch_abc123def456789012345678901234' # str | Orchestration identifier for aggregated async tool executions

    try:
        # Get Tool Orchestration Status (Async Tool Polling)
        api_response = api_instance.get_ai_orchestration_status(organisation, orchestration_id)
        print("The response of AIToolsApi->get_ai_orchestration_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIToolsApi->get_ai_orchestration_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **orchestration_id** | **str**| Orchestration identifier for aggregated async tool executions | 

### Return type

[**GetAIOrchestrationStatus200Response**](GetAIOrchestrationStatus200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Orchestration status retrieved successfully |  -  |
**404** | Orchestration not found (may have expired after 24h) |  -  |
**403** | Access denied |  -  |
**500** | Failed to retrieve orchestration status |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_ai_tool_execution_status**
> GetAIToolExecutionStatus200Response get_ai_tool_execution_status(organisation, execution_id)

Get async tool execution status and result

Retrieves the status and result of an async tool execution. Used for polling long-running tools like image generation.
     *
     * **Async Tool Execution Pattern:**
     * This endpoint enables a polling pattern for long-running tools that would otherwise hit API Gateway's 30-second timeout.
     *
     * **Flow:**
     * 1. AI requests tool use (e.g., `generate_image`)
     * 2. Chat API returns `toolUse` with execution tracking info
     * 3. Client starts polling this endpoint with the `executionId`
     * 4. When `status === 'complete'`, retrieve `result` and send back to AI
     * 5. AI incorporates result into final response
     *
     * **Status Values:**
     * - `pending`: Tool execution queued, not yet started
     * - `running`: Tool is currently executing
     * - `complete`: Tool execution finished successfully, `result` available
     * - `failed`: Tool execution failed, `error` available
     *
     * **Polling Recommendations:**
     * - Poll every 2-3 seconds for image generation
     * - Exponential backoff for other tools (start 1s, max 5s)
     * - Stop polling after 5 minutes (consider failed)
     * - Auto-cleanup after 24 hours (TTL)
     *
     * **Use Cases:**
     * - Image generation (10-15s typical runtime)
     * - Video processing
     * - Large file uploads/downloads
     * - Complex database queries
     * - External API calls with high latency

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_ai_tool_execution_status200_response import GetAIToolExecutionStatus200Response
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
    api_instance = quantcdn.AIToolsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    execution_id = 'exec_0123456789abcdef0123456789abcdef' # str | Tool execution identifier

    try:
        # Get async tool execution status and result
        api_response = api_instance.get_ai_tool_execution_status(organisation, execution_id)
        print("The response of AIToolsApi->get_ai_tool_execution_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIToolsApi->get_ai_tool_execution_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **execution_id** | **str**| Tool execution identifier | 

### Return type

[**GetAIToolExecutionStatus200Response**](GetAIToolExecutionStatus200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Tool execution status retrieved successfully |  -  |
**404** | Execution not found (may have expired after 24h) |  -  |
**403** | Access denied |  -  |
**500** | Failed to retrieve execution status |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_ai_tool_executions**
> ListAIToolExecutions200Response list_ai_tool_executions(organisation, status=status, limit=limit)

List tool executions for monitoring and debugging

Lists recent async tool executions for an organization. Useful for debugging, monitoring, and building admin UIs.
     *
     * **Query Patterns:**
     * - All recent executions: `GET /ai/tools/executions`
     * - Filter by status: `GET /ai/tools/executions?status=running`
     * - Limit results: `GET /ai/tools/executions?limit=20`
     *
     * **Results:**
     * - Ordered by creation time (newest first)
     * - Limited to 50 by default (configurable via `limit` parameter)
     * - Only shows executions not yet expired (24h TTL)
     *
     * **Use Cases:**
     * - Monitor all active tool executions
     * - Debug failed executions
     * - Build admin dashboards
     * - Track tool usage patterns
     * - Audit async operations

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_ai_tool_executions200_response import ListAIToolExecutions200Response
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
    api_instance = quantcdn.AIToolsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    status = 'status_example' # str | Filter by execution status (optional)
    limit = 50 # int | Maximum number of executions to return (optional) (default to 50)

    try:
        # List tool executions for monitoring and debugging
        api_response = api_instance.list_ai_tool_executions(organisation, status=status, limit=limit)
        print("The response of AIToolsApi->list_ai_tool_executions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIToolsApi->list_ai_tool_executions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **status** | **str**| Filter by execution status | [optional] 
 **limit** | **int**| Maximum number of executions to return | [optional] [default to 50]

### Return type

[**ListAIToolExecutions200Response**](ListAIToolExecutions200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Tool executions retrieved successfully |  -  |
**400** | Invalid parameters |  -  |
**403** | Access denied |  -  |
**500** | Failed to retrieve executions |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_ai_tool_names**
> ListAIToolNames200Response list_ai_tool_names(organisation)

List tool names only (lightweight response)

Retrieves just the names of available built-in tools. Useful for quick validation or UI dropdown population without the full tool specifications.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_ai_tool_names200_response import ListAIToolNames200Response
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
    api_instance = quantcdn.AIToolsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # List tool names only (lightweight response)
        api_response = api_instance.list_ai_tool_names(organisation)
        print("The response of AIToolsApi->list_ai_tool_names:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIToolsApi->list_ai_tool_names: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**ListAIToolNames200Response**](ListAIToolNames200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Tool names retrieved successfully |  -  |
**403** | Access denied |  -  |
**500** | Failed to fetch tool names |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_ai_tools**
> ListAITools200Response list_ai_tools(organisation)

List available built-in tools for function calling

Retrieves all available built-in tools that can be used with function calling. These tools can be included in `toolConfig` when making AI inference requests.
     *
     * **Available Built-in Tools:**
     * - `get_weather`: Get current weather for a location using Open-Meteo API
     * - `calculate`: Perform basic mathematical calculations (add, subtract, multiply, divide)
     * - `search_web`: Search the web for information (mock implementation)
     * - `generate_image`: Generate images with Amazon Nova Canvas (async execution, 10-15s typical runtime)
     *
     * **Use Cases:**
     * - Discover available tools dynamically without hardcoding
     * - Get complete tool specifications including input schemas
     * - Build UI for tool selection
     * - Validate tool names before sending requests
     *
     * **Dynamic Tool Discovery:**
     * This endpoint enables clients to:
     * 1. Fetch all available tools on page load
     * 2. Display tool capabilities to users
     * 3. Filter tools based on user permissions
     * 4. Use `allowedTools` whitelist for security
     *
     * **Alternative Endpoint:**
     * - `GET /ai/tools/names` - Returns only tool names (faster, lighter response)

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_ai_tools200_response import ListAITools200Response
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
    api_instance = quantcdn.AIToolsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # List available built-in tools for function calling
        api_response = api_instance.list_ai_tools(organisation)
        print("The response of AIToolsApi->list_ai_tools:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIToolsApi->list_ai_tools: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**ListAITools200Response**](ListAITools200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Available tools retrieved successfully |  -  |
**403** | Access denied |  -  |
**500** | Failed to fetch tools |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_mcp_servers**
> ListMcpServers200Response list_mcp_servers(organisation)

List MCP servers with gateway URLs

Lists the organization's registered MCP servers for CLI sync (QuantCode). Each server's `url` is the FULL MCP gateway URL on the AI API host — clients connect there, never to the origin server. Credentials are never exposed.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_mcp_servers200_response import ListMcpServers200Response
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
    api_instance = quantcdn.AIToolsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # List MCP servers with gateway URLs
        api_response = api_instance.list_mcp_servers(organisation)
        print("The response of AIToolsApi->list_mcp_servers:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIToolsApi->list_mcp_servers: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**ListMcpServers200Response**](ListMcpServers200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of MCP servers retrieved successfully |  -  |
**403** | Access denied |  -  |
**500** | Failed to fetch MCP servers |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

