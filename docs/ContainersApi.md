# quantcdn.ContainersApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**list_containers**](ContainersApi.md#list_containers) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/containers | Get the containers in an environment
[**update_container**](ContainersApi.md#update_container) | **PUT** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/containers/{container} | Update a container in an environment


# **list_containers**
> list_containers(organisation, application, environment)

Get the containers in an environment

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
    api_instance = quantcdn.ContainersApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID

    try:
        # Get the containers in an environment
        api_instance.list_containers(organisation, application, environment)
    except Exception as e:
        print("Exception when calling ContainersApi->list_containers: %s\n" % e)
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
**200** | The containers in the environment |  -  |
**404** | The environment not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_container**
> Container update_container(organisation, application, environment, container, container2)

Update a container in an environment

Updates one container in the environment's compose definition and redeploys the environment. The fields in the request body replace the same fields of the container. Fields that the request body omits keep their current values. Other containers and the task-level settings do not change. To clear a field, send it as null. The container name in the body must match the name in the path: a container cannot be renamed. Container updates to one environment run one at a time. A compose change made at the same moment through another endpoint can still overwrite this update.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.container import Container
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
    api_instance = quantcdn.ContainersApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID
    container = 'app' # str | The container name
    container2 = quantcdn.Container() # Container | 

    try:
        # Update a container in an environment
        api_response = api_instance.update_container(organisation, application, environment, container, container2)
        print("The response of ContainersApi->update_container:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ContainersApi->update_container: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **container** | **str**| The container name | 
 **container2** | [**Container**](Container.md)|  | 

### Return type

[**Container**](Container.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The updated container. The environment redeploys in the background. |  -  |
**400** | Quant Cloud refused the updated definition |  -  |
**403** | Permission or token scope missing |  -  |
**404** | The environment has no container with this name |  -  |
**409** | Another container update for this environment is in progress |  -  |
**422** | Invalid container definition, or the body name does not match the path name |  -  |
**502** | Quant Cloud did not accept the request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

