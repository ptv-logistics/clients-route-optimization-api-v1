
# DailyRestRule

Defines when a daily rest becomes necessary and how long it should be. Currently, each driver must have the same values specified.  See [here](./concepts/drivers-working-hours-break-and-rest-rules) for more information.

## Properties

Name | Type
------------ | -------------
`dailyRestTime` | number
`maximumDrivingTimeBetweenDailyRests` | number
`maximumTravelTimeBetweenDailyRests` | number
`dailyRestPosition` | [DailyRestPosition](DailyRestPosition.md)

## Example

```typescript
import type { DailyRestRule } from ''

// TODO: Update the object below with actual values
const example = {
  "dailyRestTime": null,
  "maximumDrivingTimeBetweenDailyRests": null,
  "maximumTravelTimeBetweenDailyRests": null,
  "dailyRestPosition": null,
} satisfies DailyRestRule

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as DailyRestRule
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


