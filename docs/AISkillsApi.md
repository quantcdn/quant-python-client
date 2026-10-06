# quantcdn.AISkillsApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_skill**](AISkillsApi.md#create_skill) | **POST** /api/v3/organizations/{organisation}/ai/skills | Create Inline Skill
[**delete_skill**](AISkillsApi.md#delete_skill) | **DELETE** /api/v3/organizations/{organisation}/ai/skills/{skillId} | Delete Skill
[**delete_skill_collection**](AISkillsApi.md#delete_skill_collection) | **DELETE** /api/v3/organizations/{organisation}/ai/skills/collections/{namespace} | Delete Skill Collection
[**get_skill**](AISkillsApi.md#get_skill) | **GET** /api/v3/organizations/{organisation}/ai/skills/{skillId} | Get Skill Details
[**import_skill**](AISkillsApi.md#import_skill) | **POST** /api/v3/organizations/{organisation}/ai/skills/import | Import Skill from External Source
[**import_skill_collection**](AISkillsApi.md#import_skill_collection) | **POST** /api/v3/organizations/{organisation}/ai/skills/import-collection | Import Skill Collection from GitHub
[**list_skill_collections**](AISkillsApi.md#list_skill_collections) | **GET** /api/v3/organizations/{organisation}/ai/skills/collections | List Skill Collections
[**list_skills**](AISkillsApi.md#list_skills) | **GET** /api/v3/organizations/{organisation}/ai/skills | List Organization&#39;s Skills
[**sync_skill**](AISkillsApi.md#sync_skill) | **POST** /api/v3/organizations/{organisation}/ai/skills/{skillId}/sync | Sync Skill from Source
[**sync_skill_collection**](AISkillsApi.md#sync_skill_collection) | **POST** /api/v3/organizations/{organisation}/ai/skills/collections/{namespace}/sync | Sync Skill Collection
[**update_skill**](AISkillsApi.md#update_skill) | **PUT** /api/v3/organizations/{organisation}/ai/skills/{skillId} | Update Skill


# **create_skill**
> CreateSkill201Response create_skill(organisation, create_skill_request)

Create Inline Skill

Creates a new skill with inline content. Use this for custom skills
     * that are defined directly in your organization.
     *
     * **Trigger Conditions:**
     * - Natural language description of when to use the skill
     * - Used by AI to determine when to suggest or apply the skill
     * - Example: 'When the user asks about code review or security analysis'

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_skill201_response import CreateSkill201Response
from quantcdn.models.create_skill_request import CreateSkillRequest
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
    api_instance = quantcdn.AISkillsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    create_skill_request = quantcdn.CreateSkillRequest() # CreateSkillRequest | 

    try:
        # Create Inline Skill
        api_response = api_instance.create_skill(organisation, create_skill_request)
        print("The response of AISkillsApi->create_skill:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISkillsApi->create_skill: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **create_skill_request** | [**CreateSkillRequest**](CreateSkillRequest.md)|  | 

### Return type

[**CreateSkill201Response**](CreateSkill201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Skill created successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**500** | Failed to create skill |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_skill**
> DeleteSkill200Response delete_skill(organisation, skill_id)

Delete Skill

Permanently deletes a skill. This will also remove it from any agents that have it assigned.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.delete_skill200_response import DeleteSkill200Response
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
    api_instance = quantcdn.AISkillsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    skill_id = 'skill_id_example' # str | The skill ID

    try:
        # Delete Skill
        api_response = api_instance.delete_skill(organisation, skill_id)
        print("The response of AISkillsApi->delete_skill:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISkillsApi->delete_skill: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **skill_id** | **str**| The skill ID | 

### Return type

[**DeleteSkill200Response**](DeleteSkill200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Skill deleted successfully |  -  |
**403** | Access denied |  -  |
**404** | Skill not found |  -  |
**500** | Failed to delete skill |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_skill_collection**
> DeleteSkillCollection200Response delete_skill_collection(organisation, namespace)

Delete Skill Collection

Permanently deletes all skills in the specified namespace.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.delete_skill_collection200_response import DeleteSkillCollection200Response
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
    api_instance = quantcdn.AISkillsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    namespace = 'namespace_example' # str | Collection namespace

    try:
        # Delete Skill Collection
        api_response = api_instance.delete_skill_collection(organisation, namespace)
        print("The response of AISkillsApi->delete_skill_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISkillsApi->delete_skill_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **namespace** | **str**| Collection namespace | 

### Return type

[**DeleteSkillCollection200Response**](DeleteSkillCollection200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Collection deleted successfully |  -  |
**403** | Access denied |  -  |
**404** | Collection not found |  -  |
**500** | Failed to delete collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_skill**
> GetSkill200Response get_skill(organisation, skill_id)

Get Skill Details

Retrieves full details of a skill including its content, source information, and metadata.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_skill200_response import GetSkill200Response
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
    api_instance = quantcdn.AISkillsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    skill_id = 'skill_id_example' # str | The skill ID

    try:
        # Get Skill Details
        api_response = api_instance.get_skill(organisation, skill_id)
        print("The response of AISkillsApi->get_skill:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISkillsApi->get_skill: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **skill_id** | **str**| The skill ID | 

### Return type

[**GetSkill200Response**](GetSkill200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Skill details retrieved successfully |  -  |
**403** | Access denied |  -  |
**404** | Skill not found |  -  |
**500** | Failed to retrieve skill |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **import_skill**
> ImportSkill201Response import_skill(organisation, import_skill_request)

Import Skill from External Source

Imports a skill from an external source like skills.sh registry or GitHub repository.
     *
     * **Supported Sources:**
     * - `skills.sh`: Import from the skills.sh community registry
     * - `github`: Import from a GitHub repository (public or private)
     *
     * **Version Control:**
     * - Skills can be pinned to specific versions
     * - Use the sync endpoint to update to latest version

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.import_skill201_response import ImportSkill201Response
from quantcdn.models.import_skill_request import ImportSkillRequest
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
    api_instance = quantcdn.AISkillsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    import_skill_request = quantcdn.ImportSkillRequest() # ImportSkillRequest | 

    try:
        # Import Skill from External Source
        api_response = api_instance.import_skill(organisation, import_skill_request)
        print("The response of AISkillsApi->import_skill:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISkillsApi->import_skill: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **import_skill_request** | [**ImportSkillRequest**](ImportSkillRequest.md)|  | 

### Return type

[**ImportSkill201Response**](ImportSkill201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Skill imported successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**502** | Failed to fetch skill from source |  -  |
**500** | Failed to import skill |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **import_skill_collection**
> ImportSkillCollection201Response import_skill_collection(organisation, import_skill_collection_request)

Import Skill Collection from GitHub

Discovers all skill directories under a given path in a GitHub repository
     * and imports each as a skill within the specified namespace. Each subdirectory must contain a SKILL.md file.
     *
     * **Namespace:** Used for grouping and slash-command invocation (e.g., `/superpowers:brainstorming`).
     *
     * **Idempotent:** If a skill with the same namespace + name already exists, it is updated.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.import_skill_collection201_response import ImportSkillCollection201Response
from quantcdn.models.import_skill_collection_request import ImportSkillCollectionRequest
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
    api_instance = quantcdn.AISkillsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    import_skill_collection_request = quantcdn.ImportSkillCollectionRequest() # ImportSkillCollectionRequest | 

    try:
        # Import Skill Collection from GitHub
        api_response = api_instance.import_skill_collection(organisation, import_skill_collection_request)
        print("The response of AISkillsApi->import_skill_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISkillsApi->import_skill_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **import_skill_collection_request** | [**ImportSkillCollectionRequest**](ImportSkillCollectionRequest.md)|  | 

### Return type

[**ImportSkillCollection201Response**](ImportSkillCollection201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Collection imported successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**502** | GitHub API error |  -  |
**500** | Failed to import collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_skill_collections**
> ListSkillCollections200Response list_skill_collections(organisation)

List Skill Collections

Lists distinct namespaces (collections) for the organization, with skill counts and skill names for each collection.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_skill_collections200_response import ListSkillCollections200Response
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
    api_instance = quantcdn.AISkillsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID

    try:
        # List Skill Collections
        api_response = api_instance.list_skill_collections(organisation)
        print("The response of AISkillsApi->list_skill_collections:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISkillsApi->list_skill_collections: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 

### Return type

[**ListSkillCollections200Response**](ListSkillCollections200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Collections retrieved successfully |  -  |
**403** | Access denied |  -  |
**500** | Failed to retrieve collections |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_skills**
> ListSkills200Response list_skills(organisation, tag=tag, namespace=namespace, limit=limit)

List Organization's Skills

Lists all skills available to the organization. Skills are reusable prompts,
     * workflows, or instructions that can be assigned to agents or invoked directly.
     *
     * **Skill Sources:**
     * - `inline`: Created directly via the API
     * - `skills.sh`: Imported from skills.sh registry
     * - `github`: Imported from a GitHub repository
     * - `local`: Uploaded from local file

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_skills200_response import ListSkills200Response
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
    api_instance = quantcdn.AISkillsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    tag = 'tag_example' # str | Filter skills by tag (optional)
    namespace = 'namespace_example' # str | Filter skills by collection namespace (e.g. 'superpowers') (optional)
    limit = 50 # int | Maximum number of skills to return (optional) (default to 50)

    try:
        # List Organization's Skills
        api_response = api_instance.list_skills(organisation, tag=tag, namespace=namespace, limit=limit)
        print("The response of AISkillsApi->list_skills:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISkillsApi->list_skills: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **tag** | **str**| Filter skills by tag | [optional] 
 **namespace** | **str**| Filter skills by collection namespace (e.g. &#39;superpowers&#39;) | [optional] 
 **limit** | **int**| Maximum number of skills to return | [optional] [default to 50]

### Return type

[**ListSkills200Response**](ListSkills200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | List of skills retrieved successfully |  -  |
**403** | Access denied |  -  |
**500** | Failed to retrieve skills |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sync_skill**
> ImportSkill201Response sync_skill(organisation, skill_id)

Sync Skill from Source

Re-fetches skill content from its original source.
     * Only applicable to skills imported from external sources (skills.sh, github).
     * Inline skills cannot be synced.
     *
     * **Version Behavior:**
     * - If version is pinned, fetches that specific version
     * - If no version specified, fetches latest

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.import_skill201_response import ImportSkill201Response
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
    api_instance = quantcdn.AISkillsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    skill_id = 'skill_id_example' # str | The skill ID

    try:
        # Sync Skill from Source
        api_response = api_instance.sync_skill(organisation, skill_id)
        print("The response of AISkillsApi->sync_skill:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISkillsApi->sync_skill: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **skill_id** | **str**| The skill ID | 

### Return type

[**ImportSkill201Response**](ImportSkill201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Skill synced successfully |  -  |
**400** | Cannot sync inline skill |  -  |
**403** | Access denied |  -  |
**404** | Skill not found |  -  |
**502** | Failed to fetch skill from source |  -  |
**500** | Failed to sync skill |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **sync_skill_collection**
> SyncSkillCollection200Response sync_skill_collection(organisation, namespace)

Sync Skill Collection

Re-syncs all skills in a namespace from their GitHub source. Detects new
     * skills added to the repository and flags skills removed from the source. Does NOT auto-delete removed skills.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.sync_skill_collection200_response import SyncSkillCollection200Response
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
    api_instance = quantcdn.AISkillsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    namespace = 'namespace_example' # str | Collection namespace

    try:
        # Sync Skill Collection
        api_response = api_instance.sync_skill_collection(organisation, namespace)
        print("The response of AISkillsApi->sync_skill_collection:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISkillsApi->sync_skill_collection: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **namespace** | **str**| Collection namespace | 

### Return type

[**SyncSkillCollection200Response**](SyncSkillCollection200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Collection synced successfully |  -  |
**400** | Invalid request |  -  |
**403** | Access denied |  -  |
**404** | Collection not found |  -  |
**502** | GitHub API error |  -  |
**500** | Failed to sync collection |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_skill**
> UpdateSkill200Response update_skill(organisation, skill_id, update_skill_request)

Update Skill

Updates an existing skill. For imported skills, this updates
     * local overrides (name, tags, triggerCondition) but not the source content.
     * Use the sync endpoint to update source content.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.update_skill200_response import UpdateSkill200Response
from quantcdn.models.update_skill_request import UpdateSkillRequest
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
    api_instance = quantcdn.AISkillsApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    skill_id = 'skill_id_example' # str | The skill ID
    update_skill_request = quantcdn.UpdateSkillRequest() # UpdateSkillRequest | 

    try:
        # Update Skill
        api_response = api_instance.update_skill(organisation, skill_id, update_skill_request)
        print("The response of AISkillsApi->update_skill:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AISkillsApi->update_skill: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **skill_id** | **str**| The skill ID | 
 **update_skill_request** | [**UpdateSkillRequest**](UpdateSkillRequest.md)|  | 

### Return type

[**UpdateSkill200Response**](UpdateSkill200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Skill updated successfully |  -  |
**400** | Invalid request parameters |  -  |
**403** | Access denied |  -  |
**404** | Skill not found |  -  |
**500** | Failed to update skill |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

