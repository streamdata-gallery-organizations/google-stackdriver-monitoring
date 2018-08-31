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
  /v2/controller/debuggees/{debuggeeId}/breakpoints/{id}:
    put:
      summary: ""
      description: Updates the breakpoint state or mutable fields
      operationId: clouddebugger.controller.debuggees.breakpoints.update
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: debuggeeId
        description: Identifies the debuggee being debugged
      - in: path
        name: id
        description: Breakpoint identifier, unique in the scope of the debuggee
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