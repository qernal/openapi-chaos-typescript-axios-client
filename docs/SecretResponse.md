# SecretResponse

Secret response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Secret name | [default to undefined]
**type** | [**SecretCreateType**](SecretCreateType.md) |  | [default to undefined]
**payload** | [**SecretResponsePayload**](SecretResponsePayload.md) |  | [optional] [default to undefined]
**revision** | **number** | Secret revision | [default to undefined]
**date** | [**ModelDate**](ModelDate.md) |  | [default to undefined]

## Example

```typescript
import { SecretResponse } from '@qernal/chaos-client';

const instance: SecretResponse = {
    name,
    type,
    payload,
    revision,
    date,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
