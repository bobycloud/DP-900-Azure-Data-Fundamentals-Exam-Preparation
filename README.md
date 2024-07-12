# Azure-Data-Fundamentals

# Explore Job Roles in the World of Data

## Overview
There is a wide variety of roles involved in managing, controlling, and using data. Roles can be business-oriented, engineering-focused, research-based, or hybrid. While job titles and responsibilities may vary across organizations, the following roles encapsulate common divisions of tasks and responsibilities.

## Key Job Roles

### Database Administrator (DBA)
- **Responsibilities:**
  - Design, implement, maintain, and manage on-premises and cloud-based databases.
  - Ensure overall availability, performance, and optimization of databases.
  - Implement backup and recovery plans to handle failures and disasters.
  - Manage data security, grant privileges, and control user access.

### Data Engineer
- **Responsibilities:**
  - Collaborate with stakeholders to design and implement data workloads.
  - Develop data ingestion pipelines, cleansing, and transformation activities.
  - Manage data stores for analytical workloads.
  - Ensure data privacy across on-premises and cloud data stores.
  - Monitor data pipelines to ensure expected data loads.

### Data Analyst
- **Responsibilities:**
  - Explore data to identify trends and relationships.
  - Design and build analytical models.
  - Create reports and visualizations to enable advanced analytics capabilities.
  - Transform raw data into relevant insights based on business requirements.

## Additional Notes
- **Hybrid Roles:** In some organizations, a single person may perform multiple roles. For example, a DBA might also create data pipelines as a Data Engineer.
- **Other Roles:** Additional data-related roles not detailed here include Data Scientist and Data Architect. Technical professionals such as application developers and software engineers also work with data.

# Identify Data Formats

## Overview
Data is a collection of facts used to record information, often organized in structures representing entities important to an organization (e.g., customers, products). Entities have attributes (e.g., name, address).

## Data Classifications
Data can be classified as:
- **Structured**
- **Semi-structured**
- **Unstructured**

### Structured Data
- Adheres to a fixed schema.
- Commonly tabular (rows and columns).
- Stored in databases using a relational model.

**Example: Customer and Product tables**

### Semi-structured Data
- Has some structure with variations between instances.
- Common format: JSON.

**Example:**
- Customer documents with varying address and contact information.

*Note: JSON is just one of many semi-structured data representations.*

### Unstructured Data
- No specific structure.
- Includes documents, images, audio, video, and binary files.

## Data Stores
Organizations store data in structured, semi-structured, or unstructured formats for recording details of entities, events, or other information. Stored data is retrieved for analysis and reporting.

### Types of Data Stores
1. **File stores**
2. **Databases**

# Explore File Storage

## Overview
The ability to store data in files is a core element of any computing system. Files can be stored in local file systems, on removable media, or centrally in a shared file storage system, increasingly hosted in the cloud for cost-effective, secure, and reliable storage.

## Factors Influencing File Format Choice
- Type of data (structured, semi-structured, or unstructured)
- Applications and services needing access to the data
- Human readability vs. optimization for storage and processing

## Common File Formats

### Delimited Text Files
- **Format:** Plain text with specific field delimiters and row terminators (e.g., CSV, TSV, space-delimited, fixed-width)
- **Usage:** Structured data accessed by various applications and services in a human-readable format.

### JavaScript Object Notation (JSON)
- **Format:** Hierarchical document schema defining data entities (objects) with multiple attributes.
- **Usage:** Both structured and semi-structured data, flexible for varying attributes.

### Extensible Markup Language (XML)
- **Format:** Human-readable, tag-based.
- **Usage:** Previously popular for structured data, largely replaced by JSON.

### Binary Large Object (BLOB)
- **Format:** Raw binary data, interpreted by applications and rendered.
- **Usage:** Unstructured data such as images, video, audio, and application-specific documents.

## Optimized File Formats
Specialized formats developed for compression, indexing, and efficient storage and processing.

### Avro
- **Type:** Row-based
- **Usage:** Compressing data, minimizing storage and network bandwidth.
- **Features:**
  - **Schema Evolution:** Supports schema changes (e.g., adding new fields) without breaking existing data.
  - **Data Serialization:** Efficiently serializes data for transport and storage.
  - **Interoperability:** Used in data serialization frameworks like Apache Kafka.
  - **Header Information:** Each record contains a header stored as JSON that describes the structure of the data, aiding in parsing binary data.
  - **Integration:** Well-integrated with Hadoop ecosystems and big data tools.

### ORC (Optimized Row Columnar)
- **Type:** Columnar
- **Usage:** Optimizing read and write operations in Apache Hive.
- **Features:**
  - **Columnar Storage:** Organizes data into columns rather than rows, improving query performance.
  - **Stripes:** Divides data into large stripes, each containing an index, data for rows, and a footer with statistical information.
  - **Compression:** Supports lightweight and fast compression techniques like Zlib, LZO, and Snappy.
  - **Predicate Pushdown:** Enhances query performance by allowing queries to skip non-relevant data.
  - **Complex Types:** Efficiently handles complex data types and nested structures.

### Parquet
- **Type:** Columnar
- **Usage:** Efficient storage and processing of nested data types.
- **Features:**
  - **Row Groups:** Data is divided into row groups. Each row group contains data for a certain number of rows.
  - **Column Chunks:** Within each row group, data is stored in column chunks. Each column chunk contains data for a single column across multiple rows.
  - **Metadata:** Includes rich metadata that describes the structure of the data, allowing for efficient data retrieval.
  - **Compression:** Supports efficient compression and encoding schemes, reducing storage space and improving read/write performance.
  - **Nested Data Structures:** Optimized for complex nested data structures, making it suitable for big data processing frameworks like Apache Spark and Hadoop.
  - **Data Encoding:** Utilizes different encoding techniques for different data types to enhance storage efficiency.

# Explore Databases

## Overview
A database is a central system used to store and query data records. Unlike file systems, databases are dedicated to managing data records efficiently.

## Relational Databases
- **Usage:** Store and query structured data.
- **Structure:** Data is stored in tables representing entities (e.g., customers, products, sales orders).
- **Primary Keys:** Unique identifiers for each entity instance, used to reference entities in other tables.
- **Normalization:** Elimination of duplicate data values, ensuring data is stored only once.
- **Query Language:** Managed and queried using Structured Query Language (SQL), based on ANSI standard.

**Example:** A customer's primary key referenced in a sales order to indicate which customer placed the order.

### Key Features
- **Tables:** Represent entities.
- **Primary Keys:** Unique identifiers.
- **Normalization:** Reduces duplicate data.
- **SQL:** Standard query language.

## Non-relational Databases
Non-relational databases, also known as NoSQL databases, do not use a relational schema. They are categorized into four common types:

### Key-value Databases
- **Structure:** Each record consists of a unique key and an associated value.
- **Flexibility:** Value can be in any format.

**Example:** Key-value pairs where the value could be text, JSON, or any other format.

### Document Databases
- **Structure:** A form of key-value database where the value is a JSON document.
- **Optimization:** Optimized for parsing and querying JSON documents.

**Example:** Storing customer information as JSON documents.

### Column Family Databases
- **Structure:** Store tabular data with rows and columns.
- **Column Families:** Columns are grouped into families that are logically related.

**Example:** A database storing user profiles, with column families for personal info and activity logs.

### Graph Databases
- **Structure:** Store entities as nodes with links (edges) defining relationships between them.
- **Usage:** Ideal for complex relationships and interconnected data.

**Example:** A social network database where users are nodes and friendships are edges.

# Explore Transactional Data Processing

## Overview
A transactional data processing system records transactions, which are discrete units of work encapsulating specific events an organization wants to track. Transactions can be financial, retail, or other types of business activities.

## Characteristics of Transactional Systems
- **High Volume:** Often handle millions of transactions per day.
- **Speed:** Data must be quickly accessible.
- **Transactional Processing:** Known as Online Transactional Processing (OLTP).

## OLTP Solutions
OLTP solutions use a database system optimized for both read and write operations to support transactional workloads involving CRUD operations (Create, Retrieve, Update, Delete). These operations must ensure data integrity through ACID semantics:

### ACID Semantics
- **Atomicity:** Each transaction is a single unit that either fully succeeds or fully fails.
  - Example: A funds transfer transaction must debit one account and credit another completely or not at all.
- **Consistency:** Transactions take the database from one valid state to another.
  - Example: A completed funds transfer must accurately reflect in both accounts involved.
- **Isolation:** Concurrent transactions do not interfere with each other.
  - Example: While a funds transfer is in process, other transactions must return consistent account balances.
- **Durability:** Committed transactions are permanently recorded.
  - Example: Once a funds transfer is committed, it remains recorded even if the system is turned off.

## Usage of OLTP Systems
OLTP systems support live applications that process business data, often referred to as line of business (LOB) applications.

# Explore Analytical Data Processing

## Overview
Analytical data processing uses read-only (or read-mostly) systems to store vast volumes of historical data or business metrics. Analytics can be based on snapshots of data at given points in time or a series of snapshots.

## Common Architecture for Enterprise-Scale Analytics
1. **ETL Process:** Operational data is extracted, transformed, and loaded into a data lake for analysis.
2. **Data Loading:** Data is loaded into a schema of tables, typically in a Spark-based data lakehouse or a data warehouse.
3. **Aggregation:** Data in the data warehouse is aggregated and loaded into an OLAP model or cube. Measures from fact tables are calculated for intersections of dimensions from dimension tables.
4. **Querying:** The data in the data lake, data warehouse, and analytical model can be queried to produce reports, visualizations, and dashboards.

## Key Components

### Data Lakes
- **Usage:** Collect and analyze large volumes of file-based data.
- **Scalability:** Flexible and scalable storage for large-scale data.

### Data Warehouses
- **Usage:** Store data in a relational schema optimized for read operations.
- **Optimization:** Primarily supports queries for reporting and data visualization.

### Data Lakehouses
- **Usage:** Combine the flexible storage of a data lake with the relational querying of a data warehouse.
- **Innovation:** Newer approach integrating the best of data lakes and data warehouses.

### OLAP Model
- **Usage:** Optimized for analytical workloads.
- **Aggregation:** Pre-aggregated data across dimensions at different levels, enabling drill-up/down functionality.
- **Performance:** Queries return summaries quickly due to pre-aggregation.

## Roles in Data Analytical Work
- **Data Scientists:** Work directly with data files in a data lake to explore and model data.
- **Data Analysts:** Query tables in the data warehouse to produce complex reports and visualizations.
- **Business Users:** Consume pre-aggregated data in analytical models via reports or dashboards.

# Identify Data Services

## Overview
Microsoft Azure is a cloud platform supporting various data services for transactional and analytical workloads. This guide covers some of the most commonly used data services.

## Commonly Used Data Services

### Azure SQL
- **Services:**
  - **Azure SQL Database:** Fully managed PaaS database.
  - **Azure SQL Managed Instance:** Hosted SQL Server instance with automated maintenance.
  - **Azure SQL VM:** Virtual machine with SQL Server for maximum configurability.
- **Usage:** Support LOB applications, data sources for ETL operations, direct querying for reports.

### Azure Database for Open-Source Relational Databases
- **Services:**
  - **Azure Database for MySQL**
  - **Azure Database for MariaDB**
  - **Azure Database for PostgreSQL**
- **Usage:** Support transactional applications, data sources for ETL operations, direct querying for reports.

### Azure Cosmos DB
- **Type:** Global-scale NoSQL database.
- **APIs Supported:** JSON documents, key-value pairs, column-families, graphs.
- **Usage:** Managed by database administrators or software developers, integrated into enterprise analytical solutions.

### Azure Storage
- **Storage Options:**
  - **Blob Containers:** Scalable, cost-effective storage for binary files.
  - **File Shares:** Network file shares.
  - **Tables:** Key-value storage for quick data access.
- **Usage:** Hosting data lakes with hierarchical namespaces for organized data storage.

### Azure Data Factory
- **Function:** Define and schedule data pipelines for data transfer and transformation.
- **Usage:** Build ETL solutions to populate analytical data stores from transactional systems.

### Azure Synapse Analytics
- **Features:**
  - **Pipelines:** Similar to Azure Data Factory.
  - **SQL:** Scalable SQL database engine for data warehousing.
  - **Apache Spark:** Distributed data processing system.
  - **Data Explorer:** High-performance querying of log and telemetry data.
- **Usage:** Unified data analytics solution combining data ingestion, data warehouse, and data lake storage.

### Azure Databricks
- **Integration:** Azure-integrated Databricks platform combining Apache Spark and SQL database semantics.
- **Usage:** Large-scale data analytics, interactive notebooks for querying and visualizing data.

### Azure HDInsight
- **Supported Technologies:**
  - **Apache Spark:** A distributed data processing system that supports multiple programming languages and APIs, including Java, Scala, Python, and SQL.
  - **Apache Hadoop:** A distributed system that uses MapReduce jobs to process large volumes of data efficiently across multiple cluster nodes. MapReduce jobs can be written in Java or abstracted by interfaces such as Apache Hive - a SQL-based API that runs on Hadoop.
  - **Apache HBase:** An open-source system for large-scale NoSQL data storage and querying.
  - **Apache Kafka:** A message broker for data stream processing.
- **Usage:** Support big data analytics workloads with multiple open-source technologies.

### Azure Stream Analytics
- **Function:** Real-time stream processing engine.
- **Usage:** Capture streaming data for ingestion into analytical data stores or real-time visualization.

### Azure Data Explorer
- **Function:** High-performance querying of log and telemetry data.
- **Usage:** Query and analyze timestamped data such as log files and IoT telemetry data.

### Microsoft Purview
- **Function:** Enterprise-wide data governance and discoverability.
- **Usage:** Create data maps, track data lineage, enforce data governance, ensure data integrity for analytical workloads.

### Microsoft Fabric
- **Function:** Unified SaaS analytics platform.
- **Features:**
  - Data ingestion and ETL
  - Data lakehouse analytics
  - Data warehouse analytics
  - Data science and machine learning
  - Real-time analytics
  - Data visualization
  - Data governance and management

# Understand Relational Data

## Overview
In a relational database, collections of entities from the real world are modeled as tables. An entity can be anything for which you want to record information, typically important objects and events.

## Key Concepts

### Entities and Tables
- **Entities:** Represent real-world objects or events (e.g., customers, products, orders).
- **Tables:** Model collections of entities. Each table contains rows, with each row representing a single instance of an entity.

**Example:**
- **Customer Table:** Each row contains data for a single customer.
- **Product Table:** Each row defines a single product.
- **Order Table:** Each row represents an order made by a customer.
- **Line Item Table:** Each row represents a product included in an order.

### Columns and Data Types
- **Columns:** Define attributes of the entity. Each row in a table has the same columns, though not all columns need to have a value (can be NULL).
- **Data Types:** Each column stores data of a specific datatype.

**Common Data Types:**
- **Text Data:** Character-based (fixed or variable length) for columns like `Email`.
- **Numeric Data:** Decimal or integer values for columns like `Price` or `Quantity`.
- **Date/Time Data:** Date and time values for columns like `OrderDate`.

### Standard Datatypes
- Most database systems support standard datatypes defined by the American National Standards Institute (ANSI).

## Example Scenario
In a retail system:
- **Customer Table:** Contains customer details such as `FirstName`, `LastName`, `Email`, `MiddleName`.
- **Product Table:** Contains product details such as `ProductID`, `ProductName`, `Price`.
- **Order Table:** Contains order details such as `OrderID`, `CustomerID`, `OrderDate`.
- **Line Item Table:** Contains line items within an order such as `OrderID`, `ProductID`, `Quantity`.

# Understand Normalization

## Overview
Normalization is a schema design process that minimizes data duplication and enforces data integrity in a database.

## Core Principles of Normalization
1. **Separate each entity into its own table.**
2. **Separate each discrete attribute into its own column.**
3. **Uniquely identify each entity instance (row) using a primary key.**
4. **Use foreign key columns to link related entities.**

## Example Scenario

### Un-normalized Data
- **Issues:** 
  - Data duplication.
  - Combined customer and product details in the same cells.

### Normalized Data
- **Changes:**
  - Each entity (e.g., customer, product, sales order, line item) is stored in its own table.
  - Each attribute is in its own column.
  - Primary keys uniquely identify rows.
  - Foreign keys link related entities.

### Benefits of Normalization
- **Reduces Duplication:** Modifying a customer's address requires changing a single row.
- **Ensures Data Integrity:** Values are constrained to appropriate data types.
- **Granularity:** Allows detailed querying (e.g., filtering customers by city).
- **Referential Integrity:** RDBMS enforces that foreign key values exist in the related table (e.g., no orders for non-existent customers).

### Composite Keys
- **Usage:** Unique combination of multiple columns to identify rows.
- **Example:** LineItem table uses a combination of `OrderNo` and `ItemNo` to identify a line item in an order.

