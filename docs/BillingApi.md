# BillingApi

All URIs are relative to *https://chaos.qernal.com/v1*

|Method | HTTP request | Description|
|------------- | ------------- | -------------|
|[**accountsPaymentMethodsCreate**](#accountspaymentmethodscreate) | **POST** /billing/accounts/{billing_account_id}/payment-methods | Create a new payment method for a billing account|
|[**accountsPaymentMethodsList**](#accountspaymentmethodslist) | **GET** /billing/accounts/{billing_account_id}/payment-methods | List payment methods for a billing account|
|[**billingAccountsCreate**](#billingaccountscreate) | **POST** /billing/accounts | Create billing account|
|[**billingAccountsDelete**](#billingaccountsdelete) | **DELETE** /billing/accounts/{billing_account_id} | Delete billing account|
|[**billingAccountsGet**](#billingaccountsget) | **GET** /billing/accounts/{billing_account_id} | Get billing account|
|[**billingAccountsList**](#billingaccountslist) | **GET** /billing/accounts | List billing accounts|
|[**billingAccountsUpdate**](#billingaccountsupdate) | **PUT** /billing/accounts/{billing_account_id} | Update billing account|
|[**paymentMethodsDelete**](#paymentmethodsdelete) | **DELETE** /billing/payment-methods/{billing_payment_method_id} | Delete a specific payment method|
|[**paymentMethodsGet**](#paymentmethodsget) | **GET** /billing/payment-methods/{billing_payment_method_id} | Retrieve metadata for a specific payment method|
|[**paymentMethodsUpdate**](#paymentmethodsupdate) | **PUT** /billing/payment-methods/{billing_payment_method_id} | Update a specific payment method|

# **accountsPaymentMethodsCreate**
> PaymentMethodCreate accountsPaymentMethodsCreate(PaymentMethodBody)

Create a new payment method associated with a specific billing account.

### Example

```typescript
import {
    BillingApi,
    Configuration,
    PaymentMethodBody
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new BillingApi(configuration);

let billing_account_id: string; //Billing account ID reference (default to undefined)
let PaymentMethodBody: PaymentMethodBody; //Create/Update any field

const { status, data } = await apiInstance.accountsPaymentMethodsCreate(
    billing_account_id,
    PaymentMethodBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **PaymentMethodBody** | **PaymentMethodBody**| Create/Update any field | |
| **billing_account_id** | [**string**] | Billing account ID reference | defaults to undefined|


### Return type

**PaymentMethodCreate**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Create payment method |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |
|**403** | Unauthorised |  -  |
|**409** | Resource Conflict |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **accountsPaymentMethodsList**
> Array<PaymentMethod> accountsPaymentMethodsList()

Retrieve a list of payment methods associated with a specific billing account.

### Example

```typescript
import {
    BillingApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new BillingApi(configuration);

let billing_account_id: string; //Billing account ID reference (default to undefined)

const { status, data } = await apiInstance.accountsPaymentMethodsList(
    billing_account_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **billing_account_id** | [**string**] | Billing account ID reference | defaults to undefined|


### Return type

**Array<PaymentMethod>**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List payment methods |  -  |
|**404** | Resource Not Found |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **billingAccountsCreate**
> BillingAccount billingAccountsCreate(BillingAccountBody)

Create a new billing account

### Example

```typescript
import {
    BillingApi,
    Configuration,
    BillingAccountBody
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new BillingApi(configuration);

let BillingAccountBody: BillingAccountBody; //Create/Update any field

const { status, data } = await apiInstance.billingAccountsCreate(
    BillingAccountBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **BillingAccountBody** | **BillingAccountBody**| Create/Update any field | |


### Return type

**BillingAccount**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**201** | Get billing account |  -  |
|**400** | Resource Bad Request |  -  |
|**401** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **billingAccountsDelete**
> DeletedResponse billingAccountsDelete()

Delete a specific billing account if it is no longer attached to any organizations or projects and has no outstanding balances or invoice payments.

### Example

```typescript
import {
    BillingApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new BillingApi(configuration);

let billing_account_id: string; //Billing account ID reference (default to undefined)

const { status, data } = await apiInstance.billingAccountsDelete(
    billing_account_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **billing_account_id** | [**string**] | Billing account ID reference | defaults to undefined|


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

# **billingAccountsGet**
> BillingAccount billingAccountsGet()

Get a specific billing account

### Example

```typescript
import {
    BillingApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new BillingApi(configuration);

let billing_account_id: string; //Billing account ID reference (default to undefined)

const { status, data } = await apiInstance.billingAccountsGet(
    billing_account_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **billing_account_id** | [**string**] | Billing account ID reference | defaults to undefined|


### Return type

**BillingAccount**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get billing account |  -  |
|**404** | Resource Not Found |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **billingAccountsList**
> Array<BillingAccount> billingAccountsList()

List all billing accounts for this user, paginated

### Example

```typescript
import {
    BillingApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new BillingApi(configuration);

const { status, data } = await apiInstance.billingAccountsList();
```

### Parameters
This endpoint does not have any parameters.


### Return type

**Array<BillingAccount>**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | List billing accounts |  -  |
|**401** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **billingAccountsUpdate**
> BillingAccount billingAccountsUpdate(BillingAccountBody)

Update the details of a specific billing account.

### Example

```typescript
import {
    BillingApi,
    Configuration,
    BillingAccountBody
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new BillingApi(configuration);

let billing_account_id: string; //Billing account ID reference (default to undefined)
let BillingAccountBody: BillingAccountBody; //Create/Update any field

const { status, data } = await apiInstance.billingAccountsUpdate(
    billing_account_id,
    BillingAccountBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **BillingAccountBody** | **BillingAccountBody**| Create/Update any field | |
| **billing_account_id** | [**string**] | Billing account ID reference | defaults to undefined|


### Return type

**BillingAccount**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get billing account |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **paymentMethodsDelete**
> DeletedResponse paymentMethodsDelete()

Remove a specific payment method entirely if there are no associated resources and no pending partial invoices.

### Example

```typescript
import {
    BillingApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new BillingApi(configuration);

let billing_payment_method_id: string; //Payment method ID reference (default to undefined)

const { status, data } = await apiInstance.paymentMethodsDelete(
    billing_payment_method_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **billing_payment_method_id** | [**string**] | Payment method ID reference | defaults to undefined|


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

# **paymentMethodsGet**
> PaymentMethod paymentMethodsGet()

Get metadata (such as state, active, declined, cancelled, etc.) for a specific payment method.

### Example

```typescript
import {
    BillingApi,
    Configuration
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new BillingApi(configuration);

let billing_payment_method_id: string; //Payment method ID reference (default to undefined)

const { status, data } = await apiInstance.paymentMethodsGet(
    billing_payment_method_id
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **billing_payment_method_id** | [**string**] | Payment method ID reference | defaults to undefined|


### Return type

**PaymentMethod**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: Not defined
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get payment method |  -  |
|**404** | Resource Not Found |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **paymentMethodsUpdate**
> PaymentMethod paymentMethodsUpdate(PaymentMethodBody)

Update the details of a specific payment method.

### Example

```typescript
import {
    BillingApi,
    Configuration,
    PaymentMethodBody
} from '@qernal/chaos-client';

const configuration = new Configuration();
const apiInstance = new BillingApi(configuration);

let billing_payment_method_id: string; //Payment method ID reference (default to undefined)
let PaymentMethodBody: PaymentMethodBody; //Create/Update any field

const { status, data } = await apiInstance.paymentMethodsUpdate(
    billing_payment_method_id,
    PaymentMethodBody
);
```

### Parameters

|Name | Type | Description  | Notes|
|------------- | ------------- | ------------- | -------------|
| **PaymentMethodBody** | **PaymentMethodBody**| Create/Update any field | |
| **billing_payment_method_id** | [**string**] | Payment method ID reference | defaults to undefined|


### Return type

**PaymentMethod**

### Authorization

[cookie](../README.md#cookie), [token](../README.md#token)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
|**200** | Get payment method |  -  |
|**404** | Resource Not Found |  -  |
|**400** | Resource Bad Request |  -  |
|**403** | Unauthorised |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

