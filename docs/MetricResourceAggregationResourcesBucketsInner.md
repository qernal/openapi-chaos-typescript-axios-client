# MetricResourceAggregationResourcesBucketsInner

Histogram bucket

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**doc_count** | **number** | Number of documents in the bucket | [optional] [default to undefined]
**histogram** | [**MetricResourceAggregationResourcesBucketsInnerHistogram**](MetricResourceAggregationResourcesBucketsInnerHistogram.md) |  | [optional] [default to undefined]
**key** | **string** | Metric key | [optional] [default to undefined]

## Example

```typescript
import { MetricResourceAggregationResourcesBucketsInner } from '@qernal/chaos-client';

const instance: MetricResourceAggregationResourcesBucketsInner = {
    doc_count,
    histogram,
    key,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
