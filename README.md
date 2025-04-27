# AWS-Cloudathon
My contribution:
[S3 Bucket - Raw Data]:
Stores unstructured/semi-structured data (e.g., CSV, JSON) in its original form. Acts as the initial data source.
[AWS Glue Crawler]:
Scans raw data, infers schema (column names, data types), and populates the Glue Data Catalog with metadata tables. Enables services like Athena to query S3 data as structured tables[1][2][3].
[AWS Glue Job (Transform)]:
Processes raw data using ETL scripts (Python/Scala). Applies transformations like filtering, joining, or cleaning via managed nodes (e.g., DropFields, RenameField)[4][5][6].
[S3 Processed Data Bucket]:
Stores transformed, analysis-ready data in optimized formats (e.g., Parquet) partitioned for efficient querying.
[Redshift Data Warehouse]:
Loads processed data for analytics, reporting, or BI tools. Uses COPY command or Glue jobs to transfer from S3.
(Sequence: Crawler catalogs structure → ETL job cleans → Processed data stored → Redshift analyzes.)
