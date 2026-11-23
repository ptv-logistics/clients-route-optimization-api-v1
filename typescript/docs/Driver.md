
# Driver

A driver is always assigned to a specific vehicle and may not always be available to operate it. To be precise, a driver can only operate the corresponding vehicle within given time intervals.

## Properties

Name | Type
------------ | -------------
`id` | string
`vehicleId` | string
`availabilities` | [Array&lt;TimeInterval&gt;](TimeInterval.md)
`workingHoursPreset` | [WorkingHoursPreset](WorkingHoursPreset.md)
`breakRule` | [BreakRule](BreakRule.md)
`dailyRestRule` | [DailyRestRule](DailyRestRule.md)
`workLogbook` | [WorkLogbook](WorkLogbook.md)
`maximumDrivingTime` | number
`maximumTravelTime` | number

## Example

```typescript
import type { Driver } from ''

// TODO: Update the object below with actual values
const example = {
  "id": null,
  "vehicleId": null,
  "availabilities": null,
  "workingHoursPreset": null,
  "breakRule": null,
  "dailyRestRule": null,
  "workLogbook": null,
  "maximumDrivingTime": null,
  "maximumTravelTime": null,
} satisfies Driver

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Driver
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


