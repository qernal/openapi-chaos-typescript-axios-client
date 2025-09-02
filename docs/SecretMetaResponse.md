# SecretMetaResponse

Secret metadata response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Secret name | [default to undefined]
**type** | [**SecretMetaType**](SecretMetaType.md) |  | [default to undefined]
**payload** | [**SecretMetaResponsePayload**](SecretMetaResponsePayload.md) |  | [optional] [default to undefined]
**revision** | **number** | Secret revision | [default to undefined]
**date** | [**ModelDate**](ModelDate.md) |  | [default to undefined]

## Example

```typescript
import { SecretMetaResponse } from '@qernal/chaos-client';

const instance: SecretMetaResponse = {
    name,
    type,
    payload,
    revision,
    date,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
