# PlansApi

All URIs are relative to *https://api.myptv.com/routeoptimization/v1*

| Method | HTTP request | Description |
|------------- | ------------- | -------------|
| [**createPlan**](PlansApi.md#createplan) | **POST** /plans |  |
| [**deletePlan**](PlansApi.md#deleteplan) | **DELETE** /plans/{id} |  |
| [**getPlan**](PlansApi.md#getplan) | **GET** /plans/{id} |  |
| [**getPlanSummaries**](PlansApi.md#getplansummaries) | **GET** /plans/summaries |  |



## createPlan

> Plan createPlan(plan)



Creates a new plan containing parts like vehicles and transports which should be used for a subsequent optimization. It persists and returns a slightly modified plan including a server generated ID that can be used for later retrieval. This returned plan can be used for automated route optimization via Operations API.

### Example

```ts
import {
  Configuration,
  PlansApi,
} from '';
import type { CreatePlanRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: apiKeyAuth
    apiKey: "YOUR API KEY",
  });
  const api = new PlansApi(config);

  const body = {
    // Plan | The plan containing vehicles and transports. The returned plan in the response body is extended by a server generated ID and details of the calculated routes.
    plan: ...,
  } satisfies CreatePlanRequest;

  try {
    const data = await api.createPlan(body);
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
| **plan** | [Plan](Plan.md) | The plan containing vehicles and transports. The returned plan in the response body is extended by a server generated ID and details of the calculated routes. | |

### Return type

[**Plan**](Plan.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: `application/json`
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **201** | Plan successfully created and persisted. |  -  |
| **0** | Response on failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## deletePlan

> deletePlan(id)



Deletes a plan identified by the ID. Also cancels a currently running optimization of the plan.

### Example

```ts
import {
  Configuration,
  PlansApi,
} from '';
import type { DeletePlanRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: apiKeyAuth
    apiKey: "YOUR API KEY",
  });
  const api = new PlansApi(config);

  const body = {
    // string | ID of the plan to be deleted.
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies DeletePlanRequest;

  try {
    const data = await api.deletePlan(body);
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
| **id** | `string` | ID of the plan to be deleted. | [Defaults to `undefined`] |

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
| **204** | Success with empty result. |  -  |
| **0** | Response on failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getPlan

> Plan getPlan(id)



Retrieves a plan identified by the ID.

### Example

```ts
import {
  Configuration,
  PlansApi,
} from '';
import type { GetPlanRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: apiKeyAuth
    apiKey: "YOUR API KEY",
  });
  const api = new PlansApi(config);

  const body = {
    // string | ID of the requested plan.
    id: 38400000-8cf0-11bd-b23e-10b96e4ef00d,
  } satisfies GetPlanRequest;

  try {
    const data = await api.getPlan(body);
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
| **id** | `string` | ID of the requested plan. | [Defaults to `undefined`] |

### Return type

[**Plan**](Plan.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The requested plan is successfully provided. |  -  |
| **0** | Response on failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)


## getPlanSummaries

> PlanSummaries getPlanSummaries()



Retrieves a list of summaries for at most 1000 least recently updated available plans.

### Example

```ts
import {
  Configuration,
  PlansApi,
} from '';
import type { GetPlanSummariesRequest } from '';

async function example() {
  console.log("🚀 Testing  SDK...");
  const config = new Configuration({ 
    // To configure API key authorization: apiKeyAuth
    apiKey: "YOUR API KEY",
  });
  const api = new PlansApi(config);

  try {
    const data = await api.getPlanSummaries();
    console.log(data);
  } catch (error) {
    console.error(error);
  }
}

// Run the test
example().catch(console.error);
```

### Parameters

This endpoint does not need any parameter.

### Return type

[**PlanSummaries**](PlanSummaries.md)

### Authorization

[apiKeyAuth](../README.md#apiKeyAuth)

### HTTP request headers

- **Content-Type**: Not defined
- **Accept**: `application/json`


### HTTP response details
| Status code | Description | Response headers |
|-------------|-------------|------------------|
| **200** | The list of plan summaries is successfully provided. |  -  |
| **0** | Response on failure. |  -  |

[[Back to top]](#) [[Back to API list]](../README.md#api-endpoints) [[Back to Model list]](../README.md#models) [[Back to README]](../README.md)

