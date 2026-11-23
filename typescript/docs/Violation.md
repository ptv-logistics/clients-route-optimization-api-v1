
# Violation

Specifies a violation of a route.

## Properties

Name | Type
------------ | -------------
`type` | [ViolationType](ViolationType.md)
`timeExceedance` | number
`distanceExceedance` | number
`numberOfStopsExceedance` | number
`capacityExceedance` | Array&lt;number&gt;
`missingEquipment` | Array&lt;string&gt;
`mixedLoadingProhibitions` | [Array&lt;MixedLoadingProhibition&gt;](MixedLoadingProhibition.md)

## Example

```typescript
import type { Violation } from ''

// TODO: Update the object below with actual values
const example = {
  "type": null,
  "timeExceedance": null,
  "distanceExceedance": null,
  "numberOfStopsExceedance": null,
  "capacityExceedance": null,
  "missingEquipment": null,
  "mixedLoadingProhibitions": null,
} satisfies Violation

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as Violation
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


