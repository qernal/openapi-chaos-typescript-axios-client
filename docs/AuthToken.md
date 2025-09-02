# AuthToken

API auth token

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Auth token uuid | [default to undefined]
**user_id** | **string** | User | [default to undefined]
**name** | **string** | Name of token | [default to undefined]
**expiry_at** | **string** | When the token expires | [optional] [default to undefined]
**token** | **string** | Combined token required for requesting an access token, this field is only returned once on creation or update (during regeneration). | [optional] [default to undefined]
**date** | [**ModelDate**](ModelDate.md) |  | [default to undefined]

## Example

```typescript
import { AuthToken } from '@qernal/chaos-client';

const instance: AuthToken = {
    id,
    user_id,
    name,
    expiry_at,
    token,
    date,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
