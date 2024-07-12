# Azure-Data-Fundamentals

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

---
