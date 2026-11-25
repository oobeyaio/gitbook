# Interpretation Guidelines

Oobeya metrics should be read together and in the context of each team. Use these guidelines before drawing conclusions from any metric on the other pages.

### Use Trends, Not Isolated Values

A single value rarely provides enough context. Review:

* Current value
* Previous-period value
* Long-term trend
* Team history
* Engineering benchmark
* Product and workflow context

### Do Not Rank Developers Using Activity Volume Alone

Metrics such as commits, code lines, pull requests, or Activity Heatmap scores should not be used alone to evaluate individual performance.

They do not directly measure:

* Business value
* Code quality
* Task difficulty
* Mentoring
* Architecture work
* Incident response
* Collaboration outside tracked tools
* Product discovery
* Customer impact

### Correlation Does Not Prove Causation

When two metrics move together, use language such as:

* Appears to be associated with
* Coincides with
* May be contributing to
* Is concentrated in
* Should be investigated together with

Avoid assuming that one metric directly caused another without supporting evidence.

### Validate Data Configuration

Unexpected metric results are often related to:

* Incorrect user or contributor mapping
* Missing repositories
* Incorrect branch selection
* Incorrect production pipeline mapping
* Missing incident sources
* Incorrect workflow status mapping
* Excluded work-item types
* Missing effort values
* Incorrect team membership
* Missing Confluence Space mappings
* Missing AI product, model, or cost-center mappings
