# BillingAccount

Billing account

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**id** | **string** | Unique identifier for the billing account | [optional] [default to undefined]
**user_id** | **string** | User ID associated with the billing account | [optional] [default to undefined]
**name** | **string** | Name of the billing account | [optional] [default to undefined]
**state** | **string** | Current state of the billing account - new accounts are created with state \&quot;created\&quot; until a card is added | [optional] [default to undefined]
**balance** | **number** | Current balance of the billing account | [optional] [default to undefined]
**created_at** | **string** | Timestamp when the billing account was created | [optional] [default to undefined]
**updated_at** | **string** | Timestamp when the billing account was last updated | [optional] [default to undefined]

## Example

```typescript
import { BillingAccount } from '@qernal/chaos-client';

const instance: BillingAccount = {
    id,
    user_id,
    name,
    state,
    balance,
    created_at,
    updated_at,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
