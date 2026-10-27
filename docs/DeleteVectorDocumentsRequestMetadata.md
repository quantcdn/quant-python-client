# DeleteVectorDocumentsRequestMetadata


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**var_field** | **str** | Metadata field name (e.g., &#39;drupal_entity_id&#39;) | [optional] 
**values** | **List[str]** | Values to match (OR logic) | [optional] 

## Example

```python
from quantcdn.models.delete_vector_documents_request_metadata import DeleteVectorDocumentsRequestMetadata

# TODO update the JSON string below
json = "{}"
# create an instance of DeleteVectorDocumentsRequestMetadata from a JSON string
delete_vector_documents_request_metadata_instance = DeleteVectorDocumentsRequestMetadata.from_json(json)
# print the JSON string representation of the object
print(DeleteVectorDocumentsRequestMetadata.to_json())

# convert the object into a dict
delete_vector_documents_request_metadata_dict = delete_vector_documents_request_metadata_instance.to_dict()
# create an instance of DeleteVectorDocumentsRequestMetadata from a dict
delete_vector_documents_request_metadata_from_dict = DeleteVectorDocumentsRequestMetadata.from_dict(delete_vector_documents_request_metadata_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


