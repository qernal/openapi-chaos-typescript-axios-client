# LogsApi

All URIs are relative to *https://chaos.qernal.com/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**logsList**](#logslist) | **GET** /logs | Get logs|

# **logsList**
> ListLogResponse logsList()

Retrieve logs for a specific project or function. Use the query parameter to search logs.  > Note: Logs are always returned in a descending order based on the timestamp. > Note: A max size of 500 logs is returned per request (when using page[size]). 

### Example

```typescript
import {
    LogsApi,
    Configuration,
    OrganisationsListPageParameter,
    LogsListFTimestampsParameter
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new LogsApi(configuration);

let page: OrganisationsListPageParameter; //Query parameters for pagination (optional) (default to undefined)
let f_project: string; //Project uuid reference (optional) (default to undefined)
let f_function: string; //Function uuid reference (optional) (default to undefined)
let f_timestamps: LogsListFTimestampsParameter; //Timestamp restriction for query (optional) (default to undefined)
let f_query: string; //Text query string (optional) (default to undefined)
let f_log_type: 'info' | 'error'; //Type of log (optional) (default to undefined)

const { status, data } = await apiInstance.logsList(
    page,
    f_project,
    f_function,
    f_timestamps,
    f_query,
    f_log_type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | **OrganisationsListPageParameter** | Query parameters for pagination | (optional) defaults to undefined|
| **f_project** | [**string**] | Project uuid reference | (optional) defaults to undefined|
| **f_function** | [**string**] | Function uuid reference | (optional) defaults to undefined|
| **f_timestamps** | **LogsListFTimestampsParameter** | Timestamp restriction for query | (optional) defaults to undefined|
| **f_query** | [**string**] | Text query string | (optional) defaults to undefined|
| **f_log_type** | [**&#39;info&#39; | &#39;error&#39;**]**Array<&#39;info&#39; &#124; &#39;error&#39;>** | Type of log | (optional) defaults to undefined|


### Return type

**ListLogResponse**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List logs |  -  |
|**400** | Resource Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

