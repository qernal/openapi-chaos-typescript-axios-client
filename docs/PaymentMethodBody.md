# PaymentMethodBody

Payment method body

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Name on the payment method | [optional] [default to undefined]
**title** | **string** | Title of the cardholder | [optional] [default to undefined]
**first_name** | **string** | First name of the cardholder | [optional] [default to undefined]
**last_name** | **string** | Last name of the cardholder | [optional] [default to undefined]
**organisation** | **string** | Organisation name, if applicable | [optional] [default to undefined]
**address_line1** | **string** | First line of the address | [optional] [default to undefined]
**address_line2** | **string** | Second line of the address, if applicable | [optional] [default to undefined]
**city** | **string** | City of the address | [optional] [default to undefined]
**county** | **string** | County or state of the address | [optional] [default to undefined]
**postal_code** | **string** | Postal or ZIP code of the address | [optional] [default to undefined]
**country** | **string** | Country of the address (ISO 3166-1 alpha-2 code) | [optional] [default to undefined]
**phone_number** | **string** | Contact phone number associated with the payment method | [optional] [default to undefined]

## Example

```typescript
import { PaymentMethodBody } from '@qernal/chaos-client';

const instance: PaymentMethodBody = {
    name,
    title,
    first_name,
    last_name,
    organisation,
    address_line1,
    address_line2,
    city,
    county,
    postal_code,
    country,
    phone_number,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
