# ImageGenerationRequestImageVariationParams

Parameters for IMAGE_VARIATION task

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**images** | **List[bytearray]** |  | [optional] 
**similarity_strength** | **float** |  | [optional] 
**text** | **str** |  | [optional] 
**negative_text** | **str** |  | [optional] 

## Example

```python
from quantcdn.models.image_generation_request_image_variation_params import ImageGenerationRequestImageVariationParams

# TODO update the JSON string below
json = "{}"
# create an instance of ImageGenerationRequestImageVariationParams from a JSON string
image_generation_request_image_variation_params_instance = ImageGenerationRequestImageVariationParams.from_json(json)
# print the JSON string representation of the object
print(ImageGenerationRequestImageVariationParams.to_json())

# convert the object into a dict
image_generation_request_image_variation_params_dict = image_generation_request_image_variation_params_instance.to_dict()
# create an instance of ImageGenerationRequestImageVariationParams from a dict
image_generation_request_image_variation_params_from_dict = ImageGenerationRequestImageVariationParams.from_dict(image_generation_request_image_variation_params_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


