# Function

Function

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | ID of the function | [default to undefined]
**project_id** | **string** | ID of the project this function belongs to | [default to undefined]
**version** | **string** | Function spec version | [default to undefined]
**name** | **string** | Name of the function | [default to undefined]
**description** | **string** | Description of what the function does | [default to undefined]
**image** | **string** | Path to container image | [default to undefined]
**revision** | **string** | Function revision | [default to undefined]
**type** | [**FunctionType**](FunctionType.md) |  | [default to undefined]
**size** | [**FunctionSize**](FunctionSize.md) |  | [default to undefined]
**port** | **number** | Port the application runs on | [default to undefined]
**routes** | [**Array&lt;FunctionRoute&gt;**](FunctionRoute.md) | The public route/path to this function, only applicable to http type functions | [optional] [default to undefined]
**scaling** | [**FunctionScaling**](FunctionScaling.md) |  | [default to undefined]
**deployments** | [**Array&lt;FunctionDeployment&gt;**](FunctionDeployment.md) | List of deployments for this function | [default to undefined]
**secrets** | [**Array&lt;FunctionEnv&gt;**](FunctionEnv.md) | List of environment variables for secrets | [default to undefined]
**compliance** | [**Array&lt;FunctionCompliance&gt;**](FunctionCompliance.md) | Tags to limit deployment | [default to undefined]

## Example

```typescript
import { Function } from '@qernal/chaos-client';

const instance: Function = {
    id,
    project_id,
    version,
    name,
    description,
    image,
    revision,
    type,
    size,
    port,
    routes,
    scaling,
    deployments,
    secrets,
    compliance,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
