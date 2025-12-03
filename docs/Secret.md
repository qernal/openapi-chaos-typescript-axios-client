# Secret

Secret response/object

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Secret name | [default to undefined]
**type** | [**SecretType**](SecretType.md) |  | [default to undefined]
**payload** | [**SecretPayload**](SecretPayload.md) |  | [optional] [default to undefined]
**revision** | **number** | Secret revision | [default to undefined]
**date** | [**ModelDate**](ModelDate.md) |  | [default to undefined]

## Example

```typescript
import { Secret } from '@qernal/chaos-client';

const instance: Secret = {
    name,
    type,
    payload,
    revision,
    date,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
