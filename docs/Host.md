# Host

Host response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Host id | [default to undefined]
**host** | **string** | Hostname, this can be the root of a domain or a subdomain | [default to undefined]
**certificate** | **string** | The secret reference to the certificate | [optional] [default to undefined]
**project_id** | **string** | Project ID this is attached to | [default to undefined]
**read_only** | **boolean** | If the host is read only and cannot be removed, primarily used for *.qrnl.app domains | [default to undefined]
**disabled** | **boolean** | If the host is disabled, then this host won\&#39;t be accessible and so the deployments will not be routable | [default to undefined]
**txt_verification** | **string** | TXT record of host to verify ownership - if this record is removed, it may become unverified as this is checked periodically to continually verify ownership | [default to undefined]
**verified_at** | **string** | UTC datetime when the host was verified (ISO 8601 date format). | [optional] [default to undefined]
**date** | [**ModelDate**](ModelDate.md) |  | [default to undefined]
**verification_status** | [**HostVerificationStatus**](HostVerificationStatus.md) |  | [default to undefined]

## Example

```typescript
import { Host } from '@qernal/chaos-client';

const instance: Host = {
    id,
    host,
    certificate,
    project_id,
    read_only,
    disabled,
    txt_verification,
    verified_at,
    date,
    verification_status,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
