---
icon: circle-exclamation-check
---

# Mean Time To Restore Service (MTTR)

## Mean Time To Restore Service Metric Definition

This measures how long it takes to restore service after a production incident.

## Mean Time To Restore Service Formula

{% code overflow="wrap" %}
```
Mean Time To Restore Service = avg ([Incident Resolved] - [Incident Created])
```
{% endcode %}
