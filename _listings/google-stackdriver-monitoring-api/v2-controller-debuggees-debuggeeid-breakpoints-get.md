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
  /v2/controller/debuggees/{debuggeeId}/breakpoints:
    get:
      summary: ""
      description: Returns the list of all active breakpoints for the debuggee
      operationId: clouddebugger.controller.debuggees.breakpoints.list
      parameters:
      - in: path
        name: debuggeeId
        description: Identifies the debuggee
      - in: query
        name: successOnTimeout
        description: If set to `true`, returns `google
      - in: query
        name: waitToken
        description: A wait token that, if specified, blocks the method call until
          the list of active breakpoints has changed, or a server selected timeout
          has expired
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