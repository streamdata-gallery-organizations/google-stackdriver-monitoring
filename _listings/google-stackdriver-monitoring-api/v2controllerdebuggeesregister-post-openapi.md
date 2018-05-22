---
swagger: "2.0"
x-collection-name: Google Stackdriver Monitoring API
x-complete: 0
info:
  title: 'Google Stackdriver Monitoring API '
  version: 1.0.0
  description: Registers the debuggee with the controller service. All agents attached
    to the same application should call this method with the same request content
    to get back the same stable `debuggee_id`. Agents should call this method again
    whenever `google.rpc.Code.NOT_FOUND` is returned from any controller method. This
    allows the controller service to disable the agent or recover from any data loss.
    If the debuggee is disabled by the server, the response will have `is_disabled`
    set to `true`.
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /{project}/metricDescriptors:
    get:
      summary: ""
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
    post:
      summary: ""
      description: Create a new metric.
      operationId: cloudmonitoring.metricDescriptors.create
      x-api-path-slug: projectmetricdescriptors-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: project
        description: The project id
      responses:
        200:
          description: OK
      tags:
      - Monitoring
  /{project}/metricDescriptors/{metric}:
    delete:
      summary: ""
      description: Delete an existing metric.
      operationId: cloudmonitoring.metricDescriptors.delete
      x-api-path-slug: projectmetricdescriptorsmetric-delete
      parameters:
      - in: path
        name: metric
        description: Name of the metric
      - in: path
        name: project
        description: The project ID to which the metric belongs
      responses:
        200:
          description: OK
      tags:
      - Monitoring
  /{project}/timeseries/{metric}:
    get:
      summary: ""
      description: List the data points of the time series that match the metric and
        labels values and that have data points in the interval. Large responses are
        paginated; use the nextPageToken returned in the response to request subsequent
        pages of results by setting the pageToken query parameter to the value of
        the nextPageToken.
      operationId: cloudmonitoring.timeseries.list
      x-api-path-slug: projecttimeseriesmetric-get
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
        description: Maximum number of data points per page, which is used for pagination
          of results
      - in: query
        name: labels
        description: 'A collection of labels for the matching time series, which are
          represented as:  - key==value: key equals the value - key=~value: key regex
          matches the value - key!=value: key does not equal the value - key!~value:
          key regex does not match the value  For example, to list all of the time
          series descriptors for the region us-central1, you could specify:label=cloud'
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
      - Monitoring
  /{project}/timeseries:write:
    post:
      summary: ""
      description: Put data points to one or more time series for one or more metrics.
        If a time series does not exist, a new time series will be created. It is
        not allowed to write a time series point that is older than the existing youngest
        point of that time series. Points that are older than the existing youngest
        point of that time series will be discarded silently. Therefore, users should
        make sure that points of a time series are written sequentially in the order
        of their end time.
      operationId: cloudmonitoring.timeseries.write
      x-api-path-slug: projecttimeserieswrite-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      - in: path
        name: project
        description: The project ID
      responses:
        200:
          description: OK
      tags:
      - Monitoring
  /{project}/timeseriesDescriptors/{metric}:
    get:
      summary: ""
      description: List the descriptors of the time series that match the metric and
        labels values and that have data points in the interval. Large responses are
        paginated; use the nextPageToken returned in the response to request subsequent
        pages of results by setting the pageToken query parameter to the value of
        the nextPageToken.
      operationId: cloudmonitoring.timeseriesDescriptors.list
      x-api-path-slug: projecttimeseriesdescriptorsmetric-get
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
        description: 'A collection of labels for the matching time series, which are
          represented as:  - key==value: key equals the value - key=~value: key regex
          matches the value - key!=value: key does not equal the value - key!~value:
          key regex does not match the value  For example, to list all of the time
          series descriptors for the region us-central1, you could specify:label=cloud'
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
      - Monitoring
  /v2/controller/debuggees/register:
    post:
      summary: ""
      description: Registers the debuggee with the controller service. All agents
        attached to the same application should call this method with the same request
        content to get back the same stable `debuggee_id`. Agents should call this
        method again whenever `google.rpc.Code.NOT_FOUND` is returned from any controller
        method. This allows the controller service to disable the agent or recover
        from any data loss. If the debuggee is disabled by the server, the response
        will have `is_disabled` set to `true`.
      operationId: clouddebugger.controller.debuggees.register
      x-api-path-slug: v2controllerdebuggeesregister-post
      parameters:
      - in: body
        name: body
        schema:
          $ref: '#/definitions/holder'
      responses:
        200:
          description: OK
      tags:
      - Debugger
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