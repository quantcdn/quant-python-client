# quantcdn.AIAuditApi

All URIs are relative to *https://dashboard.quantcdn.io*

Method | HTTP request | Description
------------- | ------------- | -------------
[**ai_audit_export**](AIAuditApi.md#ai_audit_export) | **GET** /api/v3/organizations/{organisation}/ai/audit/export | Export AI audit records as JSON Lines
[**ai_audit_ledger_entries**](AIAuditApi.md#ai_audit_ledger_entries) | **GET** /api/v3/organizations/{organisation}/ai/audit/ledger/entries | List AI governance ledger entries
[**ai_audit_ledger_proof**](AIAuditApi.md#ai_audit_ledger_proof) | **GET** /api/v3/organizations/{organisation}/ai/audit/ledger/proof | Get the inclusion proof of a governance ledger entry
[**ai_audit_ledger_public_key**](AIAuditApi.md#ai_audit_ledger_public_key) | **GET** /api/v3/organizations/{organisation}/ai/audit/ledger/public-key | Get the governance ledger public key
[**ai_audit_ledger_status**](AIAuditApi.md#ai_audit_ledger_status) | **GET** /api/v3/organizations/{organisation}/ai/audit/ledger | Get the AI governance ledger status
[**ai_audit_record_get**](AIAuditApi.md#ai_audit_record_get) | **GET** /api/v3/organizations/{organisation}/ai/audit/record | Get one AI audit record
[**ai_audit_records_list**](AIAuditApi.md#ai_audit_records_list) | **GET** /api/v3/organizations/{organisation}/ai/audit/records | List AI audit records


# **ai_audit_export**
> str ai_audit_export(organisation, start_date, end_date, user_id=user_id, model_id=model_id, record_type=record_type, decision=decision, tool=tool, outcome=outcome)

Export AI audit records as JSON Lines

Every record of the range that matches the filters (the filters of aiAuditRecordsList), one JSON object per line (the row: key, date, summary, record). At most 100 pages of 200 records; a longer export ends with an error line. A failed page ends the file with an error line. Each page read is recorded in the audit log (action export). Needs view_ai_audit and, for a scoped token, ai:audit:read. Limit: 10 requests per minute.

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
    api_instance = quantcdn.AIAuditApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    start_date = '2013-10-20' # date | 
    end_date = '2013-10-20' # date | 
    user_id = 'user_id_example' # str |  (optional)
    model_id = 'model_id_example' # str |  (optional)
    record_type = 'record_type_example' # str |  (optional)
    decision = 'decision_example' # str |  (optional)
    tool = 'tool_example' # str |  (optional)
    outcome = 'outcome_example' # str |  (optional)

    try:
        # Export AI audit records as JSON Lines
        api_response = api_instance.ai_audit_export(organisation, start_date, end_date, user_id=user_id, model_id=model_id, record_type=record_type, decision=decision, tool=tool, outcome=outcome)
        print("The response of AIAuditApi->ai_audit_export:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAuditApi->ai_audit_export: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **start_date** | **date**|  | 
 **end_date** | **date**|  | 
 **user_id** | **str**|  | [optional] 
 **model_id** | **str**|  | [optional] 
 **record_type** | **str**|  | [optional] 
 **decision** | **str**|  | [optional] 
 **tool** | **str**|  | [optional] 
 **outcome** | **str**|  | [optional] 

### Return type

**str**

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/x-ndjson, application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | JSON Lines. |  -  |
**400** | Invalid range. |  -  |
**403** | PERMISSION_DENIED or SCOPE_REQUIRED |  -  |
**429** | Too many exports. See Retry-After. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_audit_ledger_entries**
> V2KvKeysPage ai_audit_ledger_entries(organisation, since=since, until=until, limit=limit, cursor=cursor)

List AI governance ledger entries

The entries of the collection events:governance, with values, in pages: follow next_cursor while has_more is true. Each entry has its ledger block (seq, hash, prevHash, shard) for verification; open a proof with aiAuditLedgerProof and check entries offline with kv-ledger-verify and aiAuditLedgerPublicKey. Events are hash-only (no prompt or response). The read is recorded in the audit log first (503 UNAVAILABLE when it cannot be). Needs view_ai_audit and, for a scoped token, ai:audit:read.

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
    api_instance = quantcdn.AIAuditApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    since = 'since_example' # str | Epoch milliseconds or ISO 8601 with a zone. Inclusive. (optional)
    until = 'until_example' # str | Epoch milliseconds or ISO 8601 with a zone. Exclusive. (optional)
    limit = 100 # int |  (optional) (default to 100)
    cursor = 'cursor_example' # str | The next_cursor of the previous page. (optional)

    try:
        # List AI governance ledger entries
        api_response = api_instance.ai_audit_ledger_entries(organisation, since=since, until=until, limit=limit, cursor=cursor)
        print("The response of AIAuditApi->ai_audit_ledger_entries:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAuditApi->ai_audit_ledger_entries: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **since** | **str**| Epoch milliseconds or ISO 8601 with a zone. Inclusive. | [optional] 
 **until** | **str**| Epoch milliseconds or ISO 8601 with a zone. Exclusive. | [optional] 
 **limit** | **int**|  | [optional] [default to 100]
 **cursor** | **str**| The next_cursor of the previous page. | [optional] 

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
**200** | One page. |  -  |
**400** | Invalid request: VALIDATION, LIMIT_EXCEEDED, CURSOR_INVALID, REQUIRES_FORMAT_2 and the route-specific 400 codes. |  -  |
**403** | PERMISSION_DENIED or SCOPE_REQUIRED |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_audit_ledger_proof**
> V2KvLedgerProof ai_audit_ledger_proof(organisation, key)

Get the inclusion proof of a governance ledger entry

The Merkle inclusion proof of one entry (key events:governance:...): entry, hash, period, merkleRoot, auditPath, the signed digest and keyId, or status pending until the entry is archived. Returned byte for byte, as KV_ledgers_proof. The read is recorded in the audit log first (503 UNAVAILABLE when it cannot be). Needs view_ai_audit and, for a scoped token, ai:audit:read.

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
    api_instance = quantcdn.AIAuditApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    key = 'events:governance:01JB0000000000000000000000' # str | 

    try:
        # Get the inclusion proof of a governance ledger entry
        api_response = api_instance.ai_audit_ledger_proof(organisation, key)
        print("The response of AIAuditApi->ai_audit_ledger_proof:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAuditApi->ai_audit_ledger_proof: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **key** | **str**|  | 

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
**403** | PERMISSION_DENIED or SCOPE_REQUIRED |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_audit_ledger_public_key**
> V2KvLedgerPublicKey ai_audit_ledger_public_key(organisation)

Get the governance ledger public key

The public key that verifies the ledger digests and receipts offline (kv-ledger-verify). The same answer as KV_ledgers_public_key. Needs view_ai_audit and, for a scoped token, ai:audit:read.

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
    api_instance = quantcdn.AIAuditApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name

    try:
        # Get the governance ledger public key
        api_response = api_instance.ai_audit_ledger_public_key(organisation)
        print("The response of AIAuditApi->ai_audit_ledger_public_key:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAuditApi->ai_audit_ledger_public_key: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 

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
**200** | The key (the PEM is in publicKeyPem). |  -  |
**403** | PERMISSION_DENIED or SCOPE_REQUIRED |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_audit_ledger_status**
> V2KvLedgerStatus ai_audit_ledger_status(organisation, cursor=cursor)

Get the AI governance ledger status

The organisation's AI governance ledger (store int-ai-governance, ledger governance): definition, retention, instances and shards with head sequence, archive lag, last digest and last verify. The same answer as KV_ledgers_status. 404 STORE_NOT_FOUND or LEDGER_NOT_FOUND when the organisation has no governance ledger. The read is recorded in the audit log first (503 UNAVAILABLE when it cannot be). Needs view_ai_audit and, for a scoped token, ai:audit:read.

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
    api_instance = quantcdn.AIAuditApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    cursor = 'cursor_example' # str | The next_cursor of the previous page. (optional)

    try:
        # Get the AI governance ledger status
        api_response = api_instance.ai_audit_ledger_status(organisation, cursor=cursor)
        print("The response of AIAuditApi->ai_audit_ledger_status:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAuditApi->ai_audit_ledger_status: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
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
**403** | PERMISSION_DENIED or SCOPE_REQUIRED |  -  |
**404** | KEY_NOT_FOUND, STORE_NOT_FOUND, LEDGER_NOT_FOUND, SUBJECT_NOT_FOUND, EXPORT_NOT_FOUND, VERIFICATION_NOT_FOUND, SHRED_NOT_FOUND, INDEX_NOT_FOUND or NOT_FOUND (no archive, tombstone or purge). |  -  |
**503** | STORE_MIGRATING (retryable, Retry-After) or UNAVAILABLE. UNAVAILABLE with retryable true (for example a new store whose table is still being created, with Retry-After 5) is safe to retry with backoff; honour Retry-After. With retryable false the outcome of a write is unknown: read before you write again. |  * Retry-After -  <br>  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_audit_record_get**
> AiAuditRecordGet200Response ai_audit_record_get(organisation, key)

Get one AI audit record

One record by key (a key from aiAuditRecordsList). A key of another organisation is 400. prompt and response are returned only when the record stores them. The read is recorded in the audit log first (503 when it cannot be). Needs view_ai_audit and, for a scoped token, ai:audit:read.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.ai_audit_record_get200_response import AiAuditRecordGet200Response
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
    api_instance = quantcdn.AIAuditApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    key = 'key_example' # str | 

    try:
        # Get one AI audit record
        api_response = api_instance.ai_audit_record_get(organisation, key)
        print("The response of AIAuditApi->ai_audit_record_get:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAuditApi->ai_audit_record_get: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **key** | **str**|  | 

### Return type

[**AiAuditRecordGet200Response**](AiAuditRecordGet200Response.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | The record. |  -  |
**400** | The key is not a record key of this organisation. |  -  |
**403** | PERMISSION_DENIED or SCOPE_REQUIRED |  -  |
**404** | Not found, or archived (older than 365 days). |  -  |
**503** | UNAVAILABLE: the read could not be recorded, so it was not made. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ai_audit_records_list**
> AiAuditRecordsPage ai_audit_records_list(organisation, start_date, end_date, since=since, until=until, user_id=user_id, token_id=token_id, model_id=model_id, record_type=record_type, decision=decision, tool=tool, outcome=outcome, interface=interface, limit=limit, cursor=cursor)

List AI audit records

One page of the organisation's AI audit records (inference, tool approvals and denials, Slack bot API calls, audit log reads). Filters match exactly. A page stops at limit rows, at 1,000 scanned records or at 20 seconds, so it can hold fewer rows than limit while hasMore is true: pass nextCursor back as cursor until hasMore is false. Order: by day, then by key. prompt and response are returned only when the record stores them. Records older than 365 days are archived (skippedArchived). Each call is recorded in the audit log (recordType audit_access) before it reads; when that record cannot be written the answer is 503 and nothing is read. Needs the view_ai_audit permission and, for a scoped token, ai:audit:read.

### Example

* Bearer (JWT) Authentication (BearerAuth):

```python
import quantcdn
from quantcdn.models.ai_audit_records_page import AiAuditRecordsPage
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
    api_instance = quantcdn.AIAuditApi(api_client)
    organisation = 'organisation_example' # str | The organisation machine name
    start_date = '2013-10-20' # date | First UTC day (inclusive). At most 31 days, not in the future, not older than 365 days.
    end_date = '2013-10-20' # date | Last UTC day (inclusive).
    since = '2013-10-20T19:20:30+01:00' # datetime | Record time from (inclusive). (optional)
    until = '2013-10-20T19:20:30+01:00' # datetime | Record time to (exclusive). (optional)
    user_id = 'user_id_example' # str | Portal user id (also matches the requester, approver and reader of tool and access records). (optional)
    token_id = 'token_id_example' # str |  (optional)
    model_id = 'model_id_example' # str |  (optional)
    record_type = 'inference' # str |  (optional)
    decision = 'approved' # str | approved, rejected, expired, or denied (tool_denied). (optional)
    tool = 'tool_example' # str |  (optional)
    outcome = 'failed' # str | outcome or status: succeeded, failed, blocked, ok, refused, error. (optional)
    interface = 'api-gateway' # str |  (optional)
    limit = 50 # int |  (optional) (default to 50)
    cursor = 'cursor_example' # str | nextCursor of the previous page (same organisation and range). (optional)

    try:
        # List AI audit records
        api_response = api_instance.ai_audit_records_list(organisation, start_date, end_date, since=since, until=until, user_id=user_id, token_id=token_id, model_id=model_id, record_type=record_type, decision=decision, tool=tool, outcome=outcome, interface=interface, limit=limit, cursor=cursor)
        print("The response of AIAuditApi->ai_audit_records_list:\n")
        pprint(api_response)
    except Exception as e:
        print("Exception when calling AIAuditApi->ai_audit_records_list: %s\n" % e)
```



### Parameters


Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **organisation** | **str**| The organisation machine name | 
 **start_date** | **date**| First UTC day (inclusive). At most 31 days, not in the future, not older than 365 days. | 
 **end_date** | **date**| Last UTC day (inclusive). | 
 **since** | **datetime**| Record time from (inclusive). | [optional] 
 **until** | **datetime**| Record time to (exclusive). | [optional] 
 **user_id** | **str**| Portal user id (also matches the requester, approver and reader of tool and access records). | [optional] 
 **token_id** | **str**|  | [optional] 
 **model_id** | **str**|  | [optional] 
 **record_type** | **str**|  | [optional] 
 **decision** | **str**| approved, rejected, expired, or denied (tool_denied). | [optional] 
 **tool** | **str**|  | [optional] 
 **outcome** | **str**| outcome or status: succeeded, failed, blocked, ok, refused, error. | [optional] 
 **interface** | **str**|  | [optional] 
 **limit** | **int**|  | [optional] [default to 50]
 **cursor** | **str**| nextCursor of the previous page (same organisation and range). | [optional] 

### Return type

[**AiAuditRecordsPage**](AiAuditRecordsPage.md)

### Authorization

[BearerAuth](../README.md#BearerAuth)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json

### HTTP response details

| Status code | Description | Response headers |
|-------------|-------------|------------------|
**200** | One page. |  -  |
**400** | Invalid range, filter, limit or cursor. |  -  |
**401** | Invalid or expired token |  -  |
**403** | PERMISSION_DENIED or SCOPE_REQUIRED |  -  |
**502** | The AI audit log could not be reached. |  -  |
**503** | UNAVAILABLE: the read could not be recorded, so it was not made. Retry. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

