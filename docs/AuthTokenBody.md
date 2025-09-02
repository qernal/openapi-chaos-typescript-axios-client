# AuthTokenBody

API auth token create

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name of token | [default to undefined]
**expiry_duration** | **number** | Token expiration duration in days. 0 - token will never expire | [default to undefined]

## Example

```typescript
import { AuthTokenBody } from '@qernal/chaos-client';

const instance: AuthTokenBody = {
    name,
    expiry_duration,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
