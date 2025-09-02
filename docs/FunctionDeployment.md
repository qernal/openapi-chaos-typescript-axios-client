# FunctionDeployment


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | ID of the deployment | [optional] [default to undefined]
**location** | [**Location**](Location.md) |  | [default to undefined]
**replicas** | [**FunctionReplicas**](FunctionReplicas.md) |  | [default to undefined]

## Example

```typescript
import { FunctionDeployment } from '@qernal/chaos-client';

const instance: FunctionDeployment = {
    id,
    location,
    replicas,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
