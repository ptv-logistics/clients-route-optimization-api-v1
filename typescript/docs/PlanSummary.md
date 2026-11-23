
# PlanSummary

The summary of a plan.

## Properties

Name | Type
------------ | -------------
`id` | string
`numberOfLocations` | number
`numberOfVehicles` | number
`numberOfTransports` | number
`numberOfRoutes` | number
`description` | string
`updateTime` | Date
`creationTime` | Date

## Example

```typescript
import type { PlanSummary } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "numberOfLocations": null,
  "numberOfVehicles": null,
  "numberOfTransports": null,
  "numberOfRoutes": null,
  "description": null,
  "updateTime": null,
  "creationTime": null,
} satisfies PlanSummary

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as PlanSummary
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


