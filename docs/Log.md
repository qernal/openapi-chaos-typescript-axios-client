# Log

List of logs

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**container** | **string** | Container ID the log line is for | [optional] [default to undefined]
**_function** | **string** | Function ID the log line is for | [optional] [default to undefined]
**project** | **string** | Project ID the log line is for | [optional] [default to undefined]
**organisation** | **string** | Organisation ID the log line is for | [optional] [default to undefined]
**group** | **string** | Group ID the log line is for | [optional] [default to undefined]
**log** | [**LogLog**](LogLog.md) |  | [optional] [default to undefined]

## Example

```typescript
import { Log } from '@qernal/chaos-client';

const instance: Log = {
    container,
    _function,
    project,
    organisation,
    group,
    log,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
