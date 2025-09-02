# FunctionEnv

Environment variable for function

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**name** | **string** | Key name | [default to undefined]
**reference** | **string** | Reference for the secret, it\&#39;s split up into 4 main parts; - [1] \&quot;projects:\&quot; - This references which resource type the secret is within - [2] \&quot;0a6b9ff3-6807-4820-b94b-5e1d7efcdd93\&quot; - The project UUID the secret is within - [3] \&quot;MY_SECRET\&quot; - The name of the secret - [4] \&quot;0\&quot; - The revision of the secret to use  | [default to undefined]

## Example

```typescript
import { FunctionEnv } from '@qernal/chaos-client';

const instance: FunctionEnv = {
    name,
    reference,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
