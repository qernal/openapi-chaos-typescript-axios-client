# MetricHttpAggregationHttpCodes

HTTP status code aggregation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**buckets** | [**Array&lt;MetricHttpAggregationHttpCodesBucketsInner&gt;**](MetricHttpAggregationHttpCodesBucketsInner.md) | Array of unique http status codes | [optional] [default to undefined]
**doc_count_error_upper_bound** | **number** | Upper bound of error in document count | [optional] [default to undefined]
**sum_other_doc_count** | **number** | Sum of other document counts | [optional] [default to undefined]

## Example

```typescript
import { MetricHttpAggregationHttpCodes } from '@qernal/chaos-client';

const instance: MetricHttpAggregationHttpCodes = {
    buckets,
    doc_count_error_upper_bound,
    sum_other_doc_count,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
