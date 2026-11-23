
# RouteReport

A route report contains a summary of the values of all events and all reports that belong to this route, including the start time and the end time of the route.

## Properties

Name | Type
------------ | -------------
`startTime` | Date
`endTime` | Date
`travelTime` | number
`distance` | number
`drivingTime` | number
`serviceTime` | number
`waitingTime` | number
`breakTime` | number
`restTime` | number

## Example

```typescript
import type { RouteReport } from ''

// TODO: Update the object below with actual values
const example = {
  "startTime": null,
  "endTime": null,
  "travelTime": null,
  "distance": null,
  "drivingTime": null,
  "serviceTime": null,
  "waitingTime": null,
  "breakTime": null,
  "restTime": null,
} satisfies RouteReport

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as RouteReport
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


