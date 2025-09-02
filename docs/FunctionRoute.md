# FunctionRoute


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**path** | **string** | Can be a regular expression | [default to undefined]
**methods** | **Array&lt;string&gt;** | HTTP Verb(s) for this function | [default to undefined]
**weight** | **number** | The route weight for consideration | [default to undefined]

## Example

```typescript
import { FunctionRoute } from '@qernal/chaos-client';

const instance: FunctionRoute = {
    path,
    methods,
    weight,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
