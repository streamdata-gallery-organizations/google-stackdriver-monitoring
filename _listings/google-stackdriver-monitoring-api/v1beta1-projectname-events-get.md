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
  /v1beta1/{projectName}/events:
    get:
      summary: ""
      description: Lists the specified events
      operationId: clouderrorreporting.projects.events.list
      parameters:
      - in: query
        name: groupId
        description: '[Required] The group for which events shall be returned'
      - in: query
        name: pageSize
        description: '[Optional] The maximum number of results to return per response'
      - in: query
        name: pageToken
        description: '[Optional] A `next_page_token` provided by a previous response'
      - in: path
        name: projectName
        description: '[Required] The resource name of the Google Cloud Platform project'
      - in: query
        name: serviceFilter.service
        description: |-
          [Optional] The exact value to match against
          [`ServiceContext
      - in: query
        name: serviceFilter.version
        description: |-
          [Optional] The exact value to match against
          [`ServiceContext
      - in: query
        name: timeRange.period
        description: Restricts the query to the specified time range
      responses:
        200:
          description: OK
      tags:
      - errors
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