# quantcdn.ScalingPolicyApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**delete_scaling_policy**](ScalingPolicyApi.md#delete_scaling_policy) | **DELETE** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/scaling-policies | Delete Scaling Policy
[**list_scaling_policies**](ScalingPolicyApi.md#list_scaling_policies) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/scaling-policies | List Scaling Policies
[**upsert_scaling_policy**](ScalingPolicyApi.md#upsert_scaling_policy) | **PUT** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/scaling-policies | Upsert Scaling Policy


# **delete_scaling_policy**
> delete_scaling_policy(organisation, application, environment, metric=metric, policy_name=policy_name)

Delete Scaling Policy

Deletes a specific scaling policy for the environment. Specify the metric type or policy name to delete a single policy. If neither is provided, all policies will be deleted.

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
    organisation = 'organisation_example' # str | 
    application = 'application_example' # str | 
    environment = 'environment_example' # str | 
    metric = 'metric_example' # str | Optional. Delete by metric type. (optional)
    policy_name = 'policy_name_example' # str | Optional. Delete by exact policy name. (optional)

    try:
        # Delete Scaling Policy
        api_instance.delete_scaling_policy(organisation, application, environment, metric=metric, policy_name=policy_name)
    except Exception as e:
        print("Exception when calling ScalingPolicyApi->delete_scaling_policy: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **application** | **str**|  | 
 **environment** | **str**|  | 
 **metric** | **str**| Optional. Delete by metric type. | [optional] 
 **policy_name** | **str**| Optional. Delete by exact policy name. | [optional] 

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
**204** | Scaling policy deleted successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_scaling_policies**
> ScalingPolicyListResponse list_scaling_policies(organisation, application, environment, metric=metric, policy_name=policy_name)

List Scaling Policies

Retrieves all active target tracking scaling policies for the environment. Returns an array of policies, each with its metric, target value, cooldowns, and resource label (if applicable).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.scaling_policy_list_response import ScalingPolicyListResponse
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
    organisation = 'organisation_example' # str | 
    application = 'application_example' # str | 
    environment = 'environment_example' # str | 
    metric = 'metric_example' # str | Optional. Filter policies by metric type. (optional)
    policy_name = 'policy_name_example' # str | Optional. Filter policies by exact policy name. (optional)

    try:
        # List Scaling Policies
        api_response = api_instance.list_scaling_policies(organisation, application, environment, metric=metric, policy_name=policy_name)
        print("The response of ScalingPolicyApi->list_scaling_policies:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ScalingPolicyApi->list_scaling_policies: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **application** | **str**|  | 
 **environment** | **str**|  | 
 **metric** | **str**| Optional. Filter policies by metric type. | [optional] 
 **policy_name** | **str**| Optional. Filter policies by exact policy name. | [optional] 

### Return type

[**ScalingPolicyListResponse**](ScalingPolicyListResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of scaling policies for the environment. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **upsert_scaling_policy**
> GetScalingPolicyResponse upsert_scaling_policy(organisation, application, environment, set_scaling_policy_request, policy_name=policy_name)

Upsert Scaling Policy

Creates or updates a target tracking scaling policy for the environment. Specify the metric type and target value. If a policy with the same metric or name exists, it will be updated. Optionally, provide a custom policy name via query.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_scaling_policy_response import GetScalingPolicyResponse
from quantcdn.models.set_scaling_policy_request import SetScalingPolicyRequest
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
    organisation = 'organisation_example' # str | 
    application = 'application_example' # str | 
    environment = 'environment_example' # str | 
    set_scaling_policy_request = quantcdn.SetScalingPolicyRequest() # SetScalingPolicyRequest | 
    policy_name = 'policy_name_example' # str | Optional. Specify a custom policy name to upsert. (optional)

    try:
        # Upsert Scaling Policy
        api_response = api_instance.upsert_scaling_policy(organisation, application, environment, set_scaling_policy_request, policy_name=policy_name)
        print("The response of ScalingPolicyApi->upsert_scaling_policy:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ScalingPolicyApi->upsert_scaling_policy: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**|  | 
 **application** | **str**|  | 
 **environment** | **str**|  | 
 **set_scaling_policy_request** | [**SetScalingPolicyRequest**](SetScalingPolicyRequest.md)|  | 
 **policy_name** | **str**| Optional. Specify a custom policy name to upsert. | [optional] 

### Return type

[**GetScalingPolicyResponse**](GetScalingPolicyResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Scaling policy created or updated successfully. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

