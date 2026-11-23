
# ViolationType

Specifies the type of violation.   * `PLANNING_HORIZON` - The planning horizon is violated.   * `DRIVER_AVAILABILITY` - The availabilities of the driver are violated.   * `ROUTE_START_INTERVAL` - The route start interval is violated.   * `OPENING_INTERVAL` - The opening intervals of the location are violated.   * `VEHICLE_CAPACITY` - At least one of the vehicle capacities is violated.   * `VEHICLE_EQUIPMENT` - Not all vehicle equipment for the currently loaded transports is available.   * `MAXIMUM_TRAVEL_TIME_OF_DRIVER` - Indicates a violation of the maximum allowed travel time of driver as specified at the driver or by the drivers\' working hours restriction.   * `MAXIMUM_DRIVING_TIME_OF_DRIVER` - Indicates a violation of the maximum allowed driving time of driver as specified at the driver or by the drivers\' working hours restriction.  * `MAXIMUM_DISTANCE` - Indicates a violation of the maximum allowed driving distance as specified at the vehicle.   * `MAXIMUM_NUMBER_OF_CUSTOMER_STOPS` - Indicates a violation of the maximum allowed number of customer stops as specified at the vehicle.   * `REST_POSITION` - Indicates that a daily rest is not at the end of a trip. In this case the expected position for a daily rest is at the end of a trip.   * `STOP_POSITION_IN_TRIP` - Indicates a violation of the stop position in the trip.   * `TRIP_SECTION` - Indicates a violation of the trip section numbers of a customer stop.   * `MIXED_LOADING_PROHIBITION` - Indicates a violation of the mixed loading prohibitions.

## Properties

Name | Type
------------ | -------------

## Example

```typescript
import type { ViolationType } from ''

// TODO: Update the object below with actual values
const example = {
} satisfies ViolationType

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as ViolationType
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


