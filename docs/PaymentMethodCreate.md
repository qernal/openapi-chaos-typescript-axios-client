# PaymentMethodCreate

Payment method create response

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**payment_method_id** | **string** | Unique identifier for the payment method | [optional] [default to undefined]
**billing_account_id** | **string** | Unique identifier for the billing account | [optional] [default to undefined]
**name** | **string** | Name on the payment method | [optional] [default to undefined]
**description** | **string** | Description of this order (e.g. payment authorisation) | [optional] [default to undefined]
**state** | **string** | Current state of the payment method | [optional] [default to undefined]
**links** | [**PaymentMethodCreateLinks**](PaymentMethodCreateLinks.md) |  | [optional] [default to undefined]

## Example

```typescript
import { PaymentMethodCreate } from '@qernal/chaos-client';

const instance: PaymentMethodCreate = {
    payment_method_id,
    billing_account_id,
    name,
    description,
    state,
    links,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
