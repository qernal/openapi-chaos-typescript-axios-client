# Location

Location of allowed clusters

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**provider_id** | **string** | UUID of provider to deploy into | [default to undefined]
**continent** | **string** | Deployment continent | [optional] [default to undefined]
**country** | **string** | Deployment country | [optional] [default to undefined]
**city** | **string** | Deployment city | [optional] [default to undefined]

## Example

```typescript
import { Location } from '@qernal/chaos-client';

const instance: Location = {
    provider_id,
    continent,
    country,
    city,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
