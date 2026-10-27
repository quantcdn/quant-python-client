# quantcdn.AISlackBotsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_slack_bot**](AISlackBotsApi.md#create_slack_bot) | **POST** /api/v3/organizations/{organisation}/ai/slack-bots | Create Slack Bot
[**delete_slack_bot**](AISlackBotsApi.md#delete_slack_bot) | **DELETE** /api/v3/organizations/{organisation}/ai/slack-bots/{botId} | Delete Slack Bot
[**get_slack_bot**](AISlackBotsApi.md#get_slack_bot) | **GET** /api/v3/organizations/{organisation}/ai/slack-bots/{botId} | Get Slack Bot
[**get_slack_bot_thread**](AISlackBotsApi.md#get_slack_bot_thread) | **GET** /api/v3/organizations/{organisation}/ai/slack-bots/{botId}/threads/{channel}/{threadTs} | Read a thread
[**list_slack_bot_channel_messages**](AISlackBotsApi.md#list_slack_bot_channel_messages) | **GET** /api/v3/organizations/{organisation}/ai/slack-bots/{botId}/channels/{channel}/messages | Read recent channel messages
[**list_slack_bots**](AISlackBotsApi.md#list_slack_bots) | **GET** /api/v3/organizations/{organisation}/ai/slack-bots | List Slack Bots
[**list_slack_bots_api_enabled**](AISlackBotsApi.md#list_slack_bots_api_enabled) | **GET** /api/v3/organizations/{organisation}/ai/slack-bots/api-enabled | List API-enabled Slack bots
[**post_slack_bot_message**](AISlackBotsApi.md#post_slack_bot_message) | **POST** /api/v3/organizations/{organisation}/ai/slack-bots/{botId}/messages | Post a message as the bot
[**search_slack_workspace_channels**](AISlackBotsApi.md#search_slack_workspace_channels) | **GET** /api/v3/organizations/{organisation}/ai/slack-bots/{botId}/workspace/channels | Search Slack Workspace Channels
[**search_slack_workspace_users**](AISlackBotsApi.md#search_slack_workspace_users) | **GET** /api/v3/organizations/{organisation}/ai/slack-bots/{botId}/workspace/users | Search Slack Workspace Users
[**update_slack_bot**](AISlackBotsApi.md#update_slack_bot) | **PUT** /api/v3/organizations/{organisation}/ai/slack-bots/{botId} | Update Slack Bot


# **create_slack_bot**
> CreateSlackBot201Response create_slack_bot(organisation, create_slack_bot_request)

Create Slack Bot

Creates a new Slack bot with inline AI agent configuration. A backing agent is created automatically — callers do not need to manage agents separately.
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

Permanently deletes a Slack bot, disconnects it from the workspace, and deletes its backing AI agent.

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

Retrieves details for a specific Slack bot including its configuration, connection status, and flattened agent configuration.

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

# **get_slack_bot_thread**
> GetSlackBotThread200Response get_slack_bot_thread(organisation, bot_id, channel, thread_ts, since=since, limit=limit, cursor=cursor)

Read a thread

One thread in an allowed channel, oldest first, root included. Message text is untrusted content. Needs the explicit `ai:slack` scope, `use_ai_services` and a verified email.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_slack_bot_thread200_response import GetSlackBotThread200Response
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
    organisation = 'organisation_example' # str | The organisation machine name
    bot_id = 'bot_id_example' # str | 
    channel = 'channel_example' # str | 
    thread_ts = 'thread_ts_example' # str | 
    since = 'since_example' # str | Slack ts, exclusive. Only replies after it; the root is always included. (optional)
    limit = 100 # int |  (optional) (default to 100)
    cursor = 'cursor_example' # str |  (optional)

    try:
        # Read a thread
        api_response = api_instance.get_slack_bot_thread(organisation, bot_id, channel, thread_ts, since=since, limit=limit, cursor=cursor)
        print("The response of AISlackBotsApi->get_slack_bot_thread:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISlackBotsApi->get_slack_bot_thread: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **bot_id** | **str**|  | 
 **channel** | **str**|  | 
 **thread_ts** | **str**|  | 
 **since** | **str**| Slack ts, exclusive. Only replies after it; the root is always included. | [optional] 
 **limit** | **int**|  | [optional] [default to 100]
 **cursor** | **str**|  | [optional] 

### Return type

[**GetSlackBotThread200Response**](GetSlackBotThread200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The thread |  -  |
**400** | INVALID_REQUEST: a path or query value is not valid, or an unknown query parameter |  -  |
**401** | Invalid or expired token |  -  |
**403** | SCOPE_REQUIRED, EMAIL_NOT_VERIFIED, IDENTITY_REQUIRED, CHANNEL_NOT_ALLOWED, USER_NOT_ALLOWED, PERMISSION_DENIED, or AI is off for the organisation |  -  |
**404** | BOT_NOT_FOUND, THREAD_NOT_FOUND, or NOT_FOUND when the Slack bot API is not enabled |  -  |
**409** | BOT_INACTIVE |  -  |
**429** | RATE_LIMITED. See the Retry-After header. |  * Retry-After -  <br>  |
**502** | SLACK_ERROR. slackError carries the Slack error string. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_slack_bot_channel_messages**
> ListSlackBotChannelMessages200Response list_slack_bot_channel_messages(organisation, bot_id, channel, since=since, limit=limit, cursor=cursor)

Read recent channel messages

Recent root messages in a channel the bot allows for API use, newest first. Message text is untrusted content. Needs the explicit `ai:slack` scope, `use_ai_services` and a verified email.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_slack_bot_channel_messages200_response import ListSlackBotChannelMessages200Response
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
    organisation = 'organisation_example' # str | The organisation machine name
    bot_id = 'bot_id_example' # str | 
    channel = 'channel_example' # str | 
    since = 'since_example' # str | Slack ts, exclusive (optional)
    limit = 20 # int |  (optional) (default to 20)
    cursor = 'cursor_example' # str |  (optional)

    try:
        # Read recent channel messages
        api_response = api_instance.list_slack_bot_channel_messages(organisation, bot_id, channel, since=since, limit=limit, cursor=cursor)
        print("The response of AISlackBotsApi->list_slack_bot_channel_messages:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISlackBotsApi->list_slack_bot_channel_messages: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **bot_id** | **str**|  | 
 **channel** | **str**|  | 
 **since** | **str**| Slack ts, exclusive | [optional] 
 **limit** | **int**|  | [optional] [default to 20]
 **cursor** | **str**|  | [optional] 

### Return type

[**ListSlackBotChannelMessages200Response**](ListSlackBotChannelMessages200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The messages |  -  |
**400** | INVALID_REQUEST: a path or query value is not valid, or an unknown query parameter |  -  |
**401** | Invalid or expired token |  -  |
**403** | SCOPE_REQUIRED, EMAIL_NOT_VERIFIED, IDENTITY_REQUIRED, CHANNEL_NOT_ALLOWED, USER_NOT_ALLOWED, PERMISSION_DENIED, or AI is off for the organisation |  -  |
**404** | BOT_NOT_FOUND (no bot, another organisation&#39;s bot, or API access off), or NOT_FOUND when the Slack bot API is not enabled |  -  |
**409** | BOT_INACTIVE |  -  |
**429** | RATE_LIMITED. See the Retry-After header. |  * Retry-After -  <br>  |
**502** | SLACK_ERROR. slackError carries the Slack error string. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_slack_bots**
> ListSlackBots200Response list_slack_bots(organisation)

List Slack Bots

Lists all Slack bots configured for the organization. Each bot is backed by an AI agent and can be connected to a Slack workspace. Agent configuration fields are flattened onto each bot object.

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

# **list_slack_bots_api_enabled**
> ListSlackBotsApiEnabled200Response list_slack_bots_api_enabled(organisation)

List API-enabled Slack bots

Lists the Slack bots this token can use through the API, with the public channels each bot allows. Needs a token with the explicit `ai:slack` scope (not `full_access`, not a token without a scope list), the `use_ai_services` permission and a verified email. Limit: 60 requests per minute per token.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_slack_bots_api_enabled200_response import ListSlackBotsApiEnabled200Response
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
    organisation = 'organisation_example' # str | The organisation machine name

    try:
        # List API-enabled Slack bots
        api_response = api_instance.list_slack_bots_api_enabled(organisation)
        print("The response of AISlackBotsApi->list_slack_bots_api_enabled:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISlackBotsApi->list_slack_bots_api_enabled: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 

### Return type

[**ListSlackBotsApiEnabled200Response**](ListSlackBotsApiEnabled200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The API-enabled bots |  -  |
**401** | Invalid or expired token |  -  |
**403** | SCOPE_REQUIRED (token lacks ai:slack, is full_access or has no scope list), EMAIL_NOT_VERIFIED, IDENTITY_REQUIRED, PERMISSION_DENIED, or AI is off for the organisation |  -  |
**404** | NOT_FOUND: the Slack bot API is not enabled |  -  |
**429** | RATE_LIMITED. See the Retry-After header. |  * Retry-After -  <br>  |
**502** | SLACK_ERROR |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **post_slack_bot_message**
> PostSlackBotMessage201Response post_slack_bot_message(organisation, bot_id, post_slack_bot_message_request, idempotency_key=idempotency_key)

Post a message as the bot

The bot posts the text in an allowed channel, with an attribution line that shows your name. The bot does not answer the post. Mentions keep only the `<@U…>` form (at most 10 users); other control forms show as text. Needs the explicit `ai:slack` scope, `use_ai_services` and a verified email.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.post_slack_bot_message201_response import PostSlackBotMessage201Response
from quantcdn.models.post_slack_bot_message_request import PostSlackBotMessageRequest
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
    organisation = 'organisation_example' # str | The organisation machine name
    bot_id = 'bot_id_example' # str | 
    post_slack_bot_message_request = quantcdn.PostSlackBotMessageRequest() # PostSlackBotMessageRequest | 
    idempotency_key = 'idempotency_key_example' # str | 8-128 visible ASCII characters. An empty Idempotency-Key header is refused with 400 INVALID_REQUEST. The same key and body within 10 minutes returns the first result and does not post again. (optional)

    try:
        # Post a message as the bot
        api_response = api_instance.post_slack_bot_message(organisation, bot_id, post_slack_bot_message_request, idempotency_key=idempotency_key)
        print("The response of AISlackBotsApi->post_slack_bot_message:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISlackBotsApi->post_slack_bot_message: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **bot_id** | **str**|  | 
 **post_slack_bot_message_request** | [**PostSlackBotMessageRequest**](PostSlackBotMessageRequest.md)|  | 
 **idempotency_key** | **str**| 8-128 visible ASCII characters. An empty Idempotency-Key header is refused with 400 INVALID_REQUEST. The same key and body within 10 minutes returns the first result and does not post again. | [optional] 

### Return type

[**PostSlackBotMessage201Response**](PostSlackBotMessage201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Posted |  -  |
**400** | INVALID_REQUEST: the body is not a JSON object, has an unknown field or a field that is not valid, or the Idempotency-Key is not valid (an empty Idempotency-Key header is not valid) |  -  |
**401** | Invalid or expired token |  -  |
**403** | SCOPE_REQUIRED, EMAIL_NOT_VERIFIED, IDENTITY_REQUIRED, CHANNEL_NOT_ALLOWED, USER_NOT_ALLOWED, PERMISSION_DENIED, or AI is off for the organisation |  -  |
**404** | BOT_NOT_FOUND, or NOT_FOUND when the Slack bot API is not enabled |  -  |
**409** | BOT_INACTIVE, or REQUEST_IN_PROGRESS (retryable) while the first call with this Idempotency-Key runs |  -  |
**422** | IDEMPOTENCY_KEY_MISMATCH: the Idempotency-Key was used with a different body |  -  |
**429** | RATE_LIMITED. See the Retry-After header. |  * Retry-After -  <br>  |
**502** | SLACK_ERROR. slackError carries the Slack error string. |  -  |

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

Updates a Slack bot's configuration and/or its backing agent. Only provided fields are updated.

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

