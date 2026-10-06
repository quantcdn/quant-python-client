# quantcdn.AIOrchestrationsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**cancel_orchestration**](AIOrchestrationsApi.md#cancel_orchestration) | **POST** /api/v3/organizations/{organisation}/ai/orchestrations/{orchestrationId}/cancel | Cancel Durable Orchestration
[**create_orchestration**](AIOrchestrationsApi.md#create_orchestration) | **POST** /api/v3/organizations/{organisation}/ai/orchestrations | Create Durable Orchestration
[**delete_orchestration**](AIOrchestrationsApi.md#delete_orchestration) | **DELETE** /api/v3/organizations/{organisation}/ai/orchestrations/{orchestrationId} | Delete Durable Orchestration
[**get_orchestration**](AIOrchestrationsApi.md#get_orchestration) | **GET** /api/v3/organizations/{organisation}/ai/orchestrations/{orchestrationId} | Get Durable Orchestration
[**list_orchestration_batches**](AIOrchestrationsApi.md#list_orchestration_batches) | **GET** /api/v3/organizations/{organisation}/ai/orchestrations/{orchestrationId}/batches | List Orchestration Batches
[**list_orchestrations**](AIOrchestrationsApi.md#list_orchestrations) | **GET** /api/v3/organizations/{organisation}/ai/orchestrations | List Durable Orchestrations
[**pause_orchestration**](AIOrchestrationsApi.md#pause_orchestration) | **POST** /api/v3/organizations/{organisation}/ai/orchestrations/{orchestrationId}/pause | Pause Durable Orchestration
[**resume_orchestration**](AIOrchestrationsApi.md#resume_orchestration) | **POST** /api/v3/organizations/{organisation}/ai/orchestrations/{orchestrationId}/resume | Resume Durable Orchestration
[**start_orchestration**](AIOrchestrationsApi.md#start_orchestration) | **POST** /api/v3/organizations/{organisation}/ai/orchestrations/{orchestrationId}/start | Start Durable Orchestration


# **cancel_orchestration**
> object cancel_orchestration(organisation, orchestration_id)

Cancel Durable Orchestration

Cancel an orchestration permanently. Cannot be resumed. Any in-progress items will complete, but no new processing starts.

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
    api_instance = quantcdn.AIOrchestrationsApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    orchestration_id = 'orchestration_id_example' # str | Orchestration identifier

    try:
        # Cancel Durable Orchestration
        api_response = api_instance.cancel_orchestration(organisation, orchestration_id)
        print("The response of AIOrchestrationsApi->cancel_orchestration:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIOrchestrationsApi->cancel_orchestration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **orchestration_id** | **str**| Orchestration identifier | 

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
**200** | Orchestration cancelled |  -  |
**400** | Orchestration already completed/cancelled |  -  |
**403** | Access denied |  -  |
**404** | Orchestration not found |  -  |
**500** | Failed to cancel orchestration |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **create_orchestration**
> object create_orchestration(organisation, create_orchestration_request)

Create Durable Orchestration

Create a new durable orchestration for batch processing.
     *
     * **Input Sources:**
     * - `static`: Process a fixed list of items
     * - `task_query`: Process tasks matching a query
     * - `generator`: AI generates items from a prompt
     *
     * **Stop Conditions:**
     * - `all_complete`: Stop when all items processed
     * - `max_iterations`: Stop after N iterations
     * - `condition`: AI evaluates a prompt to decide
     * - `manual`: Run until manually stopped
     *
     * **Auto-start:**
     * By default, the orchestration starts immediately. Set `autoStart: false` to create in pending state.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_orchestration_request import CreateOrchestrationRequest
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
    api_instance = quantcdn.AIOrchestrationsApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    create_orchestration_request = quantcdn.CreateOrchestrationRequest() # CreateOrchestrationRequest | 

    try:
        # Create Durable Orchestration
        api_response = api_instance.create_orchestration(organisation, create_orchestration_request)
        print("The response of AIOrchestrationsApi->create_orchestration:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIOrchestrationsApi->create_orchestration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **create_orchestration_request** | [**CreateOrchestrationRequest**](CreateOrchestrationRequest.md)|  | 

### Return type

**object**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Orchestration created |  -  |
**400** | Invalid request |  -  |
**403** | Access denied |  -  |
**500** | Failed to create orchestration |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_orchestration**
> delete_orchestration(organisation, orchestration_id)

Delete Durable Orchestration

Delete an orchestration. Can only delete orchestrations in completed, failed, or cancelled status.

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
    api_instance = quantcdn.AIOrchestrationsApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    orchestration_id = 'orchestration_id_example' # str | Orchestration identifier

    try:
        # Delete Durable Orchestration
        api_instance.delete_orchestration(organisation, orchestration_id)
    except Exception as e:
        print("Exception when calling AIOrchestrationsApi->delete_orchestration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **orchestration_id** | **str**| Orchestration identifier | 

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
**204** | Orchestration deleted |  -  |
**400** | Cannot delete active orchestration |  -  |
**403** | Access denied |  -  |
**404** | Orchestration not found |  -  |
**500** | Failed to delete orchestration |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_orchestration**
> object get_orchestration(organisation, orchestration_id)

Get Durable Orchestration

Get orchestration details including status and progress.
     *
     * **Progress Tracking:**
     * - `total`: Total items to process
     * - `completed`: Successfully processed
     * - `failed`: Failed processing
     * - `pending`: Awaiting processing

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
    api_instance = quantcdn.AIOrchestrationsApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    orchestration_id = 'orch_1704067200_abc123xyz' # str | Orchestration identifier

    try:
        # Get Durable Orchestration
        api_response = api_instance.get_orchestration(organisation, orchestration_id)
        print("The response of AIOrchestrationsApi->get_orchestration:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIOrchestrationsApi->get_orchestration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **orchestration_id** | **str**| Orchestration identifier | 

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
**200** | Orchestration details |  -  |
**403** | Access denied |  -  |
**404** | Orchestration not found |  -  |
**500** | Failed to get orchestration |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_orchestration_batches**
> ListOrchestrationBatches200Response list_orchestration_batches(organisation, orchestration_id, limit=limit, cursor=cursor)

List Orchestration Batches

Get history of batches processed by this orchestration. Returns paginated batch records with status and item counts.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_orchestration_batches200_response import ListOrchestrationBatches200Response
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
    api_instance = quantcdn.AIOrchestrationsApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    orchestration_id = 'orchestration_id_example' # str | Orchestration identifier
    limit = 20 # int | Maximum number of batches to return (optional) (default to 20)
    cursor = 'cursor_example' # str | Pagination cursor from previous response (optional)

    try:
        # List Orchestration Batches
        api_response = api_instance.list_orchestration_batches(organisation, orchestration_id, limit=limit, cursor=cursor)
        print("The response of AIOrchestrationsApi->list_orchestration_batches:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIOrchestrationsApi->list_orchestration_batches: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **orchestration_id** | **str**| Orchestration identifier | 
 **limit** | **int**| Maximum number of batches to return | [optional] [default to 20]
 **cursor** | **str**| Pagination cursor from previous response | [optional] 

### Return type

[**ListOrchestrationBatches200Response**](ListOrchestrationBatches200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Batch history |  -  |
**403** | Access denied |  -  |
**404** | Orchestration not found |  -  |
**500** | Failed to list orchestration batches |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_orchestrations**
> ListOrchestrations200Response list_orchestrations(organisation, status=status, limit=limit, cursor=cursor)

List Durable Orchestrations

List durable orchestrations for an organization with optional filtering.
     *
     * **Note:** This is different from `/tools/orchestrations` which handles async tool execution
     * polling. These durable orchestrations are for long-running batch processing loops.
     *
     * **Filter Options:**
     * - `status`: Filter by orchestration status
     * - `limit`: Max results (default 20, max 100)
     * - `cursor`: Pagination cursor

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_orchestrations200_response import ListOrchestrations200Response
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
    api_instance = quantcdn.AIOrchestrationsApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    status = 'status_example' # str | Filter by orchestration status (optional)
    limit = 20 # int | Maximum number of results (optional) (default to 20)
    cursor = 'cursor_example' # str | Pagination cursor from previous response (optional)

    try:
        # List Durable Orchestrations
        api_response = api_instance.list_orchestrations(organisation, status=status, limit=limit, cursor=cursor)
        print("The response of AIOrchestrationsApi->list_orchestrations:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIOrchestrationsApi->list_orchestrations: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **status** | **str**| Filter by orchestration status | [optional] 
 **limit** | **int**| Maximum number of results | [optional] [default to 20]
 **cursor** | **str**| Pagination cursor from previous response | [optional] 

### Return type

[**ListOrchestrations200Response**](ListOrchestrations200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of orchestrations |  -  |
**403** | Access denied |  -  |
**500** | Failed to list orchestrations |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **pause_orchestration**
> object pause_orchestration(organisation, orchestration_id)

Pause Durable Orchestration

Pause a running orchestration. The current batch will complete, but no new batches will start. Can be resumed later.

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
    api_instance = quantcdn.AIOrchestrationsApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    orchestration_id = 'orchestration_id_example' # str | Orchestration identifier

    try:
        # Pause Durable Orchestration
        api_response = api_instance.pause_orchestration(organisation, orchestration_id)
        print("The response of AIOrchestrationsApi->pause_orchestration:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIOrchestrationsApi->pause_orchestration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **orchestration_id** | **str**| Orchestration identifier | 

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
**200** | Orchestration paused |  -  |
**400** | Orchestration not running |  -  |
**403** | Access denied |  -  |
**404** | Orchestration not found |  -  |
**500** | Failed to pause orchestration |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **resume_orchestration**
> object resume_orchestration(organisation, orchestration_id)

Resume Durable Orchestration

Resume a paused orchestration. Processing continues from where it left off.

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
    api_instance = quantcdn.AIOrchestrationsApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    orchestration_id = 'orchestration_id_example' # str | Orchestration identifier

    try:
        # Resume Durable Orchestration
        api_response = api_instance.resume_orchestration(organisation, orchestration_id)
        print("The response of AIOrchestrationsApi->resume_orchestration:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIOrchestrationsApi->resume_orchestration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **orchestration_id** | **str**| Orchestration identifier | 

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
**200** | Orchestration resumed |  -  |
**400** | Orchestration not paused |  -  |
**403** | Access denied |  -  |
**404** | Orchestration not found |  -  |
**500** | Failed to resume orchestration |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **start_orchestration**
> object start_orchestration(organisation, orchestration_id)

Start Durable Orchestration

Start a pending orchestration. Only works on orchestrations created with `autoStart: false`.

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
    api_instance = quantcdn.AIOrchestrationsApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    orchestration_id = 'orchestration_id_example' # str | Orchestration identifier

    try:
        # Start Durable Orchestration
        api_response = api_instance.start_orchestration(organisation, orchestration_id)
        print("The response of AIOrchestrationsApi->start_orchestration:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIOrchestrationsApi->start_orchestration: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **orchestration_id** | **str**| Orchestration identifier | 

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
**200** | Orchestration started |  -  |
**400** | Orchestration not in pending state |  -  |
**403** | Access denied |  -  |
**404** | Orchestration not found |  -  |
**500** | Failed to start orchestration |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

