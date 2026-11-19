# Engineering Experience

I am a software engineer focused on security, with experience building web applications, APIs, and data pipelines since 2022. My work supporting government organizations connects application development with input validation, access control, reliable delivery, and responsible handling of sensitive data.

## Oddball Inc.

**Software Engineer | August 2025–Present**

I build and maintain data integration and search capabilities supporting the Department of Veterans Affairs.

- Designed and built an SSIS ETL pipeline using SQL and C# to transform 16 datasets into vendor-defined CSV schemas in Amazon S3. The pipeline processed hundreds of gigabytes during the initial load and several gigabytes nightly using watermark-based incremental loads.
- Implemented access permissions and credential rotation aligned with VA security policy. Added sequential job execution, automated failure notifications, and Datadog logging that excluded personally identifiable information and protected health information.
- Implemented VA.gov search functionality with React and JavaScript, integrating AWS Kendra with Ruby on Rails backend services and applying secure coding practices.
- Automated recurring data synchronization with S3, Lambda, RDS, and Kendra, using Git and CI/CD workflows to support reliable changes and secure access patterns.
- Validated and sanitized external sitemap content before ingestion, and deployed a Python crawler with Docker and AWS EKS to publish structured content to S3.

## Alpha Omega Integration

**Fullstack Software Engineer | October 2023–August 2025**

I worked on backend validation, data ingestion, and application delivery for case-processing systems.

- Engineered Kafka-based ingestion that cross-referenced incoming data with existing database records to validate and create cases.
- Optimized Ruby validation logic to prevent invalid case creation and increase throughput of new cases by 80%.
- Used Databricks and SQL to identify workflow bottlenecks and improve ingestion and review speed by 50%.
- Evaluated Docker-based application workflows within CI/CD pipelines to improve build consistency and deployment reliability across development and testing.

## Sev1Tech LLC

**Front-End Software Engineer | August 2022–October 2023**

My work spanned user interfaces, API integration, and automated delivery for government applications.

- Developed a Rails API to process Kafka payloads and transform data for integration with an existing USCIS API.
- Collaborated with teams across government agencies on data pipelines that increased screening efficiency for Investigating Officers by 400%.
- Built React interfaces using JavaScript, HTML, and CSS, integrated them with backend services, and maintained Section 508 accessibility compliance.
- Delivered application updates through Git-based CI/CD pipelines.

## Technical skills

| Area | Technologies and practices |
|---|---|
| Languages | JavaScript, TypeScript, Ruby, Python; SQL and C# for data integration |
| Application development | React, Node.js, Express, Ruby on Rails, API integration |
| Data | PostgreSQL, MySQL, Redis, Kafka, Databricks, SSIS |
| Cloud and delivery | AWS, Docker, EKS, Terraform, Git, CI/CD |
| Application security | Authentication, authorization, input validation, secure coding, OWASP Top 10 |
| Security analysis | Wireshark, Nmap, Burp Suite, network security, incident handling, threat detection |

My [CTF experience](ncl-fall-2026.md) and [technique notes](ctf-techniques.md) show how I am extending this engineering background into security investigation.

[Connect with me on LinkedIn](https://www.linkedin.com/in/dwightdoran).
