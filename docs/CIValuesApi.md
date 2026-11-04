# quantcdn.CIValuesApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_ci_value**](CIValuesApi.md#delete_ci_value) | **DELETE** /api/v3/organizations/{organisation}/ci/values/{name} | Delete a CI secret or variable
[**list_ci_values**](CIValuesApi.md#list_ci_values) | **GET** /api/v3/organizations/{organisation}/ci/values | List the CI secrets and variables
[**put_ci_value**](CIValuesApi.md#put_ci_value) | **PUT** /api/v3/organizations/{organisation}/ci/values/{name} | Create or replace a CI secret or variable


# **delete_ci_value**
> delete_ci_value(organisation, name, repo=repo)

Delete a CI secret or variable

Deletes one value. It answers 204 also when the value does not exist. Needs the cloud:write scope and the delete_applications permission.

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
    api_instance = quantcdn.CIValuesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    name = 'DEPLOY_KEY' # str | The name, such as DEPLOY_KEY
    repo = 'acme/web' # str | Delete the repository's value of this name. Leave out for the organisation's value. Lower-cased by the server. (optional)

    try:
        # Delete a CI secret or variable
        api_instance.delete_ci_value(organisation, name, repo=repo)
    except Exception as e:
        print("Exception when calling CIValuesApi->delete_ci_value: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **name** | **str**| The name, such as DEPLOY_KEY | 
 **repo** | **str**| Delete the repository&#39;s value of this name. Leave out for the organisation&#39;s value. Lower-cased by the server. | [optional] 

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
**204** | Deleted (or did not exist) |  -  |
**404** | The organisation does not have CI runners |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_ci_values**
> ListCiValues200Response list_ci_values(organisation, repo=repo)

List the CI secrets and variables

Returns the organisation's CI values and, without the repo filter, every repository's values. A variable carries its value. A secret never does. Quant gives the values to CI jobs on the organisation's runner pools as environment variables, so a workflow uses `${{ env.NAME }}` instead of `${{ secrets.NAME }}`. Needs the cloud:read scope and the CI runners feature.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_ci_values200_response import ListCiValues200Response
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
    api_instance = quantcdn.CIValuesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    repo = 'acme/web' # str | Only the organisation's values and this repository's values. Lower-cased by the server. (optional)

    try:
        # List the CI secrets and variables
        api_response = api_instance.list_ci_values(organisation, repo=repo)
        print("The response of CIValuesApi->list_ci_values:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CIValuesApi->list_ci_values: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **repo** | **str**| Only the organisation&#39;s values and this repository&#39;s values. Lower-cased by the server. | [optional] 

### Return type

[**ListCiValues200Response**](ListCiValues200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The values |  -  |
**404** | The organisation does not have CI runners |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **put_ci_value**
> CiValueWriteResult put_ci_value(organisation, name, put_ci_value_request)

Create or replace a CI secret or variable

Sets one value for the organisation, or for one repository when repo is set. The value is write-only for a secret: the response never carries it. The backend validates the name, the value and the limits and answers 400 with a message. Needs the cloud:write scope and the delete_applications permission.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.ci_value_write_result import CiValueWriteResult
from quantcdn.models.put_ci_value_request import PutCiValueRequest
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
    api_instance = quantcdn.CIValuesApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    name = 'DEPLOY_KEY' # str | The name, such as DEPLOY_KEY
    put_ci_value_request = quantcdn.PutCiValueRequest() # PutCiValueRequest | 

    try:
        # Create or replace a CI secret or variable
        api_response = api_instance.put_ci_value(organisation, name, put_ci_value_request)
        print("The response of CIValuesApi->put_ci_value:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling CIValuesApi->put_ci_value: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **name** | **str**| The name, such as DEPLOY_KEY | 
 **put_ci_value_request** | [**PutCiValueRequest**](PutCiValueRequest.md)|  | 

### Return type

[**CiValueWriteResult**](CiValueWriteResult.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The value is saved |  -  |
**400** | The name, the value or a limit is not valid |  -  |
**404** | The organisation does not have CI runners |  -  |
**422** | The request body has the wrong shape |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

