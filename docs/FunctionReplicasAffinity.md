# FunctionReplicasAffinity

Replica strategy

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cluster** | **boolean** | If there are &gt; 1 replica, make sure they\&#39;re on different clusters | [default to undefined]
**cloud** | **boolean** | If there are &gt; 1 replica, make sure they\&#39;re on different clouds | [default to undefined]

## Example

```typescript
import { FunctionReplicasAffinity } from '@qernal/chaos-client';

const instance: FunctionReplicasAffinity = {
    cluster,
    cloud,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
