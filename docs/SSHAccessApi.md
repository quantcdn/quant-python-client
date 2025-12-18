# quantcdn.SSHAccessApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_ssh_access_credentials**](SSHAccessApi.md#get_ssh_access_credentials) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/ssh-access | Get SSH access credentials for an environment


# **get_ssh_access_credentials**
> GetSshAccessCredentials200Response get_ssh_access_credentials(organisation, application, environment)

Get SSH access credentials for an environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_ssh_access_credentials200_response import GetSshAccessCredentials200Response
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
    api_instance = quantcdn.SSHAccessApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    application = 'application_example' # str | The application name
    environment = 'environment_example' # str | The environment name

    try:
        # Get SSH access credentials for an environment
        api_response = api_instance.get_ssh_access_credentials(organisation, application, environment)
        print("The response of SSHAccessApi->get_ssh_access_credentials:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SSHAccessApi->get_ssh_access_credentials: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **application** | **str**| The application name | 
 **environment** | **str**| The environment name | 

### Return type

[**GetSshAccessCredentials200Response**](GetSshAccessCredentials200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | SSH access credentials |  -  |
**403** | Insufficient permissions |  -  |
**404** | Environment not found |  -  |
**500** | Failed to generate SSH access credentials |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

