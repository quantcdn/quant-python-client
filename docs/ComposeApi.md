# quantcdn.ComposeApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**get_environment_compose**](ComposeApi.md#get_environment_compose) | **GET** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/compose | Get the compose file for an environment
[**patch_environment_compose**](ComposeApi.md#patch_environment_compose) | **PATCH** /api/v3/organizations/{organisation}/applications/{application}/environments/{environment}/compose | Partially Update Environment Compose Definition
[**validate_compose**](ComposeApi.md#validate_compose) | **POST** /api/v3/organizations/{organisation}/compose/validate | Validate a compose file


# **get_environment_compose**
> Compose get_environment_compose(organisation, application, environment)

Get the compose file for an environment

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.compose import Compose
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
    api_instance = quantcdn.ComposeApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID

    try:
        # Get the compose file for an environment
        api_response = api_instance.get_environment_compose(organisation, application, environment)
        print("The response of ComposeApi->get_environment_compose:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComposeApi->get_environment_compose: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 

### Return type

[**Compose**](Compose.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The compose file |  -  |
**404** | The compose file not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **patch_environment_compose**
> PatchEnvironmentCompose202Response patch_environment_compose(organisation, application, environment, patch_environment_compose_request)

Partially Update Environment Compose Definition

Partially updates top-level fields of the environment's compose definition, such as architecture, task-level CPU/Memory, or min/max scaling capacity. Only fields included in the request body are modified. The 'containers' array, if provided, REPLACES the existing containers array; if omitted, the existing containers are NOT modified by this PATCH operation. (For modifying individual containers, use PATCH /containers/{containerName}). This triggers a validation, registers a new task definition, and updates the service.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.patch_environment_compose202_response import PatchEnvironmentCompose202Response
from quantcdn.models.patch_environment_compose_request import PatchEnvironmentComposeRequest
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
    api_instance = quantcdn.ComposeApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    application = 'test-app' # str | The application ID
    environment = 'test-env' # str | The environment ID
    patch_environment_compose_request = quantcdn.PatchEnvironmentComposeRequest() # PatchEnvironmentComposeRequest | Partial compose definition updates. All fields are optional.

    try:
        # Partially Update Environment Compose Definition
        api_response = api_instance.patch_environment_compose(organisation, application, environment, patch_environment_compose_request)
        print("The response of ComposeApi->patch_environment_compose:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComposeApi->patch_environment_compose: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **application** | **str**| The application ID | 
 **environment** | **str**| The environment ID | 
 **patch_environment_compose_request** | [**PatchEnvironmentComposeRequest**](PatchEnvironmentComposeRequest.md)| Partial compose definition updates. All fields are optional. | 

### Return type

[**PatchEnvironmentCompose202Response**](PatchEnvironmentCompose202Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Request accepted, compose definition partial update is processing. Returns the full updated compose definition. |  -  |
**400** | Invalid compose definition or validation failed. |  -  |
**404** | Application or environment not found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **validate_compose**
> ValidateCompose200Response validate_compose(organisation, validate_compose_request, image_suffix=image_suffix)

Validate a compose file

Accepts a docker-compose.yml file content, translates it into the internal compose definition format, and validates it. Quant Cloud provides comprehensive support for standard Docker Compose features including commands, entrypoints, health checks, dependencies, volume mounts, resource limits, and more. For detailed documentation on supported features and examples, see: https://docs.quantcdn.io/introduction-to-quant-cloud/importing-docker-compose/. Supports image tag suffixing via the imageSuffix query parameter or by sending a JSON wrapper with yamlContent and imageSuffix fields. When provided, internal image tags are transformed to {containerName}-{suffix} format (e.g., 'nginx-feature-xyz').

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.validate_compose200_response import ValidateCompose200Response
from quantcdn.models.validate_compose_request import ValidateComposeRequest
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
    api_instance = quantcdn.ComposeApi(api_client)
    organisation = 'test-org' # str | The organisation ID
    validate_compose_request = quantcdn.ValidateComposeRequest() # ValidateComposeRequest | The docker-compose.yml file content. Can be sent as raw YAML string or as a JSON wrapper containing both yamlContent (string) and imageSuffix (string) fields. Query parameter imageSuffix takes precedence if both are provided.
    image_suffix = 'pr-456' # str | Optional. Image tag suffix to apply during translation. Transforms internal image tags to consistent '{containerName}-{suffix}' format (e.g., 'nginx-pr-456'). External images are left unchanged. Useful for feature branch deployments. (optional)

    try:
        # Validate a compose file
        api_response = api_instance.validate_compose(organisation, validate_compose_request, image_suffix=image_suffix)
        print("The response of ComposeApi->validate_compose:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling ComposeApi->validate_compose: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **validate_compose_request** | [**ValidateComposeRequest**](ValidateComposeRequest.md)| The docker-compose.yml file content. Can be sent as raw YAML string or as a JSON wrapper containing both yamlContent (string) and imageSuffix (string) fields. Query parameter imageSuffix takes precedence if both are provided. | 
 **image_suffix** | **str**| Optional. Image tag suffix to apply during translation. Transforms internal image tags to consistent &#39;{containerName}-{suffix}&#39; format (e.g., &#39;nginx-pr-456&#39;). External images are left unchanged. Useful for feature branch deployments. | [optional] 

### Return type

[**ValidateCompose200Response**](ValidateCompose200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Validation successful. Body contains the translated compose definition and any warnings. |  -  |
**422** | Invalid YAML input or validation failed |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

