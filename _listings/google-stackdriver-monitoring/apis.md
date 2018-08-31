---
name: Google Stackdriver Monitoring
x-slug: google-stackdriver-monitoring
description: Google Stackdriver provides powerful monitoring, logging, and diagnostics.
  It equips you with insight into the health, performance, and availability of cloud-powered
  applications, enabling you to find and fix issues faster. It is natively integrated
  with Google Cloud Platform, Amazon Web Services, and popular open source packages.
  Stackdriver provides a wide variety of metrics, dashboards, alerting, log management,
  reporting, and tracing capabilities.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
x-kinRank: "8"
x-alexaRank: "0"
tags: Google Stackdriver Monitoring
created: "2018-08-30"
modified: "2018-08-30"
url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/apis.md
specificationVersion: "0.14"
apis:
- name: Google Stackdriver Monitoring - Get Project Metric Descriptors
  x-api-slug: projectmetricdescriptors-get
  description: List metric descriptors that match the query. If the query is not set,
    then all of the metric descriptors will be returned. Large responses will be paginated,
    use the nextPageToken returned in the response to request subsequent pages of
    results by setting the pageToken query parameter to the value of the nextPageToken.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/projectmetricdescriptors-get-openapi.md
- name: Google Stackdriver Monitoring - Post Project Metric Descriptors
  x-api-slug: projectmetricdescriptors-post
  description: Create a new metric.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/projectmetricdescriptors-post-openapi.md
- name: Google Stackdriver Monitoring - Delete Project Metric Descriptors Metric
  x-api-slug: projectmetricdescriptorsmetric-delete
  description: Delete an existing metric.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/projectmetricdescriptorsmetric-delete-openapi.md
- name: Google Stackdriver Monitoring - Get Project Timeseries Metric
  x-api-slug: projecttimeseriesmetric-get
  description: List the data points of the time series that match the metric and labels
    values and that have data points in the interval. Large responses are paginated;
    use the nextPageToken returned in the response to request subsequent pages of
    results by setting the pageToken query parameter to the value of the nextPageToken.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/projecttimeseriesmetric-get-openapi.md
- name: Google Stackdriver Monitoring - Post Project Timeseries Write
  x-api-slug: projecttimeserieswrite-post
  description: Put data points to one or more time series for one or more metrics.
    If a time series does not exist, a new time series will be created. It is not
    allowed to write a time series point that is older than the existing youngest
    point of that time series. Points that are older than the existing youngest point
    of that time series will be discarded silently. Therefore, users should make sure
    that points of a time series are written sequentially in the order of their end
    time.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/projecttimeserieswrite-post-openapi.md
- name: Google Stackdriver Monitoring - Get Project Timeseriesdescriptors Metric
  x-api-slug: projecttimeseriesdescriptorsmetric-get
  description: List the descriptors of the time series that match the metric and labels
    values and that have data points in the interval. Large responses are paginated;
    use the nextPageToken returned in the response to request subsequent pages of
    results by setting the pageToken query parameter to the value of the nextPageToken.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/projecttimeseriesdescriptorsmetric-get-openapi.md
- name: Google Stackdriver Monitoring - Post Controller Debuggees Register
  x-api-slug: v2controllerdebuggeesregister-post
  description: Registers the debuggee with the controller service. All agents attached
    to the same application should call this method with the same request content
    to get back the same stable `debuggee_id`. Agents should call this method again
    whenever `google.rpc.Code.NOT_FOUND` is returned from any controller method. This
    allows the controller service to disable the agent or recover from any data loss.
    If the debuggee is disabled by the server, the response will have `is_disabled`
    set to `true`.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v2controllerdebuggeesregister-post-openapi.md
- name: Google Stackdriver Monitoring - Get Controller Debuggees Debuggeeid Breakpoints
  x-api-slug: v2controllerdebuggeesdebuggeeidbreakpoints-get
  description: Returns the list of all active breakpoints for the debuggee. The breakpoint
    specification (location, condition, and expression fields) is semantically immutable,
    although the field values may change. For example, an agent may update the location
    line number to reflect the actual line where the breakpoint was set, but this
    doesn't change the breakpoint semantics. This means that an agent does not need
    to check if a breakpoint has changed when it encounters the same breakpoint on
    a successive call. Moreover, an agent should remember the breakpoints that are
    completed until the controller removes them from the active list to avoid setting
    those breakpoints again.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v2controllerdebuggeesdebuggeeidbreakpoints-get-openapi.md
- name: Google Stackdriver Monitoring - Put Controller Debuggees Debuggeeid Breakpoints
  x-api-slug: v2controllerdebuggeesdebuggeeidbreakpointsid-put
  description: Updates the breakpoint state or mutable fields. The entire Breakpoint
    message must be sent back to the controller service. Updates to active breakpoint
    fields are only allowed if the new value does not change the breakpoint specification.
    Updates to the `location`, `condition` and `expression` fields should not alter
    the breakpoint semantics. These may only make changes such as canonicalizing a
    value or snapping the location to the correct line of code.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v2controllerdebuggeesdebuggeeidbreakpointsid-put-openapi.md
- name: Google Stackdriver Monitoring - Get Debugger Debuggees
  x-api-slug: v2debuggerdebuggees-get
  description: Lists all the debuggees that the user can set breakpoints to.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v2debuggerdebuggees-get-openapi.md
- name: Google Stackdriver Monitoring - Get Debugger Debuggees Debuggeeid Breakpoints
  x-api-slug: v2debuggerdebuggeesdebuggeeidbreakpoints-get
  description: Lists all breakpoints for the debuggee.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v2debuggerdebuggeesdebuggeeidbreakpoints-get-openapi.md
- name: Google Stackdriver Monitoring - Post Debugger Debuggees Debuggeeid Breakpoints
    Set
  x-api-slug: v2debuggerdebuggeesdebuggeeidbreakpointsset-post
  description: Sets the breakpoint to the debuggee.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v2debuggerdebuggeesdebuggeeidbreakpointsset-post-openapi.md
- name: Google Stackdriver Monitoring - Delete Debugger Debuggees Debuggeeid Breakpoints
    Breakpointid
  x-api-slug: v2debuggerdebuggeesdebuggeeidbreakpointsbreakpointid-delete
  description: Deletes the breakpoint from the debuggee.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v2debuggerdebuggeesdebuggeeidbreakpointsbreakpointid-delete-openapi.md
- name: Google Stackdriver Monitoring - Get Debugger Debuggees Debuggeeid Breakpoints
    Breakpointid
  x-api-slug: v2debuggerdebuggeesdebuggeeidbreakpointsbreakpointid-get
  description: Gets breakpoint information.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v2debuggerdebuggeesdebuggeeidbreakpointsbreakpointid-get-openapi.md
- name: Google Stackdriver Monitoring - Get Groupname
  x-api-slug: v1beta1groupname-get
  description: Get the specified group.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v1beta1groupname-get-openapi.md
- name: Google Stackdriver Monitoring - Put Name
  x-api-slug: v1beta1name-put
  description: |-
    Replace the data for the specified group.
    Fails if the group does not exist.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v1beta1name-put-openapi.md
- name: Google Stackdriver Monitoring - Delete Project Name Events
  x-api-slug: v1beta1projectnameevents-delete
  description: Deletes all error events of a given project.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v1beta1projectnameevents-delete-openapi.md
- name: Google Stackdriver Monitoring - Get Project Name Events
  x-api-slug: v1beta1projectnameevents-get
  description: Lists the specified events.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v1beta1projectnameevents-get-openapi.md
- name: Google Stackdriver Monitoring - Post Project Name Events Report
  x-api-slug: v1beta1projectnameeventsreport-post
  description: Report an individual error event. This endpoint accepts <strong>either</strong>
    an OAuth token, or an API key for authentication. To use an API key, append it
    to the URL as the value of a `key` parameter.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v1beta1projectnameeventsreport-post-openapi.md
- name: Google Stackdriver Monitoring - Get Project Name Groupstats
  x-api-slug: v1beta1projectnamegroupstats-get
  description: Lists the specified groups.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/google-stackdriver.png
  humanURL: https://cloud.google.com/monitoring/docs/
  baseURL: https:///
  tags: Monitoring, Stack Network, API Service Provider, API Provider, Profiles, Relative
    Data, Service API
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-organizations/google-stackdriver-monitoring/master/_listings/google-stackdriver-monitoring/v1beta1projectnamegroupstats-get-openapi.md
x-common:
- type: x-api-gallery
  url: http://google.speech.api.gallery.streamdata.io
- type: x-api-stack
  url: http://google.stackdriver.monitoring.stack.network
- type: x-developer
  url: https://cloud.google.com/monitoring/api/v3/
- type: x-website
  url: https://cloud.google.com/monitoring/docs/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---