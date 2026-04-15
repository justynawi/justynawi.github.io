---
title: Global Music Scene
excerpt: "Global music scenes through structured, non-commercial data insights."
image: /images/chocolate-chip-cookies-lg.jpg
thumbnail: /images/chocolate-chip-cookies-400x200.jpg
---

Case Study
Designed and delivered a Power BI analytical solution that transformed fragmented open music data into a structured decision-support product for global comparative analysis. The dashboard examined music activity across countries and regions between 1995 and 2025, enabling users to assess scene scale, participation intensity, live event distribution, stylistic patterns, and ensemble longevity without relying on commercial metrics such as sales, charts, or streaming.
Business Context
The main challenge was not visualization, but building analytical credibility on top of imperfect open data.
MusicBrainz provided broad global coverage across artists, releases, recordings, and live events, but the data was uneven in quality and completeness. Geographic coverage varied by country, metadata depth differed by entity, and some fields were incomplete or not reliable enough for direct reporting. The project required a reporting layer that could support meaningful comparison despite those limitations.
The dashboard was designed for researchers, analysts, and policy-oriented stakeholders who needed a structural view of music ecosystems rather than a popularity-driven one.
Objective
The objective was to create an interactive analytical product that answers three core questions:
Where is global music activity concentrated?
Which countries outperform when adjusted for population size?
How do local music scenes differ in live activity, genre structure, and long-term stability?
The solution was intended to provide a single analytical layer for comparing music ecosystems across geography, time, and subject area, while preserving metric consistency and interpretability.
Data and Engineering
I owned the solution end to end:
data preparation in PostgreSQL
SQL-based analytical table design
data shaping in Power Query
semantic model design
DAX measure development
report UX and navigation architecture
KPI definition and analytical framing
The solution combined:
MusicBrainz open data
ISO-based country and region mapping
population data for per-capita normalization
Key reporting domains included:
artists
releases
recordings
live events
ended ensembles for longevity analysis
To keep the reporting layer focused and performant, I used PostgreSQL as a preparation layer before loading curated datasets into Power BI. I profiled the MusicBrainz structure, identified subject areas and relationships relevant to the analytical scope, and built SQL-based analytical tables aligned to each reporting domain. This separation reduced semantic model complexity and improved maintainability.
Rather than forcing a textbook star schema, I designed a hybrid dimensional model with shared conformed dimensions such as Date and Country, supported by multiple subject-area fact-like tables. This approach better matched the analytical problem: it preserved flexibility across reporting domains while keeping metric logic consistent and manageable in DAX.
Power Query transformation included:
standardized ISO and geographic mappings
aligned country and year logic across subject areas
merged population data for normalized KPIs
filtered analytical windows by reporting domain
excluded low-value or unreliable fields from reporting logic
created helper tables for metric switching, labels, and usability
The DAX layer included measures for:
total artists, releases, recordings, events and ensembles
artists and releases per 1M residents
ranking and Top N analysis
genre share and average genre tags per recording
average, median, and bucketed career length
dynamic titles, metric toggles, tooltips, and context-aware comparisons
Report
The final report was structured into six focused pages:
Overview for global concentration of artists and releases
Participation for artists and releases per 1M residents
Recordings for recording volume and tagging density
Genre Trends for stylistic patterns by geography and over time
Events for live music distribution by type and location
Longevity for career length analysis across ensemble types and regions
Core KPIs included:
337K total artists
4M total releases
84K distinct live events
124K recordings analyzed for 2020-2025
8K distinct genre tags
The UX was designed for guided exploration, with page-level navigation, time-range filtering, region and genre slicers, metric switching, dynamic titles, and visuals that compared absolute scale against normalized intensity.
Business Outcome
The dashboard turned open structural data into a practical tool for comparative analysis of music ecosystems across countries and regions. By combining volume-based, normalized, and activity-focused indicators, it helped reveal patterns that would remain hidden in raw totals alone, such as the strong per-capita performance of smaller developed markets and the persistent concentration of music activity in Europe and North America. Beyond descriptive analysis, the solution created a foundation for more informed cultural decision-making by helping identify mature scenes, emerging regions, and areas that may require closer strategic attention.
Key Takeaways
This project shows how Power BI can be used as a full analytical solution, not just a reporting tool. The value of the solution was not limited to presenting existing patterns, but to creating a framework that supports strategic reflection and inspires further research. By designing trustworthy KPIs on top of imperfect open data, the dashboard became both an analytical product and a starting point for deeper investigation, including future extensions into cultural funding, market data, gender-based analysis, and more granular city- or metro-level perspectives.



