# Wrenchie Backend Project Charter

## Background

Wrenchie Mechanics customer acquisition and retention is declining since 2008.
This trend is due to competitors being more favorable
across the company's target group.
Profitability has been severely impacted.
Wrenchie Mechanics is yet to turn profitable since the end of 2018.

To stay competitive it was decided that a web application is required.
This was agreed upon by management in document
Wrenchie Web Application Project Charter.
<!-- Link needed: referenced project charter -->

## Problem statement

A backend is required by Wrenchie Web Application, more specifically by the frontend.

## Solution proposal

A backend shall be designed, implemented, and delivered
matching the parameters set forth by this document.

## Objectives

- Backend is able to handle up to 1000 parallel connections
with the following characteristics
  - Latency average is under 400 ms
  - Network error rate is under 5% of total requests
  - Application error rate is under 1% of total requests

## Stakeholders

### Attila Viniczai

Roles:

- product owner
- software developer

## Budget

|     Scope                 |     Budget           |
| :------------------------ | :------------------- |
| API design                | 40 man-hours         |
| Backend implementation    | 160 man-hours        |
| Operation and maintenance | 20 man-hours / month |
| Developer tools           | 0$ (have fun!)       |
| Hosting                   | 0$ (do ads)          |

## Deliverables

<!--
Note: it would be nicer to have a user story map,
however this is not feasible due to a lack of royalty-free tooling
-->

- User stories
- Requirements document
- API schema
- Deployed, working backend
- Operation and maintenance instructions document

## Milestones

|     Task                      |   Deadline    |
| :---------------------------- | :------------ |
| MVP user stories created      | 2021.03.12    |
| Glossary first draft complete | 2021.03.12    |
| API schema complete           | 2021.03.12    |
| Backend deployed              | to be decided |
| Backend validated             | to be decided |

## Constraints

- Limited developer capacity due to tight budget
- Short deadline
- No hosting budget
- Backend should be hosted by a public cloud service provider
due to lacking knowledge and resource

## Risks

- Merger or acquisition by external company
- [Bus factor][bus-factor-wiki] of 1

## Assumptions

- Licensed developer tools are not required
- Hosting costs can be covered by third-party ads

## Dependencies

- Wrenchie frontend requirements

<!-- Links -->
[bus-factor-wiki]: https://en.wikipedia.org/wiki/Bus_factor
