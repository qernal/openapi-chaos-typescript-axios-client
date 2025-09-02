# AuthTokenPatch

API auth token patch

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of token | [optional] [default to undefined]
**expiry_duration** | **number** | Token expiration duration in days. 0 - token will never expire | [optional] [default to undefined]

## Example

```typescript
import { AuthTokenPatch } from '@qernal/chaos-client';

const instance: AuthTokenPatch = {
    name,
    expiry_duration,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
