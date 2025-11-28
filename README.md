## @qernal/chaos-client@1.0.7

This generator creates TypeScript/JavaScript client that utilizes [axios](https://github.com/axios/axios). The generated Node module can be used in the following environments:

Environment
* Node.js
* Webpack
* Browserify

Language level
* ES5 - you must have a Promises/A+ library installed
* ES6

Module system
* CommonJS
* ES6 module system

It can be used in both TypeScript and JavaScript. In TypeScript, the definition will be automatically resolved via `package.json`. ([Reference](https://www.typescriptlang.org/docs/handbook/declaration-files/consumption.html))

### Building

To build and compile the typescript sources to javascript use:
```
npm install
npm run build
```

### Publishing

First build the package then run `npm publish`

### Consuming

navigate to the folder of your consuming project and run one of the following commands.

_published:_

```
npm install @qernal/chaos-client@1.0.7 --save
```

_unPublished (not recommended):_

```
npm install PATH_TO_GENERATED_PACKAGE --save
```

### Documentation for API Endpoints

All URIs are relative to *https://chaos.qernal.com/v1*

Class | Method | HTTP request | Description
------------ | ------------- | ------------- | -------------
*BillingApi* | [**accountsPaymentMethodsCreate**](docs/BillingApi.md#accountspaymentmethodscreate) | **POST** /billing/accounts/{billing_account_id}/payment-methods | Create a new payment method for a billing account
*BillingApi* | [**accountsPaymentMethodsList**](docs/BillingApi.md#accountspaymentmethodslist) | **GET** /billing/accounts/{billing_account_id}/payment-methods | List payment methods for a billing account
*BillingApi* | [**billingAccountsCreate**](docs/BillingApi.md#billingaccountscreate) | **POST** /billing/accounts | Create billing account
*BillingApi* | [**billingAccountsDelete**](docs/BillingApi.md#billingaccountsdelete) | **DELETE** /billing/accounts/{billing_account_id} | Delete billing account
*BillingApi* | [**billingAccountsGet**](docs/BillingApi.md#billingaccountsget) | **GET** /billing/accounts/{billing_account_id} | Get billing account
*BillingApi* | [**billingAccountsList**](docs/BillingApi.md#billingaccountslist) | **GET** /billing/accounts | List billing accounts
*BillingApi* | [**billingAccountsUpdate**](docs/BillingApi.md#billingaccountsupdate) | **PUT** /billing/accounts/{billing_account_id} | Update billing account
*BillingApi* | [**paymentMethodsDelete**](docs/BillingApi.md#paymentmethodsdelete) | **DELETE** /billing/payment-methods/{billing_payment_method_id} | Delete a specific payment method
*BillingApi* | [**paymentMethodsGet**](docs/BillingApi.md#paymentmethodsget) | **GET** /billing/payment-methods/{billing_payment_method_id} | Retrieve metadata for a specific payment method
*BillingApi* | [**paymentMethodsUpdate**](docs/BillingApi.md#paymentmethodsupdate) | **PUT** /billing/payment-methods/{billing_payment_method_id} | Update a specific payment method
*FunctionsApi* | [**functionsCreate**](docs/FunctionsApi.md#functionscreate) | **POST** /functions | Create function
*FunctionsApi* | [**functionsDelete**](docs/FunctionsApi.md#functionsdelete) | **DELETE** /functions/{function_id} | Delete function
*FunctionsApi* | [**functionsGet**](docs/FunctionsApi.md#functionsget) | **GET** /functions/{function_id} | Get function (latest revision)
*FunctionsApi* | [**functionsRevisionsGet**](docs/FunctionsApi.md#functionsrevisionsget) | **GET** /functions/{function_id}/revisions/{function_revision_id} | Get a specific revision of a function
*FunctionsApi* | [**functionsRevisionsList**](docs/FunctionsApi.md#functionsrevisionslist) | **GET** /functions/{function_id}/revisions | List all revisions for a function
*FunctionsApi* | [**functionsUpdate**](docs/FunctionsApi.md#functionsupdate) | **PUT** /functions/{function_id} | Update function
*FunctionsApi* | [**projectsFunctionsList**](docs/FunctionsApi.md#projectsfunctionslist) | **GET** /projects/{project_id}/functions | List all functions within a project
*HostsApi* | [**projectsHostsCreate**](docs/HostsApi.md#projectshostscreate) | **POST** /projects/{project_id}/hosts | Create host for project
*HostsApi* | [**projectsHostsDelete**](docs/HostsApi.md#projectshostsdelete) | **DELETE** /projects/{project_id}/hosts/{hostname} | Delete specific host by hostname
*HostsApi* | [**projectsHostsGet**](docs/HostsApi.md#projectshostsget) | **GET** /projects/{project_id}/hosts/{hostname} | Get specific host by hostname
*HostsApi* | [**projectsHostsList**](docs/HostsApi.md#projectshostslist) | **GET** /projects/{project_id}/hosts | List hosts for project
*HostsApi* | [**projectsHostsUpdate**](docs/HostsApi.md#projectshostsupdate) | **PUT** /projects/{project_id}/hosts/{hostname} | Update specific host by hostname
*HostsApi* | [**projectsHostsVerifyCreate**](docs/HostsApi.md#projectshostsverifycreate) | **POST** /projects/{project_id}/hosts/{hostname}/verify | Schedule host verification task
*LogsApi* | [**logsList**](docs/LogsApi.md#logslist) | **GET** /logs | Get logs
*MetricsApi* | [**metricsAggregationsList**](docs/MetricsApi.md#metricsaggregationslist) | **GET** /metrics/aggregations/{metric_aggregation_type} | Get metrics
*OrganisationsApi* | [**organisationsCreate**](docs/OrganisationsApi.md#organisationscreate) | **POST** /organisations | Create organisations
*OrganisationsApi* | [**organisationsDelete**](docs/OrganisationsApi.md#organisationsdelete) | **DELETE** /organisations/{organisation_id} | Delete an organisation
*OrganisationsApi* | [**organisationsGet**](docs/OrganisationsApi.md#organisationsget) | **GET** /organisations/{organisation_id} | Get an organisation
*OrganisationsApi* | [**organisationsList**](docs/OrganisationsApi.md#organisationslist) | **GET** /organisations | List organisations
*OrganisationsApi* | [**organisationsQuotasGet**](docs/OrganisationsApi.md#organisationsquotasget) | **GET** /organisations/{organisation_id}/quotas/{quota_entity_quota} | Get specific organisation quota
*OrganisationsApi* | [**organisationsQuotasList**](docs/OrganisationsApi.md#organisationsquotaslist) | **GET** /organisations/{organisation_id}/quotas | List organisation quotas
*OrganisationsApi* | [**organisationsUpdate**](docs/OrganisationsApi.md#organisationsupdate) | **PUT** /organisations/{organisation_id} | Update an organisation
*ProjectsApi* | [**organisationsProjectsList**](docs/ProjectsApi.md#organisationsprojectslist) | **GET** /organisations/{organisation_id}/projects | Get all projects within an organisation
*ProjectsApi* | [**projectsCreate**](docs/ProjectsApi.md#projectscreate) | **POST** /projects | Create project
*ProjectsApi* | [**projectsDelete**](docs/ProjectsApi.md#projectsdelete) | **DELETE** /projects/{project_id} | Delete project
*ProjectsApi* | [**projectsGet**](docs/ProjectsApi.md#projectsget) | **GET** /projects/{project_id} | Get project
*ProjectsApi* | [**projectsList**](docs/ProjectsApi.md#projectslist) | **GET** /projects | List projects
*ProjectsApi* | [**projectsQuotasGet**](docs/ProjectsApi.md#projectsquotasget) | **GET** /projects/{project_id}/quotas/{quota_entity_quota} | Get specific project quota
*ProjectsApi* | [**projectsQuotasList**](docs/ProjectsApi.md#projectsquotaslist) | **GET** /projects/{project_id}/quotas | List project quotas
*ProjectsApi* | [**projectsUpdate**](docs/ProjectsApi.md#projectsupdate) | **PUT** /projects/{project_id} | Update project
*ProvidersApi* | [**providersList**](docs/ProvidersApi.md#providerslist) | **GET** /providers | Get available providers
*QuotasApi* | [**organisationsQuotasGet**](docs/QuotasApi.md#organisationsquotasget) | **GET** /organisations/{organisation_id}/quotas/{quota_entity_quota} | Get specific organisation quota
*QuotasApi* | [**organisationsQuotasList**](docs/QuotasApi.md#organisationsquotaslist) | **GET** /organisations/{organisation_id}/quotas | List organisation quotas
*QuotasApi* | [**projectsQuotasGet**](docs/QuotasApi.md#projectsquotasget) | **GET** /projects/{project_id}/quotas/{quota_entity_quota} | Get specific project quota
*QuotasApi* | [**projectsQuotasList**](docs/QuotasApi.md#projectsquotaslist) | **GET** /projects/{project_id}/quotas | List project quotas
*QuotasApi* | [**usersQuotasGet**](docs/QuotasApi.md#usersquotasget) | **GET** /users/{user_id}/quotas/{quota_entity_quota} | Get specific user quota
*QuotasApi* | [**usersQuotasList**](docs/QuotasApi.md#usersquotaslist) | **GET** /users/{user_id}/quotas | List user quotas
*SecretsApi* | [**projectsSecretsCreate**](docs/SecretsApi.md#projectssecretscreate) | **POST** /projects/{project_id}/secrets | Create project secret
*SecretsApi* | [**projectsSecretsDelete**](docs/SecretsApi.md#projectssecretsdelete) | **DELETE** /projects/{project_id}/secrets/{secret_name} | Delete project secret
*SecretsApi* | [**projectsSecretsGet**](docs/SecretsApi.md#projectssecretsget) | **GET** /projects/{project_id}/secrets/{secret_name} | Get project secret
*SecretsApi* | [**projectsSecretsList**](docs/SecretsApi.md#projectssecretslist) | **GET** /projects/{project_id}/secrets | List project secrets of a specific type
*SecretsApi* | [**projectsSecretsUpdate**](docs/SecretsApi.md#projectssecretsupdate) | **PUT** /projects/{project_id}/secrets/{secret_name} | Update project secret
*TokensApi* | [**authTokensCreate**](docs/TokensApi.md#authtokenscreate) | **POST** /auth/tokens | Create new auth token
*TokensApi* | [**authTokensDelete**](docs/TokensApi.md#authtokensdelete) | **DELETE** /auth/tokens/{token_id} | Delete token
*TokensApi* | [**authTokensGet**](docs/TokensApi.md#authtokensget) | **GET** /auth/tokens/{token_id} | Get token information
*TokensApi* | [**authTokensList**](docs/TokensApi.md#authtokenslist) | **GET** /auth/tokens | List all user auth tokens
*TokensApi* | [**authTokensUpdate**](docs/TokensApi.md#authtokensupdate) | **PUT** /auth/tokens/{token_id} | Update token
*UsersApi* | [**usersQuotasGet**](docs/UsersApi.md#usersquotasget) | **GET** /users/{user_id}/quotas/{quota_entity_quota} | Get specific user quota
*UsersApi* | [**usersQuotasList**](docs/UsersApi.md#usersquotaslist) | **GET** /users/{user_id}/quotas | List user quotas


### Documentation For Models

 - [AuthToken](docs/AuthToken.md)
 - [AuthTokenBody](docs/AuthTokenBody.md)
 - [AuthTokenMeta](docs/AuthTokenMeta.md)
 - [AuthTokenPatch](docs/AuthTokenPatch.md)
 - [BadRequestResponse](docs/BadRequestResponse.md)
 - [BadRequestResponseFields](docs/BadRequestResponseFields.md)
 - [BillingAccount](docs/BillingAccount.md)
 - [BillingAccountBody](docs/BillingAccountBody.md)
 - [ConflictResponse](docs/ConflictResponse.md)
 - [DeletedResponse](docs/DeletedResponse.md)
 - [Function](docs/Function.md)
 - [FunctionBody](docs/FunctionBody.md)
 - [FunctionCompliance](docs/FunctionCompliance.md)
 - [FunctionDeployment](docs/FunctionDeployment.md)
 - [FunctionDeploymentBody](docs/FunctionDeploymentBody.md)
 - [FunctionEnv](docs/FunctionEnv.md)
 - [FunctionReplicas](docs/FunctionReplicas.md)
 - [FunctionReplicasAffinity](docs/FunctionReplicasAffinity.md)
 - [FunctionRoute](docs/FunctionRoute.md)
 - [FunctionScaling](docs/FunctionScaling.md)
 - [FunctionSize](docs/FunctionSize.md)
 - [FunctionType](docs/FunctionType.md)
 - [Host](docs/Host.md)
 - [HostBody](docs/HostBody.md)
 - [HostBodyPatch](docs/HostBodyPatch.md)
 - [HostVerificationStatus](docs/HostVerificationStatus.md)
 - [ListFunction](docs/ListFunction.md)
 - [ListLogResponse](docs/ListLogResponse.md)
 - [ListProviderResponse](docs/ListProviderResponse.md)
 - [Location](docs/Location.md)
 - [Log](docs/Log.md)
 - [LogLog](docs/LogLog.md)
 - [LogsListFTimestampsParameter](docs/LogsListFTimestampsParameter.md)
 - [MetricHttpAggregation](docs/MetricHttpAggregation.md)
 - [MetricHttpAggregationHttpCodes](docs/MetricHttpAggregationHttpCodes.md)
 - [MetricHttpAggregationHttpCodesBucketsInner](docs/MetricHttpAggregationHttpCodesBucketsInner.md)
 - [MetricHttpAggregationHttpCodesBucketsInnerHistogram](docs/MetricHttpAggregationHttpCodesBucketsInnerHistogram.md)
 - [MetricResourceAggregation](docs/MetricResourceAggregation.md)
 - [MetricResourceAggregationResources](docs/MetricResourceAggregationResources.md)
 - [MetricResourceAggregationResourcesBucketsInner](docs/MetricResourceAggregationResourcesBucketsInner.md)
 - [MetricResourceAggregationResourcesBucketsInnerHistogram](docs/MetricResourceAggregationResourcesBucketsInnerHistogram.md)
 - [MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInner](docs/MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInner.md)
 - [MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInnerCounter](docs/MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInnerCounter.md)
 - [MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInnerGauge](docs/MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInnerGauge.md)
 - [MetricsAggregationsList200Response](docs/MetricsAggregationsList200Response.md)
 - [ModelDate](docs/ModelDate.md)
 - [NotFoundResponse](docs/NotFoundResponse.md)
 - [Organisation](docs/Organisation.md)
 - [OrganisationBody](docs/OrganisationBody.md)
 - [OrganisationBodyPatch](docs/OrganisationBodyPatch.md)
 - [OrganisationsListPageParameter](docs/OrganisationsListPageParameter.md)
 - [PaginationLinks](docs/PaginationLinks.md)
 - [PaginationMeta](docs/PaginationMeta.md)
 - [PaymentMethod](docs/PaymentMethod.md)
 - [PaymentMethodAddress](docs/PaymentMethodAddress.md)
 - [PaymentMethodBody](docs/PaymentMethodBody.md)
 - [PaymentMethodCreate](docs/PaymentMethodCreate.md)
 - [PaymentMethodCreateLinks](docs/PaymentMethodCreateLinks.md)
 - [Project](docs/Project.md)
 - [ProjectBody](docs/ProjectBody.md)
 - [ProjectBodyPatch](docs/ProjectBodyPatch.md)
 - [Provider](docs/Provider.md)
 - [ProviderLocations](docs/ProviderLocations.md)
 - [Quota](docs/Quota.md)
 - [Secret](docs/Secret.md)
 - [SecretBody](docs/SecretBody.md)
 - [SecretBodyPatch](docs/SecretBodyPatch.md)
 - [SecretCertificate](docs/SecretCertificate.md)
 - [SecretCreatePayload](docs/SecretCreatePayload.md)
 - [SecretCreateType](docs/SecretCreateType.md)
 - [SecretEnvironment](docs/SecretEnvironment.md)
 - [SecretMeta](docs/SecretMeta.md)
 - [SecretMetaCertificatePayload](docs/SecretMetaCertificatePayload.md)
 - [SecretMetaDek](docs/SecretMetaDek.md)
 - [SecretMetaPayload](docs/SecretMetaPayload.md)
 - [SecretMetaRegistryPayload](docs/SecretMetaRegistryPayload.md)
 - [SecretMetaType](docs/SecretMetaType.md)
 - [SecretPayload](docs/SecretPayload.md)
 - [SecretRegistry](docs/SecretRegistry.md)
 - [UnauthorisedResponse](docs/UnauthorisedResponse.md)


<a id="documentation-for-authorization"></a>
## Documentation For Authorization


Authentication schemes defined for the API:
<a id="token"></a>
### token

- **Type**: Bearer authentication

<a id="cookie"></a>
### cookie

- **Type**: API key
- **API key parameter name**: qernal_kratos_session
- **Location**: 

