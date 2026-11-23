
# PositionInTrip

If specified, this stop has to be the very first/last customer stop in its trip whenever there is a stop at this location. In each trip, there can only be one stop at a customer location with a trip section of type _FIRST_CUSTOMER_STOP_/_LAST_CUSTOMER_STOP_.    If specified, tripSectionNumber must not be set for the same location.   * `FIRST_CUSTOMER_STOP`    A stop at a customer location with this position type has to be the very first customer stop in its trip.   * `LAST_CUSTOMER_STOP`    A stop at a customer location with this position type has to be the very last customer stop in its trip.  See [here](./concepts/trip-sections-and-position-trips) for more information.

## Properties

Name | Type
------------ | -------------

## Example

```typescript
import type { PositionInTrip } from ''

// TODO: Update the object below with actual values
const example = {
} satisfies PositionInTrip

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as PositionInTrip
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


