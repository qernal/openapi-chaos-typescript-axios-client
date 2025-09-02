# SecretMetaResponsePayload


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**certificate** | **string** | Public SSL certificate | [default to undefined]
**registry** | **string** | Private registry domain/location, when using the private docker hub registry sepcify &#x60;docker.io&#x60; &gt; Without http scheme  | [default to undefined]
**_public** | **string** | Base64 encoded DEK public key | [default to undefined]

## Example

```typescript
import { SecretMetaResponsePayload } from '@qernal/chaos-client';

const instance: SecretMetaResponsePayload = {
    certificate,
    registry,
    _public,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
