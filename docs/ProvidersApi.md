# ProvidersApi

All URIs are relative to *https://chaos.qernal.com/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**providersList**](#providerslist) | **GET** /providers | Get available providers|

# **providersList**
> ListProviderResponse providersList()

Retrieve a list of all providers with their respective deployed regions and cities.

### Example

```typescript
import {
    ProvidersApi,
    Configuration,
    OrganisationsListPageParameter
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new ProvidersApi(configuration);

let page: OrganisationsListPageParameter; //Query parameters for pagination (optional) (default to undefined)

const { status, data } = await apiInstance.providersList(
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | **OrganisationsListPageParameter** | Query parameters for pagination | (optional) defaults to undefined|


### Return type

**ListProviderResponse**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List providers |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

