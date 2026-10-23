# S15 - Unreachable Data Sources

## Why is this a symptom?

This symptom refers to data sources used by the team's analyses that Oobeya cannot connect to. Analyses reading from an unreachable data source stop receiving new data. As a result, team metrics, scorecards, and other symptoms may silently become stale or incomplete.

**Level:** Team Level\
**Default Severity:** Warning\
**Potential Complications:** #data\_gap, #quality\_risk

## Possible Causes

* An expired or revoked access token, password, or app installation
* A changed data source URL, or a tool that has moved or been decommissioned
* Network, firewall, or proxy changes blocking Oobeya's access
* Reduced permissions for the integration account

## Improvement Areas

* Renew the data source credentials and test the connection on the **Data Sources** page
* Update the data source URL if the tool has moved
* Check network connectivity from Oobeya to the connected tool
* Use a dedicated integration account with securely managed credentials and a clear renewal process

## Detection Method

Oobeya detects this symptom when one or more data sources used by the team's analyses fail the nightly connection check.

**Formula:**

```
(unreachable_datasources) > 0
```

**Example:** A team uses a SonarQube data source for code quality analysis, but Oobeya cannot access the server during the nightly connection check. The team is flagged with **Unreachable Data Sources** until connectivity is restored and the issue is cleared by subsequent checks.
