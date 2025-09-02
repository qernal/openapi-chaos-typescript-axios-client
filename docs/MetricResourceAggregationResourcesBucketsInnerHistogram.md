# MetricResourceAggregationResourcesBucketsInnerHistogram

Histogram of resource usage

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**buckets** | [**Array&lt;MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInner&gt;**](MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInner.md) | Array of resource usage by interval  &gt; Note: A metric will have either a &#x60;counter&#x60; or &#x60;gauge&#x60; value  | [optional] [default to undefined]

## Example

```typescript
import { MetricResourceAggregationResourcesBucketsInnerHistogram } from '@qernal/chaos-client';

const instance: MetricResourceAggregationResourcesBucketsInnerHistogram = {
    buckets,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
