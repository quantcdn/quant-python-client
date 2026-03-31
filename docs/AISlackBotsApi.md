# quantcdn.AISlackBotsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_slack_bot**](AISlackBotsApi.md#create_slack_bot) | **POST** /api/v3/organizations/{organisation}/ai/slack-bots | Create Slack Bot
[**delete_slack_bot**](AISlackBotsApi.md#delete_slack_bot) | **DELETE** /api/v3/organizations/{organisation}/ai/slack-bots/{botId} | Delete Slack Bot
[**get_slack_bot**](AISlackBotsApi.md#get_slack_bot) | **GET** /api/v3/organizations/{organisation}/ai/slack-bots/{botId} | Get Slack Bot
[**list_slack_bots**](AISlackBotsApi.md#list_slack_bots) | **GET** /api/v3/organizations/{organisation}/ai/slack-bots | List Slack Bots
[**search_slack_workspace_channels**](AISlackBotsApi.md#search_slack_workspace_channels) | **GET** /api/v3/organizations/{organisation}/ai/slack-bots/{botId}/workspace/channels | Search Slack Workspace Channels
[**search_slack_workspace_users**](AISlackBotsApi.md#search_slack_workspace_users) | **GET** /api/v3/organizations/{organisation}/ai/slack-bots/{botId}/workspace/users | Search Slack Workspace Users
[**update_slack_bot**](AISlackBotsApi.md#update_slack_bot) | **PUT** /api/v3/organizations/{organisation}/ai/slack-bots/{botId} | Update Slack Bot


# **create_slack_bot**
> CreateSlackBot201Response create_slack_bot(organisation, create_slack_bot_request)

Create Slack Bot

Creates a new Slack bot backed by an AI agent. The bot must be connected to a Slack workspace via OAuth before it can receive events.
     *
     * **Setup Types:**
     * - `quant`: Quant-managed Slack app — uses shared OAuth credentials
     * - `byo`: Bring Your Own — customer provides their own Slack app credentials

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_slack_bot201_response import CreateSlackBot201Response
from quantcdn.models.create_slack_bot_request import CreateSlackBotRequest
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
    api_instance = quantcdn.AISlackBotsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    create_slack_bot_request = quantcdn.CreateSlackBotRequest() # CreateSlackBotRequest | 

    try:
        # Create Slack Bot
        api_response = api_instance.create_slack_bot(organisation, create_slack_bot_request)
        print("The response of AISlackBotsApi->create_slack_bot:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISlackBotsApi->create_slack_bot: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **create_slack_bot_request** | [**CreateSlackBotRequest**](CreateSlackBotRequest.md)|  | 

### Return type

[**CreateSlackBot201Response**](CreateSlackBot201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Slack bot created successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**500** | Failed to create Slack bot |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_slack_bot**
> DeleteSlackBot200Response delete_slack_bot(organisation, bot_id)

Delete Slack Bot

Permanently deletes a Slack bot and disconnects it from the workspace.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.delete_slack_bot200_response import DeleteSlackBot200Response
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
    api_instance = quantcdn.AISlackBotsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    bot_id = 'bot_id_example' # str | The Slack bot ID

    try:
        # Delete Slack Bot
        api_response = api_instance.delete_slack_bot(organisation, bot_id)
        print("The response of AISlackBotsApi->delete_slack_bot:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISlackBotsApi->delete_slack_bot: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **bot_id** | **str**| The Slack bot ID | 

### Return type

[**DeleteSlackBot200Response**](DeleteSlackBot200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Slack bot deleted successfully |  -  |
**403** | Access denied |  -  |
**404** | Slack bot not found |  -  |
**500** | Failed to delete Slack bot |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_slack_bot**
> GetSlackBot200Response get_slack_bot(organisation, bot_id)

Get Slack Bot

Retrieves details for a specific Slack bot including its configuration and connection status.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_slack_bot200_response import GetSlackBot200Response
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
    api_instance = quantcdn.AISlackBotsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    bot_id = 'bot_id_example' # str | The Slack bot ID

    try:
        # Get Slack Bot
        api_response = api_instance.get_slack_bot(organisation, bot_id)
        print("The response of AISlackBotsApi->get_slack_bot:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISlackBotsApi->get_slack_bot: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **bot_id** | **str**| The Slack bot ID | 

### Return type

[**GetSlackBot200Response**](GetSlackBot200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Slack bot details retrieved successfully |  -  |
**403** | Access denied |  -  |
**404** | Slack bot not found |  -  |
**500** | Failed to retrieve Slack bot |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_slack_bots**
> ListSlackBots200Response list_slack_bots(organisation)

List Slack Bots

Lists all Slack bots configured for the organization. Each bot is backed by an AI agent and can be connected to a Slack workspace.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_slack_bots200_response import ListSlackBots200Response
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
    api_instance = quantcdn.AISlackBotsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # List Slack Bots
        api_response = api_instance.list_slack_bots(organisation)
        print("The response of AISlackBotsApi->list_slack_bots:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISlackBotsApi->list_slack_bots: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**ListSlackBots200Response**](ListSlackBots200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Slack bots retrieved successfully |  -  |
**403** | Access denied |  -  |
**500** | Failed to retrieve Slack bots |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **search_slack_workspace_channels**
> SearchSlackWorkspaceChannels200Response search_slack_workspace_channels(organisation, bot_id, q=q)

Search Slack Workspace Channels

Searches channels in the Slack workspace connected to this bot. Requires the bot to be connected via OAuth.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.search_slack_workspace_channels200_response import SearchSlackWorkspaceChannels200Response
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
    api_instance = quantcdn.AISlackBotsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    bot_id = 'bot_id_example' # str | The Slack bot ID
    q = 'q_example' # str | Search query to filter channels by name (optional)

    try:
        # Search Slack Workspace Channels
        api_response = api_instance.search_slack_workspace_channels(organisation, bot_id, q=q)
        print("The response of AISlackBotsApi->search_slack_workspace_channels:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISlackBotsApi->search_slack_workspace_channels: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **bot_id** | **str**| The Slack bot ID | 
 **q** | **str**| Search query to filter channels by name | [optional] 

### Return type

[**SearchSlackWorkspaceChannels200Response**](SearchSlackWorkspaceChannels200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Workspace channels retrieved successfully |  -  |
**403** | Access denied |  -  |
**404** | Slack bot not found or not connected |  -  |
**500** | Failed to search channels |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **search_slack_workspace_users**
> SearchSlackWorkspaceUsers200Response search_slack_workspace_users(organisation, bot_id, q=q)

Search Slack Workspace Users

Searches users in the Slack workspace connected to this bot. Requires the bot to be connected via OAuth.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.search_slack_workspace_users200_response import SearchSlackWorkspaceUsers200Response
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
    api_instance = quantcdn.AISlackBotsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    bot_id = 'bot_id_example' # str | The Slack bot ID
    q = 'q_example' # str | Search query to filter users by name (optional)

    try:
        # Search Slack Workspace Users
        api_response = api_instance.search_slack_workspace_users(organisation, bot_id, q=q)
        print("The response of AISlackBotsApi->search_slack_workspace_users:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISlackBotsApi->search_slack_workspace_users: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **bot_id** | **str**| The Slack bot ID | 
 **q** | **str**| Search query to filter users by name | [optional] 

### Return type

[**SearchSlackWorkspaceUsers200Response**](SearchSlackWorkspaceUsers200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Workspace users retrieved successfully |  -  |
**403** | Access denied |  -  |
**404** | Slack bot not found or not connected |  -  |
**500** | Failed to search users |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_slack_bot**
> CreateSlackBot201Response update_slack_bot(organisation, bot_id, update_slack_bot_request)

Update Slack Bot

Updates a Slack bot's configuration. Only provided fields are updated.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_slack_bot201_response import CreateSlackBot201Response
from quantcdn.models.update_slack_bot_request import UpdateSlackBotRequest
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
    api_instance = quantcdn.AISlackBotsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    bot_id = 'bot_id_example' # str | The Slack bot ID
    update_slack_bot_request = quantcdn.UpdateSlackBotRequest() # UpdateSlackBotRequest | 

    try:
        # Update Slack Bot
        api_response = api_instance.update_slack_bot(organisation, bot_id, update_slack_bot_request)
        print("The response of AISlackBotsApi->update_slack_bot:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISlackBotsApi->update_slack_bot: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **bot_id** | **str**| The Slack bot ID | 
 **update_slack_bot_request** | [**UpdateSlackBotRequest**](UpdateSlackBotRequest.md)|  | 

### Return type

[**CreateSlackBot201Response**](CreateSlackBot201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Slack bot updated successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**404** | Slack bot not found |  -  |
**500** | Failed to update Slack bot |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

