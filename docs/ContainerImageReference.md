# ContainerImageReference


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **str** | Specifies whether the image is internal (ECR) or external (e.g., Docker Hub) | 
**identifier** | **str** | The image identifier. For &#39;internal&#39; type, this is the image tag. For &#39;external&#39; type, this is the full image name. | 

## Example

```python
from quantcdn.models.container_image_reference import ContainerImageReference

# TODO update the JSON string below
json = "{}"
# create an instance of ContainerImageReference from a JSON string
container_image_reference_instance = ContainerImageReference.from_json(json)
# print the JSON string representation of the object
print(ContainerImageReference.to_json())

# convert the object into a dict
container_image_reference_dict = container_image_reference_instance.to_dict()
# create an instance of ContainerImageReference from a dict
container_image_reference_from_dict = ContainerImageReference.from_dict(container_image_reference_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


