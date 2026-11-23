
# Plan

The request object for the service method \'createPlan\' and the result of the service method \'getPlan\'.

## Properties

Name | Type
------------ | -------------
`id` | string
`description` | string
`locations` | [Array&lt;Location&gt;](Location.md)
`vehicles` | [Array&lt;Vehicle&gt;](Vehicle.md)
`drivers` | [Array&lt;Driver&gt;](Driver.md)
`transports` | [Array&lt;Transport&gt;](Transport.md)
`planningHorizon` | [TimeInterval](TimeInterval.md)
`restrictions` | [PlanningRestrictions](PlanningRestrictions.md)
`routes` | [Array&lt;Route&gt;](Route.md)
`unplannedVehicleIds` | Array&lt;string&gt;
`unplannedTransportIds` | Array&lt;string&gt;
`warnings` | [Array&lt;Warning&gt;](Warning.md)

## Example

```typescript
import type { Plan } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "description": null,
  "locations": null,
  "vehicles": null,
  "drivers": null,
  "transports": null,
  "planningHorizon": null,
  "restrictions": null,
  "routes": null,
  "unplannedVehicleIds": null,
  "unplannedTransportIds": null,
  "warnings": null,
} satisfies Plan

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Plan
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


