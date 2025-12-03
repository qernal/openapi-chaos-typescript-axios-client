# SecretBodyRegistryPayload

Encrypted private container registry, `type: registry`

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**registry** | **string** | Private registry domain/location, when using the private docker hub registry sepcify &#x60;docker.io&#x60; &gt; Without http scheme  | [default to undefined]
**registry_value** | **string** | Token used for auth to the registry | [default to undefined]

## Example

```typescript
import { SecretBodyRegistryPayload } from '@qernal/chaos-client';

const instance: SecretBodyRegistryPayload = {
    registry,
    registry_value,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
