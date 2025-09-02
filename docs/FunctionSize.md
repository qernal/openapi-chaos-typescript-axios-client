# FunctionSize

Size of function, required CPU and Memory

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**cpu** | **number** | CPU in 0.1 vCPU increments, for a whole vCPU specify 1024 Must be in multiples of 128, with the same multiplier as memory from the base  | [default to undefined]
**memory** | **number** | Memory in 128 MB increments, values are integer always in MB Must be in multiples of 128, with the same multiplier as CPU from the base  | [default to undefined]

## Example

```typescript
import { FunctionSize } from '@qernal/chaos-client';

const instance: FunctionSize = {
    cpu,
    memory,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
