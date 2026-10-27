# V2KvLedgerAnchor

External witness of the daily digests. Default type none. customer-bucket writes each digest to your S3 bucket (needs bucketArn and accountId); rfc3161 gets a timestamp token from tsaUrl.

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** |  | 
**bucket_arn** | **str** | customer-bucket only (required on declare). | [optional] 
**prefix** | **str** | customer-bucket only, optional. Anchor keys are &lt;prefix&gt;&lt;org&gt;/&lt;store&gt;/…. | [optional] [default to '']
**account_id** | **str** | customer-bucket only (required on declare): the AWS account that owns the bucket. Every anchor write sends it as ExpectedBucketOwner. | [optional] 
**tsa_url** | **str** | rfc3161 only. | [optional] 

## Example

```python
from quantcdn.models.v2_kv_ledger_anchor import V2KvLedgerAnchor

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvLedgerAnchor from a JSON string
v2_kv_ledger_anchor_instance = V2KvLedgerAnchor.from_json(json)
# print the JSON string representation of the object
print(V2KvLedgerAnchor.to_json())

# convert the object into a dict
v2_kv_ledger_anchor_dict = v2_kv_ledger_anchor_instance.to_dict()
# create an instance of V2KvLedgerAnchor from a dict
v2_kv_ledger_anchor_from_dict = V2KvLedgerAnchor.from_dict(v2_kv_ledger_anchor_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


