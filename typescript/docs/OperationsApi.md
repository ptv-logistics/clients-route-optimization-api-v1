# OperationsApi

All URIs are relative to *https://api.myptv.com/routeoptimization/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**cancelOperation**](OperationsApi.md#canceloperation) | **DELETE** /plans/{id}/operation |  |
| [**getOperationStatus**](OperationsApi.md#getoperationstatus) | **GET** /plans/{id}/operation |  |
| [**startEvaluation**](OperationsApi.md#startevaluation) | **POST** /plans/{id}/operation/evaluation |  |
| [**startOptimization**](OperationsApi.md#startoptimization) | **POST** /plans/{id}/operation/optimization |  |



## cancelOperation

> cancelOperation(id)



Cancels the current operation of a plan. After cancelling an operation, the operation status for this plan can no longer be retrieved.

### Example

```ts
import {
  Configuration,
  OperationsApi,
} from '';
import type { CancelOperationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: apiKeyAuth
    apiKey: "YOUR API KEY",
  });
  const api = new OperationsApi(config);

  const body = {
    // string | ID of the plan which corresponding operation should be cancelled.
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies CancelOperationRequest;

  try {
    const data = await api.cancelOperation(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | `string` | ID of the plan which corresponding operation should be cancelled. | [Defaults to `undefined`] |

### Return type

`void` (Empty response body)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **204** | Cancellation and deletion of a running job for the plan is successfully triggered. |  -  |
| **0** | Response on failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getOperationStatus

> Operation getOperationStatus(id)



Retrieves the status of the current operation that is executed for the plan. If currently no operation is executed the status of the last executed operation is returned.

### Example

```ts
import {
  Configuration,
  OperationsApi,
} from '';
import type { GetOperationStatusRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: apiKeyAuth
    apiKey: "YOUR API KEY",
  });
  const api = new OperationsApi(config);

  const body = {
    // string | ID of the plan for which the corresponding operation status should be requested.
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetOperationStatusRequest;

  try {
    const data = await api.getOperationStatus(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | `string` | ID of the plan for which the corresponding operation status should be requested. | [Defaults to `undefined`] |

### Return type

[**Operation**](Operation.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The requested status is successfully provided. |  -  |
| **0** | Response on failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## startEvaluation

> startEvaluation(id)



Starts an asynchronous evaluation of the specified plan. Only one operation can be started for a plan at a time. Trying to start another operation before the current operation is finished results in an error. Whether an operation is finished or not can be checked with \&quot;getOperationStatus\&quot;. To get the result after the operation is finished \&quot;getPlan\&quot; can be used. Evaluation of a plan calculates driving times, service times, break and rest times and waiting times taking into account given time intervals. It may happen that not all restrictions can be fullfilled in which case one or more violations are reported. Evaluation does not change which transports are scheduled into which route nor their sequence, it does also not change the assignments of routes to vehicles.

### Example

```ts
import {
  Configuration,
  OperationsApi,
} from '';
import type { StartEvaluationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: apiKeyAuth
    apiKey: "YOUR API KEY",
  });
  const api = new OperationsApi(config);

  const body = {
    // string | ID of the plan to be evaluated.
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies StartEvaluationRequest;

  try {
    const data = await api.startEvaluation(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | `string` | ID of the plan to be evaluated. | [Defaults to `undefined`] |

### Return type

`void` (Empty response body)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Evaluation task accepted for processing. |  -  |
| **0** | Response on failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## startOptimization

> startOptimization(id, quality, tweaksToObjective, considerTransportPriorities, optimizationPremium)



Starts an asynchronous optimization of the specified plan. Only one operation can be started for a plan at a time. Trying to start another operation before the current operation is finished results in an error. Whether an operation is finished or not can be checked with \&quot;getOperationStatus\&quot;. To get the result after the operation is finished \&quot;getPlan\&quot; can be used. In the optimized plan, routes ideally include all transports that are specified in the request. Routes have additional information like arrival and departure times, driving times, service times and more.  If you call startOptimization multiple times consecutively for the same id, the optimization uses the result of the previous optimization as input, so previously planned transports remain planned in the output routes. If this is not what you intend to do, you can create a new plan before another startOptimization call.  When starting the optimization, the number of transports in the plan is used to calculate the number of transactions, see [here](../../help/faq-help) for more information.

### Example

```ts
import {
  Configuration,
  OperationsApi,
} from '';
import type { StartOptimizationRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: apiKeyAuth
    apiKey: "YOUR API KEY",
  });
  const api = new OperationsApi(config);

  const body = {
    // string | ID of the plan to be optimized.
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
    // OptimizationQuality | The optimization quality defines the tradeoff between calculation time and quality. A high solution quality and a low calculation time are conflicting. A larger solution search space may lead to a better solution but will take more calculation time.   * `STANDARD` - This quality level represents a good trade-off between solution quality and calculation time.   * `HIGH` - On this quality level, the search space is larger than on the standard level. This may lead to a better solution but will take more calculation time. (optional)
    quality: ...,
    // Array<TweakToObjective> | A tweak to objective defines additional optimization criteria. Without any tweak, the standard optimization goal is to plan as many transports as possible with as few vehicles as possible.   * `AVOID_INTERSECTIONS` - The focus of this approach is to avoid intersections of edges, where an edge is a straight line drawn between two consecutive stops in a route. The number of routes may be higher compared to the standard optimization goal.   * `IGNORE_MINIMIZATION_OF_NUMBER_OF_ROUTES` - With this tweak, the number of vehicles used in a plan, and thus the number of routes, is not minimized. (optional)
    tweaksToObjective: ...,
    // boolean | Set transport priority consideration to true or false.  See [here](./concepts/transport-priorities) for more information. (optional)
    considerTransportPriorities: true,
    // boolean | Set Optimization Premium to true to boost quality of results for all **quality** modes by taking advantage of additional computational resources.  Transactions\' packages for Optimization Premium are calculated differently.  See [here](./concepts/optimization-premium) for more information. (optional)
    optimizationPremium: true,
  } satisfies StartOptimizationRequest;

  try {
    const data = await api.startOptimization(body);
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters


| Name | Type | Description  | Notes |
|------------- | ------------- | ------------- | -------------|
| **id** | `string` | ID of the plan to be optimized. | [Defaults to `undefined`] |
| **quality** | `OptimizationQuality` | The optimization quality defines the tradeoff between calculation time and quality. A high solution quality and a low calculation time are conflicting. A larger solution search space may lead to a better solution but will take more calculation time.   * &#x60;STANDARD&#x60; - This quality level represents a good trade-off between solution quality and calculation time.   * &#x60;HIGH&#x60; - On this quality level, the search space is larger than on the standard level. This may lead to a better solution but will take more calculation time. | [Optional] [Defaults to `undefined`] [Enum: STANDARD, HIGH] |
| **tweaksToObjective** | `Array<TweakToObjective>` | A tweak to objective defines additional optimization criteria. Without any tweak, the standard optimization goal is to plan as many transports as possible with as few vehicles as possible.   * &#x60;AVOID_INTERSECTIONS&#x60; - The focus of this approach is to avoid intersections of edges, where an edge is a straight line drawn between two consecutive stops in a route. The number of routes may be higher compared to the standard optimization goal.   * &#x60;IGNORE_MINIMIZATION_OF_NUMBER_OF_ROUTES&#x60; - With this tweak, the number of vehicles used in a plan, and thus the number of routes, is not minimized. | [Optional] |
| **considerTransportPriorities** | `boolean` | Set transport priority consideration to true or false.  See [here](./concepts/transport-priorities) for more information. | [Optional] [Defaults to `false`] |
| **optimizationPremium** | `boolean` | Set Optimization Premium to true to boost quality of results for all **quality** modes by taking advantage of additional computational resources.  Transactions\&#39; packages for Optimization Premium are calculated differently.  See [here](./concepts/optimization-premium) for more information. | [Optional] [Defaults to `false`] |

### Return type

`void` (Empty response body)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **202** | Optimization task accepted for processing. |  -  |
| **0** | Response on failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

