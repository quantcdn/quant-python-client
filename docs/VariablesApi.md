# quantcdn.VariablesApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**bulk_set_environment_variables**](VariablesApi.md#bulk_set_environment_variables) | **PUT** /api/v3/organizations/{api_organisation}/applications/{api_application}/environments/{api_environment}/variables | Bulk set/replace environment variables
[**delete_environment_variable**](VariablesApi.md#delete_environment_variable) | **DELETE** /api/v3/organizations/{api_organisation}/applications/{api_application}/environments/{api_environment}/variables/{api_variable} | Delete a variable
[**list_environment_variables**](VariablesApi.md#list_environment_variables) | **GET** /api/v3/organizations/{api_organisation}/applications/{api_application}/environments/{api_environment}/variables | Get all variables for an environment
[**update_environment_variable**](VariablesApi.md#update_environment_variable) | **PUT** /api/v3/organizations/{api_organisation}/applications/{api_application}/environments/{api_environment}/variables/{api_variable} | Update a variable


# **bulk_set_environment_variables**
> bulk_set_environment_variables(api_organisation, api_application, api_environment, bulk_set_environment_variables_request)

Bulk set/replace environment variables

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.bulk_set_environment_variables_request import BulkSetEnvironmentVariablesRequest
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
    api_instance = quantcdn.VariablesApi(api_client)
    api_organisation = 'test-org' # str | The organisation ID
    api_application = 'test-app' # str | The application ID
    api_environment = 'test-env' # str | The environment ID
    bulk_set_environment_variables_request = quantcdn.BulkSetEnvironmentVariablesRequest() # BulkSetEnvironmentVariablesRequest | 

    try:
        # Bulk set/replace environment variables
        api_instance.bulk_set_environment_variables(api_organisation, api_application, api_environment, bulk_set_environment_variables_request)
    except Exception as e:
        print("Exception when calling VariablesApi->bulk_set_environment_variables: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_organisation** | **str**| The organisation ID | 
 **api_application** | **str**| The application ID | 
 **api_environment** | **str**| The environment ID | 
 **bulk_set_environment_variables_request** | [**BulkSetEnvironmentVariablesRequest**](BulkSetEnvironmentVariablesRequest.md)|  | 

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
**200** | Environment variables set/replaced successfully |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_environment_variable**
> delete_environment_variable(api_organisation, api_application, api_environment, api_variable)

Delete a variable

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
    api_instance = quantcdn.VariablesApi(api_client)
    api_organisation = 'api_organisation_example' # str | The organisation ID
    api_application = 'api_application_example' # str | The application ID
    api_environment = 'api_environment_example' # str | The environment ID
    api_variable = 'api_variable_example' # str | The variable key

    try:
        # Delete a variable
        api_instance.delete_environment_variable(api_organisation, api_application, api_environment, api_variable)
    except Exception as e:
        print("Exception when calling VariablesApi->delete_environment_variable: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_organisation** | **str**| The organisation ID | 
 **api_application** | **str**| The application ID | 
 **api_environment** | **str**| The environment ID | 
 **api_variable** | **str**| The variable key | 

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
**204** | The variable deleted |  -  |
**404** | The variable not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_environment_variables**
> list_environment_variables(api_organisation, api_application, api_environment)

Get all variables for an environment

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
    api_instance = quantcdn.VariablesApi(api_client)
    api_organisation = 'test-org' # str | The organisation ID
    api_application = 'test-app' # str | The application ID
    api_environment = 'test-env' # str | The environment ID

    try:
        # Get all variables for an environment
        api_instance.list_environment_variables(api_organisation, api_application, api_environment)
    except Exception as e:
        print("Exception when calling VariablesApi->list_environment_variables: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_organisation** | **str**| The organisation ID | 
 **api_application** | **str**| The application ID | 
 **api_environment** | **str**| The environment ID | 

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
**200** | A list of variables |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_environment_variable**
> update_environment_variable(api_organisation, api_application, api_environment, api_variable, update_environment_variable_request)

Update a variable

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.update_environment_variable_request import UpdateEnvironmentVariableRequest
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
    api_instance = quantcdn.VariablesApi(api_client)
    api_organisation = 'test-org' # str | The organisation ID
    api_application = 'test-app' # str | The application ID
    api_environment = 'test-env' # str | The environment ID
    api_variable = 'api_variable_example' # str | The variable key
    update_environment_variable_request = quantcdn.UpdateEnvironmentVariableRequest() # UpdateEnvironmentVariableRequest | 

    try:
        # Update a variable
        api_instance.update_environment_variable(api_organisation, api_application, api_environment, api_variable, update_environment_variable_request)
    except Exception as e:
        print("Exception when calling VariablesApi->update_environment_variable: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_organisation** | **str**| The organisation ID | 
 **api_application** | **str**| The application ID | 
 **api_environment** | **str**| The environment ID | 
 **api_variable** | **str**| The variable key | 
 **update_environment_variable_request** | [**UpdateEnvironmentVariableRequest**](UpdateEnvironmentVariableRequest.md)|  | 

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
**200** | The variable updated |  -  |
**404** | The variable not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

