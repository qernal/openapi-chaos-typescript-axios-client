# SecretCreatePayload

Payload for secret

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**registry** | **string** | Private registry domain/location, when using the private docker hub registry sepcify &#x60;docker.io&#x60; &gt; Without http scheme  | [default to undefined]
**registry_value** | **string** | Token used for auth to the registry | [default to undefined]
**environment_value** | **string** | Encrypted environment value | [default to undefined]
**certificate** | **string** | Public certificate | [default to undefined]
**certificate_value** | **string** | Encrypted certificate private key | [default to undefined]

## Example

```typescript
import { SecretCreatePayload } from '@qernal/chaos-client';

const instance: SecretCreatePayload = {
    registry,
    registry_value,
    environment_value,
    certificate,
    certificate_value,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
