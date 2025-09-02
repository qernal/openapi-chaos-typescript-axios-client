# HostBody

Host body

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**host** | **string** | Hostname, this can be the root of a domain or a subdomain | [default to undefined]
**certificate** | **string** | The secret reference to the certificate | [default to undefined]
**disabled** | **boolean** | If the host is disabled, then this host won\&#39;t be accessible and so the deployments will not be routable | [default to undefined]

## Example

```typescript
import { HostBody } from '@qernal/chaos-client';

const instance: HostBody = {
    host,
    certificate,
    disabled,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
