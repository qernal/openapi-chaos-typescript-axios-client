# MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInner


## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**doc_count** | **number** | Number of documents in the bucket | [optional] [default to undefined]
**counter** | [**MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInnerCounter**](MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInnerCounter.md) |  | [optional] [default to undefined]
**gauge** | [**MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInnerGauge**](MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInnerGauge.md) |  | [optional] [default to undefined]
**key** | **number** | Histogram key (typically unix timestamp) | [optional] [default to undefined]
**key_as_string** | **string** | Histogram key as string/date-time | [optional] [default to undefined]

## Example

```typescript
import { MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInner } from '@qernal/chaos-client';

const instance: MetricResourceAggregationResourcesBucketsInnerHistogramBucketsInner = {
    doc_count,
    counter,
    gauge,
    key,
    key_as_string,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
