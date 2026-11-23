
# Vehicle

A vehicle that is used to transport goods.

## Properties

Name | Type
------------ | -------------
`id` | string
`capacities` | Array&lt;number&gt;
`alternativeCapacities` | Array&lt;Array&lt;number&gt;&gt;
`capacitiesChangePosition` | [CapacitiesChangePosition](CapacitiesChangePosition.md)
`equipment` | Array&lt;string&gt;
`profile` | string
`startLocationId` | string
`endLocationId` | string
`serviceTimePerTransportStop` | number
`serviceTimeFactor` | number
`ignoreMixedLoadingProhibitions` | boolean
`routeStartInterval` | [TimeInterval](TimeInterval.md)
`maximumDistance` | number
`maximumNumberOfCustomerStops` | number

## Example

```typescript
import type { Vehicle } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "capacities": null,
  "alternativeCapacities": null,
  "capacitiesChangePosition": null,
  "equipment": null,
  "profile": null,
  "startLocationId": null,
  "endLocationId": null,
  "serviceTimePerTransportStop": null,
  "serviceTimeFactor": null,
  "ignoreMixedLoadingProhibitions": null,
  "routeStartInterval": null,
  "maximumDistance": null,
  "maximumNumberOfCustomerStops": null,
} satisfies Vehicle

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Vehicle
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


