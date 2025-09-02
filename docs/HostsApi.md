# HostsApi

All URIs are relative to *https://chaos.qernal.com/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**projectsHostsCreate**](#projectshostscreate) | **POST** /projects/{project_id}/hosts | Create host for project|
|[**projectsHostsDelete**](#projectshostsdelete) | **DELETE** /projects/{project_id}/hosts/{hostname} | Delete specific host by hostname|
|[**projectsHostsGet**](#projectshostsget) | **GET** /projects/{project_id}/hosts/{hostname} | Get specific host by hostname|
|[**projectsHostsList**](#projectshostslist) | **GET** /projects/{project_id}/hosts | List hosts for project|
|[**projectsHostsUpdate**](#projectshostsupdate) | **PUT** /projects/{project_id}/hosts/{hostname} | Update specific host by hostname|
|[**projectsHostsVerifyCreate**](#projectshostsverifycreate) | **POST** /projects/{project_id}/hosts/{hostname}/verify | Schedule host verification task|

# **projectsHostsCreate**
> Host projectsHostsCreate(HostBody)

Assign a host/domain to a project - hosts are globally unique and require verification, so a host cannot be assigned to multiple projects.  A host can be a valid domain, either a root domain or a subdomain. 

### Example

```typescript
import {
    HostsApi,
    Configuration,
    HostBody
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new HostsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let HostBody: HostBody; //

const { status, data } = await apiInstance.projectsHostsCreate(
    project_id,
    HostBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **HostBody** | **HostBody**|  | |
| **project_id** | [**string**] | Project ID reference | defaults to undefined|


### Return type

**Host**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Porject host |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |
|**409** | Resource Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsHostsDelete**
> DeletedResponse projectsHostsDelete()


### Example

```typescript
import {
    HostsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new HostsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let hostname: string; //Hostname (default to undefined)

const { status, data } = await apiInstance.projectsHostsDelete(
    project_id,
    hostname
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project_id** | [**string**] | Project ID reference | defaults to undefined|
| **hostname** | [**string**] | Hostname | defaults to undefined|


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

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsHostsGet**
> Host projectsHostsGet()


### Example

```typescript
import {
    HostsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new HostsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let hostname: string; //Hostname (default to undefined)

const { status, data } = await apiInstance.projectsHostsGet(
    project_id,
    hostname
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project_id** | [**string**] | Project ID reference | defaults to undefined|
| **hostname** | [**string**] | Hostname | defaults to undefined|


### Return type

**Host**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Porject host |  -  |
|**404** | Resource Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsHostsList**
> ListHosts projectsHostsList()


### Example

```typescript
import {
    HostsApi,
    Configuration,
    OrganisationsListPageParameter
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new HostsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let page: OrganisationsListPageParameter; //Query parameters for pagination (optional) (default to undefined)

const { status, data } = await apiInstance.projectsHostsList(
    project_id,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project_id** | [**string**] | Project ID reference | defaults to undefined|
| **page** | **OrganisationsListPageParameter** | Query parameters for pagination | (optional) defaults to undefined|


### Return type

**ListHosts**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List of project hosts |  -  |
|**404** | Resource Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsHostsUpdate**
> Host projectsHostsUpdate(HostBodyPatch)


### Example

```typescript
import {
    HostsApi,
    Configuration,
    HostBodyPatch
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new HostsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let hostname: string; //Hostname (default to undefined)
let HostBodyPatch: HostBodyPatch; //

const { status, data } = await apiInstance.projectsHostsUpdate(
    project_id,
    hostname,
    HostBodyPatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **HostBodyPatch** | **HostBodyPatch**|  | |
| **project_id** | [**string**] | Project ID reference | defaults to undefined|
| **hostname** | [**string**] | Hostname | defaults to undefined|


### Return type

**Host**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Porject host |  -  |
|**404** | Resource Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsHostsVerifyCreate**
> Host projectsHostsVerifyCreate()


### Example

```typescript
import {
    HostsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new HostsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let hostname: string; //Hostname (default to undefined)

const { status, data } = await apiInstance.projectsHostsVerifyCreate(
    project_id,
    hostname
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project_id** | [**string**] | Project ID reference | defaults to undefined|
| **hostname** | [**string**] | Hostname | defaults to undefined|


### Return type

**Host**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Porject host |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

