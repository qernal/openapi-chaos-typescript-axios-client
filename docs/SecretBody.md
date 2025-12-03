# SecretBody

Secret body

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Secret name | [default to undefined]
**type** | [**SecretBodyType**](SecretBodyType.md) |  | [default to undefined]
**payload** | [**SecretBodyPayload**](SecretBodyPayload.md) |  | [default to undefined]
**encryption** | **string** | Encryption entity | [default to undefined]

## Example

```typescript
import { SecretBody } from '@qernal/chaos-client';

const instance: SecretBody = {
    name,
    type,
    payload,
    encryption,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
