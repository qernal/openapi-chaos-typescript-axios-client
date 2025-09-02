# FunctionsApi

All URIs are relative to *https://chaos.qernal.com/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**functionsCreate**](#functionscreate) | **POST** /functions | Create function|
|[**functionsDelete**](#functionsdelete) | **DELETE** /functions/{function_id} | Delete function|
|[**functionsGet**](#functionsget) | **GET** /functions/{function_id} | Get function (latest revision)|
|[**functionsRevisionsGet**](#functionsrevisionsget) | **GET** /functions/{function_id}/revisions/{function_revision_id} | Get a specific revision of a function|
|[**functionsRevisionsList**](#functionsrevisionslist) | **GET** /functions/{function_id}/revisions | List all revisions for a function|
|[**functionsUpdate**](#functionsupdate) | **PUT** /functions/{function_id} | Update function|
|[**projectsFunctionsList**](#projectsfunctionslist) | **GET** /projects/{project_id}/functions | List all functions within a project|

# **functionsCreate**
> Function functionsCreate(FunctionBody)

Create a new function

### Example

```typescript
import {
    FunctionsApi,
    Configuration,
    FunctionBody
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new FunctionsApi(configuration);

let FunctionBody: FunctionBody; //Create/Update any field

const { status, data } = await apiInstance.functionsCreate(
    FunctionBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **FunctionBody** | **FunctionBody**| Create/Update any field | |


### Return type

**Function**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Get specific function |  -  |
|**400** | Resource Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **functionsDelete**
> DeletedResponse functionsDelete()

Delete a function (and all revisions)

### Example

```typescript
import {
    FunctionsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new FunctionsApi(configuration);

let function_id: string; //Function ID reference (default to undefined)

const { status, data } = await apiInstance.functionsDelete(
    function_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **function_id** | [**string**] | Function ID reference | defaults to undefined|


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

# **functionsGet**
> Function functionsGet()

Get a specific function (latest revision)

### Example

```typescript
import {
    FunctionsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new FunctionsApi(configuration);

let function_id: string; //Function ID reference (default to undefined)

const { status, data } = await apiInstance.functionsGet(
    function_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **function_id** | [**string**] | Function ID reference | defaults to undefined|


### Return type

**Function**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get specific function |  -  |
|**404** | Resource Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **functionsRevisionsGet**
> Function functionsRevisionsGet()

Get a specific revision of a function

### Example

```typescript
import {
    FunctionsApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new FunctionsApi(configuration);

let function_id: string; //Function ID reference (default to undefined)
let function_revision_id: string; //Function revision ID reference (default to undefined)

const { status, data } = await apiInstance.functionsRevisionsGet(
    function_id,
    function_revision_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **function_id** | [**string**] | Function ID reference | defaults to undefined|
| **function_revision_id** | [**string**] | Function revision ID reference | defaults to undefined|


### Return type

**Function**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get specific function |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **functionsRevisionsList**
> ListFunction functionsRevisionsList()

List all revisions for a function

### Example

```typescript
import {
    FunctionsApi,
    Configuration,
    OrganisationsListPageParameter
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new FunctionsApi(configuration);

let function_id: string; //Function ID reference (default to undefined)
let page: OrganisationsListPageParameter; //Query parameters for pagination (optional) (default to undefined)

const { status, data } = await apiInstance.functionsRevisionsList(
    function_id,
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **function_id** | [**string**] | Function ID reference | defaults to undefined|
| **page** | **OrganisationsListPageParameter** | Query parameters for pagination | (optional) defaults to undefined|


### Return type

**ListFunction**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List all functions (paginated) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **functionsUpdate**
> Function functionsUpdate(Function)

Update a function (creates a new revision)

### Example

```typescript
import {
    FunctionsApi,
    Configuration,
    Function
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new FunctionsApi(configuration);

let function_id: string; //Function ID reference (default to undefined)
let Function: Function; //Update any field

const { status, data } = await apiInstance.functionsUpdate(
    function_id,
    Function
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **Function** | **Function**| Update any field | |
| **function_id** | [**string**] | Function ID reference | defaults to undefined|


### Return type

**Function**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get specific function |  -  |
|**400** | Resource Bad Request |  -  |
|**404** | Resource Not Found |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **projectsFunctionsList**
> ListFunction projectsFunctionsList()

List all functions

### Example

```typescript
import {
    FunctionsApi,
    Configuration,
    OrganisationsListPageParameter
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new FunctionsApi(configuration);

let project_id: string; //Project ID reference (default to undefined)
let page: OrganisationsListPageParameter; //Query parameters for pagination (optional) (default to undefined)

const { status, data } = await apiInstance.projectsFunctionsList(
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

**ListFunction**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List all functions (paginated) |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

