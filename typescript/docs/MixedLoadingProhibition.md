
# MixedLoadingProhibition

There may be some transports that shall not be mixed with some other transports on one trip. For instance, it may be prohibited to load certain dangerous goods together on the same trip, such as flammable solids on the one hand and explosive substances on the other hand. A mixed loading prohibition is a pair of two conflicting load categories that prohibits transports with these load categories to be mixed on the same trip. The load category can be specified for every transport. For a vehicle, there is a flag that lets the vehicle ignore this restriction.  See [here](./concepts/mixed-loading-prohibition) for more information.

## Properties

Name | Type
------------ | -------------
`conflictingLoadCategory1` | string
`conflictingLoadCategory2` | string

## Example

```typescript
import type { MixedLoadingProhibition } from ''

// TODO: Update the object below with actual values
const example = {
  "conflictingLoadCategory1": null,
  "conflictingLoadCategory2": null,
} satisfies MixedLoadingProhibition

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as MixedLoadingProhibition
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


