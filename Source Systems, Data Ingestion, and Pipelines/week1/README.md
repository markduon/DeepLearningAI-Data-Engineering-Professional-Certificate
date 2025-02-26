# Introduction to Source system
## Data Types

### Structured Data
- Organized in tables with rows and columns.
- Commonly found in spreadsheets and relational databases.

### Semi-Structured Data
- Not in tabular form but has some inherent structure.
- Examples include **JSON** (JavaScript Object Notation), which uses key-value pairs.

### Unstructured Data
- Lacks a predefined structure.
- Includes text, video, audio, and images.

---

## Source Systems for Data Ingestion

### Databases
- Store data in an organized manner, supporting **CRUD** operations (Create, Read, Update, Delete).
- Types:
  - **Relational databases**: Tabular format (e.g., MySQL, PostgreSQL).
  - **Non-relational (NoSQL) databases**: Flexible schemas for unstructured or semi-structured data (e.g., MongoDB, Cassandra).

### Files
- Can be structured (CSV, Excel), semi-structured (JSON, XML), or unstructured (PDF, TXT).
- Serve as a universal medium for data exchange.

### Streaming Systems
- Provide a continuous flow of real-time data.
- Examples include IoT devices sending sensor data (e.g., temperature readings) or event-driven platforms like Apache Kafka.

## Database ACID Compliance
### Atomicity
- Atomicity guarantees that all operations within a transaction are completed successfully or none at all. If any part of the transaction fails, the entire transaction is rolled back, leaving the database in its original state.
- Example: A customer is placing an order that involves 2 operations: Deducting total cost from customer's account & Updating inventory to reflect purchased items. If an error occurs after the cost is deducted but before inventory is updated, atomicity ensures that the deduction is reversed, and customer is not charged.

### Consistency
- Consistency guarantees that any changes made to the database during a transaction must adhere to predefined rules or constraints set by the database schema. This means that the database will only transition from one valid state to another.
- Example: 