---
swagger: "2.0"
info:
  title: Google Stackdriver Monitoring API
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v2/debugger/debuggees/{debuggeeId}/breakpoints:
    get:
      summary: ""
      description: Lists all breakpoints for the debuggee
      operationId: clouddebugger.debugger.debuggees.breakpoints.list
      parameters:
      - in: query
        name: action.value
        description: Only breakpoints with the specified action will pass the filter
      - in: query
        name: clientVersion
        description: The client version making the call
      - in: path
        name: debuggeeId
        description: ID of the debuggee whose breakpoints to list
      - in: query
        name: includeAllUsers
        description: When set to `true`, the response includes the list of breakpoints
          set by any user
      - in: query
        name: includeInactive
        description: When set to `true`, the response includes active and inactive
          breakpoints
      - in: query
        name: stripResults
        description: 'When set to `true`, the response breakpoints are stripped of
          the results fields: `stack_frames`, `evaluated_expressions` and `variable_table`'
      - in: query
        name: waitToken
        description: A wait token that, if specified, blocks the call until the breakpoints
          list has changed, or a server selected timeout has expired
      responses:
        200:
          description: OK
      tags:
      - debugger
definitions: []
x-collection-name: Google Stackdriver Monitoring API
x-streamrank:
  polling_total_time_average: 0
  polling_size_download_average: 0
  streaming_total_time_average: 0
  streaming_size_download_average: 0
  change_yes: 0
  change_no: 0
  time_percentage: 0
  size_percentage: 0
  change_percentage: 0
  last_run: ""
  days_run: 0
  minute_run: 0
---