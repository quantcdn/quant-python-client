# ImageGenerationRequestImageGenerationConfig

General image generation configuration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**width** | **int** |  | [optional] 
**height** | **int** |  | [optional] 
**quality** | **str** |  | [optional] [default to 'standard']
**cfg_scale** | **float** |  | [optional] [default to 6.5]
**seed** | **int** |  | [optional] 
**number_of_images** | **int** |  | [optional] [default to 1]

## Example

```python
from quantcdn.models.image_generation_request_image_generation_config import ImageGenerationRequestImageGenerationConfig

# TODO update the JSON string below
json = "{}"
# create an instance of ImageGenerationRequestImageGenerationConfig from a JSON string
image_generation_request_image_generation_config_instance = ImageGenerationRequestImageGenerationConfig.from_json(json)
# print the JSON string representation of the object
print(ImageGenerationRequestImageGenerationConfig.to_json())

# convert the object into a dict
image_generation_request_image_generation_config_dict = image_generation_request_image_generation_config_instance.to_dict()
# create an instance of ImageGenerationRequestImageGenerationConfig from a dict
image_generation_request_image_generation_config_from_dict = ImageGenerationRequestImageGenerationConfig.from_dict(image_generation_request_image_generation_config_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


