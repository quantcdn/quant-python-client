# quantcdn.AIToolApprovalApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**decide_tool_proposal**](AIToolApprovalApi.md#decide_tool_proposal) | **POST** /api/v3/organizations/{organisation}/ai/tool-proposals/{proposalId}/decision | Decide a tool approval proposal
[**get_tool_proposal**](AIToolApprovalApi.md#get_tool_proposal) | **GET** /api/v3/organizations/{organisation}/ai/tool-proposals/{proposalId} | Get a tool approval proposal


# **decide_tool_proposal**
> decide_tool_proposal(organisation, proposal_id, decide_tool_proposal_request, x_quant_approval_nonce=x_quant_approval_nonce)

Decide a tool approval proposal

Approves or rejects a tool approval proposal. QuantGov AI-governance organisations only; any other organisation gets 404. Only the QuantCode PKCE token with the `ai:approve` scope may call this. Any other token gets 403 with `This token cannot decide tool approvals.` The upstream status and body are returned unchanged.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.decide_tool_proposal_request import DecideToolProposalRequest
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
    api_instance = quantcdn.AIToolApprovalApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    proposal_id = 'proposal_id_example' # str | The proposal ID
    decide_tool_proposal_request = quantcdn.DecideToolProposalRequest() # DecideToolProposalRequest | 
    x_quant_approval_nonce = 'x_quant_approval_nonce_example' # str | One-time approval nonce from the approval prompt. It is forwarded to the platform and never logged. (optional)

    try:
        # Decide a tool approval proposal
        api_instance.decide_tool_proposal(organisation, proposal_id, decide_tool_proposal_request, x_quant_approval_nonce=x_quant_approval_nonce)
    except Exception as e:
        print("Exception when calling AIToolApprovalApi->decide_tool_proposal: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **proposal_id** | **str**| The proposal ID | 
 **decide_tool_proposal_request** | [**DecideToolProposalRequest**](DecideToolProposalRequest.md)|  | 
 **x_quant_approval_nonce** | **str**| One-time approval nonce from the approval prompt. It is forwarded to the platform and never logged. | [optional] 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The decision result |  -  |
**403** | This token cannot decide tool approvals. |  -  |
**404** | Proposal not found, or the organisation is not a QuantGov AI-governance organisation |  -  |
**409** | The proposal is no longer pending |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_tool_proposal**
> get_tool_proposal(organisation, proposal_id)

Get a tool approval proposal

Returns one of the caller's own tool approval proposals. QuantGov AI-governance organisations only; any other organisation gets 404. Only the QuantCode PKCE token with the `ai:approve` scope may call this. Any other token gets 403 with `This token cannot decide tool approvals.` A proposal that belongs to another user is answered as 404.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
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
    api_instance = quantcdn.AIToolApprovalApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    proposal_id = 'proposal_id_example' # str | The proposal ID

    try:
        # Get a tool approval proposal
        api_instance.get_tool_proposal(organisation, proposal_id)
    except Exception as e:
        print("Exception when calling AIToolApprovalApi->get_tool_proposal: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **proposal_id** | **str**| The proposal ID | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The proposal |  -  |
**403** | This token cannot decide tool approvals. |  -  |
**404** | Proposal not found, or the organisation is not a QuantGov AI-governance organisation |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

