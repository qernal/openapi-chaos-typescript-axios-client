# SecretBodyPatch

Secret body patch fields

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**type** | [**SecretCreateType**](SecretCreateType.md) |  | [default to undefined]
**payload** | [**SecretCreatePayload**](SecretCreatePayload.md) |  | [default to undefined]
**encryption** | **string** | Encryption entity | [default to undefined]

## Example

```typescript
import { SecretBodyPatch } from '@qernal/chaos-client';

const instance: SecretBodyPatch = {
    type,
    payload,
    encryption,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
