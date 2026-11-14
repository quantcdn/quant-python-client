# quantcdn.AIAutoModeApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_auto_mode**](AIAutoModeApi.md#delete_auto_mode) | **DELETE** /api/v3/organizations/{organisation}/ai/auto-mode | Remove the auto mode setting for an organisation
[**get_auto_mode**](AIAutoModeApi.md#get_auto_mode) | **GET** /api/v3/organizations/{organisation}/ai/auto-mode | Get the auto mode setting for an organisation
[**update_auto_mode**](AIAutoModeApi.md#update_auto_mode) | **PUT** /api/v3/organizations/{organisation}/ai/auto-mode | Save the auto mode setting for an organisation


# **delete_auto_mode**
> DeleteAutoMode200Response delete_auto_mode(organisation)

Remove the auto mode setting for an organisation

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.delete_auto_mode200_response import DeleteAutoMode200Response
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
    api_instance = quantcdn.AIAutoModeApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # Remove the auto mode setting for an organisation
        api_response = api_instance.delete_auto_mode(organisation)
        print("The response of AIAutoModeApi->delete_auto_mode:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAutoModeApi->delete_auto_mode: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**DeleteAutoMode200Response**](DeleteAutoMode200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The setting is removed |  -  |
**409** | Another change to the setting happened at the same time. Read the setting again, then retry. |  -  |
**502** | The AI service is not available |  -  |
**503** | The AI service cannot remove the setting now (the audit ledger is not available) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_auto_mode**
> GetAutoMode200Response get_auto_mode(organisation)

Get the auto mode setting for an organisation

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_auto_mode200_response import GetAutoMode200Response
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
    api_instance = quantcdn.AIAutoModeApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # Get the auto mode setting for an organisation
        api_response = api_instance.get_auto_mode(organisation)
        print("The response of AIAutoModeApi->get_auto_mode:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAutoModeApi->get_auto_mode: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**GetAutoMode200Response**](GetAutoMode200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The auto mode setting and the eligibility report |  -  |
**502** | The AI service is not available |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_auto_mode**
> UpdateAutoMode200Response update_auto_mode(organisation, ai_auto_mode_input)

Save the auto mode setting for an organisation

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.ai_auto_mode_input import AIAutoModeInput
from quantcdn.models.update_auto_mode200_response import UpdateAutoMode200Response
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
    api_instance = quantcdn.AIAutoModeApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    ai_auto_mode_input = quantcdn.AIAutoModeInput() # AIAutoModeInput | 

    try:
        # Save the auto mode setting for an organisation
        api_response = api_instance.update_auto_mode(organisation, ai_auto_mode_input)
        print("The response of AIAutoModeApi->update_auto_mode:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAutoModeApi->update_auto_mode: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **ai_auto_mode_input** | [**AIAutoModeInput**](AIAutoModeInput.md)|  | 

### Return type

[**UpdateAutoMode200Response**](UpdateAutoMode200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The saved setting |  -  |
**400** | The setting is refused. When the models are not usable, eligible carries the eligibility report; it is null for a body shape error or an unknown organisation portal. |  -  |
**409** | Conflict: the group revision is stale (another change was saved after the last read), the governance settings changed between the read and the write, or the organisation governance settings are not saved yet (error: \&quot;Save the organisation governance settings first\&quot;). Read the setting again, then retry. |  -  |
**422** | Validation error |  -  |
**502** | The AI service is not available |  -  |
**503** | The AI service cannot save the setting now |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

