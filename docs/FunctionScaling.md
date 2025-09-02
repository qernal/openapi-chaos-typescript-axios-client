# FunctionScaling

Scaling logic

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | **string** | CPU or Memory supported | [default to undefined]
**low** | **number** | For type to drop below before scale down | [default to undefined]
**high** | **number** | For type to go above before scale up | [default to undefined]

## Example

```typescript
import { FunctionScaling } from '@qernal/chaos-client';

const instance: FunctionScaling = {
    type,
    low,
    high,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
