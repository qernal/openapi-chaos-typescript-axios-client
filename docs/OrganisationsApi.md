# OrganisationsApi

All URIs are relative to *https://chaos.qernal.com/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**organisationsCreate**](#organisationscreate) | **POST** /organisations | Create organisations|
|[**organisationsDelete**](#organisationsdelete) | **DELETE** /organisations/{organisation_id} | Delete an organisation|
|[**organisationsGet**](#organisationsget) | **GET** /organisations/{organisation_id} | Get an organisation|
|[**organisationsList**](#organisationslist) | **GET** /organisations | List organisations|
|[**organisationsQuotasGet**](#organisationsquotasget) | **GET** /organisations/{organisation_id}/quotas/{quota_entity_quota} | Get specific organisation quota|
|[**organisationsQuotasList**](#organisationsquotaslist) | **GET** /organisations/{organisation_id}/quotas | List organisation quotas|
|[**organisationsUpdate**](#organisationsupdate) | **PUT** /organisations/{organisation_id} | Update an organisation|

# **organisationsCreate**
> OrganisationResponse organisationsCreate()

Create an organisation

### Example

```typescript
import {
    OrganisationsApi,
    Configuration,
    OrganisationBody
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new OrganisationsApi(configuration);

let OrganisationBody: OrganisationBody; //Create/Update any field (optional)

const { status, data } = await apiInstance.organisationsCreate(
    OrganisationBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **OrganisationBody** | **OrganisationBody**| Create/Update any field | |


### Return type

**OrganisationResponse**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Get organisation |  -  |
|**400** | Resource Bad Request |  -  |
|**403** | Unauthorised |  -  |
|**409** | Resource Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **organisationsDelete**
> DeletedResponse organisationsDelete()

Delete organisation, this will also delete all the resources within the organisation

### Example

```typescript
import {
    OrganisationsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new OrganisationsApi(configuration);

let organisation_id: string; //Organisation ID reference (default to undefined)

const { status, data } = await apiInstance.organisationsDelete(
    organisation_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **organisation_id** | [**string**] | Organisation ID reference | defaults to undefined|


### Return type

**DeletedResponse**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Resource deleted |  -  |
|**404** | Resource Not Found |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **organisationsGet**
> OrganisationResponse organisationsGet()

Get a single organisation

### Example

```typescript
import {
    OrganisationsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new OrganisationsApi(configuration);

let organisation_id: string; //Organisation ID reference (default to undefined)

const { status, data } = await apiInstance.organisationsGet(
    organisation_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **organisation_id** | [**string**] | Organisation ID reference | defaults to undefined|


### Return type

**OrganisationResponse**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get organisation |  -  |
|**404** | Resource Not Found |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **organisationsList**
> ListOrganisationResponse organisationsList()

List organisations

### Example

```typescript
import {
    OrganisationsApi,
    Configuration,
    OrganisationsListPageParameter
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new OrganisationsApi(configuration);

let page: OrganisationsListPageParameter; //Query parameters for pagination (optional) (default to undefined)
let f_name: string; //Filter resource on name, if the value ends in an asterix it will be treated as a partial search otherwise, it\'ll be an exact match  (optional) (default to undefined)

const { status, data } = await apiInstance.organisationsList(
    page,
    f_name
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | **OrganisationsListPageParameter** | Query parameters for pagination | (optional) defaults to undefined|
| **f_name** | [**string**] | Filter resource on name, if the value ends in an asterix it will be treated as a partial search otherwise, it\&#39;ll be an exact match  | (optional) defaults to undefined|


### Return type

**ListOrganisationResponse**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List organisations |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **organisationsQuotasGet**
> Array<Quota> organisationsQuotasGet()

Get a specific quota for an organisation

### Example

```typescript
import {
    OrganisationsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new OrganisationsApi(configuration);

let organisation_id: string; //Organisation ID reference (default to undefined)
let quota_entity_quota: string; // (default to undefined)

const { status, data } = await apiInstance.organisationsQuotasGet(
    organisation_id,
    quota_entity_quota
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **organisation_id** | [**string**] | Organisation ID reference | defaults to undefined|
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

# **organisationsQuotasList**
> Array<Quota> organisationsQuotasList()

Get the quotas for an organisation

### Example

```typescript
import {
    OrganisationsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new OrganisationsApi(configuration);

let organisation_id: string; //Organisation ID reference (default to undefined)

const { status, data } = await apiInstance.organisationsQuotasList(
    organisation_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **organisation_id** | [**string**] | Organisation ID reference | defaults to undefined|


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

# **organisationsUpdate**
> OrganisationResponse organisationsUpdate()

Update an organisation

### Example

```typescript
import {
    OrganisationsApi,
    Configuration,
    OrganisationBody
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new OrganisationsApi(configuration);

let organisation_id: string; //Organisation ID reference (default to undefined)
let OrganisationBody: OrganisationBody; //Create/Update any field (optional)

const { status, data } = await apiInstance.organisationsUpdate(
    organisation_id,
    OrganisationBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **OrganisationBody** | **OrganisationBody**| Create/Update any field | |
| **organisation_id** | [**string**] | Organisation ID reference | defaults to undefined|


### Return type

**OrganisationResponse**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get organisation |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

