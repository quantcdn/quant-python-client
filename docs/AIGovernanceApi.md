# quantcdn.AIGovernanceApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_governance_config**](AIGovernanceApi.md#get_governance_config) | **GET** /api/v3/organizations/{organisation}/ai/governance | Get AI governance configuration for an organisation
[**get_governance_spend**](AIGovernanceApi.md#get_governance_spend) | **GET** /api/v3/organizations/{organisation}/ai/governance/spend | Get AI spend summary for an organisation
[**update_governance_config**](AIGovernanceApi.md#update_governance_config) | **PUT** /api/v3/organizations/{organisation}/ai/governance | Update AI governance configuration for an organisation


# **get_governance_config**
> GetGovernanceConfig200Response get_governance_config(organisation)

Get AI governance configuration for an organisation

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_governance_config200_response import GetGovernanceConfig200Response
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
    api_instance = quantcdn.AIGovernanceApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # Get AI governance configuration for an organisation
        api_response = api_instance.get_governance_config(organisation)
        print("The response of AIGovernanceApi->get_governance_config:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIGovernanceApi->get_governance_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**GetGovernanceConfig200Response**](GetGovernanceConfig200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | AI governance configuration |  -  |
**500** | Failed to retrieve governance configuration |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_governance_spend**
> GetGovernanceSpend200Response get_governance_spend(organisation)

Get AI spend summary for an organisation

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_governance_spend200_response import GetGovernanceSpend200Response
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
    api_instance = quantcdn.AIGovernanceApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # Get AI spend summary for an organisation
        api_response = api_instance.get_governance_spend(organisation)
        print("The response of AIGovernanceApi->get_governance_spend:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIGovernanceApi->get_governance_spend: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**GetGovernanceSpend200Response**](GetGovernanceSpend200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | AI spend summary |  -  |
**500** | Failed to retrieve spend summary |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_governance_config**
> UpdateGovernanceConfig200Response update_governance_config(organisation, update_governance_config_request)

Update AI governance configuration for an organisation

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.update_governance_config200_response import UpdateGovernanceConfig200Response
from quantcdn.models.update_governance_config_request import UpdateGovernanceConfigRequest
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
    api_instance = quantcdn.AIGovernanceApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    update_governance_config_request = quantcdn.UpdateGovernanceConfigRequest() # UpdateGovernanceConfigRequest | 

    try:
        # Update AI governance configuration for an organisation
        api_response = api_instance.update_governance_config(organisation, update_governance_config_request)
        print("The response of AIGovernanceApi->update_governance_config:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIGovernanceApi->update_governance_config: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **update_governance_config_request** | [**UpdateGovernanceConfigRequest**](UpdateGovernanceConfigRequest.md)|  | 

### Return type

[**UpdateGovernanceConfig200Response**](UpdateGovernanceConfig200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Governance configuration updated successfully |  -  |
**422** | Validation error |  -  |
**500** | Failed to update governance configuration |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

