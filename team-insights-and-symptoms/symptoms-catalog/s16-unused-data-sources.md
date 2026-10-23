# S16 - Unused Data Sources

## Why is this a symptom?

This symptom refers to data source categories defined in Oobeya (such as SCM & CI/CD, Project Management, or Code Quality) that none of the team's analyses use. When the team's scorecard is not connected to a category of tools used by the organization, metrics, scorecards, and other symptoms may miss that part of the team's work.

**Level:** Team Level\
**Default Severity:** Info\
**Potential Complications:** #data\_gap

## Possible Causes

* The team's repositories, boards, or projects were never selected on its scorecard
* The team moved to a new tool or instance, but its scorecard configuration was not updated
* The data source is used by other teams but is not relevant to the selected team

## Improvement Areas

* Select the team's relevant analyses from these data sources on its scorecard
* Create missing analyses for the team's repositories, boards, or projects
* Disable data sources that are no longer in use
* Verify that the unused category is actually relevant to the team before changing its configuration

## Detection Method

Oobeya detects this symptom when the team's analyses use none of the data sources from at least one category defined in Oobeya.

**Formula:**

```
(unused_datasource_categories) > 0
```

**Example:** A Project Management data source is configured in Oobeya, but no project analysis from that category is included in the selected team's scorecard. The team is flagged with **Unused Data Sources** so its configuration and data coverage can be reviewed.
