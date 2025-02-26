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
- Example: Imagine an inventory system where the stock level for a particular item cannot go below zero. If the current stock level is one and a customer attempts to order two items, the transaction will fail.

### Isolation
- Isolation guarantees that when multiple transactions are executed concurrently, each transaction operates as if it is the only transaction in the system. This means that the intermediate state of a transaction is not visible to other transactions until it is completed.
- Example: Consider a scenario where two customers place orders for the same item at the same time. If the inventory shows that there are 10 items available: Customer A orders 5 items. Customer B also orders 5 items simultaneously. The isolation principle ensures that these transactions are processed independently. If Customer A's transaction is processed first, the inventory will be updated to reflect 5 items remaining. When Customer B's transaction is processed next, it will see that only 5 items are left and can proceed successfully. If Customer B had tried to order 6 items, the transaction would fail, maintaining the integrity of the inventory.

### Durability
- Durability guarantees that completed transactions will survive any subsequent failures, such as power outages, crashes, or other unexpected events. Once a transaction is confirmed, the changes it made to the database are stored in a way that they cannot be lost.
- Example: Imagine a banking system where a customer transfers money from one account to another. Once the transaction is completed and confirmed: The amount is deducted from the sender's account. The amount is added to the recipient's account. If a power failure occurs immediately after the transaction is confirmed, the database will still retain the changes made by the transaction. When the system is restored, the accounts will reflect the correct balances, ensuring that the transaction's effects are preserved.