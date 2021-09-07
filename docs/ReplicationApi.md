# \ReplicationApi

All URIs are relative to *http://localhost/api/v2.0*

Method | HTTP request | Description
------------- | ------------- | -------------
[**GetReplicationExecution**](ReplicationApi.md#GetReplicationExecution) | **Get** /replication/executions/{id} | Get the specific replication execution
[**GetReplicationLog**](ReplicationApi.md#GetReplicationLog) | **Get** /replication/executions/{id}/tasks/{task_id}/log | Get the log of the specific replication task
[**ListReplicationExecutions**](ReplicationApi.md#ListReplicationExecutions) | **Get** /replication/executions | List replication executions
[**ListReplicationTasks**](ReplicationApi.md#ListReplicationTasks) | **Get** /replication/executions/{id}/tasks | List replication tasks for a specific execution
[**StartReplication**](ReplicationApi.md#StartReplication) | **Post** /replication/executions | Start one replication execution
[**StopReplication**](ReplicationApi.md#StopReplication) | **Put** /replication/executions/{id} | Stop the specific replication execution


# **GetReplicationExecution**
> ReplicationExecution GetReplicationExecution(ctx, id)
Get the specific replication execution

Get the replication execution specified by ID

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **id** | **int64**| The ID of the execution. | 

### Return type

[**ReplicationExecution**](ReplicationExecution.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **GetReplicationLog**
> string GetReplicationLog(ctx, id, taskId)
Get the log of the specific replication task

Get the log of the specific replication task

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **id** | **int64**| The ID of the execution that the tasks belongs to. | 
  **taskId** | **int64**| The ID of the task. | 

### Return type

**string**

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: text/plain

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ListReplicationExecutions**
> []ReplicationExecution ListReplicationExecutions(ctx, optional)
List replication executions

List replication executions

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
 **optional** | ***ReplicationApiListReplicationExecutionsOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a ReplicationApiListReplicationExecutionsOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **page** | **optional.Int64**| The page number | [default to 1]
 **pageSize** | **optional.Int64**| The size of per page | [default to 10]
 **policyId** | **optional.Int32**| The ID of the policy that the executions belong to. | 
 **status** | **optional.String**| The execution status. | 
 **trigger** | **optional.String**| The trigger mode. | 

### Return type

[**[]ReplicationExecution**](ReplicationExecution.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **ListReplicationTasks**
> []ReplicationTask ListReplicationTasks(ctx, id, optional)
List replication tasks for a specific execution

List replication tasks for a specific execution

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **id** | **int64**| The ID of the execution that the tasks belongs to. | 
 **optional** | ***ReplicationApiListReplicationTasksOpts** | optional parameters | nil if no parameters

### Optional Parameters
Optional parameters are passed through a pointer to a ReplicationApiListReplicationTasksOpts struct

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------

 **page** | **optional.Int64**| The page number | [default to 1]
 **pageSize** | **optional.Int64**| The size of per page | [default to 10]
 **status** | **optional.String**| The task status. | 
 **resourceType** | **optional.String**| The resource type. | 

### Return type

[**[]ReplicationTask**](ReplicationTask.md)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **StartReplication**
> StartReplication(ctx, execution)
Start one replication execution

Start one replication execution according to the policy

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **execution** | [**StartReplicationExecution**](StartReplicationExecution.md)| The ID of policy that the execution belongs to | 

### Return type

 (empty response body)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

# **StopReplication**
> StopReplication(ctx, id)
Stop the specific replication execution

Stop the replication execution specified by ID

### Required Parameters

Name | Type | Description  | Notes
------------- | ------------- | ------------- | -------------
 **ctx** | **context.Context** | context for authentication, logging, cancellation, deadlines, tracing, etc.
  **id** | **int64**| The ID of the execution. | 

### Return type

 (empty response body)

### Authorization

[basic](../README.md#basic)

### HTTP request headers

 - **Content-Type**: application/json
 - **Accept**: application/json

[[Back to top]](#) [[Back to API list]](../README.md#documentation-for-api-endpoints) [[Back to Model list]](../README.md#documentation-for-models) [[Back to README]](../README.md)

