# ProjectsApi

All URIs are relative to *https://chaos.qernal.com/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**organisationsProjectsList**](#organisationsprojectslist) | **GET** /organisations/{organisation_id}/projects | Get all projects within an organisation|
|[**projectsCreate**](#projectscreate) | **POST** /projects | Create project|
|[**projectsDelete**](#projectsdelete) | **DELETE** /projects/{project_id} | Delete project|
|[**projectsGet**](#projectsget) | **GET** /projects/{project_id} | Get project|
|[**projectsList**](#projectslist) | **GET** /projects | List projects|
|[**projectsQuotasGet**](#projectsquotasget) | **GET** /projects/{project_id}/quotas/{quota_entity_quota} | Get specific project quota|
|[**projectsQuotasList**](#projectsquotaslist) | **GET** /projects/{project_id}/quotas | List project quotas|
|[**projectsUpdate**](#projectsupdate) | **PUT** /projects/{project_id} | Update project|

# **organisationsProjectsList**
> Array<Project> organisationsProjectsList()

Get all the projects linked to a specific organisation

### Example

```typescript
import {
    ProjectsApi,
    Configuration,
    OrganisationsListPageParameter
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let organisation_id: string; //Organisation ID reference (default to undefined)
let page: OrganisationsListPageParameter; //Query parameters for pagination (optional) (default to undefined)
let f_name: string; //Filter resource on name, if the value ends in an asterix it will be treated as a partial search otherwise, it\'ll be an exact match  (optional) (default to undefined)

const { status, data } = await apiInstance.organisationsProjectsList(
    organisation_id,
    page,
    f_name
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **organisation_id** | [**string**] | Organisation ID reference | defaults to undefined|
| **page** | **OrganisationsListPageParameter** | Query parameters for pagination | (optional) defaults to undefined|
| **f_name** | [**string**] | Filter resource on name, if the value ends in an asterix it will be treated as a partial search otherwise, it\&#39;ll be an exact match  | (optional) defaults to undefined|


### Return type

**Array<Project>**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List projects |  * Pagination-Total-Count -  <br>  * Pagination-Page-Size -  <br>  * Pagination-Page-After -  <br>  * Pagination-Page-Before -  <br>  * Pagination-Total-Pages -  <br>  * Link -  <br>  |
|**404** | Resource Not Found |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsCreate**
> Project projectsCreate()

Create a new project

### Example

```typescript
import {
    ProjectsApi,
    Configuration,
    ProjectBody
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let ProjectBody: ProjectBody; //Create/Update any field (optional)

const { status, data } = await apiInstance.projectsCreate(
    ProjectBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ProjectBody** | **ProjectBody**| Create/Update any field | |


### Return type

**Project**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Get project |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |
|**403** | Unauthorised |  -  |
|**409** | Resource Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsDelete**
> DeletedResponse projectsDelete()

Delete project, this will also delete all the resources within the project

### Example

```typescript
import {
    ProjectsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)

const { status, data } = await apiInstance.projectsDelete(
    project_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project_id** | [**string**] | Project ID reference | defaults to undefined|


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

# **projectsGet**
> Project projectsGet()

Get a specific project

### Example

```typescript
import {
    ProjectsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)

const { status, data } = await apiInstance.projectsGet(
    project_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project_id** | [**string**] | Project ID reference | defaults to undefined|


### Return type

**Project**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get project |  -  |
|**404** | Resource Not Found |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsList**
> Array<Project> projectsList()

Get all projects for this user, paginated

### Example

```typescript
import {
    ProjectsApi,
    Configuration,
    OrganisationsListPageParameter
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let page: OrganisationsListPageParameter; //Query parameters for pagination (optional) (default to undefined)
let f_name: string; //Filter resource on name, if the value ends in an asterix it will be treated as a partial search otherwise, it\'ll be an exact match  (optional) (default to undefined)

const { status, data } = await apiInstance.projectsList(
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

**Array<Project>**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List projects |  * Pagination-Total-Count -  <br>  * Pagination-Page-Size -  <br>  * Pagination-Page-After -  <br>  * Pagination-Page-Before -  <br>  * Pagination-Total-Pages -  <br>  * Link -  <br>  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsQuotasGet**
> Array<Quota> projectsQuotasGet()

Get a specific quota for a project

### Example

```typescript
import {
    ProjectsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let quota_entity_quota: string; // (default to undefined)

const { status, data } = await apiInstance.projectsQuotasGet(
    project_id,
    quota_entity_quota
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project_id** | [**string**] | Project ID reference | defaults to undefined|
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

# **projectsQuotasList**
> Array<Quota> projectsQuotasList()

Get the quotas for a project

### Example

```typescript
import {
    ProjectsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)

const { status, data } = await apiInstance.projectsQuotasList(
    project_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project_id** | [**string**] | Project ID reference | defaults to undefined|


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

# **projectsUpdate**
> Project projectsUpdate()

Update project

### Example

```typescript
import {
    ProjectsApi,
    Configuration,
    ProjectBodyPatch
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new ProjectsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let ProjectBodyPatch: ProjectBodyPatch; //Update any field (optional)

const { status, data } = await apiInstance.projectsUpdate(
    project_id,
    ProjectBodyPatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **ProjectBodyPatch** | **ProjectBodyPatch**| Update any field | |
| **project_id** | [**string**] | Project ID reference | defaults to undefined|


### Return type

**Project**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get project |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

