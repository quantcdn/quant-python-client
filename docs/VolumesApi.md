# quantcdn.VolumesApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_volume**](VolumesApi.md#create_volume) | **POST** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/volumes | Create a new volume
[**delete_volume**](VolumesApi.md#delete_volume) | **DELETE** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/volumes/{volume} | Delete a volume
[**get_volume**](VolumesApi.md#get_volume) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/volumes/{volume} | Get a volume
[**list_volumes**](VolumesApi.md#list_volumes) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/volumes | Get all volumes for an environment


# **create_volume**
> Volume create_volume(organisation, application, environment, create_volume_request)

Create a new volume

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_volume_request import CreateVolumeRequest
from quantcdn.models.volume import Volume
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
    api_instance = quantcdn.VolumesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID
    create_volume_request = quantcdn.CreateVolumeRequest() # CreateVolumeRequest | 

    try:
        # Create a new volume
        api_response = api_instance.create_volume(organisation, application, environment, create_volume_request)
        print("The response of VolumesApi->create_volume:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VolumesApi->create_volume: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **create_volume_request** | [**CreateVolumeRequest**](CreateVolumeRequest.md)|  | 

### Return type

[**Volume**](Volume.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | The volume created |  -  |
**404** | The environment not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_volume**
> delete_volume(organisation, application, environment, volume)

Delete a volume

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
    api_instance = quantcdn.VolumesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID
    volume = 'volume_example' # str | The volume ID

    try:
        # Delete a volume
        api_instance.delete_volume(organisation, application, environment, volume)
    except Exception as e:
        print("Exception when calling VolumesApi->delete_volume: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **volume** | **str**| The volume ID | 

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
**204** | The volume deleted |  -  |
**404** | The environment not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_volume**
> Volume get_volume(organisation, application, environment, volume)

Get a volume

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.volume import Volume
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
    api_instance = quantcdn.VolumesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID
    volume = 'volume_example' # str | The volume ID

    try:
        # Get a volume
        api_response = api_instance.get_volume(organisation, application, environment, volume)
        print("The response of VolumesApi->get_volume:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VolumesApi->get_volume: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **volume** | **str**| The volume ID | 

### Return type

[**Volume**](Volume.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The volume |  -  |
**404** | The environment not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_volumes**
> Volume list_volumes(organisation, application, environment)

Get all volumes for an environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.volume import Volume
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
    api_instance = quantcdn.VolumesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID

    try:
        # Get all volumes for an environment
        api_response = api_instance.list_volumes(organisation, application, environment)
        print("The response of VolumesApi->list_volumes:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling VolumesApi->list_volumes: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 

### Return type

[**Volume**](Volume.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The volumes |  -  |
**404** | The environment not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

