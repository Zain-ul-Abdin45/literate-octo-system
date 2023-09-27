# Introduction

Data modeling is a technique used to define and organize your business processes. It allows you to create a visual description of your business by analyzing, understanding, and clarifying your data requirements and how they underpin your business processes. Data models inform your data architecture, database design, and restructuring legacy systems.

Data modeling helps solve for these challenges so you can:

- **Relationships between Data**
- **Logical & Efficient Database Structure** 
- **Understanding of Data Structure throughput Systems**
- **Maintain And Scale**

# Data Model Types

## Conceptual Model

A conceptual data model is a simple, high-level representation of the data in your organization defined according to business requirements. It focuses on business-oriented attributes, entries, and relationships, independent of any specific technology or database management system. It caters to a specific business audience and defines the key concepts and relationships between the elements in a domain.

For Example:

### Entities:
- Customer
- Account
- Transaction
- CreditCardLoan
- Investment

### Relationships:
- A customer can have one or more accounts, credit card loans, and investments.
- An account can have one or more transactions.
- A credit card loan is associated with a single customer.
- An investment is associated with a single customer.

![Conceptual Model](https://github.com/Zain-ul-Abdin45/literate-octo-system/assets/47116254/272eb941-5fcf-4db7-ba1b-db0e13480112)

## Logical Model

A logical data model is a more complex representation of the data structures and relationships within a system or your organization. It defines the entities, attributes, and relationships that make up the data, but does not specify the physical storage or implementation details. Logical models are used to communicate the conceptual design of a system to stakeholders and to guide the development of the physical data model and database. In agile DevOps or DataOps practices, this phase is sometimes skipped.

For Example:

### Entities:
- Customer (customer_id, name, email, address)
- Product (product_id, name, price, description)
- Order (order_id, customer_id, order_date, order_status)
- Order Item (order_item_id, order_id, product_id, quantity)

### Relationships:
- One customer can place one or more orders.
- One order can contain one or more order items.
- One order item is associated with a single product.

## Physical Model

A physical data model is a detailed representation of a database design that includes information about the specific data types, sizes, and constraints of each field, as well as the relationships between tables and other database objects. It also includes information about the physical storage of your data, such as the location of files and the use of indexes and other performance optimization techniques. The physical model is used to guide the actual implementation of a database and is therefore specific to the DBMS or application software you implement.
