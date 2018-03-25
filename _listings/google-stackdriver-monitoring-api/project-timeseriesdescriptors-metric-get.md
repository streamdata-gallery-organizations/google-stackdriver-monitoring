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
  /{project}/timeseriesDescriptors/{metric}:
    get:
      summary: ""
      description: List the descriptors of the time series that match the metric and
        labels values and that have data points in the interval
      operationId: cloudmonitoring.timeseriesDescriptors.list
      parameters:
      - in: query
        name: aggregator
        description: The aggregation function that will reduce the data points in
          each window to a single point
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: query
        name: count
        description: Maximum number of time series descriptors per page
      - in: query
        name: labels
        description: "A collection of labels for the matching time series, which are
          represented as:  \n- key==value: key equals the value \n- key=~value: key
          regex matches the value \n- key!=value: key does not equal the value \n-
          key!~value: key regex does not match the value  For example, to list all
          of the time series descriptors for the region us-central1, you could specify:\nlabel=cloud"
      - in: path
        name: metric
        description: Metric names are protocol-free URLs as listed in the Supported
          Metrics page
      - in: query
        name: oldest
        description: Start of the time interval (exclusive), which is expressed as
          an RFC 3339 timestamp
      - in: query
        name: pageToken
        description: The pagination token, which is used to page through large result
          sets
      - in: path
        name: project
        description: The project ID to which this time series belongs
      - in: query
        name: timespan
        description: 'Length of the time interval to query, which is an alternative
          way to declare the interval: (youngest - timespan, youngest]'
      - in: query
        name: window
        description: The sampling window
      - in: query
        name: youngest
        description: End of the time interval (inclusive), which is expressed as an
          RFC 3339 timestamp
      responses:
        200:
          description: OK
      tags:
      - monitoring
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