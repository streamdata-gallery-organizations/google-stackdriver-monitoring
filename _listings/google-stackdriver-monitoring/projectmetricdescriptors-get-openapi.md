---
swagger: "2.0"
x-collection-name: Google Stackdriver Monitoring
x-complete: 0
info:
  title: Google Stackdriver Monitoring Get Project Metric Descriptors
  description: List metric descriptors that match the query. If the query is not set,
    then all of the metric descriptors will be returned. Large responses will be paginated,
    use the nextPageToken returned in the response to request subsequent pages of
    results by setting the pageToken query parameter to the value of the nextPageToken.
  version: 1.0.0
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{project}/metricDescriptors:
    get:
      summary: Get Project Metric Descriptors
      description: List metric descriptors that match the query. If the query is not
        set, then all of the metric descriptors will be returned. Large responses
        will be paginated, use the nextPageToken returned in the response to request
        subsequent pages of results by setting the pageToken query parameter to the
        value of the nextPageToken.
      operationId: cloudmonitoring.metricDescriptors.list
      x-api-path-slug: projectmetricdescriptors-get
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: count
        description: Maximum number of metric descriptors per page
      - in: query
        name: pageToken
        description: The pagination token, which is used to page through large result
          sets
      - in: path
        name: project
        description: The project id
      - in: query
        name: query
        description: The query used to search against existing metrics
      responses:
        200:
          description: OK
      tags:
      - Monitoring
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