# quantcdn.AIFilterPoliciesApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_filter_policy**](AIFilterPoliciesApi.md#create_filter_policy) | **POST** /api/v3/organizations/{organisation}/ai/filter-policies | Create an AI filter policy for an organisation
[**delete_filter_policy**](AIFilterPoliciesApi.md#delete_filter_policy) | **DELETE** /api/v3/organizations/{organisation}/ai/filter-policies/{policyId} | Delete a specific AI filter policy
[**disable_filter_policy**](AIFilterPoliciesApi.md#disable_filter_policy) | **PUT** /api/v3/organizations/{organisation}/ai/filter-policies/{policyId}/disable | Disable a specific AI filter policy
[**enable_filter_policy**](AIFilterPoliciesApi.md#enable_filter_policy) | **PUT** /api/v3/organizations/{organisation}/ai/filter-policies/{policyId}/enable | Enable a specific AI filter policy
[**get_filter_policy**](AIFilterPoliciesApi.md#get_filter_policy) | **GET** /api/v3/organizations/{organisation}/ai/filter-policies/{policyId} | Get a specific AI filter policy
[**list_filter_policies**](AIFilterPoliciesApi.md#list_filter_policies) | **GET** /api/v3/organizations/{organisation}/ai/filter-policies | List AI filter policies for an organisation
[**update_filter_policy**](AIFilterPoliciesApi.md#update_filter_policy) | **PUT** /api/v3/organizations/{organisation}/ai/filter-policies/{policyId} | Update a specific AI filter policy


# **create_filter_policy**
> object create_filter_policy(organisation, create_filter_policy_request)

Create an AI filter policy for an organisation

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_filter_policy_request import CreateFilterPolicyRequest
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
    api_instance = quantcdn.AIFilterPoliciesApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    create_filter_policy_request = quantcdn.CreateFilterPolicyRequest() # CreateFilterPolicyRequest | 

    try:
        # Create an AI filter policy for an organisation
        api_response = api_instance.create_filter_policy(organisation, create_filter_policy_request)
        print("The response of AIFilterPoliciesApi->create_filter_policy:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIFilterPoliciesApi->create_filter_policy: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **create_filter_policy_request** | [**CreateFilterPolicyRequest**](CreateFilterPolicyRequest.md)|  | 

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
**201** | Filter policy created successfully |  -  |
**422** | Validation error |  -  |
**500** | Failed to create filter policy |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_filter_policy**
> object delete_filter_policy(organisation, policy_id)

Delete a specific AI filter policy

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
    api_instance = quantcdn.AIFilterPoliciesApi(api_client)
    organisation = 'organisation_example' # str | 
    policy_id = 'policy_id_example' # str | 

    try:
        # Delete a specific AI filter policy
        api_response = api_instance.delete_filter_policy(organisation, policy_id)
        print("The response of AIFilterPoliciesApi->delete_filter_policy:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIFilterPoliciesApi->delete_filter_policy: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **policy_id** | **str**|  | 

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
**200** | Filter policy deleted successfully |  -  |
**500** | Failed to delete filter policy |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **disable_filter_policy**
> object disable_filter_policy(organisation, policy_id)

Disable a specific AI filter policy

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
    api_instance = quantcdn.AIFilterPoliciesApi(api_client)
    organisation = 'organisation_example' # str | 
    policy_id = 'policy_id_example' # str | 

    try:
        # Disable a specific AI filter policy
        api_response = api_instance.disable_filter_policy(organisation, policy_id)
        print("The response of AIFilterPoliciesApi->disable_filter_policy:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIFilterPoliciesApi->disable_filter_policy: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **policy_id** | **str**|  | 

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
**200** | Filter policy disabled successfully |  -  |
**500** | Failed to disable filter policy |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **enable_filter_policy**
> object enable_filter_policy(organisation, policy_id)

Enable a specific AI filter policy

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
    api_instance = quantcdn.AIFilterPoliciesApi(api_client)
    organisation = 'organisation_example' # str | 
    policy_id = 'policy_id_example' # str | 

    try:
        # Enable a specific AI filter policy
        api_response = api_instance.enable_filter_policy(organisation, policy_id)
        print("The response of AIFilterPoliciesApi->enable_filter_policy:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIFilterPoliciesApi->enable_filter_policy: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **policy_id** | **str**|  | 

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
**200** | Filter policy enabled successfully |  -  |
**500** | Failed to enable filter policy |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_filter_policy**
> object get_filter_policy(organisation, policy_id)

Get a specific AI filter policy

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
    api_instance = quantcdn.AIFilterPoliciesApi(api_client)
    organisation = 'organisation_example' # str | 
    policy_id = 'policy_id_example' # str | 

    try:
        # Get a specific AI filter policy
        api_response = api_instance.get_filter_policy(organisation, policy_id)
        print("The response of AIFilterPoliciesApi->get_filter_policy:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIFilterPoliciesApi->get_filter_policy: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **policy_id** | **str**|  | 

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
**200** | Filter policy details |  -  |
**404** | Filter policy not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_filter_policies**
> object list_filter_policies(organisation)

List AI filter policies for an organisation

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
    api_instance = quantcdn.AIFilterPoliciesApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # List AI filter policies for an organisation
        api_response = api_instance.list_filter_policies(organisation)
        print("The response of AIFilterPoliciesApi->list_filter_policies:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIFilterPoliciesApi->list_filter_policies: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

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
**200** | List of filter policies |  -  |
**500** | Failed to retrieve filter policies |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_filter_policy**
> object update_filter_policy(organisation, policy_id, update_filter_policy_request)

Update a specific AI filter policy

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.update_filter_policy_request import UpdateFilterPolicyRequest
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
    api_instance = quantcdn.AIFilterPoliciesApi(api_client)
    organisation = 'organisation_example' # str | 
    policy_id = 'policy_id_example' # str | 
    update_filter_policy_request = quantcdn.UpdateFilterPolicyRequest() # UpdateFilterPolicyRequest | 

    try:
        # Update a specific AI filter policy
        api_response = api_instance.update_filter_policy(organisation, policy_id, update_filter_policy_request)
        print("The response of AIFilterPoliciesApi->update_filter_policy:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIFilterPoliciesApi->update_filter_policy: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **policy_id** | **str**|  | 
 **update_filter_policy_request** | [**UpdateFilterPolicyRequest**](UpdateFilterPolicyRequest.md)|  | 

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
**200** | Filter policy updated successfully |  -  |
**422** | Validation error |  -  |
**500** | Failed to update filter policy |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

