# quantcdn.SecretsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_environment_secret**](SecretsApi.md#delete_environment_secret) | **DELETE** /api/v3/organizations/{api_organisation}/applications/{api_application}/environments/{api_environment}/secrets/{api_secret} | Delete a secret
[**list_environment_secrets**](SecretsApi.md#list_environment_secrets) | **GET** /api/v3/organizations/{api_organisation}/applications/{api_application}/environments/{api_environment}/secrets | List the secret names for an environment
[**update_environment_secret**](SecretsApi.md#update_environment_secret) | **PUT** /api/v3/organizations/{api_organisation}/applications/{api_application}/environments/{api_environment}/secrets/{api_secret} | Create or replace a secret


# **delete_environment_secret**
> DeleteEnvironmentSecret200Response delete_environment_secret(api_organisation, api_application, api_environment, api_secret)

Delete a secret

Deletes the secret. The change takes effect on the next redeploy of the environment. A 200 with warnings means the deployed revision still references the secret and cannot start a replacement task until it is redeployed.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.delete_environment_secret200_response import DeleteEnvironmentSecret200Response
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
    api_instance = quantcdn.SecretsApi(api_client)
    api_organisation = 'api_organisation_example' # str | The organisation ID
    api_application = 'api_application_example' # str | The application ID
    api_environment = 'api_environment_example' # str | The environment ID
    api_secret = 'api_secret_example' # str | The secret key

    try:
        # Delete a secret
        api_response = api_instance.delete_environment_secret(api_organisation, api_application, api_environment, api_secret)
        print("The response of SecretsApi->delete_environment_secret:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SecretsApi->delete_environment_secret: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_organisation** | **str**| The organisation ID | 
 **api_application** | **str**| The application ID | 
 **api_environment** | **str**| The environment ID | 
 **api_secret** | **str**| The secret key | 

### Return type

[**DeleteEnvironmentSecret200Response**](DeleteEnvironmentSecret200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | The secret is deleted (or did not exist). It takes effect on the next redeploy. |  -  |
**200** | The secret is deleted, with warnings from Quant Cloud |  -  |
**422** | The key is not valid |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_environment_secrets**
> List[SecretKey] list_environment_secrets(api_organisation, api_application, api_environment)

List the secret names for an environment

Returns the names of the environment's secrets. Secret values are write-only and are never returned.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.secret_key import SecretKey
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
    api_instance = quantcdn.SecretsApi(api_client)
    api_organisation = 'test-org' # str | The organisation ID
    api_application = 'test-app' # str | The application ID
    api_environment = 'test-env' # str | The environment ID

    try:
        # List the secret names for an environment
        api_response = api_instance.list_environment_secrets(api_organisation, api_application, api_environment)
        print("The response of SecretsApi->list_environment_secrets:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SecretsApi->list_environment_secrets: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_organisation** | **str**| The organisation ID | 
 **api_application** | **str**| The application ID | 
 **api_environment** | **str**| The environment ID | 

### Return type

[**List[SecretKey]**](SecretKey.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The secret names |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_environment_secret**
> SecretWriteResult update_environment_secret(api_organisation, api_application, api_environment, api_secret, update_environment_secret_request)

Create or replace a secret

Sets the secret value. The value is write-only: the response returns the key only. The change takes effect on the next redeploy of the environment. A name that already exists as an environment variable is refused with 409.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.secret_write_result import SecretWriteResult
from quantcdn.models.update_environment_secret_request import UpdateEnvironmentSecretRequest
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
    api_instance = quantcdn.SecretsApi(api_client)
    api_organisation = 'test-org' # str | The organisation ID
    api_application = 'test-app' # str | The application ID
    api_environment = 'test-env' # str | The environment ID
    api_secret = 'DB_PASSWORD' # str | The secret key
    update_environment_secret_request = quantcdn.UpdateEnvironmentSecretRequest() # UpdateEnvironmentSecretRequest | 

    try:
        # Create or replace a secret
        api_response = api_instance.update_environment_secret(api_organisation, api_application, api_environment, api_secret, update_environment_secret_request)
        print("The response of SecretsApi->update_environment_secret:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling SecretsApi->update_environment_secret: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **api_organisation** | **str**| The organisation ID | 
 **api_application** | **str**| The application ID | 
 **api_environment** | **str**| The environment ID | 
 **api_secret** | **str**| The secret key | 
 **update_environment_secret_request** | [**UpdateEnvironmentSecretRequest**](UpdateEnvironmentSecretRequest.md)|  | 

### Return type

[**SecretWriteResult**](SecretWriteResult.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The secret is set. It takes effect on the next redeploy. |  -  |
**409** | The name already exists as an environment variable |  -  |
**422** | The key or the value is not valid |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

