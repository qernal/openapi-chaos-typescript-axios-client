# Quota

Quota usage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Quota name | [default to undefined]
**description** | **string** | Quota description | [default to undefined]
**limit** | **number** | Quota limit | [default to undefined]
**usage** | **number** | Quota usage | [default to undefined]
**type** | **string** | Quota type (group) | [default to undefined]

## Example

```typescript
import { Quota } from '@qernal/chaos-client';

const instance: Quota = {
    name,
    description,
    limit,
    usage,
    type,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
