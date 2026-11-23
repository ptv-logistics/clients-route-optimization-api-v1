
# Route

A route contains a sequence of stops. It specifies where and in which order goods are to be picked up or delivered. Each stop can be assigned to a trip. A route is subdivided into trips. Each route has at least one trip and a trip consists of at least two stops. At the beginning and end of each trip the vehicle does not carry any load. A trip starts at the vehicle start location or at a depot location, and ends at the vehicle end location or at a depot location.   See [here](./concepts/routes-and-trips) for more information.

## Properties

Name | Type
------------ | -------------
`vehicleId` | string
`stops` | [Array&lt;Stop&gt;](Stop.md)
`report` | [RouteReport](RouteReport.md)

## Example

```typescript
import type { Route } from ''

// TODO: Update the object below with actual values
const example = {
  "vehicleId": null,
  "stops": null,
  "report": null,
} satisfies Route

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Route
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


