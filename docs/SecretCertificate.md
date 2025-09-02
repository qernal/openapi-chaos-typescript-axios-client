# SecretCertificate

Encrypted SSL private key and plain certificate. Certificate expected in x509 pem format, key expected in pkcs8 or pkcs1 pem format. `type: certificate`

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**certificate** | **string** | Public certificate | [default to undefined]
**certificate_value** | **string** | Encrypted certificate private key | [default to undefined]

## Example

```typescript
import { SecretCertificate } from '@qernal/chaos-client';

const instance: SecretCertificate = {
    certificate,
    certificate_value,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
