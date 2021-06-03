---
title: "Jakarta Batch 2.1 (Under Development)"
date: 2021-04-15
summary: "Release for Jakarta EE 10"
---

Jakarta Batch specifies a Java API plus an XML-based job specification language (JSL), which lets you compose batch jobs in XML from reusable Java application artifacts and conveniently parameterize different executions of a single job.

# Plan
Jakarta Batch 2.1 will target the Jakarta EE 10 platform release.

Jakarta Batch 2.1 will be a minor update with fixes and enhancements.

## It will contain:

### CDI integration defined

When CDI is present, as within the Jakarta EE Platform, then the integration of Jakarta Batch + CDI will be well-defined and required for an implementation to be certified as Jakarta Batch-compliant.   However, an implementation should be able to certify full Jakarta Batch compliance in the absence of a CDI implementation, e.g. if is certifying itself as a Jakarta Batch implementation but not a Jakarta EE Platform implementation.

The working design for detecting the presence of CDI assumes the TCK would do something like call `CDI.current()`, and, if a `null` value is returned, "no-op" (immediately pass) the relevant tests.

### Other enhancements.  

This set is being discussed and prioritized via the Jakarta Batch dev mailing list, and tracked at: https://github.com/eclipse-ee4j/batch-api/milestone/1

Note at the current pace it is expected that the 2.1 delivery will include less than the full list of issues currently grouped within this milestone (which is more of a draft proposal than firm plan).

We are open to other minor fixes/enhancements to the Jakarta Batch API from our backlog at: https://github.com/eclipse-ee4j/batch-api/issues

A good deal of the prioritization among these will likely come from the choice of individual committers deciding what to work on.

## It may contain: 

### Standalone TCK refactor to include EE tests

Refactoring of the Batch standalone TCK, so the full suite, including the EE platform portion (which is currently only offered by the platform TCK ), can be run against a Batch implementation to ceritfy Batch compliance.  This would allow the Jakarta Batch project to avoid having to maintain a duplicate "fork" of these tests in the platform TCK.

This is the main TCK-related item, tracked via https://github.com/eclipse-ee4j/batch-tck/milestone/1

## It will also contain:

* Bug fixes as they arise during the release cycle
* Any updates required to meet the Java version requirements of Jakarta EE 10
* Any requirements identified by other specifications or the Jakarta EE 10 platform projects during the release cycle

## Optional Features:

N/A


# Release Record

[Jakarta Batch 2.1 Release Record](https://projects.eclipse.org/projects/ee4j.batch/releases/2.1.0)


# Ballots


## Plan Review

|                       |  Yes    | No  | Abstain  |
|-----------------------|---------|-----|----------|
|Fujitsu                |         |     |          |
|IBM                    |         |     |          |
|Oracle                 |         |     |          |
|Payara                 |         |     |          |
|Red Hat                |         |     |          |
|Tomitribe              |         |     |          |
|EE4J PMC               |         |     |          |
|Participant Members    |         |     |          |
|Committer Members      |         |     |          |