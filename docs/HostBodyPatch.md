# HostBodyPatch

Host body update

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**certificate** | **string** | The secret reference to the certificate | [optional] [default to undefined]
**disabled** | **boolean** | If the host is disabled, then this host won\&#39;t be accessible and so the deployments will not be routable | [optional] [default to undefined]

## Example

```typescript
import { HostBodyPatch } from '@qernal/chaos-client';

const instance: HostBodyPatch = {
    certificate,
    disabled,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
