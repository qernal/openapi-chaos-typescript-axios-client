# MetricResourceAggregationResources

Resource(s) aggregation

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**buckets** | [**Array&lt;MetricResourceAggregationResourcesBucketsInner&gt;**](MetricResourceAggregationResourcesBucketsInner.md) | Array of unqiue resources | [optional] [default to undefined]
**doc_count_error_upper_bound** | **number** | Upper bound of error in document count | [optional] [default to undefined]
**sum_other_doc_count** | **number** | Sum of other document counts | [optional] [default to undefined]

## Example

```typescript
import { MetricResourceAggregationResources } from '@qernal/chaos-client';

const instance: MetricResourceAggregationResources = {
    buckets,
    doc_count_error_upper_bound,
    sum_other_doc_count,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
