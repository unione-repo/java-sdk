

# EventDumpCreateRequest


## Properties

| Name | Type | Description | Notes | Example | Required |
|------------ | ------------- | ------------- | ------------- | ------------- | -------------|
|**startTime** | **String** | Date and time in YYYY-MM-DD hh:mm:ss format, specifying period start time. Data is stored for up to 32 days, depending on your tariff. |  | 2022-07-20 00:00:00 |  true  |
|**endTime** | **String** | Date and time in YYYY-MM-DD hh:mm:ss format, specifying period end time (non-inclusive). |  | 2022-07-21 00:00:00 |  |
|**limit** | **Integer** | Maximum number of events returned (default is 50). If this value is over 100 000, several files will be created, each having 100 000 events maximum. |  | 50 |  |
|**allProjects** | **Boolean** | For accounts with projects enabled, the value all_projects=true allows to fetch data for all existing projects. |  [default to false] |  |  |
|**filter** | [**FilterObject**](FilterObject.md) |  |  |  |  |
|**dumpFields** | **List&lt;String&gt;** | An array of strings containing the names of columns you need in your report, in your preferred order. If the 'dump_fields' array is missing or empty, a default field list and order will be applied. Allowed values, in their default order, are - 'project_id', 'event_time', 'job_id', 'from_email', 'email', 'status', 'delivery_status', 'metadata', 'destination_response', 'user_agent', 'url', 'ip', 'tags'. For maximum security, the 'subject' field is not included by default, but you can add it by explicitly including in the 'dump_fields' array. |  [default to new ArrayList<>()] | [\"string1\"] |  |
|**aggregate** | **String** | Allows you to obtain aggregated statistics for a given time period. The two allowed values are:<br><br>* __day_status__ - fetch aggregated statistics (the filter value must be missing or empty, as filters are not allowed with this option);* __an empty string__ - used by default, event_dump/create works as if the aggregate parameter is omitted. |  | day_status |  |
|**delimiter** | **String** | Field delimiter, can be set to either ',' or ';', defaults to ','. |  | ; |  |
|**format** | **String** | File format, either “csv” (default) or “csv_gzip”. |  [default to "csv"] | csv |  |


## Implemented Interfaces

* Serializable

[[Back to Model list]](../../README.md#models) [[Back to API list]](../../README.md#endpoints) [[Back to README]](../../README.md)


