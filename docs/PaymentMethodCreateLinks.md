# PaymentMethodCreateLinks

Links related to the payment method, such as checkout URL

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**checkout** | **string** | URL for the payment method checkout | [optional] [default to undefined]
**created_at** | **string** | Timestamp when the checkout link was created | [optional] [default to undefined]
**expires_at** | **string** | Timestamp when the checkout link expires | [optional] [default to undefined]

## Example

```typescript
import { PaymentMethodCreateLinks } from '@qernal/chaos-client';

const instance: PaymentMethodCreateLinks = {
    checkout,
    created_at,
    expires_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
