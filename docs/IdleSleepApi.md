# quantcdn.IdleSleepApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_idle_sleep**](IdleSleepApi.md#get_idle_sleep) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/idle-sleep | Get Idle Sleep Setting
[**set_idle_sleep**](IdleSleepApi.md#set_idle_sleep) | **PUT** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/idle-sleep | Set Idle Sleep Setting


# **get_idle_sleep**
> IdleSleepResponse get_idle_sleep(organisation, application, environment)

Get Idle Sleep Setting

Retrieves the idle sleep setting and the current sleep state for the environment.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.idle_sleep_response import IdleSleepResponse
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
    api_instance = quantcdn.IdleSleepApi(api_client)
    organisation = 'organisation_example' # str | 
    application = 'application_example' # str | 
    environment = 'environment_example' # str | 

    try:
        # Get Idle Sleep Setting
        api_response = api_instance.get_idle_sleep(organisation, application, environment)
        print("The response of IdleSleepApi->get_idle_sleep:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IdleSleepApi->get_idle_sleep: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **application** | **str**|  | 
 **environment** | **str**|  | 

### Return type

[**IdleSleepResponse**](IdleSleepResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Idle sleep setting and state. |  -  |
**403** | The caller lacks the required permission or token scope. |  -  |
**404** | Organisation, application or environment not found. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **set_idle_sleep**
> IdleSleepResponse set_idle_sleep(organisation, application, environment, set_idle_sleep_request)

Set Idle Sleep Setting

Enable or disable idle sleep. Only Fargate compute sleeps. Disabling a sleeping environment wakes it first; a 202 means it is still waking.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.idle_sleep_response import IdleSleepResponse
from quantcdn.models.set_idle_sleep_request import SetIdleSleepRequest
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
    api_instance = quantcdn.IdleSleepApi(api_client)
    organisation = 'organisation_example' # str | 
    application = 'application_example' # str | 
    environment = 'environment_example' # str | 
    set_idle_sleep_request = quantcdn.SetIdleSleepRequest() # SetIdleSleepRequest | 

    try:
        # Set Idle Sleep Setting
        api_response = api_instance.set_idle_sleep(organisation, application, environment, set_idle_sleep_request)
        print("The response of IdleSleepApi->set_idle_sleep:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling IdleSleepApi->set_idle_sleep: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **application** | **str**|  | 
 **environment** | **str**|  | 
 **set_idle_sleep_request** | [**SetIdleSleepRequest**](SetIdleSleepRequest.md)|  | 

### Return type

[**IdleSleepResponse**](IdleSleepResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Applied. |  -  |
**202** | Applied; environment still waking. |  -  |
**400** | The environment cannot use idle sleep. It runs on EC2 rather than Fargate, it has no web service, or its hostname is too long to route while asleep. |  -  |
**403** | The caller lacks the required permission or token scope. |  -  |
**404** | Organisation, application or environment not found. |  -  |
**422** | Validation failed. idleMinutes must be an integer from 10 to 1440. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

