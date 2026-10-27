# V2KvIndexJob

The background job of the index (build or drop).

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**phase** | **str** | settling: about 75 seconds before the backfill starts; scanning: the backfill reads existing items; cleaning: a drop removes index data; done: no work is left. | 
**scanned** | **int** | Items the job has examined. If phase and scanned do not change for more than 960 seconds, call KV_indexes_resume. | 

## Example

```python
from quantcdn.models.v2_kv_index_job import V2KvIndexJob

# TODO update the JSON string below
json = "{}"
# create an instance of V2KvIndexJob from a JSON string
v2_kv_index_job_instance = V2KvIndexJob.from_json(json)
# print the JSON string representation of the object
print(V2KvIndexJob.to_json())

# convert the object into a dict
v2_kv_index_job_dict = v2_kv_index_job_instance.to_dict()
# create an instance of V2KvIndexJob from a dict
v2_kv_index_job_from_dict = V2KvIndexJob.from_dict(v2_kv_index_job_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


