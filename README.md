# job-ingestion-pipeline
This service aggregates and normalizes remote job listings from multiple sources.
Remote job listings are spread across many different sources, so job seekers end up seeing the same listing again and again.
Each source also describes the job listing in its own way.

## Sources
- Remote OK
- Hacker News (monthly hiring thread)
- We Work Remotely

## What it does
- Ingests data from the sources
- Normalizes salary currency, seniority level and actual remote status
- Removes duplicate listings across different sources
- Exposes job openings through a REST API with filtering by seniority, salary range and region

## Status
- Nothing implemented yet, work in progress