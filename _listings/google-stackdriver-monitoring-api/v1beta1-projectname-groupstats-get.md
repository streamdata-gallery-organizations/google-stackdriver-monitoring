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
  /v1beta1/{projectName}/groupStats:
    get:
      summary: ""
      description: Lists the specified groups
      operationId: clouderrorreporting.projects.groupStats.list
      parameters:
      - in: query
        name: alignment
        description: '[Optional] The alignment of the timed counts to be returned'
      - in: query
        name: alignmentTime
        description: |-
          [Optional] Time where the timed counts shall be aligned if rounded
          alignment is chosen
      - in: query
        name: groupId
        description: '[Optional] List all <code>ErrorGroupStats</code> with these
          IDs'
      - in: query
        name: order
        description: '[Optional] The sort order in which the results are returned'
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
        name: timedCountDuration
        description: '[Optional] The preferred duration for a single returned `TimedCount`'
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