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
  /{project}/metricDescriptors/{metric}:
    delete:
      summary: ""
      description: Delete an existing metric
      operationId: cloudmonitoring.metricDescriptors.delete
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