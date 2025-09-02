# TokensApi

All URIs are relative to *https://chaos.qernal.com/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**authTokensCreate**](#authtokenscreate) | **POST** /auth/tokens | Create new auth token|
|[**authTokensDelete**](#authtokensdelete) | **DELETE** /auth/tokens/{token_id} | Delete token|
|[**authTokensGet**](#authtokensget) | **GET** /auth/tokens/{token_id} | Get token information|
|[**authTokensList**](#authtokenslist) | **GET** /auth/tokens | List all user auth tokens|
|[**authTokensUpdate**](#authtokensupdate) | **PUT** /auth/tokens/{token_id} | Update token|

# **authTokensCreate**
> AuthToken authTokensCreate(AuthTokenBody)

Create new auth token for use with the CLI and TF Provider  ### Warning The `token` field is only shown once and can\'t be retrieved again without generating a new token. Securely save this once the response has been received. 

### Example

```typescript
import {
    TokensApi,
    Configuration,
    AuthTokenBody
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new TokensApi(configuration);

let AuthTokenBody: AuthTokenBody; //

const { status, data } = await apiInstance.authTokensCreate(
    AuthTokenBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **AuthTokenBody** | **AuthTokenBody**|  | |


### Return type

**AuthToken**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Generated token response |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authTokensDelete**
> DeletedResponse authTokensDelete()


### Example

```typescript
import {
    TokensApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new TokensApi(configuration);

let token_id: string; //Token ID reference (default to undefined)

const { status, data } = await apiInstance.authTokensDelete(
    token_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **token_id** | [**string**] | Token ID reference | defaults to undefined|


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

# **authTokensGet**
> AuthTokenMeta authTokensGet()


### Example

```typescript
import {
    TokensApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new TokensApi(configuration);

let token_id: string; //Token ID reference (default to undefined)

const { status, data } = await apiInstance.authTokensGet(
    token_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **token_id** | [**string**] | Token ID reference | defaults to undefined|


### Return type

**AuthTokenMeta**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Token meta information |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authTokensList**
> ListAuthTokens authTokensList()


### Example

```typescript
import {
    TokensApi,
    Configuration,
    OrganisationsListPageParameter
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new TokensApi(configuration);

let page: OrganisationsListPageParameter; //Query parameters for pagination (optional) (default to undefined)

const { status, data } = await apiInstance.authTokensList(
    page
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **page** | **OrganisationsListPageParameter** | Query parameters for pagination | (optional) defaults to undefined|


### Return type

**ListAuthTokens**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List of auth token meta |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **authTokensUpdate**
> AuthToken authTokensUpdate(AuthTokenPatch)


### Example

```typescript
import {
    TokensApi,
    Configuration,
    AuthTokenPatch
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new TokensApi(configuration);

let token_id: string; //Token ID reference (default to undefined)
let AuthTokenPatch: AuthTokenPatch; //

const { status, data } = await apiInstance.authTokensUpdate(
    token_id,
    AuthTokenPatch
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **AuthTokenPatch** | **AuthTokenPatch**|  | |
| **token_id** | [**string**] | Token ID reference | defaults to undefined|


### Return type

**AuthToken**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Generated token response |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

