# FunctionReplicas

Balancing logic

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**min** | **number** | Minimum number of replicas to have | [default to undefined]
**max** | **number** | Maximum number of replicas to have | [default to undefined]
**affinity** | [**FunctionReplicasAffinity**](FunctionReplicasAffinity.md) |  | [default to undefined]

## Example

```typescript
import { FunctionReplicas } from '@qernal/chaos-client';

const instance: FunctionReplicas = {
    min,
    max,
    affinity,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
