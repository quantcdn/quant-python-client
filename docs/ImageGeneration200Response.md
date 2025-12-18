# ImageGeneration200Response


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**images** | **List[bytearray]** | Array of base64-encoded generated images | 
**mask_image** | **bytearray** | Base64-encoded mask image (for virtual try-on) | [optional] 
**error** | **str** | Error message if any images were blocked by content moderation | [optional] 

## Example

```python
from quantcdn.models.image_generation200_response import ImageGeneration200Response

# TODO update the JSON string below
json = "{}"
# create an instance of ImageGeneration200Response from a JSON string
image_generation200_response_instance = ImageGeneration200Response.from_json(json)
# print the JSON string representation of the object
print(ImageGeneration200Response.to_json())

# convert the object into a dict
image_generation200_response_dict = image_generation200_response_instance.to_dict()
# create an instance of ImageGeneration200Response from a dict
image_generation200_response_from_dict = ImageGeneration200Response.from_dict(image_generation200_response_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


