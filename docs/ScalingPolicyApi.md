# quantcdn.ScalingPolicyApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_scaling_policy**](ScalingPolicyApi.md#delete_scaling_policy) | **DELETE** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/scaling-policies/{policyName} | Delete the scaling policy for an environment
[**get_scaling_policies**](ScalingPolicyApi.md#get_scaling_policies) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/scaling-policies | Get the scaling policies for an environment
[**update_scaling_policy**](ScalingPolicyApi.md#update_scaling_policy) | **PUT** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/scaling-policies | Update the scaling policy for an environment


# **delete_scaling_policy**
> delete_scaling_policy(organisation, application, environment, policy_name)

Delete the scaling policy for an environment

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
    api_instance = quantcdn.ScalingPolicyApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID
    policy_name = 'policy_name_example' # str | The policy name

    try:
        # Delete the scaling policy for an environment
        api_instance.delete_scaling_policy(organisation, application, environment, policy_name)
    except Exception as e:
        print("Exception when calling ScalingPolicyApi->delete_scaling_policy: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **policy_name** | **str**| The policy name | 

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
**204** | The scaling policy for the environment |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_scaling_policies**
> get_scaling_policies(organisation, application, environment)

Get the scaling policies for an environment

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
    api_instance = quantcdn.ScalingPolicyApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID

    try:
        # Get the scaling policies for an environment
        api_instance.get_scaling_policies(organisation, application, environment)
    except Exception as e:
        print("Exception when calling ScalingPolicyApi->get_scaling_policies: %s\n" % e)
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
**200** | The scaling policy for the environment |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_scaling_policy**
> update_scaling_policy(organisation, application, environment, scaling_policy)

Update the scaling policy for an environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.scaling_policy import ScalingPolicy
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
    api_instance = quantcdn.ScalingPolicyApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID
    scaling_policy = quantcdn.ScalingPolicy() # ScalingPolicy | 

    try:
        # Update the scaling policy for an environment
        api_instance.update_scaling_policy(organisation, application, environment, scaling_policy)
    except Exception as e:
        print("Exception when calling ScalingPolicyApi->update_scaling_policy: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **scaling_policy** | [**ScalingPolicy**](ScalingPolicy.md)|  | 

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
**200** | The scaling policy for the environment |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

