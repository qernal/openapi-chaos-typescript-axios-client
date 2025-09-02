# LogLog

Log item

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**stream** | **string** | Which log stream | [optional] [default to undefined]
**kind** | **string** | If this was an event on the function or a log line | [optional] [default to undefined]
**labels** | **Array&lt;string&gt;** | An array of labels | [optional] [default to undefined]
**type** | **string** | Log line type | [optional] [default to undefined]
**line** | **string** | Log line | [optional] [default to undefined]
**timestamp** | **string** | The date/time that this log was generated | [optional] [default to undefined]

## Example

```typescript
import { LogLog } from '@qernal/chaos-client';

const instance: LogLog = {
    stream,
    kind,
    labels,
    type,
    line,
    timestamp,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
