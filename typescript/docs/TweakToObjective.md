
# TweakToObjective

A tweak to objective defines additional optimization criteria. Without any tweak, the standard optimization goal is to plan as many transports as possible with as few vehicles as possible.   * `AVOID_INTERSECTIONS` - The focus of this approach is to avoid intersections of edges, where an edge is a straight line drawn between two consecutive stops in a route. The number of routes may be higher compared to the standard optimization goal.   * `IGNORE_MINIMIZATION_OF_NUMBER_OF_ROUTES` - With this tweak, the number of vehicles used in a plan, and thus the number of routes, is not minimized.

## Properties

Name | Type
------------ | -------------

## Example

```typescript
import type { TweakToObjective } from ''

// TODO: Update the object below with actual values
const example = {
} satisfies TweakToObjective

console.log(example)

// Convert the instance to a JSON string
const exampleJSON: string = JSON.stringify(example)
console.log(exampleJSON)

// Parse the JSON string back to an object
const exampleParsed = JSON.parse(exampleJSON) as TweakToObjective
console.log(exampleParsed)
```

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


