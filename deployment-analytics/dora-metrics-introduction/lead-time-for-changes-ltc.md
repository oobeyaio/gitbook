---
icon: clock
---

# Lead Time For Changes (LTC)

## Lead Time For Changes Metric Definition

The interval between a code change and its release to the end users is considered Lead Time For Changes.

## Lead Time For Changes Formula

{% code overflow="wrap" %}
```
Lead Time For Changes = [Production Deployment Time] - [First Commit Time of all changes]
```
{% endcode %}

### The Anatomy of the Lead Time and Lead Time For Changes <a href="#e909" id="e909"></a>

The image below represents the Lead Time metric's anatomy that covers the Lead Time For Changes metric.

<figure><img src="https://miro.medium.com/v2/resize:fit:700/1*7r-mZIZvJu4hzIx9LVfKMw.png" alt=""><figcaption><p>Lead Time Breakdown</p></figcaption></figure>

## The Stages of the Lead Time For Changes <a href="#b1df" id="b1df"></a>

The Lead Time For Changes measures friction in the coding, code review, and CI/CD processes.

1. **Coding Time:** The time elapsed between the First commit and the PR opened.
2. **Code Review Time:** The time elapsed between the PR opened and the PR merged.
3. **Waiting For Deploy:** The time elapsed between the PR merged and the Deployment pipeline started.
4. **Deployment Time:** The time elapsed between the Deployment started and Deployment finished successfully.

***

### LEARN MORE

**BLOG POST -** [How To Reduce Lead Time For Changes (Optimizing DORA Metrics)](https://oobeya.io/blog/how-to-reduce-lead-time-for-changes-dora-metrics/)

> In this article, we will take a closer look at one of [DORA Metrics](https://oobeya.io/dora-metrics-four-key/), **Lead Time For Changes** (Change Lead Time), and how it can be reduced to optimize software development and delivery processes.
