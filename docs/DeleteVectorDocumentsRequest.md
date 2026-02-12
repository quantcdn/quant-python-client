# DeleteVectorDocumentsRequest


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**purge_all** | **bool** | Delete ALL documents in collection | [optional] 
**document_ids** | **List[str]** | Delete specific documents by UUID | [optional] 
**metadata** | [**DeleteVectorDocumentsRequestMetadata**](DeleteVectorDocumentsRequestMetadata.md) |  | [optional] 

## Example

```python
from quantcdn.models.delete_vector_documents_request import DeleteVectorDocumentsRequest

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteVectorDocumentsRequest from a JSON string
delete_vector_documents_request_instance = DeleteVectorDocumentsRequest.from_json(json)
# print the JSON string representation of the object
print(DeleteVectorDocumentsRequest.to_json())

# convert the object into a dict
delete_vector_documents_request_dict = delete_vector_documents_request_instance.to_dict()
# create an instance of DeleteVectorDocumentsRequest from a dict
delete_vector_documents_request_from_dict = DeleteVectorDocumentsRequest.from_dict(delete_vector_documents_request_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


