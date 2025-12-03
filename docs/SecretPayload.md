# SecretPayload


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**certificate** | **string** | Public TLS certificate | [default to undefined]
**registry** | **string** | Private registry domain/location, when using the private docker hub registry sepcify &#x60;docker.io&#x60; &gt; Without http scheme  | [default to undefined]
**dek** | **string** | Base64 encoded Data Encryption Key (DEK) | [default to undefined]

## Example

```typescript
import { SecretPayload } from '@qernal/chaos-client';

const instance: SecretPayload = {
    certificate,
    registry,
    dek,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
