# PaymentMethod

Payment method

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique identifier for the payment method | [optional] [default to undefined]
**billing_account** | **string** | Unique identifier for the billing account | [optional] [default to undefined]
**name** | **string** | Name on the payment method | [optional] [default to undefined]
**state** | **string** | Current state of the payment method | [optional] [default to undefined]
**address** | [**PaymentMethodAddress**](PaymentMethodAddress.md) |  | [optional] [default to undefined]

## Example

```typescript
import { PaymentMethod } from '@qernal/chaos-client';

const instance: PaymentMethod = {
    id,
    billing_account,
    name,
    state,
    address,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
