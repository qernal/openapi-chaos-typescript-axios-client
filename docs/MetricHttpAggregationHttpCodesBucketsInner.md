# MetricHttpAggregationHttpCodesBucketsInner

HTTP status code bucket

## Properties

Name | Type | Description | Notes
------------ | ------------- | ------------- | -------------
**doc_count** | **number** | Number of documents in the bucket | [optional] [default to undefined]
**histogram** | [**MetricHttpAggregationHttpCodesBucketsInnerHistogram**](MetricHttpAggregationHttpCodesBucketsInnerHistogram.md) |  | [optional] [default to undefined]
**key** | **string** | HTTP status code, typical values will be;  - http-2xx - http-3xx - http-4xx - http-5xx  &gt; Note: the \&#39;xx\&#39; is intentional and literal, all status codes within that range will be grouped  | [optional] [default to undefined]

## Example

```typescript
import { MetricHttpAggregationHttpCodesBucketsInner } from '@qernal/chaos-client';

const instance: MetricHttpAggregationHttpCodesBucketsInner = {
    doc_count,
    histogram,
    key,
};
```

[[Back to Model list]](../README.md#documentation-for-models) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to README]](../README.md)
