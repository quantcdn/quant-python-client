# quantcdn.CommandsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_command**](CommandsApi.md#create_command) | **POST** /api/v3/organizations/{organisation}/environments/{environment}/commands | Create a command for an environment
[**get_command**](CommandsApi.md#get_command) | **GET** /api/v3/organizations/{organisation}/environments/{environment}/commands/{command} | Get a command
[**list_commands**](CommandsApi.md#list_commands) | **GET** /api/v3/organizations/{organisation}/environments/{environment}/commands | Get all commands for an environment


# **create_command**
> Command create_command(organisation, environment, create_command_request)

Create a command for an environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.command import Command
from quantcdn.models.create_command_request import CreateCommandRequest
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
    api_instance = quantcdn.CommandsApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    environment = 'test-env' # str | The environment ID
    create_command_request = quantcdn.CreateCommandRequest() # CreateCommandRequest | 

    try:
        # Create a command for an environment
        api_response = api_instance.create_command(organisation, environment, create_command_request)
        print("The response of CommandsApi->create_command:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CommandsApi->create_command: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **environment** | **str**| The environment ID | 
 **create_command_request** | [**CreateCommandRequest**](CreateCommandRequest.md)|  | 

### Return type

[**Command**](Command.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The command |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_command**
> Command get_command(organisation, environment, command)

Get a command

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.command import Command
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
    api_instance = quantcdn.CommandsApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    environment = 'test-env' # str | The environment ID
    command = 'test-cmd' # str | The command ID

    try:
        # Get a command
        api_response = api_instance.get_command(organisation, environment, command)
        print("The response of CommandsApi->get_command:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CommandsApi->get_command: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **environment** | **str**| The environment ID | 
 **command** | **str**| The command ID | 

### Return type

[**Command**](Command.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The command |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_commands**
> Command list_commands(organisation, environment)

Get all commands for an environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.command import Command
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
    api_instance = quantcdn.CommandsApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    environment = 'test-env' # str | The environment ID

    try:
        # Get all commands for an environment
        api_response = api_instance.list_commands(organisation, environment)
        print("The response of CommandsApi->list_commands:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CommandsApi->list_commands: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **environment** | **str**| The environment ID | 

### Return type

[**Command**](Command.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The commands |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

