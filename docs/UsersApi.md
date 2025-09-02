# UsersApi

All URIs are relative to *https://chaos.qernal.com/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**usersQuotasGet**](#usersquotasget) | **GET** /users/{user_id}/quotas/{quota_entity_quota} | Get specific user quota|
|[**usersQuotasList**](#usersquotaslist) | **GET** /users/{user_id}/quotas | List user quotas|

# **usersQuotasGet**
> Array<Quota> usersQuotasGet()

Get a specific quota for a user

### Example

```typescript
import {
    UsersApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new UsersApi(configuration);

let user_id: string; //User ID reference (default to undefined)
let quota_entity_quota: string; // (default to undefined)

const { status, data } = await apiInstance.usersQuotasGet(
    user_id,
    quota_entity_quota
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **user_id** | [**string**] | User ID reference | defaults to undefined|
| **quota_entity_quota** | [**string**] |  | defaults to undefined|


### Return type

**Array<Quota>**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List quotas |  -  |
|**404** | Resource Not Found |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **usersQuotasList**
> Array<Quota> usersQuotasList()

Get the quotas for a user

### Example

```typescript
import {
    UsersApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new UsersApi(configuration);

let user_id: string; //User ID reference (default to undefined)

const { status, data } = await apiInstance.usersQuotasList(
    user_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **user_id** | [**string**] | User ID reference | defaults to undefined|


### Return type

**Array<Quota>**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List quotas |  -  |
|**404** | Resource Not Found |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

