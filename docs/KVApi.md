# quantcdn.KVApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**k_v_archives_list**](KVApi.md#k_v_archives_list) | **GET** /api/v2/organizations/{organization}/kv/archives | List retained ledger archives
[**k_v_archives_purge**](KVApi.md#k_v_archives_purge) | **POST** /api/v2/organizations/{organization}/kv/archives/{store_name}/purge | Dry run or start a purge of a retained archive
[**k_v_archives_purge_manifest**](KVApi.md#k_v_archives_purge_manifest) | **GET** /api/v2/organizations/{organization}/kv/archives/{store_name}/purges/{purge_id}/manifest | Get the manifest of a purge
[**k_v_archives_purge_receipt**](KVApi.md#k_v_archives_purge_receipt) | **GET** /api/v2/organizations/{organization}/kv/archives/{store_name}/purges/{purge_id}/receipt | Get the signed receipt of a purge
[**k_v_archives_purge_show**](KVApi.md#k_v_archives_purge_show) | **GET** /api/v2/organizations/{organization}/kv/archives/{store_name}/purges/{purge_id} | Show one purge of an archive
[**k_v_archives_show**](KVApi.md#k_v_archives_show) | **GET** /api/v2/organizations/{organization}/kv/archives/{store_name} | Show the archive of a deleted store
[**k_v_create**](KVApi.md#k_v_create) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv | Add a kv store
[**k_v_delete**](KVApi.md#k_v_delete) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id} | Delete a kv store
[**k_v_entries_delete**](KVApi.md#k_v_entries_delete) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items/{key}/entry | Delete a key, optionally only at a version
[**k_v_entries_put**](KVApi.md#k_v_entries_put) | **PUT** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items/{key}/entry | Set a key, optionally only if absent or only at a version
[**k_v_entries_show**](KVApi.md#k_v_entries_show) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items/{key}/entry | Get a key with its version and metadata
[**k_v_export_create**](KVApi.md#k_v_export_create) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/export | Start an export of the whole store to gzip JSON Lines files
[**k_v_export_resume**](KVApi.md#k_v_export_resume) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/export/resume | Queue a stalled export step again
[**k_v_export_show**](KVApi.md#k_v_export_show) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/export | Get the latest export and, when done, its download links
[**k_v_indexes_count**](KVApi.md#k_v_indexes_count) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/indexes/{index_name}/count | Count the keys that hold a value of a count index
[**k_v_indexes_create**](KVApi.md#k_v_indexes_create) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/indexes | Declare an index
[**k_v_indexes_delete**](KVApi.md#k_v_indexes_delete) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/indexes/{index_name} | Drop an index
[**k_v_indexes_list**](KVApi.md#k_v_indexes_list) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/indexes | List the declared indexes of a store
[**k_v_indexes_lookup**](KVApi.md#k_v_indexes_lookup) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/indexes/{index_name}/lookup | Get the key that holds a value of a unique index
[**k_v_indexes_resume**](KVApi.md#k_v_indexes_resume) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/indexes/{index_name}/resume | Queue a stalled index job step again
[**k_v_indexes_show**](KVApi.md#k_v_indexes_show) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/indexes/{index_name} | Get one index with its state and job
[**k_v_items_batch_get**](KVApi.md#k_v_items_batch_get) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/batch-get | Get up to 100 keys in one request
[**k_v_items_create**](KVApi.md#k_v_items_create) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items | Add an item to a kv store
[**k_v_items_delete**](KVApi.md#k_v_items_delete) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items/{key} | Delete an item from a kv store
[**k_v_items_increment**](KVApi.md#k_v_items_increment) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items/{key}/increment | Atomically add to a numeric value
[**k_v_items_list**](KVApi.md#k_v_items_list) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items | List items in a kv store
[**k_v_items_patch**](KVApi.md#k_v_items_patch) | **PATCH** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items/{key} | Update an item in a kv store (PATCH alias of PUT)
[**k_v_items_purge**](KVApi.md#k_v_items_purge) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items | Delete items in bulk by prefix and/or age
[**k_v_items_show**](KVApi.md#k_v_items_show) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items/{key} | Get an item from a kv store
[**k_v_items_transact**](KVApi.md#k_v_items_transact) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/transact | Run 1 to 25 operations as one transaction
[**k_v_items_update**](KVApi.md#k_v_items_update) | **PUT** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/items/{key} | Update an item in a kv store
[**k_v_keys_list**](KVApi.md#k_v_keys_list) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/keys | List keys with a cursor: by collection, prefix, filter, index or ledger time window
[**k_v_ledgers_append**](KVApi.md#k_v_ledgers_append) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/append | Append an entry to a ledger
[**k_v_ledgers_archive**](KVApi.md#k_v_ledgers_archive) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name}/archive | Get download links for the ledger archive, digests and anchor files
[**k_v_ledgers_create**](KVApi.md#k_v_ledgers_create) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers | Declare a ledger
[**k_v_ledgers_delete**](KVApi.md#k_v_ledgers_delete) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name} | Drop a ledger
[**k_v_ledgers_list**](KVApi.md#k_v_ledgers_list) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers | List the ledgers of a store
[**k_v_ledgers_proof**](KVApi.md#k_v_ledgers_proof) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name}/proof | Get the inclusion proof of one ledger entry
[**k_v_ledgers_public_key**](KVApi.md#k_v_ledgers_public_key) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/public-key | Get the public key that verifies ledger signatures
[**k_v_ledgers_show**](KVApi.md#k_v_ledgers_show) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name} | Get a ledger definition with its retention end and last verify
[**k_v_ledgers_shred**](KVApi.md#k_v_ledgers_shred) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name}/shred | Shred a data subject (cannot be undone)
[**k_v_ledgers_shreds_entries**](KVApi.md#k_v_ledgers_shreds_entries) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name}/shreds/{shred_id}/entries | List the shred entries of an erasure record
[**k_v_ledgers_shreds_list**](KVApi.md#k_v_ledgers_shreds_list) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name}/shreds | List the erasure records of a ledger
[**k_v_ledgers_shreds_receipt**](KVApi.md#k_v_ledgers_shreds_receipt) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name}/shreds/{shred_id}/receipt | Get the signed receipt of a shred
[**k_v_ledgers_status**](KVApi.md#k_v_ledgers_status) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name}/status | Get the chains, archive lag, digest, anchor and verify state of a ledger
[**k_v_ledgers_subject_entries**](KVApi.md#k_v_ledgers_subject_entries) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name}/subject-entries | List the ledger entries of one data subject
[**k_v_ledgers_subject_preview**](KVApi.md#k_v_ledgers_subject_preview) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name}/subject-preview | Preview a shred of a data subject
[**k_v_ledgers_update**](KVApi.md#k_v_ledgers_update) | **PATCH** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name} | Raise a ledger
[**k_v_ledgers_verifications_report**](KVApi.md#k_v_ledgers_verifications_report) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name}/verifications/{verification_id}/report | Get the signed report of one verification run
[**k_v_ledgers_verify**](KVApi.md#k_v_ledgers_verify) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/ledgers/{ledger_name}/verify | Verify a ledger against its archive and signed digests
[**k_v_link_to_project**](KVApi.md#k_v_link_to_project) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/link | Link a KV store to another project
[**k_v_list**](KVApi.md#k_v_list) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv | List key-value stores
[**k_v_show**](KVApi.md#k_v_show) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id} | Get a kv store
[**k_v_unlink_from_project**](KVApi.md#k_v_unlink_from_project) | **DELETE** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/link | Unlink a KV store from this project
[**k_v_upgrade_create**](KVApi.md#k_v_upgrade_create) | **POST** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/upgrade | Start, roll back, finalize or resume a format 1 to format 2 upgrade
[**k_v_upgrade_show**](KVApi.md#k_v_upgrade_show) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/upgrade | Get the store format and the latest upgrade
[**k_v_usage_show**](KVApi.md#k_v_usage_show) | **GET** /api/v2/organizations/{organization}/projects/{project}/kv/{store_id}/usage | Get 30-day usage and a cost estimate


# **k_v_archives_list**
> V2KvArchiveList k_v_archives_list(organization, limit=limit, cursor=cursor)

List retained ledger archives

Lists the deleted stores of the organisation that still hold archive objects, as the KV page envelope (data, next_cursor, has_more, page_end). The route is scoped to the organisation because a deleted store has no project link; the token also needs projects:read. Needs a token with the explicit kv:ledger:admin scope (full_access and tokens without a scope list cannot use it) and the ledger_admin permission. A token restricted to projects is refused (403 PERMISSION_DENIED): use a token without a project restriction.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_archive_list import V2KvArchiveList
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    limit = 50 # int | The maximum number of archives in the page (1-100, default 50). (optional) (default to 50)
    cursor = 'cursor_example' # str | The next_cursor of the previous page. (optional)

    try:
        # List retained ledger archives
        api_response = api_instance.k_v_archives_list(organization, limit=limit, cursor=cursor)
        print("The response of KVApi->k_v_archives_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_archives_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **limit** | **int**| The maximum number of archives in the page (1-100, default 50). | [optional] [default to 50]
 **cursor** | **str**| The next_cursor of the previous page. | [optional] 

### Return type

[**V2KvArchiveList**](V2KvArchiveList.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | A page of archives. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_archives_purge**
> V2KvArchivePurgeAnswer k_v_archives_purge(organization, store_name, v2_kv_archive_purge_request, idempotency_key=idempotency_key)

Dry run or start a purge of a retained archive

Starts the purge of the retained ledger archive of a deleted store, or reports what it would delete. dryRun defaults to true: a dry run answers 200 with dryRun true and the counts, and deletes nothing. Send dryRun false to start: the answer is 202 with purgeId and state. Both answers use the schema V2KvArchivePurgeAnswer. confirm must equal the store name, also for a dry run. Quant sets requestedBy; a client value is refused (400 VALIDATION). A repeat with the same Idempotency-Key answers 202 with the existing purge. Nothing is deleted until every object is past its lock: a purge that finds a lock or the quiet period ends as RETAINED, and a new start within 1 hour of a RETAINED result is 429 RATE_LIMITED. System stores cannot be purged (403 FORBIDDEN; the check ignores case). Read the purge with KV_archives_purge_show, then the receipt and the manifest. The route is scoped to the organisation because a deleted store has no project link; the token also needs projects:read. This route needs both explicit scopes, kv:ledger:admin and kv:ledger:purge (full_access and tokens without a scope list cannot use it), the ledger_admin permission, and, in the dashboard, a step-up (authenticator code or password). A purge cannot be undone. Rate limit: 10 requests per minute per organisation. Audited (store and purge id only, never the reason). The receipt is the platform's signed statement, not a proof of absence. A token restricted to projects is refused (403 PERMISSION_DENIED): use a token without a project restriction.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_archive_purge_answer import V2KvArchivePurgeAnswer
from quantcdn.models.v2_kv_archive_purge_request import V2KvArchivePurgeRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    store_name = 'orders' # str | The id of the deleted store, as KV_list showed it before the delete
    v2_kv_archive_purge_request = quantcdn.V2KvArchivePurgeRequest() # V2KvArchivePurgeRequest | 
    idempotency_key = 'idempotency_key_example' # str | 1 to 128 characters of letters, digits and . _ : -. A repeat with the same key answers 202 with the existing purge. (optional)

    try:
        # Dry run or start a purge of a retained archive
        api_response = api_instance.k_v_archives_purge(organization, store_name, v2_kv_archive_purge_request, idempotency_key=idempotency_key)
        print("The response of KVApi->k_v_archives_purge:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_archives_purge: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **store_name** | **str**| The id of the deleted store, as KV_list showed it before the delete | 
 **v2_kv_archive_purge_request** | [**V2KvArchivePurgeRequest**](V2KvArchivePurgeRequest.md)|  | 
 **idempotency_key** | **str**| 1 to 128 characters of letters, digits and . _ : -. A repeat with the same key answers 202 with the existing purge. | [optional] 

### Return type

[**V2KvArchivePurgeAnswer**](V2KvArchivePurgeAnswer.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Dry run: what a purge would delete (dryRun true and the counts). |  -  |
**202** | The purge was accepted, or a repeat with the same Idempotency-Key found the existing one (purgeId and state). |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_archives_purge_manifest**
> V2KvArchiveManifest k_v_archives_purge_manifest(organization, store_name, purge_id)

Get the manifest of a purge

Returns the manifest pages of a purge. Each page lists the deleted object versions and has a signed download url, valid 3,600 seconds: read the manifest again for new urls. The route is scoped to the organisation because a deleted store has no project link; the token also needs projects:read. Needs a token with the explicit kv:ledger:admin scope (full_access and tokens without a scope list cannot use it) and the ledger_admin permission. System stores have no retained archive (403 FORBIDDEN). A token restricted to projects is refused (403 PERMISSION_DENIED): use a token without a project restriction.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_archive_manifest import V2KvArchiveManifest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    store_name = 'orders' # str | The id of the deleted store, as KV_list showed it before the delete
    purge_id = '01JBX5Q8M7R2T4V6W8YZ0A1B2C' # str | The purge id (a 26-character ULID), as the purge start answered it

    try:
        # Get the manifest of a purge
        api_response = api_instance.k_v_archives_purge_manifest(organization, store_name, purge_id)
        print("The response of KVApi->k_v_archives_purge_manifest:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_archives_purge_manifest: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **store_name** | **str**| The id of the deleted store, as KV_list showed it before the delete | 
 **purge_id** | **str**| The purge id (a 26-character ULID), as the purge start answered it | 

### Return type

[**V2KvArchiveManifest**](V2KvArchiveManifest.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The manifest pages. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_archives_purge_receipt**
> V2KvArchivePurgeReceipt k_v_archives_purge_receipt(organization, store_name, purge_id)

Get the signed receipt of a purge

Returns the signed receipt of a COMPLETE purge (json, signature, keyId, algorithm ECDSA_SHA_256). Before COMPLETE the answer is 409 PURGE_NOT_COMPLETE. The receipt is the platform's signed statement that the purge ran. It is not a proof of absence. The route is scoped to the organisation because a deleted store has no project link; the token also needs projects:read. Needs a token with the explicit kv:ledger:admin scope (full_access and tokens without a scope list cannot use it) and the ledger_admin permission. System stores have no retained archive (403 FORBIDDEN). A token restricted to projects is refused (403 PERMISSION_DENIED): use a token without a project restriction.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_archive_purge_receipt import V2KvArchivePurgeReceipt
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    store_name = 'orders' # str | The id of the deleted store, as KV_list showed it before the delete
    purge_id = '01JBX5Q8M7R2T4V6W8YZ0A1B2C' # str | The purge id (a 26-character ULID), as the purge start answered it

    try:
        # Get the signed receipt of a purge
        api_response = api_instance.k_v_archives_purge_receipt(organization, store_name, purge_id)
        print("The response of KVApi->k_v_archives_purge_receipt:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_archives_purge_receipt: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **store_name** | **str**| The id of the deleted store, as KV_list showed it before the delete | 
 **purge_id** | **str**| The purge id (a 26-character ULID), as the purge start answered it | 

### Return type

[**V2KvArchivePurgeReceipt**](V2KvArchivePurgeReceipt.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The signed receipt. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_archives_purge_show**
> V2KvArchivePurge k_v_archives_purge_show(organization, store_name, purge_id)

Show one purge of an archive

Returns one purge: state, counts, requestedBy, reason and lastError. Poll it until the state is COMPLETE, RETAINED, BLOCKED or CANCELLED. Nothing is deleted until every object is past its lock. The route is scoped to the organisation because a deleted store has no project link; the token also needs projects:read. Needs a token with the explicit kv:ledger:admin scope (full_access and tokens without a scope list cannot use it) and the ledger_admin permission. System stores have no retained archive (403 FORBIDDEN). A token restricted to projects is refused (403 PERMISSION_DENIED): use a token without a project restriction.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_archive_purge import V2KvArchivePurge
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    store_name = 'orders' # str | The id of the deleted store, as KV_list showed it before the delete
    purge_id = '01JBX5Q8M7R2T4V6W8YZ0A1B2C' # str | The purge id (a 26-character ULID), as the purge start answered it

    try:
        # Show one purge of an archive
        api_response = api_instance.k_v_archives_purge_show(organization, store_name, purge_id)
        print("The response of KVApi->k_v_archives_purge_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_archives_purge_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **store_name** | **str**| The id of the deleted store, as KV_list showed it before the delete | 
 **purge_id** | **str**| The purge id (a 26-character ULID), as the purge start answered it | 

### Return type

[**V2KvArchivePurge**](V2KvArchivePurge.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The purge. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_archives_show**
> V2KvArchiveStatus k_v_archives_show(organization, store_name)

Show the archive of a deleted store

Returns the archive status of one deleted store: status, deletedAt, earliestPurgeAt (the name is not free before then), retainedUntil and the latest purge. 404 NOT_FOUND when no tombstone, purge record or archive object exists. KV_delete answers 204 and does not carry earliestPurgeAt: read it here. The route is scoped to the organisation because a deleted store has no project link; the token also needs projects:read. Needs a token with the explicit kv:ledger:admin scope (full_access and tokens without a scope list cannot use it) and the ledger_admin permission. System stores have no retained archive (403 FORBIDDEN). A token restricted to projects is refused (403 PERMISSION_DENIED): use a token without a project restriction.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_archive_status import V2KvArchiveStatus
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    store_name = 'orders' # str | The id of the deleted store, as KV_list showed it before the delete

    try:
        # Show the archive of a deleted store
        api_response = api_instance.k_v_archives_show(organization, store_name)
        print("The response of KVApi->k_v_archives_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_archives_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **store_name** | **str**| The id of the deleted store, as KV_list showed it before the delete | 

### Return type

[**V2KvArchiveStatus**](V2KvArchiveStatus.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The archive status. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_create**
> V2Store k_v_create(organization, project, v2_store_request)

Add a kv store

The new store's table takes about 5-30 seconds to become active. The request waits for the store until about 20 seconds after it started (the create call included). 200 with status ready: the store accepts data requests now. 200 without status: the store is created but the KV service gave no clear readiness answer; call KV_show. 202 with status provisioning (and Retry-After): the store exists but is not active yet; poll KV_show until status is ready. Until then every data request on the store is 503 UNAVAILABLE with retryable true and a Retry-After header; that answer is safe to retry with backoff (honour Retry-After).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_store import V2Store
from quantcdn.models.v2_store_request import V2StoreRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    v2_store_request = quantcdn.V2StoreRequest() # V2StoreRequest | 

    try:
        # Add a kv store
        api_response = api_instance.k_v_create(organization, project, v2_store_request)
        print("The response of KVApi->k_v_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **v2_store_request** | [**V2StoreRequest**](V2StoreRequest.md)|  | 

### Return type

[**V2Store**](V2Store.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The store is created. status is ready when the store accepts data requests now; status is omitted when the readiness answer was not clear (call KV_show). |  -  |
**202** | The store is created but its table is not active yet (status provisioning). Poll KV_show until status is ready. |  * Retry-After -  <br>  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**409** | STORE_NAME_RETAINED: the store name is held by a retained ledger archive (not retryable; choose another name). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_delete**
> k_v_delete(organization, project, store_id, force=force)

Delete a kv store

Deletes the store and its data. A store that still holds keys answers 409 CONFLICT with a hint: purge its keys first, or pass force=true. A store with a ledger that is not dropped and drained answers 409 LEDGER_PRESENT; ledgers lists each blocking ledger (not_dropped: drop it after its retention ends; not_drained: its last entries are not archived yet). A store that is being upgraded answers 409 UPGRADE_CONFLICT. None of these 409 answers is retryable. A store that no longer exists upstream answers 404 STORE_NOT_FOUND and its stale project link is removed. A store with an owed ledger digest answers 409 DIGEST_OWED (retryable): try again later. The answer stays 204; read KV_archives_show for earliestPurgeAt (the ledger archive of the deleted store stays until then).

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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    force = False # bool | Delete the store even if it still holds keys. Without it a non-empty store returns 409. (optional) (default to False)

    try:
        # Delete a kv store
        api_instance.k_v_delete(organization, project, store_id, force=force)
    except Exception as e:
        print("Exception when calling KVApi->k_v_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **force** | **bool**| Delete the store even if it still holds keys. Without it a non-empty store returns 409. | [optional] [default to False]

### Return type

void (empty response body)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**204** | The request has succeeded. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**404** | STORE_NOT_FOUND: the store is not in this project, or it no longer exists upstream (the stale project link is removed). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_entries_delete**
> V2KvEntryDeleteResponse k_v_entries_delete(organization, project, store_id, key, if_version=if_version)

Delete a key, optionally only at a version

With if_version (format 2 stores), deletes only when the current version matches and the key has not expired; else 409 CONFLICT with reason and currentVersion. A ledger key is 400 LEDGER_IMMUTABLE. Not retried: a lost connection is 503 UNAVAILABLE with retryable false (read the key before you delete again).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_entry_delete_response import V2KvEntryDeleteResponse
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    key = 'order:1001' # str | The key. It can contain '/'.
    if_version = 'if_version_example' # str | Format 2 stores only. Delete only at this version. (optional)

    try:
        # Delete a key, optionally only at a version
        api_response = api_instance.k_v_entries_delete(organization, project, store_id, key, if_version=if_version)
        print("The response of KVApi->k_v_entries_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_entries_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **key** | **str**| The key. It can contain &#39;/&#39;. | 
 **if_version** | **str**| Format 2 stores only. Delete only at this version. | [optional] 

### Return type

[**V2KvEntryDeleteResponse**](V2KvEntryDeleteResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Deleted. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_entries_put**
> V2KvEntryPutResponse k_v_entries_put(organization, project, store_id, key, v2_kv_entry_put_request)

Set a key, optionally only if absent or only at a version

value is any JSON value ({} stays an object). secret encrypts the value with KMS (lists show [ENCRYPTED]). ttl is 60 to 31,536,000 seconds; a write without ttl removes any expiry. Format 2 conditions: ifAbsent (201 on success) or ifVersion. A failed condition is 409 CONFLICT with reason and currentVersion. In a collection with a unique index, 409 UNIQUE_VIOLATION names index and existingKey. A ledger key is 400 LEDGER_IMMUTABLE. Not retried: a lost connection is 503 UNAVAILABLE with retryable false (the outcome is unknown; read the key before you write again).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_entry_put_request import V2KvEntryPutRequest
from quantcdn.models.v2_kv_entry_put_response import V2KvEntryPutResponse
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    key = 'order:1001' # str | The key. It can contain '/'.
    v2_kv_entry_put_request = quantcdn.V2KvEntryPutRequest() # V2KvEntryPutRequest | 

    try:
        # Set a key, optionally only if absent or only at a version
        api_response = api_instance.k_v_entries_put(organization, project, store_id, key, v2_kv_entry_put_request)
        print("The response of KVApi->k_v_entries_put:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_entries_put: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **key** | **str**| The key. It can contain &#39;/&#39;. | 
 **v2_kv_entry_put_request** | [**V2KvEntryPutRequest**](V2KvEntryPutRequest.md)|  | 

### Return type

[**V2KvEntryPutResponse**](V2KvEntryPutResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Updated. |  -  |
**201** | Created (always 201 for ifAbsent). |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_entries_show**
> V2KvEntry k_v_entries_show(organization, project, store_id, key, consistent=consistent, reveal=reveal)

Get a key with its version and metadata

Returns the value, the version (format 2 stores), timestamps, expires_at and, for a ledger entry, the ledger block. Reads are strongly consistent unless consistent is false. Works on format 1 and format 2 stores. A ledger entry needs the ledger_read permission (and, for a token with a scope list, the kv:ledger:read scope; a legacy token without a scope list needs the permission only) (else 403 PERMISSION_DENIED); its personal fields read "[PERSONAL]" (names in personal) unless the role has ledger_reveal and reveal is true. Each reveal is logged (kv.ledger.reveal). Secret values are write-only through the API: a value stored as a secret (encrypted true) reads "[ENCRYPTED]"; read it in an edge function. A lost connection is 503 UNAVAILABLE with retryable true.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_entry import V2KvEntry
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    key = 'order:1001' # str | The key. It can contain '/'.
    consistent = True # bool | false for an eventually consistent read. (optional) (default to True)
    reveal = False # bool | Ledger rows only: return personal fields in clear. Needs the ledger_reveal permission; each reveal is logged. Without it, personal fields are redacted. (optional) (default to False)

    try:
        # Get a key with its version and metadata
        api_response = api_instance.k_v_entries_show(organization, project, store_id, key, consistent=consistent, reveal=reveal)
        print("The response of KVApi->k_v_entries_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_entries_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **key** | **str**| The key. It can contain &#39;/&#39;. | 
 **consistent** | **bool**| false for an eventually consistent read. | [optional] [default to True]
 **reveal** | **bool**| Ledger rows only: return personal fields in clear. Needs the ledger_reveal permission; each reveal is logged. Without it, personal fields are redacted. | [optional] [default to False]

### Return type

[**V2KvEntry**](V2KvEntry.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The key. |  * X-Quant-KV-Format - The store format. <br>  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_export_create**
> V2KvExportResponse k_v_export_create(organization, project, store_id, body=body)

Start an export of the whole store to gzip JSON Lines files

Runs in the background; poll KV_export_show. One export at a time per store (409 EXPORT_IN_PROGRESS). Stores over 1 GiB are 400 LIMIT_EXCEEDED. 503 STORE_MIGRATING during an upgrade. When the store has any ledger, in any state (also one that is being dropped), the role also needs ledger_read (403 PERMISSION_DENIED) and a token with a scope list also needs kv:ledger:read (403 SCOPE_REQUIRED), because the files contain the ledger entries; the portal checks the store's ledger list first and refuses when it cannot read it. A lost connection is 503 UNAVAILABLE with retryable false: read KV_export_show before you send it again. Rate limit: 10 requests per minute per project, shared by every kv-admin operation (index create, delete and resume; upgrade; export create and resume; ledger declare, raise and drop). Over the limit the answer is 429 RATE_LIMITED with a Retry-After header: clients (for example Terraform) must wait Retry-After seconds, then send the request again.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_export_response import V2KvExportResponse
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    body = None # object |  (optional)

    try:
        # Start an export of the whole store to gzip JSON Lines files
        api_response = api_instance.k_v_export_create(organization, project, store_id, body=body)
        print("The response of KVApi->k_v_export_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_export_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **body** | **object**|  | [optional] 

### Return type

[**V2KvExportResponse**](V2KvExportResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Accepted. The export is requested. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_export_resume**
> V2KvExportResponse k_v_export_resume(organization, project, store_id)

Queue a stalled export step again

Use it when KV_export_show shows no change of updatedAt for more than 960 seconds (a queued step was lost). A resumed export reuses the export already started. Safe to repeat: 409 CONFLICT when the export is in a final phase or its step is still running. A lost connection is 503 UNAVAILABLE with retryable true. When the store has a ledger, the role also needs ledger_read (403 PERMISSION_DENIED) and a token with a scope list also needs kv:ledger:read (403 SCOPE_REQUIRED). Rate limit: 10 requests per minute per project, shared by every kv-admin operation (index create, delete and resume; upgrade; export create and resume; ledger declare, raise and drop). Over the limit the answer is 429 RATE_LIMITED with a Retry-After header: clients (for example Terraform) must wait Retry-After seconds, then send the request again.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_export_response import V2KvExportResponse
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list

    try:
        # Queue a stalled export step again
        api_response = api_instance.k_v_export_resume(organization, project, store_id)
        print("The response of KVApi->k_v_export_resume:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_export_resume: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 

### Return type

[**V2KvExportResponse**](V2KvExportResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Accepted. A step is queued. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_export_show**
> V2KvExportResponse k_v_export_show(organization, project, store_id)

Get the latest export and, when done, its download links

In phase done the export has downloads: one presigned URL per part, valid for 1 hour and new on every call. After expiresAt the phase is expired and there are no downloads. 404 EXPORT_NOT_FOUND when the store was never exported (or the last export failed more than 7 days ago). When the store has a ledger, the role also needs ledger_read (403 PERMISSION_DENIED) and a token with a scope list also needs kv:ledger:read (403 SCOPE_REQUIRED), because the files contain the ledger entries.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_export_response import V2KvExportResponse
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list

    try:
        # Get the latest export and, when done, its download links
        api_response = api_instance.k_v_export_show(organization, project, store_id)
        print("The response of KVApi->k_v_export_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_export_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 

### Return type

[**V2KvExportResponse**](V2KvExportResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The latest export. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_indexes_count**
> V2KvCount k_v_indexes_count(organization, project, store_id, index_name, equals=equals)

Count the keys that hold a value of a count index

Count indexes only; the index must be ACTIVE (409 INDEX_NOT_READY while BUILDING). Strongly consistent. A value that no key holds counts 0. Omit equals (or send {}) for an index with no fields, which counts the whole collection. The answer has no rows, so no ledger data (count indexes are refused on ledger collections).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_count import V2KvCount
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    index_name = 'byCustomer' # str | 
    equals = '{\"plan\":\"pro\"}' # str | A JSON object that gives a JSON scalar for exactly the index fields. (optional)

    try:
        # Count the keys that hold a value of a count index
        api_response = api_instance.k_v_indexes_count(organization, project, store_id, index_name, equals=equals)
        print("The response of KVApi->k_v_indexes_count:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_indexes_count: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **index_name** | **str**|  | 
 **equals** | **str**| A JSON object that gives a JSON scalar for exactly the index fields. | [optional] 

### Return type

[**V2KvCount**](V2KvCount.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The count. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_indexes_create**
> V2KvIndex k_v_indexes_create(organization, project, store_id, v2_kv_index_request)

Declare an index

Format 2 stores only (400 REQUIRES_FORMAT_2). The index starts in state BUILDING. About 40 seconds after the declare, writes maintain it; about 75 seconds after it, a job backfills existing items and sets the state to ACTIVE, or FAILED with error and conflicts. The answer is 202 Accepted with the index (the backend status). Poll KV_indexes_show until state is ACTIVE (Terraform waits for ACTIVE). A unique index is not enforced in the first 40 seconds: a duplicate written then makes the build end FAILED. At most 20 indexes per store and 5 per collection (400 LIMIT_EXCEEDED). Definitions are immutable. Rate limit: 10 requests per minute per project, shared by every kv-admin operation (index create, delete and resume; upgrade; export create and resume; ledger declare, raise and drop). Over the limit the answer is 429 RATE_LIMITED with a Retry-After header: clients (for example Terraform) must wait Retry-After seconds, then send the request again. A lost connection is 503 UNAVAILABLE with retryable false: read KV_indexes_show before you send it again.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_index import V2KvIndex
from quantcdn.models.v2_kv_index_request import V2KvIndexRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    v2_kv_index_request = quantcdn.V2KvIndexRequest() # V2KvIndexRequest | 

    try:
        # Declare an index
        api_response = api_instance.k_v_indexes_create(organization, project, store_id, v2_kv_index_request)
        print("The response of KVApi->k_v_indexes_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_indexes_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **v2_kv_index_request** | [**V2KvIndexRequest**](V2KvIndexRequest.md)|  | 

### Return type

[**V2KvIndex**](V2KvIndex.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Accepted. The index is BUILDING. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_indexes_delete**
> V2KvIndex k_v_indexes_delete(organization, project, store_id, index_name)

Drop an index

The index moves to state DROPPING and a background job removes its data, then the index. KV_indexes_show then answers 404 INDEX_NOT_FOUND. Dropping an index that is already DROPPING returns it unchanged. An index that is not in the store's index list is 404 INDEX_NOT_FOUND. A lost connection is 503 UNAVAILABLE with retryable false: read KV_indexes_show before you send it again. Rate limit: 10 requests per minute per project, shared by every kv-admin operation (index create, delete and resume; upgrade; export create and resume; ledger declare, raise and drop). Over the limit the answer is 429 RATE_LIMITED with a Retry-After header: clients (for example Terraform) must wait Retry-After seconds, then send the request again.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_index import V2KvIndex
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    index_name = 'byCustomer' # str | 

    try:
        # Drop an index
        api_response = api_instance.k_v_indexes_delete(organization, project, store_id, index_name)
        print("The response of KVApi->k_v_indexes_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_indexes_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **index_name** | **str**|  | 

### Return type

[**V2KvIndex**](V2KvIndex.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Accepted. The index is DROPPING. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_indexes_list**
> V2KvIndexList k_v_indexes_list(organization, project, store_id, limit=limit)

List the declared indexes of a store

Every declared index with its state (BUILDING, ACTIVE, FAILED, DROPPING) and job phase. A store has at most 20 indexes, so the list has no cursor. limit (1-1000) only cuts the list in the portal. Empty for a store without indexes (also a format 1 store).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_index_list import V2KvIndexList
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    limit = 56 # int | The maximum number of indexes to return (1-1000). Omit it for all indexes. (optional)

    try:
        # List the declared indexes of a store
        api_response = api_instance.k_v_indexes_list(organization, project, store_id, limit=limit)
        print("The response of KVApi->k_v_indexes_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_indexes_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **limit** | **int**| The maximum number of indexes to return (1-1000). Omit it for all indexes. | [optional] 

### Return type

[**V2KvIndexList**](V2KvIndexList.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The indexes (empty when none). |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_indexes_lookup**
> V2KvIndexLookup k_v_indexes_lookup(organization, project, store_id, index_name, equals, reveal=reveal)

Get the key that holds a value of a unique index

Unique indexes only; the index must be ACTIVE (409 INDEX_NOT_READY while BUILDING). Strongly consistent. An expired owner, or an owner that no longer holds the value, is 404 KEY_NOT_FOUND. An owner that is an entry of a ledger in the retired subject format is 409 LEDGER_FORMAT_RETIRED (not retryable). A ledger entry needs the ledger_read permission (and, for a token with a scope list, the kv:ledger:read scope; a legacy token without a scope list needs the permission only) (403 PERMISSION_DENIED); its personal fields are [PERSONAL] unless the role has ledger_reveal and reveal=true (each reveal is logged as kv.ledger.reveal). reveal is a portal option and is not sent to the KV service. An empty object {} in a value stays {}, but a ledger entry whose whole value is {} reads [PERSONAL] (fail closed). Secret values are write-only through the API: a value stored as a secret (encrypted true) reads [ENCRYPTED]; read it in an edge function.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_index_lookup import V2KvIndexLookup
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    index_name = 'byCustomer' # str | 
    equals = '{\"email\":\"ann@example.com\"}' # str | A JSON object that gives a JSON scalar for exactly the index fields. Values are type-tagged (1 and \"1\" differ).
    reveal = False # bool | Ledger rows only: return personal fields in clear. Needs the ledger_reveal permission; each reveal is logged. Without it, personal fields are redacted. (optional) (default to False)

    try:
        # Get the key that holds a value of a unique index
        api_response = api_instance.k_v_indexes_lookup(organization, project, store_id, index_name, equals, reveal=reveal)
        print("The response of KVApi->k_v_indexes_lookup:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_indexes_lookup: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **index_name** | **str**|  | 
 **equals** | **str**| A JSON object that gives a JSON scalar for exactly the index fields. Values are type-tagged (1 and \&quot;1\&quot; differ). | 
 **reveal** | **bool**| Ledger rows only: return personal fields in clear. Needs the ledger_reveal permission; each reveal is logged. Without it, personal fields are redacted. | [optional] [default to False]

### Return type

[**V2KvIndexLookup**](V2KvIndexLookup.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The key that holds the value. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_indexes_resume**
> V2KvIndex k_v_indexes_resume(organization, project, store_id, index_name)

Queue a stalled index job step again

Use it when KV_indexes_show shows a job whose phase and scanned count have not changed for more than 960 seconds (a queued step was lost). It changes nothing else and is safe to repeat, so a lost connection is 503 UNAVAILABLE with retryable true. An index that is not in the store's index list is 404 INDEX_NOT_FOUND. Rate limit: 10 requests per minute per project, shared by every kv-admin operation (index create, delete and resume; upgrade; export create and resume; ledger declare, raise and drop). Over the limit the answer is 429 RATE_LIMITED with a Retry-After header: clients (for example Terraform) must wait Retry-After seconds, then send the request again.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_index import V2KvIndex
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    index_name = 'byCustomer' # str | 

    try:
        # Queue a stalled index job step again
        api_response = api_instance.k_v_indexes_resume(organization, project, store_id, index_name)
        print("The response of KVApi->k_v_indexes_resume:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_indexes_resume: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **index_name** | **str**|  | 

### Return type

[**V2KvIndex**](V2KvIndex.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Accepted. A step is queued. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_indexes_show**
> V2KvIndex k_v_indexes_show(organization, project, store_id, index_name)

Get one index with its state and job

The portal reads the index list and returns the named index. State BUILDING moves to ACTIVE or FAILED; poll this route until ACTIVE. A dropped index answers 404 INDEX_NOT_FOUND once the drop job has finished. A name that does not match the index name pattern is 400 VALIDATION.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_index import V2KvIndex
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    index_name = 'byCustomer' # str | 

    try:
        # Get one index with its state and job
        api_response = api_instance.k_v_indexes_show(organization, project, store_id, index_name)
        print("The response of KVApi->k_v_indexes_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_indexes_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **index_name** | **str**|  | 

### Return type

[**V2KvIndex**](V2KvIndex.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The index. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_items_batch_get**
> V2KvBatchGetResponse k_v_items_batch_get(organization, project, store_id, v2_kv_batch_get_request, reveal=reveal)

Get up to 100 keys in one request

Reads 1 to 100 keys. Works on format 1 and format 2 stores. items has one entry per requested key in input order: the entry, or null for a missing or expired key. A response over 4 MiB is 400 LIMIT_EXCEEDED. A ledger entry needs the ledger_read permission (and, for a token with a scope list, the kv:ledger:read scope; a legacy token without a scope list needs the permission only) (else 403 PERMISSION_DENIED for the whole request); personal fields read "[PERSONAL]" unless the role has ledger_reveal and reveal is true (logged as kv.ledger.reveal). Secret values are write-only through the API: a value stored as a secret (encrypted true) reads "[ENCRYPTED]"; read it in an edge function. A read: a lost connection is 503 UNAVAILABLE with retryable true.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_batch_get_request import V2KvBatchGetRequest
from quantcdn.models.v2_kv_batch_get_response import V2KvBatchGetResponse
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    v2_kv_batch_get_request = quantcdn.V2KvBatchGetRequest() # V2KvBatchGetRequest | 
    reveal = False # bool | Ledger rows only: return personal fields in clear. Needs the ledger_reveal permission; each reveal is logged. Without it, personal fields are redacted. (optional) (default to False)

    try:
        # Get up to 100 keys in one request
        api_response = api_instance.k_v_items_batch_get(organization, project, store_id, v2_kv_batch_get_request, reveal=reveal)
        print("The response of KVApi->k_v_items_batch_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_batch_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **v2_kv_batch_get_request** | [**V2KvBatchGetRequest**](V2KvBatchGetRequest.md)|  | 
 **reveal** | **bool**| Ledger rows only: return personal fields in clear. Needs the ledger_reveal permission; each reveal is logged. Without it, personal fields are redacted. | [optional] [default to False]

### Return type

[**V2KvBatchGetResponse**](V2KvBatchGetResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | One entry per key, in input order. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_items_create**
> KVItemsCreate200Response k_v_items_create(organization, project, store_id, v2_store_item_request)

Add an item to a kv store

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.kv_items_create200_response import KVItemsCreate200Response
from quantcdn.models.v2_store_item_request import V2StoreItemRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    v2_store_item_request = quantcdn.V2StoreItemRequest() # V2StoreItemRequest | 

    try:
        # Add an item to a kv store
        api_response = api_instance.k_v_items_create(organization, project, store_id, v2_store_item_request)
        print("The response of KVApi->k_v_items_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **v2_store_item_request** | [**V2StoreItemRequest**](V2StoreItemRequest.md)|  | 

### Return type

[**KVItemsCreate200Response**](KVItemsCreate200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**422** | Validation error. |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_items_delete**
> KVItemsDelete200Response k_v_items_delete(organization, project, store_id, key)

Delete an item from a kv store

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.kv_items_delete200_response import KVItemsDelete200Response
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    key = 'key_example' # str | 

    try:
        # Delete an item from a kv store
        api_response = api_instance.k_v_items_delete(organization, project, store_id, key)
        print("The response of KVApi->k_v_items_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **key** | **str**|  | 

### Return type

[**KVItemsDelete200Response**](KVItemsDelete200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_items_increment**
> V2KvIncrementResponse k_v_items_increment(organization, project, store_id, key, v2_kv_increment_request=v2_kv_increment_request)

Atomically add to a numeric value

Adds amount (a nonzero safe integer, default 1) to an unencrypted integer value. A missing or expired key starts at 0. ttl (60 to 31,536,000 seconds) applies only when the key is created or reset after expiry. Not available in a collection with any index (400 VALIDATION) or a ledger collection (400 LEDGER_IMMUTABLE). Not idempotent: a lost connection is 503 UNAVAILABLE with retryable false; do not retry automatically.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_increment_request import V2KvIncrementRequest
from quantcdn.models.v2_kv_increment_response import V2KvIncrementResponse
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    key = 'order:1001' # str | The key. It can contain '/'.
    v2_kv_increment_request = quantcdn.V2KvIncrementRequest() # V2KvIncrementRequest |  (optional)

    try:
        # Atomically add to a numeric value
        api_response = api_instance.k_v_items_increment(organization, project, store_id, key, v2_kv_increment_request=v2_kv_increment_request)
        print("The response of KVApi->k_v_items_increment:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_increment: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **key** | **str**| The key. It can contain &#39;/&#39;. | 
 **v2_kv_increment_request** | [**V2KvIncrementRequest**](V2KvIncrementRequest.md)|  | [optional] 

### Return type

[**V2KvIncrementResponse**](V2KvIncrementResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The value after this increment. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_items_list**
> V2StoreItemsListResponse k_v_items_list(organization, project, store_id, cursor=cursor, limit=limit, search=search, include_values=include_values)

List items in a kv store

Ledger collections are left out (hidden_ledger_collections and notice say how many) when the role lacks the ledger_read permission, or when a token with a scope list lacks the kv:ledger:read scope. A legacy token without a scope list needs the permission only.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_store_items_list_response import V2StoreItemsListResponse
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    cursor = 'cursor_example' # str | Cursor for pagination (optional)
    limit = 10 # int | Number of items to return (1 to 1000, default 10) (optional) (default to 10)
    search = 'search_example' # str | Search filter for keys (optional)
    include_values = False # bool | Include values in the response. Secret values will be redacted as '[ENCRYPTED]' for security. (optional) (default to False)

    try:
        # List items in a kv store
        api_response = api_instance.k_v_items_list(organization, project, store_id, cursor=cursor, limit=limit, search=search, include_values=include_values)
        print("The response of KVApi->k_v_items_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **cursor** | **str**| Cursor for pagination | [optional] 
 **limit** | **int**| Number of items to return (1 to 1000, default 10) | [optional] [default to 10]
 **search** | **str**| Search filter for keys | [optional] 
 **include_values** | **bool**| Include values in the response. Secret values will be redacted as &#39;[ENCRYPTED]&#39; for security. | [optional] [default to False]

### Return type

[**V2StoreItemsListResponse**](V2StoreItemsListResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_items_patch**
> KVItemsCreate200Response k_v_items_patch(organization, project, store_id, key, v2_store_item_update_request)

Update an item in a kv store (PATCH alias of PUT)

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.kv_items_create200_response import KVItemsCreate200Response
from quantcdn.models.v2_store_item_update_request import V2StoreItemUpdateRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    key = 'key_example' # str | 
    v2_store_item_update_request = quantcdn.V2StoreItemUpdateRequest() # V2StoreItemUpdateRequest | 

    try:
        # Update an item in a kv store (PATCH alias of PUT)
        api_response = api_instance.k_v_items_patch(organization, project, store_id, key, v2_store_item_update_request)
        print("The response of KVApi->k_v_items_patch:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_patch: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **key** | **str**|  | 
 **v2_store_item_update_request** | [**V2StoreItemUpdateRequest**](V2StoreItemUpdateRequest.md)|  | 

### Return type

[**KVItemsCreate200Response**](KVItemsCreate200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**422** | Validation error. |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_items_purge**
> KVItemsPurge200Response k_v_items_purge(organization, project, store_id, prefix=prefix, older_than=older_than)

Delete items in bulk by prefix and/or age

Deletes every item matching the filters. With no filters the whole store is cleared. A small purge finishes in the request and returns 200; a large one returns 202 with the counts so far and continues in the background. Idempotent.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.kv_items_purge200_response import KVItemsPurge200Response
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    prefix = 'oauth_state:' # str | Only delete keys that start with this string. (optional)
    older_than = '24h' # str | Only delete keys last updated before this instant. ISO 8601, or a duration with unit s, m, h or d. (optional)

    try:
        # Delete items in bulk by prefix and/or age
        api_response = api_instance.k_v_items_purge(organization, project, store_id, prefix=prefix, older_than=older_than)
        print("The response of KVApi->k_v_items_purge:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_purge: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **prefix** | **str**| Only delete keys that start with this string. | [optional] 
 **older_than** | **str**| Only delete keys last updated before this instant. ISO 8601, or a duration with unit s, m, h or d. | [optional] 

### Return type

[**KVItemsPurge200Response**](KVItemsPurge200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The purge finished. |  -  |
**202** | The purge continues in the background. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_items_show**
> KVItemsShow200Response k_v_items_show(organization, project, store_id, key)

Get an item from a kv store

Retrieves an item from the KV store. **Security Note:** If the item was stored as a secret (secret=true), the value will be redacted and returned as '[ENCRYPTED]' for security. Secrets should be accessed directly via the Quant Cloud platform KVStore abstraction.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.kv_items_show200_response import KVItemsShow200Response
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    key = 'key_example' # str | 

    try:
        # Get an item from a kv store
        api_response = api_instance.k_v_items_show(organization, project, store_id, key)
        print("The response of KVApi->k_v_items_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **key** | **str**|  | 

### Return type

[**KVItemsShow200Response**](KVItemsShow200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_items_transact**
> V2KvTransactResponse k_v_items_transact(organization, project, store_id, v2_kv_transact_request)

Run 1 to 25 operations as one transaction

Format 2 stores only. Runs 1 to 25 operations on different keys as one transaction: all or none. check: version. set: value, secret, ttl (60 to 31,536,000 s), ifAbsent, ifVersion. delete: ifVersion. increment: amount. Any other field fails VALIDATION. A failed condition is 409 CONFLICT with operation (its index) and reason. With idempotencyKey, a repeat of the same operations within 24 hours returns the first result with replayed true. A lost connection is 503 UNAVAILABLE: retryable is true only when the request has idempotencyKey, and then retry only with the same idempotencyKey; without it the outcome is unknown (retryable false).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_transact_request import V2KvTransactRequest
from quantcdn.models.v2_kv_transact_response import V2KvTransactResponse
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    v2_kv_transact_request = quantcdn.V2KvTransactRequest() # V2KvTransactRequest | 

    try:
        # Run 1 to 25 operations as one transaction
        api_response = api_instance.k_v_items_transact(organization, project, store_id, v2_kv_transact_request)
        print("The response of KVApi->k_v_items_transact:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_transact: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **v2_kv_transact_request** | [**V2KvTransactRequest**](V2KvTransactRequest.md)|  | 

### Return type

[**V2KvTransactResponse**](V2KvTransactResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Applied (replayed true: applied by an earlier request with the same idempotencyKey). |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_items_update**
> KVItemsCreate200Response k_v_items_update(organization, project, store_id, key, v2_store_item_update_request)

Update an item in a kv store

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.kv_items_create200_response import KVItemsCreate200Response
from quantcdn.models.v2_store_item_update_request import V2StoreItemUpdateRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 
    key = 'key_example' # str | 
    v2_store_item_update_request = quantcdn.V2StoreItemUpdateRequest() # V2StoreItemUpdateRequest | 

    try:
        # Update an item in a kv store
        api_response = api_instance.k_v_items_update(organization, project, store_id, key, v2_store_item_update_request)
        print("The response of KVApi->k_v_items_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_items_update: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 
 **key** | **str**|  | 
 **v2_store_item_update_request** | [**V2StoreItemUpdateRequest**](V2StoreItemUpdateRequest.md)|  | 

### Return type

[**KVItemsCreate200Response**](KVItemsCreate200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**422** | Validation error. |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_keys_list**
> V2KvKeysPage k_v_keys_list(organization, project, store_id, collection=collection, prefix=prefix, pattern=pattern, starts_with=starts_with, after=after, before=before, reverse=reverse, since=since, until=until, index=index, equals=equals, where=where, type=type, include_values=include_values, subject_tag=subject_tag, limit=limit, cursor=cursor, reveal=reveal)

List keys with a cursor: by collection, prefix, filter, index or ledger time window

Always cursor mode. limit is 1 to 1000 (default 25). A page can hold fewer than limit rows while has_more is true (4,000,000 byte page budget or the read budget; see page_end): follow next_cursor while has_more is true. Cursors are signed, valid 24 hours and bound to the store and the query. collection lists one collection (the key text before the last ':'); collection= (empty) is the root collection. index with equals lists the members of a declared index (format 2). A ledger collection with since (inclusive) and until (exclusive) lists ledger entries by server time. prefix, pattern and where are scans, not indexes. Ledger rows: without the ledger_read permission, or with a token that has a scope list without kv:ledger:read, they are left out and hidden_ledger_collections and notice say how many collections were hidden; with it, personal fields read "[PERSONAL]". reveal=true (the role needs ledger_reveal) opens personal fields only in a ledger collection list and an index list; rows of a scan (prefix, pattern, where) stay sealed by the KV service, and a reveal that opens nothing is not logged. Each reveal that shows a field in clear is logged as kv.ledger.reveal. A cursor of a ledger collection list with values is bound to the reveal setting: change it and the cursor is 400 CURSOR_INVALID. Secret values are write-only through the API: a value stored as a secret (encrypted true) reads "[ENCRYPTED]"; read it in an edge function. A read: a lost connection is 503 UNAVAILABLE with retryable true.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_keys_page import V2KvKeysPage
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    collection = 'collection_example' # str | One collection (the key text before the last ':'). Empty: the root collection. Not with prefix, pattern or index. (optional)
    prefix = 'prefix_example' # str | Literal key prefix (a scan). Not with pattern or collection. (optional)
    pattern = 'pattern_example' # str | Wildcard pattern such as user_*, *_temp or *session* (a scan). (optional)
    starts_with = 'starts_with_example' # str | With collection: only ids that start with this text (no ':'). Not with after or before. (optional)
    after = 'after_example' # str | Exclusive lower bound: an id with collection, a JSON scalar with index. (optional)
    before = 'before_example' # str | Exclusive upper bound: an id with collection, a JSON scalar with index. (optional)
    reverse = False # bool | With collection or index: descending order. Format 2 only (else 400 REQUIRES_FORMAT_2). (optional) (default to False)
    since = '2026-10-16T00:00:00.000Z' # str | Ledger collection only. Epoch milliseconds or ISO 8601 with a zone. Inclusive. (optional)
    until = '1792195200000' # str | Ledger collection only. Epoch milliseconds or ISO 8601 with a zone. Exclusive; after since. (optional)
    index = 'index_example' # str | List the members of this declared index (format 2). Not with collection, prefix, pattern or starts_with. (optional)
    equals = '{\"customerId\":\"customer-123\"}' # str | With index: a JSON object with exactly the index fields. A filter that names the subjectField of a ledger of the store is refused (400 VALIDATION): use KV_ledgers_subject_entries. (optional)
    where = '{\"status\":\"ready\"}' # str | A JSON object of 1 to 8 top-level equalities on plaintext object values (a filter, not an index). A filter that names the subjectField of a ledger of the store is refused (400 VALIDATION): use KV_ledgers_subject_entries. (optional)
    type = all # str | Filter by encryption. (optional) (default to all)
    include_values = False # bool | Return the values. Secret values read [ENCRYPTED] (write-only through the API). (optional) (default to False)
    subject_tag = 'subject_tag_example' # str | Ledger collections only: the entries of one subject token, as shown in personal=sealed reads. (optional)
    limit = 25 # int | The maximum number of items in the page (1-1000, default 25). A page can be shorter while has_more is true (byte or read budget; see page_end). (optional) (default to 25)
    cursor = 'cursor_example' # str | The next_cursor of the previous page. (optional)
    reveal = False # bool | Ledger rows only: return personal fields in clear. Needs the ledger_reveal permission; each reveal is logged. Without it, personal fields are redacted. (optional) (default to False)

    try:
        # List keys with a cursor: by collection, prefix, filter, index or ledger time window
        api_response = api_instance.k_v_keys_list(organization, project, store_id, collection=collection, prefix=prefix, pattern=pattern, starts_with=starts_with, after=after, before=before, reverse=reverse, since=since, until=until, index=index, equals=equals, where=where, type=type, include_values=include_values, subject_tag=subject_tag, limit=limit, cursor=cursor, reveal=reveal)
        print("The response of KVApi->k_v_keys_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_keys_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **collection** | **str**| One collection (the key text before the last &#39;:&#39;). Empty: the root collection. Not with prefix, pattern or index. | [optional] 
 **prefix** | **str**| Literal key prefix (a scan). Not with pattern or collection. | [optional] 
 **pattern** | **str**| Wildcard pattern such as user_*, *_temp or *session* (a scan). | [optional] 
 **starts_with** | **str**| With collection: only ids that start with this text (no &#39;:&#39;). Not with after or before. | [optional] 
 **after** | **str**| Exclusive lower bound: an id with collection, a JSON scalar with index. | [optional] 
 **before** | **str**| Exclusive upper bound: an id with collection, a JSON scalar with index. | [optional] 
 **reverse** | **bool**| With collection or index: descending order. Format 2 only (else 400 REQUIRES_FORMAT_2). | [optional] [default to False]
 **since** | **str**| Ledger collection only. Epoch milliseconds or ISO 8601 with a zone. Inclusive. | [optional] 
 **until** | **str**| Ledger collection only. Epoch milliseconds or ISO 8601 with a zone. Exclusive; after since. | [optional] 
 **index** | **str**| List the members of this declared index (format 2). Not with collection, prefix, pattern or starts_with. | [optional] 
 **equals** | **str**| With index: a JSON object with exactly the index fields. A filter that names the subjectField of a ledger of the store is refused (400 VALIDATION): use KV_ledgers_subject_entries. | [optional] 
 **where** | **str**| A JSON object of 1 to 8 top-level equalities on plaintext object values (a filter, not an index). A filter that names the subjectField of a ledger of the store is refused (400 VALIDATION): use KV_ledgers_subject_entries. | [optional] 
 **type** | **str**| Filter by encryption. | [optional] [default to all]
 **include_values** | **bool**| Return the values. Secret values read [ENCRYPTED] (write-only through the API). | [optional] [default to False]
 **subject_tag** | **str**| Ledger collections only: the entries of one subject token, as shown in personal&#x3D;sealed reads. | [optional] 
 **limit** | **int**| The maximum number of items in the page (1-1000, default 25). A page can be shorter while has_more is true (byte or read budget; see page_end). | [optional] [default to 25]
 **cursor** | **str**| The next_cursor of the previous page. | [optional] 
 **reveal** | **bool**| Ledger rows only: return personal fields in clear. Needs the ledger_reveal permission; each reveal is logged. Without it, personal fields are redacted. | [optional] [default to False]

### Return type

[**V2KvKeysPage**](V2KvKeysPage.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | One page. |  * X-Quant-KV-Format - The store format. <br>  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_append**
> V2KvLedgerReceipt k_v_ledgers_append(organization, project, store_id, v2_kv_ledger_append_request)

Append an entry to a ledger

Format 2 stores only. Appends one entry to the ledger declared for collection. The KV service picks the chain, assigns the id, time and sequence, hash-links the entry, seals the personal fields and records the source (type api, principal token:<token id>). The entry can never be changed or deleted (PUT, DELETE, increment and transact on a ledger collection answer 400 LEDGER_IMMUTABLE). Limits: value at most 350,000 bytes (400 LIMIT_EXCEEDED); collection at most 512 UTF-8 bytes. With idempotencyKey a retry within 24 hours returns the first receipt with replayed true. A lost connection (timeout 15 s) is 503 UNAVAILABLE: retryable true only when the request has idempotencyKey; without it the outcome is unknown, so list the collection (KV_keys_list with since) before you append again. A ledger whose writerPolicy excludes API writers (only listed Quant platform services can append) refuses the append with 500 INTERNAL (the KV service answers 403); such a ledger cannot be written through this API.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_append_request import V2KvLedgerAppendRequest
from quantcdn.models.v2_kv_ledger_receipt import V2KvLedgerReceipt
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    v2_kv_ledger_append_request = quantcdn.V2KvLedgerAppendRequest() # V2KvLedgerAppendRequest | 

    try:
        # Append an entry to a ledger
        api_response = api_instance.k_v_ledgers_append(organization, project, store_id, v2_kv_ledger_append_request)
        print("The response of KVApi->k_v_ledgers_append:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_append: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **v2_kv_ledger_append_request** | [**V2KvLedgerAppendRequest**](V2KvLedgerAppendRequest.md)|  | 

### Return type

[**V2KvLedgerReceipt**](V2KvLedgerReceipt.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**201** | Appended, or (replayed true) the first receipt of the same idempotencyKey. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_archive**
> V2KvLedgerArchive k_v_ledgers_archive(organization, project, store_id, ledger_name, cursor=cursor, digest_cursor=digest_cursor)

Get download links for the ledger archive, digests and anchor files

Presigned download URLs (each valid for up to 3600 seconds; call again for fresh URLs) for up to 100 archive objects per page. The first page also lists the store's digests with their .sig files and the anchor files (.tsr, .anchor.json). Pass next_cursor as cursor for more objects; when digestsTruncated is true (more than 2,000 digest files), pass next_digest_cursor as digest_cursor for more digests. Send cursor or digest_cursor, not both. Download every file under its key path, then run the offline verifier: node verify.mjs --dir ./archive --store <org>/<store> --public-key key.pem. Every key is under the store's prefixes ledgers/<org>/<store>/<ledger>/ and digests/<org>/<store>/; the portal drops any other link.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_archive import V2KvLedgerArchive
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 
    cursor = 'cursor_example' # str | The next_cursor of the previous page of objects. (optional)
    digest_cursor = 'digest_cursor_example' # str | The next_digest_cursor of the previous digest page. (optional)

    try:
        # Get download links for the ledger archive, digests and anchor files
        api_response = api_instance.k_v_ledgers_archive(organization, project, store_id, ledger_name, cursor=cursor, digest_cursor=digest_cursor)
        print("The response of KVApi->k_v_ledgers_archive:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_archive: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 
 **cursor** | **str**| The next_cursor of the previous page of objects. | [optional] 
 **digest_cursor** | **str**| The next_digest_cursor of the previous digest page. | [optional] 

### Return type

[**V2KvLedgerArchive**](V2KvLedgerArchive.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | One page of download links. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_create**
> V2KvLedger k_v_ledgers_create(organization, project, store_id, v2_kv_ledger_admin_declare_request)

Declare a ledger

Declares an append-only, hash-chained ledger on a collection (or a pattern where * is one whole segment) of a format 2 store. The collection must be empty: no keys and no ledger entries. The ledger is PENDING for 75 seconds (appends answer 409 LEDGER_NOT_READY until activeAfter); then the emptiness check runs again and the ledger becomes ACTIVE, or FAILED when a key was written in that window. Declaring the name of a FAILED ledger replaces it. The answer is 202 with the ledger (state PENDING): the KV service accepts the declaration and finishes it after the wait. A store has at most 20 ledgers (400 LIMIT_EXCEEDED). LEDGER_SUBJECT_REQUIRED has a fixed message. name, collection, personalFields, subjectField, subjectMode, subjectCase, anchor and writerPolicy can never change; chains, retentionDays and lockMode can only go up (KV_ledgers_update). A ledger cannot be dropped before its archive retention ends.\n\nNeeds a token with the explicit kv:ledger:admin scope (full_access and tokens without a scope list cannot use it) and the ledger_admin permission. Rate limit: 10 requests per minute per project, shared by every kv-admin operation (index create, delete and resume; upgrade; export create and resume; ledger declare, raise and drop). Over the limit the answer is 429 RATE_LIMITED with a Retry-After header: clients (for example Terraform) must wait Retry-After seconds, then send the request again. Audited (the definition fields and definitionHash, never a value). A lost connection is 503 UNAVAILABLE with retryable false: read the ledger (KV_ledgers_show) before you send it again.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger import V2KvLedger
from quantcdn.models.v2_kv_ledger_admin_declare_request import V2KvLedgerAdminDeclareRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    v2_kv_ledger_admin_declare_request = quantcdn.V2KvLedgerAdminDeclareRequest() # V2KvLedgerAdminDeclareRequest | 

    try:
        # Declare a ledger
        api_response = api_instance.k_v_ledgers_create(organization, project, store_id, v2_kv_ledger_admin_declare_request)
        print("The response of KVApi->k_v_ledgers_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **v2_kv_ledger_admin_declare_request** | [**V2KvLedgerAdminDeclareRequest**](V2KvLedgerAdminDeclareRequest.md)|  | 

### Return type

[**V2KvLedger**](V2KvLedger.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Accepted: the ledger is declared and PENDING until activeAfter, then ACTIVE (or FAILED). Read it with KV_ledgers_show. |  * X-Quant-KV-Format - The store format. <br>  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_delete**
> V2KvLedger k_v_ledgers_delete(organization, project, store_id, ledger_name)

Drop a ledger

A PENDING or FAILED ledger is removed (the answer shows it as DROPPED). An ACTIVE ledger becomes DROPPED only when every shard is fully archived and the archive retention has ended; the definition is kept, so the entries stay readable and immutable. Otherwise the answer is 409 LEDGER_RETAINED with retainUntil (the retention has not ended), with reason unarchived plus collection and shard (entries are not archived yet), or with reason retention_unknown (the retention date is not recorded yet). Dropping a DROPPED ledger returns it unchanged. The drop is idempotent: after a lost connection (503 UNAVAILABLE, retryable true) or a gateway error, send it again until it answers 200.\n\nNeeds a token with the explicit kv:ledger:admin scope (full_access and tokens without a scope list cannot use it) and the ledger_admin permission. Rate limit: 10 requests per minute per project, shared by every kv-admin operation (index create, delete and resume; upgrade; export create and resume; ledger declare, raise and drop). Over the limit the answer is 429 RATE_LIMITED with a Retry-After header: clients (for example Terraform) must wait Retry-After seconds, then send the request again. Audited.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger import V2KvLedger
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 

    try:
        # Drop a ledger
        api_response = api_instance.k_v_ledgers_delete(organization, project, store_id, ledger_name)
        print("The response of KVApi->k_v_ledgers_delete:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_delete: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 

### Return type

[**V2KvLedger**](V2KvLedger.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The dropped ledger (state DROPPED). |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | LEDGER_RETAINED (retainUntil, or reason unarchived with collection and shard, or reason retention_unknown), UPGRADE_CONFLICT, or CONTENTION (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_list**
> V2KvLedgerList k_v_ledgers_list(organization, project, store_id)

List the ledgers of a store

Every ledger (PENDING, ACTIVE, FAILED and DROPPED) with its definition and a summary (archive lag, broken shards, retention end, anchor failure, last verify). Empty for a format 1 store. A store has at most 20 ledgers, so there is no paging.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_list import V2KvLedgerList
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list

    try:
        # List the ledgers of a store
        api_response = api_instance.k_v_ledgers_list(organization, project, store_id)
        print("The response of KVApi->k_v_ledgers_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 

### Return type

[**V2KvLedgerList**](V2KvLedgerList.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The ledgers. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_proof**
> V2KvLedgerProof k_v_ledgers_proof(organization, project, store_id, ledger_name, key)

Get the inclusion proof of one ledger entry

status pending until the entry is archived and the digest that covers it is signed (about 10 minutes). status archived: the stored entry (personal fields stay sealed), its hash, the Merkle audit path to the archive object root, the signed digest and its signature. The body is the exact bytes of the KV service (application/json). When the live entry differs from its archived copy the answer is 503 UNAVAILABLE with retryable false: run KV_ledgers_verify.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_proof import V2KvLedgerProof
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 
    key = 'ai-use:agency-1:01M5104A000000000000000000-00' # str | The key of a ledger entry (collection:id), as in the append receipt.

    try:
        # Get the inclusion proof of one ledger entry
        api_response = api_instance.k_v_ledgers_proof(organization, project, store_id, ledger_name, key)
        print("The response of KVApi->k_v_ledgers_proof:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_proof: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 
 **key** | **str**| The key of a ledger entry (collection:id), as in the append receipt. | 

### Return type

[**V2KvLedgerProof**](V2KvLedgerProof.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The proof, or pending. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_public_key**
> V2KvLedgerPublicKey k_v_ledgers_public_key(organization, project, store_id)

Get the public key that verifies ledger signatures

The public half of the KMS key (ECDSA P-256, SHA-256) that signs the digests, verification reports and shred receipts. The response is application/json; publicKeyPem is the PEM text: save it as key.pem for the offline verifier (node verify.mjs --dir ./archive --store <org>/<store> --public-key key.pem).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_public_key import V2KvLedgerPublicKey
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list

    try:
        # Get the public key that verifies ledger signatures
        api_response = api_instance.k_v_ledgers_public_key(organization, project, store_id)
        print("The response of KVApi->k_v_ledgers_public_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_public_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 

### Return type

[**V2KvLedgerPublicKey**](V2KvLedgerPublicKey.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The key (application/json; the PEM is in publicKeyPem). |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_show**
> V2KvLedgerDetail k_v_ledgers_show(organization, project, store_id, ledger_name)

Get a ledger definition with its retention end and last verify

The definition, plus retainUntil (an ACTIVE ledger can be dropped after it), lastDigestAt and lastVerify (the latest complete verify result, with the id of its signed report). The chain instances are on KV_ledgers_status.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_detail import V2KvLedgerDetail
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 

    try:
        # Get a ledger definition with its retention end and last verify
        api_response = api_instance.k_v_ledgers_show(organization, project, store_id, ledger_name)
        print("The response of KVApi->k_v_ledgers_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 

### Return type

[**V2KvLedgerDetail**](V2KvLedgerDetail.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The ledger. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_shred**
> V2KvLedgerErasureShredResult k_v_ledgers_shred(organization, project, store_id, ledger_name, v2_kv_ledger_erasure_shred_request)

Shred a data subject (cannot be undone)

Crypto-shreds the personal fields of one data subject: appends a shred entry to every collection of the ledger that holds the subject, then destroys the subject key. The entries stay on the chain; their personal fields can never be decrypted again. After fullyErasedAfter (shreddedAt + 35 days) no backup of the key remains. A 200 writes one erasure record (KV_ledgers_shreds_list) with a signed receipt (KV_ledgers_shreds_receipt); the answer has shredId, subjectRef and the receipt.\n\n202 in_progress: the time budget of this call ended before every collection had its shred entry. Send the same request again until it answers 200; no entry is written twice. The shred is safe to repeat: a repeat after a 200 answers 200 with alreadyShredded true, and a lost connection is 503 UNAVAILABLE with retryable true. 409 CONTENTION and 503 UNAVAILABLE are retryable: send the same request again.\n\nThe subject id is in the body, so it stays out of request paths and access logs; the portal audit keeps only the subjectRef of the answer (and the HMAC of requestedBy). subjectId: a string or a safe integer; the server canonicalises it (trim, NFC, the ledger's case rule) and refuses an invalid id with VALIDATION. A SUBJECT_NOT_FOUND error has a fixed message that never names the subject. reason, authority and requestedBy: 1-1000 characters each, not only spaces; they are stored in the shred entries and the receipt.\n\nNeeds a token with the explicit kv:ledger:erase scope (full_access and tokens without a scope list cannot use it) and the ledger_erase permission. Rate limit: 30 requests per minute per project (kv-erase). Timeout 60 seconds. Audited.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_erasure_shred_request import V2KvLedgerErasureShredRequest
from quantcdn.models.v2_kv_ledger_erasure_shred_result import V2KvLedgerErasureShredResult
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 
    v2_kv_ledger_erasure_shred_request = quantcdn.V2KvLedgerErasureShredRequest() # V2KvLedgerErasureShredRequest | 

    try:
        # Shred a data subject (cannot be undone)
        api_response = api_instance.k_v_ledgers_shred(organization, project, store_id, ledger_name, v2_kv_ledger_erasure_shred_request)
        print("The response of KVApi->k_v_ledgers_shred:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_shred: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 
 **v2_kv_ledger_erasure_shred_request** | [**V2KvLedgerErasureShredRequest**](V2KvLedgerErasureShredRequest.md)|  | 

### Return type

[**V2KvLedgerErasureShredResult**](V2KvLedgerErasureShredResult.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The subject is shredded (or was already shredded). |  -  |
**202** | In progress: send the same request again until it answers 200. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_shreds_entries**
> V2KvLedgerErasureShredEntriesPage k_v_ledgers_shreds_entries(organization, project, store_id, ledger_name, shred_id, cursor=cursor)

List the shred entries of an erasure record

The shred entries of the erasure record, sorted by key, in pages: pass next_cursor back as cursor (the cursor is bound to the shred). The entries of all pages together, in order, hash to the receipt's entriesSha256 (SHA-256 of their JCS), so a receipt without the list can be checked: kv-ledger-verify verify-signed --entries <file>.\n\nNeeds kv:ledger:read and the ledger_read permission.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_erasure_shred_entries_page import V2KvLedgerErasureShredEntriesPage
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 
    shred_id = '01JB2Z6V8Q3M4N5P6R7S8T9V0W' # str | The shredId of a shred answer, or the id of an erasure record (KV_ledgers_shreds_list). A ULID.
    cursor = 'cursor_example' # str | The next_cursor of the previous page. (optional)

    try:
        # List the shred entries of an erasure record
        api_response = api_instance.k_v_ledgers_shreds_entries(organization, project, store_id, ledger_name, shred_id, cursor=cursor)
        print("The response of KVApi->k_v_ledgers_shreds_entries:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_shreds_entries: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 
 **shred_id** | **str**| The shredId of a shred answer, or the id of an erasure record (KV_ledgers_shreds_list). A ULID. | 
 **cursor** | **str**| The next_cursor of the previous page. | [optional] 

### Return type

[**V2KvLedgerErasureShredEntriesPage**](V2KvLedgerErasureShredEntriesPage.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | One page of shred entries. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_shreds_list**
> V2KvLedgerErasureShredPage k_v_ledgers_shreds_list(organization, project, store_id, ledger_name, cursor=cursor)

List the erasure records of a ledger

The erasure records of the ledger, newest first (by shreddedAt), at most 50 per page: pass next_cursor back as cursor (the cursor is bound to this store and ledger). Each shred that answers 200 writes one record; a repeated shred adds none. A record names the data subject by subjectRef only, never by the subject id: a keyed hash under a per-store key that only Quant holds. Treat it as a pseudonym. reason, authority and requestedBy are the text of the shred request. entries is the number of shred entries (KV_ledgers_shreds_entries lists them). ledgerForked true: the shred was made on a forked store and no shred entry is recorded; the later re-shred is a new record whose supersedes names the forked record. A failed read is an error, never an empty list.\n\nNeeds kv:ledger:read and the ledger_read permission.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_erasure_shred_page import V2KvLedgerErasureShredPage
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 
    cursor = 'cursor_example' # str | The next_cursor of the previous page. (optional)

    try:
        # List the erasure records of a ledger
        api_response = api_instance.k_v_ledgers_shreds_list(organization, project, store_id, ledger_name, cursor=cursor)
        print("The response of KVApi->k_v_ledgers_shreds_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_shreds_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 
 **cursor** | **str**| The next_cursor of the previous page. | [optional] 

### Return type

[**V2KvLedgerErasureShredPage**](V2KvLedgerErasureShredPage.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | One page of erasure records. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_shreds_receipt**
> V2KvLedgerErasureShredReceiptDocument k_v_ledgers_shreds_receipt(organization, project, store_id, ledger_name, shred_id)

Get the signed receipt of a shred

The receipt of an erasure, signed with the ledger key (ECDSA P-256 over the SHA-256 of its JCS bytes). It is the same receipt as the shred answer's: signed once, stored, never signed again. It names the subject by subjectRef, never by the id. entryCount and entriesSha256 bind the shred entries; entries is left out when the receipt would pass 300 KB (then KV_ledgers_shreds_entries serves them). The body is returned byte for byte: save the whole answer and check it offline with kv-ledger-verify verify-signed and the public key (KV_ledgers_public_key), with --entries for a receipt without the list.\n\nNeeds kv:ledger:read and the ledger_read permission.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_erasure_shred_receipt_document import V2KvLedgerErasureShredReceiptDocument
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 
    shred_id = '01JB2Z6V8Q3M4N5P6R7S8T9V0W' # str | The shredId of a shred answer, or the id of an erasure record (KV_ledgers_shreds_list). A ULID.

    try:
        # Get the signed receipt of a shred
        api_response = api_instance.k_v_ledgers_shreds_receipt(organization, project, store_id, ledger_name, shred_id)
        print("The response of KVApi->k_v_ledgers_shreds_receipt:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_shreds_receipt: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 
 **shred_id** | **str**| The shredId of a shred answer, or the id of an erasure record (KV_ledgers_shreds_list). A ULID. | 

### Return type

[**V2KvLedgerErasureShredReceiptDocument**](V2KvLedgerErasureShredReceiptDocument.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The signed receipt, byte for byte. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_status**
> V2KvLedgerStatus k_v_ledgers_status(organization, project, store_id, ledger_name, cursor=cursor)

Get the chains, archive lag, digest, anchor and verify state of a ledger

The ledger, its chain instances (one per collection and shard that holds entries; 50 per page) with head and archived sequence and archive lag, the retention end, the last digest time, the anchor state, lastVerify, verifyProgress and forked. Pass next_cursor as cursor for the next page of instances.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_status import V2KvLedgerStatus
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 
    cursor = 'cursor_example' # str | The next_cursor of the previous page. (optional)

    try:
        # Get the chains, archive lag, digest, anchor and verify state of a ledger
        api_response = api_instance.k_v_ledgers_status(organization, project, store_id, ledger_name, cursor=cursor)
        print("The response of KVApi->k_v_ledgers_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 
 **cursor** | **str**| The next_cursor of the previous page. | [optional] 

### Return type

[**V2KvLedgerStatus**](V2KvLedgerStatus.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | One page of instances. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_subject_entries**
> V2KvLedgerSubjectEntries k_v_ledgers_subject_entries(organization, project, store_id, ledger_name, v2_kv_ledger_subject_entries_request)

List the ledger entries of one data subject

Lists the entries of one data subject across the ledger's collections, in pages: pass nextToken back in the body to read the next page. The subject id stays in the body, so it never reaches a URL or an access log; a GET with equals or where on the subject field is refused (use this call). subjectId: a string or a safe integer; the server canonicalises it (trim, NFC, the ledger's case rule) and refuses an invalid id with VALIDATION. collection narrows the read to one collection; since and until are date-time bounds on the entry time; limit is 1 to 1000 (default 100).\n\npersonal defaults to sealed: personal fields read "[PERSONAL]", and the subject field shows the subject token. personal decrypted shows the personal fields in clear; it needs the ledger_reveal permission and every such read is logged as kv.ledger.reveal. The answer never holds the subjectId, a subjectRef or a subject token outside the entries. subjectState is live, or shredded (then entries is empty, shreds lists the shred ids and earlierGenerationsShredded counts the earlier key generations that were shredded). A SUBJECT_NOT_FOUND error has a fixed message that never names the subject. The read is safe to repeat: a lost connection is 503 UNAVAILABLE with retryable true. Timeout 60 seconds.\n\nNeeds kv:ledger:read and the ledger_read permission.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_subject_entries import V2KvLedgerSubjectEntries
from quantcdn.models.v2_kv_ledger_subject_entries_request import V2KvLedgerSubjectEntriesRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 
    v2_kv_ledger_subject_entries_request = quantcdn.V2KvLedgerSubjectEntriesRequest() # V2KvLedgerSubjectEntriesRequest | 

    try:
        # List the ledger entries of one data subject
        api_response = api_instance.k_v_ledgers_subject_entries(organization, project, store_id, ledger_name, v2_kv_ledger_subject_entries_request)
        print("The response of KVApi->k_v_ledgers_subject_entries:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_subject_entries: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 
 **v2_kv_ledger_subject_entries_request** | [**V2KvLedgerSubjectEntriesRequest**](V2KvLedgerSubjectEntriesRequest.md)|  | 

### Return type

[**V2KvLedgerSubjectEntries**](V2KvLedgerSubjectEntries.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | One page of the subject&#39;s entries. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_subject_preview**
> V2KvLedgerErasureSubjectPreview k_v_ledgers_subject_preview(organization, project, store_id, ledger_name, v2_kv_ledger_erasure_subject_preview_request)

Preview a shred of a data subject

Shows what a shred of one data subject touches: the entry count per collection (each count means at least N, because reads are eventual; complete is false when the 20 second budget ended first) and the state of the subject key (live, or shredded with shreddedAt). Read-only: nothing is decrypted, returned or written. The subject id is in the body, so it stays out of request paths and access logs; the portal audit keeps only the subjectRef of the answer. subjectId: a string or a safe integer; the server canonicalises it (trim, NFC, the ledger's case rule) and refuses an invalid id with VALIDATION. refKeyVersion (optional, a positive integer) is sent to the server unchanged. A SUBJECT_NOT_FOUND error has a fixed message that never names the subject.\n\nNeeds a token with the explicit kv:ledger:erase scope (full_access and tokens without a scope list cannot use it) and the ledger_erase permission. Rate limit: 30 requests per minute per project (kv-erase, shared with KV_ledgers_shred). Timeout 60 seconds. Audited.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_erasure_subject_preview import V2KvLedgerErasureSubjectPreview
from quantcdn.models.v2_kv_ledger_erasure_subject_preview_request import V2KvLedgerErasureSubjectPreviewRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 
    v2_kv_ledger_erasure_subject_preview_request = quantcdn.V2KvLedgerErasureSubjectPreviewRequest() # V2KvLedgerErasureSubjectPreviewRequest | 

    try:
        # Preview a shred of a data subject
        api_response = api_instance.k_v_ledgers_subject_preview(organization, project, store_id, ledger_name, v2_kv_ledger_erasure_subject_preview_request)
        print("The response of KVApi->k_v_ledgers_subject_preview:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_subject_preview: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 
 **v2_kv_ledger_erasure_subject_preview_request** | [**V2KvLedgerErasureSubjectPreviewRequest**](V2KvLedgerErasureSubjectPreviewRequest.md)|  | 

### Return type

[**V2KvLedgerErasureSubjectPreview**](V2KvLedgerErasureSubjectPreview.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The impact preview. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_update**
> V2KvLedger k_v_ledgers_update(organization, project, store_id, ledger_name, v2_kv_ledger_admin_raise_request)

Raise a ledger

Raises chains (up to 64), retentionDays (up to 36500) or lockMode (governance to compliance). Raise only: a value that would go down is 400 LEDGER_DIRECTION, and compliance never goes back to governance. The archive worker then extends the retention of the existing archive objects. Any other field (name, collection, personalFields, subjectField, subjectMode, subjectCase, anchor, writerPolicy) is refused with 400 VALIDATION before the KV service is called, and so is an empty body. A DROPPED or FAILED ledger cannot be raised.\n\nNeeds a token with the explicit kv:ledger:admin scope (full_access and tokens without a scope list cannot use it) and the ledger_admin permission. Rate limit: 10 requests per minute per project, shared by every kv-admin operation (index create, delete and resume; upgrade; export create and resume; ledger declare, raise and drop). Over the limit the answer is 429 RATE_LIMITED with a Retry-After header: clients (for example Terraform) must wait Retry-After seconds, then send the request again. Audited.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger import V2KvLedger
from quantcdn.models.v2_kv_ledger_admin_raise_request import V2KvLedgerAdminRaiseRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 
    v2_kv_ledger_admin_raise_request = quantcdn.V2KvLedgerAdminRaiseRequest() # V2KvLedgerAdminRaiseRequest | 

    try:
        # Raise a ledger
        api_response = api_instance.k_v_ledgers_update(organization, project, store_id, ledger_name, v2_kv_ledger_admin_raise_request)
        print("The response of KVApi->k_v_ledgers_update:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_update: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 
 **v2_kv_ledger_admin_raise_request** | [**V2KvLedgerAdminRaiseRequest**](V2KvLedgerAdminRaiseRequest.md)|  | 

### Return type

[**V2KvLedger**](V2KvLedger.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The raised ledger. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_verifications_report**
> V2KvLedgerVerificationReport k_v_ledgers_verifications_report(organization, project, store_id, ledger_name, verification_id)

Get the signed report of one verification run

Every verify (API, dashboard or the daily scheduled run) is recorded and kept 400 days. This returns the record signed with the ledger key, as the exact bytes of the KV service (application/json): save it unchanged and check it offline with the public key (kv-ledger-verify verify-signed --doc report.json --public-key key.pem). A record with complete false never states that the ledger is intact.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_verification_report import V2KvLedgerVerificationReport
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 
    verification_id = '01M52R6QW07CCAW8KHYZM9210J' # str | The verificationId of a verify answer, or lastVerify.id of the ledger.

    try:
        # Get the signed report of one verification run
        api_response = api_instance.k_v_ledgers_verifications_report(organization, project, store_id, ledger_name, verification_id)
        print("The response of KVApi->k_v_ledgers_verifications_report:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_verifications_report: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 
 **verification_id** | **str**| The verificationId of a verify answer, or lastVerify.id of the ledger. | 

### Return type

[**V2KvLedgerVerificationReport**](V2KvLedgerVerificationReport.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The signed report, byte for byte. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_ledgers_verify**
> V2KvLedgerVerifyResult k_v_ledgers_verify(organization, project, store_id, ledger_name, v2_kv_ledger_verify_request=v2_kv_ledger_verify_request)

Verify a ledger against its archive and signed digests

Recomputes the hash chain of each shard in the range, compares every archived entry with its archive object and checks each object against its signed digest. Read only, but costly: at most 10,000 entries (maxEntries) and 200 archive objects per call, and 6 calls per minute per project (429 RATE_LIMITED). When next_cursor is not null, send the same collection, since and until with cursor to continue; every page of a run has the same verificationId. A finished run has a signed report (KV_ledgers_verifications_report). Anchors are checked only by the offline verifier. The portal waits up to 60 s; a lost connection is 503 UNAVAILABLE (retryable: repeat with the same cursor).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_ledger_verify_request import V2KvLedgerVerifyRequest
from quantcdn.models.v2_kv_ledger_verify_result import V2KvLedgerVerifyResult
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    ledger_name = 'aiUse' # str | 
    v2_kv_ledger_verify_request = quantcdn.V2KvLedgerVerifyRequest() # V2KvLedgerVerifyRequest |  (optional)

    try:
        # Verify a ledger against its archive and signed digests
        api_response = api_instance.k_v_ledgers_verify(organization, project, store_id, ledger_name, v2_kv_ledger_verify_request=v2_kv_ledger_verify_request)
        print("The response of KVApi->k_v_ledgers_verify:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_ledgers_verify: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **ledger_name** | **str**|  | 
 **v2_kv_ledger_verify_request** | [**V2KvLedgerVerifyRequest**](V2KvLedgerVerifyRequest.md)|  | [optional] 

### Return type

[**V2KvLedgerVerifyResult**](V2KvLedgerVerifyResult.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The result of this call. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_link_to_project**
> KVLinkToProject200Response k_v_link_to_project(organization, project, store_id, kv_link_to_project_request)

Link a KV store to another project

Share a KV store from the source project with a target project. The store will be accessible in the target project.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.kv_link_to_project200_response import KVLinkToProject200Response
from quantcdn.models.kv_link_to_project_request import KVLinkToProjectRequest
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Source project identifier
    store_id = 'store-123' # str | KV store identifier
    kv_link_to_project_request = quantcdn.KVLinkToProjectRequest() # KVLinkToProjectRequest | 

    try:
        # Link a KV store to another project
        api_response = api_instance.k_v_link_to_project(organization, project, store_id, kv_link_to_project_request)
        print("The response of KVApi->k_v_link_to_project:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_link_to_project: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Source project identifier | 
 **store_id** | **str**| KV store identifier | 
 **kv_link_to_project_request** | [**KVLinkToProjectRequest**](KVLinkToProjectRequest.md)|  | 

### Return type

[**KVLinkToProject200Response**](KVLinkToProject200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Store linked successfully |  -  |
**400** | Store already linked or invalid request |  -  |
**404** | STORE_NOT_FOUND (V2KvError body: code, retryable false) when the store is not in this project; the message Target project not found. (no code) when project_id names no project of the organisation. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_list**
> List[V2Store] k_v_list(organization, project)

List key-value stores

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_store import V2Store
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier

    try:
        # List key-value stores
        api_response = api_instance.k_v_list(organization, project)
        print("The response of KVApi->k_v_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 

### Return type

[**List[V2Store]**](V2Store.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**400** | The server could not understand the request due to invalid syntax. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_show**
> V2Store k_v_show(organization, project, store_id)

Get a kv store

status is ready when the store answers data requests and provisioning while its table is still being created (then data requests are 503 UNAVAILABLE retryable). status is omitted when the KV service gives no clear answer. A ready status is cached for up to one hour.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_store import V2Store
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = '0000' # str | 

    try:
        # Get a kv store
        api_response = api_instance.k_v_show(organization, project, store_id)
        print("The response of KVApi->k_v_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**|  | 

### Return type

[**V2Store**](V2Store.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The request has succeeded. |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_unlink_from_project**
> KVLinkToProject200Response k_v_unlink_from_project(organization, project, store_id)

Unlink a KV store from this project

Remove access to a linked KV store from this project. The store must be linked (not owned by this project).

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.kv_link_to_project200_response import KVLinkToProject200Response
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'store-123' # str | KV store identifier

    try:
        # Unlink a KV store from this project
        api_response = api_instance.k_v_unlink_from_project(organization, project, store_id)
        print("The response of KVApi->k_v_unlink_from_project:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_unlink_from_project: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store identifier | 

### Return type

[**KVLinkToProject200Response**](KVLinkToProject200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Store unlinked successfully |  -  |
**400** | Store not linked or invalid request |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**403** | Forbidden. SCOPE_REQUIRED (the token needs the kv:write scope) or PERMISSION_DENIED (the role needs kv_admin), with the V2KvError body; or, without a code, the store is owned by this project (use KV_delete instead). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_upgrade_create**
> V2KvUpgradeResponse k_v_upgrade_create(organization, project, store_id, v2_kv_upgrade_request)

Start, roll back, finalize or resume a format 1 to format 2 upgrade

Runs in the background; poll KV_upgrade_show. start checks every key (preflight), copies the store to a format 2 table and switches; with dryRun true it stops at phase checked and changes nothing. While writes are frozen (about 40 seconds plus the copy time) writes answer 503 STORE_MIGRATING with Retry-After; reads continue. Stores over 100,000 items or 1 GiB cannot be upgraded. rollback is allowed after the switch (409 LEDGER_PRESENT while the store has a ledger; 409 EXPORT_IN_PROGRESS during an export). finalize is allowed after retainUntil (14 days after the switch) and deletes the format 1 table. resume queues the current step again when the phase has not changed for more than 960 seconds (otherwise 409 UPGRADE_CONFLICT). A lost connection is 503 UNAVAILABLE. For start, rollback and finalize, retryable is false: read KV_upgrade_show, then send resume if the phase does not change for 960 seconds. resume only queues the current step again, so for resume retryable is true. Every action is audited. Rate limit: 10 requests per minute per project, shared by every kv-admin operation (index create, delete and resume; upgrade; export create and resume; ledger declare, raise and drop). Over the limit the answer is 429 RATE_LIMITED with a Retry-After header: clients (for example Terraform) must wait Retry-After seconds, then send the request again.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_upgrade_request import V2KvUpgradeRequest
from quantcdn.models.v2_kv_upgrade_response import V2KvUpgradeResponse
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list
    v2_kv_upgrade_request = quantcdn.V2KvUpgradeRequest() # V2KvUpgradeRequest | 

    try:
        # Start, roll back, finalize or resume a format 1 to format 2 upgrade
        api_response = api_instance.k_v_upgrade_create(organization, project, store_id, v2_kv_upgrade_request)
        print("The response of KVApi->k_v_upgrade_create:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_upgrade_create: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 
 **v2_kv_upgrade_request** | [**V2KvUpgradeRequest**](V2KvUpgradeRequest.md)|  | 

### Return type

[**V2KvUpgradeResponse**](V2KvUpgradeResponse.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**202** | Accepted. The X-Quant-KV-Format header gives the format at the time of the answer. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**409** | CONFLICT, UNIQUE_VIOLATION, UPGRADE_CONFLICT, EXPORT_IN_PROGRESS, the LEDGER_* conflicts and the archive purge conflicts STORE_NOT_DELETED, ARCHIVE_RETAINED, PURGE_IN_PROGRESS, PURGE_BLOCKED and PURGE_NOT_COMPLETE (not retryable); CONTENTION, INDEX_NOT_READY, LEDGER_NOT_READY and DIGEST_OWED (retryable). |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_upgrade_show**
> V2KvUpgradeState k_v_upgrade_show(organization, project, store_id)

Get the store format and the latest upgrade

The store format (1 or 2), state (active, or migrating while writes are frozen), table and the latest upgrade (null if the store was never upgraded). Poll it after KV_upgrade_create.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_upgrade_state import V2KvUpgradeState
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list

    try:
        # Get the store format and the latest upgrade
        api_response = api_instance.k_v_upgrade_show(organization, project, store_id)
        print("The response of KVApi->k_v_upgrade_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_upgrade_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 

### Return type

[**V2KvUpgradeState**](V2KvUpgradeState.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Format, state, table and the latest upgrade. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **k_v_usage_show**
> V2KvUsage k_v_usage_show(organization, project, store_id)

Get 30-day usage and a cost estimate

Read and write units per UTC day for the last 30 full days, the table size and a list-price estimate. Never returns item values. A CloudWatch or DynamoDB failure is 503 UNAVAILABLE, never zeros.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.v2_kv_usage import V2KvUsage
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
    api_instance = quantcdn.KVApi(api_client)
    organization = 'test-org' # str | Organization identifier
    project = 'test-project' # str | Project identifier
    store_id = 'test-org-test-project-orders' # str | KV store id, as returned by KV_list

    try:
        # Get 30-day usage and a cost estimate
        api_response = api_instance.k_v_usage_show(organization, project, store_id)
        print("The response of KVApi->k_v_usage_show:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling KVApi->k_v_usage_show: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organization** | **str**| Organization identifier | 
 **project** | **str**| Project identifier | 
 **store_id** | **str**| KV store id, as returned by KV_list | 

### Return type

[**V2KvUsage**](V2KvUsage.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | Usage and estimate. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | SCOPE_REQUIRED (the token does not list the scope) or PERMISSION_DENIED (the role does not have the permission). |  -  |
**404** | STORE_NOT_FOUND: the store does not exist or is not in this project. |  -  |
**429** | RATE_LIMITED (retryable): a rate limit is used up. The limits are the per-token limit (api-token, default 240 requests per minute per token and organisation) and, on some operations, the per-project KV limits (kv-admin 10, kv-erase 30, kv-verify 6 requests per minute). Wait for Retry-After seconds, then send the request again. See Rate limits in the API description. |  * Retry-After - Seconds to wait before the next request. <br>  * RateLimit-Limit - The request limit of the window (IETF draft). X-RateLimit-Limit carries the same value. <br>  * RateLimit-Remaining - Requests left in the window: 0 on a 429 (IETF draft). X-RateLimit-Remaining carries the same value. <br>  * RateLimit-Reset - Seconds until the window resets (IETF draft). X-RateLimit-Reset is the same moment as a Unix timestamp. <br>  |
**500** | INTERNAL: the KV service failed. No detail is given. |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

