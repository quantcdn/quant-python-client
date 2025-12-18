# CreateApplicationRequestDatabase

Optional database configuration

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**engine** | **str** | Database engine type (MySQL 8.4, Postgres) | [optional] [default to 'mysql']
**instance_class** | **str** | RDS instance class | [optional] [default to 'db.t4g.micro']
**storage_gb** | **int** | Allocated storage in GiB | [optional] [default to 20]
**multi_az** | **bool** | Enable Multi-AZ deployment (higher availability and cost) | [optional] [default to False]

## Example

```python
from quantcdn.models.create_application_request_database import CreateApplicationRequestDatabase

# TODO update the JSON string below
json = "{}"
# create an instance of CreateApplicationRequestDatabase from a JSON string
create_application_request_database_instance = CreateApplicationRequestDatabase.from_json(json)
# print the JSON string representation of the object
print(CreateApplicationRequestDatabase.to_json())

# convert the object into a dict
create_application_request_database_dict = create_application_request_database_instance.to_dict()
# create an instance of CreateApplicationRequestDatabase from a dict
create_application_request_database_from_dict = CreateApplicationRequestDatabase.from_dict(create_application_request_database_dict)
```
[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)


