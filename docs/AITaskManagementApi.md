# quantcdn.AITaskManagementApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**create_task**](AITaskManagementApi.md#create_task) | **POST** /api/v3/organizations/{organisation}/ai/tasks | Create a new task
[**delete_task**](AITaskManagementApi.md#delete_task) | **DELETE** /api/v3/organizations/{organisation}/ai/tasks/{taskId} | Delete a task
[**get_dependency_graph**](AITaskManagementApi.md#get_dependency_graph) | **GET** /api/v3/organizations/{organisation}/ai/tasks/{taskListId}/dependency-graph | Get dependency graph for a task list
[**get_task**](AITaskManagementApi.md#get_task) | **GET** /api/v3/organizations/{organisation}/ai/tasks/{taskId} | Get task details
[**list_tasks**](AITaskManagementApi.md#list_tasks) | **GET** /api/v3/organizations/{organisation}/ai/tasks | List tasks with optional filtering
[**update_task**](AITaskManagementApi.md#update_task) | **PUT** /api/v3/organizations/{organisation}/ai/tasks/{taskId} | Update a task


# **create_task**
> CreateTask201Response create_task(organisation, create_task_request)

Create a new task

Creates a new task for multi-agent coordination and workflow orchestration.
     *
     * **Key Features:**
     * - **Persistent State**: Tasks survive across conversations and sessions
     * - **Agent Assignment**: Pre-assign tasks to specific agents
     * - **Task Lists**: Group related tasks using taskListId (implicit - no need to create lists first)
     * - **Dependencies**: Define task dependencies for workflow orchestration
     * - **Metadata**: Store flexible JSON metadata for task-specific data
     * - **Progress Tracking**: Track progress from 0.0 to 1.0
     *
     * **Use Cases:**
     * - Break down complex requests into manageable steps
     * - Assign work to specialized agents
     * - Track long-running operations
     * - Coordinate multi-agent workflows

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.create_task201_response import CreateTask201Response
from quantcdn.models.create_task_request import CreateTaskRequest
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
    api_instance = quantcdn.AITaskManagementApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    create_task_request = quantcdn.CreateTaskRequest() # CreateTaskRequest | 

    try:
        # Create a new task
        api_response = api_instance.create_task(organisation, create_task_request)
        print("The response of AITaskManagementApi->create_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AITaskManagementApi->create_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **create_task_request** | [**CreateTaskRequest**](CreateTaskRequest.md)|  | 

### Return type

[**CreateTask201Response**](CreateTask201Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Task created successfully |  -  |
**400** | Invalid request |  -  |
**500** | Failed to create task |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **delete_task**
> DeleteTask200Response delete_task(organisation, task_id, cascade=cascade)

Delete a task

Permanently deletes a task. This action cannot be undone.
     *
     * **Dependency Protection:**
     * By default, deletion is blocked if other tasks depend on this task (TASK_HAS_DEPENDENTS error).
     * This prevents breaking workflows.
     *
     * **Cascade Delete:**
     * Use `?cascade=true` to delete the task AND all tasks that depend on it recursively.
     * Useful for cleaning up entire dependency chains.
     *
     * **Examples:**
     * - DELETE /tasks/{id} - Deletes task if no dependents, otherwise returns 409 error
     * - DELETE /tasks/{id}?cascade=true - Deletes task and all dependent tasks

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.delete_task200_response import DeleteTask200Response
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
    api_instance = quantcdn.AITaskManagementApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    task_id = 'task_id_example' # str | The task UUID
    cascade = False # bool | If true, delete task and all dependent tasks recursively (optional) (default to False)

    try:
        # Delete a task
        api_response = api_instance.delete_task(organisation, task_id, cascade=cascade)
        print("The response of AITaskManagementApi->delete_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AITaskManagementApi->delete_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **task_id** | **str**| The task UUID | 
 **cascade** | **bool**| If true, delete task and all dependent tasks recursively | [optional] [default to False]

### Return type

[**DeleteTask200Response**](DeleteTask200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Task deleted successfully |  -  |
**409** | Task has dependents - cannot delete without cascade |  -  |
**404** | Task not found |  -  |
**500** | Failed to delete task |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_dependency_graph**
> GetDependencyGraph200Response get_dependency_graph(organisation, task_list_id)

Get dependency graph for a task list

Returns the full dependency graph for all tasks in a task list.
     *
     * **Use Cases:**
     * - Visualize task dependencies in a UI (DAG diagram)
     * - Analyze workflow structure and critical paths
     * - Find starting tasks (roots) and terminal tasks (leaves)
     * - Plan parallel execution by identifying independent task groups
     *
     * **Response Structure:**
     * - `taskCount`: Total number of tasks in the list
     * - `roots`: Task IDs with no dependencies (starting points)
     * - `leaves`: Task IDs with no dependents (terminal tasks)
     * - `graph`: Adjacency list with each task's dependencies and dependents

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_dependency_graph200_response import GetDependencyGraph200Response
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
    api_instance = quantcdn.AITaskManagementApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    task_list_id = 'world-1' # str | The task list ID to get the dependency graph for

    try:
        # Get dependency graph for a task list
        api_response = api_instance.get_dependency_graph(organisation, task_list_id)
        print("The response of AITaskManagementApi->get_dependency_graph:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AITaskManagementApi->get_dependency_graph: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **task_list_id** | **str**| The task list ID to get the dependency graph for | 

### Return type

[**GetDependencyGraph200Response**](GetDependencyGraph200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Dependency graph retrieved successfully |  -  |
**500** | Failed to get dependency graph |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **get_task**
> GetTask200Response get_task(organisation, task_id)

Get task details

Retrieves detailed information about a specific task including status, progress, dependencies, and results.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.get_task200_response import GetTask200Response
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
    api_instance = quantcdn.AITaskManagementApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    task_id = 'task_id_example' # str | The task UUID

    try:
        # Get task details
        api_response = api_instance.get_task(organisation, task_id)
        print("The response of AITaskManagementApi->get_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AITaskManagementApi->get_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **task_id** | **str**| The task UUID | 

### Return type

[**GetTask200Response**](GetTask200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Task details retrieved successfully |  -  |
**404** | Task not found |  -  |
**500** | Failed to get task |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **list_tasks**
> ListTasks200Response list_tasks(organisation, task_list_id=task_list_id, status=status, assigned_agent_id=assigned_agent_id, limit=limit, depends_on=depends_on, include_details=include_details)

List tasks with optional filtering

Lists tasks for an organization with optional filtering. Filters can be combined for powerful queries.
     *
     * **Filter Examples:**
     * - All tasks in a list: ?taskListId=world-1
     * - Pending tasks in a list: ?taskListId=world-1&status=pending
     * - Tasks assigned to an agent: ?assignedAgentId=agent-code-reviewer
     * - Combined: ?taskListId=world-1&status=in_progress&assignedAgentId=agent-1
     *
     * **Reverse Dependency Lookup:**
     * Use `dependsOn` to find tasks that depend on a specific task (waiting for it to complete):
     * - ?dependsOn=task-123 - Returns task IDs only (lightweight)
     * - ?dependsOn=task-123&includeDetails=true - Returns full task objects
     * - ?dependsOn=task-123&status=pending - Pending tasks waiting for task-123
     *
     * **Ordering:**
     * Tasks are returned in reverse chronological order (most recent first).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.list_tasks200_response import ListTasks200Response
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
    api_instance = quantcdn.AITaskManagementApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    task_list_id = 'world-1' # str | Filter tasks by task list ID. Task lists are implicit groupings - any string can be used. (optional)
    status = 'pending' # str | Filter tasks by status (optional)
    assigned_agent_id = 'agent-code-reviewer' # str | Filter tasks by assigned agent ID (optional)
    limit = 50 # int | Maximum number of tasks to return (default 50, max 100) (optional) (default to 50)
    depends_on = '550e8400-e29b-41d4-a716-446655440000' # str | Reverse lookup: find tasks that depend on this task ID. Returns tasks waiting for the specified task to complete. (optional)
    include_details = False # bool | When using dependsOn, return full task objects in addition to IDs. Default false (IDs only for lightweight responses). (optional) (default to False)

    try:
        # List tasks with optional filtering
        api_response = api_instance.list_tasks(organisation, task_list_id=task_list_id, status=status, assigned_agent_id=assigned_agent_id, limit=limit, depends_on=depends_on, include_details=include_details)
        print("The response of AITaskManagementApi->list_tasks:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AITaskManagementApi->list_tasks: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **task_list_id** | **str**| Filter tasks by task list ID. Task lists are implicit groupings - any string can be used. | [optional] 
 **status** | **str**| Filter tasks by status | [optional] 
 **assigned_agent_id** | **str**| Filter tasks by assigned agent ID | [optional] 
 **limit** | **int**| Maximum number of tasks to return (default 50, max 100) | [optional] [default to 50]
 **depends_on** | **str**| Reverse lookup: find tasks that depend on this task ID. Returns tasks waiting for the specified task to complete. | [optional] 
 **include_details** | **bool**| When using dependsOn, return full task objects in addition to IDs. Default false (IDs only for lightweight responses). | [optional] [default to False]

### Return type

[**ListTasks200Response**](ListTasks200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Tasks retrieved successfully. Response format varies: standard returns {tasks, count}, with dependsOn returns {taskIds, count, dependsOn}, with dependsOn+includeDetails returns {taskIds, tasks, count, dependsOn} |  -  |
**500** | Failed to list tasks |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **update_task**
> UpdateTask200Response update_task(organisation, task_id, update_task_request)

Update a task

Updates an existing task. All fields are optional - only provided fields will be updated.
     *
     * **Status Transitions:**
     * - Changing from **pending** to **in_progress** automatically sets startedAt timestamp
     * - Changing to **completed**, **failed**, or **cancelled** automatically sets completedAt timestamp
     * - Changing to **blocked** automatically sets blockedAt timestamp
     * - Changing from **blocked** to **in_progress** or **pending** clears blocked fields
     * - Completed tasks get a 30-day TTL for automatic cleanup
     *
     * **Progress Updates:**
     * - Update progress (0.0 to 1.0) to track completion percentage
     * - Update progressMessage for human-readable status updates
     * - Set result object when task completes successfully
     * - Set error string when task fails
     * - Set blockedReason and blockedByTaskIds when blocking a task

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.update_task200_response import UpdateTask200Response
from quantcdn.models.update_task_request import UpdateTaskRequest
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
    api_instance = quantcdn.AITaskManagementApi(api_client)
    organisation = 'organisation_example' # str | The organisation ID
    task_id = '550e8400-e29b-41d4-a716-446655440000' # str | The task UUID
    update_task_request = quantcdn.UpdateTaskRequest() # UpdateTaskRequest | 

    try:
        # Update a task
        api_response = api_instance.update_task(organisation, task_id, update_task_request)
        print("The response of AITaskManagementApi->update_task:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AITaskManagementApi->update_task: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation ID | 
 **task_id** | **str**| The task UUID | 
 **update_task_request** | [**UpdateTaskRequest**](UpdateTaskRequest.md)|  | 

### Return type

[**UpdateTask200Response**](UpdateTask200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Task updated successfully |  -  |
**400** | Invalid request |  -  |
**404** | Task not found |  -  |
**500** | Failed to update task |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

