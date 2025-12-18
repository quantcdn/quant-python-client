# quantcdn.EnvironmentsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_environment**](EnvironmentsApi.md#create_environment) | **POST** /api/v3/organizations/{organisation}/applications/{application}/environments | Create a new environment
[**delete_environment**](EnvironmentsApi.md#delete_environment) | **DELETE** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment} | Delete an environment
[**get_environment**](EnvironmentsApi.md#get_environment) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment} | Get a single environment
[**get_environment_logs**](EnvironmentsApi.md#get_environment_logs) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/logs | Get the logs for an environment
[**get_environment_metrics**](EnvironmentsApi.md#get_environment_metrics) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/metrics | Get the metrics for an environment
[**list_environments**](EnvironmentsApi.md#list_environments) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments | Get all environments for an application
[**list_sync_operations**](EnvironmentsApi.md#list_sync_operations) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/sync/{type} | List the sync operations for an environment
[**sync_to_environment**](EnvironmentsApi.md#sync_to_environment) | **POST** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/sync/{type} | Perform a sync operation from a source environment to the current environment
[**update_environment**](EnvironmentsApi.md#update_environment) | **PUT** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment} | Update Environment Compose Definition
[**update_environment_state**](EnvironmentsApi.md#update_environment_state) | **PUT** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/state | Update the state of an environment


# **create_environment**
> EnvironmentResponse create_environment(organisation, application, create_environment_request)

Create a new environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_environment_request import CreateEnvironmentRequest
from quantcdn.models.environment_response import EnvironmentResponse
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
    api_instance = quantcdn.EnvironmentsApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    create_environment_request = quantcdn.CreateEnvironmentRequest() # CreateEnvironmentRequest | 

    try:
        # Create a new environment
        api_response = api_instance.create_environment(organisation, application, create_environment_request)
        print("The response of EnvironmentsApi->create_environment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnvironmentsApi->create_environment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **create_environment_request** | [**CreateEnvironmentRequest**](CreateEnvironmentRequest.md)|  | 

### Return type

[**EnvironmentResponse**](EnvironmentResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The environment created |  -  |
**400** | The environment data is invalid |  -  |
**403** | Environment limit reached - application has reached the maximum number of allowed environments |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_environment**
> delete_environment(organisation, application, environment)

Delete an environment

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
    api_instance = quantcdn.EnvironmentsApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID

    try:
        # Delete an environment
        api_instance.delete_environment(organisation, application, environment)
    except Exception as e:
        print("Exception when calling EnvironmentsApi->delete_environment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | The environment deleted |  -  |
**404** | The environment not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_environment**
> EnvironmentResponse get_environment(organisation, application, environment)

Get a single environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.environment_response import EnvironmentResponse
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
    api_instance = quantcdn.EnvironmentsApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID

    try:
        # Get a single environment
        api_response = api_instance.get_environment(organisation, application, environment)
        print("The response of EnvironmentsApi->get_environment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnvironmentsApi->get_environment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 

### Return type

[**EnvironmentResponse**](EnvironmentResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The environment with runtime details |  -  |
**404** | The environment not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_environment_logs**
> GetEnvironmentLogs200Response get_environment_logs(organisation, application, environment, start_time=start_time, end_time=end_time, container_name=container_name, filter_pattern=filter_pattern, limit=limit, next_token=next_token)

Get the logs for an environment

Retrieves logs from CloudWatch for the specified environment with optional filtering by time range, container, and pattern matching. Supports pagination via nextToken.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_environment_logs200_response import GetEnvironmentLogs200Response
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
    api_instance = quantcdn.EnvironmentsApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID
    start_time = 'start_time_example' # str | Start time for log retrieval (ISO 8601 format or Unix timestamp) (optional)
    end_time = 'end_time_example' # str | End time for log retrieval (ISO 8601 format or Unix timestamp) (optional)
    container_name = 'container_name_example' # str | Filter logs by specific container name (optional)
    filter_pattern = 'filter_pattern_example' # str | CloudWatch Logs filter pattern for searching log content (optional)
    limit = 56 # int | Maximum number of log entries to return per page (optional)
    next_token = 'next_token_example' # str | Pagination token from previous response for retrieving next page of results (optional)

    try:
        # Get the logs for an environment
        api_response = api_instance.get_environment_logs(organisation, application, environment, start_time=start_time, end_time=end_time, container_name=container_name, filter_pattern=filter_pattern, limit=limit, next_token=next_token)
        print("The response of EnvironmentsApi->get_environment_logs:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnvironmentsApi->get_environment_logs: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **start_time** | **str**| Start time for log retrieval (ISO 8601 format or Unix timestamp) | [optional] 
 **end_time** | **str**| End time for log retrieval (ISO 8601 format or Unix timestamp) | [optional] 
 **container_name** | **str**| Filter logs by specific container name | [optional] 
 **filter_pattern** | **str**| CloudWatch Logs filter pattern for searching log content | [optional] 
 **limit** | **int**| Maximum number of log entries to return per page | [optional] 
 **next_token** | **str**| Pagination token from previous response for retrieving next page of results | [optional] 

### Return type

[**GetEnvironmentLogs200Response**](GetEnvironmentLogs200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The logs |  -  |
**404** | The environment not found |  -  |
**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_environment_metrics**
> object get_environment_metrics(organisation, application, environment, start_time=start_time, end_time=end_time, period=period, statistics=statistics, container_name=container_name)

Get the metrics for an environment

Retrieves CloudWatch metrics for the specified environment with optional filtering by time range, container, and metric configuration.

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
    api_instance = quantcdn.EnvironmentsApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID
    start_time = 56 # int | Start time for metrics retrieval (Unix timestamp in milliseconds) (optional)
    end_time = 56 # int | End time for metrics retrieval (Unix timestamp in milliseconds) (optional)
    period = 56 # int | Period in seconds for metric aggregation (e.g., 60 for 1 minute, 300 for 5 minutes) (optional)
    statistics = 'statistics_example' # str | Comma-separated list of CloudWatch statistics (e.g., Average, Maximum, Minimum, Sum, SampleCount) (optional)
    container_name = 'container_name_example' # str | Filter metrics by specific container name (optional)

    try:
        # Get the metrics for an environment
        api_response = api_instance.get_environment_metrics(organisation, application, environment, start_time=start_time, end_time=end_time, period=period, statistics=statistics, container_name=container_name)
        print("The response of EnvironmentsApi->get_environment_metrics:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnvironmentsApi->get_environment_metrics: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **start_time** | **int**| Start time for metrics retrieval (Unix timestamp in milliseconds) | [optional] 
 **end_time** | **int**| End time for metrics retrieval (Unix timestamp in milliseconds) | [optional] 
 **period** | **int**| Period in seconds for metric aggregation (e.g., 60 for 1 minute, 300 for 5 minutes) | [optional] 
 **statistics** | **str**| Comma-separated list of CloudWatch statistics (e.g., Average, Maximum, Minimum, Sum, SampleCount) | [optional] 
 **container_name** | **str**| Filter metrics by specific container name | [optional] 

### Return type

**object**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The metrics |  -  |
**404** | The environment not found |  -  |
**422** | Validation error |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_environments**
> List[EnvironmentSummary] list_environments(organisation, application)

Get all environments for an application

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.environment_summary import EnvironmentSummary
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
    api_instance = quantcdn.EnvironmentsApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID

    try:
        # Get all environments for an application
        api_response = api_instance.list_environments(organisation, application)
        print("The response of EnvironmentsApi->list_environments:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnvironmentsApi->list_environments: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 

### Return type

[**List[EnvironmentSummary]**](EnvironmentSummary.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of environments with summary information including deployment status |  -  |
**404** | The organisation or application not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_sync_operations**
> List[SyncOperation] list_sync_operations(organisation, application, environment, type)

List the sync operations for an environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.sync_operation import SyncOperation
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
    api_instance = quantcdn.EnvironmentsApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID
    type = 'type_example' # str | The sync type

    try:
        # List the sync operations for an environment
        api_response = api_instance.list_sync_operations(organisation, application, environment, type)
        print("The response of EnvironmentsApi->list_sync_operations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnvironmentsApi->list_sync_operations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **type** | **str**| The sync type | 

### Return type

[**List[SyncOperation]**](SyncOperation.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The sync operations |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sync_to_environment**
> SyncOperation sync_to_environment(organisation, application, environment, type, sync_to_environment_request)

Perform a sync operation from a source environment to the current environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.sync_operation import SyncOperation
from quantcdn.models.sync_to_environment_request import SyncToEnvironmentRequest
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
    api_instance = quantcdn.EnvironmentsApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID
    type = 'type_example' # str | The sync type
    sync_to_environment_request = quantcdn.SyncToEnvironmentRequest() # SyncToEnvironmentRequest | 

    try:
        # Perform a sync operation from a source environment to the current environment
        api_response = api_instance.sync_to_environment(organisation, application, environment, type, sync_to_environment_request)
        print("The response of EnvironmentsApi->sync_to_environment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling EnvironmentsApi->sync_to_environment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **type** | **str**| The sync type | 
 **sync_to_environment_request** | [**SyncToEnvironmentRequest**](SyncToEnvironmentRequest.md)|  | 

### Return type

[**SyncOperation**](SyncOperation.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The sync operation details |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_environment**
> update_environment(organisation, application, environment, update_environment_request)

Update Environment Compose Definition

Replaces the entire task definition for the environment based on the provided multi-container compose definition. This will create a new task definition revision and update the ECS service, triggering a redeployment. Optionally accepts minCapacity and maxCapacity at the root level for convenience.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.update_environment_request import UpdateEnvironmentRequest
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
    api_instance = quantcdn.EnvironmentsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    application = 'application_example' # str | The application ID
    environment = 'environment_example' # str | The environment ID
    update_environment_request = quantcdn.UpdateEnvironmentRequest() # UpdateEnvironmentRequest | 

    try:
        # Update Environment Compose Definition
        api_instance.update_environment(organisation, application, environment, update_environment_request)
    except Exception as e:
        print("Exception when calling EnvironmentsApi->update_environment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **update_environment_request** | [**UpdateEnvironmentRequest**](UpdateEnvironmentRequest.md)|  | 

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
**202** | Request accepted, compose definition update is processing. |  -  |
**400** | Invalid compose definition or validation failed. |  -  |
**404** | Application or environment not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_environment_state**
> update_environment_state(organisation, application, environment, update_environment_state_request)

Update the state of an environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.update_environment_state_request import UpdateEnvironmentStateRequest
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
    api_instance = quantcdn.EnvironmentsApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID
    update_environment_state_request = quantcdn.UpdateEnvironmentStateRequest() # UpdateEnvironmentStateRequest | 

    try:
        # Update the state of an environment
        api_instance.update_environment_state(organisation, application, environment, update_environment_state_request)
    except Exception as e:
        print("Exception when calling EnvironmentsApi->update_environment_state: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **update_environment_state_request** | [**UpdateEnvironmentStateRequest**](UpdateEnvironmentStateRequest.md)|  | 

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: Not defined

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | The environment state updated |  -  |
**400** | The environment data is invalid |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

