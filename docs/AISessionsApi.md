# quantcdn.AISessionsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_ai_session**](AISessionsApi.md#create_ai_session) | **POST** /api/v3/organizations/{organisation}/ai/sessions | Create a new chat session with multi-tenant isolation
[**delete_ai_session**](AISessionsApi.md#delete_ai_session) | **DELETE** /api/v3/organizations/{organisation}/ai/sessions/{sessionId} | Delete a chat session
[**extend_ai_session**](AISessionsApi.md#extend_ai_session) | **PUT** /api/v3/organizations/{organisation}/ai/sessions/{sessionId}/extend | Extend Session Expiration
[**get_ai_session**](AISessionsApi.md#get_ai_session) | **GET** /api/v3/organizations/{organisation}/ai/sessions/{sessionId} | Get a specific chat session
[**list_ai_sessions**](AISessionsApi.md#list_ai_sessions) | **GET** /api/v3/organizations/{organisation}/ai/sessions | List chat sessions with multi-tenant filtering
[**update_ai_session**](AISessionsApi.md#update_ai_session) | **PUT** /api/v3/organizations/{organisation}/ai/sessions/{sessionId} | Update Session


# **create_ai_session**
> CreateAISession201Response create_ai_session(organisation, create_ai_session_request)

Create a new chat session with multi-tenant isolation

Creates an AI session with automatic expiration (60 min default, 24h max). Sessions are isolated by organization. Use userId to identify the user creating the session. Use sessionGroup for logical grouping. Use metadata for additional custom data. Filter sessions by userId or sessionGroup when listing.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_ai_session201_response import CreateAISession201Response
from quantcdn.models.create_ai_session_request import CreateAISessionRequest
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
    api_instance = quantcdn.AISessionsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    create_ai_session_request = quantcdn.CreateAISessionRequest() # CreateAISessionRequest | 

    try:
        # Create a new chat session with multi-tenant isolation
        api_response = api_instance.create_ai_session(organisation, create_ai_session_request)
        print("The response of AISessionsApi->create_ai_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISessionsApi->create_ai_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **create_ai_session_request** | [**CreateAISessionRequest**](CreateAISessionRequest.md)|  | 

### Return type

[**CreateAISession201Response**](CreateAISession201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Session created successfully |  -  |
**400** | Invalid request (missing userId or invalid parameters) |  -  |
**500** | Failed to create session |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_ai_session**
> DeleteAISession200Response delete_ai_session(organisation, session_id)

Delete a chat session

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.delete_ai_session200_response import DeleteAISession200Response
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
    api_instance = quantcdn.AISessionsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    session_id = 'session_id_example' # str | The session ID

    try:
        # Delete a chat session
        api_response = api_instance.delete_ai_session(organisation, session_id)
        print("The response of AISessionsApi->delete_ai_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISessionsApi->delete_ai_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **session_id** | **str**| The session ID | 

### Return type

[**DeleteAISession200Response**](DeleteAISession200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Session deleted successfully |  -  |
**500** | Failed to delete session |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **extend_ai_session**
> ExtendAISession200Response extend_ai_session(organisation, session_id, extend_ai_session_request=extend_ai_session_request)

Extend Session Expiration

Extends the expiration time of an active session. Useful for keeping long-running conversations alive.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.extend_ai_session200_response import ExtendAISession200Response
from quantcdn.models.extend_ai_session_request import ExtendAISessionRequest
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
    api_instance = quantcdn.AISessionsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    session_id = 'session_id_example' # str | The session ID
    extend_ai_session_request = quantcdn.ExtendAISessionRequest() # ExtendAISessionRequest |  (optional)

    try:
        # Extend Session Expiration
        api_response = api_instance.extend_ai_session(organisation, session_id, extend_ai_session_request=extend_ai_session_request)
        print("The response of AISessionsApi->extend_ai_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISessionsApi->extend_ai_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **session_id** | **str**| The session ID | 
 **extend_ai_session_request** | [**ExtendAISessionRequest**](ExtendAISessionRequest.md)|  | [optional] 

### Return type

[**ExtendAISession200Response**](ExtendAISession200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Session extended successfully |  -  |
**400** | Invalid parameters |  -  |
**403** | Access denied |  -  |
**404** | Session not found |  -  |
**500** | Failed to extend session |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_ai_session**
> GetAISession200Response get_ai_session(organisation, session_id)

Get a specific chat session

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_ai_session200_response import GetAISession200Response
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
    api_instance = quantcdn.AISessionsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    session_id = 'session_id_example' # str | The session ID

    try:
        # Get a specific chat session
        api_response = api_instance.get_ai_session(organisation, session_id)
        print("The response of AISessionsApi->get_ai_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISessionsApi->get_ai_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **session_id** | **str**| The session ID | 

### Return type

[**GetAISession200Response**](GetAISession200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The chat session |  -  |
**404** | Session not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_ai_sessions**
> List[ListAISessions200ResponseInner] list_ai_sessions(organisation, user_id=user_id, session_group=session_group, limit=limit, offset=offset, model=model)

List chat sessions with multi-tenant filtering

Lists active sessions for an organization with flexible filtering options.
     *
     * **Query Combinations:**
     * 1. By Organization (default): Returns all sessions in the organization
     * 2. By Organization + Group: `?sessionGroup=drupal-prod` - Sessions in a specific group
     * 3. By User: `?userId=user-123` - All sessions for a user
     * 4. By User + Group: `?userId=user-123&sessionGroup=drupal-prod` - User's sessions in a specific group
     *
     * **Use Cases:**
     * - List user's conversations in a specific app/environment
     * - Admin view of all sessions in a customer/tenant group
     * - User profile showing all AI conversations across apps

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_ai_sessions200_response_inner import ListAISessions200ResponseInner
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
    api_instance = quantcdn.AISessionsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    user_id = 'user-12345' # str | Filter sessions by user ID (optional)
    session_group = 'drupal-production' # str | Filter by session group. Returns only sessions matching the specified group. (optional)
    limit = 50 # int | Maximum number of sessions to return (default 50, max 100) (optional) (default to 50)
    offset = 56 # int | Offset for pagination (optional)
    model = 'model_example' # str | Filter by model ID (optional)

    try:
        # List chat sessions with multi-tenant filtering
        api_response = api_instance.list_ai_sessions(organisation, user_id=user_id, session_group=session_group, limit=limit, offset=offset, model=model)
        print("The response of AISessionsApi->list_ai_sessions:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISessionsApi->list_ai_sessions: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **user_id** | **str**| Filter sessions by user ID | [optional] 
 **session_group** | **str**| Filter by session group. Returns only sessions matching the specified group. | [optional] 
 **limit** | **int**| Maximum number of sessions to return (default 50, max 100) | [optional] [default to 50]
 **offset** | **int**| Offset for pagination | [optional] 
 **model** | **str**| Filter by model ID | [optional] 

### Return type

[**List[ListAISessions200ResponseInner]**](ListAISessions200ResponseInner.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of chat sessions |  -  |
**500** | Failed to fetch sessions |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_ai_session**
> UpdateAISession200Response update_ai_session(organisation, session_id, update_ai_session_request)

Update Session

Updates session with new conversation messages and tracks token usage. Appends new messages to conversation history and updates session stats.
     *
     * **Typical Flow:**
     * 1. Get session to retrieve conversation history
     * 2. Call AI inference with full message history
     * 3. Update session with new user + assistant messages

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.update_ai_session200_response import UpdateAISession200Response
from quantcdn.models.update_ai_session_request import UpdateAISessionRequest
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
    api_instance = quantcdn.AISessionsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    session_id = 'session_id_example' # str | The session ID
    update_ai_session_request = quantcdn.UpdateAISessionRequest() # UpdateAISessionRequest | 

    try:
        # Update Session
        api_response = api_instance.update_ai_session(organisation, session_id, update_ai_session_request)
        print("The response of AISessionsApi->update_ai_session:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISessionsApi->update_ai_session: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **session_id** | **str**| The session ID | 
 **update_ai_session_request** | [**UpdateAISessionRequest**](UpdateAISessionRequest.md)|  | 

### Return type

[**UpdateAISession200Response**](UpdateAISession200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Session updated successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**404** | Session not found |  -  |
**500** | Failed to update session |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

