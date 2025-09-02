# MetricsApi

All URIs are relative to *https://chaos.qernal.com/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**metricsAggregationsList**](#metricsaggregationslist) | **GET** /metrics/aggregations/{metric_aggregation_type} | Get metrics|

# **metricsAggregationsList**
> MetricsAggregationsList200Response metricsAggregationsList()

Retrieve metrics for a specific project or function. Use the query parameter to request a metrics report.  > Note: Metrics are always returned in a descending order based on the timestamp. 

### Example

```typescript
import {
    MetricsApi,
    Configuration,
    LogsListFTimestampsParameter
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new MetricsApi(configuration);

let metric_aggregation_type: 'httprequests' | 'resourcestats'; //Metric aggregation type, types can be used with either a project or a function filter.  - httprequests: Aggregated HTTP requests - resourcestats: Aggregated resource stats (such as CPU, Memory and Network)  > Note: aggregations cannot return more than 300 data points  (default to undefined)
let f_project: string; //Project uuid reference (optional) (default to undefined)
let f_function: string; //Function uuid reference (optional) (default to undefined)
let f_timestamps: LogsListFTimestampsParameter; //Timestamp restriction for query (optional) (default to undefined)
let f_histogram_interval: number; //Histogram interval (optional) (default to undefined)

const { status, data } = await apiInstance.metricsAggregationsList(
    metric_aggregation_type,
    f_project,
    f_function,
    f_timestamps,
    f_histogram_interval
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **metric_aggregation_type** | [**&#39;httprequests&#39; | &#39;resourcestats&#39;**]**Array<&#39;httprequests&#39; &#124; &#39;resourcestats&#39;>** | Metric aggregation type, types can be used with either a project or a function filter.  - httprequests: Aggregated HTTP requests - resourcestats: Aggregated resource stats (such as CPU, Memory and Network)  &gt; Note: aggregations cannot return more than 300 data points  | defaults to undefined|
| **f_project** | [**string**] | Project uuid reference | (optional) defaults to undefined|
| **f_function** | [**string**] | Function uuid reference | (optional) defaults to undefined|
| **f_timestamps** | **LogsListFTimestampsParameter** | Timestamp restriction for query | (optional) defaults to undefined|
| **f_histogram_interval** | [**number**] | Histogram interval | (optional) defaults to undefined|


### Return type

**MetricsAggregationsList200Response**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Metric aggregation |  -  |
|**400** | Resource Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

