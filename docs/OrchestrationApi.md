# quantcdn.OrchestrationApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_ai_orchestration_status**](OrchestrationApi.md#get_ai_orchestration_status) | **GET** /api/v3/organizations/{organisation}/ai/tools/orchestrations/{orchestrationId} | Get Tool Orchestration Status (Async Tool Polling)


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
    api_instance = quantcdn.OrchestrationApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    orchestration_id = 'orch_abc123def456789012345678901234' # str | Orchestration identifier for aggregated async tool executions

    try:
        # Get Tool Orchestration Status (Async Tool Polling)
        api_response = api_instance.get_ai_orchestration_status(organisation, orchestration_id)
        print("The response of OrchestrationApi->get_ai_orchestration_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling OrchestrationApi->get_ai_orchestration_status: %s\n" % e)
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

