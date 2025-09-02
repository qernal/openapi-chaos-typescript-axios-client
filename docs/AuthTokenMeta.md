# AuthTokenMeta

API auth token meta

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** |  | [default to undefined]
**user_id** | **string** | User | [default to undefined]
**name** | **string** | Name of token | [default to undefined]
**expiry_at** | **string** |  | [optional] [default to undefined]
**date** | [**ModelDate**](ModelDate.md) |  | [default to undefined]

## Example

```typescript
import { AuthTokenMeta } from '@qernal/chaos-client';

const instance: AuthTokenMeta = {
    id,
    user_id,
    name,
    expiry_at,
    date,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
