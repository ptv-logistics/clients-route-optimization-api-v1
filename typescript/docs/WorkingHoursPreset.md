
# WorkingHoursPreset

Specifies break and daily rest rule as well as maximum driving and travel time according to the chosen law.  If one of the concerned fields is specified as well the most restrictive rule holds. For example if a preset and maximumDrivingTime or maximumTravelTime are specified, the minimum of the specified value and the value defined by the preset counts. Currently, each driver must have the same value specified.  See [here](./concepts/drivers-working-hours-break-and-rest-rules) for more information.

## Properties

Name | Type
------------ | -------------

## Example

```typescript
import type { WorkingHoursPreset } from ''

// TODO: Update the object below with actual values
const example = {
} satisfies WorkingHoursPreset

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as WorkingHoursPreset
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


