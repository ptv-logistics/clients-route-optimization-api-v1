
# PlanningRestrictions

Planning restrictions that must hold for all routes.

## Properties

Name | Type
------------ | -------------
`singleTripPerRoute` | boolean
`singleDepotPerRoute` | boolean
`mixedLoadingProhibitions` | [Array&lt;MixedLoadingProhibition&gt;](MixedLoadingProhibition.md)

## Example

```typescript
import type { PlanningRestrictions } from ''

// TODO: Update the object below with actual values
const example = {
  "singleTripPerRoute": null,
  "singleDepotPerRoute": null,
  "mixedLoadingProhibitions": null,
} satisfies PlanningRestrictions

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as PlanningRestrictions
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


