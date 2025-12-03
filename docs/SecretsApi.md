# SecretsApi

All URIs are relative to *https://chaos.qernal.com/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**projectsSecretsCreate**](#projectssecretscreate) | **POST** /projects/{project_id}/secrets | Create project secret|
|[**projectsSecretsDelete**](#projectssecretsdelete) | **DELETE** /projects/{project_id}/secrets/{secret_name} | Delete project secret|
|[**projectsSecretsGet**](#projectssecretsget) | **GET** /projects/{project_id}/secrets/{secret_name} | Get project secret|
|[**projectsSecretsList**](#projectssecretslist) | **GET** /projects/{project_id}/secrets | List project secrets of a specific type|
|[**projectsSecretsUpdate**](#projectssecretsupdate) | **PUT** /projects/{project_id}/secrets/{secret_name} | Update project secret|

# **projectsSecretsCreate**
> Secret projectsSecretsCreate(SecretBody)

Create a new project secret

### Example

```typescript
import {
    SecretsApi,
    Configuration,
    SecretBody
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new SecretsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let SecretBody: SecretBody; //Create/Update any field  The example generated may only be for one of the secret types, look towards the payload section of the schema for further fields, values and examples. 

const { status, data } = await apiInstance.projectsSecretsCreate(
    project_id,
    SecretBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **SecretBody** | **SecretBody**| Create/Update any field  The example generated may only be for one of the secret types, look towards the payload section of the schema for further fields, values and examples.  | |
| **project_id** | [**string**] | Project ID reference | defaults to undefined|


### Return type

**Secret**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Get secret |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |
|**403** | Unauthorised |  -  |
|**409** | Resource Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsSecretsDelete**
> DeletedResponse projectsSecretsDelete()

Delete project secret, if the secret is still linked to an active/deployed function - it cannot be removed

### Example

```typescript
import {
    SecretsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new SecretsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let secret_name: string; //Unique secret name (default to undefined)

const { status, data } = await apiInstance.projectsSecretsDelete(
    project_id,
    secret_name
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project_id** | [**string**] | Project ID reference | defaults to undefined|
| **secret_name** | [**string**] | Unique secret name | defaults to undefined|


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

# **projectsSecretsGet**
> Secret projectsSecretsGet()

Get a specific project

### Example

```typescript
import {
    SecretsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new SecretsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let secret_name: string; //Unique secret name (default to undefined)

const { status, data } = await apiInstance.projectsSecretsGet(
    project_id,
    secret_name
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project_id** | [**string**] | Project ID reference | defaults to undefined|
| **secret_name** | [**string**] | Unique secret name | defaults to undefined|


### Return type

**Secret**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get secret |  -  |
|**404** | Resource Not Found |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsSecretsList**
> Array<Secret> projectsSecretsList()

List project secrets of a specific type

### Example

```typescript
import {
    SecretsApi,
    Configuration,
    OrganisationsListPageParameter
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new SecretsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let page: OrganisationsListPageParameter; //Query parameters for pagination (optional) (default to undefined)
let secret_type: SecretType; //Type of secret to filter on (optional) (default to undefined)

const { status, data } = await apiInstance.projectsSecretsList(
    project_id,
    page,
    secret_type
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **project_id** | [**string**] | Project ID reference | defaults to undefined|
| **page** | **OrganisationsListPageParameter** | Query parameters for pagination | (optional) defaults to undefined|
| **secret_type** | **SecretType** | Type of secret to filter on | (optional) defaults to undefined|


### Return type

**Array<Secret>**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List secrets |  * Pagination-Total-Count -  <br>  * Pagination-Page-Size -  <br>  * Pagination-Page-After -  <br>  * Pagination-Page-Before -  <br>  * Pagination-Total-Pages -  <br>  * Link -  <br>  |
|**404** | Resource Not Found |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsSecretsUpdate**
> Secret projectsSecretsUpdate(SecretBodyPatch)

Update project

### Example

```typescript
import {
    SecretsApi,
    Configuration,
    SecretBodyPatch
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new SecretsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let secret_name: string; //Unique secret name (default to undefined)
let SecretBodyPatch: SecretBodyPatch; //Update any field

const { status, data } = await apiInstance.projectsSecretsUpdate(
    project_id,
    secret_name,
    SecretBodyPatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **SecretBodyPatch** | **SecretBodyPatch**| Update any field | |
| **project_id** | [**string**] | Project ID reference | defaults to undefined|
| **secret_name** | [**string**] | Unique secret name | defaults to undefined|


### Return type

**Secret**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get secret |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

