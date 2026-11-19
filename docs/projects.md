# Projects

## Selected professional work

These summaries describe work completed in my engineering roles. They focus on my contributions and outcomes; employer source code and datasets are not included.

### Secure data integration

**Oddball Inc. | SQL, C#, SSIS, Amazon S3, Datadog**

I built an ETL pipeline to transform 16 datasets into a vendor-defined format for a medication-management integration. Watermark-based incremental loads supported nightly processing after an initial load of hundreds of gigabytes. I also implemented access permissions, credential rotation, sequential execution, failure notifications, and logging that excluded personal and health information.

The work connected data engineering with security and operations: controlling access, limiting sensitive information in logs, and making recurring processing observable and reliable.

### Search and content ingestion

**Oddball Inc. | React, Ruby on Rails, Python, AWS Kendra, Docker, EKS**

I implemented search functionality for VA.gov and automated content synchronization using AWS services. I validated and sanitized external sitemap content and deployed a containerized Python crawler to publish structured data to S3 for search indexing.

This work reinforced the importance of validating external input throughout an ingestion pipeline, not only at the user interface.

### Event-driven case processing

**Alpha Omega Integration | Kafka, Ruby, SQL, Databricks**

I built ingestion logic that checked incoming data against existing records before creating new cases. Improvements to Ruby validation prevented invalid case creation and increased new-case throughput by 80%. Analysis with Databricks and SQL helped identify bottlenecks and improve ingestion and review speed by 50%.

[See my full engineering experience](experience.md).

## CTF investigation and technical documentation

Through National Cyber League participation and CTF practice, I developed a structured approach to investigating files, logs, network traffic, and application behavior.

I maintain an Obsidian knowledge base that connects investigation notes with reusable techniques and tool references. My notes record hypotheses, observations, unsuccessful attempts, and verification so that I can revisit the reasoning behind a result.

The work combines command-line analysis, browser inspection, small Python scripts, and careful documentation. It has helped me practice turning unfamiliar evidence into focused questions and defensible conclusions.

[Read about the techniques I practiced](ctf-techniques.md).
